---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: 028af170e73397178dfe3b81ff216b7fdb0ecfe6
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100395674"
---
# <span data-ttu-id="bb46d-101">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="bb46d-101">Get-AzNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="bb46d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb46d-102">SYNOPSIS</span></span>
<span data-ttu-id="bb46d-103">Elenca tutti i provider di servizi Internet disponibili per una specifica area geografica di Azure.</span><span class="sxs-lookup"><span data-stu-id="bb46d-103">Lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="bb46d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bb46d-104">SYNTAX</span></span>

### <span data-ttu-id="bb46d-105">SetByName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bb46d-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <String[]>] [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb46d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="bb46d-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bb46d-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="bb46d-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherLocation <String> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bb46d-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="bb46d-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -ResourceId <String> [-Location <String[]>] [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb46d-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bb46d-109">DESCRIPTION</span></span>
<span data-ttu-id="bb46d-110">LGet-AzNetworkWatcherReachabilityProvidersList elenca tutti i provider di servizi Internet disponibili per una specifica area geografica di Azure.</span><span class="sxs-lookup"><span data-stu-id="bb46d-110">The Get-AzNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="bb46d-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bb46d-111">EXAMPLES</span></span>

### <span data-ttu-id="bb46d-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bb46d-112">Example 1</span></span>
```powershell
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

<span data-ttu-id="bb46d-113">Elenca tutti i provider disponibili nel Data Center di Seattle, WA per Azure negli Stati Uniti occidentali.</span><span class="sxs-lookup"><span data-stu-id="bb46d-113">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

### <span data-ttu-id="bb46d-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="bb46d-114">Example 2</span></span>

<span data-ttu-id="bb46d-115">Elenca tutti i provider di servizi Internet disponibili per una specifica area geografica di Azure.</span><span class="sxs-lookup"><span data-stu-id="bb46d-115">Lists all available internet service providers for a specified Azure region.</span></span> <span data-ttu-id="bb46d-116">(autogenerati)</span><span class="sxs-lookup"><span data-stu-id="bb46d-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName nw1 -ResourceGroupName myresourcegroup
```

## <span data-ttu-id="bb46d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb46d-117">PARAMETERS</span></span>

### <span data-ttu-id="bb46d-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bb46d-118">-AsJob</span></span>
<span data-ttu-id="bb46d-119">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="bb46d-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bb46d-120">-Città</span><span class="sxs-lookup"><span data-stu-id="bb46d-120">-City</span></span>
<span data-ttu-id="bb46d-121">Il nome della città.</span><span class="sxs-lookup"><span data-stu-id="bb46d-121">The name of the city.</span></span>

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

### <span data-ttu-id="bb46d-122">-Paese</span><span class="sxs-lookup"><span data-stu-id="bb46d-122">-Country</span></span>
<span data-ttu-id="bb46d-123">Nome del paese.</span><span class="sxs-lookup"><span data-stu-id="bb46d-123">The name of the country.</span></span>

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

### <span data-ttu-id="bb46d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb46d-124">-DefaultProfile</span></span>
<span data-ttu-id="bb46d-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bb46d-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb46d-126">-Location</span><span class="sxs-lookup"><span data-stu-id="bb46d-126">-Location</span></span>
<span data-ttu-id="bb46d-127">Aree di Azure facoltative per l'ambito della query.</span><span class="sxs-lookup"><span data-stu-id="bb46d-127">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="bb46d-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bb46d-128">-NetworkWatcher</span></span>
<span data-ttu-id="bb46d-129">Risorsa Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="bb46d-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="bb46d-130">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="bb46d-130">-NetworkWatcherLocation</span></span>
<span data-ttu-id="bb46d-131">Posizione del network watcher.</span><span class="sxs-lookup"><span data-stu-id="bb46d-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="bb46d-132">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="bb46d-132">-NetworkWatcherName</span></span>
<span data-ttu-id="bb46d-133">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="bb46d-133">The name of network watcher.</span></span>

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

### <span data-ttu-id="bb46d-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb46d-134">-ResourceGroupName</span></span>
<span data-ttu-id="bb46d-135">Nome del gruppo di risorse Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="bb46d-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="bb46d-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb46d-136">-ResourceId</span></span>
<span data-ttu-id="bb46d-137">ID della risorsa Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="bb46d-137">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="bb46d-138">-State</span><span class="sxs-lookup"><span data-stu-id="bb46d-138">-State</span></span>
<span data-ttu-id="bb46d-139">Nome dello stato.</span><span class="sxs-lookup"><span data-stu-id="bb46d-139">The name of the state.</span></span>

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

### <span data-ttu-id="bb46d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb46d-140">CommonParameters</span></span>
<span data-ttu-id="bb46d-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb46d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb46d-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bb46d-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb46d-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="bb46d-143">INPUTS</span></span>

### <span data-ttu-id="bb46d-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bb46d-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="bb46d-145">System.String</span><span class="sxs-lookup"><span data-stu-id="bb46d-145">System.String</span></span>

## <span data-ttu-id="bb46d-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bb46d-146">OUTPUTS</span></span>

### <span data-ttu-id="bb46d-147">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span><span class="sxs-lookup"><span data-stu-id="bb46d-147">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="bb46d-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="bb46d-148">NOTES</span></span>
<span data-ttu-id="bb46d-149">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, rete, rete, network watcher, next, hop</span><span class="sxs-lookup"><span data-stu-id="bb46d-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="bb46d-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bb46d-150">RELATED LINKS</span></span>

[<span data-ttu-id="bb46d-151">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bb46d-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="bb46d-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bb46d-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="bb46d-153">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bb46d-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="bb46d-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="bb46d-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="bb46d-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="bb46d-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="bb46d-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="bb46d-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="bb46d-157">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="bb46d-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="bb46d-158">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bb46d-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bb46d-159">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="bb46d-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="bb46d-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bb46d-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bb46d-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bb46d-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bb46d-162">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bb46d-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bb46d-163">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="bb46d-163">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="bb46d-164">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="bb46d-164">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="bb46d-165">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="bb46d-165">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="bb46d-166">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bb46d-166">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="bb46d-167">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bb46d-167">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="bb46d-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bb46d-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="bb46d-169">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="bb46d-169">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="bb46d-170">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bb46d-170">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="bb46d-171">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bb46d-171">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="bb46d-172">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="bb46d-172">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="bb46d-173">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="bb46d-173">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="bb46d-174">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="bb46d-174">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="bb46d-175">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="bb46d-175">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="bb46d-176">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="bb46d-176">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="bb46d-177">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bb46d-177">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
