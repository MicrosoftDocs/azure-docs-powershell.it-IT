---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7915A7AC-5A47-4868-B846-2896BCEBFAB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermmetricdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetricDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetricDefinition.md
ms.openlocfilehash: 8dea2e61d6d64fbb59363d157dc0b8c1096ba259
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686184"
---
# <span data-ttu-id="5ac48-101">Get-AzureRmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="5ac48-101">Get-AzureRmMetricDefinition</span></span>

## <span data-ttu-id="5ac48-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5ac48-102">SYNOPSIS</span></span>
<span data-ttu-id="5ac48-103">Ottiene le definizioni metriche.</span><span class="sxs-lookup"><span data-stu-id="5ac48-103">Gets metric definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ac48-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5ac48-104">SYNTAX</span></span>

```
Get-AzureRmMetricDefinition [-ResourceId] <String> [-MetricName <String[]>] [-MetricNamespace <String>]
 [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ac48-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ac48-105">DESCRIPTION</span></span>
<span data-ttu-id="5ac48-106">Il cmdlet **Get-AzureRmMetricDefinition** ottiene le definizioni metriche.</span><span class="sxs-lookup"><span data-stu-id="5ac48-106">The **Get-AzureRmMetricDefinition** cmdlet gets metric definitions.</span></span>

## <span data-ttu-id="5ac48-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5ac48-107">EXAMPLES</span></span>

### <span data-ttu-id="5ac48-108">Esempio 1: ottenere definizioni metriche per una risorsa</span><span class="sxs-lookup"><span data-stu-id="5ac48-108">Example 1: Get metric definitions for a resource</span></span>
```
PS C:\>Get-AzureRmMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2"
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

<span data-ttu-id="5ac48-109">Questo comando consente di ottenere le definizioni metriche per la risorsa specificata.</span><span class="sxs-lookup"><span data-stu-id="5ac48-109">This command gets the metrics definitions for the specified resource.</span></span>

### <span data-ttu-id="5ac48-110">Esempio 2: ottenere definizioni metriche con l'output dettagliato</span><span class="sxs-lookup"><span data-stu-id="5ac48-110">Example 2: Get metric definitions with detailed output</span></span>
```
PS C:\>Get-AzureRmMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2" -DetailedOutput
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

<span data-ttu-id="5ac48-111">Questo comando ottiene le definizioni metriche per WebSite2.</span><span class="sxs-lookup"><span data-stu-id="5ac48-111">This command gets the metric definitions for website2.</span></span>
<span data-ttu-id="5ac48-112">L'output è dettagliato.</span><span class="sxs-lookup"><span data-stu-id="5ac48-112">The output is detailed.</span></span>

### <span data-ttu-id="5ac48-113">Esempio 3: ottenere le definizioni metriche per nome</span><span class="sxs-lookup"><span data-stu-id="5ac48-113">Example 3: Get metric definitions by name</span></span>
```
PS C:\>Get-AzureRmMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2" -DetailedOutput -MetricNames "BytesSent,CpuTime"
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

<span data-ttu-id="5ac48-114">Questo comando ottiene le definizioni per le metriche BytesSent e CpuTime.</span><span class="sxs-lookup"><span data-stu-id="5ac48-114">This command gets definitions for the BytesSent and CpuTime metrics.</span></span>
<span data-ttu-id="5ac48-115">L'output è dettagliato.</span><span class="sxs-lookup"><span data-stu-id="5ac48-115">The output is detailed.</span></span>

## <span data-ttu-id="5ac48-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5ac48-116">PARAMETERS</span></span>

### <span data-ttu-id="5ac48-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ac48-117">-DefaultProfile</span></span>
<span data-ttu-id="5ac48-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5ac48-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ac48-119">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="5ac48-119">-DetailedOutput</span></span>
<span data-ttu-id="5ac48-120">Indica che questa operazione include l'output dettagliato.</span><span class="sxs-lookup"><span data-stu-id="5ac48-120">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="5ac48-121">Se non specifichi questo parametro, l'output viene riepilogato.</span><span class="sxs-lookup"><span data-stu-id="5ac48-121">If you do not specify this parameter, the output is summarized.</span></span>

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

### <span data-ttu-id="5ac48-122">-Metricname</span><span class="sxs-lookup"><span data-stu-id="5ac48-122">-MetricName</span></span>
<span data-ttu-id="5ac48-123">Specifica una matrice di nomi di metriche.</span><span class="sxs-lookup"><span data-stu-id="5ac48-123">Specifies an array of names of metrics.</span></span>

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

### <span data-ttu-id="5ac48-124">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="5ac48-124">-MetricNamespace</span></span>
<span data-ttu-id="5ac48-125">Specifica lo spazio dei nomi Metric per le definizioni metriche della query.</span><span class="sxs-lookup"><span data-stu-id="5ac48-125">Specifies the metric namespace to query metric definitions for.</span></span>

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

### <span data-ttu-id="5ac48-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ac48-126">-ResourceId</span></span>
<span data-ttu-id="5ac48-127">Specifica l'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="5ac48-127">Specifies the resource ID.</span></span>

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

### <span data-ttu-id="5ac48-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ac48-128">CommonParameters</span></span>
<span data-ttu-id="5ac48-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ac48-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ac48-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ac48-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ac48-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5ac48-131">INPUTS</span></span>

### <span data-ttu-id="5ac48-132">System. String</span><span class="sxs-lookup"><span data-stu-id="5ac48-132">System.String</span></span>

### <span data-ttu-id="5ac48-133">System. String []</span><span class="sxs-lookup"><span data-stu-id="5ac48-133">System.String[]</span></span>

## <span data-ttu-id="5ac48-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5ac48-134">OUTPUTS</span></span>

### <span data-ttu-id="5ac48-135">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="5ac48-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDefinition</span></span>

## <span data-ttu-id="5ac48-136">Note</span><span class="sxs-lookup"><span data-stu-id="5ac48-136">NOTES</span></span>

## <span data-ttu-id="5ac48-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5ac48-137">RELATED LINKS</span></span>

<span data-ttu-id="5ac48-138">[Get-AzureRmMetric](./Get-AzureRmMetric.md) 
 [New-AzureRmMetricFilter](./New-AzureRmMetricFilter.md)</span><span class="sxs-lookup"><span data-stu-id="5ac48-138">[Get-AzureRmMetric](./Get-AzureRmMetric.md)
[New-AzureRmMetricFilter](./New-AzureRmMetricFilter.md)</span></span>


