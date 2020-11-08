---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilterRuleConfig.md
ms.openlocfilehash: eb8de50aac1b68928d5cebe8118665b9a24e8fbf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192020"
---
# <span data-ttu-id="eeda5-101">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="eeda5-101">Set-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="eeda5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eeda5-102">SYNOPSIS</span></span>
<span data-ttu-id="eeda5-103">Modifica la regola di filtro route di un filtro di route.</span><span class="sxs-lookup"><span data-stu-id="eeda5-103">Modifies the route filter rule of a route filter.</span></span>

## <span data-ttu-id="eeda5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eeda5-104">SYNTAX</span></span>

```
Set-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eeda5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eeda5-105">DESCRIPTION</span></span>
<span data-ttu-id="eeda5-106">Il cmdlet **set-AzRouteFilterRuleConfig** modifica la regola di filtro della route di un filtro di route.</span><span class="sxs-lookup"><span data-stu-id="eeda5-106">The **Set-AzRouteFilterRuleConfig** cmdlet modifies the route filter rule of a route filter.</span></span>

## <span data-ttu-id="eeda5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eeda5-107">EXAMPLES</span></span>

### <span data-ttu-id="eeda5-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="eeda5-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
PS C:\> $rf = Set-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01" -Access Deny -RouteFilterRuleType Community -CommunityList "12076:5010","12076:5040"
PS C:\> Set-AzRouteFilter -RouteFilter $rf
```

<span data-ttu-id="eeda5-109">Il primo comando ottiene il filtro della route denominato RouteFilter01 e lo archivia nella variabile $rf.</span><span class="sxs-lookup"><span data-stu-id="eeda5-109">The first command gets the route filter named RouteFilter01 and stores it in the $rf variable.</span></span>
<span data-ttu-id="eeda5-110">Il secondo comando modifica la regola di filtro route denominata Rule01 e archivia il filtro della route aggiornato nella variabile $rf.</span><span class="sxs-lookup"><span data-stu-id="eeda5-110">The second command modifies the route filter rule named Rule01 and stores updated route filter in the $rf variable.</span></span>
<span data-ttu-id="eeda5-111">Il terzo comando Salva il filtro di route aggiornato.</span><span class="sxs-lookup"><span data-stu-id="eeda5-111">The third command saves updated route filter.</span></span>

## <span data-ttu-id="eeda5-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eeda5-112">PARAMETERS</span></span>

### <span data-ttu-id="eeda5-113">-Access</span><span class="sxs-lookup"><span data-stu-id="eeda5-113">-Access</span></span>
<span data-ttu-id="eeda5-114">Tipo di accesso della regola.</span><span class="sxs-lookup"><span data-stu-id="eeda5-114">The access type of the rule.</span></span>
<span data-ttu-id="eeda5-115">I valori possibili sono:' Allow ',' Deny '</span><span class="sxs-lookup"><span data-stu-id="eeda5-115">Possible values are: 'Allow', 'Deny'</span></span>

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

### <span data-ttu-id="eeda5-116">-Community</span><span class="sxs-lookup"><span data-stu-id="eeda5-116">-CommunityList</span></span>
<span data-ttu-id="eeda5-117">Elenco di valori della community a cui il filtro route verrà filtrato</span><span class="sxs-lookup"><span data-stu-id="eeda5-117">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="eeda5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eeda5-118">-DefaultProfile</span></span>
<span data-ttu-id="eeda5-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eeda5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eeda5-120">-Force</span><span class="sxs-lookup"><span data-stu-id="eeda5-120">-Force</span></span>
<span data-ttu-id="eeda5-121">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="eeda5-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="eeda5-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="eeda5-122">-Name</span></span>
<span data-ttu-id="eeda5-123">Nome della regola di filtro route</span><span class="sxs-lookup"><span data-stu-id="eeda5-123">The name of the route filter rule</span></span>

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

### <span data-ttu-id="eeda5-124">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="eeda5-124">-RouteFilter</span></span>
<span data-ttu-id="eeda5-125">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="eeda5-125">The RouteFilter</span></span>

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

### <span data-ttu-id="eeda5-126">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="eeda5-126">-RouteFilterRuleType</span></span>
<span data-ttu-id="eeda5-127">Tipo di regola di filtro route della regola.</span><span class="sxs-lookup"><span data-stu-id="eeda5-127">The route filter rule type of the rule.</span></span>
<span data-ttu-id="eeda5-128">I valori possibili sono:' community '</span><span class="sxs-lookup"><span data-stu-id="eeda5-128">Possible values are: 'Community'</span></span>

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

### <span data-ttu-id="eeda5-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="eeda5-129">-Confirm</span></span>
<span data-ttu-id="eeda5-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eeda5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eeda5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eeda5-131">-WhatIf</span></span>
<span data-ttu-id="eeda5-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eeda5-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eeda5-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eeda5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eeda5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeda5-134">CommonParameters</span></span>
<span data-ttu-id="eeda5-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eeda5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeda5-136">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eeda5-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeda5-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eeda5-137">INPUTS</span></span>

### <span data-ttu-id="eeda5-138">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="eeda5-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="eeda5-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eeda5-139">OUTPUTS</span></span>

### <span data-ttu-id="eeda5-140">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="eeda5-140">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="eeda5-141">Note</span><span class="sxs-lookup"><span data-stu-id="eeda5-141">NOTES</span></span>

## <span data-ttu-id="eeda5-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eeda5-142">RELATED LINKS</span></span>

[<span data-ttu-id="eeda5-143">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="eeda5-143">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="eeda5-144">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="eeda5-144">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="eeda5-145">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="eeda5-145">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="eeda5-146">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="eeda5-146">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="eeda5-147">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="eeda5-147">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="eeda5-148">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="eeda5-148">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="eeda5-149">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="eeda5-149">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="eeda5-150">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="eeda5-150">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)