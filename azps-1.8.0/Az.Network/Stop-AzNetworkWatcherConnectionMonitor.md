---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: ceb03c58c7f7c3983f89073b5bad2428a32b7934
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677897"
---
# <span data-ttu-id="084ad-101">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="084ad-101">Stop-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="084ad-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="084ad-102">SYNOPSIS</span></span>
<span data-ttu-id="084ad-103">Arrestare un monitor di connessione</span><span class="sxs-lookup"><span data-stu-id="084ad-103">Stop a connection monitor</span></span>

## <span data-ttu-id="084ad-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="084ad-104">SYNTAX</span></span>

### <span data-ttu-id="084ad-105">SetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="084ad-105">SetByName (Default)</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="084ad-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="084ad-106">SetByResource</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="084ad-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="084ad-107">SetByLocation</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="084ad-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="084ad-108">SetByResourceId</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="084ad-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="084ad-109">SetByInputObject</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="084ad-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="084ad-110">DESCRIPTION</span></span>
<span data-ttu-id="084ad-111">Il cmdlet Stop-AzNetworkWatcherConnectionMonitor arresta il monitor di connessione specificato.</span><span class="sxs-lookup"><span data-stu-id="084ad-111">The Stop-AzNetworkWatcherConnectionMonitor cmdlet stops the specified connection monitor.</span></span>

## <span data-ttu-id="084ad-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="084ad-112">EXAMPLES</span></span>

### <span data-ttu-id="084ad-113">Esempio 1: arrestare un monitor di connessione</span><span class="sxs-lookup"><span data-stu-id="084ad-113">Example 1: Stop a connection monitor</span></span>
```
PS C:\> Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm
```

<span data-ttu-id="084ad-114">In questo esempio interrompiamo il monitoraggio delle connessioni specificato per nome e Network Watcher</span><span class="sxs-lookup"><span data-stu-id="084ad-114">In this example we stop connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="084ad-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="084ad-115">PARAMETERS</span></span>

### <span data-ttu-id="084ad-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="084ad-116">-AsJob</span></span>
<span data-ttu-id="084ad-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="084ad-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="084ad-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="084ad-118">-DefaultProfile</span></span>
<span data-ttu-id="084ad-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="084ad-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="084ad-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="084ad-120">-InputObject</span></span>
<span data-ttu-id="084ad-121">Oggetto monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="084ad-121">Connection monitor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="084ad-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="084ad-122">-Location</span></span>
<span data-ttu-id="084ad-123">Posizione del monitoraggio della rete.</span><span class="sxs-lookup"><span data-stu-id="084ad-123">Location of the network watcher.</span></span>

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

### <span data-ttu-id="084ad-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="084ad-124">-Name</span></span>
<span data-ttu-id="084ad-125">Nome del monitor della connessione.</span><span class="sxs-lookup"><span data-stu-id="084ad-125">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="084ad-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="084ad-126">-NetworkWatcher</span></span>
<span data-ttu-id="084ad-127">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="084ad-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="084ad-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="084ad-128">-NetworkWatcherName</span></span>
<span data-ttu-id="084ad-129">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="084ad-129">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="084ad-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="084ad-130">-PassThru</span></span>
<span data-ttu-id="084ad-131">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="084ad-131">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="084ad-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="084ad-132">-ResourceGroupName</span></span>
<span data-ttu-id="084ad-133">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="084ad-133">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="084ad-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="084ad-134">-ResourceId</span></span>
<span data-ttu-id="084ad-135">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="084ad-135">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="084ad-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="084ad-136">-Confirm</span></span>
<span data-ttu-id="084ad-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="084ad-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="084ad-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="084ad-138">-WhatIf</span></span>
<span data-ttu-id="084ad-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="084ad-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="084ad-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="084ad-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="084ad-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="084ad-141">CommonParameters</span></span>
<span data-ttu-id="084ad-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="084ad-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="084ad-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="084ad-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="084ad-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="084ad-144">INPUTS</span></span>

### <span data-ttu-id="084ad-145">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="084ad-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="084ad-146">System. String</span><span class="sxs-lookup"><span data-stu-id="084ad-146">System.String</span></span>

### <span data-ttu-id="084ad-147">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="084ad-147">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="084ad-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="084ad-148">OUTPUTS</span></span>

### <span data-ttu-id="084ad-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="084ad-149">System.Boolean</span></span>

## <span data-ttu-id="084ad-150">Note</span><span class="sxs-lookup"><span data-stu-id="084ad-150">NOTES</span></span>
<span data-ttu-id="084ad-151">Parole chiave: Azure, azurerm, ARM, Resource, Connectivity, Management, Manager, Network, networking, Network Watcher, Connection Monitor</span><span class="sxs-lookup"><span data-stu-id="084ad-151">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="084ad-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="084ad-152">RELATED LINKS</span></span>

[<span data-ttu-id="084ad-153">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="084ad-153">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="084ad-154">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="084ad-154">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="084ad-155">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="084ad-155">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="084ad-156">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="084ad-156">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="084ad-157">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="084ad-157">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="084ad-158">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="084ad-158">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="084ad-159">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="084ad-159">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="084ad-160">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="084ad-160">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="084ad-161">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="084ad-161">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="084ad-162">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="084ad-162">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="084ad-163">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="084ad-163">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="084ad-164">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="084ad-164">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="084ad-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="084ad-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="084ad-166">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="084ad-166">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="084ad-167">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="084ad-167">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="084ad-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="084ad-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="084ad-169">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="084ad-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="084ad-170">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="084ad-170">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="084ad-171">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="084ad-171">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="084ad-172">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="084ad-172">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="084ad-173">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="084ad-173">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="084ad-174">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="084ad-174">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="084ad-175">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="084ad-175">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="084ad-176">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="084ad-176">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="084ad-177">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="084ad-177">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="084ad-178">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="084ad-178">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="084ad-179">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="084ad-179">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
