---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: a4e9c9a928d3a6c3ddeb7afa754cc957089a2283
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199875"
---
# <span data-ttu-id="293c5-101">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="293c5-101">Get-AzNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="293c5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="293c5-102">SYNOPSIS</span></span>
<span data-ttu-id="293c5-103">Elenca tutti i provider di servizi Internet disponibili per un'area di Azure specificata.</span><span class="sxs-lookup"><span data-stu-id="293c5-103">Lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="293c5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="293c5-104">SYNTAX</span></span>

### <span data-ttu-id="293c5-105">SetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="293c5-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <String[]>] [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="293c5-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="293c5-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="293c5-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="293c5-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherLocation <String> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="293c5-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="293c5-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -ResourceId <String> [-Location <String[]>] [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="293c5-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="293c5-109">DESCRIPTION</span></span>
<span data-ttu-id="293c5-110">La Get-AzNetworkWatcherReachabilityProvidersList elenca tutti i provider di servizi Internet disponibili per un'area di Azure specificata.</span><span class="sxs-lookup"><span data-stu-id="293c5-110">The Get-AzNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="293c5-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="293c5-111">EXAMPLES</span></span>

### <span data-ttu-id="293c5-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="293c5-112">Example 1</span></span>
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

<span data-ttu-id="293c5-113">Elenca tutti i provider disponibili in Seattle, WA per Azure Data Center in West US.</span><span class="sxs-lookup"><span data-stu-id="293c5-113">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

### <span data-ttu-id="293c5-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="293c5-114">Example 2</span></span>

<span data-ttu-id="293c5-115">Elenca tutti i provider di servizi Internet disponibili per un'area di Azure specificata.</span><span class="sxs-lookup"><span data-stu-id="293c5-115">Lists all available internet service providers for a specified Azure region.</span></span> <span data-ttu-id="293c5-116">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="293c5-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName nw1 -ResourceGroupName myresourcegroup
```

## <span data-ttu-id="293c5-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="293c5-117">PARAMETERS</span></span>

### <span data-ttu-id="293c5-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="293c5-118">-AsJob</span></span>
<span data-ttu-id="293c5-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="293c5-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="293c5-120">-Città</span><span class="sxs-lookup"><span data-stu-id="293c5-120">-City</span></span>
<span data-ttu-id="293c5-121">Nome della città.</span><span class="sxs-lookup"><span data-stu-id="293c5-121">The name of the city.</span></span>

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

### <span data-ttu-id="293c5-122">-Paese</span><span class="sxs-lookup"><span data-stu-id="293c5-122">-Country</span></span>
<span data-ttu-id="293c5-123">Nome del paese.</span><span class="sxs-lookup"><span data-stu-id="293c5-123">The name of the country.</span></span>

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

### <span data-ttu-id="293c5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="293c5-124">-DefaultProfile</span></span>
<span data-ttu-id="293c5-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="293c5-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="293c5-126">-Posizione</span><span class="sxs-lookup"><span data-stu-id="293c5-126">-Location</span></span>
<span data-ttu-id="293c5-127">Aree di Azure facoltative per l'ambito della query.</span><span class="sxs-lookup"><span data-stu-id="293c5-127">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="293c5-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="293c5-128">-NetworkWatcher</span></span>
<span data-ttu-id="293c5-129">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="293c5-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="293c5-130">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="293c5-130">-NetworkWatcherLocation</span></span>
<span data-ttu-id="293c5-131">Posizione del monitoraggio della rete.</span><span class="sxs-lookup"><span data-stu-id="293c5-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="293c5-132">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="293c5-132">-NetworkWatcherName</span></span>
<span data-ttu-id="293c5-133">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="293c5-133">The name of network watcher.</span></span>

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

### <span data-ttu-id="293c5-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="293c5-134">-ResourceGroupName</span></span>
<span data-ttu-id="293c5-135">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="293c5-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="293c5-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="293c5-136">-ResourceId</span></span>
<span data-ttu-id="293c5-137">ID della risorsa Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="293c5-137">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="293c5-138">-Stato</span><span class="sxs-lookup"><span data-stu-id="293c5-138">-State</span></span>
<span data-ttu-id="293c5-139">Nome dello stato.</span><span class="sxs-lookup"><span data-stu-id="293c5-139">The name of the state.</span></span>

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

### <span data-ttu-id="293c5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="293c5-140">CommonParameters</span></span>
<span data-ttu-id="293c5-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="293c5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="293c5-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="293c5-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="293c5-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="293c5-143">INPUTS</span></span>

### <span data-ttu-id="293c5-144">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="293c5-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="293c5-145">System. String</span><span class="sxs-lookup"><span data-stu-id="293c5-145">System.String</span></span>

## <span data-ttu-id="293c5-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="293c5-146">OUTPUTS</span></span>

### <span data-ttu-id="293c5-147">Microsoft. Azure. Commands. Network. Models. PSAvailableProvidersList</span><span class="sxs-lookup"><span data-stu-id="293c5-147">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="293c5-148">Note</span><span class="sxs-lookup"><span data-stu-id="293c5-148">NOTES</span></span>
<span data-ttu-id="293c5-149">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher, Next, hop</span><span class="sxs-lookup"><span data-stu-id="293c5-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="293c5-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="293c5-150">RELATED LINKS</span></span>

[<span data-ttu-id="293c5-151">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="293c5-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="293c5-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="293c5-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="293c5-153">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="293c5-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="293c5-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="293c5-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="293c5-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="293c5-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="293c5-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="293c5-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="293c5-157">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="293c5-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="293c5-158">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="293c5-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="293c5-159">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="293c5-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="293c5-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="293c5-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="293c5-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="293c5-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="293c5-162">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="293c5-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="293c5-163">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="293c5-163">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="293c5-164">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="293c5-164">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="293c5-165">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="293c5-165">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="293c5-166">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="293c5-166">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="293c5-167">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="293c5-167">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="293c5-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="293c5-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="293c5-169">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="293c5-169">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="293c5-170">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="293c5-170">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="293c5-171">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="293c5-171">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="293c5-172">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="293c5-172">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="293c5-173">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="293c5-173">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="293c5-174">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="293c5-174">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="293c5-175">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="293c5-175">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="293c5-176">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="293c5-176">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="293c5-177">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="293c5-177">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)