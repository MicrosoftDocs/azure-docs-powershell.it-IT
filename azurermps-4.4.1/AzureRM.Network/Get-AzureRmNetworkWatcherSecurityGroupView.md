---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: 44bba48f1d066c4a9006595092bd84c68252bbd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519119"
---
# <span data-ttu-id="7f178-101">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="7f178-101">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="7f178-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7f178-102">SYNOPSIS</span></span>
<span data-ttu-id="7f178-103">Visualizzare le regole di gruppo di sicurezza di rete configurate ed effettive applicate in una VM.</span><span class="sxs-lookup"><span data-stu-id="7f178-103">View the configured and effective network security group rules applied on a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f178-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7f178-104">SYNTAX</span></span>

### <span data-ttu-id="7f178-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7f178-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f178-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="7f178-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f178-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f178-107">DESCRIPTION</span></span>
<span data-ttu-id="7f178-108">Il Get-AzureRmNetworkWatcherSecurityGroupView consente di visualizzare le regole di gruppo di sicurezza di rete configurate ed effettive applicate in una VM.</span><span class="sxs-lookup"><span data-stu-id="7f178-108">The Get-AzureRmNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="7f178-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7f178-109">EXAMPLES</span></span>

### <span data-ttu-id="7f178-110">---Esempio 1: effettuare una chiamata di visualizzazione per un gruppo di sicurezza in una---VM</span><span class="sxs-lookup"><span data-stu-id="7f178-110">--- Example 1: Make a Security Group View call on a VM ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="7f178-111">Nell'esempio precedente otteniamo prima di tutto il monitoraggio della rete regionale, quindi una VM nell'area geografica.</span><span class="sxs-lookup"><span data-stu-id="7f178-111">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="7f178-112">Quindi facciamo una chiamata di gruppo di sicurezza nella VM specificata.</span><span class="sxs-lookup"><span data-stu-id="7f178-112">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="7f178-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7f178-113">PARAMETERS</span></span>

### <span data-ttu-id="7f178-114">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7f178-114">-NetworkWatcher</span></span>
<span data-ttu-id="7f178-115">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="7f178-115">The network watcher resource.</span></span>

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

### <span data-ttu-id="7f178-116">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="7f178-116">-NetworkWatcherName</span></span>
<span data-ttu-id="7f178-117">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="7f178-117">The name of network watcher.</span></span>

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

### <span data-ttu-id="7f178-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f178-118">-ResourceGroupName</span></span>
<span data-ttu-id="7f178-119">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="7f178-119">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="7f178-120">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="7f178-120">-TargetVirtualMachineId</span></span>
<span data-ttu-id="7f178-121">ID VM di destinazione</span><span class="sxs-lookup"><span data-stu-id="7f178-121">The target VM Id</span></span>

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

### <span data-ttu-id="7f178-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f178-122">-DefaultProfile</span></span>
<span data-ttu-id="7f178-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7f178-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f178-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f178-124">CommonParameters</span></span>
<span data-ttu-id="7f178-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f178-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f178-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f178-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f178-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7f178-127">INPUTS</span></span>

### <span data-ttu-id="7f178-128">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7f178-128">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="7f178-129">System. String</span><span class="sxs-lookup"><span data-stu-id="7f178-129">System.String</span></span>

## <span data-ttu-id="7f178-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7f178-130">OUTPUTS</span></span>

### <span data-ttu-id="7f178-131">Microsoft. Azure. Commands. Network. Models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="7f178-131">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="7f178-132">Note</span><span class="sxs-lookup"><span data-stu-id="7f178-132">NOTES</span></span>
<span data-ttu-id="7f178-133">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher, Flow, IP</span><span class="sxs-lookup"><span data-stu-id="7f178-133">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="7f178-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7f178-134">RELATED LINKS</span></span>

[<span data-ttu-id="7f178-135">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7f178-135">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7f178-136">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7f178-136">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7f178-137">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7f178-137">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7f178-138">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="7f178-138">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="7f178-139">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="7f178-139">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="7f178-140">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="7f178-140">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="7f178-141">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="7f178-141">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="7f178-142">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7f178-142">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7f178-143">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="7f178-143">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="7f178-144">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7f178-144">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7f178-145">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7f178-145">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7f178-146">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7f178-146">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

