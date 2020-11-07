---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchernexthop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
ms.openlocfilehash: 51fea717c352f00b4f356e6bb07b730cdeb60966
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678479"
---
# <span data-ttu-id="c7d4d-101">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c7d4d-101">Get-AzNetworkWatcherNextHop</span></span>

## <span data-ttu-id="c7d4d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c7d4d-102">SYNOPSIS</span></span>
<span data-ttu-id="c7d4d-103">Ottiene l'hop successivo da una VM.</span><span class="sxs-lookup"><span data-stu-id="c7d4d-103">Gets the next hop from a VM.</span></span>

## <span data-ttu-id="c7d4d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c7d4d-104">SYNTAX</span></span>

### <span data-ttu-id="c7d4d-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c7d4d-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7d4d-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="c7d4d-106">SetByName</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7d4d-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="c7d4d-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherNextHop -Location <String> -TargetVirtualMachineId <String> -DestinationIPAddress <String>
 -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7d4d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c7d4d-108">DESCRIPTION</span></span>
<span data-ttu-id="c7d4d-109">Il cmdlet Get-AzNetworkWatcherNextHop Ottiene l'hop successivo da una VM.</span><span class="sxs-lookup"><span data-stu-id="c7d4d-109">The Get-AzNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="c7d4d-110">L'hop successivo consente di visualizzare il tipo di risorsa Azure, l'indirizzo IP associato della risorsa e la regola della tabella di routing responsabile della route.</span><span class="sxs-lookup"><span data-stu-id="c7d4d-110">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="c7d4d-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c7d4d-111">EXAMPLES</span></span>

### <span data-ttu-id="c7d4d-112">Esempio 1: ottenere l'hop successivo quando si comunica con un IP Internet</span><span class="sxs-lookup"><span data-stu-id="c7d4d-112">Example 1: Get the Next Hop when communicating with an Internet IP</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0
$Nics = Get-AzNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}
Get-AzNetworkWatcherNextHop -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -SourceIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress  -DestinationIPAddress 204.79.197.200


NextHopIpAddress NextHopType RouteTableId
---------------- ----------- ------------
                 Internet    System Route
```

<span data-ttu-id="c7d4d-113">Ottenere l'hop successivo per le comunicazioni in uscita dall'interfaccia di rete principale nel Vachine virtuale specificato a 204.79.197.200 (www.bing.com)</span><span class="sxs-lookup"><span data-stu-id="c7d4d-113">Get's the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Vachine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="c7d4d-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c7d4d-114">PARAMETERS</span></span>

### <span data-ttu-id="c7d4d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c7d4d-115">-AsJob</span></span>
<span data-ttu-id="c7d4d-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c7d4d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c7d4d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7d4d-117">-DefaultProfile</span></span>
<span data-ttu-id="c7d4d-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c7d4d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7d4d-119">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="c7d4d-119">-DestinationIPAddress</span></span>
<span data-ttu-id="c7d4d-120">Indirizzo IP di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c7d4d-120">Destination IP address.</span></span>

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

### <span data-ttu-id="c7d4d-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="c7d4d-121">-Location</span></span>
<span data-ttu-id="c7d4d-122">Posizione del monitoraggio della rete.</span><span class="sxs-lookup"><span data-stu-id="c7d4d-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="c7d4d-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c7d4d-123">-NetworkWatcher</span></span>
<span data-ttu-id="c7d4d-124">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="c7d4d-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="c7d4d-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="c7d4d-125">-NetworkWatcherName</span></span>
<span data-ttu-id="c7d4d-126">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="c7d4d-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="c7d4d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7d4d-127">-ResourceGroupName</span></span>
<span data-ttu-id="c7d4d-128">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="c7d4d-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="c7d4d-129">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="c7d4d-129">-SourceIPAddress</span></span>
<span data-ttu-id="c7d4d-130">Indirizzo IP di origine.</span><span class="sxs-lookup"><span data-stu-id="c7d4d-130">Source IP address.</span></span>

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

### <span data-ttu-id="c7d4d-131">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="c7d4d-131">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="c7d4d-132">ID interfaccia di rete di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c7d4d-132">Target network interface Id.</span></span>

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

### <span data-ttu-id="c7d4d-133">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="c7d4d-133">-TargetVirtualMachineId</span></span>
<span data-ttu-id="c7d4d-134">ID macchina virtuale di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c7d4d-134">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="c7d4d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7d4d-135">CommonParameters</span></span>
<span data-ttu-id="c7d4d-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7d4d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7d4d-137">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c7d4d-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7d4d-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c7d4d-138">INPUTS</span></span>

### <span data-ttu-id="c7d4d-139">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c7d4d-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="c7d4d-140">System. String</span><span class="sxs-lookup"><span data-stu-id="c7d4d-140">System.String</span></span>

## <span data-ttu-id="c7d4d-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c7d4d-141">OUTPUTS</span></span>

### <span data-ttu-id="c7d4d-142">Microsoft. Azure. Commands. Network. Models. PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="c7d4d-142">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="c7d4d-143">Note</span><span class="sxs-lookup"><span data-stu-id="c7d4d-143">NOTES</span></span>
<span data-ttu-id="c7d4d-144">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher, Next, hop</span><span class="sxs-lookup"><span data-stu-id="c7d4d-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="c7d4d-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c7d4d-145">RELATED LINKS</span></span>

[<span data-ttu-id="c7d4d-146">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c7d4d-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="c7d4d-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c7d4d-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="c7d4d-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c7d4d-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="c7d4d-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c7d4d-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="c7d4d-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c7d4d-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c7d4d-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c7d4d-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="c7d4d-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c7d4d-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="c7d4d-153">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c7d4d-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c7d4d-154">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c7d4d-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="c7d4d-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c7d4d-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c7d4d-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c7d4d-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c7d4d-157">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c7d4d-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c7d4d-158">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7d4d-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="c7d4d-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c7d4d-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="c7d4d-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="c7d4d-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="c7d4d-161">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c7d4d-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c7d4d-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c7d4d-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c7d4d-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c7d4d-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c7d4d-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="c7d4d-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="c7d4d-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c7d4d-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c7d4d-166">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c7d4d-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c7d4d-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="c7d4d-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="c7d4d-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="c7d4d-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="c7d4d-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="c7d4d-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="c7d4d-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="c7d4d-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="c7d4d-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="c7d4d-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="c7d4d-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c7d4d-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
