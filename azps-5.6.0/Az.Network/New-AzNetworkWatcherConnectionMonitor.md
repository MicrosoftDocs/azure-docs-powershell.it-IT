---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 18db8d01bd9c6c54b1fdf3957f25e12848e309ae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958541"
---
# <span data-ttu-id="d0f88-101">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d0f88-101">New-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="d0f88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0f88-102">SYNOPSIS</span></span>
<span data-ttu-id="d0f88-103">Crea una risorsa di Monitor connessione.</span><span class="sxs-lookup"><span data-stu-id="d0f88-103">Creates a connection monitor resource.</span></span>

## <span data-ttu-id="d0f88-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d0f88-104">SYNTAX</span></span>

### <span data-ttu-id="d0f88-105">SetByName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d0f88-105">SetByName (Default)</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d0f88-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d0f88-106">SetByResource</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d0f88-107">SetByResourceV2</span><span class="sxs-lookup"><span data-stu-id="d0f88-107">SetByResourceV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0f88-108">SetByNameV2</span><span class="sxs-lookup"><span data-stu-id="d0f88-108">SetByNameV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0f88-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="d0f88-109">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0f88-110">SetByLocationV2</span><span class="sxs-lookup"><span data-stu-id="d0f88-110">SetByLocationV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0f88-111">SetByConnectionMonitorV2Object</span><span class="sxs-lookup"><span data-stu-id="d0f88-111">SetByConnectionMonitorV2Object</span></span>
```
New-AzNetworkWatcherConnectionMonitor [-ConnectionMonitor <PSNetworkWatcherConnectionMonitorObject>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0f88-112">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d0f88-112">DESCRIPTION</span></span>
<span data-ttu-id="d0f88-113">Il cmdlet New-AzNetworkWatcherConnectionMonitor crea una risorsa di monitoraggio della connessione per il monitor di connessione specificato di origine e destinazione (monitor di connessione SingleSourcedestination) o set di gruppi di test (MultiEndpointConnectionMonitor).</span><span class="sxs-lookup"><span data-stu-id="d0f88-113">The New-AzNetworkWatcherConnectionMonitor cmdlet creates a connection monitor resource for specified source and destination (SingleSourcedestination connection monitor) or set of test groups (MultiEndpointConnectionMonitor).</span></span>

## <span data-ttu-id="d0f88-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d0f88-114">EXAMPLES</span></span>

### <span data-ttu-id="d0f88-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d0f88-115">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm -DestinationAddress bing.com -DestinationPort 80
```

<span data-ttu-id="d0f88-116">Nome : cm ID : /subscriptions/00000000-0000-0000-0000-00000000000/resourceGro ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/t1 Etag : W/"e86b28cf-b907--4475-a8b7-34d310367694" ProvisioningState: Succeeded Source: { "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000 000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft. Compute/virtualMachines/vm", "Port": 0 } Destinazione: { "Address": "bing.com", "Port": 80 } MonitoringIntervalInSeconds : 60 AutoStart : True StartTime : 12/1/2018 7:13:11 PM MonitoringStatus : Running Location : centraluseuap Type : Microsoft.Network/networkWatchers/connectionMonitors Tags : {}</span><span class="sxs-lookup"><span data-stu-id="d0f88-116">Name                        : cm Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/t1 Etag                        : W/"e86b28cf-b907-4475-a8b7-34d310367694" ProvisioningState           : Succeeded Source                      : { "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000 00000/resourceGroups/RgCentralUSEUAP/providers/Microsoft .Compute/virtualMachines/vm", "Port": 0 } Destination                 : { "Address": "bing.com", "Port": 80 } MonitoringIntervalInSeconds : 60 AutoStart                   : True StartTime                   : 1/12/2018 7:13:11 PM MonitoringStatus            : Running Location                    : centraluseuap Type                        : Microsoft.Network/networkWatchers/connectionMonitors Tags                        : {}</span></span>

## <span data-ttu-id="d0f88-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0f88-117">PARAMETERS</span></span>

### <span data-ttu-id="d0f88-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0f88-118">-AsJob</span></span>
<span data-ttu-id="d0f88-119">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d0f88-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d0f88-120">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="d0f88-120">-ConfigureOnly</span></span>
<span data-ttu-id="d0f88-121">Configurare il monitor di connessione, ma non avviarlo</span><span class="sxs-lookup"><span data-stu-id="d0f88-121">Configure connection monitor, but do not start it</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0f88-122">-ConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d0f88-122">-ConnectionMonitor</span></span>
<span data-ttu-id="d0f88-123">Oggetto monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="d0f88-123">Connection monitor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorObject
Parameter Sets: SetByConnectionMonitorV2Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0f88-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0f88-124">-DefaultProfile</span></span>
<span data-ttu-id="d0f88-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d0f88-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0f88-126">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="d0f88-126">-DestinationAddress</span></span>
<span data-ttu-id="d0f88-127">Indirizzo della destinazione del monitor di connessione (IP o nome di dominio).</span><span class="sxs-lookup"><span data-stu-id="d0f88-127">Address of the connection monitor destination (IP or domain name).</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0f88-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="d0f88-128">-DestinationPort</span></span>
<span data-ttu-id="d0f88-129">Porta di destinazione utilizzata dal monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="d0f88-129">The destination port used by connection monitor.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0f88-130">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="d0f88-130">-DestinationResourceId</span></span>
<span data-ttu-id="d0f88-131">ID della risorsa usata come destinazione dal monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="d0f88-131">The ID of the resource used as the destination by connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0f88-132">-Force</span><span class="sxs-lookup"><span data-stu-id="d0f88-132">-Force</span></span>
<span data-ttu-id="d0f88-133">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="d0f88-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="d0f88-134">-Location</span><span class="sxs-lookup"><span data-stu-id="d0f88-134">-Location</span></span>
<span data-ttu-id="d0f88-135">Posizione del network watcher.</span><span class="sxs-lookup"><span data-stu-id="d0f88-135">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation, SetByLocationV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0f88-136">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="d0f88-136">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="d0f88-137">Intervallo di monitoraggio in secondi.</span><span class="sxs-lookup"><span data-stu-id="d0f88-137">Monitoring interval in seconds.</span></span> <span data-ttu-id="d0f88-138">Il valore predefinito è 60 secondi.</span><span class="sxs-lookup"><span data-stu-id="d0f88-138">Default value is 60 seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0f88-139">-Name</span><span class="sxs-lookup"><span data-stu-id="d0f88-139">-Name</span></span>
<span data-ttu-id="d0f88-140">Nome del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="d0f88-140">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByResourceV2, SetByNameV2, SetByLocation, SetByLocationV2
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0f88-141">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d0f88-141">-NetworkWatcher</span></span>
<span data-ttu-id="d0f88-142">Risorsa Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="d0f88-142">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource, SetByResourceV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0f88-143">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d0f88-143">-NetworkWatcherName</span></span>
<span data-ttu-id="d0f88-144">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="d0f88-144">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByNameV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0f88-145">-Nota</span><span class="sxs-lookup"><span data-stu-id="d0f88-145">-Note</span></span>
<span data-ttu-id="d0f88-146">Note associate al monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="d0f88-146">Notes associated with connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceV2, SetByNameV2, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0f88-147">-Output</span><span class="sxs-lookup"><span data-stu-id="d0f88-147">-Output</span></span>
<span data-ttu-id="d0f88-148">Descrive le destinazioni di output del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="d0f88-148">Describes a connection monitor output destinations.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject[]
Parameter Sets: SetByResourceV2, SetByNameV2, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0f88-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0f88-149">-ResourceGroupName</span></span>
<span data-ttu-id="d0f88-150">Nome del gruppo di risorse Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="d0f88-150">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByNameV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0f88-151">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="d0f88-151">-SourcePort</span></span>
<span data-ttu-id="d0f88-152">La porta di origine usata dal monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="d0f88-152">The source port used by connection monitor.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0f88-153">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="d0f88-153">-SourceResourceId</span></span>
<span data-ttu-id="d0f88-154">ID della risorsa usata come origine dal monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="d0f88-154">The ID of the resource used as the source by connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0f88-155">-Tag</span><span class="sxs-lookup"><span data-stu-id="d0f88-155">-Tag</span></span>
<span data-ttu-id="d0f88-156">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="d0f88-156">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: SetByName, SetByResource, SetByResourceV2, SetByNameV2, SetByLocation, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0f88-157">-TestGroup</span><span class="sxs-lookup"><span data-stu-id="d0f88-157">-TestGroup</span></span>
<span data-ttu-id="d0f88-158">Elenco dei gruppi di test.</span><span class="sxs-lookup"><span data-stu-id="d0f88-158">The list of test groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject[]
Parameter Sets: SetByResourceV2, SetByNameV2, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0f88-159">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d0f88-159">-Confirm</span></span>
<span data-ttu-id="d0f88-160">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0f88-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0f88-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0f88-161">-WhatIf</span></span>
<span data-ttu-id="d0f88-162">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d0f88-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0f88-163">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d0f88-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0f88-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0f88-164">CommonParameters</span></span>
<span data-ttu-id="d0f88-165">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0f88-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0f88-166">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d0f88-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0f88-167">INPUT</span><span class="sxs-lookup"><span data-stu-id="d0f88-167">INPUTS</span></span>

### <span data-ttu-id="d0f88-168">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d0f88-168">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="d0f88-169">System.String</span><span class="sxs-lookup"><span data-stu-id="d0f88-169">System.String</span></span>

### <span data-ttu-id="d0f88-170">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="d0f88-170">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="d0f88-171">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="d0f88-171">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d0f88-172">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d0f88-172">OUTPUTS</span></span>

### <span data-ttu-id="d0f88-173">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="d0f88-173">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="d0f88-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="d0f88-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="d0f88-175">NOTE</span><span class="sxs-lookup"><span data-stu-id="d0f88-175">NOTES</span></span>

## <span data-ttu-id="d0f88-176">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d0f88-176">RELATED LINKS</span></span>
