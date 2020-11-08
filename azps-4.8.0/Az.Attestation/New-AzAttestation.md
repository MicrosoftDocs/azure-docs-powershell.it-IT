---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/new-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
ms.openlocfilehash: c9295883035ca7c53742fc9cb6d1b2e9a800eb3f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033554"
---
# <span data-ttu-id="22560-101">New-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="22560-101">New-AzAttestation</span></span>

## <span data-ttu-id="22560-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="22560-102">SYNOPSIS</span></span>
<span data-ttu-id="22560-103">Crea un attestato</span><span class="sxs-lookup"><span data-stu-id="22560-103">Creates an attestation</span></span>

## <span data-ttu-id="22560-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="22560-104">SYNTAX</span></span>

```
New-AzAttestation -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-PolicySignersCertificateFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="22560-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22560-105">DESCRIPTION</span></span>
<span data-ttu-id="22560-106">Il cmdlet New-AzAttestation crea una attestazione nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="22560-106">The New-AzAttestation cmdlet creates an attestation in the specified resource group.</span></span>

## <span data-ttu-id="22560-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="22560-107">EXAMPLES</span></span>

### <span data-ttu-id="22560-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="22560-108">Example 1</span></span>
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

<span data-ttu-id="22560-109">Creare una nuova istanza di un provider di attestazioni denominato *pshtest4* con un paio di tag e usare l'attendibilità AAD per i criteri di mastering tee.</span><span class="sxs-lookup"><span data-stu-id="22560-109">Create a new instance of an Attestation Provider named *pshtest4* with a couple tags and using AAD trust for mastering TEE policy.</span></span>

### <span data-ttu-id="22560-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="22560-110">Example 2</span></span>
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

<span data-ttu-id="22560-111">Creare una nuova istanza di un provider di attestazioni denominato *pshtest3* ' che usa Isoladed trust per la Mastering Tee Policy tramite la specifica di un set di chiavi di firma attendibili tramite un file PEM.</span><span class="sxs-lookup"><span data-stu-id="22560-111">Create a new instance of an Attestation Provider named *pshtest3* \` that uses Isoladed trust for mastering TEE policy via specifying a set of trusted signing keys via a PEM file.</span></span>

## <span data-ttu-id="22560-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="22560-112">PARAMETERS</span></span>

### <span data-ttu-id="22560-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22560-113">-DefaultProfile</span></span>
<span data-ttu-id="22560-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="22560-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22560-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="22560-115">-Location</span></span>
<span data-ttu-id="22560-116">Specifica l'area di Azure in cui creare il provider di attestazioni.</span><span class="sxs-lookup"><span data-stu-id="22560-116">Specifies the Azure region in which to create the attestation provider.</span></span> <span data-ttu-id="22560-117">Usa il comando Get-AzResourceProvider con il parametro ProviderNamespace per visualizzare le tue scelte.</span><span class="sxs-lookup"><span data-stu-id="22560-117">Use the command Get-AzResourceProvider with the ProviderNamespace parameter to see your choices.</span></span>

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

### <span data-ttu-id="22560-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="22560-118">-Name</span></span>
<span data-ttu-id="22560-119">Specifica un nome dell'istanza da creare.</span><span class="sxs-lookup"><span data-stu-id="22560-119">Specifies a name of the Instance to create.</span></span>
<span data-ttu-id="22560-120">Il nome può essere costituito da qualsiasi combinazione di lettere, cifre o trattini.</span><span class="sxs-lookup"><span data-stu-id="22560-120">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="22560-121">Il nome deve iniziare e terminare con una lettera o una cifra.</span><span class="sxs-lookup"><span data-stu-id="22560-121">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="22560-122">Il nome deve essere universalmente univoco.</span><span class="sxs-lookup"><span data-stu-id="22560-122">The name must be universally unique.</span></span>

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

### <span data-ttu-id="22560-123">-PolicySignersCertificateFile</span><span class="sxs-lookup"><span data-stu-id="22560-123">-PolicySignersCertificateFile</span></span>
<span data-ttu-id="22560-124">Specifica il set di chiavi di firma attendibili per i criteri di rilascio in un singolo file di certificato.</span><span class="sxs-lookup"><span data-stu-id="22560-124">Specifies the set of trusted signing keys for issuance policy in a single certificate file.</span></span>

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

### <span data-ttu-id="22560-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22560-125">-ResourceGroupName</span></span>
<span data-ttu-id="22560-126">Specifica il nome di un gruppo di risorse esistente in cui creare l'attestazione.</span><span class="sxs-lookup"><span data-stu-id="22560-126">Specifies the name of an existing resource group in which to create the attestation.</span></span>

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

### <span data-ttu-id="22560-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="22560-127">-Tag</span></span>
<span data-ttu-id="22560-128">Tabella hash che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="22560-128">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="22560-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="22560-129">-Confirm</span></span>
<span data-ttu-id="22560-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22560-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22560-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22560-131">-WhatIf</span></span>
<span data-ttu-id="22560-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="22560-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22560-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="22560-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22560-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22560-134">CommonParameters</span></span>
<span data-ttu-id="22560-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22560-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22560-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22560-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22560-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="22560-137">INPUTS</span></span>

### <span data-ttu-id="22560-138">System. String</span><span class="sxs-lookup"><span data-stu-id="22560-138">System.String</span></span>

### <span data-ttu-id="22560-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="22560-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="22560-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="22560-140">OUTPUTS</span></span>

### <span data-ttu-id="22560-141">Microsoft. Azure. Commands. Attestation. Models. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="22560-141">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="22560-142">Note</span><span class="sxs-lookup"><span data-stu-id="22560-142">NOTES</span></span>

## <span data-ttu-id="22560-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="22560-143">RELATED LINKS</span></span>
