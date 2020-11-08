---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
ms.openlocfilehash: cce361870f6dc65f644264e52b331c209177668f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188409"
---
# <span data-ttu-id="26e30-101">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="26e30-101">Remove-AzNetworkWatcher</span></span>

## <span data-ttu-id="26e30-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="26e30-102">SYNOPSIS</span></span>
<span data-ttu-id="26e30-103">Rimuove un Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="26e30-103">Removes a Network Watcher.</span></span>

## <span data-ttu-id="26e30-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="26e30-104">SYNTAX</span></span>

### <span data-ttu-id="26e30-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="26e30-105">SetByResource</span></span>
```
Remove-AzNetworkWatcher -NetworkWatcher <PSNetworkWatcher> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26e30-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="26e30-106">SetByName</span></span>
```
Remove-AzNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26e30-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="26e30-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcher -Location <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26e30-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26e30-108">DESCRIPTION</span></span>
<span data-ttu-id="26e30-109">Il cmdlet Remove-AzNetworkWatcher consente di rimuovere una risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="26e30-109">The Remove-AzNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="26e30-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="26e30-110">EXAMPLES</span></span>

### <span data-ttu-id="26e30-111">Esempio 1: creare ed eliminare un Watcher di rete</span><span class="sxs-lookup"><span data-stu-id="26e30-111">Example 1: Create and delete a Network Watcher</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="26e30-112">Questo esempio crea un Watcher di rete in un gruppo di risorse e quindi lo elimina immediatamente.</span><span class="sxs-lookup"><span data-stu-id="26e30-112">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="26e30-113">Tieni presente che è possibile creare un solo Watcher di rete per ogni area di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="26e30-113">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="26e30-114">Per eliminare la richiesta quando si elimina la rete virtuale, usare il contrassegno-forza.</span><span class="sxs-lookup"><span data-stu-id="26e30-114">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="26e30-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="26e30-115">PARAMETERS</span></span>

### <span data-ttu-id="26e30-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="26e30-116">-AsJob</span></span>
<span data-ttu-id="26e30-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="26e30-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="26e30-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26e30-118">-DefaultProfile</span></span>
<span data-ttu-id="26e30-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="26e30-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26e30-120">-Posizione</span><span class="sxs-lookup"><span data-stu-id="26e30-120">-Location</span></span>
<span data-ttu-id="26e30-121">Posizione del monitoraggio della rete.</span><span class="sxs-lookup"><span data-stu-id="26e30-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="26e30-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="26e30-122">-Name</span></span>
<span data-ttu-id="26e30-123">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="26e30-123">The resource name.</span></span>

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

### <span data-ttu-id="26e30-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="26e30-124">-NetworkWatcher</span></span>
<span data-ttu-id="26e30-125">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="26e30-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="26e30-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26e30-126">-PassThru</span></span>
<span data-ttu-id="26e30-127">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="26e30-127">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="26e30-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26e30-128">-ResourceGroupName</span></span>
<span data-ttu-id="26e30-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="26e30-129">The resource group name.</span></span>

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

### <span data-ttu-id="26e30-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="26e30-130">-Confirm</span></span>
<span data-ttu-id="26e30-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26e30-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26e30-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26e30-132">-WhatIf</span></span>
<span data-ttu-id="26e30-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="26e30-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26e30-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="26e30-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26e30-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26e30-135">CommonParameters</span></span>
<span data-ttu-id="26e30-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26e30-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26e30-137">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26e30-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26e30-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="26e30-138">INPUTS</span></span>

### <span data-ttu-id="26e30-139">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="26e30-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="26e30-140">System. String</span><span class="sxs-lookup"><span data-stu-id="26e30-140">System.String</span></span>

## <span data-ttu-id="26e30-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="26e30-141">OUTPUTS</span></span>

### <span data-ttu-id="26e30-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="26e30-142">System.Boolean</span></span>

## <span data-ttu-id="26e30-143">Note</span><span class="sxs-lookup"><span data-stu-id="26e30-143">NOTES</span></span>
<span data-ttu-id="26e30-144">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher</span><span class="sxs-lookup"><span data-stu-id="26e30-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="26e30-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="26e30-145">RELATED LINKS</span></span>

[<span data-ttu-id="26e30-146">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="26e30-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="26e30-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="26e30-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="26e30-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="26e30-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="26e30-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="26e30-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="26e30-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="26e30-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="26e30-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="26e30-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="26e30-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="26e30-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="26e30-153">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="26e30-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="26e30-154">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="26e30-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="26e30-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="26e30-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="26e30-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="26e30-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="26e30-157">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="26e30-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="26e30-158">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="26e30-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="26e30-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="26e30-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="26e30-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="26e30-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="26e30-161">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="26e30-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="26e30-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="26e30-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="26e30-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="26e30-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="26e30-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="26e30-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="26e30-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="26e30-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="26e30-166">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="26e30-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="26e30-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="26e30-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="26e30-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="26e30-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="26e30-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="26e30-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="26e30-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="26e30-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="26e30-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="26e30-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="26e30-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="26e30-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
