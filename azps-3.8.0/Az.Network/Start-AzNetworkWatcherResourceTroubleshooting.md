---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-aznetworkwatcherresourcetroubleshooting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
ms.openlocfilehash: e8e8b9dfd217f9407af8db18a5f468d7d971c97d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864388"
---
# <span data-ttu-id="54df2-101">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="54df2-101">Start-AzNetworkWatcherResourceTroubleshooting</span></span>

## <span data-ttu-id="54df2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="54df2-102">SYNOPSIS</span></span>
<span data-ttu-id="54df2-103">Avvia la risoluzione dei problemi in una risorsa di rete in Azure.</span><span class="sxs-lookup"><span data-stu-id="54df2-103">Starts troubleshooting on a Networking resource in Azure.</span></span>

## <span data-ttu-id="54df2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="54df2-104">SYNTAX</span></span>

### <span data-ttu-id="54df2-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="54df2-105">SetByResource (Default)</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -StorageId <String> -StoragePath <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54df2-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="54df2-106">SetByName</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54df2-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="54df2-107">SetByLocation</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -Location <String> -TargetResourceId <String> -StorageId <String>
 -StoragePath <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54df2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="54df2-108">DESCRIPTION</span></span>
<span data-ttu-id="54df2-109">Il cmdlet Start-AzNetworkWatcherResourceTroubleshooting avvia la risoluzione dei problemi per una risorsa di rete in Azure e restituisce informazioni su potenziali problemi e attenuazioni.</span><span class="sxs-lookup"><span data-stu-id="54df2-109">The Start-AzNetworkWatcherResourceTroubleshooting cmdlet starts troubleshooting for a Networking resource in Azure and returns information about potential issues and mitigations.</span></span> <span data-ttu-id="54df2-110">Attualmente sono supportati i gateway e le connessioni di rete virtuali.</span><span class="sxs-lookup"><span data-stu-id="54df2-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="54df2-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="54df2-111">EXAMPLES</span></span>

### <span data-ttu-id="54df2-112">Esempio 1: avviare la risoluzione dei problemi in un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="54df2-112">Example 1: Start Troubleshooting on a Virtual Network Gateway</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath
```

<span data-ttu-id="54df2-113">L'esempio precedente avvia la risoluzione dei problemi in un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="54df2-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="54df2-114">L'operazione può richiedere alcuni minuti per il completamento.</span><span class="sxs-lookup"><span data-stu-id="54df2-114">The operation may take a few minutes to complete.</span></span>

## <span data-ttu-id="54df2-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="54df2-115">PARAMETERS</span></span>

### <span data-ttu-id="54df2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54df2-116">-DefaultProfile</span></span>
<span data-ttu-id="54df2-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="54df2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54df2-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="54df2-118">-Location</span></span>
<span data-ttu-id="54df2-119">Posizione del monitoraggio della rete.</span><span class="sxs-lookup"><span data-stu-id="54df2-119">Location of the network watcher.</span></span>

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

### <span data-ttu-id="54df2-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="54df2-120">-NetworkWatcher</span></span>
<span data-ttu-id="54df2-121">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="54df2-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="54df2-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="54df2-122">-NetworkWatcherName</span></span>
<span data-ttu-id="54df2-123">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="54df2-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="54df2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54df2-124">-ResourceGroupName</span></span>
<span data-ttu-id="54df2-125">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="54df2-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="54df2-126">-StorageId</span><span class="sxs-lookup"><span data-stu-id="54df2-126">-StorageId</span></span>
<span data-ttu-id="54df2-127">ID dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="54df2-127">The storage ID.</span></span>

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

### <span data-ttu-id="54df2-128">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="54df2-128">-StoragePath</span></span>
<span data-ttu-id="54df2-129">Percorso di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="54df2-129">The storage path.</span></span>

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

### <span data-ttu-id="54df2-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="54df2-130">-TargetResourceId</span></span>
<span data-ttu-id="54df2-131">Specifica l'ID risorsa della risorsa per la risoluzione dei problemi.</span><span class="sxs-lookup"><span data-stu-id="54df2-131">Specifies the resource id of the resource to troubleshoot.</span></span> <span data-ttu-id="54df2-132">Formato di esempio: "/subscriptions/$ {subscriptionId}/resourceGroups/$ {resourceGroupName}/providers/Microsoft.Network/connections/$ {ConnectionName}"</span><span class="sxs-lookup"><span data-stu-id="54df2-132">Example format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span></span>

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

### <span data-ttu-id="54df2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54df2-133">CommonParameters</span></span>
<span data-ttu-id="54df2-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54df2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54df2-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54df2-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54df2-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="54df2-136">INPUTS</span></span>

### <span data-ttu-id="54df2-137">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="54df2-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="54df2-138">System. String</span><span class="sxs-lookup"><span data-stu-id="54df2-138">System.String</span></span>

## <span data-ttu-id="54df2-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="54df2-139">OUTPUTS</span></span>

### <span data-ttu-id="54df2-140">Microsoft. Azure. Commands. Network. Models. PSTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="54df2-140">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="54df2-141">Note</span><span class="sxs-lookup"><span data-stu-id="54df2-141">NOTES</span></span>
<span data-ttu-id="54df2-142">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher, risoluzione dei problemi, VPN, connessione</span><span class="sxs-lookup"><span data-stu-id="54df2-142">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="54df2-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="54df2-143">RELATED LINKS</span></span>

[<span data-ttu-id="54df2-144">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="54df2-144">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="54df2-145">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="54df2-145">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="54df2-146">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="54df2-146">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="54df2-147">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="54df2-147">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="54df2-148">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="54df2-148">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="54df2-149">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="54df2-149">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="54df2-150">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="54df2-150">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="54df2-151">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="54df2-151">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="54df2-152">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="54df2-152">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="54df2-153">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="54df2-153">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="54df2-154">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="54df2-154">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="54df2-155">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="54df2-155">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="54df2-156">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="54df2-156">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="54df2-157">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="54df2-157">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="54df2-158">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="54df2-158">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="54df2-159">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="54df2-159">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="54df2-160">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="54df2-160">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="54df2-161">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="54df2-161">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="54df2-162">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="54df2-162">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="54df2-163">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="54df2-163">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="54df2-164">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="54df2-164">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="54df2-165">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="54df2-165">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="54df2-166">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="54df2-166">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="54df2-167">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="54df2-167">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="54df2-168">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="54df2-168">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="54df2-169">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="54df2-169">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="54df2-170">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="54df2-170">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)