---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeering.md
ms.openlocfilehash: 58ba131ab0bebc65d8fd5259d24b2846da229721
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032260"
---
# <span data-ttu-id="6d66e-101">Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="6d66e-101">Get-AzPeering</span></span>

## <span data-ttu-id="6d66e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6d66e-102">SYNOPSIS</span></span>
<span data-ttu-id="6d66e-103">Ottiene le risorse di peering per un abbonamento</span><span class="sxs-lookup"><span data-stu-id="6d66e-103">Gets the Peering Resources for a subscription</span></span>

## <span data-ttu-id="6d66e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6d66e-104">SYNTAX</span></span>

### <span data-ttu-id="6d66e-105">BySubscription (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6d66e-105">BySubscription (Default)</span></span>
```
Get-AzPeering [-Kind <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d66e-106">ByResourceGroupAndName</span><span class="sxs-lookup"><span data-stu-id="6d66e-106">ByResourceGroupAndName</span></span>
```
Get-AzPeering [-ResourceGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6d66e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6d66e-107">ByResourceId</span></span>
```
Get-AzPeering [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d66e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6d66e-108">DESCRIPTION</span></span>
<span data-ttu-id="6d66e-109">Ottiene i peer da un abbonamento, un gruppo di risorse o per nome.</span><span class="sxs-lookup"><span data-stu-id="6d66e-109">Gets the Peerings from a subscription, resource group, or by name.</span></span>

## <span data-ttu-id="6d66e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6d66e-110">EXAMPLES</span></span>

### <span data-ttu-id="6d66e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6d66e-111">Example 1</span></span>
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

<span data-ttu-id="6d66e-112">Ottiene tutte le risorse per l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="6d66e-112">Gets all the resources for the subscription.</span></span>

### <span data-ttu-id="6d66e-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="6d66e-113">Example 2</span></span>
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

<span data-ttu-id="6d66e-114">Ottiene il peering di Exchange denominato `myExchangePeering1`</span><span class="sxs-lookup"><span data-stu-id="6d66e-114">Gets the Exchange peering named `myExchangePeering1`</span></span>

### <span data-ttu-id="6d66e-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="6d66e-115">Example 2</span></span>
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

<span data-ttu-id="6d66e-116">Ottiene il peering di Exchange denominato `myExchangePeering1` in base all'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="6d66e-116">Gets the Exchange peering named `myExchangePeering1` based on the resource id.</span></span>

## <span data-ttu-id="6d66e-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6d66e-117">PARAMETERS</span></span>

### <span data-ttu-id="6d66e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d66e-118">-DefaultProfile</span></span>
<span data-ttu-id="6d66e-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6d66e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d66e-120">-Tipo</span><span class="sxs-lookup"><span data-stu-id="6d66e-120">-Kind</span></span>
<span data-ttu-id="6d66e-121">Mostra tutte le risorse di peering per tipo.</span><span class="sxs-lookup"><span data-stu-id="6d66e-121">Shows all Peering resource by Kind.</span></span>

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

### <span data-ttu-id="6d66e-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="6d66e-122">-Name</span></span>
<span data-ttu-id="6d66e-123">Nome univoco di PSPeering.</span><span class="sxs-lookup"><span data-stu-id="6d66e-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="6d66e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d66e-124">-ResourceGroupName</span></span>
<span data-ttu-id="6d66e-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6d66e-125">The resource group name.</span></span>

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

### <span data-ttu-id="6d66e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d66e-126">-ResourceId</span></span>
<span data-ttu-id="6d66e-127">Nome della stringa ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="6d66e-127">The resource id string name.</span></span>

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

### <span data-ttu-id="6d66e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d66e-128">CommonParameters</span></span>
<span data-ttu-id="6d66e-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d66e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d66e-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d66e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d66e-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6d66e-131">INPUTS</span></span>

### <span data-ttu-id="6d66e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="6d66e-132">System.String</span></span>

## <span data-ttu-id="6d66e-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6d66e-133">OUTPUTS</span></span>

### <span data-ttu-id="6d66e-134">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="6d66e-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="6d66e-135">Note</span><span class="sxs-lookup"><span data-stu-id="6d66e-135">NOTES</span></span>

## <span data-ttu-id="6d66e-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6d66e-136">RELATED LINKS</span></span>
