---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 1276a3c63ec4b9c4ec1c2c4c91ea792013cbacc9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188517"
---
# <span data-ttu-id="8c46a-101">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8c46a-101">Get-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="8c46a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8c46a-102">SYNOPSIS</span></span>
<span data-ttu-id="8c46a-103">Ottiene le informazioni e le proprietà e lo stato di una risorsa di acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="8c46a-103">Gets information and properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="8c46a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8c46a-104">SYNTAX</span></span>

### <span data-ttu-id="8c46a-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8c46a-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c46a-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="8c46a-106">SetByName</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c46a-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="8c46a-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherPacketCapture -Location <String> [-PacketCaptureName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c46a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8c46a-108">DESCRIPTION</span></span>
<span data-ttu-id="8c46a-109">Il Get-AzNetworkWatcherPacketCapture ottiene le proprietà e lo stato di una risorsa di acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="8c46a-109">The Get-AzNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="8c46a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8c46a-110">EXAMPLES</span></span>

### <span data-ttu-id="8c46a-111">Esempio 1: creare un'acquisizione di pacchetti con più filtri e recuperarne lo stato</span><span class="sxs-lookup"><span data-stu-id="8c46a-111">Example 1: Create a Packet Capture with multiple filters and retrieve its status</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="8c46a-112">In questo esempio creiamo un'acquisizione di pacchetti denominata "PacketCaptureTest" con più filtri e un limite di tempo.</span><span class="sxs-lookup"><span data-stu-id="8c46a-112">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="8c46a-113">Una volta completata la sessione, verrà salvata nell'account di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="8c46a-113">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="8c46a-114">Chiamiamo quindi Get-AzNetworkWatcherPacketCapture per recuperare lo stato della sessione di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="8c46a-114">We then call Get-AzNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> <span data-ttu-id="8c46a-115">Nota: l'estensione Azure Network Watcher deve essere installata nella macchina virtuale di destinazione per creare acquisizioni di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="8c46a-115">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

>[!NOTE]
><span data-ttu-id="8c46a-116">Se crei un riferimento all'acquisizione di pacchetti direttamente dal comando New-AzNetworkWatcherPacketCapture, non avrà tutte le proprietà.</span><span class="sxs-lookup"><span data-stu-id="8c46a-116">If you create a reference to the packet capture directly from the New-AzNetworkWatcherPacketCapture command, it won't have all the properties.</span></span> <span data-ttu-id="8c46a-117">È possibile ottenere tutte le proprietà dell'acquisizione di pacchetti effettuando una chiamata al comando Get-AzNetworkWatcherPacketCapture.</span><span class="sxs-lookup"><span data-stu-id="8c46a-117">You can get all of the properties of the packet capture by making a call to the Get-AzNetworkWatcherPacketCapture command.</span></span>

### <span data-ttu-id="8c46a-118">Esempio 2: creare un'acquisizione di pacchetti con più filtri e recuperarne lo stato</span><span class="sxs-lookup"><span data-stu-id="8c46a-118">Example 2: Create a Packet Capture with multiple filters and retrieve its status</span></span>
```
Get-AzNetworkWatcherPacketCapture -ResourceGroupName rg1 -NetworkWatcherName nw1 -PacketCaptureName PacketCapture*
```

<span data-ttu-id="8c46a-119">Questo cmdlet restituisce tutti i PacketCaptures che iniziano con "PacketCapture" in NW1 Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="8c46a-119">This cmdlet returns all PacketCaptures that start with "PacketCapture" in the nw1 Network Watcher.</span></span>

## <span data-ttu-id="8c46a-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8c46a-120">PARAMETERS</span></span>

### <span data-ttu-id="8c46a-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8c46a-121">-AsJob</span></span>
<span data-ttu-id="8c46a-122">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="8c46a-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8c46a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c46a-123">-DefaultProfile</span></span>
<span data-ttu-id="8c46a-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8c46a-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c46a-125">-Posizione</span><span class="sxs-lookup"><span data-stu-id="8c46a-125">-Location</span></span>
<span data-ttu-id="8c46a-126">Posizione del monitoraggio della rete.</span><span class="sxs-lookup"><span data-stu-id="8c46a-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="8c46a-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8c46a-127">-NetworkWatcher</span></span>
<span data-ttu-id="8c46a-128">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="8c46a-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="8c46a-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="8c46a-129">-NetworkWatcherName</span></span>
<span data-ttu-id="8c46a-130">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="8c46a-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="8c46a-131">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="8c46a-131">-PacketCaptureName</span></span>
<span data-ttu-id="8c46a-132">Nome del pacchetto Capture.</span><span class="sxs-lookup"><span data-stu-id="8c46a-132">The packet capture name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="8c46a-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c46a-133">-ResourceGroupName</span></span>
<span data-ttu-id="8c46a-134">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="8c46a-134">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="8c46a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c46a-135">CommonParameters</span></span>
<span data-ttu-id="8c46a-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c46a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c46a-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8c46a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c46a-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8c46a-138">INPUTS</span></span>

### <span data-ttu-id="8c46a-139">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8c46a-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="8c46a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="8c46a-140">System.String</span></span>

## <span data-ttu-id="8c46a-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8c46a-141">OUTPUTS</span></span>

### <span data-ttu-id="8c46a-142">Microsoft. Azure. Commands. Network. Models. PSGetPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="8c46a-142">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="8c46a-143">Note</span><span class="sxs-lookup"><span data-stu-id="8c46a-143">NOTES</span></span>
<span data-ttu-id="8c46a-144">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher, Packet, Capture, Traffic</span><span class="sxs-lookup"><span data-stu-id="8c46a-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="8c46a-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8c46a-145">RELATED LINKS</span></span>

[<span data-ttu-id="8c46a-146">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8c46a-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="8c46a-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8c46a-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="8c46a-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8c46a-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="8c46a-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="8c46a-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="8c46a-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="8c46a-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="8c46a-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="8c46a-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="8c46a-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="8c46a-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="8c46a-153">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8c46a-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8c46a-154">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="8c46a-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="8c46a-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8c46a-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8c46a-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8c46a-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8c46a-157">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8c46a-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8c46a-158">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="8c46a-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="8c46a-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="8c46a-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="8c46a-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="8c46a-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="8c46a-161">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8c46a-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8c46a-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8c46a-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8c46a-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8c46a-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8c46a-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="8c46a-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="8c46a-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8c46a-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8c46a-166">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8c46a-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8c46a-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="8c46a-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="8c46a-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="8c46a-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="8c46a-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="8c46a-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="8c46a-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="8c46a-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="8c46a-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="8c46a-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="8c46a-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8c46a-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

