---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 7c6ad774c7b260424821b37837882bab0b47bd53
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678257"
---
# <span data-ttu-id="8988a-101">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8988a-101">New-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="8988a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8988a-102">SYNOPSIS</span></span>
<span data-ttu-id="8988a-103">Crea un monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="8988a-103">Creates a connection monitor.</span></span>

## <span data-ttu-id="8988a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8988a-104">SYNTAX</span></span>

### <span data-ttu-id="8988a-105">SetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8988a-105">SetByName (Default)</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8988a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="8988a-106">SetByResource</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8988a-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="8988a-107">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8988a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8988a-108">DESCRIPTION</span></span>
<span data-ttu-id="8988a-109">Il cmdlet New-AzNetworkWatcherConnectionMonitor rcreates un monitor di connessione per un'origine e una destinazione specificate.</span><span class="sxs-lookup"><span data-stu-id="8988a-109">The New-AzNetworkWatcherConnectionMonitor cmdlet rcreates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="8988a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8988a-110">EXAMPLES</span></span>

### <span data-ttu-id="8988a-111">Esempio 1: creare un monitor di connessione per una VM e una destinazione Internet</span><span class="sxs-lookup"><span data-stu-id="8988a-111">Example 1: Create a connection monitor for a vm and internet destination</span></span>
```
PS C:\> New-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm -DestinationAddress bing.com -DestinationPort 80

Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/t1
Etag                        : W/"e86b28cf-b907-4475-a8b7-34d310367694"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000
                                00000/resourceGroups/RgCentralUSEUAP/providers/Microsoft
                                .Compute/virtualMachines/vm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "bing.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:13:11 PM
MonitoringStatus            : Running
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {}
```

<span data-ttu-id="8988a-112">Il cmdlet New-AzNetworkWatcherConnectionMonitor crea un monitor di connessione per un'origine e una destinazione specificate.</span><span class="sxs-lookup"><span data-stu-id="8988a-112">The New-AzNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="8988a-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8988a-113">PARAMETERS</span></span>

### <span data-ttu-id="8988a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8988a-114">-AsJob</span></span>
<span data-ttu-id="8988a-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="8988a-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8988a-116">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="8988a-116">-ConfigureOnly</span></span>
<span data-ttu-id="8988a-117">Configurare monitor di connessione, ma non avviarlo</span><span class="sxs-lookup"><span data-stu-id="8988a-117">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="8988a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8988a-118">-DefaultProfile</span></span>
<span data-ttu-id="8988a-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8988a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8988a-120">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="8988a-120">-DestinationAddress</span></span>
<span data-ttu-id="8988a-121">Indirizzo IP della destinazione del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="8988a-121">The Ip address of the connection monitor destination.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8988a-122">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="8988a-122">-DestinationPort</span></span>
<span data-ttu-id="8988a-123">Porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8988a-123">Destination port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8988a-124">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="8988a-124">-DestinationResourceId</span></span>
<span data-ttu-id="8988a-125">ID della destinazione del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="8988a-125">The ID of the connection monitor destination.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8988a-126">-Force</span><span class="sxs-lookup"><span data-stu-id="8988a-126">-Force</span></span>
<span data-ttu-id="8988a-127">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="8988a-127">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8988a-128">-Posizione</span><span class="sxs-lookup"><span data-stu-id="8988a-128">-Location</span></span>
<span data-ttu-id="8988a-129">Posizione del monitoraggio della rete.</span><span class="sxs-lookup"><span data-stu-id="8988a-129">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8988a-130">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="8988a-130">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="8988a-131">Intervallo di monitoraggio in secondi.</span><span class="sxs-lookup"><span data-stu-id="8988a-131">Monitoring interval in seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8988a-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="8988a-132">-Name</span></span>
<span data-ttu-id="8988a-133">Nome del monitor della connessione.</span><span class="sxs-lookup"><span data-stu-id="8988a-133">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8988a-134">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8988a-134">-NetworkWatcher</span></span>
<span data-ttu-id="8988a-135">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="8988a-135">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8988a-136">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="8988a-136">-NetworkWatcherName</span></span>
<span data-ttu-id="8988a-137">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="8988a-137">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8988a-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8988a-138">-ResourceGroupName</span></span>
<span data-ttu-id="8988a-139">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="8988a-139">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8988a-140">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="8988a-140">-SourcePort</span></span>
<span data-ttu-id="8988a-141">Porta di origine.</span><span class="sxs-lookup"><span data-stu-id="8988a-141">Source port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8988a-142">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="8988a-142">-SourceResourceId</span></span>
<span data-ttu-id="8988a-143">ID dell'origine del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="8988a-143">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="8988a-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="8988a-144">-Tag</span></span>
<span data-ttu-id="8988a-145">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="8988a-145">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8988a-146">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8988a-146">-Confirm</span></span>
<span data-ttu-id="8988a-147">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8988a-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8988a-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8988a-148">-WhatIf</span></span>
<span data-ttu-id="8988a-149">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8988a-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8988a-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8988a-150">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8988a-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8988a-151">CommonParameters</span></span>
<span data-ttu-id="8988a-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8988a-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8988a-153">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8988a-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8988a-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8988a-154">INPUTS</span></span>

### <span data-ttu-id="8988a-155">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8988a-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="8988a-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8988a-156">OUTPUTS</span></span>

### <span data-ttu-id="8988a-157">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="8988a-157">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="8988a-158">Note</span><span class="sxs-lookup"><span data-stu-id="8988a-158">NOTES</span></span>
<span data-ttu-id="8988a-159">Parole chiave: Azure, azurerm, ARM, Resource, Connectivity, Management, Manager, Network, networking, Network Watcher, Connection Monitor</span><span class="sxs-lookup"><span data-stu-id="8988a-159">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="8988a-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8988a-160">RELATED LINKS</span></span>

[<span data-ttu-id="8988a-161">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8988a-161">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="8988a-162">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8988a-162">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="8988a-163">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8988a-163">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="8988a-164">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="8988a-164">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="8988a-165">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="8988a-165">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="8988a-166">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="8988a-166">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="8988a-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="8988a-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="8988a-168">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8988a-168">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8988a-169">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="8988a-169">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="8988a-170">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8988a-170">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8988a-171">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8988a-171">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8988a-172">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8988a-172">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8988a-173">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8988a-173">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8988a-174">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="8988a-174">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="8988a-175">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8988a-175">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8988a-176">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8988a-176">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8988a-177">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8988a-177">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8988a-178">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8988a-178">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8988a-179">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="8988a-179">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="8988a-180">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="8988a-180">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="8988a-181">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="8988a-181">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="8988a-182">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="8988a-182">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="8988a-183">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8988a-183">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8988a-184">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="8988a-184">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="8988a-185">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="8988a-185">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="8988a-186">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="8988a-186">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="8988a-187">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="8988a-187">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
