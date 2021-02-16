---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherflowlogstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
ms.openlocfilehash: a45a6ad4ee85dfabb28bef07400a0b6ebe115d7c
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412589"
---
# <span data-ttu-id="4155f-101">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="4155f-101">Get-AzNetworkWatcherFlowLogStatus</span></span>

## <span data-ttu-id="4155f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4155f-102">SYNOPSIS</span></span>
<span data-ttu-id="4155f-103">Ottiene lo stato della registrazione del flusso per una risorsa.</span><span class="sxs-lookup"><span data-stu-id="4155f-103">Gets the status of flow logging on a resource.</span></span>

## <span data-ttu-id="4155f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4155f-104">SYNTAX</span></span>

### <span data-ttu-id="4155f-105">SetByResource (Default)</span><span class="sxs-lookup"><span data-stu-id="4155f-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4155f-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="4155f-106">SetByName</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4155f-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="4155f-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -Location <String> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4155f-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4155f-108">DESCRIPTION</span></span>
<span data-ttu-id="4155f-109">Il Get-AzNetworkWatcherFlowLogStatus cmdlet cmdlet ottiene lo stato della registrazione del flusso su una risorsa.</span><span class="sxs-lookup"><span data-stu-id="4155f-109">The Get-AzNetworkWatcherFlowLogStatus cmdlet Gets the status of flow logging on a resource.</span></span> <span data-ttu-id="4155f-110">Lo stato include se la registrazione del flusso è abilitata o meno per la risorsa fornita, l'account di archiviazione configurato per l'invio dei log e i criteri di conservazione per i log.</span><span class="sxs-lookup"><span data-stu-id="4155f-110">The status includes whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="4155f-111">Attualmente sono supportati i gruppi di sicurezza di rete per la registrazione del flusso.</span><span class="sxs-lookup"><span data-stu-id="4155f-111">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="4155f-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4155f-112">EXAMPLES</span></span>

### <span data-ttu-id="4155f-113">Esempio 1: Ottenere lo stato della registrazione del flusso per un gruppo di rete specificato</span><span class="sxs-lookup"><span data-stu-id="4155f-113">Example 1: Get the Flow Logging Status for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG

PS C:\> Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher $NW -TargetResourceId $nsg.Id

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
Properties       : {
                     "Enabled": true,
                     "RetentionPolicy": {
                       "Days": 0,
                       "Enabled": false
                     },
                     "StorageId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"
                     "Format"         : {
                       "Type ": "Json",
                       "Version": 1
                     }
                   }
```

<span data-ttu-id="4155f-114">In questo esempio viene visualizzato lo stato della registrazione del flusso per un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="4155f-114">In this example we get the flow logging status for a Network Security Group.</span></span> <span data-ttu-id="4155f-115">Per il gruppo di sicurezza NSG specificato è abilitata la registrazione del flusso, il formato predefinito e non sono impostati criteri di conservazione.</span><span class="sxs-lookup"><span data-stu-id="4155f-115">The specified NSG has flow logging enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="4155f-116">Esempio 2: Ottenere lo stato di registrazione del flusso e analisi del traffico per un NSG specificato</span><span class="sxs-lookup"><span data-stu-id="4155f-116">Example 2: Get the Flow Logging and Traffic Analytics Status for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG

PS C:\> Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher $NW -TargetResourceId $nsg.Id

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
Format           : {
                     "Type ": "Json",
                     "Version": 1
                   }
FlowAnalyticsConfiguration : {
            "networkWatcherFlowAnalyticsConfiguration": {
              "enabled": true,
              "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb",
              "workspaceRegion": "WorkspaceLocation",
              "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/WorkspaceRg/providers/microsoft.operationalinsights/workspaces/WorkspaceName",
              "TrafficAnalyticsInterval": 60
            }
          }
```

<span data-ttu-id="4155f-117">In questo esempio vengono mostrati la registrazione del flusso e lo stato di Analisi del traffico per un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="4155f-117">In this example we get the flow logging and Traffic Analytics status for a Network Security Group.</span></span> <span data-ttu-id="4155f-118">Per il gruppo NSG specificato sono abilitati la registrazione del flusso e Analisi del traffico, il formato predefinito e nessun criterio di conservazione impostato.</span><span class="sxs-lookup"><span data-stu-id="4155f-118">The specified NSG has flow logging and Traffic Analytics enabled, default format and no retention policy set.</span></span>

## <span data-ttu-id="4155f-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4155f-119">PARAMETERS</span></span>

### <span data-ttu-id="4155f-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4155f-120">-AsJob</span></span>
<span data-ttu-id="4155f-121">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="4155f-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4155f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4155f-122">-DefaultProfile</span></span>
<span data-ttu-id="4155f-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4155f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4155f-124">-Location</span><span class="sxs-lookup"><span data-stu-id="4155f-124">-Location</span></span>
<span data-ttu-id="4155f-125">Posizione del network watcher.</span><span class="sxs-lookup"><span data-stu-id="4155f-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="4155f-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4155f-126">-NetworkWatcher</span></span>
<span data-ttu-id="4155f-127">Risorsa Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="4155f-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="4155f-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="4155f-128">-NetworkWatcherName</span></span>
<span data-ttu-id="4155f-129">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="4155f-129">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4155f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4155f-130">-ResourceGroupName</span></span>
<span data-ttu-id="4155f-131">Nome del gruppo di risorse Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="4155f-131">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4155f-132">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="4155f-132">-TargetResourceId</span></span>
<span data-ttu-id="4155f-133">ID risorsa di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4155f-133">The target resource ID.</span></span>

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

### <span data-ttu-id="4155f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4155f-134">CommonParameters</span></span>
<span data-ttu-id="4155f-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4155f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4155f-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4155f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4155f-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="4155f-137">INPUTS</span></span>

### <span data-ttu-id="4155f-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4155f-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="4155f-139">System.String</span><span class="sxs-lookup"><span data-stu-id="4155f-139">System.String</span></span>

## <span data-ttu-id="4155f-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4155f-140">OUTPUTS</span></span>

### <span data-ttu-id="4155f-141">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="4155f-141">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="4155f-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="4155f-142">NOTES</span></span>
<span data-ttu-id="4155f-143">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, rete, rete, watcher, flusso, log, flowlog, registrazione</span><span class="sxs-lookup"><span data-stu-id="4155f-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="4155f-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4155f-144">RELATED LINKS</span></span>

[<span data-ttu-id="4155f-145">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4155f-145">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="4155f-146">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4155f-146">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="4155f-147">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4155f-147">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="4155f-148">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="4155f-148">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="4155f-149">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="4155f-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="4155f-150">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="4155f-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="4155f-151">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="4155f-151">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="4155f-152">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4155f-152">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4155f-153">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="4155f-153">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="4155f-154">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4155f-154">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4155f-155">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4155f-155">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4155f-156">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4155f-156">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4155f-157">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="4155f-157">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="4155f-158">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="4155f-158">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="4155f-159">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="4155f-159">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="4155f-160">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4155f-160">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4155f-161">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4155f-161">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4155f-162">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4155f-162">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4155f-163">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="4155f-163">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="4155f-164">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4155f-164">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4155f-165">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4155f-165">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4155f-166">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="4155f-166">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="4155f-167">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="4155f-167">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="4155f-168">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="4155f-168">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="4155f-169">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="4155f-169">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="4155f-170">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="4155f-170">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="4155f-171">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4155f-171">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
