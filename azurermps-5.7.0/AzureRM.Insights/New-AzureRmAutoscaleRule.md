---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscalerule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleRule.md
ms.openlocfilehash: 575c6e5b210ca47e1904c5174f97b5886b0428b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686739"
---
# <span data-ttu-id="1f01c-101">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="1f01c-101">New-AzureRmAutoscaleRule</span></span>

## <span data-ttu-id="1f01c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1f01c-102">SYNOPSIS</span></span>
<span data-ttu-id="1f01c-103">Crea una regola di scalabilità verticale.</span><span class="sxs-lookup"><span data-stu-id="1f01c-103">Creates an Autoscale rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f01c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1f01c-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f01c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f01c-105">DESCRIPTION</span></span>
<span data-ttu-id="1f01c-106">Il cmdlet **New-AzureRmAutoscaleRule** crea una regola di scalabilità verticale.</span><span class="sxs-lookup"><span data-stu-id="1f01c-106">The **New-AzureRmAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="1f01c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1f01c-107">EXAMPLES</span></span>

### <span data-ttu-id="1f01c-108">Esempio 1: creare una regola</span><span class="sxs-lookup"><span data-stu-id="1f01c-108">Example 1: Create a rule</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="1f01c-109">Questo comando crea una regola.</span><span class="sxs-lookup"><span data-stu-id="1f01c-109">This command creates a rule.</span></span>

### <span data-ttu-id="1f01c-110">Esempio 2: creare due regole</span><span class="sxs-lookup"><span data-stu-id="1f01c-110">Example 2: Create two rules</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="1f01c-111">Il primo comando crea una regola per la metrica delle richieste e quindi la archivia nella variabile $Rule 1.</span><span class="sxs-lookup"><span data-stu-id="1f01c-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>

<span data-ttu-id="1f01c-112">Il secondo comando crea una seconda regola per la metrica richieste e quindi la archivia nella variabile $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="1f01c-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

## <span data-ttu-id="1f01c-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1f01c-113">PARAMETERS</span></span>

### <span data-ttu-id="1f01c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f01c-114">-DefaultProfile</span></span>
<span data-ttu-id="1f01c-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1f01c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f01c-116">-Metricname</span><span class="sxs-lookup"><span data-stu-id="1f01c-116">-MetricName</span></span>
<span data-ttu-id="1f01c-117">Specifica il nome della metrica.</span><span class="sxs-lookup"><span data-stu-id="1f01c-117">Specifies the name of the metric.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f01c-118">-MetricResourceId</span><span class="sxs-lookup"><span data-stu-id="1f01c-118">-MetricResourceId</span></span>
<span data-ttu-id="1f01c-119">Specifica l'ID delle risorse metriche.</span><span class="sxs-lookup"><span data-stu-id="1f01c-119">Specifies the metric resource ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f01c-120">-MetricStatistic</span><span class="sxs-lookup"><span data-stu-id="1f01c-120">-MetricStatistic</span></span>
<span data-ttu-id="1f01c-121">Specifica la statistica metrica.</span><span class="sxs-lookup"><span data-stu-id="1f01c-121">Specifies the metric statistic.</span></span>
<span data-ttu-id="1f01c-122">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="1f01c-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1f01c-123">Media</span><span class="sxs-lookup"><span data-stu-id="1f01c-123">Average</span></span>
- <span data-ttu-id="1f01c-124">Min</span><span class="sxs-lookup"><span data-stu-id="1f01c-124">Min</span></span>
- <span data-ttu-id="1f01c-125">Max</span><span class="sxs-lookup"><span data-stu-id="1f01c-125">Max</span></span>
- <span data-ttu-id="1f01c-126">Somma</span><span class="sxs-lookup"><span data-stu-id="1f01c-126">Sum</span></span>

```yaml
Type: MetricStatisticType
Parameter Sets: (All)
Aliases: 
Accepted values: Average, Min, Max, Sum

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f01c-127">-Operator</span><span class="sxs-lookup"><span data-stu-id="1f01c-127">-Operator</span></span>
<span data-ttu-id="1f01c-128">Specifica l'operatore.</span><span class="sxs-lookup"><span data-stu-id="1f01c-128">Specifies the operator.</span></span>
<span data-ttu-id="1f01c-129">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="1f01c-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1f01c-130">È uguale a</span><span class="sxs-lookup"><span data-stu-id="1f01c-130">Equals</span></span>
- <span data-ttu-id="1f01c-131">NotEquals</span><span class="sxs-lookup"><span data-stu-id="1f01c-131">NotEquals</span></span>
- <span data-ttu-id="1f01c-132">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="1f01c-132">GreaterThan</span></span>
- <span data-ttu-id="1f01c-133">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="1f01c-133">GreaterThanOrEqual</span></span>
- <span data-ttu-id="1f01c-134">LessThan</span><span class="sxs-lookup"><span data-stu-id="1f01c-134">LessThan</span></span>
- <span data-ttu-id="1f01c-135">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="1f01c-135">LessThanOrEqual</span></span>

```yaml
Type: ComparisonOperationType
Parameter Sets: (All)
Aliases: 
Accepted values: Equals, NotEquals, GreaterThan, GreaterThanOrEqual, LessThan, LessThanOrEqual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f01c-136">-ScaleActionCooldown</span><span class="sxs-lookup"><span data-stu-id="1f01c-136">-ScaleActionCooldown</span></span>
<span data-ttu-id="1f01c-137">Specifica il tempo di ricarica delle azioni autoscale.</span><span class="sxs-lookup"><span data-stu-id="1f01c-137">Specifies the Autoscale action cooldown time.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f01c-138">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="1f01c-138">-ScaleActionDirection</span></span>
<span data-ttu-id="1f01c-139">Specifica la direzione dell'azione scala.</span><span class="sxs-lookup"><span data-stu-id="1f01c-139">Specifies the scale action direction.</span></span>
<span data-ttu-id="1f01c-140">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="1f01c-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1f01c-141">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1f01c-141">None</span></span>
- <span data-ttu-id="1f01c-142">Aumentare</span><span class="sxs-lookup"><span data-stu-id="1f01c-142">Increase</span></span>
- <span data-ttu-id="1f01c-143">Diminuzione</span><span class="sxs-lookup"><span data-stu-id="1f01c-143">Decrease</span></span>

```yaml
Type: ScaleDirection
Parameter Sets: (All)
Aliases: 
Accepted values: None, Increase, Decrease

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f01c-144">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="1f01c-144">-ScaleActionScaleType</span></span>
<span data-ttu-id="1f01c-145">Specifica il tipo di scala.</span><span class="sxs-lookup"><span data-stu-id="1f01c-145">Specifies the scale type.</span></span>
<span data-ttu-id="1f01c-146">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="1f01c-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1f01c-147">ChangeSize</span><span class="sxs-lookup"><span data-stu-id="1f01c-147">ChangeSize</span></span>
- <span data-ttu-id="1f01c-148">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="1f01c-148">ChangeCount</span></span>
- <span data-ttu-id="1f01c-149">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="1f01c-149">PercentChangeCount</span></span>
- <span data-ttu-id="1f01c-150">ExactCount</span><span class="sxs-lookup"><span data-stu-id="1f01c-150">ExactCount</span></span>

```yaml
Type: ScaleType
Parameter Sets: (All)
Aliases: 
Accepted values: ChangeCount, PercentChangeCount, ExactCount

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f01c-151">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="1f01c-151">-ScaleActionValue</span></span>
<span data-ttu-id="1f01c-152">Specifica il valore dell'azione.</span><span class="sxs-lookup"><span data-stu-id="1f01c-152">Specifies the action value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f01c-153">-Soglia</span><span class="sxs-lookup"><span data-stu-id="1f01c-153">-Threshold</span></span>
<span data-ttu-id="1f01c-154">Specifica la soglia del valore metrico.</span><span class="sxs-lookup"><span data-stu-id="1f01c-154">Specifies the threshold of the metric value.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f01c-155">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="1f01c-155">-TimeAggregationOperator</span></span>
<span data-ttu-id="1f01c-156">Specifica l'operatore di aggregazione temporale.</span><span class="sxs-lookup"><span data-stu-id="1f01c-156">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="1f01c-157">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="1f01c-157">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1f01c-158">Media</span><span class="sxs-lookup"><span data-stu-id="1f01c-158">Average</span></span>
- <span data-ttu-id="1f01c-159">Minimo</span><span class="sxs-lookup"><span data-stu-id="1f01c-159">Minimum</span></span>
- <span data-ttu-id="1f01c-160">Massimo</span><span class="sxs-lookup"><span data-stu-id="1f01c-160">Maximum</span></span>
- <span data-ttu-id="1f01c-161">Ultima</span><span class="sxs-lookup"><span data-stu-id="1f01c-161">Last</span></span>
- <span data-ttu-id="1f01c-162">Totale, conteggio</span><span class="sxs-lookup"><span data-stu-id="1f01c-162">Total, Count</span></span>

```yaml
Type: TimeAggregationType
Parameter Sets: (All)
Aliases: 
Accepted values: Average, Minimum, Maximum, Total, Count

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f01c-163">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="1f01c-163">-TimeGrain</span></span>
<span data-ttu-id="1f01c-164">Specifica la granulosità temporale.</span><span class="sxs-lookup"><span data-stu-id="1f01c-164">Specifies the time grain.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f01c-165">-TimeWindow</span><span class="sxs-lookup"><span data-stu-id="1f01c-165">-TimeWindow</span></span>
<span data-ttu-id="1f01c-166">Specifica la finestra temporale.</span><span class="sxs-lookup"><span data-stu-id="1f01c-166">Specifies the time window.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f01c-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f01c-167">CommonParameters</span></span>
<span data-ttu-id="1f01c-168">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f01c-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f01c-169">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f01c-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f01c-170">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1f01c-170">INPUTS</span></span>

### <span data-ttu-id="1f01c-171">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1f01c-171">None</span></span>
<span data-ttu-id="1f01c-172">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="1f01c-172">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1f01c-173">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1f01c-173">OUTPUTS</span></span>

### <span data-ttu-id="1f01c-174">Microsoft. Azure. Management. monitor. Management. Models. ScaleRule</span><span class="sxs-lookup"><span data-stu-id="1f01c-174">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="1f01c-175">Note</span><span class="sxs-lookup"><span data-stu-id="1f01c-175">NOTES</span></span>

## <span data-ttu-id="1f01c-176">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1f01c-176">RELATED LINKS</span></span>

[<span data-ttu-id="1f01c-177">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="1f01c-177">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="1f01c-178">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="1f01c-178">Get-AzureRmAutoscaleHistory</span></span>](./Get-AzureRmAutoscaleHistory.md)

[<span data-ttu-id="1f01c-179">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="1f01c-179">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="1f01c-180">New-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="1f01c-180">New-AzureRmAutoscaleProfile</span></span>](./New-AzureRmAutoscaleProfile.md)

[<span data-ttu-id="1f01c-181">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="1f01c-181">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


