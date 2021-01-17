---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 204ecf05f0781649f441399c7a9b6acfbfbd8cdd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475135"
---
# <span data-ttu-id="90b65-101">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="90b65-101">Add-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="90b65-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="90b65-102">SYNOPSIS</span></span>
<span data-ttu-id="90b65-103">Aggiunge una regola di filtro route a un filtro di route.</span><span class="sxs-lookup"><span data-stu-id="90b65-103">Adds a route filter rule to a route filter.</span></span>

## <span data-ttu-id="90b65-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="90b65-104">SYNTAX</span></span>

```
Add-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90b65-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="90b65-105">DESCRIPTION</span></span>
<span data-ttu-id="90b65-106">Il cmdlet Add-AzRouteFilterRuleConfig aggiunge una regola di filtro route a un filtro di route di Azure.</span><span class="sxs-lookup"><span data-stu-id="90b65-106">The Add-AzRouteFilterRuleConfig cmdlet adds a route filter rule to an Azure route filter.</span></span>

## <span data-ttu-id="90b65-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="90b65-107">EXAMPLES</span></span>

### <span data-ttu-id="90b65-108">Esempio 1: aggiungere una regola di filtro route a un filtro di route</span><span class="sxs-lookup"><span data-stu-id="90b65-108">Example 1: Add a route filter rule to a route filter</span></span>
```
PS C:\>$RouteFilter = Get-AzRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

<span data-ttu-id="90b65-109">Il primo comando ottiene un filtro della route denominato routefilter01 usando il cmdlet Get-AzRouteFilter.</span><span class="sxs-lookup"><span data-stu-id="90b65-109">The first command gets a route filter named routefilter01 by using the Get-AzRouteFilter cmdlet.</span></span>
<span data-ttu-id="90b65-110">Il comando Archivia il filtro nella variabile $RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="90b65-110">The command stores the filter in the $RouteFilter variable.</span></span>

## <span data-ttu-id="90b65-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="90b65-111">PARAMETERS</span></span>

### <span data-ttu-id="90b65-112">-Access</span><span class="sxs-lookup"><span data-stu-id="90b65-112">-Access</span></span>
<span data-ttu-id="90b65-113">Specifica l'accesso della regola di filtro della route, i valori validi sono Deny o Allow.</span><span class="sxs-lookup"><span data-stu-id="90b65-113">Specifies the access of the route filter rule, Valid values are Deny or Allow.</span></span>

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

### <span data-ttu-id="90b65-114">-Community</span><span class="sxs-lookup"><span data-stu-id="90b65-114">-CommunityList</span></span>
<span data-ttu-id="90b65-115">Elenco di valori della community a cui il filtro route verrà filtrato</span><span class="sxs-lookup"><span data-stu-id="90b65-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="90b65-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90b65-116">-DefaultProfile</span></span>
<span data-ttu-id="90b65-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="90b65-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90b65-118">-Force</span><span class="sxs-lookup"><span data-stu-id="90b65-118">-Force</span></span>
<span data-ttu-id="90b65-119">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="90b65-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="90b65-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="90b65-120">-Name</span></span>
<span data-ttu-id="90b65-121">Specifica un nome della regola di filtro route da aggiungere al filtro della route.</span><span class="sxs-lookup"><span data-stu-id="90b65-121">Specifies a name of the route filter rule to add to the route filter.</span></span>

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

### <span data-ttu-id="90b65-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="90b65-122">-RouteFilter</span></span>
<span data-ttu-id="90b65-123">Specifica il filtro della route a cui questo cmdlet aggiunge una regola di filtro della route.</span><span class="sxs-lookup"><span data-stu-id="90b65-123">Specifies the route filter to which this cmdlet adds a route filter rule.</span></span>

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

### <span data-ttu-id="90b65-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="90b65-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="90b65-125">Specifica il tipo di regola di filtro route.</span><span class="sxs-lookup"><span data-stu-id="90b65-125">Specifies the route filter rule type.</span></span>
<span data-ttu-id="90b65-126">I valori validi sono: community</span><span class="sxs-lookup"><span data-stu-id="90b65-126">Valid values are: Community</span></span>

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

### <span data-ttu-id="90b65-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="90b65-127">-Confirm</span></span>
<span data-ttu-id="90b65-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90b65-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90b65-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90b65-129">-WhatIf</span></span>
<span data-ttu-id="90b65-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="90b65-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="90b65-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="90b65-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90b65-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90b65-132">CommonParameters</span></span>
<span data-ttu-id="90b65-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90b65-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90b65-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90b65-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90b65-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="90b65-135">INPUTS</span></span>

### <span data-ttu-id="90b65-136">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="90b65-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="90b65-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="90b65-137">OUTPUTS</span></span>

### <span data-ttu-id="90b65-138">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="90b65-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="90b65-139">Note</span><span class="sxs-lookup"><span data-stu-id="90b65-139">NOTES</span></span>
<span data-ttu-id="90b65-140">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="90b65-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="90b65-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="90b65-141">RELATED LINKS</span></span>

[<span data-ttu-id="90b65-142">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="90b65-142">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="90b65-143">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="90b65-143">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="90b65-144">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="90b65-144">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="90b65-145">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="90b65-145">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="90b65-146">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="90b65-146">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="90b65-147">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="90b65-147">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="90b65-148">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="90b65-148">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="90b65-149">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="90b65-149">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
