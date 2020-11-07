---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 912c2a424cda533dd5d576ab6744476b689d2ae1
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "93688665"
---
# <span data-ttu-id="dc1ad-101">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dc1ad-101">Get-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="dc1ad-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dc1ad-102">SYNOPSIS</span></span>
<span data-ttu-id="dc1ad-103">Ottiene le informazioni e le proprietà e lo stato di una risorsa di acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="dc1ad-103">Gets information and properties and status of a packet capture resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc1ad-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dc1ad-104">SYNTAX</span></span>

### <span data-ttu-id="dc1ad-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dc1ad-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc1ad-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="dc1ad-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc1ad-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dc1ad-107">DESCRIPTION</span></span>
<span data-ttu-id="dc1ad-108">Il Get-AzureRmNetworkWatcherPacketCapture ottiene le proprietà e lo stato di una risorsa di acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="dc1ad-108">The Get-AzureRmNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="dc1ad-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dc1ad-109">EXAMPLES</span></span>

### <span data-ttu-id="dc1ad-110">---Esempio 1: creare un'acquisizione di pacchetti con più filtri e recuperarne lo stato---</span><span class="sxs-lookup"><span data-stu-id="dc1ad-110">--- Example 1: Create a Packet Capture with multiple filters and retrieve its status ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="dc1ad-111">In questo esempio creiamo un'acquisizione di pacchetti denominata "PacketCaptureTest" con più filtri e un limite di tempo.</span><span class="sxs-lookup"><span data-stu-id="dc1ad-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="dc1ad-112">Una volta completata la sessione, verrà salvata nell'account di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="dc1ad-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="dc1ad-113">Chiamiamo quindi Get-AzureRmNetworkWatcherPacketCapture per recuperare lo stato della sessione di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="dc1ad-113">We then call Get-AzureRmNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> 

<span data-ttu-id="dc1ad-114">Nota: l'estensione Azure Network Watcher deve essere installata nella macchina virtuale di destinazione per creare acquisizioni di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="dc1ad-114">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="dc1ad-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dc1ad-115">PARAMETERS</span></span>

### <span data-ttu-id="dc1ad-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dc1ad-116">-AsJob</span></span>
<span data-ttu-id="dc1ad-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="dc1ad-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dc1ad-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc1ad-118">-DefaultProfile</span></span>
<span data-ttu-id="dc1ad-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dc1ad-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc1ad-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dc1ad-120">-NetworkWatcher</span></span>
<span data-ttu-id="dc1ad-121">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="dc1ad-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="dc1ad-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="dc1ad-122">-NetworkWatcherName</span></span>
<span data-ttu-id="dc1ad-123">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="dc1ad-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="dc1ad-124">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="dc1ad-124">-PacketCaptureName</span></span>
<span data-ttu-id="dc1ad-125">Nome del pacchetto Capture.</span><span class="sxs-lookup"><span data-stu-id="dc1ad-125">The packet capture name.</span></span>

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

### <span data-ttu-id="dc1ad-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc1ad-126">-ResourceGroupName</span></span>
<span data-ttu-id="dc1ad-127">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="dc1ad-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="dc1ad-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc1ad-128">CommonParameters</span></span>
<span data-ttu-id="dc1ad-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc1ad-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc1ad-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc1ad-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc1ad-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dc1ad-131">INPUTS</span></span>

### <span data-ttu-id="dc1ad-132">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dc1ad-132">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="dc1ad-133">System. String</span><span class="sxs-lookup"><span data-stu-id="dc1ad-133">System.String</span></span>

## <span data-ttu-id="dc1ad-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dc1ad-134">OUTPUTS</span></span>

### <span data-ttu-id="dc1ad-135">Microsoft. Azure. Commands. Network. Models. PSGetPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="dc1ad-135">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="dc1ad-136">Note</span><span class="sxs-lookup"><span data-stu-id="dc1ad-136">NOTES</span></span>
<span data-ttu-id="dc1ad-137">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher, Packet, Capture, Traffic</span><span class="sxs-lookup"><span data-stu-id="dc1ad-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="dc1ad-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dc1ad-138">RELATED LINKS</span></span>

[<span data-ttu-id="dc1ad-139">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dc1ad-139">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dc1ad-140">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="dc1ad-140">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="dc1ad-141">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dc1ad-141">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dc1ad-142">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dc1ad-142">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dc1ad-143">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dc1ad-143">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="dc1ad-144">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dc1ad-144">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="dc1ad-145">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dc1ad-145">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="dc1ad-146">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="dc1ad-146">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="dc1ad-147">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="dc1ad-147">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="dc1ad-148">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="dc1ad-148">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="dc1ad-149">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="dc1ad-149">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="dc1ad-150">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="dc1ad-150">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

