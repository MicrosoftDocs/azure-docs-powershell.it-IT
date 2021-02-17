---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
ms.openlocfilehash: 83ff992b20c24606d09889d0bc49fd9520ef6efb
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401811"
---
# <span data-ttu-id="4f7b6-101">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4f7b6-101">Remove-AzNetworkWatcher</span></span>

## <span data-ttu-id="4f7b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f7b6-102">SYNOPSIS</span></span>
<span data-ttu-id="4f7b6-103">Rimuove un Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="4f7b6-103">Removes a Network Watcher.</span></span>

## <span data-ttu-id="4f7b6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4f7b6-104">SYNTAX</span></span>

### <span data-ttu-id="4f7b6-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4f7b6-105">SetByResource</span></span>
```
Remove-AzNetworkWatcher -NetworkWatcher <PSNetworkWatcher> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f7b6-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="4f7b6-106">SetByName</span></span>
```
Remove-AzNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f7b6-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="4f7b6-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcher -Location <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f7b6-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4f7b6-108">DESCRIPTION</span></span>
<span data-ttu-id="4f7b6-109">Il cmdlet Remove-AzNetworkWatcher rimuove una risorsa Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="4f7b6-109">The Remove-AzNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="4f7b6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4f7b6-110">EXAMPLES</span></span>

### <span data-ttu-id="4f7b6-111">Esempio 1: Creare ed eliminare un Network Watcher</span><span class="sxs-lookup"><span data-stu-id="4f7b6-111">Example 1: Create and delete a Network Watcher</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="4f7b6-112">Questo esempio crea un Network Watcher in un gruppo di risorse e quindi lo elimina immediatamente.</span><span class="sxs-lookup"><span data-stu-id="4f7b6-112">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="4f7b6-113">Si noti che per ogni abbonamento è possibile creare un solo Network Watcher per ogni area geografica.</span><span class="sxs-lookup"><span data-stu-id="4f7b6-113">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="4f7b6-114">Per eliminare la richiesta quando si elimina la rete virtuale, usare il contrassegno -Force.</span><span class="sxs-lookup"><span data-stu-id="4f7b6-114">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="4f7b6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f7b6-115">PARAMETERS</span></span>

### <span data-ttu-id="4f7b6-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4f7b6-116">-AsJob</span></span>
<span data-ttu-id="4f7b6-117">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="4f7b6-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4f7b6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f7b6-118">-DefaultProfile</span></span>
<span data-ttu-id="4f7b6-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4f7b6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f7b6-120">-Location</span><span class="sxs-lookup"><span data-stu-id="4f7b6-120">-Location</span></span>
<span data-ttu-id="4f7b6-121">Posizione del network watcher.</span><span class="sxs-lookup"><span data-stu-id="4f7b6-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="4f7b6-122">-Name</span><span class="sxs-lookup"><span data-stu-id="4f7b6-122">-Name</span></span>
<span data-ttu-id="4f7b6-123">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="4f7b6-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f7b6-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4f7b6-124">-NetworkWatcher</span></span>
<span data-ttu-id="4f7b6-125">Risorsa Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="4f7b6-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="4f7b6-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f7b6-126">-PassThru</span></span>
<span data-ttu-id="4f7b6-127">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="4f7b6-127">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="4f7b6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f7b6-128">-ResourceGroupName</span></span>
<span data-ttu-id="4f7b6-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4f7b6-129">The resource group name.</span></span>

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

### <span data-ttu-id="4f7b6-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4f7b6-130">-Confirm</span></span>
<span data-ttu-id="4f7b6-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f7b6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f7b6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f7b6-132">-WhatIf</span></span>
<span data-ttu-id="4f7b6-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4f7b6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f7b6-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4f7b6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f7b6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f7b6-135">CommonParameters</span></span>
<span data-ttu-id="4f7b6-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f7b6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f7b6-137">Per altre informazioni, vedere about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f7b6-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f7b6-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="4f7b6-138">INPUTS</span></span>

### <span data-ttu-id="4f7b6-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4f7b6-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="4f7b6-140">System.String</span><span class="sxs-lookup"><span data-stu-id="4f7b6-140">System.String</span></span>

## <span data-ttu-id="4f7b6-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4f7b6-141">OUTPUTS</span></span>

### <span data-ttu-id="4f7b6-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4f7b6-142">System.Boolean</span></span>

## <span data-ttu-id="4f7b6-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="4f7b6-143">NOTES</span></span>
<span data-ttu-id="4f7b6-144">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, rete, rete, network watcher</span><span class="sxs-lookup"><span data-stu-id="4f7b6-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="4f7b6-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4f7b6-145">RELATED LINKS</span></span>

[<span data-ttu-id="4f7b6-146">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4f7b6-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="4f7b6-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4f7b6-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="4f7b6-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4f7b6-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="4f7b6-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="4f7b6-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="4f7b6-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="4f7b6-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="4f7b6-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="4f7b6-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="4f7b6-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="4f7b6-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="4f7b6-153">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4f7b6-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4f7b6-154">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="4f7b6-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="4f7b6-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4f7b6-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4f7b6-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4f7b6-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4f7b6-157">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4f7b6-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4f7b6-158">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="4f7b6-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="4f7b6-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="4f7b6-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="4f7b6-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="4f7b6-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="4f7b6-161">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4f7b6-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4f7b6-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4f7b6-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4f7b6-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4f7b6-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4f7b6-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="4f7b6-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="4f7b6-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4f7b6-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4f7b6-166">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4f7b6-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4f7b6-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="4f7b6-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="4f7b6-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="4f7b6-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="4f7b6-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="4f7b6-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="4f7b6-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="4f7b6-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="4f7b6-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="4f7b6-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="4f7b6-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4f7b6-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
