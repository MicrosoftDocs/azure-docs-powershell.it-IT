---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherflowlogstatus
schema: 2.0.0
ms.openlocfilehash: 96d3bea781b0c595b54387a9b07b085f173d7b0a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866075"
---
# <span data-ttu-id="eff1c-101">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="eff1c-101">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>

## <span data-ttu-id="eff1c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eff1c-102">SYNOPSIS</span></span>
<span data-ttu-id="eff1c-103">Ottiene lo stato della registrazione del flusso in una risorsa.</span><span class="sxs-lookup"><span data-stu-id="eff1c-103">Gets the status of flow logging on a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eff1c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eff1c-104">SYNTAX</span></span>

### <span data-ttu-id="eff1c-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="eff1c-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eff1c-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="eff1c-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eff1c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eff1c-107">DESCRIPTION</span></span>
<span data-ttu-id="eff1c-108">Il cmdlet Get-AzureRmNetworkWatcherFlowLogStatus ottiene lo stato della registrazione del flusso in una risorsa.</span><span class="sxs-lookup"><span data-stu-id="eff1c-108">The Get-AzureRmNetworkWatcherFlowLogStatus cmdlet Gets the status of flow logging on a resource.</span></span> <span data-ttu-id="eff1c-109">Lo stato include se è abilitata o meno la registrazione del flusso per la risorsa fornita, l'account di archiviazione configurato per l'invio dei log e i criteri di conservazione per i registri.</span><span class="sxs-lookup"><span data-stu-id="eff1c-109">The status includes whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="eff1c-110">Attualmente i gruppi di sicurezza di rete sono supportati per la registrazione del flusso.</span><span class="sxs-lookup"><span data-stu-id="eff1c-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="eff1c-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eff1c-111">EXAMPLES</span></span>

### <span data-ttu-id="eff1c-112">---Esempio 1: ottenere lo stato di registrazione del flusso per un determinato NSG---</span><span class="sxs-lookup"><span data-stu-id="eff1c-112">--- Example 1: Get the Flow Logging Status for a Specified NSG ---</span></span>
```
PS C:\> $NW = Get-AzurermNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzureRmNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG

PS C:\> Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcher $NW -TargetResourceId $nsg.Id

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

<span data-ttu-id="eff1c-113">In questo esempio viene visualizzato lo stato registrazione flusso per un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="eff1c-113">In this example we get the flow logging status for a Network Security Group.</span></span> <span data-ttu-id="eff1c-114">L'oggetto NSG specificato include la registrazione del flusso abilitata e nessun criterio di conservazione impostato.</span><span class="sxs-lookup"><span data-stu-id="eff1c-114">The specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="eff1c-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eff1c-115">PARAMETERS</span></span>

### <span data-ttu-id="eff1c-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eff1c-116">-AsJob</span></span>
<span data-ttu-id="eff1c-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="eff1c-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eff1c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eff1c-118">-DefaultProfile</span></span>
<span data-ttu-id="eff1c-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eff1c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eff1c-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="eff1c-120">-NetworkWatcher</span></span>
<span data-ttu-id="eff1c-121">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="eff1c-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="eff1c-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="eff1c-122">-NetworkWatcherName</span></span>
<span data-ttu-id="eff1c-123">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="eff1c-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="eff1c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eff1c-124">-ResourceGroupName</span></span>
<span data-ttu-id="eff1c-125">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="eff1c-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="eff1c-126">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="eff1c-126">-TargetResourceId</span></span>
<span data-ttu-id="eff1c-127">ID risorsa di destinazione.</span><span class="sxs-lookup"><span data-stu-id="eff1c-127">The target resource ID.</span></span>

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

### <span data-ttu-id="eff1c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eff1c-128">CommonParameters</span></span>
<span data-ttu-id="eff1c-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eff1c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eff1c-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eff1c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eff1c-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eff1c-131">INPUTS</span></span>

### <span data-ttu-id="eff1c-132">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="eff1c-132">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="eff1c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="eff1c-133">System.String</span></span>

## <span data-ttu-id="eff1c-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eff1c-134">OUTPUTS</span></span>

### <span data-ttu-id="eff1c-135">Microsoft. Azure. Commands. Network. Models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="eff1c-135">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="eff1c-136">Note</span><span class="sxs-lookup"><span data-stu-id="eff1c-136">NOTES</span></span>
<span data-ttu-id="eff1c-137">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Watcher, Flow, logs, flowlog, logging</span><span class="sxs-lookup"><span data-stu-id="eff1c-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="eff1c-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eff1c-138">RELATED LINKS</span></span>

[<span data-ttu-id="eff1c-139">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="eff1c-139">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="eff1c-140">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="eff1c-140">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="eff1c-141">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="eff1c-141">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="eff1c-142">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="eff1c-142">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="eff1c-143">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="eff1c-143">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="eff1c-144">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="eff1c-144">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="eff1c-145">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="eff1c-145">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="eff1c-146">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="eff1c-146">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="eff1c-147">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="eff1c-147">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="eff1c-148">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="eff1c-148">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="eff1c-149">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="eff1c-149">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="eff1c-150">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="eff1c-150">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="eff1c-151">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="eff1c-151">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="eff1c-152">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="eff1c-152">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="eff1c-153">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="eff1c-153">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)
