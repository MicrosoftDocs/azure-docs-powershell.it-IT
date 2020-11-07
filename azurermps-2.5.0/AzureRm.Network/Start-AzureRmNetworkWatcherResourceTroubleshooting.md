---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermnetworkwatcherresourcetroubleshooting
schema: 2.0.0
ms.openlocfilehash: 411b70fb6018b71b1c1c7fbf67816d0c86e6d3b6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866030"
---
# <span data-ttu-id="26f8b-101">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="26f8b-101">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>

## <span data-ttu-id="26f8b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="26f8b-102">SYNOPSIS</span></span>
<span data-ttu-id="26f8b-103">Avvia la risoluzione dei problemi in una risorsa di rete in Azure.</span><span class="sxs-lookup"><span data-stu-id="26f8b-103">Starts troubleshooting on a Networking resource in Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26f8b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="26f8b-104">SYNTAX</span></span>

### <span data-ttu-id="26f8b-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="26f8b-105">SetByResource (Default)</span></span>
```
Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcher <PSNetworkWatcher>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26f8b-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="26f8b-106">SetByName</span></span>
```
Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26f8b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26f8b-107">DESCRIPTION</span></span>
<span data-ttu-id="26f8b-108">Il cmdlet Start-AzureRmNetworkWatcherResourceTroubleshooting avvia la risoluzione dei problemi per una risorsa di rete in Azure e restituisce informazioni su potenziali problemi e attenuazioni.</span><span class="sxs-lookup"><span data-stu-id="26f8b-108">The Start-AzureRmNetworkWatcherResourceTroubleshooting cmdlet starts troubleshooting for a Networking resource in Azure and returns information about potential issues and mitigations.</span></span> <span data-ttu-id="26f8b-109">Attualmente sono supportati i gateway e le connessioni di rete virtuali.</span><span class="sxs-lookup"><span data-stu-id="26f8b-109">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="26f8b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="26f8b-110">EXAMPLES</span></span>

### <span data-ttu-id="26f8b-111">---Esempio 1: avviare la risoluzione dei problemi in un gateway di rete virtuale---</span><span class="sxs-lookup"><span data-stu-id="26f8b-111">--- Example 1: Start Troubleshooting on a Virtual Network Gateway ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath
```

<span data-ttu-id="26f8b-112">L'esempio precedente avvia la risoluzione dei problemi in un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="26f8b-112">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="26f8b-113">L'operazione può richiedere alcuni minuti per il completamento.</span><span class="sxs-lookup"><span data-stu-id="26f8b-113">The operation may take a few minutes to complete.</span></span>

## <span data-ttu-id="26f8b-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="26f8b-114">PARAMETERS</span></span>

### <span data-ttu-id="26f8b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26f8b-115">-DefaultProfile</span></span>
<span data-ttu-id="26f8b-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="26f8b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26f8b-117">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="26f8b-117">-NetworkWatcher</span></span>
<span data-ttu-id="26f8b-118">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="26f8b-118">The network watcher resource.</span></span>

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

### <span data-ttu-id="26f8b-119">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="26f8b-119">-NetworkWatcherName</span></span>
<span data-ttu-id="26f8b-120">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="26f8b-120">The name of network watcher.</span></span>

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

### <span data-ttu-id="26f8b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26f8b-121">-ResourceGroupName</span></span>
<span data-ttu-id="26f8b-122">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="26f8b-122">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="26f8b-123">-StorageId</span><span class="sxs-lookup"><span data-stu-id="26f8b-123">-StorageId</span></span>
<span data-ttu-id="26f8b-124">ID dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="26f8b-124">The storage ID.</span></span>

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

### <span data-ttu-id="26f8b-125">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="26f8b-125">-StoragePath</span></span>
<span data-ttu-id="26f8b-126">Percorso di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="26f8b-126">The storage path.</span></span>

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

### <span data-ttu-id="26f8b-127">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="26f8b-127">-TargetResourceId</span></span>
<span data-ttu-id="26f8b-128">Specifica l'ID risorsa della risorsa per la risoluzione dei problemi.</span><span class="sxs-lookup"><span data-stu-id="26f8b-128">Specifies the resource id of the resource to troubleshoot.</span></span> <span data-ttu-id="26f8b-129">Formato di esempio: "/subscriptions/$ {subscriptionId}/resourceGroups/$ {resourceGroupName}/providers/Microsoft.Network/connections/$ {ConnectionName}"</span><span class="sxs-lookup"><span data-stu-id="26f8b-129">Example format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span></span>

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

### <span data-ttu-id="26f8b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26f8b-130">CommonParameters</span></span>
<span data-ttu-id="26f8b-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26f8b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26f8b-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26f8b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26f8b-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="26f8b-133">INPUTS</span></span>

### <span data-ttu-id="26f8b-134">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="26f8b-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="26f8b-135">System. String</span><span class="sxs-lookup"><span data-stu-id="26f8b-135">System.String</span></span>

## <span data-ttu-id="26f8b-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="26f8b-136">OUTPUTS</span></span>

### <span data-ttu-id="26f8b-137">Microsoft. Azure. Commands. Network. Models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="26f8b-137">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="26f8b-138">Note</span><span class="sxs-lookup"><span data-stu-id="26f8b-138">NOTES</span></span>
<span data-ttu-id="26f8b-139">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher, risoluzione dei problemi, VPN, connessione</span><span class="sxs-lookup"><span data-stu-id="26f8b-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="26f8b-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="26f8b-140">RELATED LINKS</span></span>

[<span data-ttu-id="26f8b-141">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="26f8b-141">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="26f8b-142">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="26f8b-142">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="26f8b-143">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="26f8b-143">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="26f8b-144">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="26f8b-144">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="26f8b-145">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="26f8b-145">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="26f8b-146">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="26f8b-146">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="26f8b-147">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="26f8b-147">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="26f8b-148">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="26f8b-148">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="26f8b-149">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="26f8b-149">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="26f8b-150">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="26f8b-150">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="26f8b-151">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="26f8b-151">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="26f8b-152">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="26f8b-152">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="26f8b-153">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="26f8b-153">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)
