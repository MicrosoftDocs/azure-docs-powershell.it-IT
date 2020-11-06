---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: a78114bbf47113983453a0dd5c1e13db0fc73a6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511124"
---
# <span data-ttu-id="5c44f-101">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5c44f-101">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="5c44f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5c44f-102">SYNOPSIS</span></span>
<span data-ttu-id="5c44f-103">Restituisce il monitor di connessione con il nome specificato o l'elenco dei monitor di connessione</span><span class="sxs-lookup"><span data-stu-id="5c44f-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c44f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5c44f-104">SYNTAX</span></span>

### <span data-ttu-id="5c44f-105">SetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5c44f-105">SetByName (Default)</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c44f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="5c44f-106">SetByResource</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c44f-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="5c44f-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -Location <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c44f-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5c44f-108">SetByResourceId</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5c44f-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5c44f-109">DESCRIPTION</span></span>
<span data-ttu-id="5c44f-110">Il cmdlet Get-AzureRmNetworkWatcherConnectionMonitor restituisce il monitor di connessione con il nome/resourceId specificato o l'elenco di monitor di connessione corrispondente alla posizione/Watcher di rete specificata.</span><span class="sxs-lookup"><span data-stu-id="5c44f-110">The Get-AzureRmNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="5c44f-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5c44f-111">EXAMPLES</span></span>

### <span data-ttu-id="5c44f-112">Esempio 1: ottenere il monitoraggio della connessione per nome nella posizione specificata</span><span class="sxs-lookup"><span data-stu-id="5c44f-112">Example 1: Get connection monitor by name in the specified location</span></span>
```
PS C:\> Get-AzureRmNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm


Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/cm
Etag                        : W/"40961b58-e379-4204-a47b-0c477739b095"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/96e68903-0a56-4819-9987-8d08ad6
                              a1f99/resourceGroups/VarunRgCentralUSEUAP/providers/Microsoft.C
                              ompute/virtualMachines/irinavm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "google.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:19:28 PM
MonitoringStatus            : Stopped
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {
                                "key1": "value1"
                              }
```

<span data-ttu-id="5c44f-113">In questo esempio otteniamo il monitoraggio delle connessioni per nome nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="5c44f-113">In this example we get connection monitor by name in the specified location.</span></span>

## <span data-ttu-id="5c44f-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5c44f-114">PARAMETERS</span></span>

### <span data-ttu-id="5c44f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c44f-115">-DefaultProfile</span></span>
<span data-ttu-id="5c44f-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5c44f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c44f-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="5c44f-117">-Location</span></span>
<span data-ttu-id="5c44f-118">Posizione del monitoraggio della rete.</span><span class="sxs-lookup"><span data-stu-id="5c44f-118">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c44f-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="5c44f-119">-Name</span></span>
<span data-ttu-id="5c44f-120">Nome del monitor della connessione.</span><span class="sxs-lookup"><span data-stu-id="5c44f-120">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c44f-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5c44f-121">-NetworkWatcher</span></span>
<span data-ttu-id="5c44f-122">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="5c44f-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="5c44f-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="5c44f-123">-NetworkWatcherName</span></span>
<span data-ttu-id="5c44f-124">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="5c44f-124">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c44f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c44f-125">-ResourceGroupName</span></span>
<span data-ttu-id="5c44f-126">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="5c44f-126">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c44f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c44f-127">-ResourceId</span></span>
<span data-ttu-id="5c44f-128">ID risorsa del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="5c44f-128">Resource ID of the connection monitor.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c44f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c44f-129">CommonParameters</span></span>
<span data-ttu-id="5c44f-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c44f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5c44f-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c44f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c44f-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5c44f-132">INPUTS</span></span>

### <span data-ttu-id="5c44f-133">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5c44f-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="5c44f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="5c44f-134">System.String</span></span>

## <span data-ttu-id="5c44f-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5c44f-135">OUTPUTS</span></span>

### <span data-ttu-id="5c44f-136">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="5c44f-136">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="5c44f-137">Note</span><span class="sxs-lookup"><span data-stu-id="5c44f-137">NOTES</span></span>
<span data-ttu-id="5c44f-138">Parole chiave: Azure, azurerm, ARM, Resource, Connectivity, Management, Manager, Network, networking, Network Watcher, Connection Monitor</span><span class="sxs-lookup"><span data-stu-id="5c44f-138">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="5c44f-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5c44f-139">RELATED LINKS</span></span>

[<span data-ttu-id="5c44f-140">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5c44f-140">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="5c44f-141">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5c44f-141">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="5c44f-142">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5c44f-142">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="5c44f-143">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="5c44f-143">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="5c44f-144">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="5c44f-144">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="5c44f-145">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="5c44f-145">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="5c44f-146">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="5c44f-146">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="5c44f-147">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5c44f-147">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="5c44f-148">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="5c44f-148">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="5c44f-149">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5c44f-149">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="5c44f-150">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5c44f-150">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="5c44f-151">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5c44f-151">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="5c44f-152">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5c44f-152">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="5c44f-153">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="5c44f-153">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="5c44f-154">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5c44f-154">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="5c44f-155">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5c44f-155">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="5c44f-156">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5c44f-156">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="5c44f-157">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5c44f-157">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()
