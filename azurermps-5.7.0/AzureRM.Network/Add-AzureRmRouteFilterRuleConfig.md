---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: 5daf0c5f764a095906e31167d6ddbc764ae68d19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518943"
---
# <span data-ttu-id="6c1fc-101">Add-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6c1fc-101">Add-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="6c1fc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6c1fc-102">SYNOPSIS</span></span>
<span data-ttu-id="6c1fc-103">Aggiunge una regola di filtro route a un filtro di route.</span><span class="sxs-lookup"><span data-stu-id="6c1fc-103">Adds a route filter rule to a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c1fc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6c1fc-104">SYNTAX</span></span>

```
Add-AzureRmRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c1fc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6c1fc-105">DESCRIPTION</span></span>
<span data-ttu-id="6c1fc-106">Il cmdlet Add-AzureRmRouteFilterRuleConfig aggiunge una regola di filtro route a un filtro di route di Azure.</span><span class="sxs-lookup"><span data-stu-id="6c1fc-106">The Add-AzureRmRouteFilterRuleConfig cmdlet adds a route filter rule to an Azure route filter.</span></span>

## <span data-ttu-id="6c1fc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6c1fc-107">EXAMPLES</span></span>

### <span data-ttu-id="6c1fc-108">--------------------------Esempio 1: aggiungere una regola di filtro route a un filtro di route--------------------------</span><span class="sxs-lookup"><span data-stu-id="6c1fc-108">--------------------------  Example 1: Add a route filter rule to a route filter  --------------------------</span></span>
```
PS C:\>$RouteFilter = Get-AzureRmRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzureRmRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

<span data-ttu-id="6c1fc-109">Il primo comando ottiene un filtro della route denominato routefilter01 usando il cmdlet Get-AzureRmRouteFilter.</span><span class="sxs-lookup"><span data-stu-id="6c1fc-109">The first command gets a route filter named routefilter01 by using the Get-AzureRmRouteFilter cmdlet.</span></span>
<span data-ttu-id="6c1fc-110">Il comando Archivia il filtro nella variabile $RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="6c1fc-110">The command stores the filter in the $RouteFilter variable.</span></span>

## <span data-ttu-id="6c1fc-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6c1fc-111">PARAMETERS</span></span>

### <span data-ttu-id="6c1fc-112">-Access</span><span class="sxs-lookup"><span data-stu-id="6c1fc-112">-Access</span></span>
<span data-ttu-id="6c1fc-113">Specifica l'accesso della regola di filtro della route, i valori validi sono Deny o Allow.</span><span class="sxs-lookup"><span data-stu-id="6c1fc-113">Specifies the access of the route filter rule, Valid values are Deny or Allow.</span></span>

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

### <span data-ttu-id="6c1fc-114">-Community</span><span class="sxs-lookup"><span data-stu-id="6c1fc-114">-CommunityList</span></span>
<span data-ttu-id="6c1fc-115">Elenco di valori della community a cui il filtro route verrà filtrato</span><span class="sxs-lookup"><span data-stu-id="6c1fc-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="6c1fc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c1fc-116">-DefaultProfile</span></span>
<span data-ttu-id="6c1fc-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6c1fc-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c1fc-118">-Force</span><span class="sxs-lookup"><span data-stu-id="6c1fc-118">-Force</span></span>
<span data-ttu-id="6c1fc-119">Non chiedere conferma se si vuole usare una risorsa per un sovrarito</span><span class="sxs-lookup"><span data-stu-id="6c1fc-119">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="6c1fc-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="6c1fc-120">-Name</span></span>
<span data-ttu-id="6c1fc-121">Specifica un nome della regola di filtro route da aggiungere al filtro della route.</span><span class="sxs-lookup"><span data-stu-id="6c1fc-121">Specifies a name of the route filter rule to add to the route filter.</span></span>

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

### <span data-ttu-id="6c1fc-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="6c1fc-122">-RouteFilter</span></span>
<span data-ttu-id="6c1fc-123">Specifica il filtro della route a cui questo cmdlet aggiunge una regola di filtro della route.</span><span class="sxs-lookup"><span data-stu-id="6c1fc-123">Specifies the route filter to which this cmdlet adds a route filter rule.</span></span>

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

### <span data-ttu-id="6c1fc-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="6c1fc-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="6c1fc-125">Specifica il tipo di regola di filtro route.</span><span class="sxs-lookup"><span data-stu-id="6c1fc-125">Specifies the route filter rule type.</span></span>
<span data-ttu-id="6c1fc-126">I valori validi sono: community</span><span class="sxs-lookup"><span data-stu-id="6c1fc-126">Valid values are: Community</span></span>

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

### <span data-ttu-id="6c1fc-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6c1fc-127">-Confirm</span></span>
<span data-ttu-id="6c1fc-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c1fc-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c1fc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c1fc-129">-WhatIf</span></span>
<span data-ttu-id="6c1fc-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6c1fc-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6c1fc-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6c1fc-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c1fc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c1fc-132">CommonParameters</span></span>
<span data-ttu-id="6c1fc-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c1fc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c1fc-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c1fc-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c1fc-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6c1fc-135">INPUTS</span></span>

### <span data-ttu-id="6c1fc-136">PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="6c1fc-136">PSRouteFilter</span></span>
<span data-ttu-id="6c1fc-137">Il parametro ' RouteFilter ' accetta il valore di tipo ' PSRouteFilter ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="6c1fc-137">Parameter 'RouteFilter' accepts value of type 'PSRouteFilter' from the pipeline</span></span>

## <span data-ttu-id="6c1fc-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6c1fc-138">OUTPUTS</span></span>

### <span data-ttu-id="6c1fc-139">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="6c1fc-139">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="6c1fc-140">Note</span><span class="sxs-lookup"><span data-stu-id="6c1fc-140">NOTES</span></span>
<span data-ttu-id="6c1fc-141">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="6c1fc-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="6c1fc-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6c1fc-142">RELATED LINKS</span></span>

[<span data-ttu-id="6c1fc-143">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6c1fc-143">Get-AzureRmRouteFilterRuleConfig</span></span>](./Get-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="6c1fc-144">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="6c1fc-144">Get-AzureRmRouteFilter</span></span>](./Get-AzureRmRouteFilter.md)

[<span data-ttu-id="6c1fc-145">New-AzureRmRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="6c1fc-145">New-AzureRmRouteFilterRuleConfigConfig</span></span>](./New-AzureRmRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="6c1fc-146">Remove-AzureRmRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="6c1fc-146">Remove-AzureRmRouteFilterRuleConfigConfig</span></span>](./Remove-AzureRmRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="6c1fc-147">Set-AzureRmRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="6c1fc-147">Set-AzureRmRouteFilterRuleConfigConfig</span></span>](./Set-AzureRmRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="6c1fc-148">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="6c1fc-148">Set-AzureRmRouteFilter</span></span>](./Set-AzureRmRouteFilter.md)

