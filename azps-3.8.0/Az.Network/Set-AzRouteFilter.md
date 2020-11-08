---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
ms.openlocfilehash: f97b9ac971a4eec1945ae4418332e7d6ff74c71c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021042"
---
# <span data-ttu-id="8e40d-101">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8e40d-101">Set-AzRouteFilter</span></span>

## <span data-ttu-id="8e40d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8e40d-102">SYNOPSIS</span></span>
<span data-ttu-id="8e40d-103">Aggiorna un filtro di route.</span><span class="sxs-lookup"><span data-stu-id="8e40d-103">Updates a route filter.</span></span>

## <span data-ttu-id="8e40d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8e40d-104">SYNTAX</span></span>

```
Set-AzRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e40d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8e40d-105">DESCRIPTION</span></span>
<span data-ttu-id="8e40d-106">Il cmdlet **set-AzApplicationGateway** aggiorna un filtro di route</span><span class="sxs-lookup"><span data-stu-id="8e40d-106">The **Set-AzApplicationGateway** cmdlet updates a route filter</span></span>

## <span data-ttu-id="8e40d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8e40d-107">EXAMPLES</span></span>

### <span data-ttu-id="8e40d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8e40d-108">Example 1</span></span>
```powershell
PS C:\> Set-AzRouteFilter -RouteFilter $rf
```

<span data-ttu-id="8e40d-109">Questo comando Aggiorna il filtro della route con le impostazioni nella variabile $rf.</span><span class="sxs-lookup"><span data-stu-id="8e40d-109">This command updates the route filter with settings in the $rf variable.</span></span>

## <span data-ttu-id="8e40d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8e40d-110">PARAMETERS</span></span>

### <span data-ttu-id="8e40d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e40d-111">-AsJob</span></span>
<span data-ttu-id="8e40d-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="8e40d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8e40d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e40d-113">-DefaultProfile</span></span>
<span data-ttu-id="8e40d-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8e40d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e40d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8e40d-115">-Force</span></span>
<span data-ttu-id="8e40d-116">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="8e40d-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="8e40d-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="8e40d-117">-RouteFilter</span></span>
<span data-ttu-id="8e40d-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="8e40d-118">The RouteFilter</span></span>

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

### <span data-ttu-id="8e40d-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8e40d-119">-Confirm</span></span>
<span data-ttu-id="8e40d-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e40d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e40d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e40d-121">-WhatIf</span></span>
<span data-ttu-id="8e40d-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8e40d-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8e40d-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8e40d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e40d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e40d-124">CommonParameters</span></span>
<span data-ttu-id="8e40d-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e40d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e40d-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e40d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e40d-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8e40d-127">INPUTS</span></span>

### <span data-ttu-id="8e40d-128">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8e40d-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="8e40d-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8e40d-129">OUTPUTS</span></span>

### <span data-ttu-id="8e40d-130">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8e40d-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="8e40d-131">Note</span><span class="sxs-lookup"><span data-stu-id="8e40d-131">NOTES</span></span>

## <span data-ttu-id="8e40d-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8e40d-132">RELATED LINKS</span></span>

[<span data-ttu-id="8e40d-133">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8e40d-133">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="8e40d-134">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8e40d-134">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="8e40d-135">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8e40d-135">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="8e40d-136">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8e40d-136">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="8e40d-137">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8e40d-137">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="8e40d-138">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8e40d-138">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="8e40d-139">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8e40d-139">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="8e40d-140">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8e40d-140">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
