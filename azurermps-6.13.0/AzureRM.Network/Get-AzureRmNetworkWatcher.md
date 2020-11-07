---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcher.md
ms.openlocfilehash: c8417f8a1f1d16e00629d06a75be2802801afd2e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688552"
---
# <span data-ttu-id="5eeb9-101">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5eeb9-101">Get-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="5eeb9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5eeb9-102">SYNOPSIS</span></span>
<span data-ttu-id="5eeb9-103">Ottiene le proprietà di un Watcher di rete</span><span class="sxs-lookup"><span data-stu-id="5eeb9-103">Gets the properties of a Network Watcher</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5eeb9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5eeb9-104">SYNTAX</span></span>

### <span data-ttu-id="5eeb9-105">Ottieni</span><span class="sxs-lookup"><span data-stu-id="5eeb9-105">Get</span></span>
```
Get-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5eeb9-106">Elenco</span><span class="sxs-lookup"><span data-stu-id="5eeb9-106">List</span></span>
```
Get-AzureRmNetworkWatcher [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5eeb9-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="5eeb9-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5eeb9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5eeb9-108">DESCRIPTION</span></span>
<span data-ttu-id="5eeb9-109">Il cmdlet Get-AzureRmNetworkWatcher ottiene una o più risorse di monitoraggio di rete Azure.</span><span class="sxs-lookup"><span data-stu-id="5eeb9-109">The Get-AzureRmNetworkWatcher cmdlet gets one or more Azure Network Watcher resources.</span></span>

## <span data-ttu-id="5eeb9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5eeb9-110">EXAMPLES</span></span>

### <span data-ttu-id="5eeb9-111">Esempio 1: ottenere un Watcher di rete</span><span class="sxs-lookup"><span data-stu-id="5eeb9-111">Example 1: Get a Network Watcher</span></span>
```
Get-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="5eeb9-112">Ottiene il monitoraggio della rete denominato NetworkWatcher_westcentralus nel gruppo di risorse NetworkWatcherRG.</span><span class="sxs-lookup"><span data-stu-id="5eeb9-112">Gets the Network Watcher named NetworkWatcher_westcentralus in the resource group NetworkWatcherRG.</span></span>

## <span data-ttu-id="5eeb9-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5eeb9-113">PARAMETERS</span></span>

### <span data-ttu-id="5eeb9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5eeb9-114">-DefaultProfile</span></span>
<span data-ttu-id="5eeb9-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5eeb9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5eeb9-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="5eeb9-116">-Location</span></span>
<span data-ttu-id="5eeb9-117">Posizione del monitoraggio della rete.</span><span class="sxs-lookup"><span data-stu-id="5eeb9-117">Location of the network watcher.</span></span>

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

### <span data-ttu-id="5eeb9-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="5eeb9-118">-Name</span></span>
<span data-ttu-id="5eeb9-119">Nome del Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="5eeb9-119">The network watcher name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eeb9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5eeb9-120">-ResourceGroupName</span></span>
<span data-ttu-id="5eeb9-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5eeb9-121">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eeb9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eeb9-122">CommonParameters</span></span>
<span data-ttu-id="5eeb9-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5eeb9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eeb9-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5eeb9-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eeb9-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5eeb9-125">INPUTS</span></span>

### <span data-ttu-id="5eeb9-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5eeb9-126">None</span></span>

## <span data-ttu-id="5eeb9-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5eeb9-127">OUTPUTS</span></span>

### <span data-ttu-id="5eeb9-128">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5eeb9-128">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="5eeb9-129">Note</span><span class="sxs-lookup"><span data-stu-id="5eeb9-129">NOTES</span></span>
<span data-ttu-id="5eeb9-130">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher</span><span class="sxs-lookup"><span data-stu-id="5eeb9-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span> 

## <span data-ttu-id="5eeb9-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5eeb9-131">RELATED LINKS</span></span>

[<span data-ttu-id="5eeb9-132">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5eeb9-132">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="5eeb9-133">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5eeb9-133">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="5eeb9-134">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5eeb9-134">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="5eeb9-135">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="5eeb9-135">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="5eeb9-136">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="5eeb9-136">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="5eeb9-137">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="5eeb9-137">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="5eeb9-138">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="5eeb9-138">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="5eeb9-139">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5eeb9-139">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5eeb9-140">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="5eeb9-140">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="5eeb9-141">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5eeb9-141">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5eeb9-142">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5eeb9-142">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5eeb9-143">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5eeb9-143">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5eeb9-144">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="5eeb9-144">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="5eeb9-145">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="5eeb9-145">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="5eeb9-146">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="5eeb9-146">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="5eeb9-147">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5eeb9-147">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5eeb9-148">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5eeb9-148">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5eeb9-149">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5eeb9-149">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5eeb9-150">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="5eeb9-150">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="5eeb9-151">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5eeb9-151">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5eeb9-152">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5eeb9-152">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5eeb9-153">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="5eeb9-153">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="5eeb9-154">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="5eeb9-154">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="5eeb9-155">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="5eeb9-155">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="5eeb9-156">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="5eeb9-156">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="5eeb9-157">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="5eeb9-157">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="5eeb9-158">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5eeb9-158">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
