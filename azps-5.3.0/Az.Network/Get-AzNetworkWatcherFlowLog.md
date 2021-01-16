---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 5f4322ba81cdae5bdb0b33c2658a6d7934ed638d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379861"
---
# <span data-ttu-id="c126a-101">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="c126a-101">Get-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="c126a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c126a-102">SYNOPSIS</span></span>
<span data-ttu-id="c126a-103">Ottiene una risorsa del log di flusso o un elenco di risorse del log di flusso nell'abbonamento e nell'area geografica specificati.</span><span class="sxs-lookup"><span data-stu-id="c126a-103">Gets a flow log resource or a list of flow log resources in the specified subscription and region.</span></span>

## <span data-ttu-id="c126a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c126a-104">SYNTAX</span></span>

### <span data-ttu-id="c126a-105">SetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c126a-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c126a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c126a-106">SetByResource</span></span>
```
Get-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c126a-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="c126a-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherFlowLog -Location <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c126a-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c126a-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherFlowLog -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c126a-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c126a-109">DESCRIPTION</span></span>
<span data-ttu-id="c126a-110">Ottiene una risorsa del log di flusso o un elenco di risorse del log di flusso nell'abbonamento e nell'area geografica specificati.</span><span class="sxs-lookup"><span data-stu-id="c126a-110">Gets a flow log resource or a list of flow log resources in the specified subscription and region.</span></span>

## <span data-ttu-id="c126a-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c126a-111">EXAMPLES</span></span>

### <span data-ttu-id="c126a-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c126a-112">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkWatcherFlowLog -Location eastus -Name pstest
```

<span data-ttu-id="c126a-113">Nome: pstest ID:/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ERS/Microsoft. Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest ETag: W/"f6047360-d797-4ca6-A9EC-28b5aec5c768" ProvisioningState: percorso riuscito: eastus TargetResourceId:/subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft. Network/networkSecurityGroups/MyNSG StorageId:/subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft. storage/storageAccounts/spazio di archiviazione abilitato: true RetentionPolicy: {"Days": 5, "Enabled": true} Format: {"tipo": "JSON", "Version": 2} FlowAnalyticsConfiguration: {"networkWatcherFlowAnalyticsConfiguration": {"Enabled": true, "workspaceId": "BBBBBBBB-bbbb-bbbb-bbbb-bbbbbbbbbbbb", "workspaceRegion": "eastus", "workspaceResourceId": "/subscriptions/BBBBBBBB-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr Oups/FlowLogsV2Demo/Providers/Microsoft. OperationalInsights/Workspaces/Workspace", "trafficAnalyticsInterval": 60}</span><span class="sxs-lookup"><span data-stu-id="c126a-113">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled                    : True RetentionPolicy            : { "Days": 5, "Enabled": true } Format                     : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": true, "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb", "workspaceRegion": "eastus", "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr oups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace", "trafficAnalyticsInterval": 60 }</span></span>

## <span data-ttu-id="c126a-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c126a-114">PARAMETERS</span></span>

### <span data-ttu-id="c126a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c126a-115">-DefaultProfile</span></span>
<span data-ttu-id="c126a-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c126a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c126a-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="c126a-117">-Location</span></span>
<span data-ttu-id="c126a-118">Posizione del monitoraggio della rete.</span><span class="sxs-lookup"><span data-stu-id="c126a-118">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c126a-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="c126a-119">-Name</span></span>
<span data-ttu-id="c126a-120">Nome del log di flusso.</span><span class="sxs-lookup"><span data-stu-id="c126a-120">The flow log name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: FlowLogName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c126a-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c126a-121">-NetworkWatcher</span></span>
<span data-ttu-id="c126a-122">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="c126a-122">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c126a-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="c126a-123">-NetworkWatcherName</span></span>
<span data-ttu-id="c126a-124">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="c126a-124">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c126a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c126a-125">-ResourceGroupName</span></span>
<span data-ttu-id="c126a-126">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="c126a-126">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c126a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c126a-127">-ResourceId</span></span>
<span data-ttu-id="c126a-128">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="c126a-128">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c126a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c126a-129">CommonParameters</span></span>
<span data-ttu-id="c126a-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c126a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c126a-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c126a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c126a-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c126a-132">INPUTS</span></span>

### <span data-ttu-id="c126a-133">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c126a-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="c126a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c126a-134">System.String</span></span>

## <span data-ttu-id="c126a-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c126a-135">OUTPUTS</span></span>

### <span data-ttu-id="c126a-136">Microsoft. Azure. Commands. Network. Models. PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="c126a-136">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="c126a-137">Note</span><span class="sxs-lookup"><span data-stu-id="c126a-137">NOTES</span></span>

## <span data-ttu-id="c126a-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c126a-138">RELATED LINKS</span></span>

[<span data-ttu-id="c126a-139">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c126a-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="c126a-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c126a-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="c126a-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c126a-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="c126a-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c126a-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="c126a-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c126a-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c126a-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c126a-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="c126a-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c126a-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="c126a-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c126a-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c126a-147">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c126a-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="c126a-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c126a-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c126a-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c126a-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c126a-150">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c126a-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c126a-151">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="c126a-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="c126a-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c126a-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="c126a-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="c126a-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="c126a-154">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c126a-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c126a-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c126a-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c126a-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c126a-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c126a-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="c126a-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="c126a-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c126a-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c126a-159">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c126a-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c126a-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="c126a-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="c126a-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="c126a-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="c126a-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="c126a-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="c126a-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="c126a-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="c126a-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="c126a-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="c126a-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c126a-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="c126a-166">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="c126a-166">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="c126a-167">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="c126a-167">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="c126a-168">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="c126a-168">Remove-AzNetworkWatcherFlowLog</span></span>](./Remove-AzNetworkWatcherFlowLog.md)
