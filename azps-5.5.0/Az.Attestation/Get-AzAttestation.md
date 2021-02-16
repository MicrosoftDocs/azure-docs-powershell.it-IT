---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
ms.openlocfilehash: 650ac7c478f1c27ca3ba925c4d767f02c79fa781
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199687"
---
# <span data-ttu-id="86baa-101">Get-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="86baa-101">Get-AzAttestation</span></span>

## <span data-ttu-id="86baa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86baa-102">SYNOPSIS</span></span>
<span data-ttu-id="86baa-103">Ottiene una attestazione.</span><span class="sxs-lookup"><span data-stu-id="86baa-103">Gets an attestation.</span></span>

## <span data-ttu-id="86baa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="86baa-104">SYNTAX</span></span>

### <span data-ttu-id="86baa-105">NameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="86baa-105">NameParameterSet (Default)</span></span>
```
Get-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="86baa-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="86baa-106">ResourceIdParameterSet</span></span>
```
Get-AzAttestation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86baa-107">DefaultProviderParameterSet</span><span class="sxs-lookup"><span data-stu-id="86baa-107">DefaultProviderParameterSet</span></span>
```
Get-AzAttestation [[-Location] <String>] [-DefaultProvider] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="86baa-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="86baa-108">DESCRIPTION</span></span>
<span data-ttu-id="86baa-109">Il Get-AzAttestation cmdlet riceve informazioni sulla attestazione di un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="86baa-109">The Get-AzAttestation cmdlet gets information about the attestation in a subscription.</span></span>

## <span data-ttu-id="86baa-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="86baa-110">EXAMPLES</span></span>

### <span data-ttu-id="86baa-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="86baa-111">Example 1</span></span>
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

<span data-ttu-id="86baa-112">Ottieni attestazione provider *pshtest* nel gruppo di risorse *psh-test-rg.*</span><span class="sxs-lookup"><span data-stu-id="86baa-112">Get Attestation Provider *pshtest* in Resource Group *psh-test-rg*.</span></span>

### <span data-ttu-id="86baa-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="86baa-113">Example 2</span></span>
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

<span data-ttu-id="86baa-114">Ottieni tutti i provider predefiniti di attestazione disponibili</span><span class="sxs-lookup"><span data-stu-id="86baa-114">Get all available Attestation Default Providers</span></span>

### <span data-ttu-id="86baa-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="86baa-115">Example 3</span></span>
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

<span data-ttu-id="86baa-116">Ottieni provider predefinito attestazione dalla località *Stati Uniti orientali 2*</span><span class="sxs-lookup"><span data-stu-id="86baa-116">Get Attestation Default Provider from Location *East US 2*</span></span>

## <span data-ttu-id="86baa-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86baa-117">PARAMETERS</span></span>

### <span data-ttu-id="86baa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86baa-118">-DefaultProfile</span></span>
<span data-ttu-id="86baa-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="86baa-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86baa-120">-DefaultProvider</span><span class="sxs-lookup"><span data-stu-id="86baa-120">-DefaultProvider</span></span>
<span data-ttu-id="86baa-121">Specifica che questa è la richiesta a un provider di attestazione predefinito.</span><span class="sxs-lookup"><span data-stu-id="86baa-121">Specifies this is the request to a default attestation provider.</span></span>

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

### <span data-ttu-id="86baa-122">-Location</span><span class="sxs-lookup"><span data-stu-id="86baa-122">-Location</span></span>
<span data-ttu-id="86baa-123">Specifica la posizione del provider di attestazione predefinito.</span><span class="sxs-lookup"><span data-stu-id="86baa-123">Specifies the Location of the default attestation provider.</span></span>

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

### <span data-ttu-id="86baa-124">-Name</span><span class="sxs-lookup"><span data-stu-id="86baa-124">-Name</span></span>
<span data-ttu-id="86baa-125">Nome attestazione.</span><span class="sxs-lookup"><span data-stu-id="86baa-125">Attestation Name.</span></span>

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

### <span data-ttu-id="86baa-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86baa-126">-ResourceGroupName</span></span>
<span data-ttu-id="86baa-127">Specifica il nome del gruppo di risorse associato alla attestazione in cui eseguire la query.</span><span class="sxs-lookup"><span data-stu-id="86baa-127">Specifies the name of the resource group associated with the attestation being queried.</span></span>

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

### <span data-ttu-id="86baa-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="86baa-128">-ResourceId</span></span>
<span data-ttu-id="86baa-129">Specifica il nome dell'ID Risorsa associato all'attestazione in cui eseguire la query</span><span class="sxs-lookup"><span data-stu-id="86baa-129">Specifies the name of the ResourceID associated with the attestation being queried</span></span>

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

### <span data-ttu-id="86baa-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86baa-130">CommonParameters</span></span>
<span data-ttu-id="86baa-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86baa-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86baa-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="86baa-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86baa-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="86baa-133">INPUTS</span></span>

### <span data-ttu-id="86baa-134">System.String</span><span class="sxs-lookup"><span data-stu-id="86baa-134">System.String</span></span>

## <span data-ttu-id="86baa-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="86baa-135">OUTPUTS</span></span>

### <span data-ttu-id="86baa-136">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span><span class="sxs-lookup"><span data-stu-id="86baa-136">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="86baa-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="86baa-137">NOTES</span></span>

## <span data-ttu-id="86baa-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="86baa-138">RELATED LINKS</span></span>
