---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/powershell/module/az.mixedreality/new-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccount.md
ms.openlocfilehash: a2a6dafe9aedfc41200e12bb3c583ad1b5fb02b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970525"
---
# <span data-ttu-id="f32f8-101">New-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="f32f8-101">New-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="f32f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f32f8-102">SYNOPSIS</span></span>
<span data-ttu-id="f32f8-103">Account per la creazione di ancoraggi nello spaziale</span><span class="sxs-lookup"><span data-stu-id="f32f8-103">Create Spatial Anchors Account</span></span>

## <span data-ttu-id="f32f8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f32f8-104">SYNTAX</span></span>

```
New-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f32f8-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f32f8-105">DESCRIPTION</span></span>
<span data-ttu-id="f32f8-106">Creare un nuovo account di ancoraggi nello spaziale in determinate aree, gruppi di risorse e sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="f32f8-106">Create a new Spatial Anchors Account in certain Subscription, Resource Group and Region.</span></span>

## <span data-ttu-id="f32f8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f32f8-107">EXAMPLES</span></span>

### <span data-ttu-id="f32f8-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f32f8-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmSpatialAnchorsAccount -ResourceGroup rg1 -Name example -Location centralus

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : centralus
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/SpatialAnchorsAccounts/example
Name                : example
Type                : Microsoft.MixedReality/SpatialAnchorsAccounts
```

<span data-ttu-id="f32f8-109">Creare un nuovo account di ancoraggi nello spaziale "example" nella sottoscrizione corrente, nel gruppo di risorse "rg1" e negli Stati Uniti centrali.</span><span class="sxs-lookup"><span data-stu-id="f32f8-109">Create a new Spatial Anchors Account "example" in current Subscription, Resource Group "rg1" and Central US.</span></span>

## <span data-ttu-id="f32f8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f32f8-110">PARAMETERS</span></span>

### <span data-ttu-id="f32f8-111">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f32f8-111">-Confirm</span></span>
<span data-ttu-id="f32f8-112">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f32f8-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f32f8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f32f8-113">-DefaultProfile</span></span>
<span data-ttu-id="f32f8-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f32f8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f32f8-115">-Location</span><span class="sxs-lookup"><span data-stu-id="f32f8-115">-Location</span></span>
<span data-ttu-id="f32f8-116">Posizione account degli ancoraggi nello spaziale.</span><span class="sxs-lookup"><span data-stu-id="f32f8-116">Spatial Anchors Account Location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f32f8-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f32f8-117">-Name</span></span>
<span data-ttu-id="f32f8-118">Nome account per gli ancoraggi nello spaziale.</span><span class="sxs-lookup"><span data-stu-id="f32f8-118">Spatial Anchors Account Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SpatialAnchorsAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f32f8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f32f8-119">-ResourceGroupName</span></span>
<span data-ttu-id="f32f8-120">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f32f8-120">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f32f8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f32f8-121">-WhatIf</span></span>
<span data-ttu-id="f32f8-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f32f8-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f32f8-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f32f8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f32f8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f32f8-124">CommonParameters</span></span>
<span data-ttu-id="f32f8-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f32f8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f32f8-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f32f8-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f32f8-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="f32f8-127">INPUTS</span></span>

### <span data-ttu-id="f32f8-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f32f8-128">None</span></span>

## <span data-ttu-id="f32f8-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f32f8-129">OUTPUTS</span></span>

### <span data-ttu-id="f32f8-130">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="f32f8-130">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="f32f8-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="f32f8-131">NOTES</span></span>

## <span data-ttu-id="f32f8-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f32f8-132">RELATED LINKS</span></span>
