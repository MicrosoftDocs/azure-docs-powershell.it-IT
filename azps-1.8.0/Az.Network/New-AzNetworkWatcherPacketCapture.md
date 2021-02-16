---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 0494a182feba20b2af8aab9bcf38772441e2822e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400162"
---
# <span data-ttu-id="d7ee5-101">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d7ee5-101">New-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="d7ee5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7ee5-102">SYNOPSIS</span></span>
<span data-ttu-id="d7ee5-103">Crea una nuova risorsa di acquisizione pacchetti e avvia una sessione di acquisizione pacchetti in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d7ee5-103">Creates a new packet capture resource and starts a packet capture session on a VM.</span></span>

## <span data-ttu-id="d7ee5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d7ee5-104">SYNTAX</span></span>

### <span data-ttu-id="d7ee5-105">SetByResource (Default)</span><span class="sxs-lookup"><span data-stu-id="d7ee5-105">SetByResource (Default)</span></span>
```
New-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7ee5-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="d7ee5-106">SetByName</span></span>
```
New-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> -TargetVirtualMachineId <String> [-StorageAccountId <String>]
 [-StoragePath <String>] [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>]
 [-TotalBytesPerSession <Int32>] [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7ee5-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="d7ee5-107">SetByLocation</span></span>
```
New-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7ee5-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d7ee5-108">DESCRIPTION</span></span>
<span data-ttu-id="d7ee5-109">Il cmdlet New-AzNetworkWatcherPacketCapture crea una nuova risorsa di acquisizione pacchetti e avvia una sessione di acquisizione pacchetti in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d7ee5-109">The New-AzNetworkWatcherPacketCapture cmdlet creates a new packet capture resource and starts a packet capture session on a VM.</span></span>
<span data-ttu-id="d7ee5-110">La lunghezza delle sessioni di acquisizione pacchetti può essere configurata con un vincolo temporale o di dimensioni.</span><span class="sxs-lookup"><span data-stu-id="d7ee5-110">The length of the Packet Capture sessions can be configured via a time constraint or a size constraint.</span></span> <span data-ttu-id="d7ee5-111">Può essere configurata anche la quantità di dati acquisiti per ogni pacchetto.</span><span class="sxs-lookup"><span data-stu-id="d7ee5-111">The amount of data captured for each packet can also be configured.</span></span>
<span data-ttu-id="d7ee5-112">I filtri possono essere applicati a una determinata sessione di acquisizione pacchetti, consentendo di personalizzare il tipo di pacchetti acquisiti.</span><span class="sxs-lookup"><span data-stu-id="d7ee5-112">Filters can be applied to a given packet capture session, allowing you to customize the type of packets captured.</span></span> <span data-ttu-id="d7ee5-113">I filtri possono limitare i pacchetti in indirizzi IP locali e remoti & intervalli di indirizzi, porte locali e remote & intervalli di porte e il protocollo a livello di sessione da acquisire.</span><span class="sxs-lookup"><span data-stu-id="d7ee5-113">Filters can restrict packets on local and remote IP addresses & address ranges, local and remote ports & port ranges, and the session level protocol to be captured.</span></span> <span data-ttu-id="d7ee5-114">I filtri sono componibili e possono essere applicati più filtri per fornire la granularità di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="d7ee5-114">Filters are composable, and multiple filters can be applied to provide you with granularity of capture.</span></span>

## <span data-ttu-id="d7ee5-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d7ee5-115">EXAMPLES</span></span>

### <span data-ttu-id="d7ee5-116">Esempio 1: Creare un packet capture con più filtri</span><span class="sxs-lookup"><span data-stu-id="d7ee5-116">Example 1: Create a Packet Capture with multiple filters</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filter $filter1, $filter2
```

<span data-ttu-id="d7ee5-117">In questo esempio viene creata un'acquisizione di pacchetti denominata "PacketCaptureTest" con più filtri e un limite di tempo.</span><span class="sxs-lookup"><span data-stu-id="d7ee5-117">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="d7ee5-118">Una volta completata, la sessione verrà salvata nell'account di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="d7ee5-118">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="d7ee5-119">Nota: l'estensione Network Watcher di Azure deve essere installata nella macchina virtuale di destinazione per creare acquisizioni di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="d7ee5-119">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="d7ee5-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7ee5-120">PARAMETERS</span></span>

### <span data-ttu-id="d7ee5-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d7ee5-121">-AsJob</span></span>
<span data-ttu-id="d7ee5-122">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d7ee5-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d7ee5-123">-BytesToCapturePerPacket</span><span class="sxs-lookup"><span data-stu-id="d7ee5-123">-BytesToCapturePerPacket</span></span>
<span data-ttu-id="d7ee5-124">Byte da acquisire per pacchetto.</span><span class="sxs-lookup"><span data-stu-id="d7ee5-124">Bytes to capture per packet.</span></span>

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

### <span data-ttu-id="d7ee5-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7ee5-125">-DefaultProfile</span></span>
<span data-ttu-id="d7ee5-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d7ee5-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7ee5-127">-Filter</span><span class="sxs-lookup"><span data-stu-id="d7ee5-127">-Filter</span></span>
<span data-ttu-id="d7ee5-128">Filtri per la sessione di acquisizione pacchetti.</span><span class="sxs-lookup"><span data-stu-id="d7ee5-128">Filters for packet capture session.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7ee5-129">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="d7ee5-129">-LocalFilePath</span></span>
<span data-ttu-id="d7ee5-130">Percorso file locale.</span><span class="sxs-lookup"><span data-stu-id="d7ee5-130">Local file path.</span></span>

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

### <span data-ttu-id="d7ee5-131">-Location</span><span class="sxs-lookup"><span data-stu-id="d7ee5-131">-Location</span></span>
<span data-ttu-id="d7ee5-132">Posizione del network watcher.</span><span class="sxs-lookup"><span data-stu-id="d7ee5-132">Location of the network watcher.</span></span>

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

### <span data-ttu-id="d7ee5-133">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d7ee5-133">-NetworkWatcher</span></span>
<span data-ttu-id="d7ee5-134">Risorsa Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="d7ee5-134">The network watcher resource.</span></span>

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

### <span data-ttu-id="d7ee5-135">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d7ee5-135">-NetworkWatcherName</span></span>
<span data-ttu-id="d7ee5-136">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="d7ee5-136">The name of network watcher.</span></span>

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

### <span data-ttu-id="d7ee5-137">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="d7ee5-137">-PacketCaptureName</span></span>
<span data-ttu-id="d7ee5-138">Nome di acquisizione pacchetti.</span><span class="sxs-lookup"><span data-stu-id="d7ee5-138">The packet capture name.</span></span>

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

### <span data-ttu-id="d7ee5-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7ee5-139">-ResourceGroupName</span></span>
<span data-ttu-id="d7ee5-140">Nome del gruppo di risorse Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="d7ee5-140">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="d7ee5-141">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="d7ee5-141">-StorageAccountId</span></span>
<span data-ttu-id="d7ee5-142">ID account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d7ee5-142">Storage account Id.</span></span>

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

### <span data-ttu-id="d7ee5-143">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="d7ee5-143">-StoragePath</span></span>
<span data-ttu-id="d7ee5-144">Percorso di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d7ee5-144">Storage path.</span></span>

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

### <span data-ttu-id="d7ee5-145">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="d7ee5-145">-TargetVirtualMachineId</span></span>
<span data-ttu-id="d7ee5-146">ID della macchina virtuale di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d7ee5-146">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="d7ee5-147">-TimeLimitInSeconds</span><span class="sxs-lookup"><span data-stu-id="d7ee5-147">-TimeLimitInSeconds</span></span>
<span data-ttu-id="d7ee5-148">Limite di tempo in secondi.</span><span class="sxs-lookup"><span data-stu-id="d7ee5-148">Time limit in seconds.</span></span>

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

### <span data-ttu-id="d7ee5-149">-TotalBytesPerSession</span><span class="sxs-lookup"><span data-stu-id="d7ee5-149">-TotalBytesPerSession</span></span>
<span data-ttu-id="d7ee5-150">Totale byte per sessione.</span><span class="sxs-lookup"><span data-stu-id="d7ee5-150">Total bytes per session.</span></span>

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

### <span data-ttu-id="d7ee5-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7ee5-151">-Confirm</span></span>
<span data-ttu-id="d7ee5-152">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7ee5-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7ee5-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7ee5-153">-WhatIf</span></span>
<span data-ttu-id="d7ee5-154">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d7ee5-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7ee5-155">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d7ee5-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7ee5-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7ee5-156">CommonParameters</span></span>
<span data-ttu-id="d7ee5-157">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7ee5-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7ee5-158">Per altre informazioni, vedere about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7ee5-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7ee5-159">INPUT</span><span class="sxs-lookup"><span data-stu-id="d7ee5-159">INPUTS</span></span>

### <span data-ttu-id="d7ee5-160">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d7ee5-160">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="d7ee5-161">System.String</span><span class="sxs-lookup"><span data-stu-id="d7ee5-161">System.String</span></span>

### <span data-ttu-id="d7ee5-162">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d7ee5-162">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="d7ee5-163">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d7ee5-163">OUTPUTS</span></span>

### <span data-ttu-id="d7ee5-164">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="d7ee5-164">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureResult</span></span>

## <span data-ttu-id="d7ee5-165">NOTE</span><span class="sxs-lookup"><span data-stu-id="d7ee5-165">NOTES</span></span>
<span data-ttu-id="d7ee5-166">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, rete, rete, network watcher, pacchetto, acquisizione, traffico</span><span class="sxs-lookup"><span data-stu-id="d7ee5-166">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span> 

## <span data-ttu-id="d7ee5-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d7ee5-167">RELATED LINKS</span></span>

[<span data-ttu-id="d7ee5-168">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d7ee5-168">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="d7ee5-169">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d7ee5-169">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="d7ee5-170">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d7ee5-170">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="d7ee5-171">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d7ee5-171">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="d7ee5-172">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d7ee5-172">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d7ee5-173">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d7ee5-173">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="d7ee5-174">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d7ee5-174">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="d7ee5-175">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d7ee5-175">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d7ee5-176">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d7ee5-176">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="d7ee5-177">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d7ee5-177">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d7ee5-178">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d7ee5-178">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d7ee5-179">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d7ee5-179">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d7ee5-180">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="d7ee5-180">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="d7ee5-181">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d7ee5-181">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="d7ee5-182">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="d7ee5-182">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="d7ee5-183">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d7ee5-183">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d7ee5-184">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d7ee5-184">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d7ee5-185">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d7ee5-185">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d7ee5-186">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="d7ee5-186">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="d7ee5-187">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d7ee5-187">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d7ee5-188">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d7ee5-188">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d7ee5-189">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="d7ee5-189">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="d7ee5-190">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="d7ee5-190">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="d7ee5-191">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="d7ee5-191">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="d7ee5-192">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="d7ee5-192">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="d7ee5-193">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="d7ee5-193">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="d7ee5-194">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d7ee5-194">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)


