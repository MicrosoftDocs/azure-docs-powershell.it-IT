---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherprotocolconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherProtocolConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherProtocolConfiguration.md
ms.openlocfilehash: b7c16c529bb8e3a45d45c31dd985f43f138aee6c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678253"
---
# <span data-ttu-id="a7fa9-101">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="a7fa9-101">New-AzNetworkWatcherProtocolConfiguration</span></span>

## <span data-ttu-id="a7fa9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a7fa9-102">SYNOPSIS</span></span>
<span data-ttu-id="a7fa9-103">Crea un nuovo oggetto di configurazione del protocollo.</span><span class="sxs-lookup"><span data-stu-id="a7fa9-103">Creates a new protocol configuration object.</span></span>

## <span data-ttu-id="a7fa9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a7fa9-104">SYNTAX</span></span>

```
New-AzNetworkWatcherProtocolConfiguration -Protocol <String> [-Method <String>] [-Header <IDictionary>]
 [-ValidStatusCode <Int32[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7fa9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a7fa9-105">DESCRIPTION</span></span>
<span data-ttu-id="a7fa9-106">Il cmdlet New-AzNetworkWatcherProtocolConfiguration crea un nuovo oggetto di configurazione del protocollo.</span><span class="sxs-lookup"><span data-stu-id="a7fa9-106">The New-AzNetworkWatcherProtocolConfiguration cmdlet creates a new protocol configuration object.</span></span> <span data-ttu-id="a7fa9-107">Questo oggetto viene usato per limitare il protocollo confiuration durante una sessione di controllo connecitivity con i criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="a7fa9-107">This object is used to restrict the protocol confiuration during a connecitivity check session using the specified criteria.</span></span> 

## <span data-ttu-id="a7fa9-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a7fa9-108">EXAMPLES</span></span>

### <span data-ttu-id="a7fa9-109">Esempio 1: testare la connettività di Network Watcher da una VM a un sito Web con la configurazione del protocollo</span><span class="sxs-lookup"><span data-stu-id="a7fa9-109">Example 1: Test Network Watcher Connectivity from a VM to a website with protocol configuration</span></span>
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

<span data-ttu-id="a7fa9-110">In questo esempio verifichiamo la connettività da una VM in Azure a www.bing.com.</span><span class="sxs-lookup"><span data-stu-id="a7fa9-110">In this example we test connectivity from a VM in Azure to www.bing.com.</span></span>

## <span data-ttu-id="a7fa9-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a7fa9-111">PARAMETERS</span></span>

### <span data-ttu-id="a7fa9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7fa9-112">-DefaultProfile</span></span>
<span data-ttu-id="a7fa9-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a7fa9-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7fa9-114">-Intestazione</span><span class="sxs-lookup"><span data-stu-id="a7fa9-114">-Header</span></span>
<span data-ttu-id="a7fa9-115">elenco di intestazioni HTTP</span><span class="sxs-lookup"><span data-stu-id="a7fa9-115">list of HTTP headers</span></span>

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

### <span data-ttu-id="a7fa9-116">-Method</span><span class="sxs-lookup"><span data-stu-id="a7fa9-116">-Method</span></span>
<span data-ttu-id="a7fa9-117">Metodo HTTP</span><span class="sxs-lookup"><span data-stu-id="a7fa9-117">HTTP method</span></span>

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

### <span data-ttu-id="a7fa9-118">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="a7fa9-118">-Protocol</span></span>
<span data-ttu-id="a7fa9-119">Tipo procotol</span><span class="sxs-lookup"><span data-stu-id="a7fa9-119">Procotol type</span></span>

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

### <span data-ttu-id="a7fa9-120">-ValidStatusCode</span><span class="sxs-lookup"><span data-stu-id="a7fa9-120">-ValidStatusCode</span></span>
<span data-ttu-id="a7fa9-121">codici di stato validi</span><span class="sxs-lookup"><span data-stu-id="a7fa9-121">valid status codes</span></span>

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

### <span data-ttu-id="a7fa9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7fa9-122">CommonParameters</span></span>
<span data-ttu-id="a7fa9-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7fa9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7fa9-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7fa9-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7fa9-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a7fa9-125">INPUTS</span></span>

### <span data-ttu-id="a7fa9-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a7fa9-126">None</span></span>

## <span data-ttu-id="a7fa9-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a7fa9-127">OUTPUTS</span></span>

### <span data-ttu-id="a7fa9-128">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="a7fa9-128">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherProtocolConfiguration</span></span>

## <span data-ttu-id="a7fa9-129">Note</span><span class="sxs-lookup"><span data-stu-id="a7fa9-129">NOTES</span></span>
<span data-ttu-id="a7fa9-130">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Watcher, Packet, Capture, Traffic, Filter</span><span class="sxs-lookup"><span data-stu-id="a7fa9-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span>

## <span data-ttu-id="a7fa9-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a7fa9-131">RELATED LINKS</span></span>

[<span data-ttu-id="a7fa9-132">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a7fa9-132">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="a7fa9-133">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a7fa9-133">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="a7fa9-134">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a7fa9-134">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="a7fa9-135">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="a7fa9-135">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="a7fa9-136">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="a7fa9-136">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="a7fa9-137">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="a7fa9-137">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="a7fa9-138">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="a7fa9-138">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="a7fa9-139">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a7fa9-139">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a7fa9-140">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="a7fa9-140">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="a7fa9-141">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a7fa9-141">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a7fa9-142">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a7fa9-142">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a7fa9-143">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a7fa9-143">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a7fa9-144">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="a7fa9-144">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="a7fa9-145">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="a7fa9-145">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="a7fa9-146">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="a7fa9-146">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="a7fa9-147">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a7fa9-147">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a7fa9-148">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a7fa9-148">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a7fa9-149">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a7fa9-149">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a7fa9-150">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="a7fa9-150">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="a7fa9-151">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a7fa9-151">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a7fa9-152">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a7fa9-152">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a7fa9-153">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="a7fa9-153">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="a7fa9-154">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="a7fa9-154">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="a7fa9-155">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="a7fa9-155">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="a7fa9-156">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="a7fa9-156">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="a7fa9-157">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="a7fa9-157">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="a7fa9-158">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a7fa9-158">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)