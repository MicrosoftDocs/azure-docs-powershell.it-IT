---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
ms.openlocfilehash: 5a29c0bbad712d99b03ab1ff5347cba5c07b02aa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301453"
---
# <span data-ttu-id="704e2-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="704e2-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="704e2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="704e2-102">SYNOPSIS</span></span>
<span data-ttu-id="704e2-103">Crea endpoint di monitoraggio connessione.</span><span class="sxs-lookup"><span data-stu-id="704e2-103">Creates connection monitor endpoint.</span></span>

## <span data-ttu-id="704e2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="704e2-104">SYNTAX</span></span>

### <span data-ttu-id="704e2-105">AzureVM</span><span class="sxs-lookup"><span data-stu-id="704e2-105">AzureVM</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureVM] -ResourceId <String>
 [-Address <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="704e2-106">AzureVNet</span><span class="sxs-lookup"><span data-stu-id="704e2-106">AzureVNet</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureVNet] -ResourceId <String>
 [-IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>]
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="704e2-107">AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="704e2-107">AzureSubnet</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureSubnet] -ResourceId <String>
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="704e2-108">ExternalAddress</span><span class="sxs-lookup"><span data-stu-id="704e2-108">ExternalAddress</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-ExternalAddress] -Address <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="704e2-109">MMAWorkspaceMachine</span><span class="sxs-lookup"><span data-stu-id="704e2-109">MMAWorkspaceMachine</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-MMAWorkspaceMachine] -ResourceId <String>
 -Address <String> [-IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="704e2-110">MMAWorkspaceNetwork</span><span class="sxs-lookup"><span data-stu-id="704e2-110">MMAWorkspaceNetwork</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-MMAWorkspaceNetwork] -ResourceId <String>
 -IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="704e2-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="704e2-111">DESCRIPTION</span></span>
<span data-ttu-id="704e2-112">New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet crea endpoint di monitoraggio connessione.</span><span class="sxs-lookup"><span data-stu-id="704e2-112">New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet creates connection monitor endpoint.</span></span>

## <span data-ttu-id="704e2-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="704e2-113">EXAMPLES</span></span>

### <span data-ttu-id="704e2-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="704e2-114">Example 1</span></span>
```powershell
PS C:\>$MySrcResourceId1 = "/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace"
PS C:\>$SrcEndpointScopeItem1 = New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject -Address "WIN-P0HGNDO2S1B"
PS C:\>$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndpointObject -Name "workspaceEndpoint" -MMAWorkspaceMachine -ResourceId $MySrcResourceId1 -IncludeItem $SrcEndpointScopeItem1
```

<span data-ttu-id="704e2-115">Nome: workspaceEndpoint tipo: MMAWorkspaceMachine ResourceId:/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Indirizzo: ambito: {"Includi": [{"indirizzo": "WIN-P0HGNDO2S1B"}]}</span><span class="sxs-lookup"><span data-stu-id="704e2-115">Name       : workspaceEndpoint Type       : MMAWorkspaceMachine ResourceId : /subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address    : Scope     : { "Include": [ { "Address": "WIN-P0HGNDO2S1B" } ] }</span></span>

## <span data-ttu-id="704e2-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="704e2-116">PARAMETERS</span></span>

### <span data-ttu-id="704e2-117">-Address</span><span class="sxs-lookup"><span data-stu-id="704e2-117">-Address</span></span>
<span data-ttu-id="704e2-118">Indirizzo dell'endpoint di monitoraggio della connessione (IP o nome di dominio).</span><span class="sxs-lookup"><span data-stu-id="704e2-118">Address of the connection monitor endpoint (IP or domain name).</span></span>

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

### <span data-ttu-id="704e2-119">-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="704e2-119">-AzureSubnet</span></span>
<span data-ttu-id="704e2-120">Interruttore di endpoint della subnet di Azure.</span><span class="sxs-lookup"><span data-stu-id="704e2-120">Azure Subnet endpoint switch.</span></span>

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

### <span data-ttu-id="704e2-121">-AzureVM</span><span class="sxs-lookup"><span data-stu-id="704e2-121">-AzureVM</span></span>
<span data-ttu-id="704e2-122">Interruttore endpoint di Azure VM.</span><span class="sxs-lookup"><span data-stu-id="704e2-122">Azure VM endpoint switch.</span></span>

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

### <span data-ttu-id="704e2-123">-AzureVNet</span><span class="sxs-lookup"><span data-stu-id="704e2-123">-AzureVNet</span></span>
<span data-ttu-id="704e2-124">Interruttore endpoint di Azure vnet.</span><span class="sxs-lookup"><span data-stu-id="704e2-124">Azure Vnet endpoint switch.</span></span>

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

### <span data-ttu-id="704e2-125">-CoverageLevel</span><span class="sxs-lookup"><span data-stu-id="704e2-125">-CoverageLevel</span></span>
<span data-ttu-id="704e2-126">Verificare la copertura per l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="704e2-126">Test coverage for the endpoint.</span></span>
<span data-ttu-id="704e2-127">I valori supportati sono default, low, BelowAverage, Average, AboveAvergae, Full.</span><span class="sxs-lookup"><span data-stu-id="704e2-127">Supported values are Default, Low, BelowAverage, Average, AboveAvergae, Full.</span></span>

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

### <span data-ttu-id="704e2-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="704e2-128">-DefaultProfile</span></span>
<span data-ttu-id="704e2-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="704e2-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="704e2-130">-ExcludeItem</span><span class="sxs-lookup"><span data-stu-id="704e2-130">-ExcludeItem</span></span>
<span data-ttu-id="704e2-131">Elenco di elementi che devono essere esclusi dall'ambito dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="704e2-131">List of items which need to be excluded from endpoint scope.</span></span>

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

### <span data-ttu-id="704e2-132">-ExternalAddress</span><span class="sxs-lookup"><span data-stu-id="704e2-132">-ExternalAddress</span></span>
<span data-ttu-id="704e2-133">Opzione endpoint indirizzo esterno.</span><span class="sxs-lookup"><span data-stu-id="704e2-133">External Address endpoint switch.</span></span>

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

### <span data-ttu-id="704e2-134">-IncludeItem</span><span class="sxs-lookup"><span data-stu-id="704e2-134">-IncludeItem</span></span>
<span data-ttu-id="704e2-135">Elenco di elementi che devono essere inclusi nell'ambito endpont.</span><span class="sxs-lookup"><span data-stu-id="704e2-135">List of items which need to be included into endpont scope.</span></span>

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

### <span data-ttu-id="704e2-136">-MMAWorkspaceMachine</span><span class="sxs-lookup"><span data-stu-id="704e2-136">-MMAWorkspaceMachine</span></span>
<span data-ttu-id="704e2-137">Interruttore dell'endpoint della macchina dell'area di lavoro MMA.</span><span class="sxs-lookup"><span data-stu-id="704e2-137">MMA Workspace Machine endpoint switch.</span></span>

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

### <span data-ttu-id="704e2-138">-MMAWorkspaceNetwork</span><span class="sxs-lookup"><span data-stu-id="704e2-138">-MMAWorkspaceNetwork</span></span>
<span data-ttu-id="704e2-139">Switch endpoint di rete dell'area di lavoro MMA.</span><span class="sxs-lookup"><span data-stu-id="704e2-139">MMA Workspace Network endpoint switch.</span></span>

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

### <span data-ttu-id="704e2-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="704e2-140">-Name</span></span>
<span data-ttu-id="704e2-141">Nome dell'endpoint di monitoraggio della connessione.</span><span class="sxs-lookup"><span data-stu-id="704e2-141">The name of the connection monitor endpoint.</span></span>

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

### <span data-ttu-id="704e2-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="704e2-142">-ResourceId</span></span>
<span data-ttu-id="704e2-143">ID risorsa dell'endpoint di monitoraggio connessione.</span><span class="sxs-lookup"><span data-stu-id="704e2-143">Resource ID of the connection monitor endpoint.</span></span>

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

### <span data-ttu-id="704e2-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="704e2-144">-Confirm</span></span>
<span data-ttu-id="704e2-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="704e2-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="704e2-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="704e2-146">-WhatIf</span></span>
<span data-ttu-id="704e2-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="704e2-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="704e2-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="704e2-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="704e2-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="704e2-149">CommonParameters</span></span>
<span data-ttu-id="704e2-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="704e2-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="704e2-151">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="704e2-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="704e2-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="704e2-152">INPUTS</span></span>

### <span data-ttu-id="704e2-153">Nessuno</span><span class="sxs-lookup"><span data-stu-id="704e2-153">None</span></span>

## <span data-ttu-id="704e2-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="704e2-154">OUTPUTS</span></span>

### <span data-ttu-id="704e2-155">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="704e2-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="704e2-156">Note</span><span class="sxs-lookup"><span data-stu-id="704e2-156">NOTES</span></span>

## <span data-ttu-id="704e2-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="704e2-157">RELATED LINKS</span></span>
