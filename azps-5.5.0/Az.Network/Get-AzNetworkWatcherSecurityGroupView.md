---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: ec1b53799b92f0a68c20110dfe78f9af7b8391c2
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100395759"
---
# <span data-ttu-id="2e102-101">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="2e102-101">Get-AzNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="2e102-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e102-102">SYNOPSIS</span></span>
<span data-ttu-id="2e102-103">Visualizzare le regole configurate ed efficaci del gruppo di sicurezza di rete applicate in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2e102-103">View the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="2e102-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2e102-104">SYNTAX</span></span>

### <span data-ttu-id="2e102-105">SetByResource (Default)</span><span class="sxs-lookup"><span data-stu-id="2e102-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e102-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="2e102-106">SetByName</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e102-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="2e102-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -Location <String> -TargetVirtualMachineId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e102-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2e102-108">DESCRIPTION</span></span>
<span data-ttu-id="2e102-109">LGet-AzNetworkWatcherSecurityGroupView consente di visualizzare le regole configurate ed effettive del gruppo di sicurezza di rete applicate in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2e102-109">The Get-AzNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="2e102-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2e102-110">EXAMPLES</span></span>

### <span data-ttu-id="2e102-111">Esempio 1: Effettuare una chiamata di visualizzazione gruppo di sicurezza in una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="2e102-111">Example 1: Make a Security Group View call on a VM</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="2e102-112">Nell'esempio precedente si ottiene prima Network Watcher locale, quindi una macchina virtuale nell'area geografica.</span><span class="sxs-lookup"><span data-stu-id="2e102-112">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="2e102-113">Verrà quindi creata una chiamata di visualizzazione del gruppo di sicurezza nella macchina virtuale specificata.</span><span class="sxs-lookup"><span data-stu-id="2e102-113">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="2e102-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e102-114">PARAMETERS</span></span>

### <span data-ttu-id="2e102-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2e102-115">-AsJob</span></span>
<span data-ttu-id="2e102-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="2e102-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2e102-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e102-117">-DefaultProfile</span></span>
<span data-ttu-id="2e102-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2e102-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e102-119">-Location</span><span class="sxs-lookup"><span data-stu-id="2e102-119">-Location</span></span>
<span data-ttu-id="2e102-120">Posizione del network watcher.</span><span class="sxs-lookup"><span data-stu-id="2e102-120">Location of the network watcher.</span></span>

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

### <span data-ttu-id="2e102-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2e102-121">-NetworkWatcher</span></span>
<span data-ttu-id="2e102-122">Risorsa Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="2e102-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="2e102-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="2e102-123">-NetworkWatcherName</span></span>
<span data-ttu-id="2e102-124">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="2e102-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="2e102-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e102-125">-ResourceGroupName</span></span>
<span data-ttu-id="2e102-126">Nome del gruppo di risorse Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="2e102-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="2e102-127">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="2e102-127">-TargetVirtualMachineId</span></span>
<span data-ttu-id="2e102-128">ID della macchina virtuale di destinazione</span><span class="sxs-lookup"><span data-stu-id="2e102-128">The target VM Id</span></span>

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

### <span data-ttu-id="2e102-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e102-129">CommonParameters</span></span>
<span data-ttu-id="2e102-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e102-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e102-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2e102-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e102-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="2e102-132">INPUTS</span></span>

### <span data-ttu-id="2e102-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2e102-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="2e102-134">System.String</span><span class="sxs-lookup"><span data-stu-id="2e102-134">System.String</span></span>

## <span data-ttu-id="2e102-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2e102-135">OUTPUTS</span></span>

### <span data-ttu-id="2e102-136">Microsoft.Azure.Commands.Network.Models.PSSecurityGroupViewResult</span><span class="sxs-lookup"><span data-stu-id="2e102-136">Microsoft.Azure.Commands.Network.Models.PSSecurityGroupViewResult</span></span>

## <span data-ttu-id="2e102-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="2e102-137">NOTES</span></span>
<span data-ttu-id="2e102-138">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, rete, rete, network watcher, flusso, ip</span><span class="sxs-lookup"><span data-stu-id="2e102-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="2e102-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2e102-139">RELATED LINKS</span></span>

[<span data-ttu-id="2e102-140">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2e102-140">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="2e102-141">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2e102-141">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="2e102-142">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2e102-142">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="2e102-143">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="2e102-143">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="2e102-144">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="2e102-144">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="2e102-145">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="2e102-145">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="2e102-146">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="2e102-146">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="2e102-147">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2e102-147">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2e102-148">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="2e102-148">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="2e102-149">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2e102-149">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2e102-150">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2e102-150">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2e102-151">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2e102-151">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2e102-152">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="2e102-152">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="2e102-153">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2e102-153">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="2e102-154">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="2e102-154">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="2e102-155">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2e102-155">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2e102-156">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2e102-156">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2e102-157">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2e102-157">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2e102-158">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="2e102-158">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="2e102-159">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2e102-159">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2e102-160">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2e102-160">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2e102-161">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="2e102-161">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="2e102-162">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="2e102-162">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="2e102-163">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="2e102-163">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="2e102-164">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="2e102-164">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="2e102-165">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="2e102-165">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="2e102-166">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2e102-166">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
