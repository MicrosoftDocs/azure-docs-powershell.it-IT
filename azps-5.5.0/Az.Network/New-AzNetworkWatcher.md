---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
ms.openlocfilehash: dbc1f3e942a95adf0cb56721ec1a2666da9b9188
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100414272"
---
# <span data-ttu-id="8dfaf-101">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8dfaf-101">New-AzNetworkWatcher</span></span>

## <span data-ttu-id="8dfaf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8dfaf-102">SYNOPSIS</span></span>
<span data-ttu-id="8dfaf-103">Crea una nuova risorsa Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="8dfaf-103">Creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="8dfaf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8dfaf-104">SYNTAX</span></span>

```
New-AzNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dfaf-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8dfaf-105">DESCRIPTION</span></span>
<span data-ttu-id="8dfaf-106">Il cmdlet New-AzNetworkWatcher crea una nuova risorsa Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="8dfaf-106">The New-AzNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="8dfaf-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8dfaf-107">EXAMPLES</span></span>

### <span data-ttu-id="8dfaf-108">Esempio 1: Creare un Network Watcher</span><span class="sxs-lookup"><span data-stu-id="8dfaf-108">Example 1: Create a Network Watcher</span></span>
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

<span data-ttu-id="8dfaf-109">Questo esempio crea un nuovo Network Watcher all'interno di un gruppo di risorse appena creato.</span><span class="sxs-lookup"><span data-stu-id="8dfaf-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="8dfaf-110">Si noti che per ogni abbonamento è possibile creare un solo Network Watcher per ogni area geografica.</span><span class="sxs-lookup"><span data-stu-id="8dfaf-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="8dfaf-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8dfaf-111">PARAMETERS</span></span>

### <span data-ttu-id="8dfaf-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dfaf-112">-DefaultProfile</span></span>
<span data-ttu-id="8dfaf-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8dfaf-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8dfaf-114">-Location</span><span class="sxs-lookup"><span data-stu-id="8dfaf-114">-Location</span></span>
<span data-ttu-id="8dfaf-115">Posizione.</span><span class="sxs-lookup"><span data-stu-id="8dfaf-115">Location.</span></span>

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

### <span data-ttu-id="8dfaf-116">-Name</span><span class="sxs-lookup"><span data-stu-id="8dfaf-116">-Name</span></span>
<span data-ttu-id="8dfaf-117">Nome del network watcher.</span><span class="sxs-lookup"><span data-stu-id="8dfaf-117">The network watcher name.</span></span>

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

### <span data-ttu-id="8dfaf-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dfaf-118">-ResourceGroupName</span></span>
<span data-ttu-id="8dfaf-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8dfaf-119">The resource group name.</span></span>

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

### <span data-ttu-id="8dfaf-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="8dfaf-120">-Tag</span></span>
<span data-ttu-id="8dfaf-121">Coppie chiave-valore sotto forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="8dfaf-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8dfaf-122">Ad esempio: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="8dfaf-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="8dfaf-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8dfaf-123">-Confirm</span></span>
<span data-ttu-id="8dfaf-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8dfaf-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dfaf-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dfaf-125">-WhatIf</span></span>
<span data-ttu-id="8dfaf-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8dfaf-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8dfaf-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8dfaf-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dfaf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dfaf-128">CommonParameters</span></span>
<span data-ttu-id="8dfaf-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dfaf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dfaf-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8dfaf-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dfaf-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="8dfaf-131">INPUTS</span></span>

### <span data-ttu-id="8dfaf-132">System.String</span><span class="sxs-lookup"><span data-stu-id="8dfaf-132">System.String</span></span>

### <span data-ttu-id="8dfaf-133">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="8dfaf-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8dfaf-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8dfaf-134">OUTPUTS</span></span>

### <span data-ttu-id="8dfaf-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8dfaf-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="8dfaf-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="8dfaf-136">NOTES</span></span>
<span data-ttu-id="8dfaf-137">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, rete, rete, network watcher</span><span class="sxs-lookup"><span data-stu-id="8dfaf-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="8dfaf-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8dfaf-138">RELATED LINKS</span></span>

[<span data-ttu-id="8dfaf-139">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8dfaf-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="8dfaf-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8dfaf-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="8dfaf-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8dfaf-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="8dfaf-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="8dfaf-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="8dfaf-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="8dfaf-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="8dfaf-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="8dfaf-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="8dfaf-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="8dfaf-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="8dfaf-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8dfaf-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8dfaf-147">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="8dfaf-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="8dfaf-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8dfaf-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8dfaf-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8dfaf-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8dfaf-150">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8dfaf-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8dfaf-151">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="8dfaf-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="8dfaf-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="8dfaf-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="8dfaf-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="8dfaf-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="8dfaf-154">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8dfaf-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8dfaf-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8dfaf-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8dfaf-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8dfaf-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8dfaf-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="8dfaf-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="8dfaf-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8dfaf-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8dfaf-159">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8dfaf-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8dfaf-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="8dfaf-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="8dfaf-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="8dfaf-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="8dfaf-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="8dfaf-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="8dfaf-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="8dfaf-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="8dfaf-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="8dfaf-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="8dfaf-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8dfaf-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
