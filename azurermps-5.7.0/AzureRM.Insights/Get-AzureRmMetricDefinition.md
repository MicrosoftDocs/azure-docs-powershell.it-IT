---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7915A7AC-5A47-4868-B846-2896BCEBFAB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermmetricdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetricDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetricDefinition.md
ms.openlocfilehash: de839f4b56f4aa1111e130bdf6396875f9aeb185
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515723"
---
# <span data-ttu-id="574d6-101">Get-AzureRmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="574d6-101">Get-AzureRmMetricDefinition</span></span>

## <span data-ttu-id="574d6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="574d6-102">SYNOPSIS</span></span>
<span data-ttu-id="574d6-103">Ottiene le definizioni metriche.</span><span class="sxs-lookup"><span data-stu-id="574d6-103">Gets metric definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="574d6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="574d6-104">SYNTAX</span></span>

```
Get-AzureRmMetricDefinition [-ResourceId] <String> [-MetricName <String[]>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="574d6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="574d6-105">DESCRIPTION</span></span>
<span data-ttu-id="574d6-106">Il cmdlet **Get-AzureRmMetricDefinition** ottiene le definizioni metriche.</span><span class="sxs-lookup"><span data-stu-id="574d6-106">The **Get-AzureRmMetricDefinition** cmdlet gets metric definitions.</span></span>

## <span data-ttu-id="574d6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="574d6-107">EXAMPLES</span></span>

### <span data-ttu-id="574d6-108">Esempio 1: ottenere definizioni metriche per una risorsa</span><span class="sxs-lookup"><span data-stu-id="574d6-108">Example 1: Get metric definitions for a resource</span></span>
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

<span data-ttu-id="574d6-109">Questo comando consente di ottenere le definizioni metriche per la risorsa specificata.</span><span class="sxs-lookup"><span data-stu-id="574d6-109">This command gets the metrics definitions for the specified resource.</span></span>

### <span data-ttu-id="574d6-110">Esempio 2: ottenere definizioni metriche con l'output dettagliato</span><span class="sxs-lookup"><span data-stu-id="574d6-110">Example 2: Get metric definitions with detailed output</span></span>
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

<span data-ttu-id="574d6-111">Questo comando ottiene le definizioni metriche per WebSite2.</span><span class="sxs-lookup"><span data-stu-id="574d6-111">This command gets the metric definitions for website2.</span></span>
<span data-ttu-id="574d6-112">L'output è dettagliato.</span><span class="sxs-lookup"><span data-stu-id="574d6-112">The output is detailed.</span></span>

### <span data-ttu-id="574d6-113">Esempio 3: ottenere le definizioni metriche per nome</span><span class="sxs-lookup"><span data-stu-id="574d6-113">Example 3: Get metric definitions by name</span></span>
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

<span data-ttu-id="574d6-114">Questo comando ottiene le definizioni per le metriche BytesSent e CpuTime.</span><span class="sxs-lookup"><span data-stu-id="574d6-114">This command gets definitions for the BytesSent and CpuTime metrics.</span></span>
<span data-ttu-id="574d6-115">L'output è dettagliato.</span><span class="sxs-lookup"><span data-stu-id="574d6-115">The output is detailed.</span></span>

## <span data-ttu-id="574d6-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="574d6-116">PARAMETERS</span></span>

### <span data-ttu-id="574d6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="574d6-117">-DefaultProfile</span></span>
<span data-ttu-id="574d6-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="574d6-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="574d6-119">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="574d6-119">-DetailedOutput</span></span>
<span data-ttu-id="574d6-120">Indica che questa operazione include l'output dettagliato.</span><span class="sxs-lookup"><span data-stu-id="574d6-120">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="574d6-121">Se non specifichi questo parametro, l'output viene riepilogato.</span><span class="sxs-lookup"><span data-stu-id="574d6-121">If you do not specify this parameter, the output is summarized.</span></span>

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

### <span data-ttu-id="574d6-122">-Metricname</span><span class="sxs-lookup"><span data-stu-id="574d6-122">-MetricName</span></span>
<span data-ttu-id="574d6-123">Specifica una matrice di nomi di metriche.</span><span class="sxs-lookup"><span data-stu-id="574d6-123">Specifies an array of names of metrics.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: MetricNames

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="574d6-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="574d6-124">-ResourceId</span></span>
<span data-ttu-id="574d6-125">Specifica l'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="574d6-125">Specifies the resource ID.</span></span>

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

### <span data-ttu-id="574d6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="574d6-126">CommonParameters</span></span>
<span data-ttu-id="574d6-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="574d6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="574d6-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="574d6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="574d6-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="574d6-129">INPUTS</span></span>

### <span data-ttu-id="574d6-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="574d6-130">None</span></span>
<span data-ttu-id="574d6-131">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="574d6-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="574d6-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="574d6-132">OUTPUTS</span></span>

### <span data-ttu-id="574d6-133">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricDefinition []</span><span class="sxs-lookup"><span data-stu-id="574d6-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDefinition[]</span></span>

## <span data-ttu-id="574d6-134">Note</span><span class="sxs-lookup"><span data-stu-id="574d6-134">NOTES</span></span>

## <span data-ttu-id="574d6-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="574d6-135">RELATED LINKS</span></span>

[<span data-ttu-id="574d6-136">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="574d6-136">Get-AzureRmMetric</span></span>](./Get-AzureRmMetric.md)


