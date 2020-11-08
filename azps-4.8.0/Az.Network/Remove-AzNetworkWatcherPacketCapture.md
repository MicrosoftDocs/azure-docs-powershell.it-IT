---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: e22b9d85bbc17897742fa2ac0cbdf3e2d8187d5b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188402"
---
# <span data-ttu-id="e2100-101">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e2100-101">Remove-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="e2100-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e2100-102">SYNOPSIS</span></span>
<span data-ttu-id="e2100-103">Rimuove una risorsa di acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="e2100-103">Removes a packet capture resource.</span></span>

## <span data-ttu-id="e2100-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e2100-104">SYNTAX</span></span>

### <span data-ttu-id="e2100-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e2100-105">SetByResource (Default)</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2100-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="e2100-106">SetByName</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2100-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="e2100-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2100-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2100-108">DESCRIPTION</span></span>
<span data-ttu-id="e2100-109">La Remove-AzNetworkWatcherPacketCapture rimuove una risorsa di acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="e2100-109">The Remove-AzNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="e2100-110">È consigliabile chiamare Stop-AzNetworkWatcherPacketCapture prima di chiamare Remove-AzNetworkWatcherPacketCapture.</span><span class="sxs-lookup"><span data-stu-id="e2100-110">It is recommended to call Stop-AzNetworkWatcherPacketCapture before calling Remove-AzNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="e2100-111">Se la sessione di acquisizione di pacchetti viene eseguita quando si chiama Remove-AzNetworkWatcherPacketCapture l'acquisizione di pacchetti potrebbe non essere salvata.</span><span class="sxs-lookup"><span data-stu-id="e2100-111">If the packet capture session is running when Remove-AzNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="e2100-112">Se la sessione viene interrotta prima della rimozione, il file CAP contenente i dati di acquisizione non viene rimosso.</span><span class="sxs-lookup"><span data-stu-id="e2100-112">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="e2100-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e2100-113">EXAMPLES</span></span>

### <span data-ttu-id="e2100-114">Esempio 1: rimuovere una sessione di acquisizione di pacchetti</span><span class="sxs-lookup"><span data-stu-id="e2100-114">Example 1: Remove a packet capture session</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="e2100-115">In questo esempio rimuoviamo una sessione di acquisizione di pacchetti esistente denominata "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="e2100-115">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="e2100-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e2100-116">PARAMETERS</span></span>

### <span data-ttu-id="e2100-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2100-117">-AsJob</span></span>
<span data-ttu-id="e2100-118">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e2100-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e2100-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2100-119">-DefaultProfile</span></span>
<span data-ttu-id="e2100-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e2100-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2100-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="e2100-121">-Location</span></span>
<span data-ttu-id="e2100-122">Posizione del monitoraggio della rete.</span><span class="sxs-lookup"><span data-stu-id="e2100-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="e2100-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e2100-123">-NetworkWatcher</span></span>
<span data-ttu-id="e2100-124">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="e2100-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="e2100-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="e2100-125">-NetworkWatcherName</span></span>
<span data-ttu-id="e2100-126">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="e2100-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="e2100-127">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="e2100-127">-PacketCaptureName</span></span>
<span data-ttu-id="e2100-128">Nome del pacchetto Capture.</span><span class="sxs-lookup"><span data-stu-id="e2100-128">The packet capture name.</span></span>

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

### <span data-ttu-id="e2100-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2100-129">-PassThru</span></span>
<span data-ttu-id="e2100-130">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="e2100-130">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="e2100-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2100-131">-ResourceGroupName</span></span>
<span data-ttu-id="e2100-132">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="e2100-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="e2100-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e2100-133">-Confirm</span></span>
<span data-ttu-id="e2100-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2100-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2100-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2100-135">-WhatIf</span></span>
<span data-ttu-id="e2100-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e2100-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2100-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e2100-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2100-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2100-138">CommonParameters</span></span>
<span data-ttu-id="e2100-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2100-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2100-140">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2100-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2100-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e2100-141">INPUTS</span></span>

### <span data-ttu-id="e2100-142">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e2100-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="e2100-143">System. String</span><span class="sxs-lookup"><span data-stu-id="e2100-143">System.String</span></span>

## <span data-ttu-id="e2100-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e2100-144">OUTPUTS</span></span>

### <span data-ttu-id="e2100-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e2100-145">System.Boolean</span></span>

## <span data-ttu-id="e2100-146">Note</span><span class="sxs-lookup"><span data-stu-id="e2100-146">NOTES</span></span>
<span data-ttu-id="e2100-147">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher, Packet, Capture, Traffic, Remove</span><span class="sxs-lookup"><span data-stu-id="e2100-147">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="e2100-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e2100-148">RELATED LINKS</span></span>

[<span data-ttu-id="e2100-149">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e2100-149">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="e2100-150">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e2100-150">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="e2100-151">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e2100-151">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="e2100-152">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="e2100-152">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="e2100-153">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="e2100-153">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="e2100-154">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="e2100-154">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="e2100-155">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="e2100-155">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="e2100-156">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e2100-156">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e2100-157">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="e2100-157">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="e2100-158">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e2100-158">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e2100-159">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e2100-159">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e2100-160">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e2100-160">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e2100-161">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2100-161">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="e2100-162">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="e2100-162">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="e2100-163">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="e2100-163">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="e2100-164">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e2100-164">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e2100-165">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e2100-165">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e2100-166">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e2100-166">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e2100-167">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="e2100-167">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="e2100-168">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e2100-168">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e2100-169">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e2100-169">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e2100-170">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="e2100-170">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="e2100-171">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="e2100-171">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="e2100-172">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="e2100-172">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="e2100-173">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="e2100-173">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="e2100-174">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="e2100-174">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="e2100-175">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e2100-175">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
