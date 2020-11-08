---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
ms.openlocfilehash: 101d522c1f8ae3b44545bdb204bad01fbe21df9e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192383"
---
# <span data-ttu-id="0f7c4-101">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="0f7c4-101">New-AzMetricAlertRuleV2Criteria</span></span>

## <span data-ttu-id="0f7c4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0f7c4-102">SYNOPSIS</span></span>
<span data-ttu-id="0f7c4-103">Crea un oggetto criteri locale che può essere usato per creare un nuovo avviso metrico</span><span class="sxs-lookup"><span data-stu-id="0f7c4-103">Creates a local criteria object that can be used to create a new metric alert</span></span>

## <span data-ttu-id="0f7c4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0f7c4-104">SYNTAX</span></span>

### <span data-ttu-id="0f7c4-105">StaticThresholdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0f7c4-105">StaticThresholdParameterSet (Default)</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-SkipMetricValidation <Boolean>] [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String>
 -Operator <String> -Threshold <Double> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f7c4-106">DynamicThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f7c4-106">DynamicThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-DynamicThreshold] -MetricName <String> [-MetricNamespace <String>]
 [-SkipMetricValidation <Boolean>] [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String>
 -Operator <String> [-ThresholdSensitivity <String>] [-ViolationCount <Int32>]
 [-ExaminedAggregatedPointCount <Int32>] [-IgnoreDataBefore <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f7c4-107">WebtestParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f7c4-107">WebtestParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-WebTest] -WebTestId <String> -ApplicationInsightsId <String>
 [-FailedLocationCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f7c4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0f7c4-108">DESCRIPTION</span></span>
<span data-ttu-id="0f7c4-109">Il cmdlet **New-AzMetricAlertRuleV2Criteria** crea un oggetto Criteri metrico locale da usare come cmdlet di input Add-AzMetricAlertRuleV2 che crea una nuova regola di avviso metrica.</span><span class="sxs-lookup"><span data-stu-id="0f7c4-109">The **New-AzMetricAlertRuleV2Criteria** cmdlet creates a local metric criteria object to be used as an input Add-AzMetricAlertRuleV2 cmdlet which creates a new metric alert rule.</span></span>

## <span data-ttu-id="0f7c4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0f7c4-110">EXAMPLES</span></span>

### <span data-ttu-id="0f7c4-111">Esempio 1: creare un criterio di avviso metrico semplice</span><span class="sxs-lookup"><span data-stu-id="0f7c4-111">Example 1: Create a simple metric alert criteria</span></span>

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

<span data-ttu-id="0f7c4-112">Questo comando crea un criterio di avviso metrico semplice che può essere usato in una regola di avviso metrica</span><span class="sxs-lookup"><span data-stu-id="0f7c4-112">This command creates a simple metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="0f7c4-113">Esempio 2: creare un criterio di avviso metrico dinamico</span><span class="sxs-lookup"><span data-stu-id="0f7c4-113">Example 2: Create a dynamic metric alert criteria</span></span>

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

<span data-ttu-id="0f7c4-114">Questo comando crea un criterio di avviso metrico dinamico che può essere usato in una regola di avviso metrica</span><span class="sxs-lookup"><span data-stu-id="0f7c4-114">This command creates a Dynamic metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="0f7c4-115">Esempio 3: creare un criterio di avviso metrico più complesso</span><span class="sxs-lookup"><span data-stu-id="0f7c4-115">Example 3: Create a more complex metric alert criteria</span></span>

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

<span data-ttu-id="0f7c4-116">Questo set di comandi crea un criterio di avviso metrico più complesso che include la selezione delle dimensioni</span><span class="sxs-lookup"><span data-stu-id="0f7c4-116">This set of commands creates a more complex metric alert criteria which includes dimension selection</span></span>

### <span data-ttu-id="0f7c4-117">Esempio 4: creare un criterio di disponibilità WebTest</span><span class="sxs-lookup"><span data-stu-id="0f7c4-117">Example 4: Create a webtest availability criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2Criteria -WebTest -WebTestId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/webtests/PingTest-appInsights" -ApplicationInsightsId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/components/appInsights" -FailedLocationCount 3
CriterionType        : WebtestLocationAvailabilityCriterion
WebTestId            : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/webtests/PingTest-appInsights
ComponentId          : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/components/appInsights
FailedLocationCount  : 3
AdditionalProperties :
```

<span data-ttu-id="0f7c4-118">Questo comando crea un criterio di disponibilità WebTest che può essere usato in una regola di avviso metrica</span><span class="sxs-lookup"><span data-stu-id="0f7c4-118">This command creates a webtest availability criteria that can be used in a metric alert rule</span></span>

## <span data-ttu-id="0f7c4-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0f7c4-119">PARAMETERS</span></span>

### <span data-ttu-id="0f7c4-120">-ApplicationInsightsId</span><span class="sxs-lookup"><span data-stu-id="0f7c4-120">-ApplicationInsightsId</span></span>
<span data-ttu-id="0f7c4-121">ID risorsa dell'applicazione Insights.</span><span class="sxs-lookup"><span data-stu-id="0f7c4-121">The Application Insights resource Id.</span></span>

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

### <span data-ttu-id="0f7c4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f7c4-122">-DefaultProfile</span></span>
<span data-ttu-id="0f7c4-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0f7c4-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f7c4-124">-DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="0f7c4-124">-DimensionSelection</span></span>
<span data-ttu-id="0f7c4-125">Elenco delle condizioni di dimensione</span><span class="sxs-lookup"><span data-stu-id="0f7c4-125">List of dimension conditions</span></span>

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

### <span data-ttu-id="0f7c4-126">-DynamicThreshold</span><span class="sxs-lookup"><span data-stu-id="0f7c4-126">-DynamicThreshold</span></span>
<span data-ttu-id="0f7c4-127">Parametro switch per l'uso di tipo soglia dinamico</span><span class="sxs-lookup"><span data-stu-id="0f7c4-127">Switch parameter for using Dynamic Threshold Type</span></span>

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

### <span data-ttu-id="0f7c4-128">-ExaminedAggregatedPointCount</span><span class="sxs-lookup"><span data-stu-id="0f7c4-128">-ExaminedAggregatedPointCount</span></span>
<span data-ttu-id="0f7c4-129">Numero totale di punti esaminati</span><span class="sxs-lookup"><span data-stu-id="0f7c4-129">The Total number of examined points</span></span>

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

### <span data-ttu-id="0f7c4-130">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="0f7c4-130">-FailedLocationCount</span></span>
<span data-ttu-id="0f7c4-131">Numero minimo di posizioni non riuscite per generare un avviso.</span><span class="sxs-lookup"><span data-stu-id="0f7c4-131">The minimum number of failed locations to raise an alert.</span></span>

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

### <span data-ttu-id="0f7c4-132">-IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="0f7c4-132">-IgnoreDataBefore</span></span>
<span data-ttu-id="0f7c4-133">Il parametro IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="0f7c4-133">The IgnoreDataBefore parameter</span></span>

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

### <span data-ttu-id="0f7c4-134">-Metricname</span><span class="sxs-lookup"><span data-stu-id="0f7c4-134">-MetricName</span></span>
<span data-ttu-id="0f7c4-135">Il nome della metrica per la regola</span><span class="sxs-lookup"><span data-stu-id="0f7c4-135">The metric name for rule</span></span>

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

### <span data-ttu-id="0f7c4-136">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="0f7c4-136">-MetricNamespace</span></span>
<span data-ttu-id="0f7c4-137">Lo spazio dei nomi della metrica</span><span class="sxs-lookup"><span data-stu-id="0f7c4-137">The Namespace of the metric</span></span>

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

### <span data-ttu-id="0f7c4-138">-Operator</span><span class="sxs-lookup"><span data-stu-id="0f7c4-138">-Operator</span></span>
<span data-ttu-id="0f7c4-139">Operatore della condizione di regola</span><span class="sxs-lookup"><span data-stu-id="0f7c4-139">The rule condition operator</span></span>

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

### <span data-ttu-id="0f7c4-140">-SkipMetricValidation</span><span class="sxs-lookup"><span data-stu-id="0f7c4-140">-SkipMetricValidation</span></span>
<span data-ttu-id="0f7c4-141">Consente di creare una regola di avviso su una metrica personalizzata che non è ancora stata emessa, causando la convalida metrica da ignorare</span><span class="sxs-lookup"><span data-stu-id="0f7c4-141">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped</span></span>

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

### <span data-ttu-id="0f7c4-142">-Soglia</span><span class="sxs-lookup"><span data-stu-id="0f7c4-142">-Threshold</span></span>
<span data-ttu-id="0f7c4-143">Soglia per la condizione di regola</span><span class="sxs-lookup"><span data-stu-id="0f7c4-143">The threshold for rule condition</span></span>

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

### <span data-ttu-id="0f7c4-144">-ThresholdSensitivity</span><span class="sxs-lookup"><span data-stu-id="0f7c4-144">-ThresholdSensitivity</span></span>
<span data-ttu-id="0f7c4-145">La sensibilità per la condizione di regola</span><span class="sxs-lookup"><span data-stu-id="0f7c4-145">The sensitivity for rule condition</span></span>

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

### <span data-ttu-id="0f7c4-146">-TimeAggregation</span><span class="sxs-lookup"><span data-stu-id="0f7c4-146">-TimeAggregation</span></span>
<span data-ttu-id="0f7c4-147">Operazione di aggregazione utilizzata per eseguire il rollup di più valori metrici nell'intervallo di finestra</span><span class="sxs-lookup"><span data-stu-id="0f7c4-147">The aggregation operation used to roll up multiple metric values across the window interval</span></span>

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

### <span data-ttu-id="0f7c4-148">-ViolationCount</span><span class="sxs-lookup"><span data-stu-id="0f7c4-148">-ViolationCount</span></span>
<span data-ttu-id="0f7c4-149">Il numero minimo di violazioni necessarie all'interno della finestra temporale di lookback selezionata necessaria per generare un avviso</span><span class="sxs-lookup"><span data-stu-id="0f7c4-149">The minimum number of violations required within the selected lookback time window required to raise an alert</span></span>

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

### <span data-ttu-id="0f7c4-150">-WebTest</span><span class="sxs-lookup"><span data-stu-id="0f7c4-150">-WebTest</span></span>
<span data-ttu-id="0f7c4-151">Parametro switch per l'uso del tipo di criteri di disponibilità</span><span class="sxs-lookup"><span data-stu-id="0f7c4-151">Switch parameter for using availability criteria Type</span></span>

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

### <span data-ttu-id="0f7c4-152">-Webtestid</span><span class="sxs-lookup"><span data-stu-id="0f7c4-152">-WebTestId</span></span>
<span data-ttu-id="0f7c4-153">ID test Web dell'applicazione Insights.</span><span class="sxs-lookup"><span data-stu-id="0f7c4-153">The Application Insights web test Id.</span></span>

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

### <span data-ttu-id="0f7c4-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f7c4-154">CommonParameters</span></span>
<span data-ttu-id="0f7c4-155">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f7c4-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f7c4-156">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0f7c4-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f7c4-157">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0f7c4-157">INPUTS</span></span>

### <span data-ttu-id="0f7c4-158">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricDimension []</span><span class="sxs-lookup"><span data-stu-id="0f7c4-158">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span></span>

## <span data-ttu-id="0f7c4-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0f7c4-159">OUTPUTS</span></span>

### <span data-ttu-id="0f7c4-160">Microsoft. Azure. Commands. Insights. OutputClasses. IPSMultiMetricCriteria</span><span class="sxs-lookup"><span data-stu-id="0f7c4-160">Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria</span></span>

## <span data-ttu-id="0f7c4-161">Note</span><span class="sxs-lookup"><span data-stu-id="0f7c4-161">NOTES</span></span>

## <span data-ttu-id="0f7c4-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0f7c4-162">RELATED LINKS</span></span>
