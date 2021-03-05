---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
ms.openlocfilehash: 0b75cdb63d2a8bb3c01a93a90ee01db096cf7fa5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976621"
---
# <span data-ttu-id="9f88b-101">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9f88b-101">Remove-AzRouteFilter</span></span>

## <span data-ttu-id="9f88b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f88b-102">SYNOPSIS</span></span>
<span data-ttu-id="9f88b-103">Rimuove un filtro della route.</span><span class="sxs-lookup"><span data-stu-id="9f88b-103">Removes a route filter.</span></span>

## <span data-ttu-id="9f88b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9f88b-104">SYNTAX</span></span>

```
Remove-AzRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f88b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9f88b-105">DESCRIPTION</span></span>
<span data-ttu-id="9f88b-106">Il cmdlet **Remove-AzRouteFilter** rimuove un filtro delle route.</span><span class="sxs-lookup"><span data-stu-id="9f88b-106">The **Remove-AzRouteFilter** cmdlet removes a route filter.</span></span>

## <span data-ttu-id="9f88b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9f88b-107">EXAMPLES</span></span>

### <span data-ttu-id="9f88b-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9f88b-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="9f88b-109">Il comando rimuove il filtro delle route denominato RouteFilter01 nel gruppo di risorse denominato ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="9f88b-109">The command removes the route filter named RouteFilter01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="9f88b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f88b-110">PARAMETERS</span></span>

### <span data-ttu-id="9f88b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f88b-111">-DefaultProfile</span></span>
<span data-ttu-id="9f88b-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9f88b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f88b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="9f88b-113">-Force</span></span>
<span data-ttu-id="9f88b-114">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="9f88b-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9f88b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="9f88b-115">-Name</span></span>
<span data-ttu-id="9f88b-116">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="9f88b-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f88b-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9f88b-117">-PassThru</span></span>
<span data-ttu-id="9f88b-118">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="9f88b-118">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="9f88b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f88b-119">-ResourceGroupName</span></span>
<span data-ttu-id="9f88b-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9f88b-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f88b-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9f88b-121">-Confirm</span></span>
<span data-ttu-id="9f88b-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f88b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f88b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f88b-123">-WhatIf</span></span>
<span data-ttu-id="9f88b-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9f88b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f88b-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9f88b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f88b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f88b-126">CommonParameters</span></span>
<span data-ttu-id="9f88b-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f88b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f88b-128">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f88b-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f88b-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="9f88b-129">INPUTS</span></span>

### <span data-ttu-id="9f88b-130">System.String</span><span class="sxs-lookup"><span data-stu-id="9f88b-130">System.String</span></span>

## <span data-ttu-id="9f88b-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9f88b-131">OUTPUTS</span></span>

### <span data-ttu-id="9f88b-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9f88b-132">System.Boolean</span></span>

## <span data-ttu-id="9f88b-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="9f88b-133">NOTES</span></span>

## <span data-ttu-id="9f88b-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9f88b-134">RELATED LINKS</span></span>

[<span data-ttu-id="9f88b-135">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9f88b-135">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="9f88b-136">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9f88b-136">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="9f88b-137">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9f88b-137">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="9f88b-138">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9f88b-138">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="9f88b-139">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9f88b-139">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="9f88b-140">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9f88b-140">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="9f88b-141">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9f88b-141">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="9f88b-142">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9f88b-142">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
