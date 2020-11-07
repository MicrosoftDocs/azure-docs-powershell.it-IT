---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcher.md
ms.openlocfilehash: f098e0d776ab115211fb562ed4889502995ffdd7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688390"
---
# <span data-ttu-id="5e81a-101">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5e81a-101">New-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="5e81a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5e81a-102">SYNOPSIS</span></span>
<span data-ttu-id="5e81a-103">Crea una nuova risorsa di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="5e81a-103">Creates a new Network Watcher resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e81a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5e81a-104">SYNTAX</span></span>

```
New-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e81a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e81a-105">DESCRIPTION</span></span>
<span data-ttu-id="5e81a-106">Il cmdlet New-AzureRmNetworkWatcher crea una nuova risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="5e81a-106">The New-AzureRmNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="5e81a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5e81a-107">EXAMPLES</span></span>

### <span data-ttu-id="5e81a-108">Esempio 1: creare un Watcher di rete</span><span class="sxs-lookup"><span data-stu-id="5e81a-108">Example 1: Create a Network Watcher</span></span>
```
New-AzureRmResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"7cf1f2fe-8445-4aa7-9bf5-c15347282c39"
Location          : westcentralus
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="5e81a-109">Questo esempio crea un nuovo Watcher di rete all'interno di un gruppo di risorse appena creato.</span><span class="sxs-lookup"><span data-stu-id="5e81a-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="5e81a-110">Tieni presente che è possibile creare un solo Watcher di rete per ogni area di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="5e81a-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="5e81a-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5e81a-111">PARAMETERS</span></span>

### <span data-ttu-id="5e81a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e81a-112">-DefaultProfile</span></span>
<span data-ttu-id="5e81a-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5e81a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e81a-114">-Posizione</span><span class="sxs-lookup"><span data-stu-id="5e81a-114">-Location</span></span>
<span data-ttu-id="5e81a-115">Posizione.</span><span class="sxs-lookup"><span data-stu-id="5e81a-115">Location.</span></span>

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

### <span data-ttu-id="5e81a-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="5e81a-116">-Name</span></span>
<span data-ttu-id="5e81a-117">Nome del Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="5e81a-117">The network watcher name.</span></span>

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

### <span data-ttu-id="5e81a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e81a-118">-ResourceGroupName</span></span>
<span data-ttu-id="5e81a-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5e81a-119">The resource group name.</span></span>

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

### <span data-ttu-id="5e81a-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="5e81a-120">-Tag</span></span>
<span data-ttu-id="5e81a-121">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="5e81a-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5e81a-122">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="5e81a-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5e81a-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5e81a-123">-Confirm</span></span>
<span data-ttu-id="5e81a-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e81a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e81a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e81a-125">-WhatIf</span></span>
<span data-ttu-id="5e81a-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5e81a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e81a-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5e81a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e81a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e81a-128">CommonParameters</span></span>
<span data-ttu-id="5e81a-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e81a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e81a-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e81a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e81a-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5e81a-131">INPUTS</span></span>

### <span data-ttu-id="5e81a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="5e81a-132">System.String</span></span>

### <span data-ttu-id="5e81a-133">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5e81a-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5e81a-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5e81a-134">OUTPUTS</span></span>

### <span data-ttu-id="5e81a-135">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5e81a-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="5e81a-136">Note</span><span class="sxs-lookup"><span data-stu-id="5e81a-136">NOTES</span></span>
<span data-ttu-id="5e81a-137">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher</span><span class="sxs-lookup"><span data-stu-id="5e81a-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="5e81a-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5e81a-138">RELATED LINKS</span></span>

[<span data-ttu-id="5e81a-139">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5e81a-139">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="5e81a-140">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5e81a-140">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="5e81a-141">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5e81a-141">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="5e81a-142">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="5e81a-142">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="5e81a-143">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="5e81a-143">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="5e81a-144">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="5e81a-144">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="5e81a-145">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="5e81a-145">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="5e81a-146">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5e81a-146">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5e81a-147">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="5e81a-147">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="5e81a-148">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5e81a-148">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5e81a-149">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5e81a-149">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5e81a-150">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5e81a-150">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5e81a-151">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="5e81a-151">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="5e81a-152">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="5e81a-152">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="5e81a-153">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="5e81a-153">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="5e81a-154">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5e81a-154">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5e81a-155">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5e81a-155">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5e81a-156">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5e81a-156">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5e81a-157">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="5e81a-157">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="5e81a-158">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5e81a-158">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5e81a-159">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5e81a-159">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5e81a-160">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="5e81a-160">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="5e81a-161">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="5e81a-161">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="5e81a-162">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="5e81a-162">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="5e81a-163">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="5e81a-163">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="5e81a-164">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="5e81a-164">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="5e81a-165">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5e81a-165">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
