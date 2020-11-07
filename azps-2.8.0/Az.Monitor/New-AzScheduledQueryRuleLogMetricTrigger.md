---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulelogmetrictrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
ms.openlocfilehash: 4873d093411c07af9b1a5389299e39ecca0a5f71
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854066"
---
# <span data-ttu-id="91eda-101">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="91eda-101">New-AzScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="91eda-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="91eda-102">SYNOPSIS</span></span>
<span data-ttu-id="91eda-103">Crea un oggetto di trigger metrica log di tipo</span><span class="sxs-lookup"><span data-stu-id="91eda-103">Creates an object of type Log Metric Trigger</span></span>

## <span data-ttu-id="91eda-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="91eda-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator <String> -Threshold <Double>
 -MetricTriggerType <String> -MetricColumn <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="91eda-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91eda-105">DESCRIPTION</span></span>
<span data-ttu-id="91eda-106">Crea un oggetto del trigger di metrica log di tipo ed è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="91eda-106">Creates an object of type Log Metric Trigger and is optional.</span></span>
<span data-ttu-id="91eda-107">Questa è la condizione di trigger per la regola di query metrica, da usare quando è necessario indicare il tipo di misura metrica di avviso.</span><span class="sxs-lookup"><span data-stu-id="91eda-107">This is the trigger condition for metric query rule, to be used when you need to state metric measurement type of alert.</span></span>

## <span data-ttu-id="91eda-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="91eda-108">EXAMPLES</span></span>

### <span data-ttu-id="91eda-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="91eda-109">Example 1</span></span>
```powershell
PS C:\> $metricTrigger = New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator "GreaterThan" -Threshold 5 -MetricTriggerType "Consecutive" -MetricColumn "Computer"
```

## <span data-ttu-id="91eda-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="91eda-110">PARAMETERS</span></span>

### <span data-ttu-id="91eda-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91eda-111">-DefaultProfile</span></span>
<span data-ttu-id="91eda-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="91eda-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91eda-113">-MetricColumn</span><span class="sxs-lookup"><span data-stu-id="91eda-113">-MetricColumn</span></span>
<span data-ttu-id="91eda-114">Colonna in cui viene aggregato il valore metrico</span><span class="sxs-lookup"><span data-stu-id="91eda-114">Column on which metric value is being aggregated</span></span>

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

### <span data-ttu-id="91eda-115">-MetricTriggerType</span><span class="sxs-lookup"><span data-stu-id="91eda-115">-MetricTriggerType</span></span>
<span data-ttu-id="91eda-116">Tipo di trigger Metric</span><span class="sxs-lookup"><span data-stu-id="91eda-116">The metric trigger type</span></span>

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

### <span data-ttu-id="91eda-117">-Soglia</span><span class="sxs-lookup"><span data-stu-id="91eda-117">-Threshold</span></span>
<span data-ttu-id="91eda-118">Valore soglia metrico</span><span class="sxs-lookup"><span data-stu-id="91eda-118">The metric threshold value</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91eda-119">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="91eda-119">-ThresholdOperator</span></span>
<span data-ttu-id="91eda-120">Operatore soglia metrica: GreaterThan, LessThan, uguale</span><span class="sxs-lookup"><span data-stu-id="91eda-120">The metric threshold operator : GreaterThan, LessThan, Equal</span></span>

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

### <span data-ttu-id="91eda-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91eda-121">CommonParameters</span></span>
<span data-ttu-id="91eda-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91eda-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91eda-123">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91eda-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91eda-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="91eda-124">INPUTS</span></span>

### <span data-ttu-id="91eda-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="91eda-125">None</span></span>

## <span data-ttu-id="91eda-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="91eda-126">OUTPUTS</span></span>

### <span data-ttu-id="91eda-127">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="91eda-127">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="91eda-128">Note</span><span class="sxs-lookup"><span data-stu-id="91eda-128">NOTES</span></span>

## <span data-ttu-id="91eda-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="91eda-129">RELATED LINKS</span></span>
