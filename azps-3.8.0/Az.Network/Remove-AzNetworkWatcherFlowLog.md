---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 5c8532502e4e74b94a9d0c1e252c8d1cea9ddad8
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398597"
---
# <span data-ttu-id="35b3d-101">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="35b3d-101">Remove-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="35b3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35b3d-102">SYNOPSIS</span></span>
<span data-ttu-id="35b3d-103">Elimina la risorsa del log di flusso specificata.</span><span class="sxs-lookup"><span data-stu-id="35b3d-103">Deletes the specified flow log resource.</span></span>

## <span data-ttu-id="35b3d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="35b3d-104">SYNTAX</span></span>

### <span data-ttu-id="35b3d-105">SetByName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="35b3d-105">SetByName (Default)</span></span>
```
Remove-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35b3d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="35b3d-106">SetByResource</span></span>
```
Remove-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35b3d-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="35b3d-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherFlowLog -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35b3d-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="35b3d-108">SetByResourceId</span></span>
```
Remove-AzNetworkWatcherFlowLog -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35b3d-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="35b3d-109">SetByInputObject</span></span>
```
Remove-AzNetworkWatcherFlowLog -InputObject <PSFlowLogResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35b3d-110">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="35b3d-110">DESCRIPTION</span></span>
<span data-ttu-id="35b3d-111">Elimina la risorsa del log di flusso specificata.</span><span class="sxs-lookup"><span data-stu-id="35b3d-111">Deletes the specified flow log resource.</span></span>

## <span data-ttu-id="35b3d-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="35b3d-112">EXAMPLES</span></span>

### <span data-ttu-id="35b3d-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="35b3d-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkWatcherFlowLog -Location eastus -Name pstest
```

## <span data-ttu-id="35b3d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35b3d-114">PARAMETERS</span></span>

### <span data-ttu-id="35b3d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35b3d-115">-AsJob</span></span>
<span data-ttu-id="35b3d-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="35b3d-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35b3d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35b3d-117">-DefaultProfile</span></span>
<span data-ttu-id="35b3d-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="35b3d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35b3d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35b3d-119">-InputObject</span></span>
<span data-ttu-id="35b3d-120">Oggetto log di flusso.</span><span class="sxs-lookup"><span data-stu-id="35b3d-120">Flow log object.</span></span>

```yaml
Type: PSFlowLogResource
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35b3d-121">-Location</span><span class="sxs-lookup"><span data-stu-id="35b3d-121">-Location</span></span>
<span data-ttu-id="35b3d-122">Posizione del network watcher.</span><span class="sxs-lookup"><span data-stu-id="35b3d-122">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35b3d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="35b3d-123">-Name</span></span>
<span data-ttu-id="35b3d-124">Nome del log di flusso.</span><span class="sxs-lookup"><span data-stu-id="35b3d-124">The flow log name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: FlowLogName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35b3d-125">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="35b3d-125">-NetworkWatcher</span></span>
<span data-ttu-id="35b3d-126">Risorsa Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="35b3d-126">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35b3d-127">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="35b3d-127">-NetworkWatcherName</span></span>
<span data-ttu-id="35b3d-128">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="35b3d-128">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35b3d-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35b3d-129">-PassThru</span></span>
<span data-ttu-id="35b3d-130">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="35b3d-130">{{ Fill PassThru Description }}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35b3d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35b3d-131">-ResourceGroupName</span></span>
<span data-ttu-id="35b3d-132">Nome del gruppo di risorse Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="35b3d-132">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35b3d-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35b3d-133">-ResourceId</span></span>
<span data-ttu-id="35b3d-134">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="35b3d-134">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35b3d-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35b3d-135">-Confirm</span></span>
<span data-ttu-id="35b3d-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35b3d-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35b3d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35b3d-137">-WhatIf</span></span>
<span data-ttu-id="35b3d-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35b3d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35b3d-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35b3d-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35b3d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35b3d-140">CommonParameters</span></span>
<span data-ttu-id="35b3d-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35b3d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35b3d-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="35b3d-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35b3d-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="35b3d-143">INPUTS</span></span>

### <span data-ttu-id="35b3d-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="35b3d-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="35b3d-145">System.String</span><span class="sxs-lookup"><span data-stu-id="35b3d-145">System.String</span></span>

### <span data-ttu-id="35b3d-146">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="35b3d-146">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="35b3d-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="35b3d-147">OUTPUTS</span></span>

### <span data-ttu-id="35b3d-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="35b3d-148">System.Boolean</span></span>

## <span data-ttu-id="35b3d-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="35b3d-149">NOTES</span></span>

## <span data-ttu-id="35b3d-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="35b3d-150">RELATED LINKS</span></span>

[<span data-ttu-id="35b3d-151">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="35b3d-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="35b3d-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="35b3d-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="35b3d-153">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="35b3d-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="35b3d-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="35b3d-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="35b3d-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="35b3d-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="35b3d-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="35b3d-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="35b3d-157">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="35b3d-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="35b3d-158">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="35b3d-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="35b3d-159">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="35b3d-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="35b3d-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="35b3d-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="35b3d-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="35b3d-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="35b3d-162">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="35b3d-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="35b3d-163">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="35b3d-163">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="35b3d-164">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="35b3d-164">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="35b3d-165">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="35b3d-165">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="35b3d-166">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="35b3d-166">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="35b3d-167">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="35b3d-167">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="35b3d-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="35b3d-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="35b3d-169">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="35b3d-169">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="35b3d-170">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="35b3d-170">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="35b3d-171">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="35b3d-171">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="35b3d-172">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="35b3d-172">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="35b3d-173">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="35b3d-173">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="35b3d-174">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="35b3d-174">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="35b3d-175">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="35b3d-175">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="35b3d-176">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="35b3d-176">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="35b3d-177">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="35b3d-177">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="35b3d-178">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="35b3d-178">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="35b3d-179">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="35b3d-179">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="35b3d-180">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="35b3d-180">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog.md)
