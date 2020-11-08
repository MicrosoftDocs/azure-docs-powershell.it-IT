---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 959f74472014561fa1b83631eed04b34224910e6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019062"
---
# <span data-ttu-id="674f6-101">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="674f6-101">Stop-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="674f6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="674f6-102">SYNOPSIS</span></span>
<span data-ttu-id="674f6-103">Interrompe una sessione di acquisizione di pacchetti in corso</span><span class="sxs-lookup"><span data-stu-id="674f6-103">Stops a running packet capture session</span></span>

## <span data-ttu-id="674f6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="674f6-104">SYNTAX</span></span>

### <span data-ttu-id="674f6-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="674f6-105">SetByResource (Default)</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="674f6-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="674f6-106">SetByName</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="674f6-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="674f6-107">SetByLocation</span></span>
```
Stop-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="674f6-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="674f6-108">DESCRIPTION</span></span>
<span data-ttu-id="674f6-109">L'Stop-AzNetworkWatcherPacketCapture interrompe una sessione di acquisizione di pacchetti in corso.</span><span class="sxs-lookup"><span data-stu-id="674f6-109">The Stop-AzNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="674f6-110">Dopo l'interruzione della sessione, il file di acquisizione di pacchetti viene caricato nello spazio di archiviazione e/o salvato localmente nella VM a seconda della configurazione.</span><span class="sxs-lookup"><span data-stu-id="674f6-110">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="674f6-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="674f6-111">EXAMPLES</span></span>

### <span data-ttu-id="674f6-112">Esempio 1: interrompere una sessione di acquisizione di pacchetti</span><span class="sxs-lookup"><span data-stu-id="674f6-112">Example 1: Stop a packet capture session</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="674f6-113">In questo esempio interrompiamo una sessione di acquisizione di pacchetti in corso denominata "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="674f6-113">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="674f6-114">Dopo l'interruzione della sessione, il file di acquisizione di pacchetti viene caricato nello spazio di archiviazione e/o salvato localmente nella VM a seconda della configurazione.</span><span class="sxs-lookup"><span data-stu-id="674f6-114">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="674f6-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="674f6-115">PARAMETERS</span></span>

### <span data-ttu-id="674f6-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="674f6-116">-AsJob</span></span>
<span data-ttu-id="674f6-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="674f6-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="674f6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="674f6-118">-DefaultProfile</span></span>
<span data-ttu-id="674f6-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="674f6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="674f6-120">-Posizione</span><span class="sxs-lookup"><span data-stu-id="674f6-120">-Location</span></span>
<span data-ttu-id="674f6-121">Posizione del monitoraggio della rete.</span><span class="sxs-lookup"><span data-stu-id="674f6-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="674f6-122">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="674f6-122">-NetworkWatcher</span></span>
<span data-ttu-id="674f6-123">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="674f6-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="674f6-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="674f6-124">-NetworkWatcherName</span></span>
<span data-ttu-id="674f6-125">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="674f6-125">The name of network watcher.</span></span>

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

### <span data-ttu-id="674f6-126">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="674f6-126">-PacketCaptureName</span></span>
<span data-ttu-id="674f6-127">Nome del pacchetto Capture.</span><span class="sxs-lookup"><span data-stu-id="674f6-127">The packet capture name.</span></span>

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

### <span data-ttu-id="674f6-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="674f6-128">-PassThru</span></span>
<span data-ttu-id="674f6-129">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="674f6-129">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="674f6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="674f6-130">-ResourceGroupName</span></span>
<span data-ttu-id="674f6-131">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="674f6-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="674f6-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="674f6-132">-Confirm</span></span>
<span data-ttu-id="674f6-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="674f6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="674f6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="674f6-134">-WhatIf</span></span>
<span data-ttu-id="674f6-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="674f6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="674f6-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="674f6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="674f6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="674f6-137">CommonParameters</span></span>
<span data-ttu-id="674f6-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="674f6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="674f6-139">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="674f6-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="674f6-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="674f6-140">INPUTS</span></span>

### <span data-ttu-id="674f6-141">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="674f6-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="674f6-142">System. String</span><span class="sxs-lookup"><span data-stu-id="674f6-142">System.String</span></span>

## <span data-ttu-id="674f6-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="674f6-143">OUTPUTS</span></span>

### <span data-ttu-id="674f6-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="674f6-144">System.Boolean</span></span>

## <span data-ttu-id="674f6-145">Note</span><span class="sxs-lookup"><span data-stu-id="674f6-145">NOTES</span></span>
<span data-ttu-id="674f6-146">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher, Packet, Capture, Traffic</span><span class="sxs-lookup"><span data-stu-id="674f6-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="674f6-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="674f6-147">RELATED LINKS</span></span>

[<span data-ttu-id="674f6-148">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="674f6-148">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="674f6-149">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="674f6-149">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="674f6-150">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="674f6-150">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="674f6-151">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="674f6-151">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="674f6-152">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="674f6-152">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="674f6-153">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="674f6-153">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="674f6-154">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="674f6-154">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="674f6-155">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="674f6-155">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="674f6-156">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="674f6-156">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="674f6-157">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="674f6-157">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="674f6-158">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="674f6-158">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="674f6-159">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="674f6-159">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="674f6-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="674f6-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="674f6-161">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="674f6-161">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="674f6-162">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="674f6-162">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="674f6-163">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="674f6-163">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="674f6-164">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="674f6-164">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="674f6-165">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="674f6-165">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="674f6-166">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="674f6-166">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="674f6-167">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="674f6-167">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="674f6-168">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="674f6-168">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="674f6-169">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="674f6-169">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="674f6-170">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="674f6-170">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="674f6-171">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="674f6-171">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="674f6-172">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="674f6-172">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="674f6-173">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="674f6-173">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="674f6-174">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="674f6-174">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
