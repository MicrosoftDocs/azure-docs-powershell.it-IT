---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
ms.openlocfilehash: 5a29c0bbad712d99b03ab1ff5347cba5c07b02aa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206698"
---
# <span data-ttu-id="12207-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="12207-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="12207-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12207-102">SYNOPSIS</span></span>
<span data-ttu-id="12207-103">Crea l'endpoint del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="12207-103">Creates connection monitor endpoint.</span></span>

## <span data-ttu-id="12207-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="12207-104">SYNTAX</span></span>

### <span data-ttu-id="12207-105">AzureVM</span><span class="sxs-lookup"><span data-stu-id="12207-105">AzureVM</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureVM] -ResourceId <String>
 [-Address <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12207-106">AzureVNet</span><span class="sxs-lookup"><span data-stu-id="12207-106">AzureVNet</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureVNet] -ResourceId <String>
 [-IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>]
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12207-107">AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="12207-107">AzureSubnet</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureSubnet] -ResourceId <String>
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12207-108">ExternalAddress</span><span class="sxs-lookup"><span data-stu-id="12207-108">ExternalAddress</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-ExternalAddress] -Address <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12207-109">MMAWorkspaceMachine</span><span class="sxs-lookup"><span data-stu-id="12207-109">MMAWorkspaceMachine</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-MMAWorkspaceMachine] -ResourceId <String>
 -Address <String> [-IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12207-110">MMAWorkspaceNetwork</span><span class="sxs-lookup"><span data-stu-id="12207-110">MMAWorkspaceNetwork</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-MMAWorkspaceNetwork] -ResourceId <String>
 -IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12207-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="12207-111">DESCRIPTION</span></span>
<span data-ttu-id="12207-112">New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet crea l'endpoint del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="12207-112">New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet creates connection monitor endpoint.</span></span>

## <span data-ttu-id="12207-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="12207-113">EXAMPLES</span></span>

### <span data-ttu-id="12207-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="12207-114">Example 1</span></span>
```powershell
PS C:\>$MySrcResourceId1 = "/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace"
PS C:\>$SrcEndpointScopeItem1 = New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject -Address "WIN-P0HGNDO2S1B"
PS C:\>$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndpointObject -Name "workspaceEndpoint" -MMAWorkspaceMachine -ResourceId $MySrcResourceId1 -IncludeItem $SrcEndpointScopeItem1
```

<span data-ttu-id="12207-115">Nome : workspaceEndpoint Type : MMAWorkspaceMachine ResourceId : /subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address : Scope : { "Include": [ { "Address": "WIN-P0HGNDO2S1B" } ] } }</span><span class="sxs-lookup"><span data-stu-id="12207-115">Name       : workspaceEndpoint Type       : MMAWorkspaceMachine ResourceId : /subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address    : Scope     : { "Include": [ { "Address": "WIN-P0HGNDO2S1B" } ] }</span></span>

## <span data-ttu-id="12207-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12207-116">PARAMETERS</span></span>

### <span data-ttu-id="12207-117">-Address</span><span class="sxs-lookup"><span data-stu-id="12207-117">-Address</span></span>
<span data-ttu-id="12207-118">Indirizzo dell'endpoint del monitor di connessione (IP o nome di dominio).</span><span class="sxs-lookup"><span data-stu-id="12207-118">Address of the connection monitor endpoint (IP or domain name).</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVM
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExternalAddress, MMAWorkspaceMachine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12207-119">-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="12207-119">-AzureSubnet</span></span>
<span data-ttu-id="12207-120">Passaggio all'endpoint della subnet di Azure.</span><span class="sxs-lookup"><span data-stu-id="12207-120">Azure Subnet endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12207-121">-AzureVM</span><span class="sxs-lookup"><span data-stu-id="12207-121">-AzureVM</span></span>
<span data-ttu-id="12207-122">Parametro endpoint della macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="12207-122">Azure VM endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVM
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12207-123">-AzureVNet</span><span class="sxs-lookup"><span data-stu-id="12207-123">-AzureVNet</span></span>
<span data-ttu-id="12207-124">Parametro endpoint Azure Vnet.</span><span class="sxs-lookup"><span data-stu-id="12207-124">Azure Vnet endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVNet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12207-125">-CoverageLevel</span><span class="sxs-lookup"><span data-stu-id="12207-125">-CoverageLevel</span></span>
<span data-ttu-id="12207-126">Copertura del test per l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="12207-126">Test coverage for the endpoint.</span></span>
<span data-ttu-id="12207-127">I valori supportati sono Default, Low, BelowAverage, Average, AboveAvergae, Full.</span><span class="sxs-lookup"><span data-stu-id="12207-127">Supported values are Default, Low, BelowAverage, Average, AboveAvergae, Full.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVNet, AzureSubnet, MMAWorkspaceNetwork
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12207-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12207-128">-DefaultProfile</span></span>
<span data-ttu-id="12207-129">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="12207-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12207-130">-ExcludeItem</span><span class="sxs-lookup"><span data-stu-id="12207-130">-ExcludeItem</span></span>
<span data-ttu-id="12207-131">Elenco degli elementi da escludere dall'ambito dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="12207-131">List of items which need to be excluded from endpoint scope.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem[]
Parameter Sets: AzureVNet, AzureSubnet, MMAWorkspaceNetwork
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12207-132">-ExternalAddress</span><span class="sxs-lookup"><span data-stu-id="12207-132">-ExternalAddress</span></span>
<span data-ttu-id="12207-133">Parametro endpoint Indirizzo esterno.</span><span class="sxs-lookup"><span data-stu-id="12207-133">External Address endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExternalAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12207-134">-IncludeItem</span><span class="sxs-lookup"><span data-stu-id="12207-134">-IncludeItem</span></span>
<span data-ttu-id="12207-135">Elenco degli elementi da includere nell'ambito end scope.</span><span class="sxs-lookup"><span data-stu-id="12207-135">List of items which need to be included into endpont scope.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem[]
Parameter Sets: AzureVNet, MMAWorkspaceMachine
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem[]
Parameter Sets: MMAWorkspaceNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12207-136">-MMAWorkspaceMachine</span><span class="sxs-lookup"><span data-stu-id="12207-136">-MMAWorkspaceMachine</span></span>
<span data-ttu-id="12207-137">Parametro endpoint MMA Workspace Machine.</span><span class="sxs-lookup"><span data-stu-id="12207-137">MMA Workspace Machine endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MMAWorkspaceMachine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12207-138">-MMAWorkspaceNetwork</span><span class="sxs-lookup"><span data-stu-id="12207-138">-MMAWorkspaceNetwork</span></span>
<span data-ttu-id="12207-139">Passaggio all'endpoint di rete dell'area di lavoro MMA.</span><span class="sxs-lookup"><span data-stu-id="12207-139">MMA Workspace Network endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MMAWorkspaceNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12207-140">-Name</span><span class="sxs-lookup"><span data-stu-id="12207-140">-Name</span></span>
<span data-ttu-id="12207-141">Nome dell'endpoint del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="12207-141">The name of the connection monitor endpoint.</span></span>

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

### <span data-ttu-id="12207-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12207-142">-ResourceId</span></span>
<span data-ttu-id="12207-143">ID risorsa dell'endpoint del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="12207-143">Resource ID of the connection monitor endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVM, AzureVNet, AzureSubnet, MMAWorkspaceMachine, MMAWorkspaceNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12207-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="12207-144">-Confirm</span></span>
<span data-ttu-id="12207-145">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12207-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12207-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12207-146">-WhatIf</span></span>
<span data-ttu-id="12207-147">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="12207-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12207-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="12207-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12207-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12207-149">CommonParameters</span></span>
<span data-ttu-id="12207-150">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12207-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12207-151">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="12207-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12207-152">INPUT</span><span class="sxs-lookup"><span data-stu-id="12207-152">INPUTS</span></span>

### <span data-ttu-id="12207-153">Nessuno</span><span class="sxs-lookup"><span data-stu-id="12207-153">None</span></span>

## <span data-ttu-id="12207-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="12207-154">OUTPUTS</span></span>

### <span data-ttu-id="12207-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="12207-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="12207-156">NOTE</span><span class="sxs-lookup"><span data-stu-id="12207-156">NOTES</span></span>

## <span data-ttu-id="12207-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="12207-157">RELATED LINKS</span></span>
