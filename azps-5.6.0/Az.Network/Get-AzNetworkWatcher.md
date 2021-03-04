---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcher.md
ms.openlocfilehash: 93534530c84898f3c4243ad85c75de5bc72e23c4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954462"
---
# <span data-ttu-id="35312-101">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="35312-101">Get-AzNetworkWatcher</span></span>

## <span data-ttu-id="35312-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35312-102">SYNOPSIS</span></span>
<span data-ttu-id="35312-103">Ottiene le proprietà di un Network Watcher</span><span class="sxs-lookup"><span data-stu-id="35312-103">Gets the properties of a Network Watcher</span></span>

## <span data-ttu-id="35312-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="35312-104">SYNTAX</span></span>

### <span data-ttu-id="35312-105">Elenco</span><span class="sxs-lookup"><span data-stu-id="35312-105">List</span></span>
```
Get-AzNetworkWatcher [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="35312-106">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="35312-106">SetByLocation</span></span>
```
Get-AzNetworkWatcher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35312-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="35312-107">DESCRIPTION</span></span>
<span data-ttu-id="35312-108">Il cmdlet Get-AzNetworkWatcher cmdlet ottiene una o più risorse di Azure Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="35312-108">The Get-AzNetworkWatcher cmdlet gets one or more Azure Network Watcher resources.</span></span>

## <span data-ttu-id="35312-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="35312-109">EXAMPLES</span></span>

### <span data-ttu-id="35312-110">Esempio 1: Ottenere un Network Watcher</span><span class="sxs-lookup"><span data-stu-id="35312-110">Example 1: Get a Network Watcher</span></span>
```
Get-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="35312-111">Ottiene network watcher denominato NetworkWatcher_westcentralus nel gruppo di risorse NetworkWatcherRG.</span><span class="sxs-lookup"><span data-stu-id="35312-111">Gets the Network Watcher named NetworkWatcher_westcentralus in the resource group NetworkWatcherRG.</span></span>

### <span data-ttu-id="35312-112">Esempio 2: Elencare Network Watchers con i filtri</span><span class="sxs-lookup"><span data-stu-id="35312-112">Example 2: List Network Watchers using filtering</span></span>
```
Get-AzNetworkWatcher -Name NetworkWatcher*

Name              : NetworkWatcher_westcentralus1
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus1
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded

Name              : NetworkWatcher_westcentralus2
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus2
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="35312-113">Ottiene Network Watcher che iniziano con "NetworkWatcher"</span><span class="sxs-lookup"><span data-stu-id="35312-113">Gets the Network Watchers that start with "NetworkWatcher"</span></span>

## <span data-ttu-id="35312-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35312-114">PARAMETERS</span></span>

### <span data-ttu-id="35312-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35312-115">-DefaultProfile</span></span>
<span data-ttu-id="35312-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="35312-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35312-117">-Location</span><span class="sxs-lookup"><span data-stu-id="35312-117">-Location</span></span>
<span data-ttu-id="35312-118">Posizione del network watcher.</span><span class="sxs-lookup"><span data-stu-id="35312-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="35312-119">-Name</span><span class="sxs-lookup"><span data-stu-id="35312-119">-Name</span></span>
<span data-ttu-id="35312-120">Nome del network watcher.</span><span class="sxs-lookup"><span data-stu-id="35312-120">The network watcher name.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="35312-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35312-121">-ResourceGroupName</span></span>
<span data-ttu-id="35312-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="35312-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="35312-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35312-123">CommonParameters</span></span>
<span data-ttu-id="35312-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35312-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35312-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="35312-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35312-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="35312-126">INPUTS</span></span>

### <span data-ttu-id="35312-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="35312-127">None</span></span>

## <span data-ttu-id="35312-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="35312-128">OUTPUTS</span></span>

### <span data-ttu-id="35312-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="35312-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="35312-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="35312-130">NOTES</span></span>
<span data-ttu-id="35312-131">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, rete, rete, network watcher</span><span class="sxs-lookup"><span data-stu-id="35312-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span> 

## <span data-ttu-id="35312-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="35312-132">RELATED LINKS</span></span>

[<span data-ttu-id="35312-133">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="35312-133">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="35312-134">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="35312-134">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="35312-135">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="35312-135">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="35312-136">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="35312-136">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="35312-137">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="35312-137">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="35312-138">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="35312-138">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="35312-139">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="35312-139">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="35312-140">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="35312-140">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="35312-141">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="35312-141">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="35312-142">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="35312-142">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="35312-143">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="35312-143">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="35312-144">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="35312-144">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="35312-145">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="35312-145">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="35312-146">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="35312-146">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="35312-147">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="35312-147">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="35312-148">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="35312-148">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="35312-149">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="35312-149">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="35312-150">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="35312-150">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="35312-151">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="35312-151">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="35312-152">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="35312-152">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="35312-153">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="35312-153">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="35312-154">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="35312-154">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="35312-155">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="35312-155">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="35312-156">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="35312-156">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="35312-157">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="35312-157">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="35312-158">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="35312-158">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="35312-159">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="35312-159">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
