---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 87ae0ab7be4ace85d9f02a5637ea29dd27b0ae14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520025"
---
# <span data-ttu-id="1d8fe-101">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1d8fe-101">New-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="1d8fe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1d8fe-102">SYNOPSIS</span></span>
<span data-ttu-id="1d8fe-103">Crea una nuova risorsa di acquisizione di pacchetti e avvia una sessione di acquisizione di pacchetti in una VM.</span><span class="sxs-lookup"><span data-stu-id="1d8fe-103">Creates a new packet capture resource and starts a packet capture session on a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d8fe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1d8fe-104">SYNTAX</span></span>

### <span data-ttu-id="1d8fe-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1d8fe-105">SetByResource (Default)</span></span>
```
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d8fe-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="1d8fe-106">SetByName</span></span>
```
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> -TargetVirtualMachineId <String> [-StorageAccountId <String>]
 [-StoragePath <String>] [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>]
 [-TotalBytesPerSession <Int32>] [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d8fe-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d8fe-107">DESCRIPTION</span></span>
<span data-ttu-id="1d8fe-108">Il cmdlet New-AzureRmNetworkWatcherPacketCapture crea una nuova risorsa di acquisizione di pacchetti e avvia una sessione di acquisizione di pacchetti in una VM.</span><span class="sxs-lookup"><span data-stu-id="1d8fe-108">The New-AzureRmNetworkWatcherPacketCapture cmdlet creates a new packet capture resource and starts a packet capture session on a VM.</span></span>
<span data-ttu-id="1d8fe-109">La lunghezza delle sessioni di acquisizione di pacchetti può essere configurata tramite un vincolo temporale o un vincolo di dimensione.</span><span class="sxs-lookup"><span data-stu-id="1d8fe-109">The length of the Packet Capture sessions can be configured via a time constraint or a size constraint.</span></span> <span data-ttu-id="1d8fe-110">La quantità di dati acquisiti per ogni pacchetto può anche essere configurata.</span><span class="sxs-lookup"><span data-stu-id="1d8fe-110">The amount of data captured for each packet can also be configured.</span></span>
<span data-ttu-id="1d8fe-111">I filtri possono essere applicati a una determinata sessione di acquisizione di pacchetti, che consente di personalizzare il tipo di pacchetti acquisiti.</span><span class="sxs-lookup"><span data-stu-id="1d8fe-111">Filters can be applied to a given packet capture session, allowing you to customize the type of packets captured.</span></span> <span data-ttu-id="1d8fe-112">I filtri possono limitare i pacchetti in indirizzi IP locali e remoti & intervalli di indirizzi, porte locali e remote & intervalli di porte e il protocollo del livello di sessione da acquisire.</span><span class="sxs-lookup"><span data-stu-id="1d8fe-112">Filters can restrict packets on local and remote IP addresses & address ranges, local and remote ports & port ranges, and the session level protocol to be captured.</span></span> <span data-ttu-id="1d8fe-113">I filtri sono componibili e possono essere applicati più filtri per garantirti la granularità dell'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="1d8fe-113">Filters are composable, and multiple filters can be applied to provide you with granularity of capture.</span></span>

## <span data-ttu-id="1d8fe-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1d8fe-114">EXAMPLES</span></span>

### <span data-ttu-id="1d8fe-115">---Esempio 1: creare un'acquisizione di pacchetti con più filtri---</span><span class="sxs-lookup"><span data-stu-id="1d8fe-115">--- Example 1: Create a Packet Capture with multiple filters ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filter $filter1, $filter2
```

<span data-ttu-id="1d8fe-116">In questo esempio creiamo un'acquisizione di pacchetti denominata "PacketCaptureTest" con più filtri e un limite di tempo.</span><span class="sxs-lookup"><span data-stu-id="1d8fe-116">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="1d8fe-117">Una volta completata la sessione, verrà salvata nell'account di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="1d8fe-117">Once the session is complete, it will be saved to the specified storage account.</span></span> 

<span data-ttu-id="1d8fe-118">Nota: l'estensione Azure Network Watcher deve essere installata nella macchina virtuale di destinazione per creare acquisizioni di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="1d8fe-118">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="1d8fe-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1d8fe-119">PARAMETERS</span></span>

### <span data-ttu-id="1d8fe-120">-BytesToCapturePerPacket</span><span class="sxs-lookup"><span data-stu-id="1d8fe-120">-BytesToCapturePerPacket</span></span>
<span data-ttu-id="1d8fe-121">Byte da acquisire per pacchetto.</span><span class="sxs-lookup"><span data-stu-id="1d8fe-121">Bytes to capture per packet.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d8fe-122">-Filtro</span><span class="sxs-lookup"><span data-stu-id="1d8fe-122">-Filter</span></span>
<span data-ttu-id="1d8fe-123">Filtri per la sessione di acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="1d8fe-123">Filters for packet capture session.</span></span>

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

### <span data-ttu-id="1d8fe-124">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="1d8fe-124">-LocalFilePath</span></span>
<span data-ttu-id="1d8fe-125">Percorso file locale.</span><span class="sxs-lookup"><span data-stu-id="1d8fe-125">Local file path.</span></span>

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

### <span data-ttu-id="1d8fe-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1d8fe-126">-NetworkWatcher</span></span>
<span data-ttu-id="1d8fe-127">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="1d8fe-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="1d8fe-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="1d8fe-128">-NetworkWatcherName</span></span>
<span data-ttu-id="1d8fe-129">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="1d8fe-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="1d8fe-130">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="1d8fe-130">-PacketCaptureName</span></span>
<span data-ttu-id="1d8fe-131">Nome del pacchetto Capture.</span><span class="sxs-lookup"><span data-stu-id="1d8fe-131">The packet capture name.</span></span>

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

### <span data-ttu-id="1d8fe-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d8fe-132">-ResourceGroupName</span></span>
<span data-ttu-id="1d8fe-133">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="1d8fe-133">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="1d8fe-134">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="1d8fe-134">-StorageAccountId</span></span>
<span data-ttu-id="1d8fe-135">ID account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1d8fe-135">Storage account Id.</span></span>

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

### <span data-ttu-id="1d8fe-136">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="1d8fe-136">-StoragePath</span></span>
<span data-ttu-id="1d8fe-137">Percorso di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1d8fe-137">Storage path.</span></span>

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

### <span data-ttu-id="1d8fe-138">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="1d8fe-138">-TargetVirtualMachineId</span></span>
<span data-ttu-id="1d8fe-139">ID macchina virtuale di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1d8fe-139">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="1d8fe-140">-TimeLimitInSeconds</span><span class="sxs-lookup"><span data-stu-id="1d8fe-140">-TimeLimitInSeconds</span></span>
<span data-ttu-id="1d8fe-141">Limite di tempo in secondi.</span><span class="sxs-lookup"><span data-stu-id="1d8fe-141">Time limit in seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d8fe-142">-TotalBytesPerSession</span><span class="sxs-lookup"><span data-stu-id="1d8fe-142">-TotalBytesPerSession</span></span>
<span data-ttu-id="1d8fe-143">Byte totali per sessione.</span><span class="sxs-lookup"><span data-stu-id="1d8fe-143">Total bytes per session.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d8fe-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1d8fe-144">-Confirm</span></span>
<span data-ttu-id="1d8fe-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d8fe-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d8fe-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d8fe-146">-WhatIf</span></span>
<span data-ttu-id="1d8fe-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1d8fe-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d8fe-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1d8fe-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d8fe-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d8fe-149">-DefaultProfile</span></span>
<span data-ttu-id="1d8fe-150">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1d8fe-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d8fe-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d8fe-151">CommonParameters</span></span>
<span data-ttu-id="1d8fe-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d8fe-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d8fe-153">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d8fe-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d8fe-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1d8fe-154">INPUTS</span></span>

### <span data-ttu-id="1d8fe-155">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1d8fe-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="1d8fe-156">System. String System. Nullable \` 1 \[ \[ System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089\]\]</span><span class="sxs-lookup"><span data-stu-id="1d8fe-156">System.String System.Nullable\`1\[\[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\]</span></span>

## <span data-ttu-id="1d8fe-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1d8fe-157">OUTPUTS</span></span>

### <span data-ttu-id="1d8fe-158">Microsoft. Azure. Commands. Network. Models. PSPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1d8fe-158">Microsoft.Azure.Commands.Network.Models.PSPacketCapture</span></span>

## <span data-ttu-id="1d8fe-159">Note</span><span class="sxs-lookup"><span data-stu-id="1d8fe-159">NOTES</span></span>
<span data-ttu-id="1d8fe-160">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher, Packet, Capture, Traffic</span><span class="sxs-lookup"><span data-stu-id="1d8fe-160">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span> 

## <span data-ttu-id="1d8fe-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1d8fe-161">RELATED LINKS</span></span>

[<span data-ttu-id="1d8fe-162">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="1d8fe-162">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="1d8fe-163">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1d8fe-163">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1d8fe-164">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1d8fe-164">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1d8fe-165">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1d8fe-165">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1d8fe-166">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1d8fe-166">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="1d8fe-167">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1d8fe-167">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="1d8fe-168">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1d8fe-168">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="1d8fe-169">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="1d8fe-169">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="1d8fe-170">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="1d8fe-170">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="1d8fe-171">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="1d8fe-171">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="1d8fe-172">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="1d8fe-172">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="1d8fe-173">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="1d8fe-173">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)


