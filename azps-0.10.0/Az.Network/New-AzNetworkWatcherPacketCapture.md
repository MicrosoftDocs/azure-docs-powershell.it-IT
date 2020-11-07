---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 6844db506ee8a55c7d0c16f54946e35349059ae4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860438"
---
# <span data-ttu-id="5496b-101">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5496b-101">New-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="5496b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5496b-102">SYNOPSIS</span></span>
<span data-ttu-id="5496b-103">Crea una nuova risorsa di acquisizione di pacchetti e avvia una sessione di acquisizione di pacchetti in una VM.</span><span class="sxs-lookup"><span data-stu-id="5496b-103">Creates a new packet capture resource and starts a packet capture session on a VM.</span></span>

## <span data-ttu-id="5496b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5496b-104">SYNTAX</span></span>

### <span data-ttu-id="5496b-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5496b-105">SetByResource (Default)</span></span>
```
New-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5496b-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="5496b-106">SetByName</span></span>
```
New-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> -TargetVirtualMachineId <String> [-StorageAccountId <String>]
 [-StoragePath <String>] [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>]
 [-TotalBytesPerSession <Int32>] [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5496b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5496b-107">DESCRIPTION</span></span>
<span data-ttu-id="5496b-108">Il cmdlet New-AzNetworkWatcherPacketCapture crea una nuova risorsa di acquisizione di pacchetti e avvia una sessione di acquisizione di pacchetti in una VM.</span><span class="sxs-lookup"><span data-stu-id="5496b-108">The New-AzNetworkWatcherPacketCapture cmdlet creates a new packet capture resource and starts a packet capture session on a VM.</span></span>
<span data-ttu-id="5496b-109">La lunghezza delle sessioni di acquisizione di pacchetti può essere configurata tramite un vincolo temporale o un vincolo di dimensione.</span><span class="sxs-lookup"><span data-stu-id="5496b-109">The length of the Packet Capture sessions can be configured via a time constraint or a size constraint.</span></span> <span data-ttu-id="5496b-110">La quantità di dati acquisiti per ogni pacchetto può anche essere configurata.</span><span class="sxs-lookup"><span data-stu-id="5496b-110">The amount of data captured for each packet can also be configured.</span></span>
<span data-ttu-id="5496b-111">I filtri possono essere applicati a una determinata sessione di acquisizione di pacchetti, che consente di personalizzare il tipo di pacchetti acquisiti.</span><span class="sxs-lookup"><span data-stu-id="5496b-111">Filters can be applied to a given packet capture session, allowing you to customize the type of packets captured.</span></span> <span data-ttu-id="5496b-112">I filtri possono limitare i pacchetti in indirizzi IP locali e remoti & intervalli di indirizzi, porte locali e remote & intervalli di porte e il protocollo del livello di sessione da acquisire.</span><span class="sxs-lookup"><span data-stu-id="5496b-112">Filters can restrict packets on local and remote IP addresses & address ranges, local and remote ports & port ranges, and the session level protocol to be captured.</span></span> <span data-ttu-id="5496b-113">I filtri sono componibili e possono essere applicati più filtri per garantirti la granularità dell'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="5496b-113">Filters are composable, and multiple filters can be applied to provide you with granularity of capture.</span></span>

## <span data-ttu-id="5496b-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5496b-114">EXAMPLES</span></span>

### <span data-ttu-id="5496b-115">---Esempio 1: creare un'acquisizione di pacchetti con più filtri---</span><span class="sxs-lookup"><span data-stu-id="5496b-115">--- Example 1: Create a Packet Capture with multiple filters ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filter $filter1, $filter2
```

<span data-ttu-id="5496b-116">In questo esempio creiamo un'acquisizione di pacchetti denominata "PacketCaptureTest" con più filtri e un limite di tempo.</span><span class="sxs-lookup"><span data-stu-id="5496b-116">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="5496b-117">Una volta completata la sessione, verrà salvata nell'account di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="5496b-117">Once the session is complete, it will be saved to the specified storage account.</span></span> 

<span data-ttu-id="5496b-118">Nota: l'estensione Azure Network Watcher deve essere installata nella macchina virtuale di destinazione per creare acquisizioni di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="5496b-118">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="5496b-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5496b-119">PARAMETERS</span></span>

### <span data-ttu-id="5496b-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5496b-120">-AsJob</span></span>
<span data-ttu-id="5496b-121">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="5496b-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5496b-122">-BytesToCapturePerPacket</span><span class="sxs-lookup"><span data-stu-id="5496b-122">-BytesToCapturePerPacket</span></span>
<span data-ttu-id="5496b-123">Byte da acquisire per pacchetto.</span><span class="sxs-lookup"><span data-stu-id="5496b-123">Bytes to capture per packet.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5496b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5496b-124">-DefaultProfile</span></span>
<span data-ttu-id="5496b-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5496b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5496b-126">-Filtro</span><span class="sxs-lookup"><span data-stu-id="5496b-126">-Filter</span></span>
<span data-ttu-id="5496b-127">Filtri per la sessione di acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="5496b-127">Filters for packet capture session.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5496b-128">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="5496b-128">-LocalFilePath</span></span>
<span data-ttu-id="5496b-129">Percorso file locale.</span><span class="sxs-lookup"><span data-stu-id="5496b-129">Local file path.</span></span>

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

### <span data-ttu-id="5496b-130">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5496b-130">-NetworkWatcher</span></span>
<span data-ttu-id="5496b-131">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="5496b-131">The network watcher resource.</span></span>

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

### <span data-ttu-id="5496b-132">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="5496b-132">-NetworkWatcherName</span></span>
<span data-ttu-id="5496b-133">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="5496b-133">The name of network watcher.</span></span>

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

### <span data-ttu-id="5496b-134">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="5496b-134">-PacketCaptureName</span></span>
<span data-ttu-id="5496b-135">Nome del pacchetto Capture.</span><span class="sxs-lookup"><span data-stu-id="5496b-135">The packet capture name.</span></span>

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

### <span data-ttu-id="5496b-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5496b-136">-ResourceGroupName</span></span>
<span data-ttu-id="5496b-137">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="5496b-137">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="5496b-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="5496b-138">-StorageAccountId</span></span>
<span data-ttu-id="5496b-139">ID account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="5496b-139">Storage account Id.</span></span>

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

### <span data-ttu-id="5496b-140">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="5496b-140">-StoragePath</span></span>
<span data-ttu-id="5496b-141">Percorso di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="5496b-141">Storage path.</span></span>

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

### <span data-ttu-id="5496b-142">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="5496b-142">-TargetVirtualMachineId</span></span>
<span data-ttu-id="5496b-143">ID macchina virtuale di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5496b-143">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="5496b-144">-TimeLimitInSeconds</span><span class="sxs-lookup"><span data-stu-id="5496b-144">-TimeLimitInSeconds</span></span>
<span data-ttu-id="5496b-145">Limite di tempo in secondi.</span><span class="sxs-lookup"><span data-stu-id="5496b-145">Time limit in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5496b-146">-TotalBytesPerSession</span><span class="sxs-lookup"><span data-stu-id="5496b-146">-TotalBytesPerSession</span></span>
<span data-ttu-id="5496b-147">Byte totali per sessione.</span><span class="sxs-lookup"><span data-stu-id="5496b-147">Total bytes per session.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5496b-148">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5496b-148">-Confirm</span></span>
<span data-ttu-id="5496b-149">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5496b-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5496b-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5496b-150">-WhatIf</span></span>
<span data-ttu-id="5496b-151">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5496b-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5496b-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5496b-152">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5496b-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5496b-153">CommonParameters</span></span>
<span data-ttu-id="5496b-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5496b-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5496b-155">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5496b-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5496b-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5496b-156">INPUTS</span></span>

### <span data-ttu-id="5496b-157">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5496b-157">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="5496b-158">System. String System. Nullable \` 1 \[ \[ System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089\]\]</span><span class="sxs-lookup"><span data-stu-id="5496b-158">System.String System.Nullable\`1\[\[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\]</span></span>

## <span data-ttu-id="5496b-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5496b-159">OUTPUTS</span></span>

### <span data-ttu-id="5496b-160">Microsoft. Azure. Commands. Network. Models. PSPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5496b-160">Microsoft.Azure.Commands.Network.Models.PSPacketCapture</span></span>

## <span data-ttu-id="5496b-161">Note</span><span class="sxs-lookup"><span data-stu-id="5496b-161">NOTES</span></span>
<span data-ttu-id="5496b-162">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher, Packet, Capture, Traffic</span><span class="sxs-lookup"><span data-stu-id="5496b-162">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span> 

## <span data-ttu-id="5496b-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5496b-163">RELATED LINKS</span></span>

[<span data-ttu-id="5496b-164">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="5496b-164">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="5496b-165">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5496b-165">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5496b-166">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5496b-166">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5496b-167">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5496b-167">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5496b-168">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5496b-168">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="5496b-169">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5496b-169">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="5496b-170">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5496b-170">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="5496b-171">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="5496b-171">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="5496b-172">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="5496b-172">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="5496b-173">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="5496b-173">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="5496b-174">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="5496b-174">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="5496b-175">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="5496b-175">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)


