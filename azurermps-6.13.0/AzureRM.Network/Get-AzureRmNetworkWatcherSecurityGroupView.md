---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: 9fe23ea5fa9bef544feae6112879cb1be6eeae7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510887"
---
# <span data-ttu-id="b9a07-101">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="b9a07-101">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="b9a07-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b9a07-102">SYNOPSIS</span></span>
<span data-ttu-id="b9a07-103">Visualizzare le regole di gruppo di sicurezza di rete configurate ed effettive applicate in una VM.</span><span class="sxs-lookup"><span data-stu-id="b9a07-103">View the configured and effective network security group rules applied on a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9a07-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b9a07-104">SYNTAX</span></span>

### <span data-ttu-id="b9a07-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b9a07-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9a07-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="b9a07-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9a07-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="b9a07-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -Location <String> -TargetVirtualMachineId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9a07-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9a07-108">DESCRIPTION</span></span>
<span data-ttu-id="b9a07-109">Il Get-AzureRmNetworkWatcherSecurityGroupView consente di visualizzare le regole di gruppo di sicurezza di rete configurate ed effettive applicate in una VM.</span><span class="sxs-lookup"><span data-stu-id="b9a07-109">The Get-AzureRmNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="b9a07-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b9a07-110">EXAMPLES</span></span>

### <span data-ttu-id="b9a07-111">Esempio 1: impostare una chiamata di visualizzazione per un gruppo di sicurezza in una VM</span><span class="sxs-lookup"><span data-stu-id="b9a07-111">Example 1: Make a Security Group View call on a VM</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="b9a07-112">Nell'esempio precedente otteniamo prima di tutto il monitoraggio della rete regionale, quindi una VM nell'area geografica.</span><span class="sxs-lookup"><span data-stu-id="b9a07-112">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="b9a07-113">Quindi facciamo una chiamata di gruppo di sicurezza nella VM specificata.</span><span class="sxs-lookup"><span data-stu-id="b9a07-113">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="b9a07-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b9a07-114">PARAMETERS</span></span>

### <span data-ttu-id="b9a07-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9a07-115">-AsJob</span></span>
<span data-ttu-id="b9a07-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="b9a07-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b9a07-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9a07-117">-DefaultProfile</span></span>
<span data-ttu-id="b9a07-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b9a07-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9a07-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="b9a07-119">-Location</span></span>
<span data-ttu-id="b9a07-120">Posizione del monitoraggio della rete.</span><span class="sxs-lookup"><span data-stu-id="b9a07-120">Location of the network watcher.</span></span>

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

### <span data-ttu-id="b9a07-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b9a07-121">-NetworkWatcher</span></span>
<span data-ttu-id="b9a07-122">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="b9a07-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="b9a07-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="b9a07-123">-NetworkWatcherName</span></span>
<span data-ttu-id="b9a07-124">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="b9a07-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="b9a07-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9a07-125">-ResourceGroupName</span></span>
<span data-ttu-id="b9a07-126">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="b9a07-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="b9a07-127">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="b9a07-127">-TargetVirtualMachineId</span></span>
<span data-ttu-id="b9a07-128">ID VM di destinazione</span><span class="sxs-lookup"><span data-stu-id="b9a07-128">The target VM Id</span></span>

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

### <span data-ttu-id="b9a07-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9a07-129">CommonParameters</span></span>
<span data-ttu-id="b9a07-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9a07-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9a07-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9a07-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9a07-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b9a07-132">INPUTS</span></span>

### <span data-ttu-id="b9a07-133">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b9a07-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="b9a07-134">Parametri: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b9a07-134">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="b9a07-135">System. String</span><span class="sxs-lookup"><span data-stu-id="b9a07-135">System.String</span></span>
<span data-ttu-id="b9a07-136">Parametri: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b9a07-136">Parameters: NetworkWatcherName (ByValue)</span></span>

## <span data-ttu-id="b9a07-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b9a07-137">OUTPUTS</span></span>

### <span data-ttu-id="b9a07-138">Microsoft. Azure. Commands. Network. Models. PSSecurityGroupViewResult</span><span class="sxs-lookup"><span data-stu-id="b9a07-138">Microsoft.Azure.Commands.Network.Models.PSSecurityGroupViewResult</span></span>

## <span data-ttu-id="b9a07-139">Note</span><span class="sxs-lookup"><span data-stu-id="b9a07-139">NOTES</span></span>
<span data-ttu-id="b9a07-140">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher, Flow, IP</span><span class="sxs-lookup"><span data-stu-id="b9a07-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="b9a07-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b9a07-141">RELATED LINKS</span></span>

[<span data-ttu-id="b9a07-142">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b9a07-142">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="b9a07-143">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b9a07-143">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="b9a07-144">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b9a07-144">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="b9a07-145">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="b9a07-145">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="b9a07-146">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="b9a07-146">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="b9a07-147">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="b9a07-147">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="b9a07-148">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="b9a07-148">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="b9a07-149">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b9a07-149">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b9a07-150">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="b9a07-150">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="b9a07-151">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b9a07-151">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b9a07-152">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b9a07-152">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b9a07-153">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b9a07-153">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b9a07-154">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="b9a07-154">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="b9a07-155">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="b9a07-155">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="b9a07-156">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="b9a07-156">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="b9a07-157">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b9a07-157">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b9a07-158">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b9a07-158">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b9a07-159">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b9a07-159">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b9a07-160">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="b9a07-160">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="b9a07-161">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b9a07-161">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b9a07-162">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b9a07-162">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b9a07-163">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="b9a07-163">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="b9a07-164">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="b9a07-164">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="b9a07-165">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="b9a07-165">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="b9a07-166">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="b9a07-166">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="b9a07-167">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="b9a07-167">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="b9a07-168">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b9a07-168">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
