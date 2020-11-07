---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalerule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
ms.openlocfilehash: 2464a3b7fb35cce28dd06884cd8ed69e5197eced
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835032"
---
# <span data-ttu-id="94235-101">New-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="94235-101">New-AzAutoscaleRule</span></span>

## <span data-ttu-id="94235-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="94235-102">SYNOPSIS</span></span>
<span data-ttu-id="94235-103">Crea una regola di scalabilità verticale.</span><span class="sxs-lookup"><span data-stu-id="94235-103">Creates an Autoscale rule.</span></span>

## <span data-ttu-id="94235-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="94235-104">SYNTAX</span></span>

```
New-AzAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94235-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="94235-105">DESCRIPTION</span></span>
<span data-ttu-id="94235-106">Il cmdlet **New-AzAutoscaleRule** crea una regola di scalabilità verticale.</span><span class="sxs-lookup"><span data-stu-id="94235-106">The **New-AzAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="94235-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="94235-107">EXAMPLES</span></span>

### <span data-ttu-id="94235-108">Esempio 1: creare una regola</span><span class="sxs-lookup"><span data-stu-id="94235-108">Example 1: Create a rule</span></span>
```
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="94235-109">Questo comando crea una regola.</span><span class="sxs-lookup"><span data-stu-id="94235-109">This command creates a rule.</span></span>

### <span data-ttu-id="94235-110">Esempio 2: creare due regole</span><span class="sxs-lookup"><span data-stu-id="94235-110">Example 2: Create two rules</span></span>
```
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="94235-111">Il primo comando crea una regola per la metrica delle richieste e quindi la archivia nella variabile $Rule 1.</span><span class="sxs-lookup"><span data-stu-id="94235-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>
<span data-ttu-id="94235-112">Il secondo comando crea una seconda regola per la metrica richieste e quindi la archivia nella variabile $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="94235-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

## <span data-ttu-id="94235-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="94235-113">PARAMETERS</span></span>

### <span data-ttu-id="94235-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94235-114">-DefaultProfile</span></span>
<span data-ttu-id="94235-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="94235-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94235-116">-Metricname</span><span class="sxs-lookup"><span data-stu-id="94235-116">-MetricName</span></span>
<span data-ttu-id="94235-117">Specifica il nome della metrica.</span><span class="sxs-lookup"><span data-stu-id="94235-117">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="94235-118">-MetricResourceId</span><span class="sxs-lookup"><span data-stu-id="94235-118">-MetricResourceId</span></span>
<span data-ttu-id="94235-119">Specifica l'ID delle risorse metriche.</span><span class="sxs-lookup"><span data-stu-id="94235-119">Specifies the metric resource ID.</span></span>

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

### <span data-ttu-id="94235-120">-MetricStatistic</span><span class="sxs-lookup"><span data-stu-id="94235-120">-MetricStatistic</span></span>
<span data-ttu-id="94235-121">Specifica la statistica metrica.</span><span class="sxs-lookup"><span data-stu-id="94235-121">Specifies the metric statistic.</span></span>
<span data-ttu-id="94235-122">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="94235-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="94235-123">Media</span><span class="sxs-lookup"><span data-stu-id="94235-123">Average</span></span>
- <span data-ttu-id="94235-124">Min</span><span class="sxs-lookup"><span data-stu-id="94235-124">Min</span></span>
- <span data-ttu-id="94235-125">Max</span><span class="sxs-lookup"><span data-stu-id="94235-125">Max</span></span>
- <span data-ttu-id="94235-126">Somma</span><span class="sxs-lookup"><span data-stu-id="94235-126">Sum</span></span>

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

### <span data-ttu-id="94235-127">-Operator</span><span class="sxs-lookup"><span data-stu-id="94235-127">-Operator</span></span>
<span data-ttu-id="94235-128">Specifica l'operatore.</span><span class="sxs-lookup"><span data-stu-id="94235-128">Specifies the operator.</span></span>
<span data-ttu-id="94235-129">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="94235-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="94235-130">È uguale a</span><span class="sxs-lookup"><span data-stu-id="94235-130">Equals</span></span>
- <span data-ttu-id="94235-131">NotEquals</span><span class="sxs-lookup"><span data-stu-id="94235-131">NotEquals</span></span>
- <span data-ttu-id="94235-132">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="94235-132">GreaterThan</span></span>
- <span data-ttu-id="94235-133">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="94235-133">GreaterThanOrEqual</span></span>
- <span data-ttu-id="94235-134">LessThan</span><span class="sxs-lookup"><span data-stu-id="94235-134">LessThan</span></span>
- <span data-ttu-id="94235-135">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="94235-135">LessThanOrEqual</span></span>

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

### <span data-ttu-id="94235-136">-ScaleActionCooldown</span><span class="sxs-lookup"><span data-stu-id="94235-136">-ScaleActionCooldown</span></span>
<span data-ttu-id="94235-137">Specifica il tempo di ricarica delle azioni autoscale.</span><span class="sxs-lookup"><span data-stu-id="94235-137">Specifies the Autoscale action cooldown time.</span></span>

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

### <span data-ttu-id="94235-138">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="94235-138">-ScaleActionDirection</span></span>
<span data-ttu-id="94235-139">Specifica la direzione dell'azione scala.</span><span class="sxs-lookup"><span data-stu-id="94235-139">Specifies the scale action direction.</span></span>
<span data-ttu-id="94235-140">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="94235-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="94235-141">Nessuno</span><span class="sxs-lookup"><span data-stu-id="94235-141">None</span></span>
- <span data-ttu-id="94235-142">Aumentare</span><span class="sxs-lookup"><span data-stu-id="94235-142">Increase</span></span>
- <span data-ttu-id="94235-143">Diminuzione</span><span class="sxs-lookup"><span data-stu-id="94235-143">Decrease</span></span>

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

### <span data-ttu-id="94235-144">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="94235-144">-ScaleActionScaleType</span></span>
<span data-ttu-id="94235-145">Specifica il tipo di scala.</span><span class="sxs-lookup"><span data-stu-id="94235-145">Specifies the scale type.</span></span>
<span data-ttu-id="94235-146">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="94235-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="94235-147">ChangeSize</span><span class="sxs-lookup"><span data-stu-id="94235-147">ChangeSize</span></span>
- <span data-ttu-id="94235-148">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="94235-148">ChangeCount</span></span>
- <span data-ttu-id="94235-149">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="94235-149">PercentChangeCount</span></span>
- <span data-ttu-id="94235-150">ExactCount</span><span class="sxs-lookup"><span data-stu-id="94235-150">ExactCount</span></span>

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

### <span data-ttu-id="94235-151">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="94235-151">-ScaleActionValue</span></span>
<span data-ttu-id="94235-152">Specifica il valore dell'azione.</span><span class="sxs-lookup"><span data-stu-id="94235-152">Specifies the action value.</span></span>

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

### <span data-ttu-id="94235-153">-Soglia</span><span class="sxs-lookup"><span data-stu-id="94235-153">-Threshold</span></span>
<span data-ttu-id="94235-154">Specifica la soglia del valore metrico.</span><span class="sxs-lookup"><span data-stu-id="94235-154">Specifies the threshold of the metric value.</span></span>

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

### <span data-ttu-id="94235-155">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="94235-155">-TimeAggregationOperator</span></span>
<span data-ttu-id="94235-156">Specifica l'operatore di aggregazione temporale.</span><span class="sxs-lookup"><span data-stu-id="94235-156">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="94235-157">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="94235-157">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="94235-158">Media</span><span class="sxs-lookup"><span data-stu-id="94235-158">Average</span></span>
- <span data-ttu-id="94235-159">Minimo</span><span class="sxs-lookup"><span data-stu-id="94235-159">Minimum</span></span>
- <span data-ttu-id="94235-160">Massimo</span><span class="sxs-lookup"><span data-stu-id="94235-160">Maximum</span></span>
- <span data-ttu-id="94235-161">Ultima</span><span class="sxs-lookup"><span data-stu-id="94235-161">Last</span></span>
- <span data-ttu-id="94235-162">Totale, conteggio</span><span class="sxs-lookup"><span data-stu-id="94235-162">Total, Count</span></span>

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

### <span data-ttu-id="94235-163">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="94235-163">-TimeGrain</span></span>
<span data-ttu-id="94235-164">Specifica la granulosità temporale.</span><span class="sxs-lookup"><span data-stu-id="94235-164">Specifies the time grain.</span></span>

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

### <span data-ttu-id="94235-165">-TimeWindow</span><span class="sxs-lookup"><span data-stu-id="94235-165">-TimeWindow</span></span>
<span data-ttu-id="94235-166">Specifica la finestra temporale.</span><span class="sxs-lookup"><span data-stu-id="94235-166">Specifies the time window.</span></span>

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

### <span data-ttu-id="94235-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94235-167">CommonParameters</span></span>
<span data-ttu-id="94235-168">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94235-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94235-169">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94235-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94235-170">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="94235-170">INPUTS</span></span>

### <span data-ttu-id="94235-171">System. String</span><span class="sxs-lookup"><span data-stu-id="94235-171">System.String</span></span>

### <span data-ttu-id="94235-172">Microsoft. Azure. Management. monitor. Management. Models. ComparisonOperationType</span><span class="sxs-lookup"><span data-stu-id="94235-172">Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType</span></span>

### <span data-ttu-id="94235-173">Microsoft. Azure. Management. monitor. Management. Models. MetricStatisticType</span><span class="sxs-lookup"><span data-stu-id="94235-173">Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType</span></span>

### <span data-ttu-id="94235-174">System. Double</span><span class="sxs-lookup"><span data-stu-id="94235-174">System.Double</span></span>

### <span data-ttu-id="94235-175">Microsoft. Azure. Management. monitor. Management. Models. TimeAggregationType</span><span class="sxs-lookup"><span data-stu-id="94235-175">Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType</span></span>

### <span data-ttu-id="94235-176">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="94235-176">System.TimeSpan</span></span>

### <span data-ttu-id="94235-177">Microsoft. Azure. Management. monitor. Management. Models. ScaleDirection</span><span class="sxs-lookup"><span data-stu-id="94235-177">Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection</span></span>

### <span data-ttu-id="94235-178">Microsoft. Azure. Management. monitor. Management. Models. ScaleType</span><span class="sxs-lookup"><span data-stu-id="94235-178">Microsoft.Azure.Management.Monitor.Management.Models.ScaleType</span></span>

## <span data-ttu-id="94235-179">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="94235-179">OUTPUTS</span></span>

### <span data-ttu-id="94235-180">Microsoft. Azure. Management. monitor. Management. Models. ScaleRule</span><span class="sxs-lookup"><span data-stu-id="94235-180">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="94235-181">Note</span><span class="sxs-lookup"><span data-stu-id="94235-181">NOTES</span></span>

## <span data-ttu-id="94235-182">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="94235-182">RELATED LINKS</span></span>

[<span data-ttu-id="94235-183">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="94235-183">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="94235-184">Get-AzAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="94235-184">Get-AzAutoscaleHistory</span></span>](./Get-AzAutoscaleHistory.md)

[<span data-ttu-id="94235-185">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="94235-185">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="94235-186">New-AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="94235-186">New-AzAutoscaleProfile</span></span>](./New-AzAutoscaleProfile.md)

[<span data-ttu-id="94235-187">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="94235-187">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


