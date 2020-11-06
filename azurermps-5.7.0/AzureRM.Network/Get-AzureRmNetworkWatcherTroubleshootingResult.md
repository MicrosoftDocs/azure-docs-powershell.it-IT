---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchertroubleshootingresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherTroubleshootingResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherTroubleshootingResult.md
ms.openlocfilehash: ef730b8ee6e6c35408b9d57d9dc23b0ab51a63d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511120"
---
# <span data-ttu-id="41e5d-101">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="41e5d-101">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>

## <span data-ttu-id="41e5d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="41e5d-102">SYNOPSIS</span></span>
<span data-ttu-id="41e5d-103">Ottiene il risultato della risoluzione dei problemi dell'operazione di risoluzione dei problemi eseguita in precedenza o attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="41e5d-103">Gets the troubleshooting result from the previously run or currently running troubleshooting operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41e5d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="41e5d-104">SYNTAX</span></span>

### <span data-ttu-id="41e5d-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="41e5d-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41e5d-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="41e5d-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41e5d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="41e5d-107">DESCRIPTION</span></span>
<span data-ttu-id="41e5d-108">Il cmdlet Get-AzureRmNetworkWatcherTroubleshootingResult ottiene il risultato della risoluzione dei problemi dell'operazione eseguita in precedenza o attualmente in esecuzione Start-AzureRmNetworkWatcherResourceTroubleshooting.</span><span class="sxs-lookup"><span data-stu-id="41e5d-108">The Get-AzureRmNetworkWatcherTroubleshootingResult cmdlet gets the troubleshooting result from the previously run or currently running Start-AzureRmNetworkWatcherResourceTroubleshooting operation.</span></span> <span data-ttu-id="41e5d-109">Se l'operazione di risoluzione dei problemi è attualmente in corso, questa operazione può richiedere alcuni minuti per il completamento.</span><span class="sxs-lookup"><span data-stu-id="41e5d-109">If the troubleshooting operation is currently in progress, then this operation may take a few minutes to complete.</span></span> <span data-ttu-id="41e5d-110">Attualmente sono supportati i gateway e le connessioni di rete virtuali.</span><span class="sxs-lookup"><span data-stu-id="41e5d-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="41e5d-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="41e5d-111">EXAMPLES</span></span>

### <span data-ttu-id="41e5d-112">---Esempio 1: avviare la risoluzione dei problemi su un gateway di rete virtuale e recuperare i risultati---</span><span class="sxs-lookup"><span data-stu-id="41e5d-112">--- Example 1: Start Troubleshooting on a Virtual Network Gateway and Retrieve Result ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath

Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcher $NW -TargetResourceId $target
```

<span data-ttu-id="41e5d-113">L'esempio precedente avvia la risoluzione dei problemi in un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="41e5d-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="41e5d-114">L'operazione può richiedere alcuni minuti per il completamento.</span><span class="sxs-lookup"><span data-stu-id="41e5d-114">The operation may take a few minutes to complete.</span></span>
<span data-ttu-id="41e5d-115">Dopo aver avviato la risoluzione dei problemi, viene eseguita una chiamata Get-AzureRmNetworkWatcherTroubleshootingResult alla risorsa per recuperare il risultato di questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="41e5d-115">After troubleshooting has started, a Get-AzureRmNetworkWatcherTroubleshootingResult call is made to the resource to retrieve the result of this call.</span></span> 

## <span data-ttu-id="41e5d-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="41e5d-116">PARAMETERS</span></span>

### <span data-ttu-id="41e5d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41e5d-117">-DefaultProfile</span></span>
<span data-ttu-id="41e5d-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="41e5d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41e5d-119">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="41e5d-119">-NetworkWatcher</span></span>
<span data-ttu-id="41e5d-120">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="41e5d-120">The network watcher resource.</span></span>

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

### <span data-ttu-id="41e5d-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="41e5d-121">-NetworkWatcherName</span></span>
<span data-ttu-id="41e5d-122">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="41e5d-122">The name of network watcher.</span></span>

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

### <span data-ttu-id="41e5d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41e5d-123">-ResourceGroupName</span></span>
<span data-ttu-id="41e5d-124">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="41e5d-124">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="41e5d-125">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="41e5d-125">-TargetResourceId</span></span>
<span data-ttu-id="41e5d-126">ID risorsa di destinazione.</span><span class="sxs-lookup"><span data-stu-id="41e5d-126">The target resource ID.</span></span>

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

### <span data-ttu-id="41e5d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41e5d-127">CommonParameters</span></span>
<span data-ttu-id="41e5d-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41e5d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41e5d-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41e5d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41e5d-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="41e5d-130">INPUTS</span></span>

### <span data-ttu-id="41e5d-131">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="41e5d-131">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="41e5d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="41e5d-132">System.String</span></span>

## <span data-ttu-id="41e5d-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="41e5d-133">OUTPUTS</span></span>

### <span data-ttu-id="41e5d-134">Microsoft. Azure. Commands. Network. Models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="41e5d-134">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="41e5d-135">Note</span><span class="sxs-lookup"><span data-stu-id="41e5d-135">NOTES</span></span>
<span data-ttu-id="41e5d-136">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher, risoluzione dei problemi, VPN, connessione</span><span class="sxs-lookup"><span data-stu-id="41e5d-136">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="41e5d-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="41e5d-137">RELATED LINKS</span></span>

[<span data-ttu-id="41e5d-138">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="41e5d-138">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="41e5d-139">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="41e5d-139">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="41e5d-140">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="41e5d-140">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="41e5d-141">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="41e5d-141">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="41e5d-142">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="41e5d-142">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="41e5d-143">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="41e5d-143">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="41e5d-144">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="41e5d-144">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="41e5d-145">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="41e5d-145">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="41e5d-146">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="41e5d-146">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="41e5d-147">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="41e5d-147">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="41e5d-148">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="41e5d-148">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="41e5d-149">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="41e5d-149">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="41e5d-150">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="41e5d-150">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)
