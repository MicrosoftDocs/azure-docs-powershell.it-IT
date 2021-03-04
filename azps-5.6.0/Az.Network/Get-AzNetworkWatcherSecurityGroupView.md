---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: 3d2fa4a0d5c98ae468466780cffc2ea6439343f8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954366"
---
# <span data-ttu-id="acc90-101">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="acc90-101">Get-AzNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="acc90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acc90-102">SYNOPSIS</span></span>
<span data-ttu-id="acc90-103">Visualizzare le regole configurate ed efficaci del gruppo di sicurezza di rete applicate in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="acc90-103">View the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="acc90-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="acc90-104">SYNTAX</span></span>

### <span data-ttu-id="acc90-105">SetByResource (Default)</span><span class="sxs-lookup"><span data-stu-id="acc90-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acc90-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="acc90-106">SetByName</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acc90-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="acc90-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -Location <String> -TargetVirtualMachineId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acc90-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="acc90-108">DESCRIPTION</span></span>
<span data-ttu-id="acc90-109">LGet-AzNetworkWatcherSecurityGroupView consente di visualizzare le regole configurate ed effettive del gruppo di sicurezza di rete applicate in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="acc90-109">The Get-AzNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="acc90-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="acc90-110">EXAMPLES</span></span>

### <span data-ttu-id="acc90-111">Esempio 1: Effettuare una chiamata di visualizzazione del gruppo di sicurezza in una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="acc90-111">Example 1: Make a Security Group View call on a VM</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="acc90-112">Nell'esempio precedente si ottiene prima network watcher locale, poi una macchina virtuale nell'area geografica.</span><span class="sxs-lookup"><span data-stu-id="acc90-112">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="acc90-113">Verrà quindi creata una chiamata di visualizzazione del gruppo di sicurezza nella macchina virtuale specificata.</span><span class="sxs-lookup"><span data-stu-id="acc90-113">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="acc90-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="acc90-114">PARAMETERS</span></span>

### <span data-ttu-id="acc90-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="acc90-115">-AsJob</span></span>
<span data-ttu-id="acc90-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="acc90-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="acc90-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acc90-117">-DefaultProfile</span></span>
<span data-ttu-id="acc90-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="acc90-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="acc90-119">-Location</span><span class="sxs-lookup"><span data-stu-id="acc90-119">-Location</span></span>
<span data-ttu-id="acc90-120">Posizione del network watcher.</span><span class="sxs-lookup"><span data-stu-id="acc90-120">Location of the network watcher.</span></span>

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

### <span data-ttu-id="acc90-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="acc90-121">-NetworkWatcher</span></span>
<span data-ttu-id="acc90-122">Risorsa Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="acc90-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="acc90-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="acc90-123">-NetworkWatcherName</span></span>
<span data-ttu-id="acc90-124">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="acc90-124">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="acc90-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acc90-125">-ResourceGroupName</span></span>
<span data-ttu-id="acc90-126">Nome del gruppo di risorse Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="acc90-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="acc90-127">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="acc90-127">-TargetVirtualMachineId</span></span>
<span data-ttu-id="acc90-128">ID della macchina virtuale di destinazione</span><span class="sxs-lookup"><span data-stu-id="acc90-128">The target VM Id</span></span>

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

### <span data-ttu-id="acc90-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acc90-129">CommonParameters</span></span>
<span data-ttu-id="acc90-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acc90-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acc90-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="acc90-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acc90-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="acc90-132">INPUTS</span></span>

### <span data-ttu-id="acc90-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="acc90-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="acc90-134">System.String</span><span class="sxs-lookup"><span data-stu-id="acc90-134">System.String</span></span>

## <span data-ttu-id="acc90-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="acc90-135">OUTPUTS</span></span>

### <span data-ttu-id="acc90-136">Microsoft.Azure.Commands.Network.Models.PSSecurityGroupViewResult</span><span class="sxs-lookup"><span data-stu-id="acc90-136">Microsoft.Azure.Commands.Network.Models.PSSecurityGroupViewResult</span></span>

## <span data-ttu-id="acc90-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="acc90-137">NOTES</span></span>
<span data-ttu-id="acc90-138">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, rete, rete, network watcher, flusso, ip</span><span class="sxs-lookup"><span data-stu-id="acc90-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="acc90-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="acc90-139">RELATED LINKS</span></span>

[<span data-ttu-id="acc90-140">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="acc90-140">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="acc90-141">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="acc90-141">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="acc90-142">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="acc90-142">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="acc90-143">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="acc90-143">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="acc90-144">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="acc90-144">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="acc90-145">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="acc90-145">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="acc90-146">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="acc90-146">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="acc90-147">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="acc90-147">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="acc90-148">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="acc90-148">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="acc90-149">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="acc90-149">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="acc90-150">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="acc90-150">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="acc90-151">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="acc90-151">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="acc90-152">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="acc90-152">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="acc90-153">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="acc90-153">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="acc90-154">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="acc90-154">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="acc90-155">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="acc90-155">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="acc90-156">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="acc90-156">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="acc90-157">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="acc90-157">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="acc90-158">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="acc90-158">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="acc90-159">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="acc90-159">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="acc90-160">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="acc90-160">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="acc90-161">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="acc90-161">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="acc90-162">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="acc90-162">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="acc90-163">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="acc90-163">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="acc90-164">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="acc90-164">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="acc90-165">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="acc90-165">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="acc90-166">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="acc90-166">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
