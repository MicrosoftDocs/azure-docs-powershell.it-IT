---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2criteria
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
ms.openlocfilehash: 951f9e5843987d1ad36378716b7a95e5d7a1f0a5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964414"
---
# <span data-ttu-id="70a45-101">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="70a45-101">New-AzMetricAlertRuleV2Criteria</span></span>

## <span data-ttu-id="70a45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70a45-102">SYNOPSIS</span></span>
<span data-ttu-id="70a45-103">Crea un oggetto criteri locale che può essere usato per creare un nuovo avviso metrico</span><span class="sxs-lookup"><span data-stu-id="70a45-103">Creates a local criteria object that can be used to create a new metric alert</span></span>

## <span data-ttu-id="70a45-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="70a45-104">SYNTAX</span></span>

### <span data-ttu-id="70a45-105">StaticThresholdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="70a45-105">StaticThresholdParameterSet (Default)</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-SkipMetricValidation <Boolean>] [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String>
 -Operator <String> -Threshold <Double> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70a45-106">DynamicThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="70a45-106">DynamicThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-DynamicThreshold] -MetricName <String> [-MetricNamespace <String>]
 [-SkipMetricValidation <Boolean>] [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String>
 -Operator <String> [-ThresholdSensitivity <String>] [-ViolationCount <Int32>]
 [-ExaminedAggregatedPointCount <Int32>] [-IgnoreDataBefore <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70a45-107">WebtestParameterSet</span><span class="sxs-lookup"><span data-stu-id="70a45-107">WebtestParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-WebTest] -WebTestId <String> -ApplicationInsightsId <String>
 [-FailedLocationCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70a45-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="70a45-108">DESCRIPTION</span></span>
<span data-ttu-id="70a45-109">Il cmdlet **New-AzMetricAlertRuleV2Criteria** crea un oggetto criteri metrico locale da usare come cmdlet [add-AzMetricAlertRuleV2](https://docs.microsoft.com/powershell/module/az.monitor/add-azmetricalertrulev2) di input, che crea una nuova regola di avviso per la metrica.</span><span class="sxs-lookup"><span data-stu-id="70a45-109">The **New-AzMetricAlertRuleV2Criteria** cmdlet creates a local metric criteria object to be used as an input [Add-AzMetricAlertRuleV2](https://docs.microsoft.com/powershell/module/az.monitor/add-azmetricalertrulev2) cmdlet which creates a new metric alert rule.</span></span>

## <span data-ttu-id="70a45-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="70a45-110">EXAMPLES</span></span>

### <span data-ttu-id="70a45-111">Esempio 1: Creare un semplice criterio di avviso per una metrica</span><span class="sxs-lookup"><span data-stu-id="70a45-111">Example 1: Create a simple metric alert criteria</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2Criteria -MetricName "Percentage CPU" -MetricNameSpace "Microsoft.Compute/virtualMachines" -TimeAggregation Average -Operator GreaterThan -Threshold 5

CriterionType        : StaticThresholdCriterion
OperatorProperty     : GreaterThan
Threshold            : 5
AdditionalProperties :
Name                 : metric1
MetricName           : Percentage CPU
MetricNamespace      : Microsoft.Compute/virtualMachines
TimeAggregation      : Average
Dimensions           :
```

<span data-ttu-id="70a45-112">Questo comando crea un semplice criterio di avviso metrico che può essere usato in una regola di avviso metrica</span><span class="sxs-lookup"><span data-stu-id="70a45-112">This command creates a simple metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="70a45-113">Esempio 2: Creare criteri di avviso per una metrica dinamica</span><span class="sxs-lookup"><span data-stu-id="70a45-113">Example 2: Create a dynamic metric alert criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2Criteria -Dynamic -MetricName "Percentage CPU" -MetricNameSpace "Microsoft.Compute/virtualMachines" -TimeAggregation Average -Operator GreaterThan -ThresholdSensitivity Medium -ViolationCount 2 -ExaminedAggregatedPointCount 4
CriterionType        : DynamicThresholdCriterion
OperatorProperty     : GreaterThan
AlertSensitivity     : Medium
FailingPeriods       : Microsoft.Azure.Management.Monitor.Models.DynamicThresholdFailingPeriods
IgnoreDataBefore     :
AdditionalProperties :
Name                 : metric1
MetricName           : Percentage CPU
MetricNamespace      : Microsoft.Compute/virtualMachines
TimeAggregation      : Average
Dimensions           :
```

<span data-ttu-id="70a45-114">Questo comando crea un criterio di avviso metrico dinamico che può essere usato in una regola di avviso metrica</span><span class="sxs-lookup"><span data-stu-id="70a45-114">This command creates a Dynamic metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="70a45-115">Esempio 3: Creare criteri di avviso per una metrica più complessi</span><span class="sxs-lookup"><span data-stu-id="70a45-115">Example 3: Create a more complex metric alert criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2DimensionSelection -DimensionName "availabilityResult/name" -ValuesToInclude "gdtest" | New-AzMetricAlertRuleV2Criteria -MetricName "availabilityResults/availabilityPercentage" -TimeAggregation Average -Operator GreaterThan -Threshold 2
CriterionType        : StaticThresholdCriterion
OperatorProperty     : GreaterThan
Threshold            : 2
AdditionalProperties :
Name                 : metric1
MetricName           : availabilityResults/availabilityPercentage
MetricNamespace      :
TimeAggregation      : Average
Dimensions           : {availabilityResult/name}
```

<span data-ttu-id="70a45-116">Questo set di comandi crea un criterio di avviso metrico più complesso, che include la selezione della dimensione</span><span class="sxs-lookup"><span data-stu-id="70a45-116">This set of commands creates a more complex metric alert criteria which includes dimension selection</span></span>

### <span data-ttu-id="70a45-117">Esempio 4: Creare criteri di disponibilità per un test Web</span><span class="sxs-lookup"><span data-stu-id="70a45-117">Example 4: Create a webtest availability criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2Criteria -WebTest -WebTestId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/webtests/PingTest-appInsights" -ApplicationInsightsId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/components/appInsights" -FailedLocationCount 3
CriterionType        : WebtestLocationAvailabilityCriterion
WebTestId            : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/webtests/PingTest-appInsights
ComponentId          : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/components/appInsights
FailedLocationCount  : 3
AdditionalProperties :
```

<span data-ttu-id="70a45-118">Questo comando crea un criterio di disponibilità per il test Web che può essere usato in una regola di avviso metrica</span><span class="sxs-lookup"><span data-stu-id="70a45-118">This command creates a webtest availability criteria that can be used in a metric alert rule</span></span>

## <span data-ttu-id="70a45-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70a45-119">PARAMETERS</span></span>

### <span data-ttu-id="70a45-120">-ApplicationInsightsId</span><span class="sxs-lookup"><span data-stu-id="70a45-120">-ApplicationInsightsId</span></span>
<span data-ttu-id="70a45-121">ID risorsa di Application Insights.</span><span class="sxs-lookup"><span data-stu-id="70a45-121">The Application Insights resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: WebtestParameterSet
Aliases: componentId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70a45-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70a45-122">-DefaultProfile</span></span>
<span data-ttu-id="70a45-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="70a45-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70a45-124">-DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="70a45-124">-DimensionSelection</span></span>
<span data-ttu-id="70a45-125">Elenco delle condizioni delle dimensioni</span><span class="sxs-lookup"><span data-stu-id="70a45-125">List of dimension conditions</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70a45-126">-DynamicThreshold</span><span class="sxs-lookup"><span data-stu-id="70a45-126">-DynamicThreshold</span></span>
<span data-ttu-id="70a45-127">Parametro switch per l'uso del tipo di soglia dinamica</span><span class="sxs-lookup"><span data-stu-id="70a45-127">Switch parameter for using Dynamic Threshold Type</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70a45-128">-ExaminedAggregatedPointCount</span><span class="sxs-lookup"><span data-stu-id="70a45-128">-ExaminedAggregatedPointCount</span></span>
<span data-ttu-id="70a45-129">Il numero totale di punti esaminati</span><span class="sxs-lookup"><span data-stu-id="70a45-129">The Total number of examined points</span></span>

```yaml
Type: System.Int32
Parameter Sets: DynamicThresholdParameterSet
Aliases: TotalPeriod, NumberOfExaminedAggregatedPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70a45-130">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="70a45-130">-FailedLocationCount</span></span>
<span data-ttu-id="70a45-131">Il numero minimo di posizioni non riuscite per generare un avviso.</span><span class="sxs-lookup"><span data-stu-id="70a45-131">The minimum number of failed locations to raise an alert.</span></span>

```yaml
Type: System.Int32
Parameter Sets: WebtestParameterSet
Aliases: AlertLocationThreshold

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70a45-132">-IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="70a45-132">-IgnoreDataBefore</span></span>
<span data-ttu-id="70a45-133">Parametro IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="70a45-133">The IgnoreDataBefore parameter</span></span>

```yaml
Type: System.DateTime
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70a45-134">-MetricName</span><span class="sxs-lookup"><span data-stu-id="70a45-134">-MetricName</span></span>
<span data-ttu-id="70a45-135">Nome della metrica per la regola</span><span class="sxs-lookup"><span data-stu-id="70a45-135">The metric name for rule</span></span>

```yaml
Type: System.String
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70a45-136">-MetricMetricMetric</span><span class="sxs-lookup"><span data-stu-id="70a45-136">-MetricNamespace</span></span>
<span data-ttu-id="70a45-137">Spazio dei nomi della metrica</span><span class="sxs-lookup"><span data-stu-id="70a45-137">The Namespace of the metric</span></span>

```yaml
Type: System.String
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70a45-138">-Operatore</span><span class="sxs-lookup"><span data-stu-id="70a45-138">-Operator</span></span>
<span data-ttu-id="70a45-139">Operatore condizione regola</span><span class="sxs-lookup"><span data-stu-id="70a45-139">The rule condition operator</span></span>

```yaml
Type: System.String
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70a45-140">-SkipMetricValid</span><span class="sxs-lookup"><span data-stu-id="70a45-140">-SkipMetricValidation</span></span>
<span data-ttu-id="70a45-141">Consente di creare una regola di avviso su una metrica personalizzata non ancora emessa, causando l'omissione della convalida della metrica</span><span class="sxs-lookup"><span data-stu-id="70a45-141">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped</span></span>

```yaml
Type: System.Boolean
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70a45-142">-Threshold</span><span class="sxs-lookup"><span data-stu-id="70a45-142">-Threshold</span></span>
<span data-ttu-id="70a45-143">Soglia per la condizione della regola</span><span class="sxs-lookup"><span data-stu-id="70a45-143">The threshold for rule condition</span></span>

```yaml
Type: System.Double
Parameter Sets: StaticThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70a45-144">-ThresholdSensitivity</span><span class="sxs-lookup"><span data-stu-id="70a45-144">-ThresholdSensitivity</span></span>
<span data-ttu-id="70a45-145">Riservatezza per la condizione della regola</span><span class="sxs-lookup"><span data-stu-id="70a45-145">The sensitivity for rule condition</span></span>

```yaml
Type: System.String
Parameter Sets: DynamicThresholdParameterSet
Aliases: Sensitivity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70a45-146">-TimeAggregation</span><span class="sxs-lookup"><span data-stu-id="70a45-146">-TimeAggregation</span></span>
<span data-ttu-id="70a45-147">Operazione di aggregazione usata per eseguire il roll up di più valori di metrica nell'intervallo della finestra</span><span class="sxs-lookup"><span data-stu-id="70a45-147">The aggregation operation used to roll up multiple metric values across the window interval</span></span>

```yaml
Type: System.String
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70a45-148">-ViolationCount</span><span class="sxs-lookup"><span data-stu-id="70a45-148">-ViolationCount</span></span>
<span data-ttu-id="70a45-149">Il numero minimo di violazioni necessarie nell'intervallo di tempo di lookback selezionato necessario per generare un avviso</span><span class="sxs-lookup"><span data-stu-id="70a45-149">The minimum number of violations required within the selected lookback time window required to raise an alert</span></span>

```yaml
Type: System.Int32
Parameter Sets: DynamicThresholdParameterSet
Aliases: FailingPeriod, NumberOfViolations

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70a45-150">-WebTest</span><span class="sxs-lookup"><span data-stu-id="70a45-150">-WebTest</span></span>
<span data-ttu-id="70a45-151">Parametro switch per l'uso del tipo di criteri di disponibilità</span><span class="sxs-lookup"><span data-stu-id="70a45-151">Switch parameter for using availability criteria Type</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebtestParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70a45-152">-WebTestId</span><span class="sxs-lookup"><span data-stu-id="70a45-152">-WebTestId</span></span>
<span data-ttu-id="70a45-153">ID test Web di Application Insights.</span><span class="sxs-lookup"><span data-stu-id="70a45-153">The Application Insights web test Id.</span></span>

```yaml
Type: System.String
Parameter Sets: WebtestParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70a45-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70a45-154">CommonParameters</span></span>
<span data-ttu-id="70a45-155">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70a45-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70a45-156">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="70a45-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70a45-157">INPUT</span><span class="sxs-lookup"><span data-stu-id="70a45-157">INPUTS</span></span>

### <span data-ttu-id="70a45-158">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span><span class="sxs-lookup"><span data-stu-id="70a45-158">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span></span>

## <span data-ttu-id="70a45-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="70a45-159">OUTPUTS</span></span>

### <span data-ttu-id="70a45-160">Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria</span><span class="sxs-lookup"><span data-stu-id="70a45-160">Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria</span></span>

## <span data-ttu-id="70a45-161">NOTE</span><span class="sxs-lookup"><span data-stu-id="70a45-161">NOTES</span></span>

## <span data-ttu-id="70a45-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="70a45-162">RELATED LINKS</span></span>
