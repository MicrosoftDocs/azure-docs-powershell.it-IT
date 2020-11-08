---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
ms.openlocfilehash: 8253e43052203d4f5ba844cec02ec3b2af592b1d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020015"
---
# <span data-ttu-id="0e711-101">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0e711-101">New-AzNetworkWatcher</span></span>

## <span data-ttu-id="0e711-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0e711-102">SYNOPSIS</span></span>
<span data-ttu-id="0e711-103">Crea una nuova risorsa di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="0e711-103">Creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="0e711-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0e711-104">SYNTAX</span></span>

```
New-AzNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e711-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0e711-105">DESCRIPTION</span></span>
<span data-ttu-id="0e711-106">Il cmdlet New-AzNetworkWatcher crea una nuova risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="0e711-106">The New-AzNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="0e711-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0e711-107">EXAMPLES</span></span>

### <span data-ttu-id="0e711-108">Esempio 1: creare un Watcher di rete</span><span class="sxs-lookup"><span data-stu-id="0e711-108">Example 1: Create a Network Watcher</span></span>
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

<span data-ttu-id="0e711-109">Questo esempio crea un nuovo Watcher di rete all'interno di un gruppo di risorse appena creato.</span><span class="sxs-lookup"><span data-stu-id="0e711-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="0e711-110">Tieni presente che è possibile creare un solo Watcher di rete per ogni area di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="0e711-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="0e711-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0e711-111">PARAMETERS</span></span>

### <span data-ttu-id="0e711-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e711-112">-DefaultProfile</span></span>
<span data-ttu-id="0e711-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0e711-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e711-114">-Posizione</span><span class="sxs-lookup"><span data-stu-id="0e711-114">-Location</span></span>
<span data-ttu-id="0e711-115">Posizione.</span><span class="sxs-lookup"><span data-stu-id="0e711-115">Location.</span></span>

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

### <span data-ttu-id="0e711-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="0e711-116">-Name</span></span>
<span data-ttu-id="0e711-117">Nome del Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="0e711-117">The network watcher name.</span></span>

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

### <span data-ttu-id="0e711-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e711-118">-ResourceGroupName</span></span>
<span data-ttu-id="0e711-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0e711-119">The resource group name.</span></span>

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

### <span data-ttu-id="0e711-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="0e711-120">-Tag</span></span>
<span data-ttu-id="0e711-121">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="0e711-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0e711-122">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="0e711-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="0e711-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0e711-123">-Confirm</span></span>
<span data-ttu-id="0e711-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e711-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e711-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e711-125">-WhatIf</span></span>
<span data-ttu-id="0e711-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0e711-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e711-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0e711-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e711-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e711-128">CommonParameters</span></span>
<span data-ttu-id="0e711-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e711-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e711-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e711-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e711-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0e711-131">INPUTS</span></span>

### <span data-ttu-id="0e711-132">System. String</span><span class="sxs-lookup"><span data-stu-id="0e711-132">System.String</span></span>

### <span data-ttu-id="0e711-133">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0e711-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0e711-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0e711-134">OUTPUTS</span></span>

### <span data-ttu-id="0e711-135">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0e711-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="0e711-136">Note</span><span class="sxs-lookup"><span data-stu-id="0e711-136">NOTES</span></span>
<span data-ttu-id="0e711-137">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher</span><span class="sxs-lookup"><span data-stu-id="0e711-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="0e711-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0e711-138">RELATED LINKS</span></span>

[<span data-ttu-id="0e711-139">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0e711-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="0e711-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0e711-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="0e711-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0e711-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="0e711-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="0e711-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="0e711-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="0e711-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="0e711-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="0e711-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="0e711-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="0e711-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="0e711-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0e711-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0e711-147">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="0e711-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="0e711-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0e711-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0e711-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0e711-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0e711-150">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0e711-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0e711-151">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e711-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="0e711-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="0e711-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="0e711-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="0e711-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="0e711-154">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0e711-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0e711-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0e711-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0e711-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0e711-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0e711-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="0e711-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="0e711-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0e711-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0e711-159">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0e711-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0e711-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="0e711-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="0e711-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="0e711-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="0e711-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="0e711-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="0e711-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="0e711-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="0e711-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="0e711-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="0e711-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0e711-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
