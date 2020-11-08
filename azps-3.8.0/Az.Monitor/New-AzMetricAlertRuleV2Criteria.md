---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
ms.openlocfilehash: 6e50269e98a942d425f914eed5cc0a75938d0e9f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018367"
---
# <span data-ttu-id="2f91e-101">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="2f91e-101">New-AzMetricAlertRuleV2Criteria</span></span>

## <span data-ttu-id="2f91e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2f91e-102">SYNOPSIS</span></span>
<span data-ttu-id="2f91e-103">Crea un oggetto criteri locale che può essere usato per creare un nuovo avviso metrico</span><span class="sxs-lookup"><span data-stu-id="2f91e-103">Creates a local criteria object that can be used to create a new metric alert</span></span>

## <span data-ttu-id="2f91e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2f91e-104">SYNTAX</span></span>

### <span data-ttu-id="2f91e-105">StaticThresholdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2f91e-105">StaticThresholdParameterSet (Default)</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String> -Operator <String> -Threshold <Double>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f91e-106">DynamicThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f91e-106">DynamicThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-DynamicThreshold] -MetricName <String> [-MetricNamespace <String>]
 [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String> -Operator <String>
 [-ThresholdSensitivity <String>] [-ViolationCount <Int32>] [-ExaminedAggregatedPointCount <Int32>]
 [-IgnoreDataBefore <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f91e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2f91e-107">DESCRIPTION</span></span>
<span data-ttu-id="2f91e-108">Il cmdlet **New-AzMetricAlertRuleV2Criteria** crea un oggetto Criteri metrico locale da usare come cmdlet di input Add-AzMetricAlertRuleV2 che crea una nuova regola di avviso metrica.</span><span class="sxs-lookup"><span data-stu-id="2f91e-108">The **New-AzMetricAlertRuleV2Criteria** cmdlet creates a local metric criteria object to be used as an input Add-AzMetricAlertRuleV2 cmdlet which creates a new metric alert rule.</span></span>

## <span data-ttu-id="2f91e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2f91e-109">EXAMPLES</span></span>

### <span data-ttu-id="2f91e-110">Esempio 1: creare un criterio di avviso metrico semplice</span><span class="sxs-lookup"><span data-stu-id="2f91e-110">Example 1: Create a simple metric alert criteria</span></span>

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

<span data-ttu-id="2f91e-111">Questo comando crea un criterio di avviso metrico semplice che può essere usato in una regola di avviso metrica</span><span class="sxs-lookup"><span data-stu-id="2f91e-111">This command creates a simple metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="2f91e-112">Esempio 2: creare un criterio di avviso metrico dinamico</span><span class="sxs-lookup"><span data-stu-id="2f91e-112">Example 2: Create a dynamic metric alert criteria</span></span>

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

<span data-ttu-id="2f91e-113">Questo comando crea un criterio di avviso metrico dinamico che può essere usato in una regola di avviso metrica</span><span class="sxs-lookup"><span data-stu-id="2f91e-113">This command creates a Dynamic metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="2f91e-114">Esempio 3: creare un criterio di avviso metrico più complesso</span><span class="sxs-lookup"><span data-stu-id="2f91e-114">Example 3: Create a more complex metric alert criteria</span></span>

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

<span data-ttu-id="2f91e-115">Questo set di comandi crea un criterio di avviso metrico più complesso che include la selezione delle dimensioni</span><span class="sxs-lookup"><span data-stu-id="2f91e-115">This set of commands creates a more complex metric alert criteria which includes dimension selection</span></span>

## <span data-ttu-id="2f91e-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2f91e-116">PARAMETERS</span></span>

### <span data-ttu-id="2f91e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f91e-117">-DefaultProfile</span></span>
<span data-ttu-id="2f91e-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2f91e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f91e-119">-DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="2f91e-119">-DimensionSelection</span></span>
<span data-ttu-id="2f91e-120">Elenco delle condizioni di dimensione</span><span class="sxs-lookup"><span data-stu-id="2f91e-120">List of dimension conditions</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f91e-121">-DynamicThreshold</span><span class="sxs-lookup"><span data-stu-id="2f91e-121">-DynamicThreshold</span></span>
<span data-ttu-id="2f91e-122">Parametro switch per l'uso di tipo soglia dinamico</span><span class="sxs-lookup"><span data-stu-id="2f91e-122">Switch parameter for using Dynamic Threshold Type</span></span>

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

### <span data-ttu-id="2f91e-123">-ExaminedAggregatedPointCount</span><span class="sxs-lookup"><span data-stu-id="2f91e-123">-ExaminedAggregatedPointCount</span></span>
<span data-ttu-id="2f91e-124">Numero totale di punti esaminati</span><span class="sxs-lookup"><span data-stu-id="2f91e-124">The Total number of examined points</span></span>

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

### <span data-ttu-id="2f91e-125">-IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="2f91e-125">-IgnoreDataBefore</span></span>
<span data-ttu-id="2f91e-126">Il parametro IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="2f91e-126">The IgnoreDataBefore parameter</span></span>

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

### <span data-ttu-id="2f91e-127">-Metricname</span><span class="sxs-lookup"><span data-stu-id="2f91e-127">-MetricName</span></span>
<span data-ttu-id="2f91e-128">Il nome della metrica per la regola</span><span class="sxs-lookup"><span data-stu-id="2f91e-128">The metric name for rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f91e-129">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="2f91e-129">-MetricNamespace</span></span>
<span data-ttu-id="2f91e-130">Lo spazio dei nomi della metrica</span><span class="sxs-lookup"><span data-stu-id="2f91e-130">The Namespace of the metric</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f91e-131">-Operator</span><span class="sxs-lookup"><span data-stu-id="2f91e-131">-Operator</span></span>
<span data-ttu-id="2f91e-132">Operatore della condizione di regola</span><span class="sxs-lookup"><span data-stu-id="2f91e-132">The rule condition operator</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f91e-133">-Soglia</span><span class="sxs-lookup"><span data-stu-id="2f91e-133">-Threshold</span></span>
<span data-ttu-id="2f91e-134">Soglia per la condizione di regola</span><span class="sxs-lookup"><span data-stu-id="2f91e-134">The threshold for rule condition</span></span>

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

### <span data-ttu-id="2f91e-135">-ThresholdSensitivity</span><span class="sxs-lookup"><span data-stu-id="2f91e-135">-ThresholdSensitivity</span></span>
<span data-ttu-id="2f91e-136">La sensibilità per la condizione di regola</span><span class="sxs-lookup"><span data-stu-id="2f91e-136">The sensitivity for rule condition</span></span>

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

### <span data-ttu-id="2f91e-137">-TimeAggregation</span><span class="sxs-lookup"><span data-stu-id="2f91e-137">-TimeAggregation</span></span>
<span data-ttu-id="2f91e-138">Operazione di aggregazione utilizzata per eseguire il rollup di più valori metrici nell'intervallo di finestra</span><span class="sxs-lookup"><span data-stu-id="2f91e-138">The aggregation operation used to roll up multiple metric values across the window interval</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f91e-139">-ViolationCount</span><span class="sxs-lookup"><span data-stu-id="2f91e-139">-ViolationCount</span></span>
<span data-ttu-id="2f91e-140">Il numero minimo di violazioni necessarie all'interno della finestra temporale di lookback selezionata necessaria per generare un avviso</span><span class="sxs-lookup"><span data-stu-id="2f91e-140">The minimum number of violations required within the selected lookback time window required to raise an alert</span></span>

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

### <span data-ttu-id="2f91e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f91e-141">CommonParameters</span></span>
<span data-ttu-id="2f91e-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f91e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f91e-143">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2f91e-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f91e-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2f91e-144">INPUTS</span></span>

### <span data-ttu-id="2f91e-145">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricDimension []</span><span class="sxs-lookup"><span data-stu-id="2f91e-145">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span></span>

## <span data-ttu-id="2f91e-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2f91e-146">OUTPUTS</span></span>

### <span data-ttu-id="2f91e-147">Microsoft. Azure. Commands. Insights. OutputClasses. IPSMultiMetricCriteria</span><span class="sxs-lookup"><span data-stu-id="2f91e-147">Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria</span></span>

## <span data-ttu-id="2f91e-148">Note</span><span class="sxs-lookup"><span data-stu-id="2f91e-148">NOTES</span></span>

## <span data-ttu-id="2f91e-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2f91e-149">RELATED LINKS</span></span>
