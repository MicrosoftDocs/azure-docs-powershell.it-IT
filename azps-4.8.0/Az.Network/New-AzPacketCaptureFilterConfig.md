---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpacketcapturefilterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
ms.openlocfilehash: 194e3c71cc763aeb74091f912b37dd15e4dfe4aa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192327"
---
# <span data-ttu-id="95f56-101">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="95f56-101">New-AzPacketCaptureFilterConfig</span></span>

## <span data-ttu-id="95f56-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="95f56-102">SYNOPSIS</span></span>
<span data-ttu-id="95f56-103">Crea un nuovo oggetto filtro di acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="95f56-103">Creates a new packet capture filter object.</span></span>

## <span data-ttu-id="95f56-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="95f56-104">SYNTAX</span></span>

```
New-AzPacketCaptureFilterConfig [-Protocol <String>] [-RemoteIPAddress <String>] [-LocalIPAddress <String>]
 [-LocalPort <String>] [-RemotePort <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95f56-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95f56-105">DESCRIPTION</span></span>
<span data-ttu-id="95f56-106">Il cmdlet New-AzPacketCaptureFilterConfig crea un nuovo oggetto filtro di acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="95f56-106">The New-AzPacketCaptureFilterConfig cmdlet creates a new packet capture filter object.</span></span> <span data-ttu-id="95f56-107">Questo oggetto viene usato per limitare il tipo di pacchetti acquisiti durante una sessione di acquisizione di pacchetti usando i criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="95f56-107">This object is used to restrict the type of packets that are captured during a packet capture session using the specified criteria.</span></span> <span data-ttu-id="95f56-108">Il cmdlet New-AzNetworkWatcherPacketCapture può accettare più oggetti Filter per abilitare sessioni di acquisizione componibili.</span><span class="sxs-lookup"><span data-stu-id="95f56-108">The New-AzNetworkWatcherPacketCapture cmdlet can accept multiple filter objects to enable composable capture sessions.</span></span>

## <span data-ttu-id="95f56-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="95f56-109">EXAMPLES</span></span>

### <span data-ttu-id="95f56-110">Esempio 1: creare un'acquisizione di pacchetti con più filtri</span><span class="sxs-lookup"><span data-stu-id="95f56-110">Example 1: Create a Packet Capture with multiple filters</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2
```

<span data-ttu-id="95f56-111">In questo esempio creiamo un'acquisizione di pacchetti denominata "PacketCaptureTest" con più filtri e un limite di tempo.</span><span class="sxs-lookup"><span data-stu-id="95f56-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="95f56-112">Una volta completata la sessione, verrà salvata nell'account di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="95f56-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="95f56-113">Nota: l'estensione Azure Network Watcher deve essere installata nella macchina virtuale di destinazione per creare acquisizioni di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="95f56-113">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="95f56-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="95f56-114">PARAMETERS</span></span>

### <span data-ttu-id="95f56-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95f56-115">-DefaultProfile</span></span>
<span data-ttu-id="95f56-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="95f56-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95f56-117">-IndirizzoIPLocale</span><span class="sxs-lookup"><span data-stu-id="95f56-117">-LocalIPAddress</span></span>
<span data-ttu-id="95f56-118">Specifica l'indirizzo IP locale a cui applicare il filtro.</span><span class="sxs-lookup"><span data-stu-id="95f56-118">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="95f56-119">Input di esempio: "127.0.0.1" per l'immissione di un singolo indirizzo.</span><span class="sxs-lookup"><span data-stu-id="95f56-119">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="95f56-120">"127.0.0.1-127.0.0.255" per l'intervallo.</span><span class="sxs-lookup"><span data-stu-id="95f56-120">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="95f56-121">"127.0.0.1; 127.0.0.5;" per più voci.</span><span class="sxs-lookup"><span data-stu-id="95f56-121">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="95f56-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="95f56-122">-LocalPort</span></span>
<span data-ttu-id="95f56-123">Specifica l'indirizzo IP locale a cui applicare il filtro.</span><span class="sxs-lookup"><span data-stu-id="95f56-123">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="95f56-124">Input di esempio: "127.0.0.1" per l'immissione di un singolo indirizzo.</span><span class="sxs-lookup"><span data-stu-id="95f56-124">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="95f56-125">"127.0.0.1-127.0.0.255" per l'intervallo.</span><span class="sxs-lookup"><span data-stu-id="95f56-125">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="95f56-126">"127.0.0.1; 127.0.0.5;" per più voci.</span><span class="sxs-lookup"><span data-stu-id="95f56-126">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="95f56-127">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="95f56-127">-Protocol</span></span>
<span data-ttu-id="95f56-128">Specifica il protocollo su cui applicare il filtro.</span><span class="sxs-lookup"><span data-stu-id="95f56-128">Specifies the Protocol to filter on.</span></span> <span data-ttu-id="95f56-129">Valori accettabili "TCP", "UDP", "any"</span><span class="sxs-lookup"><span data-stu-id="95f56-129">Acceptable values "TCP","UDP","Any"</span></span>

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

### <span data-ttu-id="95f56-130">-IndirizzoIPRemoto</span><span class="sxs-lookup"><span data-stu-id="95f56-130">-RemoteIPAddress</span></span>
<span data-ttu-id="95f56-131">Specifica l'indirizzo IP remoto su cui applicare il filtro.</span><span class="sxs-lookup"><span data-stu-id="95f56-131">Specifies the remote IP address to filter on.</span></span>
<span data-ttu-id="95f56-132">Input di esempio: "127.0.0.1" per l'immissione di un singolo indirizzo.</span><span class="sxs-lookup"><span data-stu-id="95f56-132">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="95f56-133">"127.0.0.1-127.0.0.255" per l'intervallo.</span><span class="sxs-lookup"><span data-stu-id="95f56-133">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="95f56-134">"127.0.0.1; 127.0.0.5;" per più voci.</span><span class="sxs-lookup"><span data-stu-id="95f56-134">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="95f56-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="95f56-135">-RemotePort</span></span>
<span data-ttu-id="95f56-136">Specifica la porta remota in cui applicare il filtro.</span><span class="sxs-lookup"><span data-stu-id="95f56-136">Specifies the Remote Port to filter on.</span></span>
<span data-ttu-id="95f56-137">Input di esempio di porta remota: "80" per l'immissione di una sola porta.</span><span class="sxs-lookup"><span data-stu-id="95f56-137">Remote port Example inputs: "80" for single port entry.</span></span>
<span data-ttu-id="95f56-138">"80-85" per l'intervallo.</span><span class="sxs-lookup"><span data-stu-id="95f56-138">"80-85" for range.</span></span>
<span data-ttu-id="95f56-139">"80; 443;" per più voci.</span><span class="sxs-lookup"><span data-stu-id="95f56-139">"80;443;" for multiple entries.</span></span>

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

### <span data-ttu-id="95f56-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95f56-140">CommonParameters</span></span>
<span data-ttu-id="95f56-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95f56-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95f56-142">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95f56-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95f56-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="95f56-143">INPUTS</span></span>

### <span data-ttu-id="95f56-144">System. String</span><span class="sxs-lookup"><span data-stu-id="95f56-144">System.String</span></span>

## <span data-ttu-id="95f56-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="95f56-145">OUTPUTS</span></span>

### <span data-ttu-id="95f56-146">Microsoft. Azure. Commands. Network. Models. PSPacketCaptureFilter</span><span class="sxs-lookup"><span data-stu-id="95f56-146">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span></span>

## <span data-ttu-id="95f56-147">Note</span><span class="sxs-lookup"><span data-stu-id="95f56-147">NOTES</span></span>
<span data-ttu-id="95f56-148">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Watcher, Packet, Capture, Traffic, Filter</span><span class="sxs-lookup"><span data-stu-id="95f56-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span> 

## <span data-ttu-id="95f56-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="95f56-149">RELATED LINKS</span></span>

[<span data-ttu-id="95f56-150">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="95f56-150">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="95f56-151">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="95f56-151">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="95f56-152">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="95f56-152">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="95f56-153">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="95f56-153">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="95f56-154">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="95f56-154">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="95f56-155">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="95f56-155">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="95f56-156">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="95f56-156">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="95f56-157">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="95f56-157">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="95f56-158">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="95f56-158">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="95f56-159">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="95f56-159">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="95f56-160">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="95f56-160">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="95f56-161">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="95f56-161">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="95f56-162">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="95f56-162">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="95f56-163">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="95f56-163">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="95f56-164">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="95f56-164">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="95f56-165">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="95f56-165">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="95f56-166">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="95f56-166">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="95f56-167">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="95f56-167">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="95f56-168">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="95f56-168">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="95f56-169">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="95f56-169">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="95f56-170">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="95f56-170">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="95f56-171">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="95f56-171">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="95f56-172">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="95f56-172">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="95f56-173">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="95f56-173">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="95f56-174">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="95f56-174">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="95f56-175">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="95f56-175">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="95f56-176">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="95f56-176">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)