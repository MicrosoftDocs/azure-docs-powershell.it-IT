---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
ms.openlocfilehash: d66a684b6cd9b26aa9d616a74a4d2eaabaa891ff
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189639"
---
# <span data-ttu-id="01fb2-101">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="01fb2-101">New-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="01fb2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01fb2-102">SYNOPSIS</span></span>
<span data-ttu-id="01fb2-103">Crea una regola di filtro della route per un filtro delle route.</span><span class="sxs-lookup"><span data-stu-id="01fb2-103">Creates a route filter rule for a route filter.</span></span>

## <span data-ttu-id="01fb2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="01fb2-104">SYNTAX</span></span>

```
New-AzRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01fb2-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="01fb2-105">DESCRIPTION</span></span>
<span data-ttu-id="01fb2-106">Il cmdlet New-AzRouteFilterRuleConfig crea una regola di filtro delle route per un filtro delle route di Azure.</span><span class="sxs-lookup"><span data-stu-id="01fb2-106">The New-AzRouteFilterRuleConfig cmdlet creates a route filter rule for an Azure route filter.</span></span>

## <span data-ttu-id="01fb2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="01fb2-107">EXAMPLES</span></span>

### <span data-ttu-id="01fb2-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="01fb2-108">Example 1</span></span>
```powershell
PS C:\> $rule1 = New-AzRouteFilterRuleConfig -Name "Rule01" -Access "Allow" -RouteFilterRuleType "Community" -CommunityList "12076:5040"
```

<span data-ttu-id="01fb2-109">Il comando crea una nuova regola di filtro delle route e la archivia in $rule 1.</span><span class="sxs-lookup"><span data-stu-id="01fb2-109">The command creates a new route filter rule and stores it in variable $rule1.</span></span>

## <span data-ttu-id="01fb2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01fb2-110">PARAMETERS</span></span>

### <span data-ttu-id="01fb2-111">-Access</span><span class="sxs-lookup"><span data-stu-id="01fb2-111">-Access</span></span>
<span data-ttu-id="01fb2-112">Accesso per la regola di filtro delle route.</span><span class="sxs-lookup"><span data-stu-id="01fb2-112">Access for route filter rule.</span></span>
<span data-ttu-id="01fb2-113">I valori validi sono Consenti o Nega.</span><span class="sxs-lookup"><span data-stu-id="01fb2-113">Valid values are Allow or Deny.</span></span>

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

### <span data-ttu-id="01fb2-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="01fb2-114">-CommunityList</span></span>
<span data-ttu-id="01fb2-115">Elenco di valori community in base a cui verrà filtrato il filtro della route</span><span class="sxs-lookup"><span data-stu-id="01fb2-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="01fb2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01fb2-116">-DefaultProfile</span></span>
<span data-ttu-id="01fb2-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="01fb2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01fb2-118">-Force</span><span class="sxs-lookup"><span data-stu-id="01fb2-118">-Force</span></span>
<span data-ttu-id="01fb2-119">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="01fb2-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="01fb2-120">-Name</span><span class="sxs-lookup"><span data-stu-id="01fb2-120">-Name</span></span>
<span data-ttu-id="01fb2-121">Specifica un nome per la regola di filtro delle route.</span><span class="sxs-lookup"><span data-stu-id="01fb2-121">Specifies a name for the route filter rule.</span></span>

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

### <span data-ttu-id="01fb2-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="01fb2-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="01fb2-123">Tipo di regola del filtro della route.</span><span class="sxs-lookup"><span data-stu-id="01fb2-123">Route Filter Rule Type.</span></span>
<span data-ttu-id="01fb2-124">I valori validi sono: Community</span><span class="sxs-lookup"><span data-stu-id="01fb2-124">Valid values are: Community</span></span>

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

### <span data-ttu-id="01fb2-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01fb2-125">-Confirm</span></span>
<span data-ttu-id="01fb2-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01fb2-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01fb2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01fb2-127">-WhatIf</span></span>
<span data-ttu-id="01fb2-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="01fb2-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="01fb2-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="01fb2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01fb2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01fb2-130">CommonParameters</span></span>
<span data-ttu-id="01fb2-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01fb2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01fb2-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01fb2-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01fb2-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="01fb2-133">INPUTS</span></span>

### <span data-ttu-id="01fb2-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="01fb2-134">None</span></span>

## <span data-ttu-id="01fb2-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="01fb2-135">OUTPUTS</span></span>

### <span data-ttu-id="01fb2-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="01fb2-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="01fb2-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="01fb2-137">NOTES</span></span>
<span data-ttu-id="01fb2-138">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, rete, rete</span><span class="sxs-lookup"><span data-stu-id="01fb2-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="01fb2-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="01fb2-139">RELATED LINKS</span></span>

[<span data-ttu-id="01fb2-140">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="01fb2-140">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="01fb2-141">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="01fb2-141">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="01fb2-142">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="01fb2-142">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="01fb2-143">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="01fb2-143">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="01fb2-144">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="01fb2-144">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="01fb2-145">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="01fb2-145">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="01fb2-146">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="01fb2-146">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="01fb2-147">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="01fb2-147">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
