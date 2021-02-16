---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: d6d11590699b52bb7245222ddaa01fbc42938d22
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100414000"
---
# <span data-ttu-id="ed131-101">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ed131-101">Remove-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="ed131-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed131-102">SYNOPSIS</span></span>
<span data-ttu-id="ed131-103">Rimuove una risorsa di acquisizione pacchetti.</span><span class="sxs-lookup"><span data-stu-id="ed131-103">Removes a packet capture resource.</span></span>

## <span data-ttu-id="ed131-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ed131-104">SYNTAX</span></span>

### <span data-ttu-id="ed131-105">SetByResource (Default)</span><span class="sxs-lookup"><span data-stu-id="ed131-105">SetByResource (Default)</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed131-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="ed131-106">SetByName</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed131-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="ed131-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed131-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ed131-108">DESCRIPTION</span></span>
<span data-ttu-id="ed131-109">LRemove-AzNetworkWatcherPacketCapture rimuove una risorsa di acquisizione pacchetti.</span><span class="sxs-lookup"><span data-stu-id="ed131-109">The Remove-AzNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="ed131-110">È consigliabile chiamare il Stop-AzNetworkWatcherPacketCapture rimuovere-AzNetworkWatcherPacketCapture.</span><span class="sxs-lookup"><span data-stu-id="ed131-110">It is recommended to call Stop-AzNetworkWatcherPacketCapture before calling Remove-AzNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="ed131-111">Se la sessione di acquisizione pacchetti è in esecuzione quando Remove-AzNetworkWatcherPacketCapture è chiamata packet capture, l'acquisizione pacchetti potrebbe non essere salvata.</span><span class="sxs-lookup"><span data-stu-id="ed131-111">If the packet capture session is running when Remove-AzNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="ed131-112">Se la sessione viene interrotta prima della rimozione del file CAP contenente dati di acquisizione, non viene rimossa.</span><span class="sxs-lookup"><span data-stu-id="ed131-112">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="ed131-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ed131-113">EXAMPLES</span></span>

### <span data-ttu-id="ed131-114">Esempio 1: Rimuovere una sessione di acquisizione pacchetti</span><span class="sxs-lookup"><span data-stu-id="ed131-114">Example 1: Remove a packet capture session</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="ed131-115">In questo esempio viene rimosso un sessione di acquisizione pacchetti esistente denominata "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="ed131-115">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="ed131-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed131-116">PARAMETERS</span></span>

### <span data-ttu-id="ed131-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed131-117">-AsJob</span></span>
<span data-ttu-id="ed131-118">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ed131-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ed131-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed131-119">-DefaultProfile</span></span>
<span data-ttu-id="ed131-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ed131-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed131-121">-Location</span><span class="sxs-lookup"><span data-stu-id="ed131-121">-Location</span></span>
<span data-ttu-id="ed131-122">Posizione del network watcher.</span><span class="sxs-lookup"><span data-stu-id="ed131-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="ed131-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ed131-123">-NetworkWatcher</span></span>
<span data-ttu-id="ed131-124">Risorsa Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="ed131-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="ed131-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="ed131-125">-NetworkWatcherName</span></span>
<span data-ttu-id="ed131-126">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="ed131-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="ed131-127">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="ed131-127">-PacketCaptureName</span></span>
<span data-ttu-id="ed131-128">Nome di acquisizione pacchetti.</span><span class="sxs-lookup"><span data-stu-id="ed131-128">The packet capture name.</span></span>

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

### <span data-ttu-id="ed131-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ed131-129">-PassThru</span></span>
<span data-ttu-id="ed131-130">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="ed131-130">Returns an object representing the item with which you are working.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed131-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed131-131">-ResourceGroupName</span></span>
<span data-ttu-id="ed131-132">Nome del gruppo di risorse Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="ed131-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="ed131-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed131-133">-Confirm</span></span>
<span data-ttu-id="ed131-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed131-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed131-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed131-135">-WhatIf</span></span>
<span data-ttu-id="ed131-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ed131-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed131-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ed131-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed131-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed131-138">CommonParameters</span></span>
<span data-ttu-id="ed131-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed131-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed131-140">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed131-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed131-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="ed131-141">INPUTS</span></span>

### <span data-ttu-id="ed131-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ed131-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="ed131-143">System.String</span><span class="sxs-lookup"><span data-stu-id="ed131-143">System.String</span></span>

## <span data-ttu-id="ed131-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ed131-144">OUTPUTS</span></span>

### <span data-ttu-id="ed131-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ed131-145">System.Boolean</span></span>

## <span data-ttu-id="ed131-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="ed131-146">NOTES</span></span>
<span data-ttu-id="ed131-147">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, rete, rete, network watcher, pacchetto, acquisizione, traffico, rimuovere</span><span class="sxs-lookup"><span data-stu-id="ed131-147">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="ed131-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ed131-148">RELATED LINKS</span></span>

[<span data-ttu-id="ed131-149">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ed131-149">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="ed131-150">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ed131-150">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="ed131-151">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ed131-151">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="ed131-152">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="ed131-152">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="ed131-153">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="ed131-153">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="ed131-154">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="ed131-154">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="ed131-155">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="ed131-155">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="ed131-156">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ed131-156">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ed131-157">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="ed131-157">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="ed131-158">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ed131-158">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ed131-159">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ed131-159">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ed131-160">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ed131-160">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ed131-161">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed131-161">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="ed131-162">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="ed131-162">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="ed131-163">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="ed131-163">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="ed131-164">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ed131-164">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ed131-165">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ed131-165">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ed131-166">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ed131-166">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ed131-167">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="ed131-167">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="ed131-168">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ed131-168">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ed131-169">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ed131-169">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ed131-170">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="ed131-170">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="ed131-171">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="ed131-171">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="ed131-172">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="ed131-172">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="ed131-173">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="ed131-173">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="ed131-174">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="ed131-174">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="ed131-175">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ed131-175">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
