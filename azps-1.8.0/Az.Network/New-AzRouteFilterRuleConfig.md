---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
ms.openlocfilehash: d8213ecbbd331fdbff2e4a94fc690d2953d0d70a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678236"
---
# <span data-ttu-id="32aa0-101">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="32aa0-101">New-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="32aa0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="32aa0-102">SYNOPSIS</span></span>
<span data-ttu-id="32aa0-103">Crea una regola di filtro route per un filtro di route.</span><span class="sxs-lookup"><span data-stu-id="32aa0-103">Creates a route filter rule for a route filter.</span></span>

## <span data-ttu-id="32aa0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="32aa0-104">SYNTAX</span></span>

```
New-AzRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32aa0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32aa0-105">DESCRIPTION</span></span>
<span data-ttu-id="32aa0-106">Il cmdlet New-AzRouteFilterRuleConfig crea una regola di filtro route per un filtro di route di Azure.</span><span class="sxs-lookup"><span data-stu-id="32aa0-106">The New-AzRouteFilterRuleConfig cmdlet creates a route filter rule for an Azure route filter.</span></span>

## <span data-ttu-id="32aa0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="32aa0-107">EXAMPLES</span></span>

### <span data-ttu-id="32aa0-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="32aa0-108">Example 1</span></span>
```powershell
PS C:\> $rule1 = New-AzRouteFilterRuleConfig -Name "Rule01" -Access "Allow" -RouteFilterRuleType "Community" -CommunityList "12076:5040"
```

<span data-ttu-id="32aa0-109">Il comando crea una nuova regola di filtro della route e la archivia in una variabile $rule 1.</span><span class="sxs-lookup"><span data-stu-id="32aa0-109">The command creates a new route filter rule and stores it in variable $rule1.</span></span>

## <span data-ttu-id="32aa0-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="32aa0-110">PARAMETERS</span></span>

### <span data-ttu-id="32aa0-111">-Access</span><span class="sxs-lookup"><span data-stu-id="32aa0-111">-Access</span></span>
<span data-ttu-id="32aa0-112">Accesso per la regola di filtro route.</span><span class="sxs-lookup"><span data-stu-id="32aa0-112">Access for route filter rule.</span></span>
<span data-ttu-id="32aa0-113">I valori validi sono allow o Deny.</span><span class="sxs-lookup"><span data-stu-id="32aa0-113">Valid values are Allow or Deny.</span></span>

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

### <span data-ttu-id="32aa0-114">-Community</span><span class="sxs-lookup"><span data-stu-id="32aa0-114">-CommunityList</span></span>
<span data-ttu-id="32aa0-115">Elenco di valori della community a cui il filtro route verrà filtrato</span><span class="sxs-lookup"><span data-stu-id="32aa0-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="32aa0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32aa0-116">-DefaultProfile</span></span>
<span data-ttu-id="32aa0-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="32aa0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32aa0-118">-Force</span><span class="sxs-lookup"><span data-stu-id="32aa0-118">-Force</span></span>
<span data-ttu-id="32aa0-119">Non chiedere conferma se si vuole usare una risorsa per un sovrarito</span><span class="sxs-lookup"><span data-stu-id="32aa0-119">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="32aa0-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="32aa0-120">-Name</span></span>
<span data-ttu-id="32aa0-121">Specifica un nome per la regola di filtro della route.</span><span class="sxs-lookup"><span data-stu-id="32aa0-121">Specifies a name for the route filter rule.</span></span>

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

### <span data-ttu-id="32aa0-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="32aa0-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="32aa0-123">Tipo di regola filtro route.</span><span class="sxs-lookup"><span data-stu-id="32aa0-123">Route Filter Rule Type.</span></span>
<span data-ttu-id="32aa0-124">I valori validi sono: community</span><span class="sxs-lookup"><span data-stu-id="32aa0-124">Valid values are: Community</span></span>

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

### <span data-ttu-id="32aa0-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="32aa0-125">-Confirm</span></span>
<span data-ttu-id="32aa0-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32aa0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32aa0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32aa0-127">-WhatIf</span></span>
<span data-ttu-id="32aa0-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="32aa0-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="32aa0-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="32aa0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32aa0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32aa0-130">CommonParameters</span></span>
<span data-ttu-id="32aa0-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32aa0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32aa0-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32aa0-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32aa0-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="32aa0-133">INPUTS</span></span>

### <span data-ttu-id="32aa0-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="32aa0-134">None</span></span>

## <span data-ttu-id="32aa0-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="32aa0-135">OUTPUTS</span></span>

### <span data-ttu-id="32aa0-136">Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="32aa0-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="32aa0-137">Note</span><span class="sxs-lookup"><span data-stu-id="32aa0-137">NOTES</span></span>
<span data-ttu-id="32aa0-138">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="32aa0-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="32aa0-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="32aa0-139">RELATED LINKS</span></span>

[<span data-ttu-id="32aa0-140">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="32aa0-140">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="32aa0-141">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="32aa0-141">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="32aa0-142">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="32aa0-142">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="32aa0-143">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="32aa0-143">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="32aa0-144">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="32aa0-144">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="32aa0-145">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="32aa0-145">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="32aa0-146">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="32aa0-146">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="32aa0-147">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="32aa0-147">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)