---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleRule.md
ms.openlocfilehash: e6f157e199dedf6a7587f607cdd275183ec67c78
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521234"
---
# <span data-ttu-id="c040f-101">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="c040f-101">New-AzureRmAutoscaleRule</span></span>

## <span data-ttu-id="c040f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c040f-102">SYNOPSIS</span></span>
<span data-ttu-id="c040f-103">Crea una regola di scalabilità verticale.</span><span class="sxs-lookup"><span data-stu-id="c040f-103">Creates an Autoscale rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c040f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c040f-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c040f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c040f-105">DESCRIPTION</span></span>
<span data-ttu-id="c040f-106">Il cmdlet **New-AzureRmAutoscaleRule** crea una regola di scalabilità verticale.</span><span class="sxs-lookup"><span data-stu-id="c040f-106">The **New-AzureRmAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="c040f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c040f-107">EXAMPLES</span></span>

### <span data-ttu-id="c040f-108">Esempio 1: creare una regola</span><span class="sxs-lookup"><span data-stu-id="c040f-108">Example 1: Create a rule</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="c040f-109">Questo comando crea una regola.</span><span class="sxs-lookup"><span data-stu-id="c040f-109">This command creates a rule.</span></span>

### <span data-ttu-id="c040f-110">Esempio 2: creare due regole</span><span class="sxs-lookup"><span data-stu-id="c040f-110">Example 2: Create two rules</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="c040f-111">Il primo comando crea una regola per la metrica delle richieste e quindi la archivia nella variabile $Rule 1.</span><span class="sxs-lookup"><span data-stu-id="c040f-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>

<span data-ttu-id="c040f-112">Il secondo comando crea una seconda regola per la metrica richieste e quindi la archivia nella variabile $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="c040f-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

## <span data-ttu-id="c040f-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c040f-113">PARAMETERS</span></span>

### <span data-ttu-id="c040f-114">-Metricname</span><span class="sxs-lookup"><span data-stu-id="c040f-114">-MetricName</span></span>
<span data-ttu-id="c040f-115">Specifica il nome della metrica.</span><span class="sxs-lookup"><span data-stu-id="c040f-115">Specifies the name of the metric.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c040f-116">-MetricResourceId</span><span class="sxs-lookup"><span data-stu-id="c040f-116">-MetricResourceId</span></span>
<span data-ttu-id="c040f-117">Specifica l'ID delle risorse metriche.</span><span class="sxs-lookup"><span data-stu-id="c040f-117">Specifies the metric resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c040f-118">-MetricStatistic</span><span class="sxs-lookup"><span data-stu-id="c040f-118">-MetricStatistic</span></span>
<span data-ttu-id="c040f-119">Specifica la statistica metrica.</span><span class="sxs-lookup"><span data-stu-id="c040f-119">Specifies the metric statistic.</span></span>
<span data-ttu-id="c040f-120">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c040f-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c040f-121">Media</span><span class="sxs-lookup"><span data-stu-id="c040f-121">Average</span></span>
- <span data-ttu-id="c040f-122">Min</span><span class="sxs-lookup"><span data-stu-id="c040f-122">Min</span></span>
- <span data-ttu-id="c040f-123">Max</span><span class="sxs-lookup"><span data-stu-id="c040f-123">Max</span></span>
- <span data-ttu-id="c040f-124">Somma</span><span class="sxs-lookup"><span data-stu-id="c040f-124">Sum</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType
Parameter Sets: (All)
Aliases: 
Accepted values: Average, Min, Max, Sum

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c040f-125">-Operator</span><span class="sxs-lookup"><span data-stu-id="c040f-125">-Operator</span></span>
<span data-ttu-id="c040f-126">Specifica l'operatore.</span><span class="sxs-lookup"><span data-stu-id="c040f-126">Specifies the operator.</span></span>
<span data-ttu-id="c040f-127">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c040f-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c040f-128">È uguale a</span><span class="sxs-lookup"><span data-stu-id="c040f-128">Equals</span></span>
- <span data-ttu-id="c040f-129">NotEquals</span><span class="sxs-lookup"><span data-stu-id="c040f-129">NotEquals</span></span>
- <span data-ttu-id="c040f-130">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="c040f-130">GreaterThan</span></span>
- <span data-ttu-id="c040f-131">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="c040f-131">GreaterThanOrEqual</span></span>
- <span data-ttu-id="c040f-132">LessThan</span><span class="sxs-lookup"><span data-stu-id="c040f-132">LessThan</span></span>
- <span data-ttu-id="c040f-133">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="c040f-133">LessThanOrEqual</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType
Parameter Sets: (All)
Aliases: 
Accepted values: Equals, NotEquals, GreaterThan, GreaterThanOrEqual, LessThan, LessThanOrEqual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c040f-134">-ScaleActionCooldown</span><span class="sxs-lookup"><span data-stu-id="c040f-134">-ScaleActionCooldown</span></span>
<span data-ttu-id="c040f-135">Specifica il tempo di ricarica delle azioni autoscale.</span><span class="sxs-lookup"><span data-stu-id="c040f-135">Specifies the Autoscale action cooldown time.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c040f-136">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="c040f-136">-ScaleActionDirection</span></span>
<span data-ttu-id="c040f-137">Specifica la direzione dell'azione scala.</span><span class="sxs-lookup"><span data-stu-id="c040f-137">Specifies the scale action direction.</span></span>
<span data-ttu-id="c040f-138">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c040f-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c040f-139">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c040f-139">None</span></span>
- <span data-ttu-id="c040f-140">Aumentare</span><span class="sxs-lookup"><span data-stu-id="c040f-140">Increase</span></span>
- <span data-ttu-id="c040f-141">Diminuzione</span><span class="sxs-lookup"><span data-stu-id="c040f-141">Decrease</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection
Parameter Sets: (All)
Aliases: 
Accepted values: None, Increase, Decrease

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c040f-142">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="c040f-142">-ScaleActionScaleType</span></span>
<span data-ttu-id="c040f-143">Specifica il tipo di scala.</span><span class="sxs-lookup"><span data-stu-id="c040f-143">Specifies the scale type.</span></span>
<span data-ttu-id="c040f-144">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c040f-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c040f-145">ChangeSize</span><span class="sxs-lookup"><span data-stu-id="c040f-145">ChangeSize</span></span>
- <span data-ttu-id="c040f-146">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="c040f-146">ChangeCount</span></span>
- <span data-ttu-id="c040f-147">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="c040f-147">PercentChangeCount</span></span>
- <span data-ttu-id="c040f-148">ExactCount</span><span class="sxs-lookup"><span data-stu-id="c040f-148">ExactCount</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.ScaleType
Parameter Sets: (All)
Aliases: 
Accepted values: ChangeCount, PercentChangeCount, ExactCount

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c040f-149">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="c040f-149">-ScaleActionValue</span></span>
<span data-ttu-id="c040f-150">Specifica il valore dell'azione.</span><span class="sxs-lookup"><span data-stu-id="c040f-150">Specifies the action value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c040f-151">-Soglia</span><span class="sxs-lookup"><span data-stu-id="c040f-151">-Threshold</span></span>
<span data-ttu-id="c040f-152">Specifica la soglia del valore metrico.</span><span class="sxs-lookup"><span data-stu-id="c040f-152">Specifies the threshold of the metric value.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c040f-153">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="c040f-153">-TimeAggregationOperator</span></span>
<span data-ttu-id="c040f-154">Specifica l'operatore di aggregazione temporale.</span><span class="sxs-lookup"><span data-stu-id="c040f-154">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="c040f-155">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c040f-155">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c040f-156">Media</span><span class="sxs-lookup"><span data-stu-id="c040f-156">Average</span></span>
- <span data-ttu-id="c040f-157">Minimo</span><span class="sxs-lookup"><span data-stu-id="c040f-157">Minimum</span></span>
- <span data-ttu-id="c040f-158">Massimo</span><span class="sxs-lookup"><span data-stu-id="c040f-158">Maximum</span></span>
- <span data-ttu-id="c040f-159">Ultima</span><span class="sxs-lookup"><span data-stu-id="c040f-159">Last</span></span>
- <span data-ttu-id="c040f-160">Totale, conteggio</span><span class="sxs-lookup"><span data-stu-id="c040f-160">Total, Count</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType
Parameter Sets: (All)
Aliases: 
Accepted values: Average, Minimum, Maximum, Total, Count

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c040f-161">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="c040f-161">-TimeGrain</span></span>
<span data-ttu-id="c040f-162">Specifica la granulosità temporale.</span><span class="sxs-lookup"><span data-stu-id="c040f-162">Specifies the time grain.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c040f-163">-TimeWindow</span><span class="sxs-lookup"><span data-stu-id="c040f-163">-TimeWindow</span></span>
<span data-ttu-id="c040f-164">Specifica la finestra temporale.</span><span class="sxs-lookup"><span data-stu-id="c040f-164">Specifies the time window.</span></span>

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

### <span data-ttu-id="c040f-165">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c040f-165">-DefaultProfile</span></span>
<span data-ttu-id="c040f-166">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c040f-166">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c040f-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c040f-167">CommonParameters</span></span>
<span data-ttu-id="c040f-168">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c040f-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c040f-169">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c040f-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c040f-170">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c040f-170">INPUTS</span></span>

## <span data-ttu-id="c040f-171">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c040f-171">OUTPUTS</span></span>

### <span data-ttu-id="c040f-172">Microsoft. Azure. Management. monitor. Management. Models. ScaleRule</span><span class="sxs-lookup"><span data-stu-id="c040f-172">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="c040f-173">Note</span><span class="sxs-lookup"><span data-stu-id="c040f-173">NOTES</span></span>

## <span data-ttu-id="c040f-174">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c040f-174">RELATED LINKS</span></span>

[<span data-ttu-id="c040f-175">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="c040f-175">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="c040f-176">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="c040f-176">Get-AzureRmAutoscaleHistory</span></span>](./Get-AzureRmAutoscaleHistory.md)

[<span data-ttu-id="c040f-177">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="c040f-177">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="c040f-178">New-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="c040f-178">New-AzureRmAutoscaleProfile</span></span>](./New-AzureRmAutoscaleProfile.md)

[<span data-ttu-id="c040f-179">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="c040f-179">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


