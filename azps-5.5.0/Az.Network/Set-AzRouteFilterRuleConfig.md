---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilterRuleConfig.md
ms.openlocfilehash: eb8de50aac1b68928d5cebe8118665b9a24e8fbf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191622"
---
# <span data-ttu-id="bc612-101">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bc612-101">Set-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="bc612-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc612-102">SYNOPSIS</span></span>
<span data-ttu-id="bc612-103">Modifica la regola di filtro della route di un filtro delle route.</span><span class="sxs-lookup"><span data-stu-id="bc612-103">Modifies the route filter rule of a route filter.</span></span>

## <span data-ttu-id="bc612-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bc612-104">SYNTAX</span></span>

```
Set-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc612-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bc612-105">DESCRIPTION</span></span>
<span data-ttu-id="bc612-106">Il cmdlet **Set-AzRouteFilterRuleConfig** modifica la regola di filtro della route di un filtro delle route.</span><span class="sxs-lookup"><span data-stu-id="bc612-106">The **Set-AzRouteFilterRuleConfig** cmdlet modifies the route filter rule of a route filter.</span></span>

## <span data-ttu-id="bc612-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bc612-107">EXAMPLES</span></span>

### <span data-ttu-id="bc612-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bc612-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
PS C:\> $rf = Set-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01" -Access Deny -RouteFilterRuleType Community -CommunityList "12076:5010","12076:5040"
PS C:\> Set-AzRouteFilter -RouteFilter $rf
```

<span data-ttu-id="bc612-109">Il primo comando recupera il filtro di route denominato RouteFilter01 e lo archivia nella $rf variabile.</span><span class="sxs-lookup"><span data-stu-id="bc612-109">The first command gets the route filter named RouteFilter01 and stores it in the $rf variable.</span></span>
<span data-ttu-id="bc612-110">Il secondo comando modifica la regola di filtro delle route denominata Rule01 e archivia il filtro delle route aggiornato nella $rf variabile.</span><span class="sxs-lookup"><span data-stu-id="bc612-110">The second command modifies the route filter rule named Rule01 and stores updated route filter in the $rf variable.</span></span>
<span data-ttu-id="bc612-111">Il terzo comando salva il filtro delle route aggiornato.</span><span class="sxs-lookup"><span data-stu-id="bc612-111">The third command saves updated route filter.</span></span>

## <span data-ttu-id="bc612-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc612-112">PARAMETERS</span></span>

### <span data-ttu-id="bc612-113">-Access</span><span class="sxs-lookup"><span data-stu-id="bc612-113">-Access</span></span>
<span data-ttu-id="bc612-114">Tipo di accesso della regola.</span><span class="sxs-lookup"><span data-stu-id="bc612-114">The access type of the rule.</span></span>
<span data-ttu-id="bc612-115">I valori possibili sono: "Consenti", "Nega"</span><span class="sxs-lookup"><span data-stu-id="bc612-115">Possible values are: 'Allow', 'Deny'</span></span>

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

### <span data-ttu-id="bc612-116">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="bc612-116">-CommunityList</span></span>
<span data-ttu-id="bc612-117">Elenco di valori community in base a cui verrà filtrato il filtro della route</span><span class="sxs-lookup"><span data-stu-id="bc612-117">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="bc612-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc612-118">-DefaultProfile</span></span>
<span data-ttu-id="bc612-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bc612-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc612-120">-Force</span><span class="sxs-lookup"><span data-stu-id="bc612-120">-Force</span></span>
<span data-ttu-id="bc612-121">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="bc612-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="bc612-122">-Name</span><span class="sxs-lookup"><span data-stu-id="bc612-122">-Name</span></span>
<span data-ttu-id="bc612-123">Nome della regola di filtro delle route</span><span class="sxs-lookup"><span data-stu-id="bc612-123">The name of the route filter rule</span></span>

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

### <span data-ttu-id="bc612-124">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="bc612-124">-RouteFilter</span></span>
<span data-ttu-id="bc612-125">The RouteFilter</span><span class="sxs-lookup"><span data-stu-id="bc612-125">The RouteFilter</span></span>

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

### <span data-ttu-id="bc612-126">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="bc612-126">-RouteFilterRuleType</span></span>
<span data-ttu-id="bc612-127">Tipo di regola di filtro della route.</span><span class="sxs-lookup"><span data-stu-id="bc612-127">The route filter rule type of the rule.</span></span>
<span data-ttu-id="bc612-128">I valori possibili sono: "Community"</span><span class="sxs-lookup"><span data-stu-id="bc612-128">Possible values are: 'Community'</span></span>

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

### <span data-ttu-id="bc612-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bc612-129">-Confirm</span></span>
<span data-ttu-id="bc612-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc612-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc612-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc612-131">-WhatIf</span></span>
<span data-ttu-id="bc612-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bc612-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bc612-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bc612-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc612-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc612-134">CommonParameters</span></span>
<span data-ttu-id="bc612-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc612-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc612-136">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc612-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc612-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="bc612-137">INPUTS</span></span>

### <span data-ttu-id="bc612-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="bc612-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="bc612-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bc612-139">OUTPUTS</span></span>

### <span data-ttu-id="bc612-140">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="bc612-140">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="bc612-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="bc612-141">NOTES</span></span>

## <span data-ttu-id="bc612-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bc612-142">RELATED LINKS</span></span>

[<span data-ttu-id="bc612-143">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bc612-143">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="bc612-144">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bc612-144">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="bc612-145">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bc612-145">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="bc612-146">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bc612-146">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="bc612-147">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="bc612-147">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="bc612-148">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="bc612-148">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="bc612-149">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="bc612-149">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="bc612-150">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="bc612-150">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
