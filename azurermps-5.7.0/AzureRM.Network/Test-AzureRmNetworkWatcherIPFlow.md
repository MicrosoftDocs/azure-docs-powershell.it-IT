---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/test-azurermnetworkwatcheripflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherIPFlow.md
ms.openlocfilehash: 577f883affc772c01343a57a533c5ae06eccf31c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687877"
---
# <span data-ttu-id="32459-101">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="32459-101">Test-AzureRmNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="32459-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="32459-102">SYNOPSIS</span></span>
<span data-ttu-id="32459-103">Restituisce un valore che indica se il pacchetto è consentito o negato per o da una determinata destinazione.</span><span class="sxs-lookup"><span data-stu-id="32459-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32459-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="32459-104">SYNTAX</span></span>

### <span data-ttu-id="32459-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="32459-105">SetByResource (Default)</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32459-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="32459-106">SetByName</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32459-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32459-107">DESCRIPTION</span></span>
<span data-ttu-id="32459-108">Il cmdlet Test-AzureRmNetworkWatcherIPFlow, per una risorsa VM specificata e un pacchetto con una direzione specificata con gli indirizzi IP locali e remoti e le porte, restituisce se il pacchetto è consentito o negato.</span><span class="sxs-lookup"><span data-stu-id="32459-108">The Test-AzureRmNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="32459-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="32459-109">EXAMPLES</span></span>

### <span data-ttu-id="32459-110">---Esempio 1: eseguire Test-AzureRmNetworkWatcherIPFlow---</span><span class="sxs-lookup"><span data-stu-id="32459-110">--- Example 1: Run Test-AzureRmNetworkWatcherIPFlow ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzureRmNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}

Test-AzureRmNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="32459-111">Ottieni l'osservatore di rete in West Central US per questo abbonamento, quindi ottiene la VM ed è associata alle interfacce di rete.</span><span class="sxs-lookup"><span data-stu-id="32459-111">Get's the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="32459-112">Quindi, per la prima interfaccia di rete, viene eseguito Test-AzureRmNetworkWatcherIPFlow usando il primo IP della prima interfaccia di rete per una connessione in uscita a un IP su Internet.</span><span class="sxs-lookup"><span data-stu-id="32459-112">Then for the first Network Interface, runs Test-AzureRmNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="32459-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="32459-113">PARAMETERS</span></span>

### <span data-ttu-id="32459-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="32459-114">-AsJob</span></span>
<span data-ttu-id="32459-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="32459-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="32459-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32459-116">-DefaultProfile</span></span>
<span data-ttu-id="32459-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="32459-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32459-118">-Direzione</span><span class="sxs-lookup"><span data-stu-id="32459-118">-Direction</span></span>
<span data-ttu-id="32459-119">Direzione.</span><span class="sxs-lookup"><span data-stu-id="32459-119">Direction.</span></span>

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

### <span data-ttu-id="32459-120">-IndirizzoIPLocale</span><span class="sxs-lookup"><span data-stu-id="32459-120">-LocalIPAddress</span></span>
<span data-ttu-id="32459-121">Indirizzo IP locale.</span><span class="sxs-lookup"><span data-stu-id="32459-121">Local IP Address.</span></span>

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

### <span data-ttu-id="32459-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="32459-122">-LocalPort</span></span>
<span data-ttu-id="32459-123">Porta locale.</span><span class="sxs-lookup"><span data-stu-id="32459-123">Local Port.</span></span>

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

### <span data-ttu-id="32459-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="32459-124">-NetworkWatcher</span></span>
<span data-ttu-id="32459-125">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="32459-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="32459-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="32459-126">-NetworkWatcherName</span></span>
<span data-ttu-id="32459-127">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="32459-127">The name of network watcher.</span></span>

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

### <span data-ttu-id="32459-128">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="32459-128">-Protocol</span></span>
<span data-ttu-id="32459-129">Protocollo.</span><span class="sxs-lookup"><span data-stu-id="32459-129">Protocol.</span></span>

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

### <span data-ttu-id="32459-130">-IndirizzoIPRemoto</span><span class="sxs-lookup"><span data-stu-id="32459-130">-RemoteIPAddress</span></span>
<span data-ttu-id="32459-131">Indirizzo IP remoto.</span><span class="sxs-lookup"><span data-stu-id="32459-131">Remote IP Address.</span></span>

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

### <span data-ttu-id="32459-132">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="32459-132">-RemotePort</span></span>
<span data-ttu-id="32459-133">Porta remota.</span><span class="sxs-lookup"><span data-stu-id="32459-133">Remote port.</span></span>

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

### <span data-ttu-id="32459-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32459-134">-ResourceGroupName</span></span>
<span data-ttu-id="32459-135">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="32459-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="32459-136">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="32459-136">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="32459-137">ID interfaccia di rete di destinazione.</span><span class="sxs-lookup"><span data-stu-id="32459-137">Target network interface Id.</span></span>

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

### <span data-ttu-id="32459-138">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="32459-138">-TargetVirtualMachineId</span></span>
<span data-ttu-id="32459-139">ID macchina virtuale di destinazione.</span><span class="sxs-lookup"><span data-stu-id="32459-139">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="32459-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32459-140">CommonParameters</span></span>
<span data-ttu-id="32459-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32459-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32459-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32459-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32459-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="32459-143">INPUTS</span></span>

### <span data-ttu-id="32459-144">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="32459-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="32459-145">System. String</span><span class="sxs-lookup"><span data-stu-id="32459-145">System.String</span></span>

## <span data-ttu-id="32459-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="32459-146">OUTPUTS</span></span>

### <span data-ttu-id="32459-147">Microsoft. Azure. Commands. Network. Models. PSIPFlowVerifyResult</span><span class="sxs-lookup"><span data-stu-id="32459-147">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="32459-148">Note</span><span class="sxs-lookup"><span data-stu-id="32459-148">NOTES</span></span>
<span data-ttu-id="32459-149">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher, Flow, IP</span><span class="sxs-lookup"><span data-stu-id="32459-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="32459-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="32459-150">RELATED LINKS</span></span>

[<span data-ttu-id="32459-151">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="32459-151">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="32459-152">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="32459-152">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="32459-153">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="32459-153">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="32459-154">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="32459-154">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="32459-155">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="32459-155">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="32459-156">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="32459-156">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="32459-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="32459-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="32459-158">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="32459-158">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="32459-159">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="32459-159">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="32459-160">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="32459-160">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="32459-161">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="32459-161">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="32459-162">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="32459-162">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)
