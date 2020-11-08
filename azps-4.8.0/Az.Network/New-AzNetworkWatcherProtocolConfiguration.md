---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherprotocolconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherProtocolConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherProtocolConfiguration.md
ms.openlocfilehash: 7f974d9be1faaaf4d78a2527250cdec1775ae49f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192777"
---
# <span data-ttu-id="4c64c-101">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="4c64c-101">New-AzNetworkWatcherProtocolConfiguration</span></span>

## <span data-ttu-id="4c64c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4c64c-102">SYNOPSIS</span></span>
<span data-ttu-id="4c64c-103">Crea un nuovo oggetto di configurazione del protocollo.</span><span class="sxs-lookup"><span data-stu-id="4c64c-103">Creates a new protocol configuration object.</span></span>

## <span data-ttu-id="4c64c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4c64c-104">SYNTAX</span></span>

```
New-AzNetworkWatcherProtocolConfiguration -Protocol <String> [-Method <String>] [-Header <IDictionary>]
 [-ValidStatusCode <Int32[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c64c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4c64c-105">DESCRIPTION</span></span>
<span data-ttu-id="4c64c-106">Il cmdlet New-AzNetworkWatcherProtocolConfiguration crea un nuovo oggetto di configurazione del protocollo.</span><span class="sxs-lookup"><span data-stu-id="4c64c-106">The New-AzNetworkWatcherProtocolConfiguration cmdlet creates a new protocol configuration object.</span></span> <span data-ttu-id="4c64c-107">Questo oggetto viene usato per limitare la configurazione del protocollo durante una sessione di controllo della connettività usando i criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="4c64c-107">This object is used to restrict the protocol configuration during a connectivity check session using the specified criteria.</span></span> 

## <span data-ttu-id="4c64c-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4c64c-108">EXAMPLES</span></span>

### <span data-ttu-id="4c64c-109">Esempio 1: testare la connettività di Network Watcher da una VM a un sito Web con la configurazione del protocollo</span><span class="sxs-lookup"><span data-stu-id="4c64c-109">Example 1: Test Network Watcher Connectivity from a VM to a website with protocol configuration</span></span>
```
$config = New-AzNetworkWatcherProtocolConfiguration -Protocol Http -Method Get -Headers @{"accept"="application/json"} -ValidStatusCodes @(200,202,204)

Test-AzNetworkWatcherConnectivity -NetworkWatcherName NetworkWatcher -ResourceGroupName NetworkWatcherRG -SourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" -DestinationAddress "bing.com" -DestinationPort 80 -ProtocolConfiguration $config


ConnectionStatus : Reachable
AvgLatencyInMs   : 4
MinLatencyInMs   : 2
MaxLatencyInMs   : 15
ProbesSent       : 15
ProbesFailed     : 0
Hops             : [
                     {
                       "Type": "Source",
                       "Id": "f8cff464-e13f-457f-a09e-4dcd53d38a85",
                       "Address": "10.1.1.4",
                       "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/provi                   iders/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                       "NextHopIds": [
                         "1034b1bf-0b1b-4f0a-93b2-900477f45485"
                       ],
                       "Issues": []
                     },
                     {
                       "Type": "Internet",
                       "Id": "1034b1bf-0b1b-4f0a-93b2-900477f45485",
                       "Address": "13.107.21.200",
                       "ResourceId": "Internet",
                       "NextHopIds": [],
                       "Issues": []
                     }
                   ]
```

<span data-ttu-id="4c64c-110">In questo esempio verifichiamo la connettività da una VM in Azure a www.bing.com.</span><span class="sxs-lookup"><span data-stu-id="4c64c-110">In this example we test connectivity from a VM in Azure to www.bing.com.</span></span>

## <span data-ttu-id="4c64c-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4c64c-111">PARAMETERS</span></span>

### <span data-ttu-id="4c64c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c64c-112">-DefaultProfile</span></span>
<span data-ttu-id="4c64c-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4c64c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c64c-114">-Intestazione</span><span class="sxs-lookup"><span data-stu-id="4c64c-114">-Header</span></span>
<span data-ttu-id="4c64c-115">elenco di intestazioni HTTP</span><span class="sxs-lookup"><span data-stu-id="4c64c-115">list of HTTP headers</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c64c-116">-Method</span><span class="sxs-lookup"><span data-stu-id="4c64c-116">-Method</span></span>
<span data-ttu-id="4c64c-117">Metodo HTTP</span><span class="sxs-lookup"><span data-stu-id="4c64c-117">HTTP method</span></span>

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

### <span data-ttu-id="4c64c-118">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="4c64c-118">-Protocol</span></span>
<span data-ttu-id="4c64c-119">Tipo di protocollo</span><span class="sxs-lookup"><span data-stu-id="4c64c-119">Protocol type</span></span>

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

### <span data-ttu-id="4c64c-120">-ValidStatusCode</span><span class="sxs-lookup"><span data-stu-id="4c64c-120">-ValidStatusCode</span></span>
<span data-ttu-id="4c64c-121">codici di stato validi</span><span class="sxs-lookup"><span data-stu-id="4c64c-121">valid status codes</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c64c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c64c-122">CommonParameters</span></span>
<span data-ttu-id="4c64c-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c64c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c64c-124">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c64c-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c64c-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4c64c-125">INPUTS</span></span>

### <span data-ttu-id="4c64c-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4c64c-126">None</span></span>

## <span data-ttu-id="4c64c-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4c64c-127">OUTPUTS</span></span>

### <span data-ttu-id="4c64c-128">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="4c64c-128">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherProtocolConfiguration</span></span>

## <span data-ttu-id="4c64c-129">Note</span><span class="sxs-lookup"><span data-stu-id="4c64c-129">NOTES</span></span>
<span data-ttu-id="4c64c-130">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Watcher, Packet, Capture, Traffic, Filter</span><span class="sxs-lookup"><span data-stu-id="4c64c-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span>

## <span data-ttu-id="4c64c-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4c64c-131">RELATED LINKS</span></span>

[<span data-ttu-id="4c64c-132">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4c64c-132">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="4c64c-133">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4c64c-133">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="4c64c-134">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4c64c-134">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="4c64c-135">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="4c64c-135">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="4c64c-136">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="4c64c-136">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="4c64c-137">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="4c64c-137">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="4c64c-138">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="4c64c-138">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="4c64c-139">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4c64c-139">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4c64c-140">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="4c64c-140">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="4c64c-141">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4c64c-141">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4c64c-142">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4c64c-142">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4c64c-143">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4c64c-143">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4c64c-144">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="4c64c-144">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="4c64c-145">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="4c64c-145">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="4c64c-146">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="4c64c-146">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="4c64c-147">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4c64c-147">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4c64c-148">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4c64c-148">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4c64c-149">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4c64c-149">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4c64c-150">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="4c64c-150">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="4c64c-151">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4c64c-151">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4c64c-152">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4c64c-152">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4c64c-153">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="4c64c-153">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="4c64c-154">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="4c64c-154">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="4c64c-155">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="4c64c-155">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="4c64c-156">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="4c64c-156">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="4c64c-157">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="4c64c-157">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="4c64c-158">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4c64c-158">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
