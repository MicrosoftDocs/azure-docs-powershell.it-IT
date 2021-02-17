---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeering.md
ms.openlocfilehash: 58ba131ab0bebc65d8fd5259d24b2846da229721
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189383"
---
# <span data-ttu-id="024b7-101">Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="024b7-101">Get-AzPeering</span></span>

## <span data-ttu-id="024b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="024b7-102">SYNOPSIS</span></span>
<span data-ttu-id="024b7-103">Ottiene le risorse peering per una sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="024b7-103">Gets the Peering Resources for a subscription</span></span>

## <span data-ttu-id="024b7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="024b7-104">SYNTAX</span></span>

### <span data-ttu-id="024b7-105">BySubscription (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="024b7-105">BySubscription (Default)</span></span>
```
Get-AzPeering [-Kind <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="024b7-106">ByResourceGroupAndName</span><span class="sxs-lookup"><span data-stu-id="024b7-106">ByResourceGroupAndName</span></span>
```
Get-AzPeering [-ResourceGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="024b7-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="024b7-107">ByResourceId</span></span>
```
Get-AzPeering [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="024b7-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="024b7-108">DESCRIPTION</span></span>
<span data-ttu-id="024b7-109">Ottiene i peering da una sottoscrizione, un gruppo di risorse o in base al nome.</span><span class="sxs-lookup"><span data-stu-id="024b7-109">Gets the Peerings from a subscription, resource group, or by name.</span></span>

## <span data-ttu-id="024b7-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="024b7-110">EXAMPLES</span></span>

### <span data-ttu-id="024b7-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="024b7-111">Example 1</span></span>
```powershell
PS C:> Get-AzPeering

Name              : myExchangePeering1
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {99999}
PeerAsn.Id        : /subscriptions/providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions/resourceGroups/test/providers/Microsoft.Peering/peerings/myExchangePeering1
Type              : Microsoft.Peering/peerings
Tags              : {}

Name                 : ContosoSeattlePeering
Sku                  : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringSku
Kind                 : Direct
Connections          : {99999}
UseForPeeringService : False
PeerAsn              : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSSubResource
PeeringLocation      : Seattle
ProvisioningState    : Succeeded
Location             : centralus
Id                   : /subscriptions/resourceGroups/testCarrier/providers/Microsoft.Peering/peerings/ContosoSeattlePeering
Type                 : Microsoft.Peering/peerings
Tags                 : {}
```

<span data-ttu-id="024b7-112">Recupera tutte le risorse per la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="024b7-112">Gets all the resources for the subscription.</span></span>

### <span data-ttu-id="024b7-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="024b7-113">Example 2</span></span>
```powershell
PS C:> Get-AzPeering -ResourceGroupName test -Name myExchangePeering1

Name              : myExchangePeering1
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {99999}
PeerAsn.Id        : /subscriptions/providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions/resourceGroups/test/providers/Microsoft.Peering/peerings/myExchangePeering1
Type              : Microsoft.Peering/peerings
Tags              : {}
```

<span data-ttu-id="024b7-114">Ottiene il nome del peering di Exchange `myExchangePeering1`</span><span class="sxs-lookup"><span data-stu-id="024b7-114">Gets the Exchange peering named `myExchangePeering1`</span></span>

### <span data-ttu-id="024b7-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="024b7-115">Example 2</span></span>
```powershell
PS C:> Get-AzPeering -ResourceId $resourceId

Name              : myExchangePeering1
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {99999}
PeerAsn.Id        : /subscriptions/providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions/resourceGroups/test/providers/Microsoft.Peering/peerings/myExchangePeering1
Type              : Microsoft.Peering/peerings
Tags              : {}
```

<span data-ttu-id="024b7-116">Ottiene il peering di Exchange denominato `myExchangePeering1` in base all'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="024b7-116">Gets the Exchange peering named `myExchangePeering1` based on the resource id.</span></span>

## <span data-ttu-id="024b7-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="024b7-117">PARAMETERS</span></span>

### <span data-ttu-id="024b7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="024b7-118">-DefaultProfile</span></span>
<span data-ttu-id="024b7-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="024b7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="024b7-120">-Kind</span><span class="sxs-lookup"><span data-stu-id="024b7-120">-Kind</span></span>
<span data-ttu-id="024b7-121">Mostra tutte le risorse di peering per tipo.</span><span class="sxs-lookup"><span data-stu-id="024b7-121">Shows all Peering resource by Kind.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="024b7-122">-Name</span><span class="sxs-lookup"><span data-stu-id="024b7-122">-Name</span></span>
<span data-ttu-id="024b7-123">Nome univoco di PSCollectioning.</span><span class="sxs-lookup"><span data-stu-id="024b7-123">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="024b7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="024b7-124">-ResourceGroupName</span></span>
<span data-ttu-id="024b7-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="024b7-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="024b7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="024b7-126">-ResourceId</span></span>
<span data-ttu-id="024b7-127">Il nome stringa dell'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="024b7-127">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="024b7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="024b7-128">CommonParameters</span></span>
<span data-ttu-id="024b7-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="024b7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="024b7-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="024b7-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="024b7-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="024b7-131">INPUTS</span></span>

### <span data-ttu-id="024b7-132">System.String</span><span class="sxs-lookup"><span data-stu-id="024b7-132">System.String</span></span>

## <span data-ttu-id="024b7-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="024b7-133">OUTPUTS</span></span>

### <span data-ttu-id="024b7-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSApplicationing</span><span class="sxs-lookup"><span data-stu-id="024b7-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="024b7-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="024b7-135">NOTES</span></span>

## <span data-ttu-id="024b7-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="024b7-136">RELATED LINKS</span></span>
