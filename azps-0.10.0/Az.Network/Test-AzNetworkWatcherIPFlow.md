---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-aznetworkwatcheripflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
ms.openlocfilehash: 307bb2c954526b744f31763f0d3a09d0163c8057
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862662"
---
# <span data-ttu-id="302d2-101">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="302d2-101">Test-AzNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="302d2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="302d2-102">SYNOPSIS</span></span>
<span data-ttu-id="302d2-103">Restituisce un valore che indica se il pacchetto è consentito o negato per o da una determinata destinazione.</span><span class="sxs-lookup"><span data-stu-id="302d2-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

## <span data-ttu-id="302d2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="302d2-104">SYNTAX</span></span>

### <span data-ttu-id="302d2-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="302d2-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="302d2-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="302d2-106">SetByName</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="302d2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="302d2-107">DESCRIPTION</span></span>
<span data-ttu-id="302d2-108">Il cmdlet Test-AzNetworkWatcherIPFlow, per una risorsa VM specificata e un pacchetto con una direzione specificata con gli indirizzi IP locali e remoti e le porte, restituisce se il pacchetto è consentito o negato.</span><span class="sxs-lookup"><span data-stu-id="302d2-108">The Test-AzNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="302d2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="302d2-109">EXAMPLES</span></span>

### <span data-ttu-id="302d2-110">---Esempio 1: eseguire Test-AzNetworkWatcherIPFlow---</span><span class="sxs-lookup"><span data-stu-id="302d2-110">--- Example 1: Run Test-AzNetworkWatcherIPFlow ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}

Test-AzNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="302d2-111">Ottieni l'osservatore di rete in West Central US per questo abbonamento, quindi ottiene la VM ed è associata alle interfacce di rete.</span><span class="sxs-lookup"><span data-stu-id="302d2-111">Get's the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="302d2-112">Quindi, per la prima interfaccia di rete, viene eseguito Test-AzNetworkWatcherIPFlow usando il primo IP della prima interfaccia di rete per una connessione in uscita a un IP su Internet.</span><span class="sxs-lookup"><span data-stu-id="302d2-112">Then for the first Network Interface, runs Test-AzNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="302d2-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="302d2-113">PARAMETERS</span></span>

### <span data-ttu-id="302d2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="302d2-114">-AsJob</span></span>
<span data-ttu-id="302d2-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="302d2-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="302d2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="302d2-116">-DefaultProfile</span></span>
<span data-ttu-id="302d2-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="302d2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="302d2-118">-Direzione</span><span class="sxs-lookup"><span data-stu-id="302d2-118">-Direction</span></span>
<span data-ttu-id="302d2-119">Direzione.</span><span class="sxs-lookup"><span data-stu-id="302d2-119">Direction.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Inbound, Outbound

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="302d2-120">-IndirizzoIPLocale</span><span class="sxs-lookup"><span data-stu-id="302d2-120">-LocalIPAddress</span></span>
<span data-ttu-id="302d2-121">Indirizzo IP locale.</span><span class="sxs-lookup"><span data-stu-id="302d2-121">Local IP Address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="302d2-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="302d2-122">-LocalPort</span></span>
<span data-ttu-id="302d2-123">Porta locale.</span><span class="sxs-lookup"><span data-stu-id="302d2-123">Local Port.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="302d2-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="302d2-124">-NetworkWatcher</span></span>
<span data-ttu-id="302d2-125">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="302d2-125">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="302d2-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="302d2-126">-NetworkWatcherName</span></span>
<span data-ttu-id="302d2-127">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="302d2-127">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="302d2-128">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="302d2-128">-Protocol</span></span>
<span data-ttu-id="302d2-129">Protocollo.</span><span class="sxs-lookup"><span data-stu-id="302d2-129">Protocol.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: TCP, UDP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="302d2-130">-IndirizzoIPRemoto</span><span class="sxs-lookup"><span data-stu-id="302d2-130">-RemoteIPAddress</span></span>
<span data-ttu-id="302d2-131">Indirizzo IP remoto.</span><span class="sxs-lookup"><span data-stu-id="302d2-131">Remote IP Address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="302d2-132">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="302d2-132">-RemotePort</span></span>
<span data-ttu-id="302d2-133">Porta remota.</span><span class="sxs-lookup"><span data-stu-id="302d2-133">Remote port.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="302d2-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="302d2-134">-ResourceGroupName</span></span>
<span data-ttu-id="302d2-135">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="302d2-135">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="302d2-136">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="302d2-136">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="302d2-137">ID interfaccia di rete di destinazione.</span><span class="sxs-lookup"><span data-stu-id="302d2-137">Target network interface Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="302d2-138">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="302d2-138">-TargetVirtualMachineId</span></span>
<span data-ttu-id="302d2-139">ID macchina virtuale di destinazione.</span><span class="sxs-lookup"><span data-stu-id="302d2-139">The target virtual machine ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="302d2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="302d2-140">CommonParameters</span></span>
<span data-ttu-id="302d2-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="302d2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="302d2-142">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="302d2-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="302d2-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="302d2-143">INPUTS</span></span>

### <span data-ttu-id="302d2-144">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="302d2-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="302d2-145">System. String</span><span class="sxs-lookup"><span data-stu-id="302d2-145">System.String</span></span>

## <span data-ttu-id="302d2-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="302d2-146">OUTPUTS</span></span>

### <span data-ttu-id="302d2-147">Microsoft. Azure. Commands. Network. Models. PSIPFlowVerifyResult</span><span class="sxs-lookup"><span data-stu-id="302d2-147">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="302d2-148">Note</span><span class="sxs-lookup"><span data-stu-id="302d2-148">NOTES</span></span>
<span data-ttu-id="302d2-149">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher, Flow, IP</span><span class="sxs-lookup"><span data-stu-id="302d2-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="302d2-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="302d2-150">RELATED LINKS</span></span>

[<span data-ttu-id="302d2-151">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="302d2-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="302d2-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="302d2-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="302d2-153">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="302d2-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="302d2-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="302d2-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="302d2-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="302d2-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="302d2-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="302d2-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="302d2-157">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="302d2-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="302d2-158">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="302d2-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="302d2-159">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="302d2-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="302d2-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="302d2-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="302d2-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="302d2-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="302d2-162">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="302d2-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)
