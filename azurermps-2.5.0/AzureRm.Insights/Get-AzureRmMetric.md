---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: EAFB9C98-000C-4EAC-A32D-6B0F1939AA2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermmetric
schema: 2.0.0
ms.openlocfilehash: 5a0594bc1a90457874a590628076daf7e7d49d8d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865833"
---
# <span data-ttu-id="c7f59-101">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="c7f59-101">Get-AzureRmMetric</span></span>

## <span data-ttu-id="c7f59-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c7f59-102">SYNOPSIS</span></span>
<span data-ttu-id="c7f59-103">Ottiene i valori metrici di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="c7f59-103">Gets the metric values of a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7f59-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c7f59-104">SYNTAX</span></span>

### <span data-ttu-id="c7f59-105">GetWithDefaultParameters (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c7f59-105">GetWithDefaultParameters (Default)</span></span>
```
Get-AzureRmMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-StartTime <DateTime>] [-EndTime <DateTime>]
 [[-MetricName] <String[]>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7f59-106">GetWithFullParameters</span><span class="sxs-lookup"><span data-stu-id="c7f59-106">GetWithFullParameters</span></span>
```
Get-AzureRmMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-AggregationType <AggregationType>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Top <Int32>] [-OrderBy <String>] [-MetricNamespace <String>]
 [-ResultType <ResultType>] [-MetricFilter <String>] [-MetricName] <String[]> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7f59-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c7f59-107">DESCRIPTION</span></span>
<span data-ttu-id="c7f59-108">Il cmdlet **Get-AzureRmMetric** ottiene i valori metrici per una risorsa specificata.</span><span class="sxs-lookup"><span data-stu-id="c7f59-108">The **Get-AzureRmMetric** cmdlet gets the metric values for a specified resource.</span></span>

## <span data-ttu-id="c7f59-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c7f59-109">EXAMPLES</span></span>

### <span data-ttu-id="c7f59-110">Esempio 1: ottenere una metrica con output riepilogato</span><span class="sxs-lookup"><span data-stu-id="c7f59-110">Example 1: Get a metric with summarized output</span></span>
```
PS C:\>Get-AzureRmMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00
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

<span data-ttu-id="c7f59-111">Questo comando consente di ottenere i valori metrici per WebSite3 con una granulosità temporale di 1 minuto.</span><span class="sxs-lookup"><span data-stu-id="c7f59-111">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>

### <span data-ttu-id="c7f59-112">Esempio 2: ottenere una metrica con output dettagliato</span><span class="sxs-lookup"><span data-stu-id="c7f59-112">Example 2: Get a metric with detailed output</span></span>
```
PS C:\>Get-AzureRmMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00 -DetailedOutput
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

<span data-ttu-id="c7f59-113">Questo comando consente di ottenere i valori metrici per WebSite3 con una granulosità temporale di 1 minuto.</span><span class="sxs-lookup"><span data-stu-id="c7f59-113">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>
<span data-ttu-id="c7f59-114">L'output è dettagliato.</span><span class="sxs-lookup"><span data-stu-id="c7f59-114">The output is detailed.</span></span>

### <span data-ttu-id="c7f59-115">Esempio 3: ottenere l'output dettagliato per una metrica specificata</span><span class="sxs-lookup"><span data-stu-id="c7f59-115">Example 3: Get detailed output for a specified metric</span></span>
```
PS C:\>Get-AzureRmMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -MetricNames "Requests" -TimeGrain 00:01:00 -DetailedOutput
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

<span data-ttu-id="c7f59-116">Questo comando ottiene l'output dettagliato per la metrica richieste.</span><span class="sxs-lookup"><span data-stu-id="c7f59-116">This command gets detailed output for the Requests metric.</span></span>

### <span data-ttu-id="c7f59-117">Esempio 4: ottenere l'output riepilogato per una metrica specificata con il filtro di dimensione specificato</span><span class="sxs-lookup"><span data-stu-id="c7f59-117">Example 4: Get summarized output for a specified metric with specified dimension filter</span></span>
```
PS C:\> $dimFilter = @((New-AzureRmMetricFilter -Dimension City -Operator eq -Values "Seattle","Toronto"), (New-AzureRmMetricDimensionFilter -Dimension AuthenticationType -Operator eq -Values User))

PS C:\> Get-AzureRmMetricValues -ResourceId <resourcId> -MetricName PageViews -TimeGrain PT5M -MetricFilter $dimFilter -StartTime 2018-02-01T12:00:00Z -EndTime 2018-02-01T12:10:00Z -AggregationType -Average
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

<span data-ttu-id="c7f59-118">Questo comando ottiene l'output riepilogato per la metrica delle visualizzazioni di pagina con il filtro di dimenza e il tipo di aggregazione specificati.</span><span class="sxs-lookup"><span data-stu-id="c7f59-118">This command gets summarized output for the PageViews metric with specified dimesion filter and aggregation type.</span></span>

## <span data-ttu-id="c7f59-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c7f59-119">PARAMETERS</span></span>

### <span data-ttu-id="c7f59-120">-AggregationType</span><span class="sxs-lookup"><span data-stu-id="c7f59-120">-AggregationType</span></span>
<span data-ttu-id="c7f59-121">Tipo di aggregazione della query</span><span class="sxs-lookup"><span data-stu-id="c7f59-121">The aggregation type of the query</span></span>

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

### <span data-ttu-id="c7f59-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7f59-122">-DefaultProfile</span></span>
<span data-ttu-id="c7f59-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c7f59-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7f59-124">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="c7f59-124">-DetailedOutput</span></span>
<span data-ttu-id="c7f59-125">Indica che questo cmdlet Visualizza l'output dettagliato.</span><span class="sxs-lookup"><span data-stu-id="c7f59-125">Indicates that this cmdlet displays detailed output.</span></span>
<span data-ttu-id="c7f59-126">Per impostazione predefinita, l'output viene riepilogato.</span><span class="sxs-lookup"><span data-stu-id="c7f59-126">By default, output is summarized.</span></span>

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

### <span data-ttu-id="c7f59-127">-EndTime</span><span class="sxs-lookup"><span data-stu-id="c7f59-127">-EndTime</span></span>
<span data-ttu-id="c7f59-128">Specifica l'ora di fine della query in ora locale.</span><span class="sxs-lookup"><span data-stu-id="c7f59-128">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="c7f59-129">L'impostazione predefinita è l'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="c7f59-129">The default is the current time.</span></span>

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

### <span data-ttu-id="c7f59-130">-MetricFilter</span><span class="sxs-lookup"><span data-stu-id="c7f59-130">-MetricFilter</span></span>
<span data-ttu-id="c7f59-131">Specifica il filtro della dimensione metrica per la query delle metriche.</span><span class="sxs-lookup"><span data-stu-id="c7f59-131">Specifies the metric dimension filter to query metrics for.</span></span>

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

### <span data-ttu-id="c7f59-132">-Metricname</span><span class="sxs-lookup"><span data-stu-id="c7f59-132">-MetricName</span></span>
<span data-ttu-id="c7f59-133">Specifica una matrice di nomi di metriche.</span><span class="sxs-lookup"><span data-stu-id="c7f59-133">Specifies an array of names of metrics.</span></span>

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

### <span data-ttu-id="c7f59-134">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="c7f59-134">-MetricNamespace</span></span>
<span data-ttu-id="c7f59-135">Specifica lo spazio dei nomi Metric a cui eseguire la query metriche.</span><span class="sxs-lookup"><span data-stu-id="c7f59-135">Specifies the metric namespace to query metrics for.</span></span>

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

### <span data-ttu-id="c7f59-136">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="c7f59-136">-OrderBy</span></span>
<span data-ttu-id="c7f59-137">Specifica l'aggregazione da usare per l'ordinamento dei risultati e la direzione dell'ordinamento (esempio: Sum ASC).</span><span class="sxs-lookup"><span data-stu-id="c7f59-137">Specifies the aggregation to use for sorting results and the direction of the sort (Example: sum asc).</span></span>

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

### <span data-ttu-id="c7f59-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7f59-138">-ResourceId</span></span>
<span data-ttu-id="c7f59-139">Specifica l'ID risorsa della metrica.</span><span class="sxs-lookup"><span data-stu-id="c7f59-139">Specifies the resource ID of the metric.</span></span>

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

### <span data-ttu-id="c7f59-140">-ResultType</span><span class="sxs-lookup"><span data-stu-id="c7f59-140">-ResultType</span></span>
<span data-ttu-id="c7f59-141">Specifica il tipo di risultato da restituire (metadati o dati).</span><span class="sxs-lookup"><span data-stu-id="c7f59-141">Specifies the result type to be returned (metadata or data).</span></span>

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

### <span data-ttu-id="c7f59-142">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c7f59-142">-StartTime</span></span>
<span data-ttu-id="c7f59-143">Specifica l'ora di inizio della query in ora locale.</span><span class="sxs-lookup"><span data-stu-id="c7f59-143">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="c7f59-144">L'impostazione predefinita è l'ora locale corrente meno un'ora.</span><span class="sxs-lookup"><span data-stu-id="c7f59-144">The default is the current local time minus one hour.</span></span>

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

### <span data-ttu-id="c7f59-145">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="c7f59-145">-TimeGrain</span></span>
<span data-ttu-id="c7f59-146">Specifica la granulosità temporale della metrica come oggetto **TimeSpan** nel formato HH: mm: SS.</span><span class="sxs-lookup"><span data-stu-id="c7f59-146">Specifies the time grain of the metric as a **TimeSpan** object in the format hh:mm:ss.</span></span>

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

### <span data-ttu-id="c7f59-147">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="c7f59-147">-Top</span></span>
<span data-ttu-id="c7f59-148">Specifica il numero massimo di record da recuperare (impostazione predefinita: 10), da specificare con $filter.</span><span class="sxs-lookup"><span data-stu-id="c7f59-148">Specifies the maximum number of records to retrieve (default:10), to be specified with $filter.</span></span>

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

### <span data-ttu-id="c7f59-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7f59-149">CommonParameters</span></span>
<span data-ttu-id="c7f59-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7f59-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7f59-151">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7f59-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7f59-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c7f59-152">INPUTS</span></span>

### <span data-ttu-id="c7f59-153">System. String</span><span class="sxs-lookup"><span data-stu-id="c7f59-153">System.String</span></span>

### <span data-ttu-id="c7f59-154">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="c7f59-154">System.TimeSpan</span></span>

### <span data-ttu-id="c7f59-155">System. Nullable ' 1 [[Microsoft. Azure. Management. monitor. Models. AggregationType, Microsoft. Azure. Management. monitor, Version = 0.19.1.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="c7f59-155">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Models.AggregationType, Microsoft.Azure.Management.Monitor, Version=0.19.1.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="c7f59-156">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="c7f59-156">System.DateTime</span></span>

### <span data-ttu-id="c7f59-157">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="c7f59-157">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="c7f59-158">System. Nullable ' 1 [[Microsoft. Azure. Management. monitor. Models. ResultType, Microsoft. Azure. Management. monitor, Version = 0.19.1.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="c7f59-158">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Models.ResultType, Microsoft.Azure.Management.Monitor, Version=0.19.1.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="c7f59-159">System. String []</span><span class="sxs-lookup"><span data-stu-id="c7f59-159">System.String[]</span></span>

### <span data-ttu-id="c7f59-160">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c7f59-160">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c7f59-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c7f59-161">OUTPUTS</span></span>

### <span data-ttu-id="c7f59-162">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetric</span><span class="sxs-lookup"><span data-stu-id="c7f59-162">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetric</span></span>

## <span data-ttu-id="c7f59-163">Note</span><span class="sxs-lookup"><span data-stu-id="c7f59-163">NOTES</span></span>

## <span data-ttu-id="c7f59-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c7f59-164">RELATED LINKS</span></span>

<span data-ttu-id="c7f59-165">[Get-AzureRmMetricDefinition](./Get-AzureRmMetricDefinition.md) 
 [New-AzureRmMetricFilter](./New-AzureRmMetricFilter.md)</span><span class="sxs-lookup"><span data-stu-id="c7f59-165">[Get-AzureRmMetricDefinition](./Get-AzureRmMetricDefinition.md)
[New-AzureRmMetricFilter](./New-AzureRmMetricFilter.md)</span></span>


