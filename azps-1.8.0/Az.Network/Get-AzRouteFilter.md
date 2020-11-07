---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilter.md
ms.openlocfilehash: 26fb3e9a7b4b097e79fdb328d79a82fc423ac675
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678460"
---
# <span data-ttu-id="627b0-101">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="627b0-101">Get-AzRouteFilter</span></span>

## <span data-ttu-id="627b0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="627b0-102">SYNOPSIS</span></span>
<span data-ttu-id="627b0-103">Ottiene un filtro di route.</span><span class="sxs-lookup"><span data-stu-id="627b0-103">Gets a route filter.</span></span>

## <span data-ttu-id="627b0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="627b0-104">SYNTAX</span></span>

### <span data-ttu-id="627b0-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="627b0-105">NoExpand</span></span>
```
Get-AzRouteFilter [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="627b0-106">Espandere</span><span class="sxs-lookup"><span data-stu-id="627b0-106">Expand</span></span>
```
Get-AzRouteFilter -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="627b0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="627b0-107">DESCRIPTION</span></span>
<span data-ttu-id="627b0-108">Il cmdlet **Get-AzRouteFilter** ottiene un filtro di route.</span><span class="sxs-lookup"><span data-stu-id="627b0-108">The **Get-AzRouteFilter** cmdlet gets a route filter.</span></span>

## <span data-ttu-id="627b0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="627b0-109">EXAMPLES</span></span>

### <span data-ttu-id="627b0-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="627b0-110">Example 1</span></span>
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

<span data-ttu-id="627b0-111">Questo comando ottiene il filtro della route denominato RouteFilter01 che appartiene al gruppo di risorse denominato ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="627b0-111">This command gets the route filter named RouteFilter01 that belongs to the resource group named ResourceGroup01.</span></span>

### <span data-ttu-id="627b0-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="627b0-112">Example 2</span></span>
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

<span data-ttu-id="627b0-113">Questo comando consente di ottenere tutti i filtri di route che iniziano con "RouteFilter".</span><span class="sxs-lookup"><span data-stu-id="627b0-113">This command gets all route filters that start with "RouteFilter".</span></span>

## <span data-ttu-id="627b0-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="627b0-114">PARAMETERS</span></span>

### <span data-ttu-id="627b0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="627b0-115">-DefaultProfile</span></span>
<span data-ttu-id="627b0-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="627b0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="627b0-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="627b0-117">-ExpandResource</span></span>
<span data-ttu-id="627b0-118">Riferimento alla risorsa da espandere.</span><span class="sxs-lookup"><span data-stu-id="627b0-118">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="627b0-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="627b0-119">-Name</span></span>
<span data-ttu-id="627b0-120">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="627b0-120">The resource name.</span></span>

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

### <span data-ttu-id="627b0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="627b0-121">-ResourceGroupName</span></span>
<span data-ttu-id="627b0-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="627b0-122">The resource group name.</span></span>

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

### <span data-ttu-id="627b0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="627b0-123">CommonParameters</span></span>
<span data-ttu-id="627b0-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="627b0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="627b0-125">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="627b0-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="627b0-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="627b0-126">INPUTS</span></span>

### <span data-ttu-id="627b0-127">System. String</span><span class="sxs-lookup"><span data-stu-id="627b0-127">System.String</span></span>

## <span data-ttu-id="627b0-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="627b0-128">OUTPUTS</span></span>

### <span data-ttu-id="627b0-129">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="627b0-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="627b0-130">Note</span><span class="sxs-lookup"><span data-stu-id="627b0-130">NOTES</span></span>

## <span data-ttu-id="627b0-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="627b0-131">RELATED LINKS</span></span>

[<span data-ttu-id="627b0-132">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="627b0-132">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="627b0-133">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="627b0-133">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="627b0-134">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="627b0-134">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="627b0-135">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="627b0-135">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="627b0-136">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="627b0-136">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="627b0-137">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="627b0-137">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="627b0-138">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="627b0-138">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="627b0-139">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="627b0-139">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
