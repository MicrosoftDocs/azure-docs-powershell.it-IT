---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azrouteserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteServer.md
ms.openlocfilehash: 20021b2d557b4590a9853d3124930db27286313a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184671"
---
# <span data-ttu-id="2cccb-101">Get-AzRouteServer</span><span class="sxs-lookup"><span data-stu-id="2cccb-101">Get-AzRouteServer</span></span>

## <span data-ttu-id="2cccb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2cccb-102">SYNOPSIS</span></span>
<span data-ttu-id="2cccb-103">Ottenere un server di route di Azure</span><span class="sxs-lookup"><span data-stu-id="2cccb-103">Get an Azure RouteServer</span></span>

## <span data-ttu-id="2cccb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2cccb-104">SYNTAX</span></span>

### <span data-ttu-id="2cccb-105">RouteServerSubscriptionIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2cccb-105">RouteServerSubscriptionIdParameterSet (Default)</span></span>
```
Get-AzRouteServer [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cccb-106">RouteServerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cccb-106">RouteServerNameParameterSet</span></span>
```
Get-AzRouteServer -ResourceGroupName <String> [-RouteServerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cccb-107">RouteServerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cccb-107">RouteServerResourceIdParameterSet</span></span>
```
Get-AzRouteServer -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2cccb-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2cccb-108">DESCRIPTION</span></span>
<span data-ttu-id="2cccb-109">Il cmdlet **Get-AzRouteServer** ottiene un Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="2cccb-109">The **Get-AzRouteServer** cmdlet gets an Azure RouteServer</span></span>

## <span data-ttu-id="2cccb-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2cccb-110">EXAMPLES</span></span>

### <span data-ttu-id="2cccb-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2cccb-111">Example 1</span></span>
```powershell
Get-AzRouteServer -ResourceGroupName routeServerRG -RouteServerName routeServer
```

### <span data-ttu-id="2cccb-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="2cccb-112">Example 2</span></span>
```powershell
$routeServerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer'
Get-AzRouteServer -ResourceId $routeServerId
```
## <span data-ttu-id="2cccb-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2cccb-113">PARAMETERS</span></span>

### <span data-ttu-id="2cccb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cccb-114">-DefaultProfile</span></span>
<span data-ttu-id="2cccb-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2cccb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cccb-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cccb-116">-ResourceGroupName</span></span>
<span data-ttu-id="2cccb-117">Nome del gruppo di risorse del server di route.</span><span class="sxs-lookup"><span data-stu-id="2cccb-117">The resource group name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cccb-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2cccb-118">-ResourceId</span></span>
<span data-ttu-id="2cccb-119">ResourceId del server delle route.</span><span class="sxs-lookup"><span data-stu-id="2cccb-119">ResourceId of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cccb-120">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="2cccb-120">-RouteServerName</span></span>
<span data-ttu-id="2cccb-121">Nome del server di route.</span><span class="sxs-lookup"><span data-stu-id="2cccb-121">The name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cccb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cccb-122">CommonParameters</span></span>
<span data-ttu-id="2cccb-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cccb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cccb-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2cccb-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cccb-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="2cccb-125">INPUTS</span></span>

### <span data-ttu-id="2cccb-126">System.String</span><span class="sxs-lookup"><span data-stu-id="2cccb-126">System.String</span></span>

## <span data-ttu-id="2cccb-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2cccb-127">OUTPUTS</span></span>

### <span data-ttu-id="2cccb-128">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="2cccb-128">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="2cccb-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="2cccb-129">NOTES</span></span>

## <span data-ttu-id="2cccb-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2cccb-130">RELATED LINKS</span></span>
