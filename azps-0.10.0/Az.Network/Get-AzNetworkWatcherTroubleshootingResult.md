---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchertroubleshootingresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
ms.openlocfilehash: c3d1e7e3a76a2561c77c8d580b7365f8fd2e6fee
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860709"
---
# <span data-ttu-id="dce98-101">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="dce98-101">Get-AzNetworkWatcherTroubleshootingResult</span></span>

## <span data-ttu-id="dce98-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dce98-102">SYNOPSIS</span></span>
<span data-ttu-id="dce98-103">Ottiene il risultato della risoluzione dei problemi dell'operazione di risoluzione dei problemi eseguita in precedenza o attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="dce98-103">Gets the troubleshooting result from the previously run or currently running troubleshooting operation.</span></span>

## <span data-ttu-id="dce98-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dce98-104">SYNTAX</span></span>

### <span data-ttu-id="dce98-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dce98-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dce98-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="dce98-106">SetByName</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dce98-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dce98-107">DESCRIPTION</span></span>
<span data-ttu-id="dce98-108">Il cmdlet Get-AzNetworkWatcherTroubleshootingResult ottiene il risultato della risoluzione dei problemi dell'operazione eseguita in precedenza o attualmente in esecuzione Start-AzNetworkWatcherResourceTroubleshooting.</span><span class="sxs-lookup"><span data-stu-id="dce98-108">The Get-AzNetworkWatcherTroubleshootingResult cmdlet gets the troubleshooting result from the previously run or currently running Start-AzNetworkWatcherResourceTroubleshooting operation.</span></span> <span data-ttu-id="dce98-109">Se l'operazione di risoluzione dei problemi è attualmente in corso, questa operazione può richiedere alcuni minuti per il completamento.</span><span class="sxs-lookup"><span data-stu-id="dce98-109">If the troubleshooting operation is currently in progress, then this operation may take a few minutes to complete.</span></span> <span data-ttu-id="dce98-110">Attualmente sono supportati i gateway e le connessioni di rete virtuali.</span><span class="sxs-lookup"><span data-stu-id="dce98-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="dce98-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dce98-111">EXAMPLES</span></span>

### <span data-ttu-id="dce98-112">---Esempio 1: avviare la risoluzione dei problemi su un gateway di rete virtuale e recuperare i risultati---</span><span class="sxs-lookup"><span data-stu-id="dce98-112">--- Example 1: Start Troubleshooting on a Virtual Network Gateway and Retrieve Result ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath

Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher $NW -TargetResourceId $target
```

<span data-ttu-id="dce98-113">L'esempio precedente avvia la risoluzione dei problemi in un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="dce98-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="dce98-114">L'operazione può richiedere alcuni minuti per il completamento.</span><span class="sxs-lookup"><span data-stu-id="dce98-114">The operation may take a few minutes to complete.</span></span>
<span data-ttu-id="dce98-115">Dopo aver avviato la risoluzione dei problemi, viene eseguita una chiamata Get-AzNetworkWatcherTroubleshootingResult alla risorsa per recuperare il risultato di questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="dce98-115">After troubleshooting has started, a Get-AzNetworkWatcherTroubleshootingResult call is made to the resource to retrieve the result of this call.</span></span> 

## <span data-ttu-id="dce98-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dce98-116">PARAMETERS</span></span>

### <span data-ttu-id="dce98-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dce98-117">-DefaultProfile</span></span>
<span data-ttu-id="dce98-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dce98-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dce98-119">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dce98-119">-NetworkWatcher</span></span>
<span data-ttu-id="dce98-120">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="dce98-120">The network watcher resource.</span></span>

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

### <span data-ttu-id="dce98-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="dce98-121">-NetworkWatcherName</span></span>
<span data-ttu-id="dce98-122">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="dce98-122">The name of network watcher.</span></span>

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

### <span data-ttu-id="dce98-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dce98-123">-ResourceGroupName</span></span>
<span data-ttu-id="dce98-124">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="dce98-124">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="dce98-125">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="dce98-125">-TargetResourceId</span></span>
<span data-ttu-id="dce98-126">ID risorsa di destinazione.</span><span class="sxs-lookup"><span data-stu-id="dce98-126">The target resource ID.</span></span>

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

### <span data-ttu-id="dce98-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dce98-127">CommonParameters</span></span>
<span data-ttu-id="dce98-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dce98-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dce98-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dce98-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dce98-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dce98-130">INPUTS</span></span>

### <span data-ttu-id="dce98-131">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dce98-131">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="dce98-132">System. String</span><span class="sxs-lookup"><span data-stu-id="dce98-132">System.String</span></span>

## <span data-ttu-id="dce98-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dce98-133">OUTPUTS</span></span>

### <span data-ttu-id="dce98-134">Microsoft. Azure. Commands. Network. Models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="dce98-134">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="dce98-135">Note</span><span class="sxs-lookup"><span data-stu-id="dce98-135">NOTES</span></span>
<span data-ttu-id="dce98-136">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher, risoluzione dei problemi, VPN, connessione</span><span class="sxs-lookup"><span data-stu-id="dce98-136">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="dce98-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dce98-137">RELATED LINKS</span></span>

[<span data-ttu-id="dce98-138">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="dce98-138">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="dce98-139">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dce98-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="dce98-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dce98-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="dce98-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dce98-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="dce98-142">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dce98-142">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dce98-143">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="dce98-143">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="dce98-144">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dce98-144">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dce98-145">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dce98-145">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dce98-146">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dce98-146">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dce98-147">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="dce98-147">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="dce98-148">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="dce98-148">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="dce98-149">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="dce98-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="dce98-150">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="dce98-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)
