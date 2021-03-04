---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/test-aznetworkwatcheripflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
ms.openlocfilehash: 8be10fd630bbc9d4e1952150728d144b5f552fe6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951726"
---
# <span data-ttu-id="062f4-101">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="062f4-101">Test-AzNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="062f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="062f4-102">SYNOPSIS</span></span>
<span data-ttu-id="062f4-103">Restituisce se il pacchetto è consentito o negato a o da una destinazione specifica.</span><span class="sxs-lookup"><span data-stu-id="062f4-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

## <span data-ttu-id="062f4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="062f4-104">SYNTAX</span></span>

### <span data-ttu-id="062f4-105">SetByResource (Default)</span><span class="sxs-lookup"><span data-stu-id="062f4-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="062f4-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="062f4-106">SetByName</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="062f4-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="062f4-107">SetByLocation</span></span>
```
Test-AzNetworkWatcherIPFlow -Location <String> -TargetVirtualMachineId <String> -Direction <String>
 -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="062f4-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="062f4-108">DESCRIPTION</span></span>
<span data-ttu-id="062f4-109">Il cmdlet Test-AzNetworkWatcherIPFlow, per una risorsa VM specificata e un pacchetto con la direzione specificata usando porte e indirizzi IP locali e remoti, restituisce se il pacchetto è consentito o negato.</span><span class="sxs-lookup"><span data-stu-id="062f4-109">The Test-AzNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="062f4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="062f4-110">EXAMPLES</span></span>

### <span data-ttu-id="062f4-111">Esempio 1: Eseguire Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="062f4-111">Example 1: Run Test-AzNetworkWatcherIPFlow</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzNetworkInterface | Where-Object { $vm.NetworkProfile.NetworkInterfaces.Id -contains $_.Id }

Test-AzNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="062f4-112">Ottiene Network Watcher negli Stati Uniti centrali occidentali per questo abbonamento, quindi ottiene la macchina virtuale e le interfacce di rete associate.</span><span class="sxs-lookup"><span data-stu-id="062f4-112">Gets the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="062f4-113">Quindi, per la prima interfaccia di rete, viene Test-AzNetworkWatcherIPFlow il primo IP dalla prima interfaccia di rete per una connessione in uscita a un indirizzo IP su Internet.</span><span class="sxs-lookup"><span data-stu-id="062f4-113">Then for the first Network Interface, runs Test-AzNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="062f4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="062f4-114">PARAMETERS</span></span>

### <span data-ttu-id="062f4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="062f4-115">-AsJob</span></span>
<span data-ttu-id="062f4-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="062f4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="062f4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="062f4-117">-DefaultProfile</span></span>
<span data-ttu-id="062f4-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="062f4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="062f4-119">-Direction</span><span class="sxs-lookup"><span data-stu-id="062f4-119">-Direction</span></span>
<span data-ttu-id="062f4-120">Direzione.</span><span class="sxs-lookup"><span data-stu-id="062f4-120">Direction.</span></span>

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

### <span data-ttu-id="062f4-121">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="062f4-121">-LocalIPAddress</span></span>
<span data-ttu-id="062f4-122">Indirizzo IP locale.</span><span class="sxs-lookup"><span data-stu-id="062f4-122">Local IP Address.</span></span>

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

### <span data-ttu-id="062f4-123">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="062f4-123">-LocalPort</span></span>
<span data-ttu-id="062f4-124">Porta locale.</span><span class="sxs-lookup"><span data-stu-id="062f4-124">Local Port.</span></span>

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

### <span data-ttu-id="062f4-125">-Location</span><span class="sxs-lookup"><span data-stu-id="062f4-125">-Location</span></span>
<span data-ttu-id="062f4-126">Posizione del network watcher.</span><span class="sxs-lookup"><span data-stu-id="062f4-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="062f4-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="062f4-127">-NetworkWatcher</span></span>
<span data-ttu-id="062f4-128">Risorsa Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="062f4-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="062f4-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="062f4-129">-NetworkWatcherName</span></span>
<span data-ttu-id="062f4-130">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="062f4-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="062f4-131">-Protocol</span><span class="sxs-lookup"><span data-stu-id="062f4-131">-Protocol</span></span>
<span data-ttu-id="062f4-132">Protocollo.</span><span class="sxs-lookup"><span data-stu-id="062f4-132">Protocol.</span></span>

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

### <span data-ttu-id="062f4-133">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="062f4-133">-RemoteIPAddress</span></span>
<span data-ttu-id="062f4-134">Indirizzo IP remoto.</span><span class="sxs-lookup"><span data-stu-id="062f4-134">Remote IP Address.</span></span>

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

### <span data-ttu-id="062f4-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="062f4-135">-RemotePort</span></span>
<span data-ttu-id="062f4-136">Porta remota.</span><span class="sxs-lookup"><span data-stu-id="062f4-136">Remote port.</span></span>

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

### <span data-ttu-id="062f4-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="062f4-137">-ResourceGroupName</span></span>
<span data-ttu-id="062f4-138">Nome del gruppo di risorse Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="062f4-138">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="062f4-139">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="062f4-139">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="062f4-140">ID interfaccia di rete di destinazione.</span><span class="sxs-lookup"><span data-stu-id="062f4-140">Target network interface Id.</span></span>

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

### <span data-ttu-id="062f4-141">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="062f4-141">-TargetVirtualMachineId</span></span>
<span data-ttu-id="062f4-142">ID della macchina virtuale di destinazione.</span><span class="sxs-lookup"><span data-stu-id="062f4-142">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="062f4-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="062f4-143">CommonParameters</span></span>
<span data-ttu-id="062f4-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="062f4-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="062f4-145">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="062f4-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="062f4-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="062f4-146">INPUTS</span></span>

### <span data-ttu-id="062f4-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="062f4-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="062f4-148">System.String</span><span class="sxs-lookup"><span data-stu-id="062f4-148">System.String</span></span>

## <span data-ttu-id="062f4-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="062f4-149">OUTPUTS</span></span>

### <span data-ttu-id="062f4-150">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span><span class="sxs-lookup"><span data-stu-id="062f4-150">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="062f4-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="062f4-151">NOTES</span></span>
<span data-ttu-id="062f4-152">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, rete, rete, network watcher, flusso, ip</span><span class="sxs-lookup"><span data-stu-id="062f4-152">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="062f4-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="062f4-153">RELATED LINKS</span></span>

[<span data-ttu-id="062f4-154">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="062f4-154">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="062f4-155">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="062f4-155">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="062f4-156">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="062f4-156">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="062f4-157">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="062f4-157">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="062f4-158">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="062f4-158">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="062f4-159">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="062f4-159">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="062f4-160">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="062f4-160">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="062f4-161">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="062f4-161">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="062f4-162">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="062f4-162">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="062f4-163">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="062f4-163">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="062f4-164">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="062f4-164">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="062f4-165">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="062f4-165">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="062f4-166">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="062f4-166">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="062f4-167">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="062f4-167">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="062f4-168">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="062f4-168">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="062f4-169">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="062f4-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="062f4-170">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="062f4-170">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="062f4-171">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="062f4-171">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="062f4-172">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="062f4-172">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="062f4-173">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="062f4-173">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="062f4-174">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="062f4-174">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="062f4-175">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="062f4-175">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="062f4-176">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="062f4-176">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="062f4-177">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="062f4-177">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="062f4-178">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="062f4-178">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="062f4-179">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="062f4-179">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="062f4-180">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="062f4-180">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
