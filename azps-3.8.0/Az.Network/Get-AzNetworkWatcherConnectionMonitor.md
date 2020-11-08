---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: c2da2b9173b3977a606699fd8e1def3dae2a68d9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021270"
---
# <span data-ttu-id="b2d5f-101">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b2d5f-101">Get-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="b2d5f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b2d5f-102">SYNOPSIS</span></span>
<span data-ttu-id="b2d5f-103">Restituisce il monitor di connessione con il nome specificato o l'elenco dei monitor di connessione</span><span class="sxs-lookup"><span data-stu-id="b2d5f-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

## <span data-ttu-id="b2d5f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b2d5f-104">SYNTAX</span></span>

### <span data-ttu-id="b2d5f-105">SetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b2d5f-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2d5f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b2d5f-106">SetByResource</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2d5f-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="b2d5f-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2d5f-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b2d5f-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b2d5f-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2d5f-109">DESCRIPTION</span></span>
<span data-ttu-id="b2d5f-110">Il cmdlet Get-AzNetworkWatcherConnectionMonitor restituisce il monitor di connessione con il nome/resourceId specificato o l'elenco di monitor di connessione corrispondente alla posizione/Watcher di rete specificata.</span><span class="sxs-lookup"><span data-stu-id="b2d5f-110">The Get-AzNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="b2d5f-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b2d5f-111">EXAMPLES</span></span>

### <span data-ttu-id="b2d5f-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b2d5f-112">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm
```

<span data-ttu-id="b2d5f-113">Nome: cm ID:/subscriptions/00000000-0000-0000-0000-000000000000/resourceGro UPS/NetworkWatcherRG/Providers/Microsoft. Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/cm ETag: W/"40961b58-e379-4204-a47b-0c477739b095" ProvisioningState: succeeded Source: {"ResourceId": "/subscriptions/96e68903-0a56-4819-9987-8d08ad6 a1f99/resourceGroups/VarunRgCentralUSEUAP/Providers/Microsoft. C ompute/virtualMachines/irinavm", "porta": 0} destinazione: {"Address": "google.com", "Port": 80} MonitoringIntervalInSeconds: 60 autostart: true StartTime: 1/12/2018 7:19:28 PM MonitoringStatus: Stopped location: centraluseuap Type: Microsoft. Network/networkWatchers/connectionMonitors Tags: {"Key1": "value1"}</span><span class="sxs-lookup"><span data-stu-id="b2d5f-113">Name                        : cm Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/cm Etag                        : W/"40961b58-e379-4204-a47b-0c477739b095" ProvisioningState           : Succeeded Source                      : { "ResourceId": "/subscriptions/96e68903-0a56-4819-9987-8d08ad6 a1f99/resourceGroups/VarunRgCentralUSEUAP/providers/Microsoft.C ompute/virtualMachines/irinavm", "Port": 0 } Destination                 : { "Address": "google.com", "Port": 80 } MonitoringIntervalInSeconds : 60 AutoStart                   : True StartTime                   : 1/12/2018 7:19:28 PM MonitoringStatus            : Stopped Location                    : centraluseuap Type                        : Microsoft.Network/networkWatchers/connectionMonitors Tags                        : { "key1": "value1" }</span></span>

## <span data-ttu-id="b2d5f-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b2d5f-114">PARAMETERS</span></span>

### <span data-ttu-id="b2d5f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2d5f-115">-DefaultProfile</span></span>
<span data-ttu-id="b2d5f-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b2d5f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2d5f-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="b2d5f-117">-Location</span></span>
<span data-ttu-id="b2d5f-118">Posizione del monitoraggio della rete.</span><span class="sxs-lookup"><span data-stu-id="b2d5f-118">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2d5f-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="b2d5f-119">-Name</span></span>
<span data-ttu-id="b2d5f-120">Nome del monitor della connessione.</span><span class="sxs-lookup"><span data-stu-id="b2d5f-120">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2d5f-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b2d5f-121">-NetworkWatcher</span></span>
<span data-ttu-id="b2d5f-122">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="b2d5f-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="b2d5f-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="b2d5f-123">-NetworkWatcherName</span></span>
<span data-ttu-id="b2d5f-124">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="b2d5f-124">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2d5f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2d5f-125">-ResourceGroupName</span></span>
<span data-ttu-id="b2d5f-126">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="b2d5f-126">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2d5f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2d5f-127">-ResourceId</span></span>
<span data-ttu-id="b2d5f-128">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="b2d5f-128">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2d5f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2d5f-129">CommonParameters</span></span>
<span data-ttu-id="b2d5f-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2d5f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2d5f-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2d5f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2d5f-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b2d5f-132">INPUTS</span></span>

### <span data-ttu-id="b2d5f-133">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b2d5f-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="b2d5f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b2d5f-134">System.String</span></span>

## <span data-ttu-id="b2d5f-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b2d5f-135">OUTPUTS</span></span>

### <span data-ttu-id="b2d5f-136">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="b2d5f-136">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="b2d5f-137">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="b2d5f-137">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="b2d5f-138">Note</span><span class="sxs-lookup"><span data-stu-id="b2d5f-138">NOTES</span></span>

## <span data-ttu-id="b2d5f-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b2d5f-139">RELATED LINKS</span></span>
