---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
ms.openlocfilehash: 16687824216fa0014d59b78a96d22a4da8a19fda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835031"
---
# <span data-ttu-id="22117-101">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="22117-101">New-AzMetricAlertRuleV2Criteria</span></span>

## <span data-ttu-id="22117-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="22117-102">SYNOPSIS</span></span>
<span data-ttu-id="22117-103">Crea un oggetto criteri locale che può essere usato per creare un nuovo avviso metrico</span><span class="sxs-lookup"><span data-stu-id="22117-103">Creates a local criteria object that can be used to create a new metric alert</span></span>

## <span data-ttu-id="22117-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="22117-104">SYNTAX</span></span>

### <span data-ttu-id="22117-105">StaticThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="22117-105">StaticThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String> -Operator <String> -Threshold <Double>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22117-106">DynamicThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="22117-106">DynamicThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String> -Operator <String>
 -DynamicThreshold <String> [-Sensitivity <String>] [-FailingPeriod <Int32>] [-TotalPeriod <Int32>]
 [-IgnoreDataBefore <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22117-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22117-107">DESCRIPTION</span></span>
<span data-ttu-id="22117-108">Il cmdlet **New-AzMetricAlertRuleV2Criteria** crea un oggetto Criteri metrico locale da usare come cmdlet di input Add-AzMetricAlertRuleV2 che crea una nuova regola di avviso metrica.</span><span class="sxs-lookup"><span data-stu-id="22117-108">The **New-AzMetricAlertRuleV2Criteria** cmdlet creates a local metric criteria object to be used as an input Add-AzMetricAlertRuleV2 cmdlet which creates a new metric alert rule.</span></span>

## <span data-ttu-id="22117-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="22117-109">EXAMPLES</span></span>

### <span data-ttu-id="22117-110">Esempio 1: creare un criterio di avviso metrico semplice</span><span class="sxs-lookup"><span data-stu-id="22117-110">Example 1: Create a simple metric alert criteria</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2Criteria -MetricName "Percentage CPU" -MetricNameSpace "Microsoft.Compute/virtualMachines" -TimeAggregation Average -Operator GreaterThan -Threshold 5

Name                 : metric1
MetricName           : Percentage CPU
MetricNamespace      : Microsoft.Compute/virtualMachines
OperatorProperty     : GreaterThan
TimeAggregation      : Average
Threshold            : 5
Dimensions           :
AdditionalProperties :
```

<span data-ttu-id="22117-111">Questo comando crea un criterio di avviso metrico semplice che può essere usato in una regola di avviso metrica</span><span class="sxs-lookup"><span data-stu-id="22117-111">This command creates a simple metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="22117-112">Esempio 2: creare un criterio di avviso metrico più complesso</span><span class="sxs-lookup"><span data-stu-id="22117-112">Example 2: Create a more complex metric alert criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2DimensionSelection -DimensionName "availabilityResult/name" -ValuesToInclude "gdtest" | New-AzMetricAlertRuleV2Criteria -MetricName "availabilityResults/availabilityPercentage" -TimeAggregation Average -Operator GreaterThan -Threshold 2
Name                 : metric1
MetricName           : availabilityResults/availabilityPercentage
MetricNamespace      :
OperatorProperty     : GreaterThan
TimeAggregation      : Average
Threshold            : 2
Dimensions           : {availabilityResult/name}
AdditionalProperties :
```

<span data-ttu-id="22117-113">Questo set di comandi crea un criterio di avviso metrico più complesso che include la selezione delle dimensioni</span><span class="sxs-lookup"><span data-stu-id="22117-113">This set of commands creates a more complex metric alert criteria which includes dimension selection</span></span>

## <span data-ttu-id="22117-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="22117-114">PARAMETERS</span></span>

### <span data-ttu-id="22117-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22117-115">-DefaultProfile</span></span>
<span data-ttu-id="22117-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="22117-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22117-117">-DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="22117-117">-DimensionSelection</span></span>
<span data-ttu-id="22117-118">Elenco delle condizioni di dimensione</span><span class="sxs-lookup"><span data-stu-id="22117-118">List of dimension conditions</span></span>

```yaml
Type: PSMetricDimension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22117-119">-DynamicThreshold</span><span class="sxs-lookup"><span data-stu-id="22117-119">-DynamicThreshold</span></span>
<span data-ttu-id="22117-120">Soglia dinamica per la condizione di regola</span><span class="sxs-lookup"><span data-stu-id="22117-120">The Dynamic Threshold for rule condition</span></span>

```yaml
Type: String
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22117-121">-FailingPeriod</span><span class="sxs-lookup"><span data-stu-id="22117-121">-FailingPeriod</span></span>
<span data-ttu-id="22117-122">Periodo di errore per la condizione di regola</span><span class="sxs-lookup"><span data-stu-id="22117-122">The Failing Period for rule condition</span></span>

```yaml
Type: Int32
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22117-123">-IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="22117-123">-IgnoreDataBefore</span></span>
<span data-ttu-id="22117-124">Il parametro IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="22117-124">The IgnoreDataBefore parameter</span></span>

```yaml
Type: DateTime
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22117-125">-Metricname</span><span class="sxs-lookup"><span data-stu-id="22117-125">-MetricName</span></span>
<span data-ttu-id="22117-126">Il nome della metrica per la regola</span><span class="sxs-lookup"><span data-stu-id="22117-126">The metric name for rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22117-127">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="22117-127">-MetricNamespace</span></span>
<span data-ttu-id="22117-128">Lo spazio dei nomi della metrica</span><span class="sxs-lookup"><span data-stu-id="22117-128">The Namespace of the metric</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22117-129">-Operator</span><span class="sxs-lookup"><span data-stu-id="22117-129">-Operator</span></span>
<span data-ttu-id="22117-130">Operatore della condizione di regola</span><span class="sxs-lookup"><span data-stu-id="22117-130">The rule condition operator</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22117-131">-Sensitivity</span><span class="sxs-lookup"><span data-stu-id="22117-131">-Sensitivity</span></span>
<span data-ttu-id="22117-132">La sensibilità per la condizione di regola</span><span class="sxs-lookup"><span data-stu-id="22117-132">The sensitivity for rule condition</span></span>

```yaml
Type: String
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22117-133">-Soglia</span><span class="sxs-lookup"><span data-stu-id="22117-133">-Threshold</span></span>
<span data-ttu-id="22117-134">Soglia per la condizione di regola</span><span class="sxs-lookup"><span data-stu-id="22117-134">The threshold for rule condition</span></span>

```yaml
Type: Double
Parameter Sets: StaticThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22117-135">-TimeAggregation</span><span class="sxs-lookup"><span data-stu-id="22117-135">-TimeAggregation</span></span>
<span data-ttu-id="22117-136">Operazione di aggregazione utilizzata per eseguire il rollup di più valori metrici nell'intervallo di finestra</span><span class="sxs-lookup"><span data-stu-id="22117-136">The aggregation operation used to roll up multiple metric values across the window interval</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22117-137">-TotalPeriod</span><span class="sxs-lookup"><span data-stu-id="22117-137">-TotalPeriod</span></span>
<span data-ttu-id="22117-138">Periodo totale per la condizione di regola</span><span class="sxs-lookup"><span data-stu-id="22117-138">The Total Period for rule condition</span></span>

```yaml
Type: Int32
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22117-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22117-139">CommonParameters</span></span>
<span data-ttu-id="22117-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22117-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="22117-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22117-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22117-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="22117-142">INPUTS</span></span>

### <span data-ttu-id="22117-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricDimension []</span><span class="sxs-lookup"><span data-stu-id="22117-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span></span>

## <span data-ttu-id="22117-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="22117-144">OUTPUTS</span></span>

### <span data-ttu-id="22117-145">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricCriteria</span><span class="sxs-lookup"><span data-stu-id="22117-145">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricCriteria</span></span>

## <span data-ttu-id="22117-146">Note</span><span class="sxs-lookup"><span data-stu-id="22117-146">NOTES</span></span>

## <span data-ttu-id="22117-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="22117-147">RELATED LINKS</span></span>
