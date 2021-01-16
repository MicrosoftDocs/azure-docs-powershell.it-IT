---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 3fe26c99dd92afb65105008524908a10dec02e0e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334612"
---
# <span data-ttu-id="140b7-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="140b7-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="140b7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="140b7-102">SYNOPSIS</span></span>
<span data-ttu-id="140b7-103">Ottiene il punteggio relativo alla latenza per i provider di servizi Internet da una posizione specificata alle aree di Azure.</span><span class="sxs-lookup"><span data-stu-id="140b7-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="140b7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="140b7-104">SYNTAX</span></span>

### <span data-ttu-id="140b7-105">SetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="140b7-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <String[]>] [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="140b7-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="140b7-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="140b7-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="140b7-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String> [-Provider <String[]>] [-Location <String[]>]
 -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="140b7-108">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="140b7-108">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherLocation <String> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="140b7-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="140b7-109">DESCRIPTION</span></span>
<span data-ttu-id="140b7-110">Il Get-AzNetworkWatcherReachabilityReport ottiene il punteggio relativo alla latenza per i provider di servizi Internet da una posizione specificata alle aree di Azure.</span><span class="sxs-lookup"><span data-stu-id="140b7-110">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="140b7-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="140b7-111">EXAMPLES</span></span>

### <span data-ttu-id="140b7-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="140b7-112">Example 1</span></span>
```powershell
$nw = Get-AzNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher $nw -Location "West US" -Country "United States" -StartTime "2017-10-10" -EndTime "2017-10-12"

"aggregationLevel" : "Country",
"providerLocation" : {
    "country" : "United States"
},
"reachabilityReport" : [
    {
        "provider" : "Frontier Communications of America, Inc. - ASN 5650",
        "azureLocation": "West US",
        "latencies": [
            {
                "timeStamp": "2017-10-10T00:00:00Z",
                "score": 94
            },
            {
                "timeStamp": "2017-10-11T00:00:00Z",
                "score": 94
            },
            {
                "timeStamp": "2017-10-12T00:00:00Z",
                "score": 94    
            }
        ]  
    }
]
```

<span data-ttu-id="140b7-113">Ottiene le latenze relative al Data Center di Azure in West US da 2017-10-10 a 2017-10-12 all'interno dello stato United.</span><span class="sxs-lookup"><span data-stu-id="140b7-113">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

### <span data-ttu-id="140b7-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="140b7-114">Example 2</span></span>

<span data-ttu-id="140b7-115">Ottiene il punteggio relativo alla latenza per i provider di servizi Internet da una posizione specificata alle aree di Azure.</span><span class="sxs-lookup"><span data-stu-id="140b7-115">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span> <span data-ttu-id="140b7-116">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="140b7-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNetworkWatcherReachabilityReport -Country 'United States' -EndTime '2017-10-12' -Location 'West US' -NetworkWatcherName nw1 -ResourceGroupName myresourcegroup -StartTime '2017-10-10' -State 'washington'
```

## <span data-ttu-id="140b7-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="140b7-117">PARAMETERS</span></span>

### <span data-ttu-id="140b7-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="140b7-118">-AsJob</span></span>
<span data-ttu-id="140b7-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="140b7-119">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="140b7-120">-Città</span><span class="sxs-lookup"><span data-stu-id="140b7-120">-City</span></span>
<span data-ttu-id="140b7-121">Nome della città.</span><span class="sxs-lookup"><span data-stu-id="140b7-121">The name of the city.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="140b7-122">-Paese</span><span class="sxs-lookup"><span data-stu-id="140b7-122">-Country</span></span>
<span data-ttu-id="140b7-123">Nome del paese.</span><span class="sxs-lookup"><span data-stu-id="140b7-123">The name of the country.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="140b7-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="140b7-124">-DefaultProfile</span></span>
<span data-ttu-id="140b7-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="140b7-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="140b7-126">-EndTime</span><span class="sxs-lookup"><span data-stu-id="140b7-126">-EndTime</span></span>
<span data-ttu-id="140b7-127">Ora di fine per il report di accessibilità di Azure.</span><span class="sxs-lookup"><span data-stu-id="140b7-127">The end time for the Azure reachability report.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="140b7-128">-Posizione</span><span class="sxs-lookup"><span data-stu-id="140b7-128">-Location</span></span>
<span data-ttu-id="140b7-129">Aree di Azure facoltative per l'ambito della query.</span><span class="sxs-lookup"><span data-stu-id="140b7-129">Optional Azure regions to scope the query to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="140b7-130">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="140b7-130">-NetworkWatcher</span></span>
<span data-ttu-id="140b7-131">Risorsa Watcher di rete</span><span class="sxs-lookup"><span data-stu-id="140b7-131">The network watcher resource</span></span>

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

### <span data-ttu-id="140b7-132">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="140b7-132">-NetworkWatcherLocation</span></span>
<span data-ttu-id="140b7-133">Posizione del monitoraggio della rete.</span><span class="sxs-lookup"><span data-stu-id="140b7-133">Location of the network watcher.</span></span>

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

### <span data-ttu-id="140b7-134">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="140b7-134">-NetworkWatcherName</span></span>
<span data-ttu-id="140b7-135">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="140b7-135">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: ResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="140b7-136">-Provider</span><span class="sxs-lookup"><span data-stu-id="140b7-136">-Provider</span></span>
<span data-ttu-id="140b7-137">Elenco dei provider di servizi Internet.</span><span class="sxs-lookup"><span data-stu-id="140b7-137">List of Internet service providers.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="140b7-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="140b7-138">-ResourceGroupName</span></span>
<span data-ttu-id="140b7-139">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="140b7-139">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="140b7-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="140b7-140">-ResourceId</span></span>
<span data-ttu-id="140b7-141">ID della risorsa Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="140b7-141">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="140b7-142">-StartTime</span><span class="sxs-lookup"><span data-stu-id="140b7-142">-StartTime</span></span>
<span data-ttu-id="140b7-143">Ora di inizio per il report di raggiungibilità di Azure.</span><span class="sxs-lookup"><span data-stu-id="140b7-143">The start time for the Azure reachability report.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="140b7-144">-Stato</span><span class="sxs-lookup"><span data-stu-id="140b7-144">-State</span></span>
<span data-ttu-id="140b7-145">Nome dello stato.</span><span class="sxs-lookup"><span data-stu-id="140b7-145">The name of the state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="140b7-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="140b7-146">CommonParameters</span></span>
<span data-ttu-id="140b7-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="140b7-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="140b7-148">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="140b7-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="140b7-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="140b7-149">INPUTS</span></span>

### <span data-ttu-id="140b7-150">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="140b7-150">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="140b7-151">System. String</span><span class="sxs-lookup"><span data-stu-id="140b7-151">System.String</span></span>

## <span data-ttu-id="140b7-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="140b7-152">OUTPUTS</span></span>

### <span data-ttu-id="140b7-153">Microsoft. Azure. Commands. Network. Models. PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="140b7-153">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="140b7-154">Note</span><span class="sxs-lookup"><span data-stu-id="140b7-154">NOTES</span></span>
<span data-ttu-id="140b7-155">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher, raggiungibilità, report</span><span class="sxs-lookup"><span data-stu-id="140b7-155">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="140b7-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="140b7-156">RELATED LINKS</span></span>

[<span data-ttu-id="140b7-157">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="140b7-157">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="140b7-158">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="140b7-158">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="140b7-159">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="140b7-159">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="140b7-160">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="140b7-160">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="140b7-161">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="140b7-161">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="140b7-162">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="140b7-162">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="140b7-163">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="140b7-163">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="140b7-164">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="140b7-164">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="140b7-165">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="140b7-165">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="140b7-166">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="140b7-166">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="140b7-167">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="140b7-167">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="140b7-168">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="140b7-168">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="140b7-169">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="140b7-169">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="140b7-170">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="140b7-170">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="140b7-171">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="140b7-171">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="140b7-172">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="140b7-172">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="140b7-173">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="140b7-173">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="140b7-174">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="140b7-174">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="140b7-175">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="140b7-175">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="140b7-176">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="140b7-176">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="140b7-177">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="140b7-177">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="140b7-178">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="140b7-178">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="140b7-179">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="140b7-179">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="140b7-180">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="140b7-180">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="140b7-181">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="140b7-181">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="140b7-182">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="140b7-182">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="140b7-183">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="140b7-183">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
