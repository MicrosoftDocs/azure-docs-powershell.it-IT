---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpacketcapturefilterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
ms.openlocfilehash: c81eada89865585ae56af2ed629ee17e43d57aa8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019730"
---
# <span data-ttu-id="a2403-101">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="a2403-101">New-AzPacketCaptureFilterConfig</span></span>

## <span data-ttu-id="a2403-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a2403-102">SYNOPSIS</span></span>
<span data-ttu-id="a2403-103">Crea un nuovo oggetto filtro di acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="a2403-103">Creates a new packet capture filter object.</span></span>

## <span data-ttu-id="a2403-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a2403-104">SYNTAX</span></span>

```
New-AzPacketCaptureFilterConfig [-Protocol <String>] [-RemoteIPAddress <String>] [-LocalIPAddress <String>]
 [-LocalPort <String>] [-RemotePort <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2403-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a2403-105">DESCRIPTION</span></span>
<span data-ttu-id="a2403-106">Il cmdlet New-AzPacketCaptureFilterConfig crea un nuovo oggetto filtro di acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="a2403-106">The New-AzPacketCaptureFilterConfig cmdlet creates a new packet capture filter object.</span></span> <span data-ttu-id="a2403-107">Questo oggetto viene usato per limitare il tipo di pacchetti acquisiti durante una sessione di acquisizione di pacchetti usando i criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="a2403-107">This object is used to restrict the type of packets that are captured during a packet capture session using the specified criteria.</span></span> <span data-ttu-id="a2403-108">Il cmdlet New-AzNetworkWatcherPacketCapture può accettare più oggetti Filter per abilitare sessioni di acquisizione componibili.</span><span class="sxs-lookup"><span data-stu-id="a2403-108">The New-AzNetworkWatcherPacketCapture cmdlet can accept multiple filter objects to enable composable capture sessions.</span></span>

## <span data-ttu-id="a2403-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a2403-109">EXAMPLES</span></span>

### <span data-ttu-id="a2403-110">Esempio 1: creare un'acquisizione di pacchetti con più filtri</span><span class="sxs-lookup"><span data-stu-id="a2403-110">Example 1: Create a Packet Capture with multiple filters</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2
```

<span data-ttu-id="a2403-111">In questo esempio creiamo un'acquisizione di pacchetti denominata "PacketCaptureTest" con più filtri e un limite di tempo.</span><span class="sxs-lookup"><span data-stu-id="a2403-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="a2403-112">Una volta completata la sessione, verrà salvata nell'account di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="a2403-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="a2403-113">Nota: l'estensione Azure Network Watcher deve essere installata nella macchina virtuale di destinazione per creare acquisizioni di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="a2403-113">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="a2403-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a2403-114">PARAMETERS</span></span>

### <span data-ttu-id="a2403-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2403-115">-DefaultProfile</span></span>
<span data-ttu-id="a2403-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a2403-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2403-117">-IndirizzoIPLocale</span><span class="sxs-lookup"><span data-stu-id="a2403-117">-LocalIPAddress</span></span>
<span data-ttu-id="a2403-118">Specifica l'indirizzo IP locale a cui applicare il filtro.</span><span class="sxs-lookup"><span data-stu-id="a2403-118">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="a2403-119">Input di esempio: "127.0.0.1" per l'immissione di un singolo indirizzo.</span><span class="sxs-lookup"><span data-stu-id="a2403-119">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="a2403-120">"127.0.0.1-127.0.0.255" per l'intervallo.</span><span class="sxs-lookup"><span data-stu-id="a2403-120">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="a2403-121">"127.0.0.1; 127.0.0.5;" per più voci.</span><span class="sxs-lookup"><span data-stu-id="a2403-121">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2403-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="a2403-122">-LocalPort</span></span>
<span data-ttu-id="a2403-123">Specifica l'indirizzo IP locale a cui applicare il filtro.</span><span class="sxs-lookup"><span data-stu-id="a2403-123">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="a2403-124">Input di esempio: "127.0.0.1" per l'immissione di un singolo indirizzo.</span><span class="sxs-lookup"><span data-stu-id="a2403-124">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="a2403-125">"127.0.0.1-127.0.0.255" per l'intervallo.</span><span class="sxs-lookup"><span data-stu-id="a2403-125">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="a2403-126">"127.0.0.1; 127.0.0.5;" per più voci.</span><span class="sxs-lookup"><span data-stu-id="a2403-126">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2403-127">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="a2403-127">-Protocol</span></span>
<span data-ttu-id="a2403-128">Specifica il protocollo su cui applicare il filtro.</span><span class="sxs-lookup"><span data-stu-id="a2403-128">Specifies the Protocol to filter on.</span></span> <span data-ttu-id="a2403-129">Valori accettabili "TCP", "UDP", "any"</span><span class="sxs-lookup"><span data-stu-id="a2403-129">Acceptable values "TCP","UDP","Any"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2403-130">-IndirizzoIPRemoto</span><span class="sxs-lookup"><span data-stu-id="a2403-130">-RemoteIPAddress</span></span>
<span data-ttu-id="a2403-131">Specifica l'indirizzo IP remoto su cui applicare il filtro.</span><span class="sxs-lookup"><span data-stu-id="a2403-131">Specifies the remote IP address to filter on.</span></span>
<span data-ttu-id="a2403-132">Input di esempio: "127.0.0.1" per l'immissione di un singolo indirizzo.</span><span class="sxs-lookup"><span data-stu-id="a2403-132">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="a2403-133">"127.0.0.1-127.0.0.255" per l'intervallo.</span><span class="sxs-lookup"><span data-stu-id="a2403-133">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="a2403-134">"127.0.0.1; 127.0.0.5;" per più voci.</span><span class="sxs-lookup"><span data-stu-id="a2403-134">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2403-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="a2403-135">-RemotePort</span></span>
<span data-ttu-id="a2403-136">Specifica la porta remota in cui applicare il filtro.</span><span class="sxs-lookup"><span data-stu-id="a2403-136">Specifies the Remote Port to filter on.</span></span>
<span data-ttu-id="a2403-137">Input di esempio di porta remota: "80" per l'immissione di una sola porta.</span><span class="sxs-lookup"><span data-stu-id="a2403-137">Remote port Example inputs: "80" for single port entry.</span></span>
<span data-ttu-id="a2403-138">"80-85" per l'intervallo.</span><span class="sxs-lookup"><span data-stu-id="a2403-138">"80-85" for range.</span></span>
<span data-ttu-id="a2403-139">"80; 443;" per più voci.</span><span class="sxs-lookup"><span data-stu-id="a2403-139">"80;443;" for multiple entries.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2403-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2403-140">CommonParameters</span></span>
<span data-ttu-id="a2403-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2403-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2403-142">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2403-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2403-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a2403-143">INPUTS</span></span>

### <span data-ttu-id="a2403-144">System. String</span><span class="sxs-lookup"><span data-stu-id="a2403-144">System.String</span></span>

## <span data-ttu-id="a2403-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a2403-145">OUTPUTS</span></span>

### <span data-ttu-id="a2403-146">Microsoft. Azure. Commands. Network. Models. PSPacketCaptureFilter</span><span class="sxs-lookup"><span data-stu-id="a2403-146">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span></span>

## <span data-ttu-id="a2403-147">Note</span><span class="sxs-lookup"><span data-stu-id="a2403-147">NOTES</span></span>
<span data-ttu-id="a2403-148">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Watcher, Packet, Capture, Traffic, Filter</span><span class="sxs-lookup"><span data-stu-id="a2403-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span> 

## <span data-ttu-id="a2403-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a2403-149">RELATED LINKS</span></span>

[<span data-ttu-id="a2403-150">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a2403-150">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="a2403-151">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a2403-151">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="a2403-152">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a2403-152">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="a2403-153">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="a2403-153">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="a2403-154">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="a2403-154">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="a2403-155">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="a2403-155">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="a2403-156">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="a2403-156">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="a2403-157">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a2403-157">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a2403-158">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="a2403-158">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="a2403-159">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a2403-159">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a2403-160">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a2403-160">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a2403-161">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a2403-161">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a2403-162">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="a2403-162">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="a2403-163">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="a2403-163">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="a2403-164">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="a2403-164">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="a2403-165">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a2403-165">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a2403-166">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a2403-166">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a2403-167">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a2403-167">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a2403-168">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="a2403-168">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="a2403-169">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a2403-169">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a2403-170">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a2403-170">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a2403-171">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="a2403-171">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="a2403-172">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="a2403-172">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="a2403-173">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="a2403-173">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="a2403-174">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="a2403-174">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="a2403-175">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="a2403-175">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="a2403-176">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a2403-176">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)