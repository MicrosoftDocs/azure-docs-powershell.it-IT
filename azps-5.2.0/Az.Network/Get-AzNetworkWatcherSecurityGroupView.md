---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: 37da72dd26df32dddee0ea28d2378418e9e4922e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355888"
---
# <span data-ttu-id="d4c03-101">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d4c03-101">Get-AzNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="d4c03-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d4c03-102">SYNOPSIS</span></span>
<span data-ttu-id="d4c03-103">Visualizzare le regole di gruppo di sicurezza di rete configurate ed effettive applicate in una VM.</span><span class="sxs-lookup"><span data-stu-id="d4c03-103">View the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="d4c03-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d4c03-104">SYNTAX</span></span>

### <span data-ttu-id="d4c03-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d4c03-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4c03-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="d4c03-106">SetByName</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4c03-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="d4c03-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -Location <String> -TargetVirtualMachineId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4c03-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d4c03-108">DESCRIPTION</span></span>
<span data-ttu-id="d4c03-109">Il Get-AzNetworkWatcherSecurityGroupView consente di visualizzare le regole di gruppo di sicurezza di rete configurate ed effettive applicate in una VM.</span><span class="sxs-lookup"><span data-stu-id="d4c03-109">The Get-AzNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="d4c03-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d4c03-110">EXAMPLES</span></span>

### <span data-ttu-id="d4c03-111">Esempio 1: impostare una chiamata di visualizzazione per un gruppo di sicurezza in una VM</span><span class="sxs-lookup"><span data-stu-id="d4c03-111">Example 1: Make a Security Group View call on a VM</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="d4c03-112">Nell'esempio precedente otteniamo prima di tutto il monitoraggio della rete regionale, quindi una VM nell'area geografica.</span><span class="sxs-lookup"><span data-stu-id="d4c03-112">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="d4c03-113">Quindi facciamo una chiamata di gruppo di sicurezza nella VM specificata.</span><span class="sxs-lookup"><span data-stu-id="d4c03-113">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="d4c03-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d4c03-114">PARAMETERS</span></span>

### <span data-ttu-id="d4c03-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d4c03-115">-AsJob</span></span>
<span data-ttu-id="d4c03-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d4c03-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d4c03-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4c03-117">-DefaultProfile</span></span>
<span data-ttu-id="d4c03-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d4c03-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4c03-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d4c03-119">-Location</span></span>
<span data-ttu-id="d4c03-120">Posizione del monitoraggio della rete.</span><span class="sxs-lookup"><span data-stu-id="d4c03-120">Location of the network watcher.</span></span>

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

### <span data-ttu-id="d4c03-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d4c03-121">-NetworkWatcher</span></span>
<span data-ttu-id="d4c03-122">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="d4c03-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="d4c03-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d4c03-123">-NetworkWatcherName</span></span>
<span data-ttu-id="d4c03-124">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="d4c03-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="d4c03-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4c03-125">-ResourceGroupName</span></span>
<span data-ttu-id="d4c03-126">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="d4c03-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="d4c03-127">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="d4c03-127">-TargetVirtualMachineId</span></span>
<span data-ttu-id="d4c03-128">ID VM di destinazione</span><span class="sxs-lookup"><span data-stu-id="d4c03-128">The target VM Id</span></span>

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

### <span data-ttu-id="d4c03-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4c03-129">CommonParameters</span></span>
<span data-ttu-id="d4c03-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4c03-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4c03-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4c03-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4c03-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d4c03-132">INPUTS</span></span>

### <span data-ttu-id="d4c03-133">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d4c03-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="d4c03-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d4c03-134">System.String</span></span>

## <span data-ttu-id="d4c03-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d4c03-135">OUTPUTS</span></span>

### <span data-ttu-id="d4c03-136">Microsoft. Azure. Commands. Network. Models. PSSecurityGroupViewResult</span><span class="sxs-lookup"><span data-stu-id="d4c03-136">Microsoft.Azure.Commands.Network.Models.PSSecurityGroupViewResult</span></span>

## <span data-ttu-id="d4c03-137">Note</span><span class="sxs-lookup"><span data-stu-id="d4c03-137">NOTES</span></span>
<span data-ttu-id="d4c03-138">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher, Flow, IP</span><span class="sxs-lookup"><span data-stu-id="d4c03-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="d4c03-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d4c03-139">RELATED LINKS</span></span>

[<span data-ttu-id="d4c03-140">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d4c03-140">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="d4c03-141">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d4c03-141">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="d4c03-142">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d4c03-142">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="d4c03-143">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d4c03-143">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="d4c03-144">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d4c03-144">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d4c03-145">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d4c03-145">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="d4c03-146">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d4c03-146">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="d4c03-147">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d4c03-147">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d4c03-148">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d4c03-148">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="d4c03-149">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d4c03-149">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d4c03-150">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d4c03-150">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d4c03-151">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d4c03-151">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d4c03-152">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4c03-152">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="d4c03-153">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d4c03-153">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="d4c03-154">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="d4c03-154">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="d4c03-155">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d4c03-155">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d4c03-156">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d4c03-156">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d4c03-157">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d4c03-157">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d4c03-158">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="d4c03-158">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="d4c03-159">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d4c03-159">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d4c03-160">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d4c03-160">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d4c03-161">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="d4c03-161">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="d4c03-162">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="d4c03-162">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="d4c03-163">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="d4c03-163">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="d4c03-164">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="d4c03-164">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="d4c03-165">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="d4c03-165">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="d4c03-166">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d4c03-166">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
