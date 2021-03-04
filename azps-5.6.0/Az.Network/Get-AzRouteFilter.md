---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilter.md
ms.openlocfilehash: 5ae145c79012a62ae5e46c14bd649b17460f8d3c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954093"
---
# <span data-ttu-id="ca6b4-101">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ca6b4-101">Get-AzRouteFilter</span></span>

## <span data-ttu-id="ca6b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca6b4-102">SYNOPSIS</span></span>
<span data-ttu-id="ca6b4-103">Ottiene un filtro della route.</span><span class="sxs-lookup"><span data-stu-id="ca6b4-103">Gets a route filter.</span></span>

## <span data-ttu-id="ca6b4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ca6b4-104">SYNTAX</span></span>

### <span data-ttu-id="ca6b4-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="ca6b4-105">NoExpand</span></span>
```
Get-AzRouteFilter [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ca6b4-106">Espandi</span><span class="sxs-lookup"><span data-stu-id="ca6b4-106">Expand</span></span>
```
Get-AzRouteFilter -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca6b4-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ca6b4-107">DESCRIPTION</span></span>
<span data-ttu-id="ca6b4-108">Il cmdlet **Get-AzRouteFilter** ottiene un filtro delle route.</span><span class="sxs-lookup"><span data-stu-id="ca6b4-108">The **Get-AzRouteFilter** cmdlet gets a route filter.</span></span>

## <span data-ttu-id="ca6b4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ca6b4-109">EXAMPLES</span></span>

### <span data-ttu-id="ca6b4-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ca6b4-110">Example 1</span></span>
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

<span data-ttu-id="ca6b4-111">Questo comando recupera il filtro della route denominato RouteFilter01 che appartiene al gruppo di risorse denominato ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="ca6b4-111">This command gets the route filter named RouteFilter01 that belongs to the resource group named ResourceGroup01.</span></span>

### <span data-ttu-id="ca6b4-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ca6b4-112">Example 2</span></span>
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

<span data-ttu-id="ca6b4-113">Questo comando recupera tutti i filtri di route che iniziano con "RouteFilter".</span><span class="sxs-lookup"><span data-stu-id="ca6b4-113">This command gets all route filters that start with "RouteFilter".</span></span>

## <span data-ttu-id="ca6b4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca6b4-114">PARAMETERS</span></span>

### <span data-ttu-id="ca6b4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca6b4-115">-DefaultProfile</span></span>
<span data-ttu-id="ca6b4-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ca6b4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca6b4-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="ca6b4-117">-ExpandResource</span></span>
<span data-ttu-id="ca6b4-118">Riferimento di risorsa da espandere.</span><span class="sxs-lookup"><span data-stu-id="ca6b4-118">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="ca6b4-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ca6b4-119">-Name</span></span>
<span data-ttu-id="ca6b4-120">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ca6b4-120">The resource name.</span></span>

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

### <span data-ttu-id="ca6b4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca6b4-121">-ResourceGroupName</span></span>
<span data-ttu-id="ca6b4-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ca6b4-122">The resource group name.</span></span>

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

### <span data-ttu-id="ca6b4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca6b4-123">CommonParameters</span></span>
<span data-ttu-id="ca6b4-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca6b4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca6b4-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ca6b4-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca6b4-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="ca6b4-126">INPUTS</span></span>

### <span data-ttu-id="ca6b4-127">System.String</span><span class="sxs-lookup"><span data-stu-id="ca6b4-127">System.String</span></span>

## <span data-ttu-id="ca6b4-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ca6b4-128">OUTPUTS</span></span>

### <span data-ttu-id="ca6b4-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ca6b4-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="ca6b4-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="ca6b4-130">NOTES</span></span>

## <span data-ttu-id="ca6b4-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ca6b4-131">RELATED LINKS</span></span>

[<span data-ttu-id="ca6b4-132">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ca6b4-132">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="ca6b4-133">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ca6b4-133">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="ca6b4-134">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ca6b4-134">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="ca6b4-135">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ca6b4-135">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="ca6b4-136">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ca6b4-136">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="ca6b4-137">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ca6b4-137">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="ca6b4-138">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ca6b4-138">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="ca6b4-139">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ca6b4-139">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
