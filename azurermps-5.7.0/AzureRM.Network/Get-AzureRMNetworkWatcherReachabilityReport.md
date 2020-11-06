---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRMNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRMNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 7ec4ebbe9e1224e47605a35f7f21feb2dfbcf045
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518936"
---
# <span data-ttu-id="71950-101">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="71950-101">Get-AzureRMNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="71950-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="71950-102">SYNOPSIS</span></span>
<span data-ttu-id="71950-103">Ottiene il punteggio relativo alla latenza per i provider di servizi Internet da una posizione specificata alle aree di Azure.</span><span class="sxs-lookup"><span data-stu-id="71950-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71950-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="71950-104">SYNTAX</span></span>

### <span data-ttu-id="71950-105">SetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="71950-105">SetByName (Default)</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="71950-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="71950-106">SetByResource</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="71950-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="71950-107">SetByResourceId</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -ResourceId <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="71950-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71950-108">DESCRIPTION</span></span>
<span data-ttu-id="71950-109">Il Get-AzureRmNetworkWatcherReachabilityReport ottiene il punteggio relativo alla latenza per i provider di servizi Internet da una posizione specificata alle aree di Azure.</span><span class="sxs-lookup"><span data-stu-id="71950-109">The Get-AzureRmNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="71950-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="71950-110">EXAMPLES</span></span>

### <span data-ttu-id="71950-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="71950-111">Example 1</span></span>
```
$nw = Get-AzureRmNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
Get-AzureRmNetworkWatcherReachabilityReport -NetworkWatcher $nw -Location "West US" -Country "United States" -StartTime "2017-10-10" -EndTime "2017-10-12"

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

<span data-ttu-id="71950-112">Ottiene le latenze relative al Data Center di Azure in West US da 2017-10-10 a 2017-10-12 all'interno dello stato United.</span><span class="sxs-lookup"><span data-stu-id="71950-112">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

## <span data-ttu-id="71950-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="71950-113">PARAMETERS</span></span>

### <span data-ttu-id="71950-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71950-114">-AsJob</span></span>
<span data-ttu-id="71950-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="71950-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="71950-116">-Città</span><span class="sxs-lookup"><span data-stu-id="71950-116">-City</span></span>
<span data-ttu-id="71950-117">Nome della città.</span><span class="sxs-lookup"><span data-stu-id="71950-117">The name of the city.</span></span>

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

### <span data-ttu-id="71950-118">-Paese</span><span class="sxs-lookup"><span data-stu-id="71950-118">-Country</span></span>
<span data-ttu-id="71950-119">Nome del paese.</span><span class="sxs-lookup"><span data-stu-id="71950-119">The name of the country.</span></span>

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

### <span data-ttu-id="71950-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71950-120">-DefaultProfile</span></span>
<span data-ttu-id="71950-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="71950-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71950-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="71950-122">-EndTime</span></span>
<span data-ttu-id="71950-123">Ora di fine per il report di accessibilità di Azure.</span><span class="sxs-lookup"><span data-stu-id="71950-123">The end time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="71950-124">-Posizione</span><span class="sxs-lookup"><span data-stu-id="71950-124">-Location</span></span>
<span data-ttu-id="71950-125">Aree di Azure facoltative per l'ambito della query.</span><span class="sxs-lookup"><span data-stu-id="71950-125">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="71950-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="71950-126">-NetworkWatcher</span></span>
<span data-ttu-id="71950-127">Risorsa Watcher di rete</span><span class="sxs-lookup"><span data-stu-id="71950-127">The network watcher resource</span></span>

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

### <span data-ttu-id="71950-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="71950-128">-NetworkWatcherName</span></span>
<span data-ttu-id="71950-129">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="71950-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="71950-130">-Provider</span><span class="sxs-lookup"><span data-stu-id="71950-130">-Provider</span></span>
<span data-ttu-id="71950-131">Elenco dei provider di servizi Internet.</span><span class="sxs-lookup"><span data-stu-id="71950-131">List of Internet service providers.</span></span>

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

### <span data-ttu-id="71950-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71950-132">-ResourceGroupName</span></span>
<span data-ttu-id="71950-133">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="71950-133">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="71950-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71950-134">-ResourceId</span></span>
<span data-ttu-id="71950-135">ID della risorsa Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="71950-135">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="71950-136">-StartTime</span><span class="sxs-lookup"><span data-stu-id="71950-136">-StartTime</span></span>
<span data-ttu-id="71950-137">Ora di inizio per il report di raggiungibilità di Azure.</span><span class="sxs-lookup"><span data-stu-id="71950-137">The start time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="71950-138">-Stato</span><span class="sxs-lookup"><span data-stu-id="71950-138">-State</span></span>
<span data-ttu-id="71950-139">Nome dello stato.</span><span class="sxs-lookup"><span data-stu-id="71950-139">The name of the state.</span></span>

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

### <span data-ttu-id="71950-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71950-140">CommonParameters</span></span>
<span data-ttu-id="71950-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71950-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71950-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71950-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71950-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="71950-143">INPUTS</span></span>

### <span data-ttu-id="71950-144">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="71950-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="71950-145">System. String</span><span class="sxs-lookup"><span data-stu-id="71950-145">System.String</span></span>

## <span data-ttu-id="71950-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="71950-146">OUTPUTS</span></span>

### <span data-ttu-id="71950-147">Microsoft. Azure. Commands. Network. Models. PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="71950-147">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="71950-148">Note</span><span class="sxs-lookup"><span data-stu-id="71950-148">NOTES</span></span>
<span data-ttu-id="71950-149">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher, raggiungibilità, report</span><span class="sxs-lookup"><span data-stu-id="71950-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="71950-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="71950-150">RELATED LINKS</span></span>

[<span data-ttu-id="71950-151">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="71950-151">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="71950-152">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="71950-152">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="71950-153">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="71950-153">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="71950-154">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="71950-154">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="71950-155">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="71950-155">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="71950-156">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="71950-156">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="71950-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="71950-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="71950-158">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="71950-158">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="71950-159">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="71950-159">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="71950-160">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="71950-160">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="71950-161">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="71950-161">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="71950-162">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="71950-162">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)
