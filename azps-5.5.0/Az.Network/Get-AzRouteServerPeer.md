---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azrouteserverpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteServerPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteServerPeer.md
ms.openlocfilehash: d36a919adfbf1a7a2e2b7a10313433e820cc478a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184670"
---
# <span data-ttu-id="75e39-101">Get-AzRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="75e39-101">Get-AzRouteServerPeer</span></span>

## <span data-ttu-id="75e39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75e39-102">SYNOPSIS</span></span>
<span data-ttu-id="75e39-103">Ottiene un peer RouteServer in un Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="75e39-103">Gets a RouteServer peer in an Azure RouteServer</span></span>

## <span data-ttu-id="75e39-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="75e39-104">SYNTAX</span></span>

### <span data-ttu-id="75e39-105">RouteServerNParameterNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="75e39-105">RouteServerNPeerNameParameterSet (Default)</span></span>
```
Get-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -RouteServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75e39-106">RouteServerNResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="75e39-106">RouteServerNPeerResourceIdParameterSet</span></span>
```
Get-AzRouteServerPeer -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75e39-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="75e39-107">DESCRIPTION</span></span>
<span data-ttu-id="75e39-108">Il cmdlet **Get-AzRouteServerDare** ottiene un peer in un Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="75e39-108">The **Get-AzRouteServerPeer** cmdlet gets a Peer in an Azure RouteServer</span></span>

## <span data-ttu-id="75e39-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="75e39-109">EXAMPLES</span></span>

### <span data-ttu-id="75e39-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="75e39-110">Example 1</span></span>
```powershell
Get-AzRouteServerPeer -ResourceGroupName routeServerRG -RouteServerName routeServer -PeerName peer
```

### <span data-ttu-id="75e39-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="75e39-111">Example 2</span></span>
```powershell
$routeServerPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer/bgpConnections/peer'
Get-AzRouteServerPeer -ResourceId $routeServerPeerId
```

## <span data-ttu-id="75e39-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75e39-112">PARAMETERS</span></span>

### <span data-ttu-id="75e39-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75e39-113">-DefaultProfile</span></span>
<span data-ttu-id="75e39-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="75e39-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75e39-115">-PeerName</span><span class="sxs-lookup"><span data-stu-id="75e39-115">-PeerName</span></span>
<span data-ttu-id="75e39-116">Nome del peer del server di route.</span><span class="sxs-lookup"><span data-stu-id="75e39-116">The name of the route server peer.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNPeerNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75e39-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75e39-117">-ResourceGroupName</span></span>
<span data-ttu-id="75e39-118">Nome del gruppo di risorse del server di route.</span><span class="sxs-lookup"><span data-stu-id="75e39-118">The resource group name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75e39-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75e39-119">-ResourceId</span></span>
<span data-ttu-id="75e39-120">ResourceId del peer del server di route.</span><span class="sxs-lookup"><span data-stu-id="75e39-120">ResourceId of the route server peer.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNPeerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75e39-121">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="75e39-121">-RouteServerName</span></span>
<span data-ttu-id="75e39-122">Nome del server di route.</span><span class="sxs-lookup"><span data-stu-id="75e39-122">The name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75e39-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75e39-123">CommonParameters</span></span>
<span data-ttu-id="75e39-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75e39-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75e39-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="75e39-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75e39-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="75e39-126">INPUTS</span></span>

### <span data-ttu-id="75e39-127">System.String</span><span class="sxs-lookup"><span data-stu-id="75e39-127">System.String</span></span>

## <span data-ttu-id="75e39-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="75e39-128">OUTPUTS</span></span>

### <span data-ttu-id="75e39-129">Microsoft.Azure.Commands.Network.Models.PSRouteServerDir</span><span class="sxs-lookup"><span data-stu-id="75e39-129">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span></span>

## <span data-ttu-id="75e39-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="75e39-130">NOTES</span></span>

## <span data-ttu-id="75e39-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="75e39-131">RELATED LINKS</span></span>
