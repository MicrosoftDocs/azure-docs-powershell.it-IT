---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
ms.openlocfilehash: d55c16f7fa4f45ac3b1249f4e2e8b41dfb529d4c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184678"
---
# <span data-ttu-id="ddb91-101">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ddb91-101">Get-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="ddb91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddb91-102">SYNOPSIS</span></span>
<span data-ttu-id="ddb91-103">Ottiene una regola di filtro della route in un filtro delle route.</span><span class="sxs-lookup"><span data-stu-id="ddb91-103">Gets a route filter rule in a route filter.</span></span>

## <span data-ttu-id="ddb91-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ddb91-104">SYNTAX</span></span>

```
Get-AzRouteFilterRuleConfig [-Name <String>] -RouteFilter <PSRouteFilter>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddb91-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ddb91-105">DESCRIPTION</span></span>
<span data-ttu-id="ddb91-106">Il cmdlet **Get-AzRouteFilterRuleConfig** ottiene una regola di filtro della route o un elenco di regole di filtro delle route in un filtro delle route.</span><span class="sxs-lookup"><span data-stu-id="ddb91-106">The **Get-AzRouteFilterRuleConfig** cmdlet gets a route filter rule or a list of route filter rules in a route filter.</span></span>

## <span data-ttu-id="ddb91-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ddb91-107">EXAMPLES</span></span>

### <span data-ttu-id="ddb91-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ddb91-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "MyRouteFilter" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf
```

<span data-ttu-id="ddb91-109">Il primo comando ottiene il filtro delle route denominato MyRouteFilter e quindi lo archivia nella variabile $rf.</span><span class="sxs-lookup"><span data-stu-id="ddb91-109">The first command gets the route filter named MyRouteFilter, and then stores it in the variable $rf.</span></span>
<span data-ttu-id="ddb91-110">Il secondo comando ottiene la regola di filtro della route denominata Rule01 associata a tale filtro.</span><span class="sxs-lookup"><span data-stu-id="ddb91-110">The second command gets the route filter rule named Rule01 associated with that route filter.</span></span>
<span data-ttu-id="ddb91-111">Il terzo comando ottiene un elenco di regole di filtro delle route associate a tale filtro.</span><span class="sxs-lookup"><span data-stu-id="ddb91-111">The third command gets a list of route filter rules associated with that route filter.</span></span>

## <span data-ttu-id="ddb91-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ddb91-112">PARAMETERS</span></span>

### <span data-ttu-id="ddb91-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddb91-113">-DefaultProfile</span></span>
<span data-ttu-id="ddb91-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ddb91-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddb91-115">-Name</span><span class="sxs-lookup"><span data-stu-id="ddb91-115">-Name</span></span>
<span data-ttu-id="ddb91-116">Nome della regola di filtro delle route</span><span class="sxs-lookup"><span data-stu-id="ddb91-116">The name of the route filter rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddb91-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="ddb91-117">-RouteFilter</span></span>
<span data-ttu-id="ddb91-118">The RouteFilter</span><span class="sxs-lookup"><span data-stu-id="ddb91-118">The RouteFilter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ddb91-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddb91-119">CommonParameters</span></span>
<span data-ttu-id="ddb91-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddb91-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddb91-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ddb91-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddb91-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="ddb91-122">INPUTS</span></span>

### <span data-ttu-id="ddb91-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ddb91-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="ddb91-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ddb91-124">OUTPUTS</span></span>

### <span data-ttu-id="ddb91-125">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="ddb91-125">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="ddb91-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="ddb91-126">NOTES</span></span>

## <span data-ttu-id="ddb91-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ddb91-127">RELATED LINKS</span></span>

[<span data-ttu-id="ddb91-128">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ddb91-128">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="ddb91-129">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ddb91-129">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="ddb91-130">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ddb91-130">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="ddb91-131">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ddb91-131">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="ddb91-132">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ddb91-132">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="ddb91-133">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ddb91-133">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="ddb91-134">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ddb91-134">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="ddb91-135">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ddb91-135">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
