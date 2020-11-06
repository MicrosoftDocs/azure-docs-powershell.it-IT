---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: EAFB9C98-000C-4EAC-A32D-6B0F1939AA2F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetric.md
ms.openlocfilehash: d8b7c83ff2804de3e60af7c5ea8ce9f3e2d1eb97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520090"
---
# <span data-ttu-id="8026e-101">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="8026e-101">Get-AzureRmMetric</span></span>

## <span data-ttu-id="8026e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8026e-102">SYNOPSIS</span></span>
<span data-ttu-id="8026e-103">Ottiene i valori metrici di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="8026e-103">Gets the metric values of a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8026e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8026e-104">SYNTAX</span></span>

### <span data-ttu-id="8026e-105">Parametri per Get-AzureRmMetric cmdlet nella modalità predefinita</span><span class="sxs-lookup"><span data-stu-id="8026e-105">Parameters for Get-AzureRmMetric cmdlet in the default mode</span></span>
```
Get-AzureRmMetric [-ResourceId] <String> [-MetricNames <String[]>] [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8026e-106">Parametri per Get-AzureRmMetric cmdlet nella modalità set di param completo</span><span class="sxs-lookup"><span data-stu-id="8026e-106">Parameters for Get-AzureRmMetric cmdlet in the full param set mode</span></span>
```
Get-AzureRmMetric [-ResourceId] <String> [[-TimeGrain] <TimeSpan>] [-AggregationType <AggregationType>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] -MetricNames <String[]> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8026e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8026e-107">DESCRIPTION</span></span>
<span data-ttu-id="8026e-108">Il cmdlet **Get-AzureRmMetric** ottiene i valori metrici per una risorsa specificata.</span><span class="sxs-lookup"><span data-stu-id="8026e-108">The **Get-AzureRmMetric** cmdlet gets the metric values for a specified resource.</span></span>

## <span data-ttu-id="8026e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8026e-109">EXAMPLES</span></span>

### <span data-ttu-id="8026e-110">Esempio 1: ottenere una metrica con output riepilogato</span><span class="sxs-lookup"><span data-stu-id="8026e-110">Example 1: Get a metric with summarized output</span></span>
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

<span data-ttu-id="8026e-111">Questo comando consente di ottenere i valori metrici per WebSite3 con una granulosità temporale di 1 minuto.</span><span class="sxs-lookup"><span data-stu-id="8026e-111">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>

### <span data-ttu-id="8026e-112">Esempio 2: ottenere una metrica con output dettagliato</span><span class="sxs-lookup"><span data-stu-id="8026e-112">Example 2: Get a metric with detailed output</span></span>
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

<span data-ttu-id="8026e-113">Questo comando consente di ottenere i valori metrici per WebSite3 con una granulosità temporale di 1 minuto.</span><span class="sxs-lookup"><span data-stu-id="8026e-113">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>
<span data-ttu-id="8026e-114">L'output è dettagliato.</span><span class="sxs-lookup"><span data-stu-id="8026e-114">The output is detailed.</span></span>

### <span data-ttu-id="8026e-115">Esempio 3: ottenere l'output dettagliato per una metrica specificata</span><span class="sxs-lookup"><span data-stu-id="8026e-115">Example 3: Get detailed output for a specified metric</span></span>
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

<span data-ttu-id="8026e-116">Questo comando ottiene l'output dettagliato per la metrica richieste.</span><span class="sxs-lookup"><span data-stu-id="8026e-116">This command gets detailed output for the Requests metric.</span></span>

## <span data-ttu-id="8026e-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8026e-117">PARAMETERS</span></span>

### <span data-ttu-id="8026e-118">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="8026e-118">-DetailedOutput</span></span>
<span data-ttu-id="8026e-119">Indica che questo cmdlet Visualizza l'output dettagliato.</span><span class="sxs-lookup"><span data-stu-id="8026e-119">Indicates that this cmdlet displays detailed output.</span></span>
<span data-ttu-id="8026e-120">Per impostazione predefinita, l'output viene riepilogato.</span><span class="sxs-lookup"><span data-stu-id="8026e-120">By default, output is summarized.</span></span>

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

### <span data-ttu-id="8026e-121">-EndTime</span><span class="sxs-lookup"><span data-stu-id="8026e-121">-EndTime</span></span>
<span data-ttu-id="8026e-122">Specifica l'ora di fine della query in ora locale.</span><span class="sxs-lookup"><span data-stu-id="8026e-122">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="8026e-123">L'impostazione predefinita è l'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="8026e-123">The default is the current time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: Parameters for Get-AzureRmMetric cmdlet in the full param set mode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8026e-124">-MetricNames</span><span class="sxs-lookup"><span data-stu-id="8026e-124">-MetricNames</span></span>
<span data-ttu-id="8026e-125">Specifica una matrice di nomi di metriche.</span><span class="sxs-lookup"><span data-stu-id="8026e-125">Specifies an array of names of metrics.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Parameters for Get-AzureRmMetric cmdlet in the default mode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: Parameters for Get-AzureRmMetric cmdlet in the full param set mode
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8026e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8026e-126">-ResourceId</span></span>
<span data-ttu-id="8026e-127">Specifica l'ID risorsa della metrica.</span><span class="sxs-lookup"><span data-stu-id="8026e-127">Specifies the resource ID of the metric.</span></span>

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

### <span data-ttu-id="8026e-128">-StartTime</span><span class="sxs-lookup"><span data-stu-id="8026e-128">-StartTime</span></span>
<span data-ttu-id="8026e-129">Specifica l'ora di inizio della query in ora locale.</span><span class="sxs-lookup"><span data-stu-id="8026e-129">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="8026e-130">L'impostazione predefinita è l'ora locale corrente meno un'ora.</span><span class="sxs-lookup"><span data-stu-id="8026e-130">The default is the current local time minus one hour.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: Parameters for Get-AzureRmMetric cmdlet in the full param set mode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8026e-131">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="8026e-131">-TimeGrain</span></span>
<span data-ttu-id="8026e-132">Specifica la granulosità temporale della metrica come oggetto **TimeSpan** nel formato HH: mm: SS.</span><span class="sxs-lookup"><span data-stu-id="8026e-132">Specifies the time grain of the metric as a **TimeSpan** object in the format hh:mm:ss.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Parameters for Get-AzureRmMetric cmdlet in the full param set mode
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8026e-133">-AggregationType</span><span class="sxs-lookup"><span data-stu-id="8026e-133">-AggregationType</span></span>
<span data-ttu-id="8026e-134">Tipo di aggregazione di Quer</span><span class="sxs-lookup"><span data-stu-id="8026e-134">The aggregation type of the quer</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Monitor.Models.AggregationType]
Parameter Sets: Parameters for Get-AzureRmMetric cmdlet in the full param set mode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8026e-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8026e-135">-DefaultProfile</span></span>
<span data-ttu-id="8026e-136">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8026e-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8026e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8026e-137">CommonParameters</span></span>
<span data-ttu-id="8026e-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8026e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8026e-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8026e-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8026e-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8026e-140">INPUTS</span></span>

## <span data-ttu-id="8026e-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8026e-141">OUTPUTS</span></span>

### <span data-ttu-id="8026e-142">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetric []</span><span class="sxs-lookup"><span data-stu-id="8026e-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetric[]</span></span>

## <span data-ttu-id="8026e-143">Note</span><span class="sxs-lookup"><span data-stu-id="8026e-143">NOTES</span></span>

## <span data-ttu-id="8026e-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8026e-144">RELATED LINKS</span></span>

[<span data-ttu-id="8026e-145">Get-AzureRmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="8026e-145">Get-AzureRmMetricDefinition</span></span>](./Get-AzureRmMetricDefinition.md)


