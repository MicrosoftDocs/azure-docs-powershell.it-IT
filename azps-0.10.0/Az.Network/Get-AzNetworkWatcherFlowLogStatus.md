---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherflowlogstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
ms.openlocfilehash: 2f855175065f743bdfec5fb8dc9c917af262b05b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860722"
---
# <span data-ttu-id="9dfab-101">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="9dfab-101">Get-AzNetworkWatcherFlowLogStatus</span></span>

## <span data-ttu-id="9dfab-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9dfab-102">SYNOPSIS</span></span>
<span data-ttu-id="9dfab-103">Ottiene lo stato della registrazione del flusso in una risorsa.</span><span class="sxs-lookup"><span data-stu-id="9dfab-103">Gets the status of flow logging on a resource.</span></span>

## <span data-ttu-id="9dfab-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9dfab-104">SYNTAX</span></span>

### <span data-ttu-id="9dfab-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9dfab-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9dfab-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="9dfab-106">SetByName</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9dfab-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9dfab-107">DESCRIPTION</span></span>
<span data-ttu-id="9dfab-108">Il cmdlet Get-AzNetworkWatcherFlowLogStatus ottiene lo stato della registrazione del flusso in una risorsa.</span><span class="sxs-lookup"><span data-stu-id="9dfab-108">The Get-AzNetworkWatcherFlowLogStatus cmdlet Gets the status of flow logging on a resource.</span></span> <span data-ttu-id="9dfab-109">Lo stato include se è abilitata o meno la registrazione del flusso per la risorsa fornita, l'account di archiviazione configurato per l'invio dei log e i criteri di conservazione per i registri.</span><span class="sxs-lookup"><span data-stu-id="9dfab-109">The status includes whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="9dfab-110">Attualmente i gruppi di sicurezza di rete sono supportati per la registrazione del flusso.</span><span class="sxs-lookup"><span data-stu-id="9dfab-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="9dfab-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9dfab-111">EXAMPLES</span></span>

### <span data-ttu-id="9dfab-112">---Esempio 1: ottenere lo stato di registrazione del flusso per un determinato NSG---</span><span class="sxs-lookup"><span data-stu-id="9dfab-112">--- Example 1: Get the Flow Logging Status for a Specified NSG ---</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG

PS C:\> Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher $NW -TargetResourceId $nsg.Id

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
Properties       : {
                     "Enabled": true,
                     "RetentionPolicy": {
                       "Days": 0,
                       "Enabled": false
                     },
                     "StorageId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"
                   }
```

<span data-ttu-id="9dfab-113">In questo esempio viene visualizzato lo stato registrazione flusso per un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="9dfab-113">In this example we get the flow logging status for a Network Security Group.</span></span> <span data-ttu-id="9dfab-114">L'oggetto NSG specificato include la registrazione del flusso abilitata e nessun criterio di conservazione impostato.</span><span class="sxs-lookup"><span data-stu-id="9dfab-114">The specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="9dfab-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9dfab-115">PARAMETERS</span></span>

### <span data-ttu-id="9dfab-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9dfab-116">-AsJob</span></span>
<span data-ttu-id="9dfab-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="9dfab-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9dfab-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dfab-118">-DefaultProfile</span></span>
<span data-ttu-id="9dfab-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9dfab-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9dfab-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9dfab-120">-NetworkWatcher</span></span>
<span data-ttu-id="9dfab-121">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="9dfab-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="9dfab-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="9dfab-122">-NetworkWatcherName</span></span>
<span data-ttu-id="9dfab-123">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="9dfab-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="9dfab-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dfab-124">-ResourceGroupName</span></span>
<span data-ttu-id="9dfab-125">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="9dfab-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="9dfab-126">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="9dfab-126">-TargetResourceId</span></span>
<span data-ttu-id="9dfab-127">ID risorsa di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9dfab-127">The target resource ID.</span></span>

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

### <span data-ttu-id="9dfab-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dfab-128">CommonParameters</span></span>
<span data-ttu-id="9dfab-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dfab-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dfab-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9dfab-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dfab-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9dfab-131">INPUTS</span></span>

### <span data-ttu-id="9dfab-132">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9dfab-132">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="9dfab-133">System. String</span><span class="sxs-lookup"><span data-stu-id="9dfab-133">System.String</span></span>

## <span data-ttu-id="9dfab-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9dfab-134">OUTPUTS</span></span>

### <span data-ttu-id="9dfab-135">Microsoft. Azure. Commands. Network. Models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="9dfab-135">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="9dfab-136">Note</span><span class="sxs-lookup"><span data-stu-id="9dfab-136">NOTES</span></span>
<span data-ttu-id="9dfab-137">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Watcher, Flow, logs, flowlog, logging</span><span class="sxs-lookup"><span data-stu-id="9dfab-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="9dfab-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9dfab-138">RELATED LINKS</span></span>

[<span data-ttu-id="9dfab-139">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="9dfab-139">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="9dfab-140">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9dfab-140">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="9dfab-141">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9dfab-141">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="9dfab-142">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9dfab-142">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="9dfab-143">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9dfab-143">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9dfab-144">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="9dfab-144">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="9dfab-145">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9dfab-145">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9dfab-146">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9dfab-146">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9dfab-147">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9dfab-147">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9dfab-148">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="9dfab-148">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="9dfab-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="9dfab-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="9dfab-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="9dfab-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="9dfab-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="9dfab-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="9dfab-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="9dfab-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="9dfab-153">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="9dfab-153">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)
