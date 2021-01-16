---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: EAFB9C98-000C-4EAC-A32D-6B0F1939AA2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetric.md
ms.openlocfilehash: d02a6f9ca3f4821fa8a552f92ef90fa24a9e6bd2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382672"
---
# <span data-ttu-id="0a888-101">Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="0a888-101">Get-AzMetric</span></span>

## <span data-ttu-id="0a888-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0a888-102">SYNOPSIS</span></span>
<span data-ttu-id="0a888-103">Ottiene i valori metrici di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="0a888-103">Gets the metric values of a resource.</span></span>

## <span data-ttu-id="0a888-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0a888-104">SYNTAX</span></span>

### <span data-ttu-id="0a888-105">GetWithDefaultParameters (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0a888-105">GetWithDefaultParameters (Default)</span></span>
```
Get-AzMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-StartTime <DateTime>] [-EndTime <DateTime>]
 [[-MetricName] <String[]>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a888-106">GetWithFullParameters</span><span class="sxs-lookup"><span data-stu-id="0a888-106">GetWithFullParameters</span></span>
```
Get-AzMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-AggregationType <AggregationType>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Top <Int32>] [-OrderBy <String>] [-MetricNamespace <String>]
 [-ResultType <ResultType>] [-MetricFilter <String>] [-MetricName] <String[]> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a888-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0a888-107">DESCRIPTION</span></span>
<span data-ttu-id="0a888-108">Il cmdlet **Get-AzMetric** ottiene i valori metrici per una risorsa specificata.</span><span class="sxs-lookup"><span data-stu-id="0a888-108">The **Get-AzMetric** cmdlet gets the metric values for a specified resource.</span></span>

## <span data-ttu-id="0a888-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0a888-109">EXAMPLES</span></span>

### <span data-ttu-id="0a888-110">Esempio 1: ottenere una metrica con output riepilogato</span><span class="sxs-lookup"><span data-stu-id="0a888-110">Example 1: Get a metric with summarized output</span></span>
```
PS C:\>Get-AzMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00
DimensionName  : 
DimensionValue : 
Name           : AverageResponseTime
EndTime        : 3/20/2015 6:40:46 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, 
                 Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3
StartTime      : 3/20/2015 5:40:00 PM
TimeGrain      : 00:01:00
Unit           : Seconds
DimensionName  : 
DimensionValue : 
Name           : AverageMemoryWorkingSet
EndTime        : 3/20/2015 6:40:46 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, 
                 Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3
StartTime      : 3/20/2015 5:40:00 PM
TimeGrain      : 00:01:00
Unit           : Bytes
```

<span data-ttu-id="0a888-111">Questo comando consente di ottenere i valori metrici per WebSite3 con una granulosità temporale di 1 minuto.</span><span class="sxs-lookup"><span data-stu-id="0a888-111">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>

### <span data-ttu-id="0a888-112">Esempio 2: ottenere una metrica con output dettagliato</span><span class="sxs-lookup"><span data-stu-id="0a888-112">Example 2: Get a metric with detailed output</span></span>
```
PS C:\>Get-AzMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00 -DetailedOutput
MetricValues   : 
                     Average    : 0
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:37:00 PM
                     Total      : 0
                     Average    : 0.106
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:39:00 PM
                     Total      : 0.106
                     Average    : 0.064
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:41:00 PM
                     Total      : 0.064
Properties     : 
DimensionName  : 
DimensionValue : 
Name           : AverageResponseTime
EndTime        : 3/20/2015 6:43:33 PM
ResourceId     : /subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3
StartTime      : 3/20/2015 5:43:00 PM
TimeGrain      : 00:01:00
Unit           : Seconds
```

<span data-ttu-id="0a888-113">Questo comando consente di ottenere i valori metrici per WebSite3 con una granulosità temporale di 1 minuto.</span><span class="sxs-lookup"><span data-stu-id="0a888-113">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>
<span data-ttu-id="0a888-114">L'output è dettagliato.</span><span class="sxs-lookup"><span data-stu-id="0a888-114">The output is detailed.</span></span>

### <span data-ttu-id="0a888-115">Esempio 3: ottenere l'output dettagliato per una metrica specificata</span><span class="sxs-lookup"><span data-stu-id="0a888-115">Example 3: Get detailed output for a specified metric</span></span>
```
PS C:\>Get-AzMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -MetricName "Requests" -TimeGrain 00:01:00 -DetailedOutput
MetricValues   : 
                     Average    : 1
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:39:00 PM
                     Total      : 1
                     Average    : 1
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:41:00 PM
                     Total      : 1
                     Average    : 0
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:43:00 PM
                     Total      : 0
                     Average    : 1
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:44:00 PM
                     Total      : 1
                     Average    : 0
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:45:00 PM
                     Total      : 0
Properties     : 
DimensionName  : 
DimensionValue : 
Name           : Requests
EndTime        : 3/20/2015 6:47:56 PM
ResourceId     : /subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3
StartTime      : 3/20/2015 5:47:00 PM
TimeGrain      : 00:01:00
Unit           : Count
```

<span data-ttu-id="0a888-116">Questo comando ottiene l'output dettagliato per la metrica richieste.</span><span class="sxs-lookup"><span data-stu-id="0a888-116">This command gets detailed output for the Requests metric.</span></span>

### <span data-ttu-id="0a888-117">Esempio 4: ottenere l'output riepilogato per una metrica specificata con il filtro di dimensione specificato</span><span class="sxs-lookup"><span data-stu-id="0a888-117">Example 4: Get summarized output for a specified metric with specified dimension filter</span></span>
```
PS C:\> $dimFilter = @((New-AzMetricFilter -Dimension City -Operator eq -Value "Seattle","Toronto"), (New-AzMetricFilter -Dimension AuthenticationType -Operator eq -Value User))

PS C:\> Get-AzMetric -ResourceId <resourceId> -MetricName PageViews -TimeGrain PT5M -MetricFilter $dimFilter -StartTime 2018-02-01T12:00:00Z -EndTime 2018-02-01T12:10:00Z -AggregationType -Average
ResourceId  : [ResourceId]
MetricNamespace : Microsoft.Insights/ApplicationInsights
Metric Name :
                    LocalizedValue  : Page Views
                    Value       : PageViews
Unit        : Seconds
Timeseries  :
            City            : Seattle
            AuthenticationType  : User

                    Timestamp   : 2018-02-01 12:00:00 PM
                    Average     : 3518

                    Timestamp   : 2018-02-01 12:05:00 PM
                    Average     : 1984

            City            : Toronto
            AuthenticationType  : User

                    Timestamp   : 2018-02-01 12:00:00 PM
                    Average     : 894

                    Timestamp   : 2018-02-01 12:05:00 PM
                    Average     : 967
```

<span data-ttu-id="0a888-118">Questo comando ottiene l'output riepilogato per la metrica delle visualizzazioni di pagina con il filtro di dimensione e il tipo di aggregazione specificati.</span><span class="sxs-lookup"><span data-stu-id="0a888-118">This command gets summarized output for the PageViews metric with specified dimension filter and aggregation type.</span></span>

## <span data-ttu-id="0a888-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0a888-119">PARAMETERS</span></span>

### <span data-ttu-id="0a888-120">-AggregationType</span><span class="sxs-lookup"><span data-stu-id="0a888-120">-AggregationType</span></span>
<span data-ttu-id="0a888-121">Tipo di aggregazione della query</span><span class="sxs-lookup"><span data-stu-id="0a888-121">The aggregation type of the query</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Monitor.Models.AggregationType]
Parameter Sets: GetWithFullParameters
Aliases:
Accepted values: None, Average, Count, Minimum, Maximum, Total

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a888-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a888-122">-DefaultProfile</span></span>
<span data-ttu-id="0a888-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0a888-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a888-124">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="0a888-124">-DetailedOutput</span></span>
<span data-ttu-id="0a888-125">Indica che questo cmdlet Visualizza l'output dettagliato.</span><span class="sxs-lookup"><span data-stu-id="0a888-125">Indicates that this cmdlet displays detailed output.</span></span>
<span data-ttu-id="0a888-126">Per impostazione predefinita, l'output viene riepilogato.</span><span class="sxs-lookup"><span data-stu-id="0a888-126">By default, output is summarized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a888-127">-EndTime</span><span class="sxs-lookup"><span data-stu-id="0a888-127">-EndTime</span></span>
<span data-ttu-id="0a888-128">Specifica l'ora di fine della query in ora locale.</span><span class="sxs-lookup"><span data-stu-id="0a888-128">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="0a888-129">L'impostazione predefinita è l'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="0a888-129">The default is the current time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a888-130">-MetricFilter</span><span class="sxs-lookup"><span data-stu-id="0a888-130">-MetricFilter</span></span>
<span data-ttu-id="0a888-131">Specifica il filtro della dimensione metrica per la query delle metriche.</span><span class="sxs-lookup"><span data-stu-id="0a888-131">Specifies the metric dimension filter to query metrics for.</span></span>

```yaml
Type: System.String
Parameter Sets: GetWithFullParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a888-132">-Metricname</span><span class="sxs-lookup"><span data-stu-id="0a888-132">-MetricName</span></span>
<span data-ttu-id="0a888-133">Specifica una matrice di nomi di metriche.</span><span class="sxs-lookup"><span data-stu-id="0a888-133">Specifies an array of names of metrics.</span></span>

```yaml
Type: System.String[]
Parameter Sets: GetWithDefaultParameters
Aliases: MetricNames

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: GetWithFullParameters
Aliases: MetricNames

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a888-134">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="0a888-134">-MetricNamespace</span></span>
<span data-ttu-id="0a888-135">Specifica lo spazio dei nomi Metric a cui eseguire la query metriche.</span><span class="sxs-lookup"><span data-stu-id="0a888-135">Specifies the metric namespace to query metrics for.</span></span>

```yaml
Type: System.String
Parameter Sets: GetWithFullParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a888-136">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="0a888-136">-OrderBy</span></span>
<span data-ttu-id="0a888-137">Specifica l'aggregazione da usare per l'ordinamento dei risultati e la direzione dell'ordinamento (esempio: Sum ASC).</span><span class="sxs-lookup"><span data-stu-id="0a888-137">Specifies the aggregation to use for sorting results and the direction of the sort (Example: sum asc).</span></span>

```yaml
Type: System.String
Parameter Sets: GetWithFullParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a888-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a888-138">-ResourceId</span></span>
<span data-ttu-id="0a888-139">Specifica l'ID risorsa della metrica.</span><span class="sxs-lookup"><span data-stu-id="0a888-139">Specifies the resource ID of the metric.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a888-140">-ResultType</span><span class="sxs-lookup"><span data-stu-id="0a888-140">-ResultType</span></span>
<span data-ttu-id="0a888-141">Specifica il tipo di risultato da restituire (metadati o dati).</span><span class="sxs-lookup"><span data-stu-id="0a888-141">Specifies the result type to be returned (metadata or data).</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Monitor.Models.ResultType]
Parameter Sets: GetWithFullParameters
Aliases:
Accepted values: Data, Metadata

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a888-142">-StartTime</span><span class="sxs-lookup"><span data-stu-id="0a888-142">-StartTime</span></span>
<span data-ttu-id="0a888-143">Specifica l'ora di inizio della query in ora locale.</span><span class="sxs-lookup"><span data-stu-id="0a888-143">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="0a888-144">L'impostazione predefinita è l'ora locale corrente meno un'ora.</span><span class="sxs-lookup"><span data-stu-id="0a888-144">The default is the current local time minus one hour.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a888-145">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="0a888-145">-TimeGrain</span></span>
<span data-ttu-id="0a888-146">Specifica la granulosità temporale della metrica come oggetto **TimeSpan** nel formato HH: mm: SS.</span><span class="sxs-lookup"><span data-stu-id="0a888-146">Specifies the time grain of the metric as a **TimeSpan** object in the format hh:mm:ss.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a888-147">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="0a888-147">-Top</span></span>
<span data-ttu-id="0a888-148">Specifica il numero massimo di record da recuperare (impostazione predefinita: 10), da specificare con $filter.</span><span class="sxs-lookup"><span data-stu-id="0a888-148">Specifies the maximum number of records to retrieve (default:10), to be specified with $filter.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetWithFullParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a888-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a888-149">CommonParameters</span></span>
<span data-ttu-id="0a888-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a888-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a888-151">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0a888-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a888-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0a888-152">INPUTS</span></span>

### <span data-ttu-id="0a888-153">System. String</span><span class="sxs-lookup"><span data-stu-id="0a888-153">System.String</span></span>

### <span data-ttu-id="0a888-154">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="0a888-154">System.TimeSpan</span></span>

### <span data-ttu-id="0a888-155">System. Nullable ' 1 [[Microsoft. Azure. Management. monitor. Models. AggregationType, Microsoft. Azure. Management. monitor, Version = 0.21.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="0a888-155">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Models.AggregationType, Microsoft.Azure.Management.Monitor, Version=0.21.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="0a888-156">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="0a888-156">System.DateTime</span></span>

### <span data-ttu-id="0a888-157">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0a888-157">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="0a888-158">System. Nullable ' 1 [[Microsoft. Azure. Management. monitor. Models. ResultType, Microsoft. Azure. Management. monitor, Version = 0.21.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="0a888-158">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Models.ResultType, Microsoft.Azure.Management.Monitor, Version=0.21.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="0a888-159">System. String []</span><span class="sxs-lookup"><span data-stu-id="0a888-159">System.String[]</span></span>

### <span data-ttu-id="0a888-160">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0a888-160">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0a888-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0a888-161">OUTPUTS</span></span>

### <span data-ttu-id="0a888-162">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetric</span><span class="sxs-lookup"><span data-stu-id="0a888-162">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetric</span></span>

## <span data-ttu-id="0a888-163">Note</span><span class="sxs-lookup"><span data-stu-id="0a888-163">NOTES</span></span>

<span data-ttu-id="0a888-164">Altre informazioni sulle metriche supportate possono essere trovate in: https://docs.microsoft.com/en-us/azure/azure-monitor/platform/metrics-supported</span><span class="sxs-lookup"><span data-stu-id="0a888-164">More information about the supported metrics may be found at: https://docs.microsoft.com/en-us/azure/azure-monitor/platform/metrics-supported</span></span>

## <span data-ttu-id="0a888-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0a888-165">RELATED LINKS</span></span>

<span data-ttu-id="0a888-166">[Get-AzMetricDefinition](./Get-AzMetricDefinition.md) 
 [New-AzMetricFilter](./New-AzMetricFilter.md)</span><span class="sxs-lookup"><span data-stu-id="0a888-166">[Get-AzMetricDefinition](./Get-AzMetricDefinition.md)
[New-AzMetricFilter](./New-AzMetricFilter.md)</span></span>


