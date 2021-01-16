---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7915A7AC-5A47-4868-B846-2896BCEBFAB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azmetricdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricDefinition.md
ms.openlocfilehash: 9ca873736ad86eaac17dd2795ad61716197ceaba
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331828"
---
# <span data-ttu-id="b0c6d-101">Get-AzMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="b0c6d-101">Get-AzMetricDefinition</span></span>

## <span data-ttu-id="b0c6d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b0c6d-102">SYNOPSIS</span></span>
<span data-ttu-id="b0c6d-103">Ottiene le definizioni metriche.</span><span class="sxs-lookup"><span data-stu-id="b0c6d-103">Gets metric definitions.</span></span>

## <span data-ttu-id="b0c6d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b0c6d-104">SYNTAX</span></span>

```
Get-AzMetricDefinition [-ResourceId] <String> [-MetricName <String[]>] [-MetricNamespace <String>]
 [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0c6d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b0c6d-105">DESCRIPTION</span></span>
<span data-ttu-id="b0c6d-106">Il cmdlet **Get-AzMetricDefinition** ottiene le definizioni metriche.</span><span class="sxs-lookup"><span data-stu-id="b0c6d-106">The **Get-AzMetricDefinition** cmdlet gets metric definitions.</span></span>

## <span data-ttu-id="b0c6d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b0c6d-107">EXAMPLES</span></span>

### <span data-ttu-id="b0c6d-108">Esempio 1: ottenere definizioni metriche per una risorsa</span><span class="sxs-lookup"><span data-stu-id="b0c6d-108">Example 1: Get metric definitions for a resource</span></span>
```
PS C:\>Get-AzMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2"
Name                   : CpuTime
Dimensions             : {}
MetricAvailabilities   : {Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability}
PrimaryAggregationType : Total
Properties             : {}
ResourceUri            : 
Unit                   : Seconds
Name                   : Requests
Dimensions             : {}
MetricAvailabilities   : {Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability}
PrimaryAggregationType : Total
Properties             : {}
ResourceUri            : 
Unit                   : Count
```

<span data-ttu-id="b0c6d-109">Questo comando consente di ottenere le definizioni metriche per la risorsa specificata.</span><span class="sxs-lookup"><span data-stu-id="b0c6d-109">This command gets the metrics definitions for the specified resource.</span></span>

### <span data-ttu-id="b0c6d-110">Esempio 2: ottenere definizioni metriche con l'output dettagliato</span><span class="sxs-lookup"><span data-stu-id="b0c6d-110">Example 2: Get metric definitions with detailed output</span></span>
```
PS C:\>Get-AzMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2" -DetailedOutput
Dimensions             : 
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : CpuTime
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Seconds
Dimensions             : 
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : Requests
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Count
```

<span data-ttu-id="b0c6d-111">Questo comando ottiene le definizioni metriche per WebSite2.</span><span class="sxs-lookup"><span data-stu-id="b0c6d-111">This command gets the metric definitions for website2.</span></span>
<span data-ttu-id="b0c6d-112">L'output è dettagliato.</span><span class="sxs-lookup"><span data-stu-id="b0c6d-112">The output is detailed.</span></span>

### <span data-ttu-id="b0c6d-113">Esempio 3: ottenere le definizioni metriche per nome</span><span class="sxs-lookup"><span data-stu-id="b0c6d-113">Example 3: Get metric definitions by name</span></span>
```
PS C:\>Get-AzMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2" -DetailedOutput -MetricName "BytesSent,CpuTime"
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : CpuTime
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Seconds
Dimensions             : 
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : BytesSent
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Bytes
```

<span data-ttu-id="b0c6d-114">Questo comando ottiene le definizioni per le metriche BytesSent e CpuTime.</span><span class="sxs-lookup"><span data-stu-id="b0c6d-114">This command gets definitions for the BytesSent and CpuTime metrics.</span></span>
<span data-ttu-id="b0c6d-115">L'output è dettagliato.</span><span class="sxs-lookup"><span data-stu-id="b0c6d-115">The output is detailed.</span></span>

## <span data-ttu-id="b0c6d-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b0c6d-116">PARAMETERS</span></span>

### <span data-ttu-id="b0c6d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0c6d-117">-DefaultProfile</span></span>
<span data-ttu-id="b0c6d-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b0c6d-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b0c6d-119">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="b0c6d-119">-DetailedOutput</span></span>
<span data-ttu-id="b0c6d-120">Indica che questa operazione include l'output dettagliato.</span><span class="sxs-lookup"><span data-stu-id="b0c6d-120">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="b0c6d-121">Se non specifichi questo parametro, l'output viene riepilogato.</span><span class="sxs-lookup"><span data-stu-id="b0c6d-121">If you do not specify this parameter, the output is summarized.</span></span>

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

### <span data-ttu-id="b0c6d-122">-Metricname</span><span class="sxs-lookup"><span data-stu-id="b0c6d-122">-MetricName</span></span>
<span data-ttu-id="b0c6d-123">Specifica una matrice di nomi di metriche.</span><span class="sxs-lookup"><span data-stu-id="b0c6d-123">Specifies an array of names of metrics.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0c6d-124">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="b0c6d-124">-MetricNamespace</span></span>
<span data-ttu-id="b0c6d-125">Specifica lo spazio dei nomi Metric per le definizioni metriche della query.</span><span class="sxs-lookup"><span data-stu-id="b0c6d-125">Specifies the metric namespace to query metric definitions for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0c6d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0c6d-126">-ResourceId</span></span>
<span data-ttu-id="b0c6d-127">Specifica l'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="b0c6d-127">Specifies the resource ID.</span></span>

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

### <span data-ttu-id="b0c6d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0c6d-128">CommonParameters</span></span>
<span data-ttu-id="b0c6d-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0c6d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0c6d-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0c6d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0c6d-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b0c6d-131">INPUTS</span></span>

### <span data-ttu-id="b0c6d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b0c6d-132">System.String</span></span>

### <span data-ttu-id="b0c6d-133">System. String []</span><span class="sxs-lookup"><span data-stu-id="b0c6d-133">System.String[]</span></span>

## <span data-ttu-id="b0c6d-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b0c6d-134">OUTPUTS</span></span>

### <span data-ttu-id="b0c6d-135">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="b0c6d-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDefinition</span></span>

## <span data-ttu-id="b0c6d-136">Note</span><span class="sxs-lookup"><span data-stu-id="b0c6d-136">NOTES</span></span>

<span data-ttu-id="b0c6d-137">Altre informazioni sulle metriche supportate possono essere trovate in: https://docs.microsoft.com/en-us/azure/azure-monitor/platform/metrics-supported</span><span class="sxs-lookup"><span data-stu-id="b0c6d-137">More information about the supported metrics may be found at: https://docs.microsoft.com/en-us/azure/azure-monitor/platform/metrics-supported</span></span>

## <span data-ttu-id="b0c6d-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b0c6d-138">RELATED LINKS</span></span>

<span data-ttu-id="b0c6d-139">[Get-AzMetric](./Get-AzMetric.md) 
 [New-AzMetricFilter](./New-AzMetricFilter.md)</span><span class="sxs-lookup"><span data-stu-id="b0c6d-139">[Get-AzMetric](./Get-AzMetric.md)
[New-AzMetricFilter](./New-AzMetricFilter.md)</span></span>


