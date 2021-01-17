---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
ms.openlocfilehash: d55c16f7fa4f45ac3b1249f4e2e8b41dfb529d4c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369921"
---
# <span data-ttu-id="81c41-101">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="81c41-101">Get-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="81c41-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="81c41-102">SYNOPSIS</span></span>
<span data-ttu-id="81c41-103">Ottiene una regola di filtro route in un filtro di route.</span><span class="sxs-lookup"><span data-stu-id="81c41-103">Gets a route filter rule in a route filter.</span></span>

## <span data-ttu-id="81c41-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="81c41-104">SYNTAX</span></span>

```
Get-AzRouteFilterRuleConfig [-Name <String>] -RouteFilter <PSRouteFilter>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81c41-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="81c41-105">DESCRIPTION</span></span>
<span data-ttu-id="81c41-106">Il cmdlet **Get-AzRouteFilterRuleConfig** ottiene una regola di filtro route o un elenco di regole di filtro delle route in un filtro di route.</span><span class="sxs-lookup"><span data-stu-id="81c41-106">The **Get-AzRouteFilterRuleConfig** cmdlet gets a route filter rule or a list of route filter rules in a route filter.</span></span>

## <span data-ttu-id="81c41-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="81c41-107">EXAMPLES</span></span>

### <span data-ttu-id="81c41-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="81c41-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "MyRouteFilter" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf
```

<span data-ttu-id="81c41-109">Il primo comando ottiene il filtro della route denominato MyRouteFilter e lo archivia nella variabile $rf.</span><span class="sxs-lookup"><span data-stu-id="81c41-109">The first command gets the route filter named MyRouteFilter, and then stores it in the variable $rf.</span></span>
<span data-ttu-id="81c41-110">Il secondo comando consente di ottenere la regola di filtro route denominata Rule01 associata al filtro della route.</span><span class="sxs-lookup"><span data-stu-id="81c41-110">The second command gets the route filter rule named Rule01 associated with that route filter.</span></span>
<span data-ttu-id="81c41-111">Il terzo comando ottiene un elenco delle regole di filtro delle route associate al filtro della route.</span><span class="sxs-lookup"><span data-stu-id="81c41-111">The third command gets a list of route filter rules associated with that route filter.</span></span>

## <span data-ttu-id="81c41-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="81c41-112">PARAMETERS</span></span>

### <span data-ttu-id="81c41-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81c41-113">-DefaultProfile</span></span>
<span data-ttu-id="81c41-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="81c41-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81c41-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="81c41-115">-Name</span></span>
<span data-ttu-id="81c41-116">Nome della regola di filtro route</span><span class="sxs-lookup"><span data-stu-id="81c41-116">The name of the route filter rule</span></span>

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

### <span data-ttu-id="81c41-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="81c41-117">-RouteFilter</span></span>
<span data-ttu-id="81c41-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="81c41-118">The RouteFilter</span></span>

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

### <span data-ttu-id="81c41-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81c41-119">CommonParameters</span></span>
<span data-ttu-id="81c41-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81c41-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81c41-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81c41-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81c41-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="81c41-122">INPUTS</span></span>

### <span data-ttu-id="81c41-123">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="81c41-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="81c41-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="81c41-124">OUTPUTS</span></span>

### <span data-ttu-id="81c41-125">Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="81c41-125">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="81c41-126">Note</span><span class="sxs-lookup"><span data-stu-id="81c41-126">NOTES</span></span>

## <span data-ttu-id="81c41-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="81c41-127">RELATED LINKS</span></span>

[<span data-ttu-id="81c41-128">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="81c41-128">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="81c41-129">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="81c41-129">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="81c41-130">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="81c41-130">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="81c41-131">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="81c41-131">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="81c41-132">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="81c41-132">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="81c41-133">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="81c41-133">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="81c41-134">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="81c41-134">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="81c41-135">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="81c41-135">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
