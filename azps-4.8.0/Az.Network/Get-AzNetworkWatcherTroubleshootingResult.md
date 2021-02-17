---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchertroubleshootingresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
ms.openlocfilehash: 871509fc03a7cb80735b6f011a7103350fd945ac
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100404599"
---
# <span data-ttu-id="32f59-101">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="32f59-101">Get-AzNetworkWatcherTroubleshootingResult</span></span>

## <span data-ttu-id="32f59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32f59-102">SYNOPSIS</span></span>
<span data-ttu-id="32f59-103">Recupera il risultato della risoluzione dei problemi dall'operazione eseguita in precedenza o in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="32f59-103">Gets the troubleshooting result from the previously run or currently running troubleshooting operation.</span></span>

## <span data-ttu-id="32f59-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="32f59-104">SYNTAX</span></span>

### <span data-ttu-id="32f59-105">SetByResource (Default)</span><span class="sxs-lookup"><span data-stu-id="32f59-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32f59-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="32f59-106">SetByName</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32f59-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="32f59-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -Location <String> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32f59-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="32f59-108">DESCRIPTION</span></span>
<span data-ttu-id="32f59-109">Il cmdlet Get-AzNetworkWatcherTroubleshootingResult cmdlet recupera il risultato della risoluzione dei problemi dall'operazione eseguita in precedenza o da Start-AzNetworkWatcherResourceTroubleshooting in corso.</span><span class="sxs-lookup"><span data-stu-id="32f59-109">The Get-AzNetworkWatcherTroubleshootingResult cmdlet gets the troubleshooting result from the previously run or currently running Start-AzNetworkWatcherResourceTroubleshooting operation.</span></span> <span data-ttu-id="32f59-110">Se è in corso l'operazione di risoluzione dei problemi, il completamento dell'operazione potrebbe richiedere alcuni minuti.</span><span class="sxs-lookup"><span data-stu-id="32f59-110">If the troubleshooting operation is currently in progress, then this operation may take a few minutes to complete.</span></span> <span data-ttu-id="32f59-111">Attualmente sono supportati gateway e connessioni di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="32f59-111">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="32f59-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="32f59-112">EXAMPLES</span></span>

### <span data-ttu-id="32f59-113">Esempio 1: Avviare la risoluzione dei problemi in un Gateway di rete virtuale e recuperare i risultati</span><span class="sxs-lookup"><span data-stu-id="32f59-113">Example 1: Start Troubleshooting on a Virtual Network Gateway and Retrieve Result</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath

Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher $NW -TargetResourceId $target
```

<span data-ttu-id="32f59-114">Nell'esempio precedente viene avviata la risoluzione dei problemi in un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="32f59-114">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="32f59-115">Il completamento dell'operazione può richiedere alcuni minuti.</span><span class="sxs-lookup"><span data-stu-id="32f59-115">The operation may take a few minutes to complete.</span></span>
<span data-ttu-id="32f59-116">Una volta avviata la risoluzione dei Get-AzNetworkWatcherTroubleshootingResult, viene effettuata una Get-AzNetworkWatcherTroubleshootingResult chiamata alla risorsa per recuperare il risultato della chiamata.</span><span class="sxs-lookup"><span data-stu-id="32f59-116">After troubleshooting has started, a Get-AzNetworkWatcherTroubleshootingResult call is made to the resource to retrieve the result of this call.</span></span> 

## <span data-ttu-id="32f59-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32f59-117">PARAMETERS</span></span>

### <span data-ttu-id="32f59-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32f59-118">-DefaultProfile</span></span>
<span data-ttu-id="32f59-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="32f59-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32f59-120">-Location</span><span class="sxs-lookup"><span data-stu-id="32f59-120">-Location</span></span>
<span data-ttu-id="32f59-121">Posizione del network watcher.</span><span class="sxs-lookup"><span data-stu-id="32f59-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="32f59-122">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="32f59-122">-NetworkWatcher</span></span>
<span data-ttu-id="32f59-123">Risorsa Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="32f59-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="32f59-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="32f59-124">-NetworkWatcherName</span></span>
<span data-ttu-id="32f59-125">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="32f59-125">The name of network watcher.</span></span>

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

### <span data-ttu-id="32f59-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32f59-126">-ResourceGroupName</span></span>
<span data-ttu-id="32f59-127">Nome del gruppo di risorse Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="32f59-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="32f59-128">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="32f59-128">-TargetResourceId</span></span>
<span data-ttu-id="32f59-129">ID risorsa di destinazione.</span><span class="sxs-lookup"><span data-stu-id="32f59-129">The target resource ID.</span></span>

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

### <span data-ttu-id="32f59-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32f59-130">CommonParameters</span></span>
<span data-ttu-id="32f59-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32f59-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32f59-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="32f59-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32f59-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="32f59-133">INPUTS</span></span>

### <span data-ttu-id="32f59-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="32f59-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="32f59-135">System.String</span><span class="sxs-lookup"><span data-stu-id="32f59-135">System.String</span></span>

## <span data-ttu-id="32f59-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="32f59-136">OUTPUTS</span></span>

### <span data-ttu-id="32f59-137">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="32f59-137">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="32f59-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="32f59-138">NOTES</span></span>
<span data-ttu-id="32f59-139">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, rete, rete, network watcher, risoluzione dei problemi, VPN, connessione</span><span class="sxs-lookup"><span data-stu-id="32f59-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="32f59-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="32f59-140">RELATED LINKS</span></span>

[<span data-ttu-id="32f59-141">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="32f59-141">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="32f59-142">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="32f59-142">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="32f59-143">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="32f59-143">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="32f59-144">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="32f59-144">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="32f59-145">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="32f59-145">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="32f59-146">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="32f59-146">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="32f59-147">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="32f59-147">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="32f59-148">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="32f59-148">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="32f59-149">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="32f59-149">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="32f59-150">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="32f59-150">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="32f59-151">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="32f59-151">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="32f59-152">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="32f59-152">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="32f59-153">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="32f59-153">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="32f59-154">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="32f59-154">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="32f59-155">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="32f59-155">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="32f59-156">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="32f59-156">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="32f59-157">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="32f59-157">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="32f59-158">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="32f59-158">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="32f59-159">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="32f59-159">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="32f59-160">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="32f59-160">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="32f59-161">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="32f59-161">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="32f59-162">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="32f59-162">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="32f59-163">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="32f59-163">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="32f59-164">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="32f59-164">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="32f59-165">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="32f59-165">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="32f59-166">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="32f59-166">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="32f59-167">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="32f59-167">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
