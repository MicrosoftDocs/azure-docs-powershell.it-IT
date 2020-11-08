---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
ms.openlocfilehash: 650ac7c478f1c27ca3ba925c4d767f02c79fa781
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188603"
---
# <span data-ttu-id="87f77-101">Get-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="87f77-101">Get-AzAttestation</span></span>

## <span data-ttu-id="87f77-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="87f77-102">SYNOPSIS</span></span>
<span data-ttu-id="87f77-103">Ottiene un attestato.</span><span class="sxs-lookup"><span data-stu-id="87f77-103">Gets an attestation.</span></span>

## <span data-ttu-id="87f77-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="87f77-104">SYNTAX</span></span>

### <span data-ttu-id="87f77-105">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="87f77-105">NameParameterSet (Default)</span></span>
```
Get-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="87f77-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="87f77-106">ResourceIdParameterSet</span></span>
```
Get-AzAttestation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87f77-107">DefaultProviderParameterSet</span><span class="sxs-lookup"><span data-stu-id="87f77-107">DefaultProviderParameterSet</span></span>
```
Get-AzAttestation [[-Location] <String>] [-DefaultProvider] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="87f77-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="87f77-108">DESCRIPTION</span></span>
<span data-ttu-id="87f77-109">Il cmdlet Get-AzAttestation ottiene informazioni sull'attestazione in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="87f77-109">The Get-AzAttestation cmdlet gets information about the attestation in a subscription.</span></span>

## <span data-ttu-id="87f77-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="87f77-110">EXAMPLES</span></span>

### <span data-ttu-id="87f77-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="87f77-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAttestation -Name pshtest -ResourceGroupName psh-test-rg                                                                                                                                                                                                                                                       
Id                : subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/psh-test-rg/providers/Microsoft.Attestation/attestationProviders/pshtest
Location          : East US
ResourceGroupName : psh-test-rg
Name              : pshtest
Status            : Ready
TrustModel        : AAD
AttestUri         : https://pshtest.us.attest.azure.net
Tags              : {Production, Example}
TagsTable         :
                    Name        Value
                    ==========  =====
                    Production  False
                    Example     True
```

<span data-ttu-id="87f77-112">Ottenere il provider di attestazioni *pshtest* nel gruppo di risorse *PSH-test-RG*.</span><span class="sxs-lookup"><span data-stu-id="87f77-112">Get Attestation Provider *pshtest* in Resource Group *psh-test-rg*.</span></span>

### <span data-ttu-id="87f77-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="87f77-113">Example 2</span></span>
```powershell
PS C:\> Get-AzAttestation -DefaultProvider
Id                : /providers/Microsoft.Attestation/attestationProviders/sharedeus2
Location          : East US 2
ResourceGroupName :
Name              : sharedeus2
Status            : Ready
TrustModel        : AAD
AttestUri         : https://sharedeus2.eus2.attest.azure.net
Tags              :
TagsTable         :

Id                : /providers/Microsoft.Attestation/attestationProviders/sharedcus
Location          : Central US
ResourceGroupName :
Name              : sharedcus
Status            : Ready
TrustModel        : AAD
AttestUri         : https://sharedcus.cus.attest.azure.net
Tags              :
TagsTable         :

Id                : /providers/Microsoft.Attestation/attestationProviders/shareduks
Location          : UK South
ResourceGroupName :
Name              : shareduks
Status            : Ready
TrustModel        : AAD
AttestUri         : https://shareduks.uks.attest.azure.net
Tags              :
TagsTable         :
```

<span data-ttu-id="87f77-114">Ottenere tutti i provider predefiniti di attestazione disponibili</span><span class="sxs-lookup"><span data-stu-id="87f77-114">Get all available Attestation Default Providers</span></span>

### <span data-ttu-id="87f77-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="87f77-115">Example 3</span></span>
```powershell
PS C:\> Get-AzAttestation -DefaultProvider -Location "East US 2"
Id                : /providers/Microsoft.Attestation/attestationProviders/sharedeus2
Location          : East US 2
ResourceGroupName :
Name              : sharedeus2
Status            : Ready
TrustModel        : AAD
AttestUri         : https://sharedeus2.eus2.attest.azure.net
Tags              :
TagsTable         :
```

<span data-ttu-id="87f77-116">Ottenere il provider predefinito dell'attestazione dalla posizione *est degli Stati Uniti 2*</span><span class="sxs-lookup"><span data-stu-id="87f77-116">Get Attestation Default Provider from Location *East US 2*</span></span>

## <span data-ttu-id="87f77-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="87f77-117">PARAMETERS</span></span>

### <span data-ttu-id="87f77-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87f77-118">-DefaultProfile</span></span>
<span data-ttu-id="87f77-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="87f77-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87f77-120">-DefaultProvider</span><span class="sxs-lookup"><span data-stu-id="87f77-120">-DefaultProvider</span></span>
<span data-ttu-id="87f77-121">Specifica la richiesta di un provider di attestazione predefinito.</span><span class="sxs-lookup"><span data-stu-id="87f77-121">Specifies this is the request to a default attestation provider.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultProviderParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87f77-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="87f77-122">-Location</span></span>
<span data-ttu-id="87f77-123">Specifica la posizione del provider di attestazioni predefinito.</span><span class="sxs-lookup"><span data-stu-id="87f77-123">Specifies the Location of the default attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultProviderParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87f77-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="87f77-124">-Name</span></span>
<span data-ttu-id="87f77-125">Nome dell'attestazione.</span><span class="sxs-lookup"><span data-stu-id="87f77-125">Attestation Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87f77-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87f77-126">-ResourceGroupName</span></span>
<span data-ttu-id="87f77-127">Specifica il nome del gruppo di risorse associato all'attestazione in cui viene eseguita la query.</span><span class="sxs-lookup"><span data-stu-id="87f77-127">Specifies the name of the resource group associated with the attestation being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87f77-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87f77-128">-ResourceId</span></span>
<span data-ttu-id="87f77-129">Specifica il nome del ResourceID associato all'attestazione in cui viene eseguita la query</span><span class="sxs-lookup"><span data-stu-id="87f77-129">Specifies the name of the ResourceID associated with the attestation being queried</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87f77-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87f77-130">CommonParameters</span></span>
<span data-ttu-id="87f77-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87f77-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87f77-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="87f77-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87f77-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="87f77-133">INPUTS</span></span>

### <span data-ttu-id="87f77-134">System. String</span><span class="sxs-lookup"><span data-stu-id="87f77-134">System.String</span></span>

## <span data-ttu-id="87f77-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="87f77-135">OUTPUTS</span></span>

### <span data-ttu-id="87f77-136">Microsoft. Azure. Commands. Attestation. Models. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="87f77-136">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="87f77-137">Note</span><span class="sxs-lookup"><span data-stu-id="87f77-137">NOTES</span></span>

## <span data-ttu-id="87f77-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="87f77-138">RELATED LINKS</span></span>
