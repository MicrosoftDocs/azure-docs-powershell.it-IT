---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilter.md
ms.openlocfilehash: 88b755a8865a5ce07a5dc86c94958de0c0e72485
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021252"
---
# <span data-ttu-id="5578a-101">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="5578a-101">Get-AzRouteFilter</span></span>

## <span data-ttu-id="5578a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5578a-102">SYNOPSIS</span></span>
<span data-ttu-id="5578a-103">Ottiene un filtro di route.</span><span class="sxs-lookup"><span data-stu-id="5578a-103">Gets a route filter.</span></span>

## <span data-ttu-id="5578a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5578a-104">SYNTAX</span></span>

### <span data-ttu-id="5578a-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="5578a-105">NoExpand</span></span>
```
Get-AzRouteFilter [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5578a-106">Espandere</span><span class="sxs-lookup"><span data-stu-id="5578a-106">Expand</span></span>
```
Get-AzRouteFilter -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5578a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5578a-107">DESCRIPTION</span></span>
<span data-ttu-id="5578a-108">Il cmdlet **Get-AzRouteFilter** ottiene un filtro di route.</span><span class="sxs-lookup"><span data-stu-id="5578a-108">The **Get-AzRouteFilter** cmdlet gets a route filter.</span></span>

## <span data-ttu-id="5578a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5578a-109">EXAMPLES</span></span>

### <span data-ttu-id="5578a-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5578a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"

Name              : RouteFilter01
ResourceGroupName : ResourceGroup01
Location          : westus
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsof
                    t.Network/routeFilters/RouteFilter01
Etag              : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState : Succeeded
Tags              :
Rules             : []
Peerings          : []
```

<span data-ttu-id="5578a-111">Questo comando ottiene il filtro della route denominato RouteFilter01 che appartiene al gruppo di risorse denominato ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="5578a-111">This command gets the route filter named RouteFilter01 that belongs to the resource group named ResourceGroup01.</span></span>

### <span data-ttu-id="5578a-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="5578a-112">Example 2</span></span>
```powershell
PS C:\> Get-AzRouteFilter -Name "RouteFilter*"

Name              : RouteFilter01
ResourceGroupName : ResourceGroup01
Location          : westus
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsof
                    t.Network/routeFilters/RouteFilter01
Etag              : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState : Succeeded
Tags              :
Rules             : []
Peerings          : []

Name              : RouteFilter02
ResourceGroupName : ResourceGroup01
Location          : westus
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsof
                    t.Network/routeFilters/RouteFilter02
Etag              : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState : Succeeded
Tags              :
Rules             : []
Peerings          : []
```

<span data-ttu-id="5578a-113">Questo comando consente di ottenere tutti i filtri di route che iniziano con "RouteFilter".</span><span class="sxs-lookup"><span data-stu-id="5578a-113">This command gets all route filters that start with "RouteFilter".</span></span>

## <span data-ttu-id="5578a-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5578a-114">PARAMETERS</span></span>

### <span data-ttu-id="5578a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5578a-115">-DefaultProfile</span></span>
<span data-ttu-id="5578a-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5578a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5578a-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="5578a-117">-ExpandResource</span></span>
<span data-ttu-id="5578a-118">Riferimento alla risorsa da espandere.</span><span class="sxs-lookup"><span data-stu-id="5578a-118">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5578a-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="5578a-119">-Name</span></span>
<span data-ttu-id="5578a-120">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="5578a-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="5578a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5578a-121">-ResourceGroupName</span></span>
<span data-ttu-id="5578a-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5578a-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="5578a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5578a-123">CommonParameters</span></span>
<span data-ttu-id="5578a-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5578a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5578a-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5578a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5578a-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5578a-126">INPUTS</span></span>

### <span data-ttu-id="5578a-127">System. String</span><span class="sxs-lookup"><span data-stu-id="5578a-127">System.String</span></span>

## <span data-ttu-id="5578a-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5578a-128">OUTPUTS</span></span>

### <span data-ttu-id="5578a-129">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="5578a-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="5578a-130">Note</span><span class="sxs-lookup"><span data-stu-id="5578a-130">NOTES</span></span>

## <span data-ttu-id="5578a-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5578a-131">RELATED LINKS</span></span>

[<span data-ttu-id="5578a-132">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="5578a-132">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="5578a-133">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="5578a-133">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="5578a-134">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="5578a-134">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="5578a-135">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5578a-135">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="5578a-136">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5578a-136">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="5578a-137">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5578a-137">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="5578a-138">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5578a-138">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="5578a-139">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5578a-139">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
