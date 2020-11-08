---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: 37da72dd26df32dddee0ea28d2378418e9e4922e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189028"
---
# <span data-ttu-id="cad1b-101">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="cad1b-101">Get-AzNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="cad1b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cad1b-102">SYNOPSIS</span></span>
<span data-ttu-id="cad1b-103">Visualizzare le regole di gruppo di sicurezza di rete configurate ed effettive applicate in una VM.</span><span class="sxs-lookup"><span data-stu-id="cad1b-103">View the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="cad1b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cad1b-104">SYNTAX</span></span>

### <span data-ttu-id="cad1b-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cad1b-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cad1b-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="cad1b-106">SetByName</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cad1b-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="cad1b-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -Location <String> -TargetVirtualMachineId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cad1b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cad1b-108">DESCRIPTION</span></span>
<span data-ttu-id="cad1b-109">Il Get-AzNetworkWatcherSecurityGroupView consente di visualizzare le regole di gruppo di sicurezza di rete configurate ed effettive applicate in una VM.</span><span class="sxs-lookup"><span data-stu-id="cad1b-109">The Get-AzNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="cad1b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cad1b-110">EXAMPLES</span></span>

### <span data-ttu-id="cad1b-111">Esempio 1: impostare una chiamata di visualizzazione per un gruppo di sicurezza in una VM</span><span class="sxs-lookup"><span data-stu-id="cad1b-111">Example 1: Make a Security Group View call on a VM</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="cad1b-112">Nell'esempio precedente otteniamo prima di tutto il monitoraggio della rete regionale, quindi una VM nell'area geografica.</span><span class="sxs-lookup"><span data-stu-id="cad1b-112">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="cad1b-113">Quindi facciamo una chiamata di gruppo di sicurezza nella VM specificata.</span><span class="sxs-lookup"><span data-stu-id="cad1b-113">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="cad1b-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cad1b-114">PARAMETERS</span></span>

### <span data-ttu-id="cad1b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cad1b-115">-AsJob</span></span>
<span data-ttu-id="cad1b-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="cad1b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cad1b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cad1b-117">-DefaultProfile</span></span>
<span data-ttu-id="cad1b-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cad1b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cad1b-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="cad1b-119">-Location</span></span>
<span data-ttu-id="cad1b-120">Posizione del monitoraggio della rete.</span><span class="sxs-lookup"><span data-stu-id="cad1b-120">Location of the network watcher.</span></span>

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

### <span data-ttu-id="cad1b-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cad1b-121">-NetworkWatcher</span></span>
<span data-ttu-id="cad1b-122">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="cad1b-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="cad1b-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="cad1b-123">-NetworkWatcherName</span></span>
<span data-ttu-id="cad1b-124">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="cad1b-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="cad1b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cad1b-125">-ResourceGroupName</span></span>
<span data-ttu-id="cad1b-126">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="cad1b-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="cad1b-127">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="cad1b-127">-TargetVirtualMachineId</span></span>
<span data-ttu-id="cad1b-128">ID VM di destinazione</span><span class="sxs-lookup"><span data-stu-id="cad1b-128">The target VM Id</span></span>

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

### <span data-ttu-id="cad1b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cad1b-129">CommonParameters</span></span>
<span data-ttu-id="cad1b-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cad1b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cad1b-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cad1b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cad1b-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cad1b-132">INPUTS</span></span>

### <span data-ttu-id="cad1b-133">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cad1b-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="cad1b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="cad1b-134">System.String</span></span>

## <span data-ttu-id="cad1b-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cad1b-135">OUTPUTS</span></span>

### <span data-ttu-id="cad1b-136">Microsoft. Azure. Commands. Network. Models. PSSecurityGroupViewResult</span><span class="sxs-lookup"><span data-stu-id="cad1b-136">Microsoft.Azure.Commands.Network.Models.PSSecurityGroupViewResult</span></span>

## <span data-ttu-id="cad1b-137">Note</span><span class="sxs-lookup"><span data-stu-id="cad1b-137">NOTES</span></span>
<span data-ttu-id="cad1b-138">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher, Flow, IP</span><span class="sxs-lookup"><span data-stu-id="cad1b-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="cad1b-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cad1b-139">RELATED LINKS</span></span>

[<span data-ttu-id="cad1b-140">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cad1b-140">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="cad1b-141">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cad1b-141">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="cad1b-142">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cad1b-142">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="cad1b-143">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="cad1b-143">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="cad1b-144">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="cad1b-144">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="cad1b-145">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="cad1b-145">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="cad1b-146">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="cad1b-146">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="cad1b-147">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cad1b-147">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cad1b-148">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="cad1b-148">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="cad1b-149">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cad1b-149">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cad1b-150">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cad1b-150">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cad1b-151">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cad1b-151">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cad1b-152">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="cad1b-152">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="cad1b-153">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="cad1b-153">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="cad1b-154">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="cad1b-154">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="cad1b-155">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cad1b-155">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cad1b-156">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cad1b-156">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cad1b-157">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cad1b-157">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cad1b-158">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="cad1b-158">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="cad1b-159">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cad1b-159">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cad1b-160">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cad1b-160">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cad1b-161">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="cad1b-161">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="cad1b-162">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="cad1b-162">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="cad1b-163">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="cad1b-163">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="cad1b-164">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="cad1b-164">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="cad1b-165">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="cad1b-165">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="cad1b-166">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cad1b-166">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
