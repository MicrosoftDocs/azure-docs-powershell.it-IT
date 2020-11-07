---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 8e2e7a25b2c6e2c9eaa5e53234d7c1c9c3d0fa9f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860717"
---
# <span data-ttu-id="8a214-101">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8a214-101">Get-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="8a214-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8a214-102">SYNOPSIS</span></span>
<span data-ttu-id="8a214-103">Ottiene le informazioni e le proprietà e lo stato di una risorsa di acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="8a214-103">Gets information and properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="8a214-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8a214-104">SYNTAX</span></span>

### <span data-ttu-id="8a214-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8a214-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a214-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="8a214-106">SetByName</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a214-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8a214-107">DESCRIPTION</span></span>
<span data-ttu-id="8a214-108">Il Get-AzNetworkWatcherPacketCapture ottiene le proprietà e lo stato di una risorsa di acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="8a214-108">The Get-AzNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="8a214-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8a214-109">EXAMPLES</span></span>

### <span data-ttu-id="8a214-110">---Esempio 1: creare un'acquisizione di pacchetti con più filtri e recuperarne lo stato---</span><span class="sxs-lookup"><span data-stu-id="8a214-110">--- Example 1: Create a Packet Capture with multiple filters and retrieve its status ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="8a214-111">In questo esempio creiamo un'acquisizione di pacchetti denominata "PacketCaptureTest" con più filtri e un limite di tempo.</span><span class="sxs-lookup"><span data-stu-id="8a214-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="8a214-112">Una volta completata la sessione, verrà salvata nell'account di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="8a214-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="8a214-113">Chiamiamo quindi Get-AzNetworkWatcherPacketCapture per recuperare lo stato della sessione di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="8a214-113">We then call Get-AzNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> 

<span data-ttu-id="8a214-114">Nota: l'estensione Azure Network Watcher deve essere installata nella macchina virtuale di destinazione per creare acquisizioni di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="8a214-114">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="8a214-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8a214-115">PARAMETERS</span></span>

### <span data-ttu-id="8a214-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8a214-116">-AsJob</span></span>
<span data-ttu-id="8a214-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="8a214-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8a214-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a214-118">-DefaultProfile</span></span>
<span data-ttu-id="8a214-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8a214-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a214-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8a214-120">-NetworkWatcher</span></span>
<span data-ttu-id="8a214-121">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="8a214-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="8a214-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="8a214-122">-NetworkWatcherName</span></span>
<span data-ttu-id="8a214-123">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="8a214-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="8a214-124">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="8a214-124">-PacketCaptureName</span></span>
<span data-ttu-id="8a214-125">Nome del pacchetto Capture.</span><span class="sxs-lookup"><span data-stu-id="8a214-125">The packet capture name.</span></span>

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

### <span data-ttu-id="8a214-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a214-126">-ResourceGroupName</span></span>
<span data-ttu-id="8a214-127">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="8a214-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="8a214-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a214-128">CommonParameters</span></span>
<span data-ttu-id="8a214-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a214-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a214-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a214-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a214-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8a214-131">INPUTS</span></span>

### <span data-ttu-id="8a214-132">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8a214-132">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="8a214-133">System. String</span><span class="sxs-lookup"><span data-stu-id="8a214-133">System.String</span></span>

## <span data-ttu-id="8a214-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8a214-134">OUTPUTS</span></span>

### <span data-ttu-id="8a214-135">Microsoft. Azure. Commands. Network. Models. PSGetPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="8a214-135">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="8a214-136">Note</span><span class="sxs-lookup"><span data-stu-id="8a214-136">NOTES</span></span>
<span data-ttu-id="8a214-137">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher, Packet, Capture, Traffic</span><span class="sxs-lookup"><span data-stu-id="8a214-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="8a214-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8a214-138">RELATED LINKS</span></span>

[<span data-ttu-id="8a214-139">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8a214-139">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8a214-140">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="8a214-140">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="8a214-141">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8a214-141">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8a214-142">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8a214-142">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8a214-143">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8a214-143">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="8a214-144">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8a214-144">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="8a214-145">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8a214-145">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="8a214-146">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="8a214-146">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="8a214-147">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="8a214-147">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="8a214-148">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="8a214-148">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="8a214-149">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="8a214-149">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="8a214-150">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="8a214-150">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

