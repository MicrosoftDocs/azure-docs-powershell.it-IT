---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherNextHop.md
ms.openlocfilehash: d26f50768c561e05b4dc27ad829c063b73c5a336
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521583"
---
# <span data-ttu-id="099f0-101">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="099f0-101">Get-AzureRmNetworkWatcherNextHop</span></span>

## <span data-ttu-id="099f0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="099f0-102">SYNOPSIS</span></span>
<span data-ttu-id="099f0-103">Ottiene l'hop successivo da una VM.</span><span class="sxs-lookup"><span data-stu-id="099f0-103">Gets the next hop from a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="099f0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="099f0-104">SYNTAX</span></span>

### <span data-ttu-id="099f0-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="099f0-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="099f0-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="099f0-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="099f0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="099f0-107">DESCRIPTION</span></span>
<span data-ttu-id="099f0-108">Il cmdlet Get-AzureRmNetworkWatcherNextHop Ottiene l'hop successivo da una VM.</span><span class="sxs-lookup"><span data-stu-id="099f0-108">The Get-AzureRmNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="099f0-109">L'hop successivo consente di visualizzare il tipo di risorsa Azure, l'indirizzo IP associato della risorsa e la regola della tabella di routing responsabile della route.</span><span class="sxs-lookup"><span data-stu-id="099f0-109">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="099f0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="099f0-110">EXAMPLES</span></span>

### <span data-ttu-id="099f0-111">--Esempio 1: ottenere l'hop successivo quando si comunica con un IP Internet--</span><span class="sxs-lookup"><span data-stu-id="099f0-111">-- Example 1: Get the Next Hop when communicating with an Internet IP --</span></span>
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

<span data-ttu-id="099f0-112">Ottenere l'hop successivo per le comunicazioni in uscita dall'interfaccia di rete principale nel Vachine virtuale specificato a 204.79.197.200 (www.bing.com)</span><span class="sxs-lookup"><span data-stu-id="099f0-112">Get's the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Vachine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="099f0-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="099f0-113">PARAMETERS</span></span>

### <span data-ttu-id="099f0-114">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="099f0-114">-DestinationIPAddress</span></span>
<span data-ttu-id="099f0-115">Indirizzo IP di destinazione.</span><span class="sxs-lookup"><span data-stu-id="099f0-115">Destination IP address.</span></span>

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

### <span data-ttu-id="099f0-116">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="099f0-116">-NetworkWatcher</span></span>
<span data-ttu-id="099f0-117">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="099f0-117">The network watcher resource.</span></span>

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

### <span data-ttu-id="099f0-118">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="099f0-118">-NetworkWatcherName</span></span>
<span data-ttu-id="099f0-119">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="099f0-119">The name of network watcher.</span></span>

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

### <span data-ttu-id="099f0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="099f0-120">-ResourceGroupName</span></span>
<span data-ttu-id="099f0-121">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="099f0-121">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="099f0-122">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="099f0-122">-SourceIPAddress</span></span>
<span data-ttu-id="099f0-123">Indirizzo IP di origine.</span><span class="sxs-lookup"><span data-stu-id="099f0-123">Source IP address.</span></span>

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

### <span data-ttu-id="099f0-124">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="099f0-124">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="099f0-125">ID interfaccia di rete di destinazione.</span><span class="sxs-lookup"><span data-stu-id="099f0-125">Target network interface Id.</span></span>

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

### <span data-ttu-id="099f0-126">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="099f0-126">-TargetVirtualMachineId</span></span>
<span data-ttu-id="099f0-127">ID macchina virtuale di destinazione.</span><span class="sxs-lookup"><span data-stu-id="099f0-127">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="099f0-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="099f0-128">-DefaultProfile</span></span>
<span data-ttu-id="099f0-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="099f0-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="099f0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="099f0-130">CommonParameters</span></span>
<span data-ttu-id="099f0-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="099f0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="099f0-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="099f0-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="099f0-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="099f0-133">INPUTS</span></span>

### <span data-ttu-id="099f0-134">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="099f0-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="099f0-135">System. String</span><span class="sxs-lookup"><span data-stu-id="099f0-135">System.String</span></span>

## <span data-ttu-id="099f0-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="099f0-136">OUTPUTS</span></span>

### <span data-ttu-id="099f0-137">Microsoft. Azure. Commands. Network. Models. PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="099f0-137">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="099f0-138">Note</span><span class="sxs-lookup"><span data-stu-id="099f0-138">NOTES</span></span>
<span data-ttu-id="099f0-139">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher, Next, hop</span><span class="sxs-lookup"><span data-stu-id="099f0-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="099f0-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="099f0-140">RELATED LINKS</span></span>

[<span data-ttu-id="099f0-141">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="099f0-141">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="099f0-142">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="099f0-142">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="099f0-143">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="099f0-143">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="099f0-144">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="099f0-144">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="099f0-145">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="099f0-145">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="099f0-146">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="099f0-146">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="099f0-147">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="099f0-147">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="099f0-148">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="099f0-148">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="099f0-149">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="099f0-149">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="099f0-150">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="099f0-150">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="099f0-151">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="099f0-151">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="099f0-152">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="099f0-152">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

