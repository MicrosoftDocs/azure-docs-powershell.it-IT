---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
ms.openlocfilehash: 0c6fa8b973af2f2ab4a9c8547dddffda18eb15c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990903"
---
# <span data-ttu-id="824d8-101">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="824d8-101">Set-AzRouteFilter</span></span>

## <span data-ttu-id="824d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="824d8-102">SYNOPSIS</span></span>
<span data-ttu-id="824d8-103">Aggiorna un filtro delle route.</span><span class="sxs-lookup"><span data-stu-id="824d8-103">Updates a route filter.</span></span>

## <span data-ttu-id="824d8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="824d8-104">SYNTAX</span></span>

```
Set-AzRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="824d8-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="824d8-105">DESCRIPTION</span></span>
<span data-ttu-id="824d8-106">Il cmdlet **Set-AzApplicationGateway** aggiorna un filtro della route</span><span class="sxs-lookup"><span data-stu-id="824d8-106">The **Set-AzApplicationGateway** cmdlet updates a route filter</span></span>

## <span data-ttu-id="824d8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="824d8-107">EXAMPLES</span></span>

### <span data-ttu-id="824d8-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="824d8-108">Example 1</span></span>
```powershell
PS C:\> Set-AzRouteFilter -RouteFilter $rf
```

<span data-ttu-id="824d8-109">Questo comando aggiorna il filtro delle route con le impostazioni nella $rf variabile.</span><span class="sxs-lookup"><span data-stu-id="824d8-109">This command updates the route filter with settings in the $rf variable.</span></span>

## <span data-ttu-id="824d8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="824d8-110">PARAMETERS</span></span>

### <span data-ttu-id="824d8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="824d8-111">-AsJob</span></span>
<span data-ttu-id="824d8-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="824d8-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="824d8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="824d8-113">-DefaultProfile</span></span>
<span data-ttu-id="824d8-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="824d8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="824d8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="824d8-115">-Force</span></span>
<span data-ttu-id="824d8-116">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="824d8-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="824d8-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="824d8-117">-RouteFilter</span></span>
<span data-ttu-id="824d8-118">The RouteFilter</span><span class="sxs-lookup"><span data-stu-id="824d8-118">The RouteFilter</span></span>

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

### <span data-ttu-id="824d8-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="824d8-119">-Confirm</span></span>
<span data-ttu-id="824d8-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="824d8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="824d8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="824d8-121">-WhatIf</span></span>
<span data-ttu-id="824d8-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="824d8-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="824d8-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="824d8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="824d8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="824d8-124">CommonParameters</span></span>
<span data-ttu-id="824d8-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="824d8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="824d8-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="824d8-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="824d8-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="824d8-127">INPUTS</span></span>

### <span data-ttu-id="824d8-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="824d8-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="824d8-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="824d8-129">OUTPUTS</span></span>

### <span data-ttu-id="824d8-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="824d8-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="824d8-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="824d8-131">NOTES</span></span>

## <span data-ttu-id="824d8-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="824d8-132">RELATED LINKS</span></span>

[<span data-ttu-id="824d8-133">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="824d8-133">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="824d8-134">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="824d8-134">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="824d8-135">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="824d8-135">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="824d8-136">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="824d8-136">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="824d8-137">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="824d8-137">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="824d8-138">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="824d8-138">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="824d8-139">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="824d8-139">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="824d8-140">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="824d8-140">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
