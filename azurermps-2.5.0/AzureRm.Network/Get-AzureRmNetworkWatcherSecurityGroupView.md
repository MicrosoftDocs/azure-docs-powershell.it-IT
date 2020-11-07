---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchersecuritygroupview
schema: 2.0.0
ms.openlocfilehash: fad852ff589b2929df83775a2fa955e72663cfa2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865910"
---
# <span data-ttu-id="4bcec-101">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="4bcec-101">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="4bcec-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4bcec-102">SYNOPSIS</span></span>
<span data-ttu-id="4bcec-103">Visualizzare le regole di gruppo di sicurezza di rete configurate ed effettive applicate in una VM.</span><span class="sxs-lookup"><span data-stu-id="4bcec-103">View the configured and effective network security group rules applied on a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4bcec-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4bcec-104">SYNTAX</span></span>

### <span data-ttu-id="4bcec-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4bcec-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bcec-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="4bcec-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4bcec-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4bcec-107">DESCRIPTION</span></span>
<span data-ttu-id="4bcec-108">Il Get-AzureRmNetworkWatcherSecurityGroupView consente di visualizzare le regole di gruppo di sicurezza di rete configurate ed effettive applicate in una VM.</span><span class="sxs-lookup"><span data-stu-id="4bcec-108">The Get-AzureRmNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="4bcec-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4bcec-109">EXAMPLES</span></span>

### <span data-ttu-id="4bcec-110">---Esempio 1: effettuare una chiamata di visualizzazione per un gruppo di sicurezza in una---VM</span><span class="sxs-lookup"><span data-stu-id="4bcec-110">--- Example 1: Make a Security Group View call on a VM ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="4bcec-111">Nell'esempio precedente otteniamo prima di tutto il monitoraggio della rete regionale, quindi una VM nell'area geografica.</span><span class="sxs-lookup"><span data-stu-id="4bcec-111">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="4bcec-112">Quindi facciamo una chiamata di gruppo di sicurezza nella VM specificata.</span><span class="sxs-lookup"><span data-stu-id="4bcec-112">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="4bcec-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4bcec-113">PARAMETERS</span></span>

### <span data-ttu-id="4bcec-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4bcec-114">-AsJob</span></span>
<span data-ttu-id="4bcec-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="4bcec-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4bcec-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bcec-116">-DefaultProfile</span></span>
<span data-ttu-id="4bcec-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4bcec-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bcec-118">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4bcec-118">-NetworkWatcher</span></span>
<span data-ttu-id="4bcec-119">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="4bcec-119">The network watcher resource.</span></span>

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

### <span data-ttu-id="4bcec-120">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="4bcec-120">-NetworkWatcherName</span></span>
<span data-ttu-id="4bcec-121">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="4bcec-121">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4bcec-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bcec-122">-ResourceGroupName</span></span>
<span data-ttu-id="4bcec-123">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="4bcec-123">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bcec-124">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="4bcec-124">-TargetVirtualMachineId</span></span>
<span data-ttu-id="4bcec-125">ID VM di destinazione</span><span class="sxs-lookup"><span data-stu-id="4bcec-125">The target VM Id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bcec-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bcec-126">CommonParameters</span></span>
<span data-ttu-id="4bcec-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bcec-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bcec-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bcec-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bcec-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4bcec-129">INPUTS</span></span>

### <span data-ttu-id="4bcec-130">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4bcec-130">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="4bcec-131">System. String</span><span class="sxs-lookup"><span data-stu-id="4bcec-131">System.String</span></span>

## <span data-ttu-id="4bcec-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4bcec-132">OUTPUTS</span></span>

### <span data-ttu-id="4bcec-133">Microsoft. Azure. Commands. Network. Models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="4bcec-133">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="4bcec-134">Note</span><span class="sxs-lookup"><span data-stu-id="4bcec-134">NOTES</span></span>
<span data-ttu-id="4bcec-135">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher, Flow, IP</span><span class="sxs-lookup"><span data-stu-id="4bcec-135">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="4bcec-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4bcec-136">RELATED LINKS</span></span>

[<span data-ttu-id="4bcec-137">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4bcec-137">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="4bcec-138">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4bcec-138">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="4bcec-139">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4bcec-139">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="4bcec-140">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="4bcec-140">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="4bcec-141">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="4bcec-141">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="4bcec-142">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="4bcec-142">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="4bcec-143">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="4bcec-143">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="4bcec-144">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4bcec-144">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4bcec-145">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="4bcec-145">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="4bcec-146">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4bcec-146">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4bcec-147">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4bcec-147">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4bcec-148">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4bcec-148">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

