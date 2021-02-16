---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: dcdd4ef2fd6ca3481d9bb3f8333174307be7e3f6
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100404081"
---
# <span data-ttu-id="0313e-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="0313e-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="0313e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0313e-102">SYNOPSIS</span></span>
<span data-ttu-id="0313e-103">Recupera il punteggio di latenza relativo per i provider di servizi Internet da una posizione specificata alle aree geografiche di Azure.</span><span class="sxs-lookup"><span data-stu-id="0313e-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="0313e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0313e-104">SYNTAX</span></span>

### <span data-ttu-id="0313e-105">SetByName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0313e-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <String[]>] [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0313e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="0313e-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0313e-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0313e-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String> [-Provider <String[]>] [-Location <String[]>]
 -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0313e-108">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="0313e-108">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherLocation <String> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0313e-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0313e-109">DESCRIPTION</span></span>
<span data-ttu-id="0313e-110">LGet-AzNetworkWatcherReachabilityReport ottiene il punteggio di latenza relativo per i provider di servizi Internet da una posizione specificata alle aree geografiche di Azure.</span><span class="sxs-lookup"><span data-stu-id="0313e-110">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="0313e-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0313e-111">EXAMPLES</span></span>

### <span data-ttu-id="0313e-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0313e-112">Example 1</span></span>
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

<span data-ttu-id="0313e-113">Recupera le latenze relative al data center di Azure negli Stati Uniti occidentali dal 2017-10-10 al 10-10-12 nello Stato Unito.</span><span class="sxs-lookup"><span data-stu-id="0313e-113">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

## <span data-ttu-id="0313e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0313e-114">PARAMETERS</span></span>

### <span data-ttu-id="0313e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0313e-115">-AsJob</span></span>
<span data-ttu-id="0313e-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="0313e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0313e-117">-Città</span><span class="sxs-lookup"><span data-stu-id="0313e-117">-City</span></span>
<span data-ttu-id="0313e-118">Il nome della città.</span><span class="sxs-lookup"><span data-stu-id="0313e-118">The name of the city.</span></span>

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

### <span data-ttu-id="0313e-119">-Paese</span><span class="sxs-lookup"><span data-stu-id="0313e-119">-Country</span></span>
<span data-ttu-id="0313e-120">Nome del paese.</span><span class="sxs-lookup"><span data-stu-id="0313e-120">The name of the country.</span></span>

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

### <span data-ttu-id="0313e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0313e-121">-DefaultProfile</span></span>
<span data-ttu-id="0313e-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0313e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0313e-123">-EndTime</span><span class="sxs-lookup"><span data-stu-id="0313e-123">-EndTime</span></span>
<span data-ttu-id="0313e-124">Ora di fine per il report di raggiungibilità di Azure.</span><span class="sxs-lookup"><span data-stu-id="0313e-124">The end time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="0313e-125">-Location</span><span class="sxs-lookup"><span data-stu-id="0313e-125">-Location</span></span>
<span data-ttu-id="0313e-126">Aree di Azure facoltative per l'ambito della query.</span><span class="sxs-lookup"><span data-stu-id="0313e-126">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="0313e-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0313e-127">-NetworkWatcher</span></span>
<span data-ttu-id="0313e-128">Risorsa Network Watcher</span><span class="sxs-lookup"><span data-stu-id="0313e-128">The network watcher resource</span></span>

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

### <span data-ttu-id="0313e-129">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="0313e-129">-NetworkWatcherLocation</span></span>
<span data-ttu-id="0313e-130">Posizione del network watcher.</span><span class="sxs-lookup"><span data-stu-id="0313e-130">Location of the network watcher.</span></span>

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

### <span data-ttu-id="0313e-131">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="0313e-131">-NetworkWatcherName</span></span>
<span data-ttu-id="0313e-132">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="0313e-132">The name of network watcher.</span></span>

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

### <span data-ttu-id="0313e-133">-Provider</span><span class="sxs-lookup"><span data-stu-id="0313e-133">-Provider</span></span>
<span data-ttu-id="0313e-134">Elenco di provider di servizi Internet.</span><span class="sxs-lookup"><span data-stu-id="0313e-134">List of Internet service providers.</span></span>

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

### <span data-ttu-id="0313e-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0313e-135">-ResourceGroupName</span></span>
<span data-ttu-id="0313e-136">Nome del gruppo di risorse Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="0313e-136">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="0313e-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0313e-137">-ResourceId</span></span>
<span data-ttu-id="0313e-138">ID della risorsa Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="0313e-138">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="0313e-139">-StartTime</span><span class="sxs-lookup"><span data-stu-id="0313e-139">-StartTime</span></span>
<span data-ttu-id="0313e-140">Ora di inizio per il report di raggiungibilità di Azure.</span><span class="sxs-lookup"><span data-stu-id="0313e-140">The start time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="0313e-141">-State</span><span class="sxs-lookup"><span data-stu-id="0313e-141">-State</span></span>
<span data-ttu-id="0313e-142">Nome dello stato.</span><span class="sxs-lookup"><span data-stu-id="0313e-142">The name of the state.</span></span>

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

### <span data-ttu-id="0313e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0313e-143">CommonParameters</span></span>
<span data-ttu-id="0313e-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0313e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0313e-145">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0313e-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0313e-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="0313e-146">INPUTS</span></span>

### <span data-ttu-id="0313e-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0313e-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="0313e-148">System.String</span><span class="sxs-lookup"><span data-stu-id="0313e-148">System.String</span></span>

## <span data-ttu-id="0313e-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0313e-149">OUTPUTS</span></span>

### <span data-ttu-id="0313e-150">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="0313e-150">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="0313e-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="0313e-151">NOTES</span></span>
<span data-ttu-id="0313e-152">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, rete, rete, network watcher, raggiungibilità, report</span><span class="sxs-lookup"><span data-stu-id="0313e-152">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="0313e-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0313e-153">RELATED LINKS</span></span>

[<span data-ttu-id="0313e-154">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0313e-154">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="0313e-155">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0313e-155">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="0313e-156">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0313e-156">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="0313e-157">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="0313e-157">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="0313e-158">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="0313e-158">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="0313e-159">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="0313e-159">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="0313e-160">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="0313e-160">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="0313e-161">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0313e-161">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0313e-162">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="0313e-162">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="0313e-163">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0313e-163">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0313e-164">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0313e-164">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0313e-165">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0313e-165">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0313e-166">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="0313e-166">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="0313e-167">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="0313e-167">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="0313e-168">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="0313e-168">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="0313e-169">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0313e-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0313e-170">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0313e-170">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0313e-171">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0313e-171">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0313e-172">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="0313e-172">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="0313e-173">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0313e-173">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0313e-174">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0313e-174">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0313e-175">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="0313e-175">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="0313e-176">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="0313e-176">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="0313e-177">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="0313e-177">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="0313e-178">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="0313e-178">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="0313e-179">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="0313e-179">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="0313e-180">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0313e-180">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
