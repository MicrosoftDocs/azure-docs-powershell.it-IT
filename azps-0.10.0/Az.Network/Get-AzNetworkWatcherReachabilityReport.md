---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 6da0a36ee5e394008ea1d1de4a16f7982227ca06
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860714"
---
# <span data-ttu-id="f2850-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="f2850-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="f2850-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f2850-102">SYNOPSIS</span></span>
<span data-ttu-id="f2850-103">Ottiene il punteggio relativo alla latenza per i provider di servizi Internet da una posizione specificata alle aree di Azure.</span><span class="sxs-lookup"><span data-stu-id="f2850-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="f2850-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f2850-104">SYNTAX</span></span>

### <span data-ttu-id="f2850-105">SetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f2850-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2850-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f2850-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2850-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f2850-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f2850-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f2850-108">DESCRIPTION</span></span>
<span data-ttu-id="f2850-109">Il Get-AzNetworkWatcherReachabilityReport ottiene il punteggio relativo alla latenza per i provider di servizi Internet da una posizione specificata alle aree di Azure.</span><span class="sxs-lookup"><span data-stu-id="f2850-109">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="f2850-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f2850-110">EXAMPLES</span></span>

### <span data-ttu-id="f2850-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f2850-111">Example 1</span></span>
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

<span data-ttu-id="f2850-112">Ottiene le latenze relative al Data Center di Azure in West US da 2017-10-10 a 2017-10-12 all'interno dello stato United.</span><span class="sxs-lookup"><span data-stu-id="f2850-112">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

## <span data-ttu-id="f2850-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f2850-113">PARAMETERS</span></span>

### <span data-ttu-id="f2850-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f2850-114">-AsJob</span></span>
<span data-ttu-id="f2850-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f2850-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2850-116">-Città</span><span class="sxs-lookup"><span data-stu-id="f2850-116">-City</span></span>
<span data-ttu-id="f2850-117">Nome della città.</span><span class="sxs-lookup"><span data-stu-id="f2850-117">The name of the city.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2850-118">-Paese</span><span class="sxs-lookup"><span data-stu-id="f2850-118">-Country</span></span>
<span data-ttu-id="f2850-119">Nome del paese.</span><span class="sxs-lookup"><span data-stu-id="f2850-119">The name of the country.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2850-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2850-120">-DefaultProfile</span></span>
<span data-ttu-id="f2850-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f2850-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2850-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="f2850-122">-EndTime</span></span>
<span data-ttu-id="f2850-123">Ora di fine per il report di accessibilità di Azure.</span><span class="sxs-lookup"><span data-stu-id="f2850-123">The end time for the Azure reachability report.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2850-124">-Posizione</span><span class="sxs-lookup"><span data-stu-id="f2850-124">-Location</span></span>
<span data-ttu-id="f2850-125">Aree di Azure facoltative per l'ambito della query.</span><span class="sxs-lookup"><span data-stu-id="f2850-125">Optional Azure regions to scope the query to.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2850-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f2850-126">-NetworkWatcher</span></span>
<span data-ttu-id="f2850-127">Risorsa Watcher di rete</span><span class="sxs-lookup"><span data-stu-id="f2850-127">The network watcher resource</span></span>

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

### <span data-ttu-id="f2850-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="f2850-128">-NetworkWatcherName</span></span>
<span data-ttu-id="f2850-129">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="f2850-129">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: ResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2850-130">-Provider</span><span class="sxs-lookup"><span data-stu-id="f2850-130">-Provider</span></span>
<span data-ttu-id="f2850-131">Elenco dei provider di servizi Internet.</span><span class="sxs-lookup"><span data-stu-id="f2850-131">List of Internet service providers.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2850-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2850-132">-ResourceGroupName</span></span>
<span data-ttu-id="f2850-133">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="f2850-133">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="f2850-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2850-134">-ResourceId</span></span>
<span data-ttu-id="f2850-135">ID della risorsa Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="f2850-135">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="f2850-136">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f2850-136">-StartTime</span></span>
<span data-ttu-id="f2850-137">Ora di inizio per il report di raggiungibilità di Azure.</span><span class="sxs-lookup"><span data-stu-id="f2850-137">The start time for the Azure reachability report.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2850-138">-Stato</span><span class="sxs-lookup"><span data-stu-id="f2850-138">-State</span></span>
<span data-ttu-id="f2850-139">Nome dello stato.</span><span class="sxs-lookup"><span data-stu-id="f2850-139">The name of the state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2850-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2850-140">CommonParameters</span></span>
<span data-ttu-id="f2850-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2850-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2850-142">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2850-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2850-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f2850-143">INPUTS</span></span>

### <span data-ttu-id="f2850-144">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f2850-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="f2850-145">System. String</span><span class="sxs-lookup"><span data-stu-id="f2850-145">System.String</span></span>

## <span data-ttu-id="f2850-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f2850-146">OUTPUTS</span></span>

### <span data-ttu-id="f2850-147">Microsoft. Azure. Commands. Network. Models. PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="f2850-147">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="f2850-148">Note</span><span class="sxs-lookup"><span data-stu-id="f2850-148">NOTES</span></span>
<span data-ttu-id="f2850-149">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher, raggiungibilità, report</span><span class="sxs-lookup"><span data-stu-id="f2850-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="f2850-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f2850-150">RELATED LINKS</span></span>

[<span data-ttu-id="f2850-151">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f2850-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="f2850-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f2850-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="f2850-153">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f2850-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="f2850-154">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="f2850-154">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="f2850-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="f2850-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="f2850-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="f2850-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="f2850-157">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="f2850-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="f2850-158">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f2850-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f2850-159">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f2850-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="f2850-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f2850-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f2850-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f2850-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f2850-162">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f2850-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)
