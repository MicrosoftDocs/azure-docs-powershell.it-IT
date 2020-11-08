---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalerule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
ms.openlocfilehash: cd4e374909fa58f036a0f67cd7a89bb968defd71
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192389"
---
# <span data-ttu-id="37353-101">New-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="37353-101">New-AzAutoscaleRule</span></span>

## <span data-ttu-id="37353-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="37353-102">SYNOPSIS</span></span>
<span data-ttu-id="37353-103">Crea una regola di scalabilità verticale.</span><span class="sxs-lookup"><span data-stu-id="37353-103">Creates an Autoscale rule.</span></span>

## <span data-ttu-id="37353-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="37353-104">SYNTAX</span></span>

```
New-AzAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37353-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="37353-105">DESCRIPTION</span></span>
<span data-ttu-id="37353-106">Il cmdlet **New-AzAutoscaleRule** crea una regola di scalabilità verticale.</span><span class="sxs-lookup"><span data-stu-id="37353-106">The **New-AzAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="37353-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="37353-107">EXAMPLES</span></span>

### <span data-ttu-id="37353-108">Esempio 1: creare una regola</span><span class="sxs-lookup"><span data-stu-id="37353-108">Example 1: Create a rule</span></span>
```powershell
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="37353-109">Questo comando crea una regola.</span><span class="sxs-lookup"><span data-stu-id="37353-109">This command creates a rule.</span></span>

### <span data-ttu-id="37353-110">Esempio 2: creare due regole</span><span class="sxs-lookup"><span data-stu-id="37353-110">Example 2: Create two rules</span></span>
```powershell
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="37353-111">Il primo comando crea una regola per la metrica delle richieste e quindi la archivia nella variabile $Rule 1.</span><span class="sxs-lookup"><span data-stu-id="37353-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>
<span data-ttu-id="37353-112">Il secondo comando crea una seconda regola per la metrica richieste e quindi la archivia nella variabile $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="37353-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

### <span data-ttu-id="37353-113">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="37353-113">Example 3</span></span>

<span data-ttu-id="37353-114">Crea una regola di scalabilità verticale.</span><span class="sxs-lookup"><span data-stu-id="37353-114">Creates an Autoscale rule.</span></span> <span data-ttu-id="37353-115">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="37353-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzAutoscaleRule -MetricName 'Requests' -MetricResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite' -MetricStatistic Average -Operator Equals -ScaleActionCooldown 00:05:00 -ScaleActionDirection None -ScaleActionScaleType ChangeCount -ScaleActionValue '1' -Threshold 10 -TimeGrain 00:01:00 -TimeWindow <TimeSpan>
```

## <span data-ttu-id="37353-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="37353-116">PARAMETERS</span></span>

### <span data-ttu-id="37353-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37353-117">-DefaultProfile</span></span>
<span data-ttu-id="37353-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="37353-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37353-119">-Metricname</span><span class="sxs-lookup"><span data-stu-id="37353-119">-MetricName</span></span>
<span data-ttu-id="37353-120">Specifica il nome della metrica.</span><span class="sxs-lookup"><span data-stu-id="37353-120">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="37353-121">-MetricResourceId</span><span class="sxs-lookup"><span data-stu-id="37353-121">-MetricResourceId</span></span>
<span data-ttu-id="37353-122">Specifica l'ID delle risorse metriche.</span><span class="sxs-lookup"><span data-stu-id="37353-122">Specifies the metric resource ID.</span></span>

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

### <span data-ttu-id="37353-123">-MetricStatistic</span><span class="sxs-lookup"><span data-stu-id="37353-123">-MetricStatistic</span></span>
<span data-ttu-id="37353-124">Specifica la statistica metrica.</span><span class="sxs-lookup"><span data-stu-id="37353-124">Specifies the metric statistic.</span></span>
<span data-ttu-id="37353-125">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="37353-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="37353-126">Media</span><span class="sxs-lookup"><span data-stu-id="37353-126">Average</span></span>
- <span data-ttu-id="37353-127">Min</span><span class="sxs-lookup"><span data-stu-id="37353-127">Min</span></span>
- <span data-ttu-id="37353-128">Max</span><span class="sxs-lookup"><span data-stu-id="37353-128">Max</span></span>
- <span data-ttu-id="37353-129">Somma</span><span class="sxs-lookup"><span data-stu-id="37353-129">Sum</span></span>

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

### <span data-ttu-id="37353-130">-Operator</span><span class="sxs-lookup"><span data-stu-id="37353-130">-Operator</span></span>
<span data-ttu-id="37353-131">Specifica l'operatore.</span><span class="sxs-lookup"><span data-stu-id="37353-131">Specifies the operator.</span></span>
<span data-ttu-id="37353-132">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="37353-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="37353-133">È uguale a</span><span class="sxs-lookup"><span data-stu-id="37353-133">Equals</span></span>
- <span data-ttu-id="37353-134">NotEquals</span><span class="sxs-lookup"><span data-stu-id="37353-134">NotEquals</span></span>
- <span data-ttu-id="37353-135">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="37353-135">GreaterThan</span></span>
- <span data-ttu-id="37353-136">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="37353-136">GreaterThanOrEqual</span></span>
- <span data-ttu-id="37353-137">LessThan</span><span class="sxs-lookup"><span data-stu-id="37353-137">LessThan</span></span>
- <span data-ttu-id="37353-138">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="37353-138">LessThanOrEqual</span></span>

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

### <span data-ttu-id="37353-139">-ScaleActionCooldown</span><span class="sxs-lookup"><span data-stu-id="37353-139">-ScaleActionCooldown</span></span>
<span data-ttu-id="37353-140">Specifica il tempo di ricarica delle azioni autoscale.</span><span class="sxs-lookup"><span data-stu-id="37353-140">Specifies the Autoscale action cooldown time.</span></span>

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

### <span data-ttu-id="37353-141">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="37353-141">-ScaleActionDirection</span></span>
<span data-ttu-id="37353-142">Specifica la direzione dell'azione scala.</span><span class="sxs-lookup"><span data-stu-id="37353-142">Specifies the scale action direction.</span></span>
<span data-ttu-id="37353-143">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="37353-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="37353-144">Nessuno</span><span class="sxs-lookup"><span data-stu-id="37353-144">None</span></span>
- <span data-ttu-id="37353-145">Aumentare</span><span class="sxs-lookup"><span data-stu-id="37353-145">Increase</span></span>
- <span data-ttu-id="37353-146">Diminuzione</span><span class="sxs-lookup"><span data-stu-id="37353-146">Decrease</span></span>

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

### <span data-ttu-id="37353-147">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="37353-147">-ScaleActionScaleType</span></span>
<span data-ttu-id="37353-148">Specifica il tipo di scala.</span><span class="sxs-lookup"><span data-stu-id="37353-148">Specifies the scale type.</span></span>
<span data-ttu-id="37353-149">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="37353-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="37353-150">ChangeSize</span><span class="sxs-lookup"><span data-stu-id="37353-150">ChangeSize</span></span>
- <span data-ttu-id="37353-151">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="37353-151">ChangeCount</span></span>
- <span data-ttu-id="37353-152">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="37353-152">PercentChangeCount</span></span>
- <span data-ttu-id="37353-153">ExactCount</span><span class="sxs-lookup"><span data-stu-id="37353-153">ExactCount</span></span>

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

### <span data-ttu-id="37353-154">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="37353-154">-ScaleActionValue</span></span>
<span data-ttu-id="37353-155">Specifica il valore dell'azione.</span><span class="sxs-lookup"><span data-stu-id="37353-155">Specifies the action value.</span></span>

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

### <span data-ttu-id="37353-156">-Soglia</span><span class="sxs-lookup"><span data-stu-id="37353-156">-Threshold</span></span>
<span data-ttu-id="37353-157">Specifica la soglia del valore metrico.</span><span class="sxs-lookup"><span data-stu-id="37353-157">Specifies the threshold of the metric value.</span></span>

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

### <span data-ttu-id="37353-158">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="37353-158">-TimeAggregationOperator</span></span>
<span data-ttu-id="37353-159">Specifica l'operatore di aggregazione temporale.</span><span class="sxs-lookup"><span data-stu-id="37353-159">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="37353-160">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="37353-160">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="37353-161">Media</span><span class="sxs-lookup"><span data-stu-id="37353-161">Average</span></span>
- <span data-ttu-id="37353-162">Minimo</span><span class="sxs-lookup"><span data-stu-id="37353-162">Minimum</span></span>
- <span data-ttu-id="37353-163">Massimo</span><span class="sxs-lookup"><span data-stu-id="37353-163">Maximum</span></span>
- <span data-ttu-id="37353-164">Ultima</span><span class="sxs-lookup"><span data-stu-id="37353-164">Last</span></span>
- <span data-ttu-id="37353-165">Totale, conteggio</span><span class="sxs-lookup"><span data-stu-id="37353-165">Total, Count</span></span>

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

### <span data-ttu-id="37353-166">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="37353-166">-TimeGrain</span></span>
<span data-ttu-id="37353-167">Specifica la granulosità temporale.</span><span class="sxs-lookup"><span data-stu-id="37353-167">Specifies the time grain.</span></span>

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

### <span data-ttu-id="37353-168">-TimeWindow</span><span class="sxs-lookup"><span data-stu-id="37353-168">-TimeWindow</span></span>
<span data-ttu-id="37353-169">Specifica la finestra temporale.</span><span class="sxs-lookup"><span data-stu-id="37353-169">Specifies the time window.</span></span>

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

### <span data-ttu-id="37353-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37353-170">CommonParameters</span></span>
<span data-ttu-id="37353-171">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37353-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37353-172">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37353-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37353-173">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="37353-173">INPUTS</span></span>

### <span data-ttu-id="37353-174">System. String</span><span class="sxs-lookup"><span data-stu-id="37353-174">System.String</span></span>

### <span data-ttu-id="37353-175">Microsoft. Azure. Management. monitor. Management. Models. ComparisonOperationType</span><span class="sxs-lookup"><span data-stu-id="37353-175">Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType</span></span>

### <span data-ttu-id="37353-176">Microsoft. Azure. Management. monitor. Management. Models. MetricStatisticType</span><span class="sxs-lookup"><span data-stu-id="37353-176">Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType</span></span>

### <span data-ttu-id="37353-177">System. Double</span><span class="sxs-lookup"><span data-stu-id="37353-177">System.Double</span></span>

### <span data-ttu-id="37353-178">Microsoft. Azure. Management. monitor. Management. Models. TimeAggregationType</span><span class="sxs-lookup"><span data-stu-id="37353-178">Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType</span></span>

### <span data-ttu-id="37353-179">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="37353-179">System.TimeSpan</span></span>

### <span data-ttu-id="37353-180">Microsoft. Azure. Management. monitor. Management. Models. ScaleDirection</span><span class="sxs-lookup"><span data-stu-id="37353-180">Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection</span></span>

### <span data-ttu-id="37353-181">Microsoft. Azure. Management. monitor. Management. Models. ScaleType</span><span class="sxs-lookup"><span data-stu-id="37353-181">Microsoft.Azure.Management.Monitor.Management.Models.ScaleType</span></span>

## <span data-ttu-id="37353-182">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="37353-182">OUTPUTS</span></span>

### <span data-ttu-id="37353-183">Microsoft. Azure. Management. monitor. Management. Models. ScaleRule</span><span class="sxs-lookup"><span data-stu-id="37353-183">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="37353-184">Note</span><span class="sxs-lookup"><span data-stu-id="37353-184">NOTES</span></span>

## <span data-ttu-id="37353-185">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="37353-185">RELATED LINKS</span></span>

[<span data-ttu-id="37353-186">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="37353-186">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="37353-187">Get-AzAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="37353-187">Get-AzAutoscaleHistory</span></span>](./Get-AzAutoscaleHistory.md)

[<span data-ttu-id="37353-188">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="37353-188">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="37353-189">New-AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="37353-189">New-AzAutoscaleProfile</span></span>](./New-AzAutoscaleProfile.md)

[<span data-ttu-id="37353-190">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="37353-190">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


