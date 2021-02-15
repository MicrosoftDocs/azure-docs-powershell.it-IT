---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: b84d11f259ffbf606bf0538a2ff71f6e9999db0a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187039"
---
# <span data-ttu-id="352b0-101">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="352b0-101">New-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="352b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="352b0-102">SYNOPSIS</span></span>
<span data-ttu-id="352b0-103">Crea una risorsa di monitor della connessione.</span><span class="sxs-lookup"><span data-stu-id="352b0-103">Creates a connection monitor resource.</span></span>

## <span data-ttu-id="352b0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="352b0-104">SYNTAX</span></span>

### <span data-ttu-id="352b0-105">SetByName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="352b0-105">SetByName (Default)</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="352b0-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="352b0-106">SetByResource</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="352b0-107">SetByResourceV2</span><span class="sxs-lookup"><span data-stu-id="352b0-107">SetByResourceV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="352b0-108">SetByNameV2</span><span class="sxs-lookup"><span data-stu-id="352b0-108">SetByNameV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="352b0-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="352b0-109">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="352b0-110">SetByLocationV2</span><span class="sxs-lookup"><span data-stu-id="352b0-110">SetByLocationV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="352b0-111">SetByConnectionMonitorV2Object</span><span class="sxs-lookup"><span data-stu-id="352b0-111">SetByConnectionMonitorV2Object</span></span>
```
New-AzNetworkWatcherConnectionMonitor [-ConnectionMonitor <PSNetworkWatcherConnectionMonitorObject>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="352b0-112">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="352b0-112">DESCRIPTION</span></span>
<span data-ttu-id="352b0-113">Il cmdlet New-AzNetworkWatcherConnectionMonitor crea una risorsa di monitor di connessione per il monitor di connessione di origine e destinazione specificato (monitor di connessione SingleSourcedestination) o per un set di gruppi di test (MultiEndpointConnectionMonitor).</span><span class="sxs-lookup"><span data-stu-id="352b0-113">The New-AzNetworkWatcherConnectionMonitor cmdlet creates a connection monitor resource for specified source and destination (SingleSourcedestination connection monitor) or set of test groups (MultiEndpointConnectionMonitor).</span></span>

## <span data-ttu-id="352b0-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="352b0-114">EXAMPLES</span></span>

### <span data-ttu-id="352b0-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="352b0-115">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm -DestinationAddress bing.com -DestinationPort 80
```

<span data-ttu-id="352b0-116">Nome : cm ID : /subscriptions/00000000-0000-0000-0000-0000000000/resourceGro ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/t1 Etag : W/"e86b28cf-b907-4475-a8b7-34d310367694" ProvisioningState: Succeeded Source: { "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000 000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft. Compute/virtualMachines/vm", "Port": 0 } Destinazione: { "Address": "bing.com", "Port": 80 } MonitoringIntervalInSeconds : 60 AutoStart : True StartTime : 12/1/2018 7:13:11 PM MonitoringStatus : Running Location : centraluseuap Type : Microsoft.Network/networkWatchers/connectionMonitors Tags : {}</span><span class="sxs-lookup"><span data-stu-id="352b0-116">Name                        : cm Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/t1 Etag                        : W/"e86b28cf-b907-4475-a8b7-34d310367694" ProvisioningState           : Succeeded Source                      : { "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000 00000/resourceGroups/RgCentralUSEUAP/providers/Microsoft .Compute/virtualMachines/vm", "Port": 0 } Destination                 : { "Address": "bing.com", "Port": 80 } MonitoringIntervalInSeconds : 60 AutoStart                   : True StartTime                   : 1/12/2018 7:13:11 PM MonitoringStatus            : Running Location                    : centraluseuap Type                        : Microsoft.Network/networkWatchers/connectionMonitors Tags                        : {}</span></span>

## <span data-ttu-id="352b0-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="352b0-117">PARAMETERS</span></span>

### <span data-ttu-id="352b0-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="352b0-118">-AsJob</span></span>
<span data-ttu-id="352b0-119">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="352b0-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="352b0-120">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="352b0-120">-ConfigureOnly</span></span>
<span data-ttu-id="352b0-121">Configurare il monitor di connessione, ma non avviarlo</span><span class="sxs-lookup"><span data-stu-id="352b0-121">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="352b0-122">-ConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="352b0-122">-ConnectionMonitor</span></span>
<span data-ttu-id="352b0-123">Oggetto monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="352b0-123">Connection monitor object.</span></span>

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

### <span data-ttu-id="352b0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="352b0-124">-DefaultProfile</span></span>
<span data-ttu-id="352b0-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="352b0-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="352b0-126">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="352b0-126">-DestinationAddress</span></span>
<span data-ttu-id="352b0-127">Indirizzo della destinazione del monitor di connessione (IP o nome di dominio).</span><span class="sxs-lookup"><span data-stu-id="352b0-127">Address of the connection monitor destination (IP or domain name).</span></span>

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

### <span data-ttu-id="352b0-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="352b0-128">-DestinationPort</span></span>
<span data-ttu-id="352b0-129">Porta di destinazione utilizzata dal monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="352b0-129">The destination port used by connection monitor.</span></span>

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

### <span data-ttu-id="352b0-130">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="352b0-130">-DestinationResourceId</span></span>
<span data-ttu-id="352b0-131">ID della risorsa usata come destinazione dal monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="352b0-131">The ID of the resource used as the destination by connection monitor.</span></span>

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

### <span data-ttu-id="352b0-132">-Force</span><span class="sxs-lookup"><span data-stu-id="352b0-132">-Force</span></span>
<span data-ttu-id="352b0-133">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="352b0-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="352b0-134">-Location</span><span class="sxs-lookup"><span data-stu-id="352b0-134">-Location</span></span>
<span data-ttu-id="352b0-135">Posizione del network watcher.</span><span class="sxs-lookup"><span data-stu-id="352b0-135">Location of the network watcher.</span></span>

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

### <span data-ttu-id="352b0-136">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="352b0-136">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="352b0-137">Intervallo di monitoraggio in secondi.</span><span class="sxs-lookup"><span data-stu-id="352b0-137">Monitoring interval in seconds.</span></span> <span data-ttu-id="352b0-138">Il valore predefinito è 60 secondi.</span><span class="sxs-lookup"><span data-stu-id="352b0-138">Default value is 60 seconds.</span></span>

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

### <span data-ttu-id="352b0-139">-Name</span><span class="sxs-lookup"><span data-stu-id="352b0-139">-Name</span></span>
<span data-ttu-id="352b0-140">Nome del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="352b0-140">The connection monitor name.</span></span>

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

### <span data-ttu-id="352b0-141">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="352b0-141">-NetworkWatcher</span></span>
<span data-ttu-id="352b0-142">Risorsa Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="352b0-142">The network watcher resource.</span></span>

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

### <span data-ttu-id="352b0-143">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="352b0-143">-NetworkWatcherName</span></span>
<span data-ttu-id="352b0-144">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="352b0-144">The name of network watcher.</span></span>

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

### <span data-ttu-id="352b0-145">-Nota</span><span class="sxs-lookup"><span data-stu-id="352b0-145">-Note</span></span>
<span data-ttu-id="352b0-146">Note associate al monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="352b0-146">Notes associated with connection monitor.</span></span>

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

### <span data-ttu-id="352b0-147">-Output</span><span class="sxs-lookup"><span data-stu-id="352b0-147">-Output</span></span>
<span data-ttu-id="352b0-148">Descrive le destinazioni di output del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="352b0-148">Describes a connection monitor output destinations.</span></span>

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

### <span data-ttu-id="352b0-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="352b0-149">-ResourceGroupName</span></span>
<span data-ttu-id="352b0-150">Nome del gruppo di risorse Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="352b0-150">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="352b0-151">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="352b0-151">-SourcePort</span></span>
<span data-ttu-id="352b0-152">La porta di origine usata dal monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="352b0-152">The source port used by connection monitor.</span></span>

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

### <span data-ttu-id="352b0-153">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="352b0-153">-SourceResourceId</span></span>
<span data-ttu-id="352b0-154">ID della risorsa usata come origine dal monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="352b0-154">The ID of the resource used as the source by connection monitor.</span></span>

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

### <span data-ttu-id="352b0-155">-Tag</span><span class="sxs-lookup"><span data-stu-id="352b0-155">-Tag</span></span>
<span data-ttu-id="352b0-156">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="352b0-156">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="352b0-157">-TestGroup</span><span class="sxs-lookup"><span data-stu-id="352b0-157">-TestGroup</span></span>
<span data-ttu-id="352b0-158">Elenco dei gruppi di test.</span><span class="sxs-lookup"><span data-stu-id="352b0-158">The list of test groups.</span></span>

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

### <span data-ttu-id="352b0-159">-Confirm</span><span class="sxs-lookup"><span data-stu-id="352b0-159">-Confirm</span></span>
<span data-ttu-id="352b0-160">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="352b0-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="352b0-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="352b0-161">-WhatIf</span></span>
<span data-ttu-id="352b0-162">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="352b0-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="352b0-163">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="352b0-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="352b0-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="352b0-164">CommonParameters</span></span>
<span data-ttu-id="352b0-165">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="352b0-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="352b0-166">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="352b0-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="352b0-167">INPUT</span><span class="sxs-lookup"><span data-stu-id="352b0-167">INPUTS</span></span>

### <span data-ttu-id="352b0-168">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="352b0-168">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="352b0-169">System.String</span><span class="sxs-lookup"><span data-stu-id="352b0-169">System.String</span></span>

### <span data-ttu-id="352b0-170">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="352b0-170">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="352b0-171">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="352b0-171">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="352b0-172">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="352b0-172">OUTPUTS</span></span>

### <span data-ttu-id="352b0-173">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="352b0-173">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="352b0-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="352b0-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="352b0-175">NOTE</span><span class="sxs-lookup"><span data-stu-id="352b0-175">NOTES</span></span>

## <span data-ttu-id="352b0-176">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="352b0-176">RELATED LINKS</span></span>
