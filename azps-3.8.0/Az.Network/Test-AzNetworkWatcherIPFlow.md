---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-aznetworkwatcheripflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
ms.openlocfilehash: e20c0087c44ee7dbf29d65733712eb28022da1b2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020615"
---
# <span data-ttu-id="7ab1e-101">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="7ab1e-101">Test-AzNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="7ab1e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7ab1e-102">SYNOPSIS</span></span>
<span data-ttu-id="7ab1e-103">Restituisce un valore che indica se il pacchetto è consentito o negato per o da una determinata destinazione.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

## <span data-ttu-id="7ab1e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7ab1e-104">SYNTAX</span></span>

### <span data-ttu-id="7ab1e-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7ab1e-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ab1e-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="7ab1e-106">SetByName</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ab1e-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="7ab1e-107">SetByLocation</span></span>
```
Test-AzNetworkWatcherIPFlow -Location <String> -TargetVirtualMachineId <String> -Direction <String>
 -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ab1e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ab1e-108">DESCRIPTION</span></span>
<span data-ttu-id="7ab1e-109">Il cmdlet Test-AzNetworkWatcherIPFlow, per una risorsa VM specificata e un pacchetto con una direzione specificata con gli indirizzi IP locali e remoti e le porte, restituisce se il pacchetto è consentito o negato.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-109">The Test-AzNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="7ab1e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7ab1e-110">EXAMPLES</span></span>

### <span data-ttu-id="7ab1e-111">Esempio 1: eseguire Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="7ab1e-111">Example 1: Run Test-AzNetworkWatcherIPFlow</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzNetworkInterface | Where-Object { $vm.NetworkProfile.NetworkInterfaces.Id -contains $_.Id }

Test-AzNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="7ab1e-112">Ottiene il Network Watcher in West Central US per questo abbonamento, quindi ottiene la VM ed è associata alle interfacce di rete.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-112">Gets the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="7ab1e-113">Quindi, per la prima interfaccia di rete, viene eseguito Test-AzNetworkWatcherIPFlow usando il primo IP della prima interfaccia di rete per una connessione in uscita a un IP su Internet.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-113">Then for the first Network Interface, runs Test-AzNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="7ab1e-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7ab1e-114">PARAMETERS</span></span>

### <span data-ttu-id="7ab1e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7ab1e-115">-AsJob</span></span>
<span data-ttu-id="7ab1e-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7ab1e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7ab1e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ab1e-117">-DefaultProfile</span></span>
<span data-ttu-id="7ab1e-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ab1e-119">-Direzione</span><span class="sxs-lookup"><span data-stu-id="7ab1e-119">-Direction</span></span>
<span data-ttu-id="7ab1e-120">Direzione.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-120">Direction.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Inbound, Outbound

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ab1e-121">-IndirizzoIPLocale</span><span class="sxs-lookup"><span data-stu-id="7ab1e-121">-LocalIPAddress</span></span>
<span data-ttu-id="7ab1e-122">Indirizzo IP locale.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-122">Local IP Address.</span></span>

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

### <span data-ttu-id="7ab1e-123">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="7ab1e-123">-LocalPort</span></span>
<span data-ttu-id="7ab1e-124">Porta locale.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-124">Local Port.</span></span>

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

### <span data-ttu-id="7ab1e-125">-Posizione</span><span class="sxs-lookup"><span data-stu-id="7ab1e-125">-Location</span></span>
<span data-ttu-id="7ab1e-126">Posizione del monitoraggio della rete.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="7ab1e-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7ab1e-127">-NetworkWatcher</span></span>
<span data-ttu-id="7ab1e-128">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="7ab1e-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="7ab1e-129">-NetworkWatcherName</span></span>
<span data-ttu-id="7ab1e-130">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="7ab1e-131">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="7ab1e-131">-Protocol</span></span>
<span data-ttu-id="7ab1e-132">Protocollo.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-132">Protocol.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TCP, UDP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ab1e-133">-IndirizzoIPRemoto</span><span class="sxs-lookup"><span data-stu-id="7ab1e-133">-RemoteIPAddress</span></span>
<span data-ttu-id="7ab1e-134">Indirizzo IP remoto.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-134">Remote IP Address.</span></span>

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

### <span data-ttu-id="7ab1e-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="7ab1e-135">-RemotePort</span></span>
<span data-ttu-id="7ab1e-136">Porta remota.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-136">Remote port.</span></span>

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

### <span data-ttu-id="7ab1e-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ab1e-137">-ResourceGroupName</span></span>
<span data-ttu-id="7ab1e-138">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-138">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="7ab1e-139">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="7ab1e-139">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="7ab1e-140">ID interfaccia di rete di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-140">Target network interface Id.</span></span>

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

### <span data-ttu-id="7ab1e-141">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="7ab1e-141">-TargetVirtualMachineId</span></span>
<span data-ttu-id="7ab1e-142">ID macchina virtuale di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-142">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="7ab1e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ab1e-143">CommonParameters</span></span>
<span data-ttu-id="7ab1e-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ab1e-145">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ab1e-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ab1e-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7ab1e-146">INPUTS</span></span>

### <span data-ttu-id="7ab1e-147">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7ab1e-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="7ab1e-148">System. String</span><span class="sxs-lookup"><span data-stu-id="7ab1e-148">System.String</span></span>

## <span data-ttu-id="7ab1e-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7ab1e-149">OUTPUTS</span></span>

### <span data-ttu-id="7ab1e-150">Microsoft. Azure. Commands. Network. Models. PSIPFlowVerifyResult</span><span class="sxs-lookup"><span data-stu-id="7ab1e-150">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="7ab1e-151">Note</span><span class="sxs-lookup"><span data-stu-id="7ab1e-151">NOTES</span></span>
<span data-ttu-id="7ab1e-152">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher, Flow, IP</span><span class="sxs-lookup"><span data-stu-id="7ab1e-152">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="7ab1e-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7ab1e-153">RELATED LINKS</span></span>

[<span data-ttu-id="7ab1e-154">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7ab1e-154">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="7ab1e-155">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7ab1e-155">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="7ab1e-156">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7ab1e-156">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="7ab1e-157">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="7ab1e-157">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="7ab1e-158">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="7ab1e-158">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="7ab1e-159">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="7ab1e-159">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="7ab1e-160">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="7ab1e-160">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="7ab1e-161">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7ab1e-161">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7ab1e-162">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="7ab1e-162">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="7ab1e-163">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7ab1e-163">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7ab1e-164">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7ab1e-164">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7ab1e-165">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7ab1e-165">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7ab1e-166">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ab1e-166">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="7ab1e-167">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="7ab1e-167">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="7ab1e-168">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="7ab1e-168">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="7ab1e-169">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7ab1e-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7ab1e-170">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7ab1e-170">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7ab1e-171">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7ab1e-171">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7ab1e-172">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="7ab1e-172">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="7ab1e-173">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7ab1e-173">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7ab1e-174">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7ab1e-174">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7ab1e-175">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="7ab1e-175">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="7ab1e-176">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="7ab1e-176">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="7ab1e-177">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="7ab1e-177">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="7ab1e-178">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="7ab1e-178">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="7ab1e-179">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="7ab1e-179">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="7ab1e-180">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7ab1e-180">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
