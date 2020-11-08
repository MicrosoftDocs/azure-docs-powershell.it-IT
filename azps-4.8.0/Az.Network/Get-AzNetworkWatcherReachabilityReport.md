---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 3fe26c99dd92afb65105008524908a10dec02e0e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189029"
---
# <span data-ttu-id="72bec-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="72bec-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="72bec-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="72bec-102">SYNOPSIS</span></span>
<span data-ttu-id="72bec-103">Ottiene il punteggio relativo alla latenza per i provider di servizi Internet da una posizione specificata alle aree di Azure.</span><span class="sxs-lookup"><span data-stu-id="72bec-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="72bec-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="72bec-104">SYNTAX</span></span>

### <span data-ttu-id="72bec-105">SetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="72bec-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <String[]>] [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72bec-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="72bec-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72bec-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="72bec-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String> [-Provider <String[]>] [-Location <String[]>]
 -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72bec-108">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="72bec-108">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherLocation <String> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72bec-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="72bec-109">DESCRIPTION</span></span>
<span data-ttu-id="72bec-110">Il Get-AzNetworkWatcherReachabilityReport ottiene il punteggio relativo alla latenza per i provider di servizi Internet da una posizione specificata alle aree di Azure.</span><span class="sxs-lookup"><span data-stu-id="72bec-110">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="72bec-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="72bec-111">EXAMPLES</span></span>

### <span data-ttu-id="72bec-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="72bec-112">Example 1</span></span>
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

<span data-ttu-id="72bec-113">Ottiene le latenze relative al Data Center di Azure in West US da 2017-10-10 a 2017-10-12 all'interno dello stato United.</span><span class="sxs-lookup"><span data-stu-id="72bec-113">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

### <span data-ttu-id="72bec-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="72bec-114">Example 2</span></span>

<span data-ttu-id="72bec-115">Ottiene il punteggio relativo alla latenza per i provider di servizi Internet da una posizione specificata alle aree di Azure.</span><span class="sxs-lookup"><span data-stu-id="72bec-115">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span> <span data-ttu-id="72bec-116">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="72bec-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNetworkWatcherReachabilityReport -Country 'United States' -EndTime '2017-10-12' -Location 'West US' -NetworkWatcherName nw1 -ResourceGroupName myresourcegroup -StartTime '2017-10-10' -State 'washington'
```

## <span data-ttu-id="72bec-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="72bec-117">PARAMETERS</span></span>

### <span data-ttu-id="72bec-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="72bec-118">-AsJob</span></span>
<span data-ttu-id="72bec-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="72bec-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="72bec-120">-Città</span><span class="sxs-lookup"><span data-stu-id="72bec-120">-City</span></span>
<span data-ttu-id="72bec-121">Nome della città.</span><span class="sxs-lookup"><span data-stu-id="72bec-121">The name of the city.</span></span>

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

### <span data-ttu-id="72bec-122">-Paese</span><span class="sxs-lookup"><span data-stu-id="72bec-122">-Country</span></span>
<span data-ttu-id="72bec-123">Nome del paese.</span><span class="sxs-lookup"><span data-stu-id="72bec-123">The name of the country.</span></span>

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

### <span data-ttu-id="72bec-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72bec-124">-DefaultProfile</span></span>
<span data-ttu-id="72bec-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="72bec-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72bec-126">-EndTime</span><span class="sxs-lookup"><span data-stu-id="72bec-126">-EndTime</span></span>
<span data-ttu-id="72bec-127">Ora di fine per il report di accessibilità di Azure.</span><span class="sxs-lookup"><span data-stu-id="72bec-127">The end time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="72bec-128">-Posizione</span><span class="sxs-lookup"><span data-stu-id="72bec-128">-Location</span></span>
<span data-ttu-id="72bec-129">Aree di Azure facoltative per l'ambito della query.</span><span class="sxs-lookup"><span data-stu-id="72bec-129">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="72bec-130">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="72bec-130">-NetworkWatcher</span></span>
<span data-ttu-id="72bec-131">Risorsa Watcher di rete</span><span class="sxs-lookup"><span data-stu-id="72bec-131">The network watcher resource</span></span>

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

### <span data-ttu-id="72bec-132">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="72bec-132">-NetworkWatcherLocation</span></span>
<span data-ttu-id="72bec-133">Posizione del monitoraggio della rete.</span><span class="sxs-lookup"><span data-stu-id="72bec-133">Location of the network watcher.</span></span>

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

### <span data-ttu-id="72bec-134">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="72bec-134">-NetworkWatcherName</span></span>
<span data-ttu-id="72bec-135">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="72bec-135">The name of network watcher.</span></span>

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

### <span data-ttu-id="72bec-136">-Provider</span><span class="sxs-lookup"><span data-stu-id="72bec-136">-Provider</span></span>
<span data-ttu-id="72bec-137">Elenco dei provider di servizi Internet.</span><span class="sxs-lookup"><span data-stu-id="72bec-137">List of Internet service providers.</span></span>

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

### <span data-ttu-id="72bec-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72bec-138">-ResourceGroupName</span></span>
<span data-ttu-id="72bec-139">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="72bec-139">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="72bec-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="72bec-140">-ResourceId</span></span>
<span data-ttu-id="72bec-141">ID della risorsa Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="72bec-141">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="72bec-142">-StartTime</span><span class="sxs-lookup"><span data-stu-id="72bec-142">-StartTime</span></span>
<span data-ttu-id="72bec-143">Ora di inizio per il report di raggiungibilità di Azure.</span><span class="sxs-lookup"><span data-stu-id="72bec-143">The start time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="72bec-144">-Stato</span><span class="sxs-lookup"><span data-stu-id="72bec-144">-State</span></span>
<span data-ttu-id="72bec-145">Nome dello stato.</span><span class="sxs-lookup"><span data-stu-id="72bec-145">The name of the state.</span></span>

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

### <span data-ttu-id="72bec-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72bec-146">CommonParameters</span></span>
<span data-ttu-id="72bec-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72bec-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72bec-148">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72bec-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72bec-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="72bec-149">INPUTS</span></span>

### <span data-ttu-id="72bec-150">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="72bec-150">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="72bec-151">System. String</span><span class="sxs-lookup"><span data-stu-id="72bec-151">System.String</span></span>

## <span data-ttu-id="72bec-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="72bec-152">OUTPUTS</span></span>

### <span data-ttu-id="72bec-153">Microsoft. Azure. Commands. Network. Models. PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="72bec-153">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="72bec-154">Note</span><span class="sxs-lookup"><span data-stu-id="72bec-154">NOTES</span></span>
<span data-ttu-id="72bec-155">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher, raggiungibilità, report</span><span class="sxs-lookup"><span data-stu-id="72bec-155">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="72bec-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="72bec-156">RELATED LINKS</span></span>

[<span data-ttu-id="72bec-157">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="72bec-157">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="72bec-158">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="72bec-158">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="72bec-159">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="72bec-159">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="72bec-160">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="72bec-160">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="72bec-161">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="72bec-161">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="72bec-162">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="72bec-162">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="72bec-163">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="72bec-163">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="72bec-164">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="72bec-164">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="72bec-165">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="72bec-165">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="72bec-166">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="72bec-166">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="72bec-167">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="72bec-167">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="72bec-168">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="72bec-168">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="72bec-169">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="72bec-169">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="72bec-170">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="72bec-170">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="72bec-171">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="72bec-171">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="72bec-172">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="72bec-172">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="72bec-173">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="72bec-173">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="72bec-174">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="72bec-174">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="72bec-175">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="72bec-175">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="72bec-176">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="72bec-176">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="72bec-177">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="72bec-177">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="72bec-178">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="72bec-178">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="72bec-179">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="72bec-179">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="72bec-180">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="72bec-180">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="72bec-181">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="72bec-181">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="72bec-182">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="72bec-182">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="72bec-183">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="72bec-183">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
