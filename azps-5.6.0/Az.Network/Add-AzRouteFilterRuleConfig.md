---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 26e759256f5641f1e38553b8a2db4ab444c2aa53
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009470"
---
# <span data-ttu-id="c9f58-101">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c9f58-101">Add-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="c9f58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9f58-102">SYNOPSIS</span></span>
<span data-ttu-id="c9f58-103">Aggiunge una regola di filtro della route a un filtro delle route.</span><span class="sxs-lookup"><span data-stu-id="c9f58-103">Adds a route filter rule to a route filter.</span></span>

## <span data-ttu-id="c9f58-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c9f58-104">SYNTAX</span></span>

```
Add-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9f58-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c9f58-105">DESCRIPTION</span></span>
<span data-ttu-id="c9f58-106">Il cmdlet Add-AzRouteFilterRuleConfig aggiunge una regola di filtro delle route a un filtro delle route di Azure.</span><span class="sxs-lookup"><span data-stu-id="c9f58-106">The Add-AzRouteFilterRuleConfig cmdlet adds a route filter rule to an Azure route filter.</span></span>

## <span data-ttu-id="c9f58-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c9f58-107">EXAMPLES</span></span>

### <span data-ttu-id="c9f58-108">Esempio 1: Aggiungere una regola di filtro delle route a un filtro delle route</span><span class="sxs-lookup"><span data-stu-id="c9f58-108">Example 1: Add a route filter rule to a route filter</span></span>
```
PS C:\>$RouteFilter = Get-AzRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

<span data-ttu-id="c9f58-109">Il primo comando ottiene un filtro di route denominato routefilter01 usando il cmdlet Get-AzRouteFilter route.</span><span class="sxs-lookup"><span data-stu-id="c9f58-109">The first command gets a route filter named routefilter01 by using the Get-AzRouteFilter cmdlet.</span></span>
<span data-ttu-id="c9f58-110">Il comando archivia il filtro nella $RouteFilter variabile.</span><span class="sxs-lookup"><span data-stu-id="c9f58-110">The command stores the filter in the $RouteFilter variable.</span></span>

## <span data-ttu-id="c9f58-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9f58-111">PARAMETERS</span></span>

### <span data-ttu-id="c9f58-112">-Access</span><span class="sxs-lookup"><span data-stu-id="c9f58-112">-Access</span></span>
<span data-ttu-id="c9f58-113">Specifica l'accesso alla regola di filtro della route. I valori validi sono Nega o Consenti.</span><span class="sxs-lookup"><span data-stu-id="c9f58-113">Specifies the access of the route filter rule, Valid values are Deny or Allow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9f58-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="c9f58-114">-CommunityList</span></span>
<span data-ttu-id="c9f58-115">Elenco di valori community in base a cui verrà filtrato il filtro della route</span><span class="sxs-lookup"><span data-stu-id="c9f58-115">The list of community value that route filter will filter on</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9f58-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9f58-116">-DefaultProfile</span></span>
<span data-ttu-id="c9f58-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c9f58-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9f58-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c9f58-118">-Force</span></span>
<span data-ttu-id="c9f58-119">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="c9f58-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9f58-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c9f58-120">-Name</span></span>
<span data-ttu-id="c9f58-121">Specifica un nome della regola di filtro delle route da aggiungere al filtro delle route.</span><span class="sxs-lookup"><span data-stu-id="c9f58-121">Specifies a name of the route filter rule to add to the route filter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9f58-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="c9f58-122">-RouteFilter</span></span>
<span data-ttu-id="c9f58-123">Specifica il filtro della route a cui questo cmdlet aggiunge una regola di filtro della route.</span><span class="sxs-lookup"><span data-stu-id="c9f58-123">Specifies the route filter to which this cmdlet adds a route filter rule.</span></span>

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

### <span data-ttu-id="c9f58-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="c9f58-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="c9f58-125">Specifica il tipo di regola del filtro delle route.</span><span class="sxs-lookup"><span data-stu-id="c9f58-125">Specifies the route filter rule type.</span></span>
<span data-ttu-id="c9f58-126">I valori validi sono: Community</span><span class="sxs-lookup"><span data-stu-id="c9f58-126">Valid values are: Community</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Community

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9f58-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c9f58-127">-Confirm</span></span>
<span data-ttu-id="c9f58-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9f58-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9f58-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9f58-129">-WhatIf</span></span>
<span data-ttu-id="c9f58-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c9f58-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c9f58-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c9f58-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9f58-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9f58-132">CommonParameters</span></span>
<span data-ttu-id="c9f58-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9f58-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9f58-134">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9f58-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9f58-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="c9f58-135">INPUTS</span></span>

### <span data-ttu-id="c9f58-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c9f58-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="c9f58-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c9f58-137">OUTPUTS</span></span>

### <span data-ttu-id="c9f58-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c9f58-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="c9f58-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="c9f58-139">NOTES</span></span>
<span data-ttu-id="c9f58-140">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, rete, rete</span><span class="sxs-lookup"><span data-stu-id="c9f58-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="c9f58-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c9f58-141">RELATED LINKS</span></span>

[<span data-ttu-id="c9f58-142">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c9f58-142">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="c9f58-143">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c9f58-143">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="c9f58-144">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c9f58-144">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="c9f58-145">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c9f58-145">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="c9f58-146">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c9f58-146">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="c9f58-147">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c9f58-147">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="c9f58-148">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c9f58-148">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="c9f58-149">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c9f58-149">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
