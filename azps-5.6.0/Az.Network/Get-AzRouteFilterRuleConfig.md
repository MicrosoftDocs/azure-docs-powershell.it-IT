---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 0ed7233cda87c376707e0a5b5682a61a179550d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954078"
---
# <span data-ttu-id="1f392-101">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1f392-101">Get-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="1f392-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f392-102">SYNOPSIS</span></span>
<span data-ttu-id="1f392-103">Ottiene una regola di filtro della route in un filtro delle route.</span><span class="sxs-lookup"><span data-stu-id="1f392-103">Gets a route filter rule in a route filter.</span></span>

## <span data-ttu-id="1f392-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1f392-104">SYNTAX</span></span>

```
Get-AzRouteFilterRuleConfig [-Name <String>] -RouteFilter <PSRouteFilter>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f392-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1f392-105">DESCRIPTION</span></span>
<span data-ttu-id="1f392-106">Il cmdlet **Get-AzRouteFilterRuleConfig** ottiene una regola di filtro della route o un elenco di regole di filtro delle route in un filtro delle route.</span><span class="sxs-lookup"><span data-stu-id="1f392-106">The **Get-AzRouteFilterRuleConfig** cmdlet gets a route filter rule or a list of route filter rules in a route filter.</span></span>

## <span data-ttu-id="1f392-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1f392-107">EXAMPLES</span></span>

### <span data-ttu-id="1f392-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1f392-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "MyRouteFilter" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf
```

<span data-ttu-id="1f392-109">Il primo comando ottiene il filtro delle route denominato MyRouteFilter e quindi lo archivia nella variabile $rf.</span><span class="sxs-lookup"><span data-stu-id="1f392-109">The first command gets the route filter named MyRouteFilter, and then stores it in the variable $rf.</span></span>
<span data-ttu-id="1f392-110">Il secondo comando ottiene la regola di filtro delle route denominata Rule01 associata a tale filtro.</span><span class="sxs-lookup"><span data-stu-id="1f392-110">The second command gets the route filter rule named Rule01 associated with that route filter.</span></span>
<span data-ttu-id="1f392-111">Il terzo comando ottiene un elenco di regole di filtro delle route associate a tale filtro.</span><span class="sxs-lookup"><span data-stu-id="1f392-111">The third command gets a list of route filter rules associated with that route filter.</span></span>

## <span data-ttu-id="1f392-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f392-112">PARAMETERS</span></span>

### <span data-ttu-id="1f392-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f392-113">-DefaultProfile</span></span>
<span data-ttu-id="1f392-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1f392-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f392-115">-Name</span><span class="sxs-lookup"><span data-stu-id="1f392-115">-Name</span></span>
<span data-ttu-id="1f392-116">Nome della regola di filtro delle route</span><span class="sxs-lookup"><span data-stu-id="1f392-116">The name of the route filter rule</span></span>

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

### <span data-ttu-id="1f392-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="1f392-117">-RouteFilter</span></span>
<span data-ttu-id="1f392-118">The RouteFilter</span><span class="sxs-lookup"><span data-stu-id="1f392-118">The RouteFilter</span></span>

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

### <span data-ttu-id="1f392-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f392-119">CommonParameters</span></span>
<span data-ttu-id="1f392-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f392-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f392-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1f392-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f392-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="1f392-122">INPUTS</span></span>

### <span data-ttu-id="1f392-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1f392-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="1f392-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1f392-124">OUTPUTS</span></span>

### <span data-ttu-id="1f392-125">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="1f392-125">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="1f392-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="1f392-126">NOTES</span></span>

## <span data-ttu-id="1f392-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1f392-127">RELATED LINKS</span></span>

[<span data-ttu-id="1f392-128">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1f392-128">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="1f392-129">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1f392-129">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="1f392-130">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1f392-130">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="1f392-131">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1f392-131">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="1f392-132">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1f392-132">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="1f392-133">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1f392-133">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="1f392-134">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1f392-134">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="1f392-135">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1f392-135">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
