---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 048eeb08b820f5eccd76a74587d4949f1f9de110
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100408407"
---
# <span data-ttu-id="ae4e6-101">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ae4e6-101">Stop-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="ae4e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae4e6-102">SYNOPSIS</span></span>
<span data-ttu-id="ae4e6-103">Interrompe una sessione di acquisizione pacchetti in esecuzione</span><span class="sxs-lookup"><span data-stu-id="ae4e6-103">Stops a running packet capture session</span></span>

## <span data-ttu-id="ae4e6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ae4e6-104">SYNTAX</span></span>

### <span data-ttu-id="ae4e6-105">SetByResource (Default)</span><span class="sxs-lookup"><span data-stu-id="ae4e6-105">SetByResource (Default)</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae4e6-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="ae4e6-106">SetByName</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae4e6-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="ae4e6-107">SetByLocation</span></span>
```
Stop-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae4e6-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ae4e6-108">DESCRIPTION</span></span>
<span data-ttu-id="ae4e6-109">LStop-AzNetworkWatcherPacketCapture interrompe una sessione di acquisizione pacchetti in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="ae4e6-109">The Stop-AzNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="ae4e6-110">Dopo l'interruzione della sessione, il file di acquisizione pacchetti viene caricato nella memoria e/o salvato localmente nella macchina virtuale, a seconda della configurazione.</span><span class="sxs-lookup"><span data-stu-id="ae4e6-110">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="ae4e6-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ae4e6-111">EXAMPLES</span></span>

### <span data-ttu-id="ae4e6-112">Esempio 1: Interrompere una sessione di acquisizione pacchetti</span><span class="sxs-lookup"><span data-stu-id="ae4e6-112">Example 1: Stop a packet capture session</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="ae4e6-113">In questo esempio viene interrotta una sessione di acquisizione pacchetti in esecuzione denominata "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="ae4e6-113">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="ae4e6-114">Dopo l'interruzione della sessione, il file di acquisizione pacchetti viene caricato nella memoria e/o salvato localmente nella macchina virtuale, a seconda della configurazione.</span><span class="sxs-lookup"><span data-stu-id="ae4e6-114">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="ae4e6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae4e6-115">PARAMETERS</span></span>

### <span data-ttu-id="ae4e6-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ae4e6-116">-AsJob</span></span>
<span data-ttu-id="ae4e6-117">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ae4e6-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ae4e6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae4e6-118">-DefaultProfile</span></span>
<span data-ttu-id="ae4e6-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ae4e6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae4e6-120">-Location</span><span class="sxs-lookup"><span data-stu-id="ae4e6-120">-Location</span></span>
<span data-ttu-id="ae4e6-121">Posizione del network watcher.</span><span class="sxs-lookup"><span data-stu-id="ae4e6-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="ae4e6-122">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ae4e6-122">-NetworkWatcher</span></span>
<span data-ttu-id="ae4e6-123">Risorsa Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="ae4e6-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="ae4e6-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="ae4e6-124">-NetworkWatcherName</span></span>
<span data-ttu-id="ae4e6-125">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="ae4e6-125">The name of network watcher.</span></span>

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

### <span data-ttu-id="ae4e6-126">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="ae4e6-126">-PacketCaptureName</span></span>
<span data-ttu-id="ae4e6-127">Nome di acquisizione pacchetti.</span><span class="sxs-lookup"><span data-stu-id="ae4e6-127">The packet capture name.</span></span>

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

### <span data-ttu-id="ae4e6-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ae4e6-128">-PassThru</span></span>
<span data-ttu-id="ae4e6-129">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="ae4e6-129">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="ae4e6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae4e6-130">-ResourceGroupName</span></span>
<span data-ttu-id="ae4e6-131">Nome del gruppo di risorse Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="ae4e6-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="ae4e6-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ae4e6-132">-Confirm</span></span>
<span data-ttu-id="ae4e6-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae4e6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae4e6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae4e6-134">-WhatIf</span></span>
<span data-ttu-id="ae4e6-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae4e6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae4e6-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae4e6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae4e6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae4e6-137">CommonParameters</span></span>
<span data-ttu-id="ae4e6-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae4e6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae4e6-139">Per altre informazioni, vedere about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae4e6-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae4e6-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="ae4e6-140">INPUTS</span></span>

### <span data-ttu-id="ae4e6-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ae4e6-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="ae4e6-142">System.String</span><span class="sxs-lookup"><span data-stu-id="ae4e6-142">System.String</span></span>

## <span data-ttu-id="ae4e6-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ae4e6-143">OUTPUTS</span></span>

### <span data-ttu-id="ae4e6-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ae4e6-144">System.Boolean</span></span>

## <span data-ttu-id="ae4e6-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="ae4e6-145">NOTES</span></span>
<span data-ttu-id="ae4e6-146">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, rete, rete, network watcher, pacchetto, acquisizione, traffico</span><span class="sxs-lookup"><span data-stu-id="ae4e6-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="ae4e6-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ae4e6-147">RELATED LINKS</span></span>

[<span data-ttu-id="ae4e6-148">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ae4e6-148">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ae4e6-149">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="ae4e6-149">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="ae4e6-150">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ae4e6-150">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ae4e6-151">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ae4e6-151">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ae4e6-152">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ae4e6-152">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="ae4e6-153">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ae4e6-153">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="ae4e6-154">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ae4e6-154">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="ae4e6-155">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="ae4e6-155">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="ae4e6-156">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="ae4e6-156">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="ae4e6-157">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="ae4e6-157">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="ae4e6-158">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="ae4e6-158">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="ae4e6-159">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="ae4e6-159">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="ae4e6-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="ae4e6-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="ae4e6-161">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ae4e6-161">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ae4e6-162">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae4e6-162">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="ae4e6-163">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="ae4e6-163">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="ae4e6-164">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ae4e6-164">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ae4e6-165">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ae4e6-165">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ae4e6-166">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ae4e6-166">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ae4e6-167">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="ae4e6-167">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="ae4e6-168">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ae4e6-168">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ae4e6-169">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ae4e6-169">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ae4e6-170">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="ae4e6-170">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="ae4e6-171">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="ae4e6-171">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="ae4e6-172">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="ae4e6-172">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="ae4e6-173">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="ae4e6-173">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="ae4e6-174">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ae4e6-174">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
