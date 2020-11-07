---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-aznetworkwatcherresourcetroubleshooting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
ms.openlocfilehash: a72f494518b3a511eac3e4b1a92330f666bbca64
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862681"
---
# <span data-ttu-id="5d264-101">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="5d264-101">Start-AzNetworkWatcherResourceTroubleshooting</span></span>

## <span data-ttu-id="5d264-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5d264-102">SYNOPSIS</span></span>
<span data-ttu-id="5d264-103">Avvia la risoluzione dei problemi in una risorsa di rete in Azure.</span><span class="sxs-lookup"><span data-stu-id="5d264-103">Starts troubleshooting on a Networking resource in Azure.</span></span>

## <span data-ttu-id="5d264-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5d264-104">SYNTAX</span></span>

### <span data-ttu-id="5d264-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5d264-105">SetByResource (Default)</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher <PSNetworkWatcher>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d264-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="5d264-106">SetByName</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d264-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5d264-107">DESCRIPTION</span></span>
<span data-ttu-id="5d264-108">Il cmdlet Start-AzNetworkWatcherResourceTroubleshooting avvia la risoluzione dei problemi per una risorsa di rete in Azure e restituisce informazioni su potenziali problemi e attenuazioni.</span><span class="sxs-lookup"><span data-stu-id="5d264-108">The Start-AzNetworkWatcherResourceTroubleshooting cmdlet starts troubleshooting for a Networking resource in Azure and returns information about potential issues and mitigations.</span></span> <span data-ttu-id="5d264-109">Attualmente sono supportati i gateway e le connessioni di rete virtuali.</span><span class="sxs-lookup"><span data-stu-id="5d264-109">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="5d264-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5d264-110">EXAMPLES</span></span>

### <span data-ttu-id="5d264-111">---Esempio 1: avviare la risoluzione dei problemi in un gateway di rete virtuale---</span><span class="sxs-lookup"><span data-stu-id="5d264-111">--- Example 1: Start Troubleshooting on a Virtual Network Gateway ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath
```

<span data-ttu-id="5d264-112">L'esempio precedente avvia la risoluzione dei problemi in un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="5d264-112">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="5d264-113">L'operazione può richiedere alcuni minuti per il completamento.</span><span class="sxs-lookup"><span data-stu-id="5d264-113">The operation may take a few minutes to complete.</span></span>

## <span data-ttu-id="5d264-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5d264-114">PARAMETERS</span></span>

### <span data-ttu-id="5d264-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d264-115">-DefaultProfile</span></span>
<span data-ttu-id="5d264-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5d264-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d264-117">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5d264-117">-NetworkWatcher</span></span>
<span data-ttu-id="5d264-118">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="5d264-118">The network watcher resource.</span></span>

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

### <span data-ttu-id="5d264-119">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="5d264-119">-NetworkWatcherName</span></span>
<span data-ttu-id="5d264-120">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="5d264-120">The name of network watcher.</span></span>

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

### <span data-ttu-id="5d264-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d264-121">-ResourceGroupName</span></span>
<span data-ttu-id="5d264-122">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="5d264-122">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="5d264-123">-StorageId</span><span class="sxs-lookup"><span data-stu-id="5d264-123">-StorageId</span></span>
<span data-ttu-id="5d264-124">ID dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="5d264-124">The storage ID.</span></span>

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

### <span data-ttu-id="5d264-125">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="5d264-125">-StoragePath</span></span>
<span data-ttu-id="5d264-126">Percorso di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="5d264-126">The storage path.</span></span>

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

### <span data-ttu-id="5d264-127">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="5d264-127">-TargetResourceId</span></span>
<span data-ttu-id="5d264-128">Specifica l'ID risorsa della risorsa per la risoluzione dei problemi.</span><span class="sxs-lookup"><span data-stu-id="5d264-128">Specifies the resource id of the resource to troubleshoot.</span></span> <span data-ttu-id="5d264-129">Formato di esempio: "/subscriptions/$ {subscriptionId}/resourceGroups/$ {resourceGroupName}/providers/Microsoft.Network/connections/$ {ConnectionName}"</span><span class="sxs-lookup"><span data-stu-id="5d264-129">Example format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span></span>

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

### <span data-ttu-id="5d264-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d264-130">CommonParameters</span></span>
<span data-ttu-id="5d264-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d264-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d264-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d264-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d264-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5d264-133">INPUTS</span></span>

### <span data-ttu-id="5d264-134">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5d264-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="5d264-135">System. String</span><span class="sxs-lookup"><span data-stu-id="5d264-135">System.String</span></span>

## <span data-ttu-id="5d264-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5d264-136">OUTPUTS</span></span>

### <span data-ttu-id="5d264-137">Microsoft. Azure. Commands. Network. Models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="5d264-137">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="5d264-138">Note</span><span class="sxs-lookup"><span data-stu-id="5d264-138">NOTES</span></span>
<span data-ttu-id="5d264-139">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher, risoluzione dei problemi, VPN, connessione</span><span class="sxs-lookup"><span data-stu-id="5d264-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="5d264-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5d264-140">RELATED LINKS</span></span>

[<span data-ttu-id="5d264-141">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="5d264-141">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="5d264-142">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5d264-142">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="5d264-143">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5d264-143">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="5d264-144">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5d264-144">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="5d264-145">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5d264-145">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5d264-146">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="5d264-146">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="5d264-147">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5d264-147">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5d264-148">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5d264-148">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5d264-149">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5d264-149">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5d264-150">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="5d264-150">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="5d264-151">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="5d264-151">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="5d264-152">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="5d264-152">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="5d264-153">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="5d264-153">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)
