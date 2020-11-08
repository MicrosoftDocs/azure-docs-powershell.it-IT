---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
ms.openlocfilehash: f97b9ac971a4eec1945ae4418332e7d6ff74c71c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192272"
---
# <span data-ttu-id="cd527-101">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="cd527-101">Set-AzRouteFilter</span></span>

## <span data-ttu-id="cd527-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cd527-102">SYNOPSIS</span></span>
<span data-ttu-id="cd527-103">Aggiorna un filtro di route.</span><span class="sxs-lookup"><span data-stu-id="cd527-103">Updates a route filter.</span></span>

## <span data-ttu-id="cd527-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cd527-104">SYNTAX</span></span>

```
Set-AzRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd527-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd527-105">DESCRIPTION</span></span>
<span data-ttu-id="cd527-106">Il cmdlet **set-AzApplicationGateway** aggiorna un filtro di route</span><span class="sxs-lookup"><span data-stu-id="cd527-106">The **Set-AzApplicationGateway** cmdlet updates a route filter</span></span>

## <span data-ttu-id="cd527-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cd527-107">EXAMPLES</span></span>

### <span data-ttu-id="cd527-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cd527-108">Example 1</span></span>
```powershell
PS C:\> Set-AzRouteFilter -RouteFilter $rf
```

<span data-ttu-id="cd527-109">Questo comando Aggiorna il filtro della route con le impostazioni nella variabile $rf.</span><span class="sxs-lookup"><span data-stu-id="cd527-109">This command updates the route filter with settings in the $rf variable.</span></span>

## <span data-ttu-id="cd527-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cd527-110">PARAMETERS</span></span>

### <span data-ttu-id="cd527-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd527-111">-AsJob</span></span>
<span data-ttu-id="cd527-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="cd527-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cd527-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd527-113">-DefaultProfile</span></span>
<span data-ttu-id="cd527-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cd527-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd527-115">-Force</span><span class="sxs-lookup"><span data-stu-id="cd527-115">-Force</span></span>
<span data-ttu-id="cd527-116">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="cd527-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="cd527-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="cd527-117">-RouteFilter</span></span>
<span data-ttu-id="cd527-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="cd527-118">The RouteFilter</span></span>

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

### <span data-ttu-id="cd527-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cd527-119">-Confirm</span></span>
<span data-ttu-id="cd527-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd527-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd527-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd527-121">-WhatIf</span></span>
<span data-ttu-id="cd527-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd527-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cd527-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd527-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd527-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd527-124">CommonParameters</span></span>
<span data-ttu-id="cd527-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd527-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd527-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd527-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd527-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cd527-127">INPUTS</span></span>

### <span data-ttu-id="cd527-128">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="cd527-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="cd527-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cd527-129">OUTPUTS</span></span>

### <span data-ttu-id="cd527-130">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="cd527-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="cd527-131">Note</span><span class="sxs-lookup"><span data-stu-id="cd527-131">NOTES</span></span>

## <span data-ttu-id="cd527-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cd527-132">RELATED LINKS</span></span>

[<span data-ttu-id="cd527-133">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="cd527-133">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="cd527-134">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="cd527-134">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="cd527-135">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="cd527-135">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="cd527-136">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cd527-136">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="cd527-137">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cd527-137">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="cd527-138">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cd527-138">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="cd527-139">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cd527-139">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="cd527-140">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cd527-140">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
