---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
ms.openlocfilehash: ded23a30c078cd1d474310d73d94717d050f6824
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399278"
---
# <span data-ttu-id="49583-101">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="49583-101">Add-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="49583-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49583-102">SYNOPSIS</span></span>
<span data-ttu-id="49583-103">Aggiunge una regola di filtro della route a un filtro delle route.</span><span class="sxs-lookup"><span data-stu-id="49583-103">Adds a route filter rule to a route filter.</span></span>

## <span data-ttu-id="49583-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="49583-104">SYNTAX</span></span>

```
Add-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49583-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="49583-105">DESCRIPTION</span></span>
<span data-ttu-id="49583-106">Il cmdlet Add-AzRouteFilterRuleConfig aggiunge una regola di filtro delle route a un filtro delle route di Azure.</span><span class="sxs-lookup"><span data-stu-id="49583-106">The Add-AzRouteFilterRuleConfig cmdlet adds a route filter rule to an Azure route filter.</span></span>

## <span data-ttu-id="49583-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="49583-107">EXAMPLES</span></span>

### <span data-ttu-id="49583-108">-------------------------- esempio 1: Aggiungere una regola di filtro delle route a un filtro delle route --------------------------</span><span class="sxs-lookup"><span data-stu-id="49583-108">--------------------------  Example 1: Add a route filter rule to a route filter  --------------------------</span></span>
```
PS C:\>$RouteFilter = Get-AzRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

<span data-ttu-id="49583-109">Il primo comando ottiene un filtro di route denominato routefilter01 usando il cmdlet Get-AzRouteFilter route.</span><span class="sxs-lookup"><span data-stu-id="49583-109">The first command gets a route filter named routefilter01 by using the Get-AzRouteFilter cmdlet.</span></span>
<span data-ttu-id="49583-110">Il comando archivia il filtro nella $RouteFilter variabile.</span><span class="sxs-lookup"><span data-stu-id="49583-110">The command stores the filter in the $RouteFilter variable.</span></span>

## <span data-ttu-id="49583-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49583-111">PARAMETERS</span></span>

### <span data-ttu-id="49583-112">-Access</span><span class="sxs-lookup"><span data-stu-id="49583-112">-Access</span></span>
<span data-ttu-id="49583-113">Specifica l'accesso alla regola di filtro della route. I valori validi sono Nega o Consenti.</span><span class="sxs-lookup"><span data-stu-id="49583-113">Specifies the access of the route filter rule, Valid values are Deny or Allow.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49583-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="49583-114">-CommunityList</span></span>
<span data-ttu-id="49583-115">Elenco di valori community in base a cui verrà filtrato il filtro della route</span><span class="sxs-lookup"><span data-stu-id="49583-115">The list of community value that route filter will filter on</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49583-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49583-116">-DefaultProfile</span></span>
<span data-ttu-id="49583-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="49583-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49583-118">-Force</span><span class="sxs-lookup"><span data-stu-id="49583-118">-Force</span></span>
<span data-ttu-id="49583-119">Non chiedere conferma se si vuole sovrassere una risorsa</span><span class="sxs-lookup"><span data-stu-id="49583-119">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49583-120">-Name</span><span class="sxs-lookup"><span data-stu-id="49583-120">-Name</span></span>
<span data-ttu-id="49583-121">Specifica un nome della regola di filtro delle route da aggiungere al filtro delle route.</span><span class="sxs-lookup"><span data-stu-id="49583-121">Specifies a name of the route filter rule to add to the route filter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49583-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="49583-122">-RouteFilter</span></span>
<span data-ttu-id="49583-123">Specifica il filtro della route a cui questo cmdlet aggiunge una regola di filtro della route.</span><span class="sxs-lookup"><span data-stu-id="49583-123">Specifies the route filter to which this cmdlet adds a route filter rule.</span></span>

```yaml
Type: PSRouteFilter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49583-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="49583-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="49583-125">Specifica il tipo di regola del filtro delle route.</span><span class="sxs-lookup"><span data-stu-id="49583-125">Specifies the route filter rule type.</span></span>
<span data-ttu-id="49583-126">I valori validi sono: Community</span><span class="sxs-lookup"><span data-stu-id="49583-126">Valid values are: Community</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Community

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49583-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="49583-127">-Confirm</span></span>
<span data-ttu-id="49583-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49583-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49583-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49583-129">-WhatIf</span></span>
<span data-ttu-id="49583-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="49583-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="49583-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="49583-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49583-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49583-132">CommonParameters</span></span>
<span data-ttu-id="49583-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49583-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49583-134">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49583-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49583-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="49583-135">INPUTS</span></span>

### <span data-ttu-id="49583-136">PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="49583-136">PSRouteFilter</span></span>
<span data-ttu-id="49583-137">Il parametro 'RouteFilter' accetta il valore di tipo 'PSRouteFilter' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="49583-137">Parameter 'RouteFilter' accepts value of type 'PSRouteFilter' from the pipeline</span></span>

## <span data-ttu-id="49583-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="49583-138">OUTPUTS</span></span>

### <span data-ttu-id="49583-139">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="49583-139">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="49583-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="49583-140">NOTES</span></span>
<span data-ttu-id="49583-141">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, rete, rete</span><span class="sxs-lookup"><span data-stu-id="49583-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="49583-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="49583-142">RELATED LINKS</span></span>

[<span data-ttu-id="49583-143">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="49583-143">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="49583-144">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="49583-144">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)




[<span data-ttu-id="49583-145">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="49583-145">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

