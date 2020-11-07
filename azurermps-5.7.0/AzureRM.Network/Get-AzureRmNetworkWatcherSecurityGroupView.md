---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: 5b48cbabfe91b16924a1296a73354db659ec8f3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688446"
---
# <span data-ttu-id="354af-101">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="354af-101">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="354af-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="354af-102">SYNOPSIS</span></span>
<span data-ttu-id="354af-103">Visualizzare le regole di gruppo di sicurezza di rete configurate ed effettive applicate in una VM.</span><span class="sxs-lookup"><span data-stu-id="354af-103">View the configured and effective network security group rules applied on a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="354af-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="354af-104">SYNTAX</span></span>

### <span data-ttu-id="354af-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="354af-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="354af-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="354af-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="354af-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="354af-107">DESCRIPTION</span></span>
<span data-ttu-id="354af-108">Il Get-AzureRmNetworkWatcherSecurityGroupView consente di visualizzare le regole di gruppo di sicurezza di rete configurate ed effettive applicate in una VM.</span><span class="sxs-lookup"><span data-stu-id="354af-108">The Get-AzureRmNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="354af-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="354af-109">EXAMPLES</span></span>

### <span data-ttu-id="354af-110">---Esempio 1: effettuare una chiamata di visualizzazione per un gruppo di sicurezza in una---VM</span><span class="sxs-lookup"><span data-stu-id="354af-110">--- Example 1: Make a Security Group View call on a VM ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="354af-111">Nell'esempio precedente otteniamo prima di tutto il monitoraggio della rete regionale, quindi una VM nell'area geografica.</span><span class="sxs-lookup"><span data-stu-id="354af-111">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="354af-112">Quindi facciamo una chiamata di gruppo di sicurezza nella VM specificata.</span><span class="sxs-lookup"><span data-stu-id="354af-112">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="354af-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="354af-113">PARAMETERS</span></span>

### <span data-ttu-id="354af-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="354af-114">-AsJob</span></span>
<span data-ttu-id="354af-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="354af-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="354af-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="354af-116">-DefaultProfile</span></span>
<span data-ttu-id="354af-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="354af-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="354af-118">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="354af-118">-NetworkWatcher</span></span>
<span data-ttu-id="354af-119">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="354af-119">The network watcher resource.</span></span>

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

### <span data-ttu-id="354af-120">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="354af-120">-NetworkWatcherName</span></span>
<span data-ttu-id="354af-121">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="354af-121">The name of network watcher.</span></span>

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

### <span data-ttu-id="354af-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="354af-122">-ResourceGroupName</span></span>
<span data-ttu-id="354af-123">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="354af-123">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="354af-124">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="354af-124">-TargetVirtualMachineId</span></span>
<span data-ttu-id="354af-125">ID VM di destinazione</span><span class="sxs-lookup"><span data-stu-id="354af-125">The target VM Id</span></span>

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

### <span data-ttu-id="354af-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="354af-126">CommonParameters</span></span>
<span data-ttu-id="354af-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="354af-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="354af-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="354af-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="354af-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="354af-129">INPUTS</span></span>

### <span data-ttu-id="354af-130">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="354af-130">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="354af-131">System. String</span><span class="sxs-lookup"><span data-stu-id="354af-131">System.String</span></span>

## <span data-ttu-id="354af-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="354af-132">OUTPUTS</span></span>

### <span data-ttu-id="354af-133">Microsoft. Azure. Commands. Network. Models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="354af-133">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="354af-134">Note</span><span class="sxs-lookup"><span data-stu-id="354af-134">NOTES</span></span>
<span data-ttu-id="354af-135">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher, Flow, IP</span><span class="sxs-lookup"><span data-stu-id="354af-135">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="354af-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="354af-136">RELATED LINKS</span></span>

[<span data-ttu-id="354af-137">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="354af-137">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="354af-138">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="354af-138">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="354af-139">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="354af-139">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="354af-140">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="354af-140">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="354af-141">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="354af-141">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="354af-142">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="354af-142">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="354af-143">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="354af-143">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="354af-144">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="354af-144">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="354af-145">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="354af-145">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="354af-146">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="354af-146">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="354af-147">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="354af-147">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="354af-148">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="354af-148">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

