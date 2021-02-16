---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7915A7AC-5A47-4868-B846-2896BCEBFAB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azmetricdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricDefinition.md
ms.openlocfilehash: 9ca873736ad86eaac17dd2795ad61716197ceaba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184967"
---
# <span data-ttu-id="fade5-101">Get-AzMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="fade5-101">Get-AzMetricDefinition</span></span>

## <span data-ttu-id="fade5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fade5-102">SYNOPSIS</span></span>
<span data-ttu-id="fade5-103">Ottiene le definizioni della metrica.</span><span class="sxs-lookup"><span data-stu-id="fade5-103">Gets metric definitions.</span></span>

## <span data-ttu-id="fade5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fade5-104">SYNTAX</span></span>

```
Get-AzMetricDefinition [-ResourceId] <String> [-MetricName <String[]>] [-MetricNamespace <String>]
 [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fade5-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fade5-105">DESCRIPTION</span></span>
<span data-ttu-id="fade5-106">Il cmdlet **Get-AzMetricDefinition** ottiene le definizioni della metrica.</span><span class="sxs-lookup"><span data-stu-id="fade5-106">The **Get-AzMetricDefinition** cmdlet gets metric definitions.</span></span>

## <span data-ttu-id="fade5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fade5-107">EXAMPLES</span></span>

### <span data-ttu-id="fade5-108">Esempio 1: Ottenere le definizioni metriche per una risorsa</span><span class="sxs-lookup"><span data-stu-id="fade5-108">Example 1: Get metric definitions for a resource</span></span>
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

<span data-ttu-id="fade5-109">Questo comando recupera le definizioni delle metriche per la risorsa specificata.</span><span class="sxs-lookup"><span data-stu-id="fade5-109">This command gets the metrics definitions for the specified resource.</span></span>

### <span data-ttu-id="fade5-110">Esempio 2: Ottenere le definizioni della metrica con output dettagliato</span><span class="sxs-lookup"><span data-stu-id="fade5-110">Example 2: Get metric definitions with detailed output</span></span>
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

<span data-ttu-id="fade5-111">Questo comando ottiene le definizioni metriche per sito Web2.</span><span class="sxs-lookup"><span data-stu-id="fade5-111">This command gets the metric definitions for website2.</span></span>
<span data-ttu-id="fade5-112">L'output è dettagliato.</span><span class="sxs-lookup"><span data-stu-id="fade5-112">The output is detailed.</span></span>

### <span data-ttu-id="fade5-113">Esempio 3: Ottenere le definizioni delle metriche in base al nome</span><span class="sxs-lookup"><span data-stu-id="fade5-113">Example 3: Get metric definitions by name</span></span>
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

<span data-ttu-id="fade5-114">Questo comando recupera le definizioni per le metriche ByteSent e CpuTime.</span><span class="sxs-lookup"><span data-stu-id="fade5-114">This command gets definitions for the BytesSent and CpuTime metrics.</span></span>
<span data-ttu-id="fade5-115">L'output è dettagliato.</span><span class="sxs-lookup"><span data-stu-id="fade5-115">The output is detailed.</span></span>

## <span data-ttu-id="fade5-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fade5-116">PARAMETERS</span></span>

### <span data-ttu-id="fade5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fade5-117">-DefaultProfile</span></span>
<span data-ttu-id="fade5-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="fade5-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fade5-119">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="fade5-119">-DetailedOutput</span></span>
<span data-ttu-id="fade5-120">Indica che questa operazione includeva un output dettagliato.</span><span class="sxs-lookup"><span data-stu-id="fade5-120">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="fade5-121">Se non si specifica questo parametro, l'output viene riepilogato.</span><span class="sxs-lookup"><span data-stu-id="fade5-121">If you do not specify this parameter, the output is summarized.</span></span>

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

### <span data-ttu-id="fade5-122">-MetricName</span><span class="sxs-lookup"><span data-stu-id="fade5-122">-MetricName</span></span>
<span data-ttu-id="fade5-123">Specifica una matrice di nomi di metriche.</span><span class="sxs-lookup"><span data-stu-id="fade5-123">Specifies an array of names of metrics.</span></span>

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

### <span data-ttu-id="fade5-124">-MetricMetricMetric</span><span class="sxs-lookup"><span data-stu-id="fade5-124">-MetricNamespace</span></span>
<span data-ttu-id="fade5-125">Specifica lo spazio dei nomi metrico di cui eseguire query per le definizioni della metrica.</span><span class="sxs-lookup"><span data-stu-id="fade5-125">Specifies the metric namespace to query metric definitions for.</span></span>

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

### <span data-ttu-id="fade5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fade5-126">-ResourceId</span></span>
<span data-ttu-id="fade5-127">Specifica l'ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="fade5-127">Specifies the resource ID.</span></span>

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

### <span data-ttu-id="fade5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fade5-128">CommonParameters</span></span>
<span data-ttu-id="fade5-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fade5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fade5-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fade5-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fade5-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="fade5-131">INPUTS</span></span>

### <span data-ttu-id="fade5-132">System.String</span><span class="sxs-lookup"><span data-stu-id="fade5-132">System.String</span></span>

### <span data-ttu-id="fade5-133">System.String[]</span><span class="sxs-lookup"><span data-stu-id="fade5-133">System.String[]</span></span>

## <span data-ttu-id="fade5-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fade5-134">OUTPUTS</span></span>

### <span data-ttu-id="fade5-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="fade5-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDefinition</span></span>

## <span data-ttu-id="fade5-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="fade5-136">NOTES</span></span>

<span data-ttu-id="fade5-137">Altre informazioni sulle metriche supportate sono disponibili all'indirizzo: https://docs.microsoft.com/en-us/azure/azure-monitor/platform/metrics-supported</span><span class="sxs-lookup"><span data-stu-id="fade5-137">More information about the supported metrics may be found at: https://docs.microsoft.com/en-us/azure/azure-monitor/platform/metrics-supported</span></span>

## <span data-ttu-id="fade5-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fade5-138">RELATED LINKS</span></span>

<span data-ttu-id="fade5-139">[Get-AzMetric](./Get-AzMetric.md) 
 [New-AzMetricFilter](./New-AzMetricFilter.md)</span><span class="sxs-lookup"><span data-stu-id="fade5-139">[Get-AzMetric](./Get-AzMetric.md)
[New-AzMetricFilter](./New-AzMetricFilter.md)</span></span>


