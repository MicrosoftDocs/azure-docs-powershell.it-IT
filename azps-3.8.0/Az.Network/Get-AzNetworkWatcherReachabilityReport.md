---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 0ad2b1fa6278e085a57d94f2fec9be2c6853993d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864641"
---
# <span data-ttu-id="81730-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="81730-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="81730-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="81730-102">SYNOPSIS</span></span>
<span data-ttu-id="81730-103">Ottiene il punteggio relativo alla latenza per i provider di servizi Internet da una posizione specificata alle aree di Azure.</span><span class="sxs-lookup"><span data-stu-id="81730-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="81730-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="81730-104">SYNTAX</span></span>

### <span data-ttu-id="81730-105">SetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="81730-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <String[]>] [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81730-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="81730-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81730-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="81730-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String> [-Provider <String[]>] [-Location <String[]>]
 -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81730-108">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="81730-108">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherLocation <String> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81730-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="81730-109">DESCRIPTION</span></span>
<span data-ttu-id="81730-110">Il Get-AzNetworkWatcherReachabilityReport ottiene il punteggio relativo alla latenza per i provider di servizi Internet da una posizione specificata alle aree di Azure.</span><span class="sxs-lookup"><span data-stu-id="81730-110">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="81730-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="81730-111">EXAMPLES</span></span>

### <span data-ttu-id="81730-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="81730-112">Example 1</span></span>
```
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

<span data-ttu-id="81730-113">Ottiene le latenze relative al Data Center di Azure in West US da 2017-10-10 a 2017-10-12 all'interno dello stato United.</span><span class="sxs-lookup"><span data-stu-id="81730-113">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

## <span data-ttu-id="81730-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="81730-114">PARAMETERS</span></span>

### <span data-ttu-id="81730-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="81730-115">-AsJob</span></span>
<span data-ttu-id="81730-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="81730-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="81730-117">-Città</span><span class="sxs-lookup"><span data-stu-id="81730-117">-City</span></span>
<span data-ttu-id="81730-118">Nome della città.</span><span class="sxs-lookup"><span data-stu-id="81730-118">The name of the city.</span></span>

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

### <span data-ttu-id="81730-119">-Paese</span><span class="sxs-lookup"><span data-stu-id="81730-119">-Country</span></span>
<span data-ttu-id="81730-120">Nome del paese.</span><span class="sxs-lookup"><span data-stu-id="81730-120">The name of the country.</span></span>

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

### <span data-ttu-id="81730-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81730-121">-DefaultProfile</span></span>
<span data-ttu-id="81730-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="81730-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81730-123">-EndTime</span><span class="sxs-lookup"><span data-stu-id="81730-123">-EndTime</span></span>
<span data-ttu-id="81730-124">Ora di fine per il report di accessibilità di Azure.</span><span class="sxs-lookup"><span data-stu-id="81730-124">The end time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="81730-125">-Posizione</span><span class="sxs-lookup"><span data-stu-id="81730-125">-Location</span></span>
<span data-ttu-id="81730-126">Aree di Azure facoltative per l'ambito della query.</span><span class="sxs-lookup"><span data-stu-id="81730-126">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="81730-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="81730-127">-NetworkWatcher</span></span>
<span data-ttu-id="81730-128">Risorsa Watcher di rete</span><span class="sxs-lookup"><span data-stu-id="81730-128">The network watcher resource</span></span>

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

### <span data-ttu-id="81730-129">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="81730-129">-NetworkWatcherLocation</span></span>
<span data-ttu-id="81730-130">Posizione del monitoraggio della rete.</span><span class="sxs-lookup"><span data-stu-id="81730-130">Location of the network watcher.</span></span>

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

### <span data-ttu-id="81730-131">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="81730-131">-NetworkWatcherName</span></span>
<span data-ttu-id="81730-132">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="81730-132">The name of network watcher.</span></span>

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

### <span data-ttu-id="81730-133">-Provider</span><span class="sxs-lookup"><span data-stu-id="81730-133">-Provider</span></span>
<span data-ttu-id="81730-134">Elenco dei provider di servizi Internet.</span><span class="sxs-lookup"><span data-stu-id="81730-134">List of Internet service providers.</span></span>

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

### <span data-ttu-id="81730-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81730-135">-ResourceGroupName</span></span>
<span data-ttu-id="81730-136">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="81730-136">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="81730-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="81730-137">-ResourceId</span></span>
<span data-ttu-id="81730-138">ID della risorsa Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="81730-138">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="81730-139">-StartTime</span><span class="sxs-lookup"><span data-stu-id="81730-139">-StartTime</span></span>
<span data-ttu-id="81730-140">Ora di inizio per il report di raggiungibilità di Azure.</span><span class="sxs-lookup"><span data-stu-id="81730-140">The start time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="81730-141">-Stato</span><span class="sxs-lookup"><span data-stu-id="81730-141">-State</span></span>
<span data-ttu-id="81730-142">Nome dello stato.</span><span class="sxs-lookup"><span data-stu-id="81730-142">The name of the state.</span></span>

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

### <span data-ttu-id="81730-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81730-143">CommonParameters</span></span>
<span data-ttu-id="81730-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81730-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81730-145">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81730-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81730-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="81730-146">INPUTS</span></span>

### <span data-ttu-id="81730-147">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="81730-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="81730-148">System. String</span><span class="sxs-lookup"><span data-stu-id="81730-148">System.String</span></span>

## <span data-ttu-id="81730-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="81730-149">OUTPUTS</span></span>

### <span data-ttu-id="81730-150">Microsoft. Azure. Commands. Network. Models. PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="81730-150">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="81730-151">Note</span><span class="sxs-lookup"><span data-stu-id="81730-151">NOTES</span></span>
<span data-ttu-id="81730-152">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher, raggiungibilità, report</span><span class="sxs-lookup"><span data-stu-id="81730-152">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="81730-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="81730-153">RELATED LINKS</span></span>

[<span data-ttu-id="81730-154">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="81730-154">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="81730-155">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="81730-155">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="81730-156">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="81730-156">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="81730-157">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="81730-157">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="81730-158">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="81730-158">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="81730-159">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="81730-159">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="81730-160">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="81730-160">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="81730-161">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="81730-161">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="81730-162">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="81730-162">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="81730-163">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="81730-163">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="81730-164">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="81730-164">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="81730-165">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="81730-165">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="81730-166">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="81730-166">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="81730-167">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="81730-167">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="81730-168">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="81730-168">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="81730-169">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="81730-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="81730-170">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="81730-170">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="81730-171">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="81730-171">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="81730-172">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="81730-172">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="81730-173">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="81730-173">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="81730-174">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="81730-174">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="81730-175">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="81730-175">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="81730-176">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="81730-176">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="81730-177">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="81730-177">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="81730-178">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="81730-178">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="81730-179">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="81730-179">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="81730-180">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="81730-180">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)