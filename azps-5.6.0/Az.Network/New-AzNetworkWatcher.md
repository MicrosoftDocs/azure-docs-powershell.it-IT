---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
ms.openlocfilehash: 331665aae56715db41e4789e9d0c74fc253e7440
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971901"
---
# <span data-ttu-id="1b31d-101">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1b31d-101">New-AzNetworkWatcher</span></span>

## <span data-ttu-id="1b31d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b31d-102">SYNOPSIS</span></span>
<span data-ttu-id="1b31d-103">Crea una nuova risorsa Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="1b31d-103">Creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="1b31d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1b31d-104">SYNTAX</span></span>

```
New-AzNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b31d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1b31d-105">DESCRIPTION</span></span>
<span data-ttu-id="1b31d-106">Il cmdlet New-AzNetworkWatcher crea una nuova risorsa Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="1b31d-106">The New-AzNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="1b31d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1b31d-107">EXAMPLES</span></span>

### <span data-ttu-id="1b31d-108">Esempio 1: Creare un Network Watcher</span><span class="sxs-lookup"><span data-stu-id="1b31d-108">Example 1: Create a Network Watcher</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"7cf1f2fe-8445-4aa7-9bf5-c15347282c39"
Location          : westcentralus
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="1b31d-109">Questo esempio crea un nuovo Network Watcher all'interno di un gruppo di risorse appena creato.</span><span class="sxs-lookup"><span data-stu-id="1b31d-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="1b31d-110">Si noti che per ogni abbonamento è possibile creare un solo Network Watcher per ogni area geografica.</span><span class="sxs-lookup"><span data-stu-id="1b31d-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="1b31d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b31d-111">PARAMETERS</span></span>

### <span data-ttu-id="1b31d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b31d-112">-DefaultProfile</span></span>
<span data-ttu-id="1b31d-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1b31d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b31d-114">-Location</span><span class="sxs-lookup"><span data-stu-id="1b31d-114">-Location</span></span>
<span data-ttu-id="1b31d-115">Posizione.</span><span class="sxs-lookup"><span data-stu-id="1b31d-115">Location.</span></span>

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

### <span data-ttu-id="1b31d-116">-Name</span><span class="sxs-lookup"><span data-stu-id="1b31d-116">-Name</span></span>
<span data-ttu-id="1b31d-117">Nome del network watcher.</span><span class="sxs-lookup"><span data-stu-id="1b31d-117">The network watcher name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b31d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b31d-118">-ResourceGroupName</span></span>
<span data-ttu-id="1b31d-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1b31d-119">The resource group name.</span></span>

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

### <span data-ttu-id="1b31d-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="1b31d-120">-Tag</span></span>
<span data-ttu-id="1b31d-121">Coppie chiave-valore sotto forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="1b31d-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1b31d-122">Ad esempio: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="1b31d-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b31d-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1b31d-123">-Confirm</span></span>
<span data-ttu-id="1b31d-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b31d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b31d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b31d-125">-WhatIf</span></span>
<span data-ttu-id="1b31d-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1b31d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b31d-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1b31d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b31d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b31d-128">CommonParameters</span></span>
<span data-ttu-id="1b31d-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b31d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b31d-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b31d-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b31d-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="1b31d-131">INPUTS</span></span>

### <span data-ttu-id="1b31d-132">System.String</span><span class="sxs-lookup"><span data-stu-id="1b31d-132">System.String</span></span>

### <span data-ttu-id="1b31d-133">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="1b31d-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1b31d-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1b31d-134">OUTPUTS</span></span>

### <span data-ttu-id="1b31d-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1b31d-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="1b31d-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="1b31d-136">NOTES</span></span>
<span data-ttu-id="1b31d-137">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, rete, rete, network watcher</span><span class="sxs-lookup"><span data-stu-id="1b31d-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="1b31d-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1b31d-138">RELATED LINKS</span></span>

[<span data-ttu-id="1b31d-139">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1b31d-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="1b31d-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1b31d-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="1b31d-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1b31d-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="1b31d-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="1b31d-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="1b31d-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="1b31d-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="1b31d-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="1b31d-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="1b31d-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="1b31d-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="1b31d-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1b31d-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1b31d-147">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="1b31d-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="1b31d-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1b31d-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1b31d-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1b31d-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1b31d-150">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1b31d-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1b31d-151">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="1b31d-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="1b31d-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="1b31d-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="1b31d-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="1b31d-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="1b31d-154">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1b31d-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1b31d-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1b31d-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1b31d-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1b31d-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1b31d-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="1b31d-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="1b31d-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1b31d-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1b31d-159">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1b31d-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1b31d-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="1b31d-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="1b31d-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="1b31d-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="1b31d-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="1b31d-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="1b31d-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="1b31d-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="1b31d-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="1b31d-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="1b31d-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1b31d-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
