---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchernexthop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
ms.openlocfilehash: 02e24fd35fbe2e5aec5fc8b6ed73d3608d07c5b2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860721"
---
# <span data-ttu-id="44665-101">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="44665-101">Get-AzNetworkWatcherNextHop</span></span>

## <span data-ttu-id="44665-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="44665-102">SYNOPSIS</span></span>
<span data-ttu-id="44665-103">Ottiene l'hop successivo da una VM.</span><span class="sxs-lookup"><span data-stu-id="44665-103">Gets the next hop from a VM.</span></span>

## <span data-ttu-id="44665-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="44665-104">SYNTAX</span></span>

### <span data-ttu-id="44665-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="44665-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44665-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="44665-106">SetByName</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44665-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="44665-107">DESCRIPTION</span></span>
<span data-ttu-id="44665-108">Il cmdlet Get-AzNetworkWatcherNextHop Ottiene l'hop successivo da una VM.</span><span class="sxs-lookup"><span data-stu-id="44665-108">The Get-AzNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="44665-109">L'hop successivo consente di visualizzare il tipo di risorsa Azure, l'indirizzo IP associato della risorsa e la regola della tabella di routing responsabile della route.</span><span class="sxs-lookup"><span data-stu-id="44665-109">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="44665-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="44665-110">EXAMPLES</span></span>

### <span data-ttu-id="44665-111">--Esempio 1: ottenere l'hop successivo quando si comunica con un IP Internet--</span><span class="sxs-lookup"><span data-stu-id="44665-111">-- Example 1: Get the Next Hop when communicating with an Internet IP --</span></span>
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

<span data-ttu-id="44665-112">Ottenere l'hop successivo per le comunicazioni in uscita dall'interfaccia di rete principale nel Vachine virtuale specificato a 204.79.197.200 (www.bing.com)</span><span class="sxs-lookup"><span data-stu-id="44665-112">Get's the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Vachine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="44665-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="44665-113">PARAMETERS</span></span>

### <span data-ttu-id="44665-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="44665-114">-AsJob</span></span>
<span data-ttu-id="44665-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="44665-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="44665-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44665-116">-DefaultProfile</span></span>
<span data-ttu-id="44665-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="44665-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44665-118">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="44665-118">-DestinationIPAddress</span></span>
<span data-ttu-id="44665-119">Indirizzo IP di destinazione.</span><span class="sxs-lookup"><span data-stu-id="44665-119">Destination IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44665-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="44665-120">-NetworkWatcher</span></span>
<span data-ttu-id="44665-121">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="44665-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="44665-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="44665-122">-NetworkWatcherName</span></span>
<span data-ttu-id="44665-123">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="44665-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="44665-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44665-124">-ResourceGroupName</span></span>
<span data-ttu-id="44665-125">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="44665-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="44665-126">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="44665-126">-SourceIPAddress</span></span>
<span data-ttu-id="44665-127">Indirizzo IP di origine.</span><span class="sxs-lookup"><span data-stu-id="44665-127">Source IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44665-128">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="44665-128">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="44665-129">ID interfaccia di rete di destinazione.</span><span class="sxs-lookup"><span data-stu-id="44665-129">Target network interface Id.</span></span>

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

### <span data-ttu-id="44665-130">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="44665-130">-TargetVirtualMachineId</span></span>
<span data-ttu-id="44665-131">ID macchina virtuale di destinazione.</span><span class="sxs-lookup"><span data-stu-id="44665-131">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="44665-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44665-132">CommonParameters</span></span>
<span data-ttu-id="44665-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44665-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44665-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44665-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44665-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="44665-135">INPUTS</span></span>

### <span data-ttu-id="44665-136">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="44665-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="44665-137">System. String</span><span class="sxs-lookup"><span data-stu-id="44665-137">System.String</span></span>

## <span data-ttu-id="44665-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="44665-138">OUTPUTS</span></span>

### <span data-ttu-id="44665-139">Microsoft. Azure. Commands. Network. Models. PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="44665-139">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="44665-140">Note</span><span class="sxs-lookup"><span data-stu-id="44665-140">NOTES</span></span>
<span data-ttu-id="44665-141">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher, Next, hop</span><span class="sxs-lookup"><span data-stu-id="44665-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="44665-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="44665-142">RELATED LINKS</span></span>

[<span data-ttu-id="44665-143">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="44665-143">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="44665-144">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="44665-144">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="44665-145">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="44665-145">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="44665-146">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="44665-146">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="44665-147">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="44665-147">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="44665-148">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="44665-148">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="44665-149">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="44665-149">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="44665-150">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="44665-150">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="44665-151">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="44665-151">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="44665-152">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="44665-152">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="44665-153">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="44665-153">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="44665-154">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="44665-154">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

