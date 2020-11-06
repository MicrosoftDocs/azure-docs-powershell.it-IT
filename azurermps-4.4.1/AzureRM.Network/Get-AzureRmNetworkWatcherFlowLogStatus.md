---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherFlowLogStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherFlowLogStatus.md
ms.openlocfilehash: 1c7e67eacc52e995632a526514c84bf7a9f45425
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520032"
---
# <span data-ttu-id="ec249-101">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="ec249-101">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>

## <span data-ttu-id="ec249-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ec249-102">SYNOPSIS</span></span>
<span data-ttu-id="ec249-103">Ottiene lo stato della registrazione del flusso in una risorsa.</span><span class="sxs-lookup"><span data-stu-id="ec249-103">Gets the status of flow logging on a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec249-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ec249-104">SYNTAX</span></span>

### <span data-ttu-id="ec249-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ec249-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec249-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="ec249-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec249-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ec249-107">DESCRIPTION</span></span>
<span data-ttu-id="ec249-108">Il cmdlet Get-AzureRmNetworkWatcherFlowLogStatus ottiene lo stato della registrazione del flusso in una risorsa.</span><span class="sxs-lookup"><span data-stu-id="ec249-108">The Get-AzureRmNetworkWatcherFlowLogStatus cmdlet Gets the status of flow logging on a resource.</span></span> <span data-ttu-id="ec249-109">Lo stato include se è abilitata o meno la registrazione del flusso per la risorsa fornita, l'account di archiviazione configurato per l'invio dei log e i criteri di conservazione per i registri.</span><span class="sxs-lookup"><span data-stu-id="ec249-109">The status includes whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="ec249-110">Attualmente i gruppi di sicurezza di rete sono supportati per la registrazione del flusso.</span><span class="sxs-lookup"><span data-stu-id="ec249-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="ec249-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ec249-111">EXAMPLES</span></span>

### <span data-ttu-id="ec249-112">---Esempio 1: ottenere lo stato di registrazione del flusso per un determinato NSG---</span><span class="sxs-lookup"><span data-stu-id="ec249-112">--- Example 1: Get the Flow Logging Status for a Specified NSG ---</span></span>
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

<span data-ttu-id="ec249-113">In questo esempio viene visualizzato lo stato registrazione flusso per un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="ec249-113">In this example we get the flow logging status for a Network Security Group.</span></span> <span data-ttu-id="ec249-114">L'oggetto NSG specificato include la registrazione del flusso abilitata e nessun criterio di conservazione impostato.</span><span class="sxs-lookup"><span data-stu-id="ec249-114">The specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="ec249-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ec249-115">PARAMETERS</span></span>

### <span data-ttu-id="ec249-116">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ec249-116">-NetworkWatcher</span></span>
<span data-ttu-id="ec249-117">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="ec249-117">The network watcher resource.</span></span>

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

### <span data-ttu-id="ec249-118">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="ec249-118">-NetworkWatcherName</span></span>
<span data-ttu-id="ec249-119">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="ec249-119">The name of network watcher.</span></span>

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

### <span data-ttu-id="ec249-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec249-120">-ResourceGroupName</span></span>
<span data-ttu-id="ec249-121">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="ec249-121">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="ec249-122">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="ec249-122">-TargetResourceId</span></span>
<span data-ttu-id="ec249-123">ID risorsa di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ec249-123">The target resource ID.</span></span>

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

### <span data-ttu-id="ec249-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec249-124">-DefaultProfile</span></span>
<span data-ttu-id="ec249-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ec249-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec249-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec249-126">CommonParameters</span></span>
<span data-ttu-id="ec249-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec249-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec249-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec249-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec249-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ec249-129">INPUTS</span></span>

### <span data-ttu-id="ec249-130">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ec249-130">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="ec249-131">System. String</span><span class="sxs-lookup"><span data-stu-id="ec249-131">System.String</span></span>

## <span data-ttu-id="ec249-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ec249-132">OUTPUTS</span></span>

### <span data-ttu-id="ec249-133">Microsoft. Azure. Commands. Network. Models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="ec249-133">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="ec249-134">Note</span><span class="sxs-lookup"><span data-stu-id="ec249-134">NOTES</span></span>
<span data-ttu-id="ec249-135">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Watcher, Flow, logs, flowlog, logging</span><span class="sxs-lookup"><span data-stu-id="ec249-135">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="ec249-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ec249-136">RELATED LINKS</span></span>

[<span data-ttu-id="ec249-137">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="ec249-137">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="ec249-138">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ec249-138">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="ec249-139">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ec249-139">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="ec249-140">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ec249-140">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="ec249-141">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ec249-141">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ec249-142">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="ec249-142">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="ec249-143">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ec249-143">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ec249-144">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ec249-144">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ec249-145">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ec249-145">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ec249-146">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="ec249-146">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="ec249-147">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="ec249-147">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="ec249-148">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="ec249-148">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="ec249-149">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="ec249-149">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="ec249-150">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="ec249-150">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="ec249-151">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="ec249-151">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)
