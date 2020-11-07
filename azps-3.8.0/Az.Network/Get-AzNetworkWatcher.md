---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcher.md
ms.openlocfilehash: c1ea29572bb42bea0c7e64c3ec818fe2f2d0ed0f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864655"
---
# <span data-ttu-id="f987e-101">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f987e-101">Get-AzNetworkWatcher</span></span>

## <span data-ttu-id="f987e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f987e-102">SYNOPSIS</span></span>
<span data-ttu-id="f987e-103">Ottiene le proprietà di un Watcher di rete</span><span class="sxs-lookup"><span data-stu-id="f987e-103">Gets the properties of a Network Watcher</span></span>

## <span data-ttu-id="f987e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f987e-104">SYNTAX</span></span>

### <span data-ttu-id="f987e-105">Elenco</span><span class="sxs-lookup"><span data-stu-id="f987e-105">List</span></span>
```
Get-AzNetworkWatcher [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f987e-106">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="f987e-106">SetByLocation</span></span>
```
Get-AzNetworkWatcher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f987e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f987e-107">DESCRIPTION</span></span>
<span data-ttu-id="f987e-108">Il cmdlet Get-AzNetworkWatcher ottiene una o più risorse di monitoraggio di rete Azure.</span><span class="sxs-lookup"><span data-stu-id="f987e-108">The Get-AzNetworkWatcher cmdlet gets one or more Azure Network Watcher resources.</span></span>

## <span data-ttu-id="f987e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f987e-109">EXAMPLES</span></span>

### <span data-ttu-id="f987e-110">Esempio 1: ottenere un Watcher di rete</span><span class="sxs-lookup"><span data-stu-id="f987e-110">Example 1: Get a Network Watcher</span></span>
```
Get-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="f987e-111">Ottiene il monitoraggio della rete denominato NetworkWatcher_westcentralus nel gruppo di risorse NetworkWatcherRG.</span><span class="sxs-lookup"><span data-stu-id="f987e-111">Gets the Network Watcher named NetworkWatcher_westcentralus in the resource group NetworkWatcherRG.</span></span>

### <span data-ttu-id="f987e-112">Esempio 2: elencare gli osservatori di rete usando il filtro</span><span class="sxs-lookup"><span data-stu-id="f987e-112">Example 2: List Network Watchers using filtering</span></span>
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

<span data-ttu-id="f987e-113">Ottiene gli osservatori di rete che iniziano con "NetworkWatcher"</span><span class="sxs-lookup"><span data-stu-id="f987e-113">Gets the Network Watchers that start with "NetworkWatcher"</span></span>

## <span data-ttu-id="f987e-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f987e-114">PARAMETERS</span></span>

### <span data-ttu-id="f987e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f987e-115">-DefaultProfile</span></span>
<span data-ttu-id="f987e-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f987e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f987e-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="f987e-117">-Location</span></span>
<span data-ttu-id="f987e-118">Posizione del monitoraggio della rete.</span><span class="sxs-lookup"><span data-stu-id="f987e-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="f987e-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="f987e-119">-Name</span></span>
<span data-ttu-id="f987e-120">Nome del Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="f987e-120">The network watcher name.</span></span>

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

### <span data-ttu-id="f987e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f987e-121">-ResourceGroupName</span></span>
<span data-ttu-id="f987e-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f987e-122">The resource group name.</span></span>

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

### <span data-ttu-id="f987e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f987e-123">CommonParameters</span></span>
<span data-ttu-id="f987e-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f987e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f987e-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f987e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f987e-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f987e-126">INPUTS</span></span>

### <span data-ttu-id="f987e-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f987e-127">None</span></span>

## <span data-ttu-id="f987e-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f987e-128">OUTPUTS</span></span>

### <span data-ttu-id="f987e-129">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f987e-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="f987e-130">Note</span><span class="sxs-lookup"><span data-stu-id="f987e-130">NOTES</span></span>
<span data-ttu-id="f987e-131">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher</span><span class="sxs-lookup"><span data-stu-id="f987e-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span> 

## <span data-ttu-id="f987e-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f987e-132">RELATED LINKS</span></span>

[<span data-ttu-id="f987e-133">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f987e-133">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="f987e-134">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f987e-134">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="f987e-135">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f987e-135">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="f987e-136">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="f987e-136">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="f987e-137">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="f987e-137">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="f987e-138">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="f987e-138">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="f987e-139">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="f987e-139">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="f987e-140">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f987e-140">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f987e-141">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f987e-141">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="f987e-142">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f987e-142">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f987e-143">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f987e-143">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f987e-144">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f987e-144">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f987e-145">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="f987e-145">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="f987e-146">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="f987e-146">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="f987e-147">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="f987e-147">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="f987e-148">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f987e-148">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f987e-149">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f987e-149">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f987e-150">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f987e-150">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f987e-151">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="f987e-151">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="f987e-152">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f987e-152">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f987e-153">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f987e-153">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f987e-154">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="f987e-154">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="f987e-155">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="f987e-155">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="f987e-156">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="f987e-156">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="f987e-157">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="f987e-157">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="f987e-158">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="f987e-158">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="f987e-159">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f987e-159">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
