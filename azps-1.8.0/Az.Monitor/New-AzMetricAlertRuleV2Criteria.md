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
# New-AzMetricAlertRuleV2Criteria

## Sinossi
Crea un oggetto criteri locale che può essere usato per creare un nuovo avviso metrico

## SINTASSI

### StaticThresholdParameterSet
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String> -Operator <String> -Threshold <Double>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### DynamicThresholdParameterSet
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String> -Operator <String>
 -DynamicThreshold <String> [-Sensitivity <String>] [-FailingPeriod <Int32>] [-TotalPeriod <Int32>]
 [-IgnoreDataBefore <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzMetricAlertRuleV2Criteria** crea un oggetto Criteri metrico locale da usare come cmdlet di input Add-AzMetricAlertRuleV2 che crea una nuova regola di avviso metrica.

## ESEMPI

### Esempio 1: creare un criterio di avviso metrico semplice

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

Questo comando crea un criterio di avviso metrico semplice che può essere usato in una regola di avviso metrica

### Esempio 2: creare un criterio di avviso metrico più complesso

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

Questo set di comandi crea un criterio di avviso metrico più complesso che include la selezione delle dimensioni

## PARAMETRI

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

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

### -DimensionSelection
Elenco delle condizioni di dimensione

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

### -DynamicThreshold
Soglia dinamica per la condizione di regola

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

### -FailingPeriod
Periodo di errore per la condizione di regola

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

### -IgnoreDataBefore
Il parametro IgnoreDataBefore

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

### -Metricname
Il nome della metrica per la regola

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

### -MetricNamespace
Lo spazio dei nomi della metrica

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

### -Operator
Operatore della condizione di regola

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

### -Sensitivity
La sensibilità per la condizione di regola

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

### -Soglia
Soglia per la condizione di regola

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

### -TimeAggregation
Operazione di aggregazione utilizzata per eseguire il rollup di più valori metrici nell'intervallo di finestra

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

### -TotalPeriod
Periodo totale per la condizione di regola

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

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.
Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricDimension []

## OUTPUT

### Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricCriteria

## Note

## COLLEGAMENTI CORRELATI
