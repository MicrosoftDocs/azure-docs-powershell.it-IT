---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/new-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
ms.openlocfilehash: ce21b116ceb41bfdfb26008dd44c914f3198ab39
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675841"
---
# <span data-ttu-id="7cf19-101">New-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="7cf19-101">New-AzAttestation</span></span>

## <span data-ttu-id="7cf19-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7cf19-102">SYNOPSIS</span></span>
<span data-ttu-id="7cf19-103">Crea un attestato</span><span class="sxs-lookup"><span data-stu-id="7cf19-103">Creates an attestation</span></span>

## <span data-ttu-id="7cf19-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7cf19-104">SYNTAX</span></span>

```
New-AzAttestation -Name <String> -ResourceGroupName <String> [-AttestationPolicy <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cf19-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7cf19-105">DESCRIPTION</span></span>
<span data-ttu-id="7cf19-106">Il cmdlet New-AzAttestation crea una attestazione nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="7cf19-106">The New-AzAttestation cmdlet creates an attestation in the specified resource group.</span></span>

## <span data-ttu-id="7cf19-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7cf19-107">EXAMPLES</span></span>

### <span data-ttu-id="7cf19-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7cf19-108">Example 1</span></span>
```powershell
PS C:\> New-AzAttestation -Name example -ResourceGroupName rg1 
Id                  : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/rg1/providers/Microsoft.Attestation/attestationProviders/example
Name                : example
Type                : Microsoft.Attestation/attestationProviders
Status              : Ready
AttesUri            : https://example.us.attest.azure.net
ResoureGroupName    : rg1 
SubscriptionId      : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
```

<span data-ttu-id="7cf19-109">Creare una nuova attestazione "esempio" nell'abbonamento corrente, gruppo risorse "RG1"</span><span class="sxs-lookup"><span data-stu-id="7cf19-109">Create a new Attestation "example" in current Subscription, Resource Group "rg1"</span></span>

## <span data-ttu-id="7cf19-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7cf19-110">PARAMETERS</span></span>

### <span data-ttu-id="7cf19-111">-AttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="7cf19-111">-AttestationPolicy</span></span>
<span data-ttu-id="7cf19-112">Specifica i criteri di attestazione passati per creare l'attestazione.</span><span class="sxs-lookup"><span data-stu-id="7cf19-112">Specifies the attestation policy passed in which to create the attestation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cf19-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cf19-113">-DefaultProfile</span></span>
<span data-ttu-id="7cf19-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf19-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf19-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="7cf19-115">-Name</span></span>
<span data-ttu-id="7cf19-116">Specifica un nome dell'istanza da creare.</span><span class="sxs-lookup"><span data-stu-id="7cf19-116">Specifies a name of the Instance to create.</span></span>
<span data-ttu-id="7cf19-117">Il nome può essere costituito da qualsiasi combinazione di lettere, cifre o trattini.</span><span class="sxs-lookup"><span data-stu-id="7cf19-117">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="7cf19-118">Il nome deve iniziare e terminare con una lettera o una cifra.</span><span class="sxs-lookup"><span data-stu-id="7cf19-118">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="7cf19-119">Il nome deve essere universalmente univoco.</span><span class="sxs-lookup"><span data-stu-id="7cf19-119">The name must be universally unique.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cf19-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cf19-120">-ResourceGroupName</span></span>
<span data-ttu-id="7cf19-121">Specifica il nome di un gruppo di risorse esistente in cui creare l'attestazione.</span><span class="sxs-lookup"><span data-stu-id="7cf19-121">Specifies the name of an existing resource group in which to create the attestation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cf19-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7cf19-122">-Confirm</span></span>
<span data-ttu-id="7cf19-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cf19-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf19-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cf19-124">-WhatIf</span></span>
<span data-ttu-id="7cf19-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7cf19-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cf19-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7cf19-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf19-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cf19-127">CommonParameters</span></span>
<span data-ttu-id="7cf19-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cf19-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cf19-129">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7cf19-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cf19-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7cf19-130">INPUTS</span></span>

### <span data-ttu-id="7cf19-131">System. String</span><span class="sxs-lookup"><span data-stu-id="7cf19-131">System.String</span></span>

## <span data-ttu-id="7cf19-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7cf19-132">OUTPUTS</span></span>

### <span data-ttu-id="7cf19-133">Microsoft. Azure. Commands. Attestation. Models. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="7cf19-133">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="7cf19-134">Note</span><span class="sxs-lookup"><span data-stu-id="7cf19-134">NOTES</span></span>

## <span data-ttu-id="7cf19-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7cf19-135">RELATED LINKS</span></span>
