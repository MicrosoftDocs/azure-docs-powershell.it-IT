---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/powershell/module/az.attestation/new-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
ms.openlocfilehash: 1fbb3c5d1a82261f5c25bd4351aabcb838355bda
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998240"
---
# <span data-ttu-id="5d389-101">New-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="5d389-101">New-AzAttestation</span></span>

## <span data-ttu-id="5d389-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d389-102">SYNOPSIS</span></span>
<span data-ttu-id="5d389-103">Crea una attestazione</span><span class="sxs-lookup"><span data-stu-id="5d389-103">Creates an attestation</span></span>

## <span data-ttu-id="5d389-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5d389-104">SYNTAX</span></span>

```
New-AzAttestation -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-PolicySignersCertificateFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5d389-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5d389-105">DESCRIPTION</span></span>
<span data-ttu-id="5d389-106">Il New-AzAttestation cmdlet crea un'attestazione nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="5d389-106">The New-AzAttestation cmdlet creates an attestation in the specified resource group.</span></span>

## <span data-ttu-id="5d389-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5d389-107">EXAMPLES</span></span>

### <span data-ttu-id="5d389-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5d389-108">Example 1</span></span>
```powershell
PS C:\> New-AzAttestation -Name pshtest4 -ResourceGroupName psh-test-rg -Location "East US" -Tags @{Test="true";CreationYear="2020"}                                                                                                                                                                                         
Id                : subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/psh-test-rg/providers/Microsoft.Attestation/attestationProviders/pshtest4
Location          : East US
ResourceGroupName : psh-test-rg
Name              : pshtest4
Status            : Ready
TrustModel        : AAD
AttestUri         : https://pshtest4.us.attest.azure.net
Tags              : {CreationYear, Test}
TagsTable         :
                    Name          Value
                    ============  =====
                    CreationYear  2020
                    Test          true
```

<span data-ttu-id="5d389-109">Creare una nuova istanza di un provider di attestazioni denominato *pshtest4* con un paio di tag e usando l'attendibilità AAD per padroneggiare i criteri di TEE.</span><span class="sxs-lookup"><span data-stu-id="5d389-109">Create a new instance of an Attestation Provider named *pshtest4* with a couple tags and using AAD trust for mastering TEE policy.</span></span>

### <span data-ttu-id="5d389-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="5d389-110">Example 2</span></span>
```powershell
PS C:\> New-AzAttestation -Name pshtest3 -ResourceGroupName psh-test-rg -Location "East US" -PolicySignersCertificateFile .\cert1.pem                                                                                                                                                
Id                : subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/psh-test-rg/providers/Microsoft.Attestation/attestationProviders/pshtest3
Location          : East US
ResourceGroupName : psh-test-rg
Name              : pshtest3
Status            : Ready
TrustModel        : Isolated
AttestUri         : https://pshtest3.us.attest.azure.net
Tags              :
TagsTable         :
```

<span data-ttu-id="5d389-111">Creare una nuova istanza di un provider di certificati denominato *pshtest3*' che usa l'attendibilità isolata per la gestione dei criteri di TEE specificando un set di chiavi di firma attendibili tramite un file PEM.</span><span class="sxs-lookup"><span data-stu-id="5d389-111">Create a new instance of an Attestation Provider named *pshtest3*\` that uses Isoladed trust for mastering TEE policy via specifying a set of trusted signing keys via a PEM file.</span></span>

## <span data-ttu-id="5d389-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d389-112">PARAMETERS</span></span>

### <span data-ttu-id="5d389-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d389-113">-DefaultProfile</span></span>
<span data-ttu-id="5d389-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5d389-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d389-115">-Location</span><span class="sxs-lookup"><span data-stu-id="5d389-115">-Location</span></span>
<span data-ttu-id="5d389-116">Specifica l'area geografica di Azure in cui creare il provider di attestazione.</span><span class="sxs-lookup"><span data-stu-id="5d389-116">Specifies the Azure region in which to create the attestation provider.</span></span> <span data-ttu-id="5d389-117">Usare il comando Get-AzResourceProvider con il parametro ProviderNtassi per visualizzare le opzioni disponibili.</span><span class="sxs-lookup"><span data-stu-id="5d389-117">Use the command Get-AzResourceProvider with the ProviderNamespace parameter to see your choices.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d389-118">-Name</span><span class="sxs-lookup"><span data-stu-id="5d389-118">-Name</span></span>
<span data-ttu-id="5d389-119">Specifica un nome dell'istanza da creare.</span><span class="sxs-lookup"><span data-stu-id="5d389-119">Specifies a name of the Instance to create.</span></span>
<span data-ttu-id="5d389-120">Il nome può essere qualsiasi combinazione di lettere, cifre o trattini.</span><span class="sxs-lookup"><span data-stu-id="5d389-120">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="5d389-121">Il nome deve iniziare e terminare con una lettera o una cifra.</span><span class="sxs-lookup"><span data-stu-id="5d389-121">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="5d389-122">Il nome deve essere universalmente univoco.</span><span class="sxs-lookup"><span data-stu-id="5d389-122">The name must be universally unique.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d389-123">-PolicySignersCertificateFile</span><span class="sxs-lookup"><span data-stu-id="5d389-123">-PolicySignersCertificateFile</span></span>
<span data-ttu-id="5d389-124">Specifica il set di chiavi di firma attendibili per i criteri di rilascio in un unico file di certificato.</span><span class="sxs-lookup"><span data-stu-id="5d389-124">Specifies the set of trusted signing keys for issuance policy in a single certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d389-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d389-125">-ResourceGroupName</span></span>
<span data-ttu-id="5d389-126">Specifica il nome di un gruppo di risorse esistente in cui creare l'attestazione.</span><span class="sxs-lookup"><span data-stu-id="5d389-126">Specifies the name of an existing resource group in which to create the attestation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d389-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="5d389-127">-Tag</span></span>
<span data-ttu-id="5d389-128">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="5d389-128">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d389-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d389-129">-Confirm</span></span>
<span data-ttu-id="5d389-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d389-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d389-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d389-131">-WhatIf</span></span>
<span data-ttu-id="5d389-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5d389-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d389-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5d389-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d389-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d389-134">CommonParameters</span></span>
<span data-ttu-id="5d389-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d389-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d389-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5d389-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d389-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="5d389-137">INPUTS</span></span>

### <span data-ttu-id="5d389-138">System.String</span><span class="sxs-lookup"><span data-stu-id="5d389-138">System.String</span></span>

### <span data-ttu-id="5d389-139">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="5d389-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5d389-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5d389-140">OUTPUTS</span></span>

### <span data-ttu-id="5d389-141">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span><span class="sxs-lookup"><span data-stu-id="5d389-141">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="5d389-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="5d389-142">NOTES</span></span>

## <span data-ttu-id="5d389-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5d389-143">RELATED LINKS</span></span>
