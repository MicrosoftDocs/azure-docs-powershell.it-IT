---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 2212ffb43f646e49a4552713b6408091dd985aae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996111"
---
# <span data-ttu-id="048d9-101">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="048d9-101">Remove-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="048d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="048d9-102">SYNOPSIS</span></span>
<span data-ttu-id="048d9-103">Rimuove una regola di filtro della route da un filtro delle route.</span><span class="sxs-lookup"><span data-stu-id="048d9-103">Removes a route filter rule from a route filter.</span></span>

## <span data-ttu-id="048d9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="048d9-104">SYNTAX</span></span>

```
Remove-AzRouteFilterRuleConfig -Name <String> -RouteFilter <PSRouteFilter> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="048d9-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="048d9-105">DESCRIPTION</span></span>
<span data-ttu-id="048d9-106">Il cmdlet **Remove-AzRouteFilterRuleConfig** rimuove una regola di filtro della route da un filtro delle route.</span><span class="sxs-lookup"><span data-stu-id="048d9-106">The **Remove-AzRouteFilterRuleConfig** cmdlet removes a route filter rule from a route filter.</span></span>

## <span data-ttu-id="048d9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="048d9-107">EXAMPLES</span></span>

### <span data-ttu-id="048d9-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="048d9-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01"
```

<span data-ttu-id="048d9-109">Il primo comando ottiene un filtro di route denominato RouteFilter01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella $rf variabile.</span><span class="sxs-lookup"><span data-stu-id="048d9-109">The first command gets a route filter named RouteFilter01 that belongs to the resource group named ResourceGroup01 and stores it in the $rf variable.</span></span>
<span data-ttu-id="048d9-110">Il secondo comando rimuove la regola di filtro delle route denominata Rule01 dal filtro delle route archiviato in $rf.</span><span class="sxs-lookup"><span data-stu-id="048d9-110">The second command removes the route filter rule named Rule01 from the route filter stored in $rf.</span></span>

## <span data-ttu-id="048d9-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="048d9-111">PARAMETERS</span></span>

### <span data-ttu-id="048d9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="048d9-112">-DefaultProfile</span></span>
<span data-ttu-id="048d9-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="048d9-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="048d9-114">-Force</span><span class="sxs-lookup"><span data-stu-id="048d9-114">-Force</span></span>
<span data-ttu-id="048d9-115">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="048d9-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="048d9-116">-Name</span><span class="sxs-lookup"><span data-stu-id="048d9-116">-Name</span></span>
<span data-ttu-id="048d9-117">Nome della regola di filtro delle route</span><span class="sxs-lookup"><span data-stu-id="048d9-117">The name of the route filter rule</span></span>

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

### <span data-ttu-id="048d9-118">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="048d9-118">-RouteFilter</span></span>
<span data-ttu-id="048d9-119">The RouteFilter</span><span class="sxs-lookup"><span data-stu-id="048d9-119">The RouteFilter</span></span>

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

### <span data-ttu-id="048d9-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="048d9-120">-Confirm</span></span>
<span data-ttu-id="048d9-121">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="048d9-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="048d9-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="048d9-122">-WhatIf</span></span>
<span data-ttu-id="048d9-123">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="048d9-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="048d9-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="048d9-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="048d9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="048d9-125">CommonParameters</span></span>
<span data-ttu-id="048d9-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="048d9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="048d9-127">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="048d9-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="048d9-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="048d9-128">INPUTS</span></span>

### <span data-ttu-id="048d9-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="048d9-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="048d9-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="048d9-130">OUTPUTS</span></span>

### <span data-ttu-id="048d9-131">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="048d9-131">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="048d9-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="048d9-132">NOTES</span></span>

## <span data-ttu-id="048d9-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="048d9-133">RELATED LINKS</span></span>

[<span data-ttu-id="048d9-134">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="048d9-134">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="048d9-135">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="048d9-135">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="048d9-136">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="048d9-136">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="048d9-137">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="048d9-137">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="048d9-138">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="048d9-138">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="048d9-139">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="048d9-139">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="048d9-140">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="048d9-140">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="048d9-141">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="048d9-141">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
