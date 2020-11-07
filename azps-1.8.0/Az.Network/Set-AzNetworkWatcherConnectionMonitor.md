---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 7e3836f2c546c5ba3ad2ee4a2845e7c813601dda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677940"
---
# <span data-ttu-id="4ebc3-101">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4ebc3-101">Set-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="4ebc3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4ebc3-102">SYNOPSIS</span></span>
<span data-ttu-id="4ebc3-103">Aggiornare un monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="4ebc3-103">Update a connection monitor.</span></span>

## <span data-ttu-id="4ebc3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4ebc3-104">SYNTAX</span></span>

### <span data-ttu-id="4ebc3-105">SetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4ebc3-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ebc3-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4ebc3-106">SetByResource</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ebc3-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="4ebc3-107">SetByLocation</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ebc3-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4ebc3-108">SetByResourceId</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ebc3-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="4ebc3-109">SetByInputObject</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ebc3-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4ebc3-110">DESCRIPTION</span></span>
<span data-ttu-id="4ebc3-111">Il cmdlet Set-AzNetworkWatcherConnectionMonitor aggiorna il monitor di connessione specificato.</span><span class="sxs-lookup"><span data-stu-id="4ebc3-111">The Set-AzNetworkWatcherConnectionMonitor cmdlet updates the specified connection monitor.</span></span>

## <span data-ttu-id="4ebc3-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4ebc3-112">EXAMPLES</span></span>

### <span data-ttu-id="4ebc3-113">Esempio 1: aggiornare un monitor di connessione</span><span class="sxs-lookup"><span data-stu-id="4ebc3-113">Example 1: Update a connection monitor</span></span>
```
PS C:\> Set-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm
-DestinationAddress google.com -DestinationPort 80 -Tag @{"key1" = "value1"}

Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/cm
Etag                        : W/"5b2b20e8-0ce0-417e-9607-76208149bb67"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000
                                00000/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMach
                                ines/vm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "google.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:19:28 PM
MonitoringStatus            : Running
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {
                                "key1": "value1"
                              }
```

<span data-ttu-id="4ebc3-114">In questo esempio aggiorniamo il monitor di connessione esistente modificando destinationAddress e aggiungendo i tag.</span><span class="sxs-lookup"><span data-stu-id="4ebc3-114">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="4ebc3-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4ebc3-115">PARAMETERS</span></span>

### <span data-ttu-id="4ebc3-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4ebc3-116">-AsJob</span></span>
<span data-ttu-id="4ebc3-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="4ebc3-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4ebc3-118">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="4ebc3-118">-ConfigureOnly</span></span>
<span data-ttu-id="4ebc3-119">Configurare monitor di connessione, ma non avviarlo</span><span class="sxs-lookup"><span data-stu-id="4ebc3-119">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="4ebc3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ebc3-120">-DefaultProfile</span></span>
<span data-ttu-id="4ebc3-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4ebc3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ebc3-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="4ebc3-122">-DestinationAddress</span></span>
<span data-ttu-id="4ebc3-123">Indirizzo IP della destinazione del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="4ebc3-123">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="4ebc3-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="4ebc3-124">-DestinationPort</span></span>
<span data-ttu-id="4ebc3-125">Porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4ebc3-125">Destination port.</span></span>

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

### <span data-ttu-id="4ebc3-126">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="4ebc3-126">-DestinationResourceId</span></span>
<span data-ttu-id="4ebc3-127">ID della destinazione del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="4ebc3-127">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="4ebc3-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ebc3-128">-InputObject</span></span>
<span data-ttu-id="4ebc3-129">Oggetto monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="4ebc3-129">Connection monitor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ebc3-130">-Posizione</span><span class="sxs-lookup"><span data-stu-id="4ebc3-130">-Location</span></span>
<span data-ttu-id="4ebc3-131">Posizione del monitoraggio della rete.</span><span class="sxs-lookup"><span data-stu-id="4ebc3-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="4ebc3-132">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="4ebc3-132">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="4ebc3-133">Intervallo di monitoraggio in secondi.</span><span class="sxs-lookup"><span data-stu-id="4ebc3-133">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="4ebc3-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="4ebc3-134">-Name</span></span>
<span data-ttu-id="4ebc3-135">Nome del monitor della connessione.</span><span class="sxs-lookup"><span data-stu-id="4ebc3-135">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ebc3-136">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4ebc3-136">-NetworkWatcher</span></span>
<span data-ttu-id="4ebc3-137">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="4ebc3-137">The network watcher resource.</span></span>

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

### <span data-ttu-id="4ebc3-138">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="4ebc3-138">-NetworkWatcherName</span></span>
<span data-ttu-id="4ebc3-139">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="4ebc3-139">The name of network watcher.</span></span>

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

### <span data-ttu-id="4ebc3-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ebc3-140">-ResourceGroupName</span></span>
<span data-ttu-id="4ebc3-141">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="4ebc3-141">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="4ebc3-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ebc3-142">-ResourceId</span></span>
<span data-ttu-id="4ebc3-143">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="4ebc3-143">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ebc3-144">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="4ebc3-144">-SourcePort</span></span>
<span data-ttu-id="4ebc3-145">Porta di origine.</span><span class="sxs-lookup"><span data-stu-id="4ebc3-145">Source port.</span></span>

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

### <span data-ttu-id="4ebc3-146">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="4ebc3-146">-SourceResourceId</span></span>
<span data-ttu-id="4ebc3-147">ID dell'origine del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="4ebc3-147">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="4ebc3-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="4ebc3-148">-Tag</span></span>
<span data-ttu-id="4ebc3-149">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="4ebc3-149">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="4ebc3-150">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4ebc3-150">-Confirm</span></span>
<span data-ttu-id="4ebc3-151">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ebc3-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ebc3-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ebc3-152">-WhatIf</span></span>
<span data-ttu-id="4ebc3-153">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4ebc3-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ebc3-154">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4ebc3-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ebc3-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ebc3-155">CommonParameters</span></span>
<span data-ttu-id="4ebc3-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ebc3-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ebc3-157">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ebc3-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ebc3-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4ebc3-158">INPUTS</span></span>

### <span data-ttu-id="4ebc3-159">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4ebc3-159">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="4ebc3-160">System. String</span><span class="sxs-lookup"><span data-stu-id="4ebc3-160">System.String</span></span>

### <span data-ttu-id="4ebc3-161">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="4ebc3-161">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="4ebc3-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4ebc3-162">OUTPUTS</span></span>

### <span data-ttu-id="4ebc3-163">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="4ebc3-163">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="4ebc3-164">Note</span><span class="sxs-lookup"><span data-stu-id="4ebc3-164">NOTES</span></span>
<span data-ttu-id="4ebc3-165">Parole chiave: Azure, azurerm, ARM, Resource, Connectivity, Management, Manager, Network, networking, Network Watcher, Connection Monitor</span><span class="sxs-lookup"><span data-stu-id="4ebc3-165">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="4ebc3-166">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4ebc3-166">RELATED LINKS</span></span>

[<span data-ttu-id="4ebc3-167">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4ebc3-167">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="4ebc3-168">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4ebc3-168">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="4ebc3-169">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4ebc3-169">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="4ebc3-170">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="4ebc3-170">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="4ebc3-171">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="4ebc3-171">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="4ebc3-172">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="4ebc3-172">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="4ebc3-173">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="4ebc3-173">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="4ebc3-174">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4ebc3-174">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4ebc3-175">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="4ebc3-175">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="4ebc3-176">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4ebc3-176">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4ebc3-177">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4ebc3-177">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4ebc3-178">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4ebc3-178">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4ebc3-179">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4ebc3-179">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4ebc3-180">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="4ebc3-180">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="4ebc3-181">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4ebc3-181">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4ebc3-182">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4ebc3-182">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4ebc3-183">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4ebc3-183">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4ebc3-184">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4ebc3-184">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4ebc3-185">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ebc3-185">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="4ebc3-186">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="4ebc3-186">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="4ebc3-187">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="4ebc3-187">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="4ebc3-188">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="4ebc3-188">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="4ebc3-189">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4ebc3-189">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4ebc3-190">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="4ebc3-190">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="4ebc3-191">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="4ebc3-191">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="4ebc3-192">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="4ebc3-192">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="4ebc3-193">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="4ebc3-193">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
