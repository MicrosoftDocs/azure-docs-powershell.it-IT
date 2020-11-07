---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: EAFB9C98-000C-4EAC-A32D-6B0F1939AA2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetric.md
ms.openlocfilehash: 63ade199b63e57cc72e965002942773f47214494
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685726"
---
# <span data-ttu-id="aef06-101">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="aef06-101">Get-AzureRmMetric</span></span>

## <span data-ttu-id="aef06-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aef06-102">SYNOPSIS</span></span>
<span data-ttu-id="aef06-103">Ottiene i valori metrici di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="aef06-103">Gets the metric values of a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aef06-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aef06-104">SYNTAX</span></span>

### <span data-ttu-id="aef06-105">GetWithDefaultParameters</span><span class="sxs-lookup"><span data-stu-id="aef06-105">GetWithDefaultParameters</span></span>
```
Get-AzureRmMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-StartTime <DateTime>] [-EndTime <DateTime>]
 [[-MetricName] <String[]>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aef06-106">GetWithFullParameters</span><span class="sxs-lookup"><span data-stu-id="aef06-106">GetWithFullParameters</span></span>
```
Get-AzureRmMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-AggregationType <AggregationType>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-MetricName] <String[]> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aef06-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aef06-107">DESCRIPTION</span></span>
<span data-ttu-id="aef06-108">Il cmdlet **Get-AzureRmMetric** ottiene i valori metrici per una risorsa specificata.</span><span class="sxs-lookup"><span data-stu-id="aef06-108">The **Get-AzureRmMetric** cmdlet gets the metric values for a specified resource.</span></span>

## <span data-ttu-id="aef06-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aef06-109">EXAMPLES</span></span>

### <span data-ttu-id="aef06-110">Esempio 1: ottenere una metrica con output riepilogato</span><span class="sxs-lookup"><span data-stu-id="aef06-110">Example 1: Get a metric with summarized output</span></span>
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

<span data-ttu-id="aef06-111">Questo comando consente di ottenere i valori metrici per WebSite3 con una granulosità temporale di 1 minuto.</span><span class="sxs-lookup"><span data-stu-id="aef06-111">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>

### <span data-ttu-id="aef06-112">Esempio 2: ottenere una metrica con output dettagliato</span><span class="sxs-lookup"><span data-stu-id="aef06-112">Example 2: Get a metric with detailed output</span></span>
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

<span data-ttu-id="aef06-113">Questo comando consente di ottenere i valori metrici per WebSite3 con una granulosità temporale di 1 minuto.</span><span class="sxs-lookup"><span data-stu-id="aef06-113">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>
<span data-ttu-id="aef06-114">L'output è dettagliato.</span><span class="sxs-lookup"><span data-stu-id="aef06-114">The output is detailed.</span></span>

### <span data-ttu-id="aef06-115">Esempio 3: ottenere l'output dettagliato per una metrica specificata</span><span class="sxs-lookup"><span data-stu-id="aef06-115">Example 3: Get detailed output for a specified metric</span></span>
```
PS C:\>Get-AzureRmMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00 -DetailedOutput -MetricNames "Requests"
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

<span data-ttu-id="aef06-116">Questo comando ottiene l'output dettagliato per la metrica richieste.</span><span class="sxs-lookup"><span data-stu-id="aef06-116">This command gets detailed output for the Requests metric.</span></span>

## <span data-ttu-id="aef06-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aef06-117">PARAMETERS</span></span>

### <span data-ttu-id="aef06-118">-AggregationType</span><span class="sxs-lookup"><span data-stu-id="aef06-118">-AggregationType</span></span>
<span data-ttu-id="aef06-119">Tipo di aggregazione della query</span><span class="sxs-lookup"><span data-stu-id="aef06-119">The aggregation type of the query</span></span>

```yaml
Type: AggregationType
Parameter Sets: GetWithFullParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aef06-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aef06-120">-DefaultProfile</span></span>
<span data-ttu-id="aef06-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aef06-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aef06-122">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="aef06-122">-DetailedOutput</span></span>
<span data-ttu-id="aef06-123">Indica che questo cmdlet Visualizza l'output dettagliato.</span><span class="sxs-lookup"><span data-stu-id="aef06-123">Indicates that this cmdlet displays detailed output.</span></span>
<span data-ttu-id="aef06-124">Per impostazione predefinita, l'output viene riepilogato.</span><span class="sxs-lookup"><span data-stu-id="aef06-124">By default, output is summarized.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aef06-125">-EndTime</span><span class="sxs-lookup"><span data-stu-id="aef06-125">-EndTime</span></span>
<span data-ttu-id="aef06-126">Specifica l'ora di fine della query in ora locale.</span><span class="sxs-lookup"><span data-stu-id="aef06-126">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="aef06-127">L'impostazione predefinita è l'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="aef06-127">The default is the current time.</span></span>

```yaml
Type: DateTime
Parameter Sets: GetWithFullParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aef06-128">-Metricname</span><span class="sxs-lookup"><span data-stu-id="aef06-128">-MetricName</span></span>
<span data-ttu-id="aef06-129">Specifica una matrice di nomi di metriche.</span><span class="sxs-lookup"><span data-stu-id="aef06-129">Specifies an array of names of metrics.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: MetricNames

Required: False (GetWithDefaultParameters), True (GetAzureRmAMetricFullParamGroup)
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: GetWithFullParameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aef06-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aef06-130">-ResourceId</span></span>
<span data-ttu-id="aef06-131">Specifica l'ID risorsa della metrica.</span><span class="sxs-lookup"><span data-stu-id="aef06-131">Specifies the resource ID of the metric.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aef06-132">-StartTime</span><span class="sxs-lookup"><span data-stu-id="aef06-132">-StartTime</span></span>
<span data-ttu-id="aef06-133">Specifica l'ora di inizio della query in ora locale.</span><span class="sxs-lookup"><span data-stu-id="aef06-133">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="aef06-134">L'impostazione predefinita è l'ora locale corrente meno un'ora.</span><span class="sxs-lookup"><span data-stu-id="aef06-134">The default is the current local time minus one hour.</span></span>

```yaml
Type: DateTime
Parameter Sets: GetWithFullParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aef06-135">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="aef06-135">-TimeGrain</span></span>
<span data-ttu-id="aef06-136">Specifica la granulosità temporale della metrica come oggetto **TimeSpan** nel formato HH: mm: SS.</span><span class="sxs-lookup"><span data-stu-id="aef06-136">Specifies the time grain of the metric as a **TimeSpan** object in the format hh:mm:ss.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: GetWithFullParameters
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aef06-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aef06-137">CommonParameters</span></span>
<span data-ttu-id="aef06-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aef06-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aef06-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aef06-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aef06-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aef06-140">INPUTS</span></span>

### <span data-ttu-id="aef06-141">Nessuno</span><span class="sxs-lookup"><span data-stu-id="aef06-141">None</span></span>
<span data-ttu-id="aef06-142">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="aef06-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="aef06-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aef06-143">OUTPUTS</span></span>

### <span data-ttu-id="aef06-144">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetric []</span><span class="sxs-lookup"><span data-stu-id="aef06-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetric[]</span></span>

## <span data-ttu-id="aef06-145">Note</span><span class="sxs-lookup"><span data-stu-id="aef06-145">NOTES</span></span>

## <span data-ttu-id="aef06-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aef06-146">RELATED LINKS</span></span>

[<span data-ttu-id="aef06-147">Get-AzureRmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="aef06-147">Get-AzureRmMetricDefinition</span></span>](./Get-AzureRmMetricDefinition.md)


