---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchernexthop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
ms.openlocfilehash: 7fe316bda1cc6385babad2b5a7cb03d44a6fc128
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864650"
---
# <span data-ttu-id="5d4c1-101">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="5d4c1-101">Get-AzNetworkWatcherNextHop</span></span>

## <span data-ttu-id="5d4c1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5d4c1-102">SYNOPSIS</span></span>
<span data-ttu-id="5d4c1-103">Ottiene l'hop successivo da una VM.</span><span class="sxs-lookup"><span data-stu-id="5d4c1-103">Gets the next hop from a VM.</span></span>

## <span data-ttu-id="5d4c1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5d4c1-104">SYNTAX</span></span>

### <span data-ttu-id="5d4c1-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5d4c1-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d4c1-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="5d4c1-106">SetByName</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d4c1-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="5d4c1-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherNextHop -Location <String> -TargetVirtualMachineId <String> -DestinationIPAddress <String>
 -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d4c1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5d4c1-108">DESCRIPTION</span></span>
<span data-ttu-id="5d4c1-109">Il cmdlet Get-AzNetworkWatcherNextHop Ottiene l'hop successivo da una VM.</span><span class="sxs-lookup"><span data-stu-id="5d4c1-109">The Get-AzNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="5d4c1-110">L'hop successivo consente di visualizzare il tipo di risorsa Azure, l'indirizzo IP associato della risorsa e la regola della tabella di routing responsabile della route.</span><span class="sxs-lookup"><span data-stu-id="5d4c1-110">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="5d4c1-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5d4c1-111">EXAMPLES</span></span>

### <span data-ttu-id="5d4c1-112">Esempio 1: ottenere l'hop successivo quando si comunica con un IP Internet</span><span class="sxs-lookup"><span data-stu-id="5d4c1-112">Example 1: Get the Next Hop when communicating with an Internet IP</span></span>
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

<span data-ttu-id="5d4c1-113">Ottiene l'hop successivo per le comunicazioni in uscita dall'interfaccia di rete principale nella macchina virtuale specificata in 204.79.197.200 (www.bing.com)</span><span class="sxs-lookup"><span data-stu-id="5d4c1-113">Gets the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Machine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="5d4c1-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5d4c1-114">PARAMETERS</span></span>

### <span data-ttu-id="5d4c1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5d4c1-115">-AsJob</span></span>
<span data-ttu-id="5d4c1-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="5d4c1-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5d4c1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d4c1-117">-DefaultProfile</span></span>
<span data-ttu-id="5d4c1-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5d4c1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d4c1-119">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="5d4c1-119">-DestinationIPAddress</span></span>
<span data-ttu-id="5d4c1-120">Indirizzo IP di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5d4c1-120">Destination IP address.</span></span>

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

### <span data-ttu-id="5d4c1-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="5d4c1-121">-Location</span></span>
<span data-ttu-id="5d4c1-122">Posizione del monitoraggio della rete.</span><span class="sxs-lookup"><span data-stu-id="5d4c1-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="5d4c1-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5d4c1-123">-NetworkWatcher</span></span>
<span data-ttu-id="5d4c1-124">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="5d4c1-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="5d4c1-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="5d4c1-125">-NetworkWatcherName</span></span>
<span data-ttu-id="5d4c1-126">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="5d4c1-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="5d4c1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d4c1-127">-ResourceGroupName</span></span>
<span data-ttu-id="5d4c1-128">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="5d4c1-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="5d4c1-129">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="5d4c1-129">-SourceIPAddress</span></span>
<span data-ttu-id="5d4c1-130">Indirizzo IP di origine.</span><span class="sxs-lookup"><span data-stu-id="5d4c1-130">Source IP address.</span></span>

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

### <span data-ttu-id="5d4c1-131">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="5d4c1-131">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="5d4c1-132">ID interfaccia di rete di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5d4c1-132">Target network interface Id.</span></span>

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

### <span data-ttu-id="5d4c1-133">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="5d4c1-133">-TargetVirtualMachineId</span></span>
<span data-ttu-id="5d4c1-134">ID macchina virtuale di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5d4c1-134">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="5d4c1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d4c1-135">CommonParameters</span></span>
<span data-ttu-id="5d4c1-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d4c1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d4c1-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5d4c1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d4c1-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5d4c1-138">INPUTS</span></span>

### <span data-ttu-id="5d4c1-139">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5d4c1-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="5d4c1-140">System. String</span><span class="sxs-lookup"><span data-stu-id="5d4c1-140">System.String</span></span>

## <span data-ttu-id="5d4c1-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5d4c1-141">OUTPUTS</span></span>

### <span data-ttu-id="5d4c1-142">Microsoft. Azure. Commands. Network. Models. PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="5d4c1-142">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="5d4c1-143">Note</span><span class="sxs-lookup"><span data-stu-id="5d4c1-143">NOTES</span></span>
<span data-ttu-id="5d4c1-144">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher, Next, hop</span><span class="sxs-lookup"><span data-stu-id="5d4c1-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="5d4c1-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5d4c1-145">RELATED LINKS</span></span>

[<span data-ttu-id="5d4c1-146">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5d4c1-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="5d4c1-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5d4c1-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="5d4c1-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5d4c1-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="5d4c1-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="5d4c1-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="5d4c1-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="5d4c1-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="5d4c1-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="5d4c1-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="5d4c1-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="5d4c1-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="5d4c1-153">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5d4c1-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5d4c1-154">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="5d4c1-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="5d4c1-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5d4c1-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5d4c1-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5d4c1-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5d4c1-157">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5d4c1-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5d4c1-158">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="5d4c1-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="5d4c1-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="5d4c1-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="5d4c1-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="5d4c1-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="5d4c1-161">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5d4c1-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5d4c1-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5d4c1-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5d4c1-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5d4c1-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5d4c1-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="5d4c1-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="5d4c1-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5d4c1-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5d4c1-166">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5d4c1-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5d4c1-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="5d4c1-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="5d4c1-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="5d4c1-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="5d4c1-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="5d4c1-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="5d4c1-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="5d4c1-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="5d4c1-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="5d4c1-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="5d4c1-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5d4c1-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
