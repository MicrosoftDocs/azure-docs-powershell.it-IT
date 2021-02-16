---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: 46acc935729f31e190bbf36b7afca5682eb79398
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399193"
---
# <span data-ttu-id="1b855-101">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="1b855-101">Get-AzNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="1b855-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b855-102">SYNOPSIS</span></span>
<span data-ttu-id="1b855-103">Elenca tutti i provider di servizi Internet disponibili per una specifica area geografica di Azure.</span><span class="sxs-lookup"><span data-stu-id="1b855-103">Lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="1b855-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1b855-104">SYNTAX</span></span>

### <span data-ttu-id="1b855-105">SetByName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1b855-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <String[]>] [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b855-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="1b855-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1b855-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="1b855-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherLocation <String> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1b855-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1b855-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -ResourceId <String> [-Location <String[]>] [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b855-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1b855-109">DESCRIPTION</span></span>
<span data-ttu-id="1b855-110">LGet-AzNetworkWatcherReachabilityProvidersList elenca tutti i provider di servizi Internet disponibili per una specifica area geografica di Azure.</span><span class="sxs-lookup"><span data-stu-id="1b855-110">The Get-AzNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="1b855-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1b855-111">EXAMPLES</span></span>

### <span data-ttu-id="1b855-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1b855-112">Example 1</span></span>
```
PS C:\> $nw = Get-AzNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
PS C:\> Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher $nw -Location "West US" -Country "United States" -State "washington" -City "seattle"

"countries" : [
    {
        "countryName" : "United States",
        "states" : [
            {
                "stateName" : "washington",
                "cities" : [
                    {
                        "cityName" : "seattle",
                        "providers" : [
                            "Comcast Cable Communications, Inc. - ASN 7922",
                            "Comcast Cable Communications, LLC - ASN 7922",
                            "Level 3 Communications, Inc. (GBLX) - ASN 3549",
                            "Qwest Communications Company, LLC - ASN 209"
                        ]
                    }
                ]
            }
        ]
    }
]
```

<span data-ttu-id="1b855-113">Elenca tutti i provider disponibili nel Data Center di Seattle, WA per Azure negli Stati Uniti occidentali.</span><span class="sxs-lookup"><span data-stu-id="1b855-113">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

## <span data-ttu-id="1b855-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b855-114">PARAMETERS</span></span>

### <span data-ttu-id="1b855-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1b855-115">-AsJob</span></span>
<span data-ttu-id="1b855-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="1b855-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1b855-117">-Città</span><span class="sxs-lookup"><span data-stu-id="1b855-117">-City</span></span>
<span data-ttu-id="1b855-118">Il nome della città.</span><span class="sxs-lookup"><span data-stu-id="1b855-118">The name of the city.</span></span>

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

### <span data-ttu-id="1b855-119">-Paese</span><span class="sxs-lookup"><span data-stu-id="1b855-119">-Country</span></span>
<span data-ttu-id="1b855-120">Nome del paese.</span><span class="sxs-lookup"><span data-stu-id="1b855-120">The name of the country.</span></span>

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

### <span data-ttu-id="1b855-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b855-121">-DefaultProfile</span></span>
<span data-ttu-id="1b855-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1b855-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b855-123">-Location</span><span class="sxs-lookup"><span data-stu-id="1b855-123">-Location</span></span>
<span data-ttu-id="1b855-124">Aree di Azure facoltative per l'ambito della query.</span><span class="sxs-lookup"><span data-stu-id="1b855-124">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="1b855-125">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1b855-125">-NetworkWatcher</span></span>
<span data-ttu-id="1b855-126">Risorsa Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="1b855-126">The network watcher resource.</span></span>

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

### <span data-ttu-id="1b855-127">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="1b855-127">-NetworkWatcherLocation</span></span>
<span data-ttu-id="1b855-128">Posizione del network watcher.</span><span class="sxs-lookup"><span data-stu-id="1b855-128">Location of the network watcher.</span></span>

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

### <span data-ttu-id="1b855-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="1b855-129">-NetworkWatcherName</span></span>
<span data-ttu-id="1b855-130">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="1b855-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="1b855-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b855-131">-ResourceGroupName</span></span>
<span data-ttu-id="1b855-132">Nome del gruppo di risorse Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="1b855-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="1b855-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b855-133">-ResourceId</span></span>
<span data-ttu-id="1b855-134">ID della risorsa Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="1b855-134">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="1b855-135">-State</span><span class="sxs-lookup"><span data-stu-id="1b855-135">-State</span></span>
<span data-ttu-id="1b855-136">Nome dello stato.</span><span class="sxs-lookup"><span data-stu-id="1b855-136">The name of the state.</span></span>

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

### <span data-ttu-id="1b855-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b855-137">CommonParameters</span></span>
<span data-ttu-id="1b855-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b855-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b855-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1b855-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b855-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="1b855-140">INPUTS</span></span>

### <span data-ttu-id="1b855-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1b855-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="1b855-142">System.String</span><span class="sxs-lookup"><span data-stu-id="1b855-142">System.String</span></span>

## <span data-ttu-id="1b855-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1b855-143">OUTPUTS</span></span>

### <span data-ttu-id="1b855-144">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span><span class="sxs-lookup"><span data-stu-id="1b855-144">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="1b855-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="1b855-145">NOTES</span></span>
<span data-ttu-id="1b855-146">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, rete, rete, network watcher, next, hop</span><span class="sxs-lookup"><span data-stu-id="1b855-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="1b855-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1b855-147">RELATED LINKS</span></span>

[<span data-ttu-id="1b855-148">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1b855-148">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="1b855-149">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1b855-149">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="1b855-150">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1b855-150">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="1b855-151">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="1b855-151">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="1b855-152">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="1b855-152">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="1b855-153">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="1b855-153">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="1b855-154">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="1b855-154">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="1b855-155">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1b855-155">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1b855-156">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="1b855-156">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="1b855-157">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1b855-157">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1b855-158">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1b855-158">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1b855-159">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1b855-159">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1b855-160">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="1b855-160">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="1b855-161">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="1b855-161">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="1b855-162">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="1b855-162">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="1b855-163">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1b855-163">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1b855-164">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1b855-164">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1b855-165">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1b855-165">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1b855-166">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="1b855-166">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="1b855-167">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1b855-167">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1b855-168">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1b855-168">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1b855-169">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="1b855-169">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="1b855-170">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="1b855-170">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="1b855-171">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="1b855-171">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="1b855-172">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="1b855-172">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="1b855-173">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="1b855-173">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="1b855-174">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1b855-174">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
