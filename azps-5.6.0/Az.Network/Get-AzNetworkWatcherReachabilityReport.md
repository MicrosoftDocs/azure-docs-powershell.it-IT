---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 72aa9748cddee0a8ff894463e569d15a2fa01ec0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954381"
---
# <span data-ttu-id="7be46-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="7be46-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="7be46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7be46-102">SYNOPSIS</span></span>
<span data-ttu-id="7be46-103">Recupera il punteggio di latenza relativo per i provider di servizi Internet da una posizione specificata alle aree geografiche di Azure.</span><span class="sxs-lookup"><span data-stu-id="7be46-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="7be46-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7be46-104">SYNTAX</span></span>

### <span data-ttu-id="7be46-105">SetByName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7be46-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <String[]>] [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7be46-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7be46-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7be46-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7be46-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String> [-Provider <String[]>] [-Location <String[]>]
 -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7be46-108">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="7be46-108">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherLocation <String> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7be46-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7be46-109">DESCRIPTION</span></span>
<span data-ttu-id="7be46-110">LGet-AzNetworkWatcherReachabilityReport ottiene il punteggio di latenza relativo per i provider di servizi Internet da una posizione specificata alle aree geografiche di Azure.</span><span class="sxs-lookup"><span data-stu-id="7be46-110">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="7be46-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7be46-111">EXAMPLES</span></span>

### <span data-ttu-id="7be46-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7be46-112">Example 1</span></span>
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

<span data-ttu-id="7be46-113">Recupera le latenze relative al data center di Azure negli Stati Uniti occidentali dal 2017-10-10 al 10-10-12 nello Stato Unito.</span><span class="sxs-lookup"><span data-stu-id="7be46-113">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

### <span data-ttu-id="7be46-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7be46-114">Example 2</span></span>

<span data-ttu-id="7be46-115">Recupera il punteggio di latenza relativo per i provider di servizi Internet da una posizione specificata alle aree geografiche di Azure.</span><span class="sxs-lookup"><span data-stu-id="7be46-115">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span> <span data-ttu-id="7be46-116">(autogenerati)</span><span class="sxs-lookup"><span data-stu-id="7be46-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNetworkWatcherReachabilityReport -Country 'United States' -EndTime '2017-10-12' -Location 'West US' -NetworkWatcherName nw1 -ResourceGroupName myresourcegroup -StartTime '2017-10-10' -State 'washington'
```

## <span data-ttu-id="7be46-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7be46-117">PARAMETERS</span></span>

### <span data-ttu-id="7be46-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7be46-118">-AsJob</span></span>
<span data-ttu-id="7be46-119">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7be46-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7be46-120">-Città</span><span class="sxs-lookup"><span data-stu-id="7be46-120">-City</span></span>
<span data-ttu-id="7be46-121">Il nome della città.</span><span class="sxs-lookup"><span data-stu-id="7be46-121">The name of the city.</span></span>

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

### <span data-ttu-id="7be46-122">-Paese</span><span class="sxs-lookup"><span data-stu-id="7be46-122">-Country</span></span>
<span data-ttu-id="7be46-123">Nome del paese.</span><span class="sxs-lookup"><span data-stu-id="7be46-123">The name of the country.</span></span>

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

### <span data-ttu-id="7be46-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7be46-124">-DefaultProfile</span></span>
<span data-ttu-id="7be46-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7be46-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7be46-126">-EndTime</span><span class="sxs-lookup"><span data-stu-id="7be46-126">-EndTime</span></span>
<span data-ttu-id="7be46-127">Ora di fine per il report sulla raggiungibilità di Azure.</span><span class="sxs-lookup"><span data-stu-id="7be46-127">The end time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="7be46-128">-Location</span><span class="sxs-lookup"><span data-stu-id="7be46-128">-Location</span></span>
<span data-ttu-id="7be46-129">Aree di Azure facoltative per l'ambito della query.</span><span class="sxs-lookup"><span data-stu-id="7be46-129">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="7be46-130">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7be46-130">-NetworkWatcher</span></span>
<span data-ttu-id="7be46-131">Risorsa Network Watcher</span><span class="sxs-lookup"><span data-stu-id="7be46-131">The network watcher resource</span></span>

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

### <span data-ttu-id="7be46-132">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="7be46-132">-NetworkWatcherLocation</span></span>
<span data-ttu-id="7be46-133">Posizione del network watcher.</span><span class="sxs-lookup"><span data-stu-id="7be46-133">Location of the network watcher.</span></span>

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

### <span data-ttu-id="7be46-134">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="7be46-134">-NetworkWatcherName</span></span>
<span data-ttu-id="7be46-135">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="7be46-135">The name of network watcher.</span></span>

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

### <span data-ttu-id="7be46-136">-Provider</span><span class="sxs-lookup"><span data-stu-id="7be46-136">-Provider</span></span>
<span data-ttu-id="7be46-137">Elenco di provider di servizi Internet.</span><span class="sxs-lookup"><span data-stu-id="7be46-137">List of Internet service providers.</span></span>

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

### <span data-ttu-id="7be46-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7be46-138">-ResourceGroupName</span></span>
<span data-ttu-id="7be46-139">Nome del gruppo di risorse Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="7be46-139">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="7be46-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7be46-140">-ResourceId</span></span>
<span data-ttu-id="7be46-141">ID della risorsa Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="7be46-141">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="7be46-142">-StartTime</span><span class="sxs-lookup"><span data-stu-id="7be46-142">-StartTime</span></span>
<span data-ttu-id="7be46-143">Ora di inizio per il report di raggiungibilità di Azure.</span><span class="sxs-lookup"><span data-stu-id="7be46-143">The start time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="7be46-144">-State</span><span class="sxs-lookup"><span data-stu-id="7be46-144">-State</span></span>
<span data-ttu-id="7be46-145">Nome dello stato.</span><span class="sxs-lookup"><span data-stu-id="7be46-145">The name of the state.</span></span>

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

### <span data-ttu-id="7be46-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7be46-146">CommonParameters</span></span>
<span data-ttu-id="7be46-147">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7be46-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7be46-148">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7be46-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7be46-149">INPUT</span><span class="sxs-lookup"><span data-stu-id="7be46-149">INPUTS</span></span>

### <span data-ttu-id="7be46-150">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7be46-150">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="7be46-151">System.String</span><span class="sxs-lookup"><span data-stu-id="7be46-151">System.String</span></span>

## <span data-ttu-id="7be46-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7be46-152">OUTPUTS</span></span>

### <span data-ttu-id="7be46-153">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="7be46-153">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="7be46-154">NOTE</span><span class="sxs-lookup"><span data-stu-id="7be46-154">NOTES</span></span>
<span data-ttu-id="7be46-155">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, rete, rete, network watcher, raggiungibilità, report</span><span class="sxs-lookup"><span data-stu-id="7be46-155">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="7be46-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7be46-156">RELATED LINKS</span></span>

[<span data-ttu-id="7be46-157">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7be46-157">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="7be46-158">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7be46-158">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="7be46-159">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7be46-159">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="7be46-160">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="7be46-160">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="7be46-161">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="7be46-161">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="7be46-162">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="7be46-162">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="7be46-163">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="7be46-163">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="7be46-164">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7be46-164">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7be46-165">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="7be46-165">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="7be46-166">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7be46-166">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7be46-167">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7be46-167">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7be46-168">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7be46-168">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7be46-169">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="7be46-169">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="7be46-170">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="7be46-170">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="7be46-171">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="7be46-171">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="7be46-172">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7be46-172">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7be46-173">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7be46-173">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7be46-174">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7be46-174">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7be46-175">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="7be46-175">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="7be46-176">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7be46-176">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7be46-177">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7be46-177">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7be46-178">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="7be46-178">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="7be46-179">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="7be46-179">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="7be46-180">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="7be46-180">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="7be46-181">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="7be46-181">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="7be46-182">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="7be46-182">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="7be46-183">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7be46-183">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
