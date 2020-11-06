---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchernexthop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherNextHop.md
ms.openlocfilehash: 641678db33e8e7436bda103f95863aefbf31eb96
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509820"
---
# <span data-ttu-id="fbfda-101">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="fbfda-101">Get-AzureRmNetworkWatcherNextHop</span></span>

## <span data-ttu-id="fbfda-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fbfda-102">SYNOPSIS</span></span>
<span data-ttu-id="fbfda-103">Ottiene l'hop successivo da una VM.</span><span class="sxs-lookup"><span data-stu-id="fbfda-103">Gets the next hop from a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fbfda-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fbfda-104">SYNTAX</span></span>

### <span data-ttu-id="fbfda-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fbfda-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fbfda-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="fbfda-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbfda-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fbfda-107">DESCRIPTION</span></span>
<span data-ttu-id="fbfda-108">Il cmdlet Get-AzureRmNetworkWatcherNextHop Ottiene l'hop successivo da una VM.</span><span class="sxs-lookup"><span data-stu-id="fbfda-108">The Get-AzureRmNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="fbfda-109">L'hop successivo consente di visualizzare il tipo di risorsa Azure, l'indirizzo IP associato della risorsa e la regola della tabella di routing responsabile della route.</span><span class="sxs-lookup"><span data-stu-id="fbfda-109">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="fbfda-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fbfda-110">EXAMPLES</span></span>

### <span data-ttu-id="fbfda-111">--Esempio 1: ottenere l'hop successivo quando si comunica con un IP Internet--</span><span class="sxs-lookup"><span data-stu-id="fbfda-111">-- Example 1: Get the Next Hop when communicating with an Internet IP --</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName ContosoResourceGroup -Name VM0
$Nics = Get-AzureRmNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}
Get-AzureRmNetworkWatcherNextHop -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -SourceIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress  -DestinationIPAddress 204.79.197.200


NextHopIpAddress NextHopType RouteTableId
---------------- ----------- ------------
                 Internet    System Route
```

<span data-ttu-id="fbfda-112">Ottenere l'hop successivo per le comunicazioni in uscita dall'interfaccia di rete principale nel Vachine virtuale specificato a 204.79.197.200 (www.bing.com)</span><span class="sxs-lookup"><span data-stu-id="fbfda-112">Get's the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Vachine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="fbfda-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fbfda-113">PARAMETERS</span></span>

### <span data-ttu-id="fbfda-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fbfda-114">-AsJob</span></span>
<span data-ttu-id="fbfda-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="fbfda-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fbfda-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbfda-116">-DefaultProfile</span></span>
<span data-ttu-id="fbfda-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fbfda-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fbfda-118">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="fbfda-118">-DestinationIPAddress</span></span>
<span data-ttu-id="fbfda-119">Indirizzo IP di destinazione.</span><span class="sxs-lookup"><span data-stu-id="fbfda-119">Destination IP address.</span></span>

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

### <span data-ttu-id="fbfda-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fbfda-120">-NetworkWatcher</span></span>
<span data-ttu-id="fbfda-121">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="fbfda-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="fbfda-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="fbfda-122">-NetworkWatcherName</span></span>
<span data-ttu-id="fbfda-123">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="fbfda-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="fbfda-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbfda-124">-ResourceGroupName</span></span>
<span data-ttu-id="fbfda-125">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="fbfda-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="fbfda-126">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="fbfda-126">-SourceIPAddress</span></span>
<span data-ttu-id="fbfda-127">Indirizzo IP di origine.</span><span class="sxs-lookup"><span data-stu-id="fbfda-127">Source IP address.</span></span>

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

### <span data-ttu-id="fbfda-128">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="fbfda-128">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="fbfda-129">ID interfaccia di rete di destinazione.</span><span class="sxs-lookup"><span data-stu-id="fbfda-129">Target network interface Id.</span></span>

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

### <span data-ttu-id="fbfda-130">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="fbfda-130">-TargetVirtualMachineId</span></span>
<span data-ttu-id="fbfda-131">ID macchina virtuale di destinazione.</span><span class="sxs-lookup"><span data-stu-id="fbfda-131">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="fbfda-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbfda-132">CommonParameters</span></span>
<span data-ttu-id="fbfda-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbfda-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbfda-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbfda-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbfda-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fbfda-135">INPUTS</span></span>

### <span data-ttu-id="fbfda-136">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fbfda-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="fbfda-137">System. String</span><span class="sxs-lookup"><span data-stu-id="fbfda-137">System.String</span></span>

## <span data-ttu-id="fbfda-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fbfda-138">OUTPUTS</span></span>

### <span data-ttu-id="fbfda-139">Microsoft. Azure. Commands. Network. Models. PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="fbfda-139">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="fbfda-140">Note</span><span class="sxs-lookup"><span data-stu-id="fbfda-140">NOTES</span></span>
<span data-ttu-id="fbfda-141">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher, Next, hop</span><span class="sxs-lookup"><span data-stu-id="fbfda-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="fbfda-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fbfda-142">RELATED LINKS</span></span>

[<span data-ttu-id="fbfda-143">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fbfda-143">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="fbfda-144">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fbfda-144">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="fbfda-145">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fbfda-145">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="fbfda-146">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="fbfda-146">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="fbfda-147">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="fbfda-147">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="fbfda-148">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="fbfda-148">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="fbfda-149">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="fbfda-149">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="fbfda-150">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fbfda-150">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fbfda-151">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="fbfda-151">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="fbfda-152">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fbfda-152">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fbfda-153">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fbfda-153">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fbfda-154">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fbfda-154">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

