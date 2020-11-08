---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchertroubleshootingresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
ms.openlocfilehash: 710f35a96872ccf840810d8c2fe5189cccdbcaed
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018329"
---
# <span data-ttu-id="e6a4f-101">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="e6a4f-101">Get-AzNetworkWatcherTroubleshootingResult</span></span>

## <span data-ttu-id="e6a4f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e6a4f-102">SYNOPSIS</span></span>
<span data-ttu-id="e6a4f-103">Ottiene il risultato della risoluzione dei problemi dell'operazione di risoluzione dei problemi eseguita in precedenza o attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="e6a4f-103">Gets the troubleshooting result from the previously run or currently running troubleshooting operation.</span></span>

## <span data-ttu-id="e6a4f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e6a4f-104">SYNTAX</span></span>

### <span data-ttu-id="e6a4f-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e6a4f-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6a4f-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="e6a4f-106">SetByName</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6a4f-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="e6a4f-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -Location <String> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6a4f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e6a4f-108">DESCRIPTION</span></span>
<span data-ttu-id="e6a4f-109">Il cmdlet Get-AzNetworkWatcherTroubleshootingResult ottiene il risultato della risoluzione dei problemi dell'operazione eseguita in precedenza o attualmente in esecuzione Start-AzNetworkWatcherResourceTroubleshooting.</span><span class="sxs-lookup"><span data-stu-id="e6a4f-109">The Get-AzNetworkWatcherTroubleshootingResult cmdlet gets the troubleshooting result from the previously run or currently running Start-AzNetworkWatcherResourceTroubleshooting operation.</span></span> <span data-ttu-id="e6a4f-110">Se l'operazione di risoluzione dei problemi è attualmente in corso, questa operazione può richiedere alcuni minuti per il completamento.</span><span class="sxs-lookup"><span data-stu-id="e6a4f-110">If the troubleshooting operation is currently in progress, then this operation may take a few minutes to complete.</span></span> <span data-ttu-id="e6a4f-111">Attualmente sono supportati i gateway e le connessioni di rete virtuali.</span><span class="sxs-lookup"><span data-stu-id="e6a4f-111">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="e6a4f-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e6a4f-112">EXAMPLES</span></span>

### <span data-ttu-id="e6a4f-113">Esempio 1: avviare la risoluzione dei problemi in un gateway di rete virtuale e recuperare il risultato</span><span class="sxs-lookup"><span data-stu-id="e6a4f-113">Example 1: Start Troubleshooting on a Virtual Network Gateway and Retrieve Result</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath

Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher $NW -TargetResourceId $target
```

<span data-ttu-id="e6a4f-114">L'esempio precedente avvia la risoluzione dei problemi in un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="e6a4f-114">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="e6a4f-115">L'operazione può richiedere alcuni minuti per il completamento.</span><span class="sxs-lookup"><span data-stu-id="e6a4f-115">The operation may take a few minutes to complete.</span></span>
<span data-ttu-id="e6a4f-116">Dopo aver avviato la risoluzione dei problemi, viene eseguita una chiamata Get-AzNetworkWatcherTroubleshootingResult alla risorsa per recuperare il risultato di questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="e6a4f-116">After troubleshooting has started, a Get-AzNetworkWatcherTroubleshootingResult call is made to the resource to retrieve the result of this call.</span></span> 

## <span data-ttu-id="e6a4f-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e6a4f-117">PARAMETERS</span></span>

### <span data-ttu-id="e6a4f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6a4f-118">-DefaultProfile</span></span>
<span data-ttu-id="e6a4f-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e6a4f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6a4f-120">-Posizione</span><span class="sxs-lookup"><span data-stu-id="e6a4f-120">-Location</span></span>
<span data-ttu-id="e6a4f-121">Posizione del monitoraggio della rete.</span><span class="sxs-lookup"><span data-stu-id="e6a4f-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="e6a4f-122">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e6a4f-122">-NetworkWatcher</span></span>
<span data-ttu-id="e6a4f-123">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="e6a4f-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="e6a4f-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="e6a4f-124">-NetworkWatcherName</span></span>
<span data-ttu-id="e6a4f-125">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="e6a4f-125">The name of network watcher.</span></span>

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

### <span data-ttu-id="e6a4f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6a4f-126">-ResourceGroupName</span></span>
<span data-ttu-id="e6a4f-127">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="e6a4f-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="e6a4f-128">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="e6a4f-128">-TargetResourceId</span></span>
<span data-ttu-id="e6a4f-129">ID risorsa di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e6a4f-129">The target resource ID.</span></span>

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

### <span data-ttu-id="e6a4f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6a4f-130">CommonParameters</span></span>
<span data-ttu-id="e6a4f-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6a4f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6a4f-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e6a4f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6a4f-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e6a4f-133">INPUTS</span></span>

### <span data-ttu-id="e6a4f-134">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e6a4f-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="e6a4f-135">System. String</span><span class="sxs-lookup"><span data-stu-id="e6a4f-135">System.String</span></span>

## <span data-ttu-id="e6a4f-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e6a4f-136">OUTPUTS</span></span>

### <span data-ttu-id="e6a4f-137">Microsoft. Azure. Commands. Network. Models. PSTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="e6a4f-137">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="e6a4f-138">Note</span><span class="sxs-lookup"><span data-stu-id="e6a4f-138">NOTES</span></span>
<span data-ttu-id="e6a4f-139">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher, risoluzione dei problemi, VPN, connessione</span><span class="sxs-lookup"><span data-stu-id="e6a4f-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="e6a4f-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e6a4f-140">RELATED LINKS</span></span>

[<span data-ttu-id="e6a4f-141">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e6a4f-141">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="e6a4f-142">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e6a4f-142">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="e6a4f-143">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e6a4f-143">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="e6a4f-144">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="e6a4f-144">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="e6a4f-145">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="e6a4f-145">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="e6a4f-146">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="e6a4f-146">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="e6a4f-147">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="e6a4f-147">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="e6a4f-148">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e6a4f-148">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e6a4f-149">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="e6a4f-149">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="e6a4f-150">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e6a4f-150">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e6a4f-151">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e6a4f-151">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e6a4f-152">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e6a4f-152">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e6a4f-153">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="e6a4f-153">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="e6a4f-154">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="e6a4f-154">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="e6a4f-155">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="e6a4f-155">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="e6a4f-156">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e6a4f-156">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e6a4f-157">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e6a4f-157">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e6a4f-158">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e6a4f-158">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e6a4f-159">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="e6a4f-159">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="e6a4f-160">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e6a4f-160">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e6a4f-161">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e6a4f-161">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e6a4f-162">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="e6a4f-162">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="e6a4f-163">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="e6a4f-163">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="e6a4f-164">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="e6a4f-164">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="e6a4f-165">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="e6a4f-165">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="e6a4f-166">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="e6a4f-166">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="e6a4f-167">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e6a4f-167">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
