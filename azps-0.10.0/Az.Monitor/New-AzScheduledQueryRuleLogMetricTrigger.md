---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulelogmetrictrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
ms.openlocfilehash: c5fb336d7ba105469506bb0a80a5b69036e5474b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861117"
---
# <span data-ttu-id="4faa3-101">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="4faa3-101">New-AzScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="4faa3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4faa3-102">SYNOPSIS</span></span>
<span data-ttu-id="4faa3-103">Crea un oggetto di trigger metrica log di tipo</span><span class="sxs-lookup"><span data-stu-id="4faa3-103">Creates an object of type Log Metric Trigger</span></span>

## <span data-ttu-id="4faa3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4faa3-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator <String> -Threshold <Double>
 -MetricTriggerType <String> -MetricColumn <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4faa3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4faa3-105">DESCRIPTION</span></span>
<span data-ttu-id="4faa3-106">Crea un oggetto del trigger di metrica log di tipo ed è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="4faa3-106">Creates an object of type Log Metric Trigger and is optional.</span></span>
<span data-ttu-id="4faa3-107">Questa è la condizione di trigger per la regola di query metrica, da usare quando è necessario indicare il tipo di misura metrica di avviso.</span><span class="sxs-lookup"><span data-stu-id="4faa3-107">This is the trigger condition for metric query rule, to be used when you need to state metric measurement type of alert.</span></span>

## <span data-ttu-id="4faa3-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4faa3-108">EXAMPLES</span></span>

### <span data-ttu-id="4faa3-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4faa3-109">Example 1</span></span>
```powershell
PS C:\> $metricTrigger = New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator "GreaterThan" -Threshold 5 -MetricTriggerType "Consecutive" -MetricColumn "Computer"
```

## <span data-ttu-id="4faa3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4faa3-110">PARAMETERS</span></span>

### <span data-ttu-id="4faa3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4faa3-111">-DefaultProfile</span></span>
<span data-ttu-id="4faa3-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4faa3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4faa3-113">-MetricColumn</span><span class="sxs-lookup"><span data-stu-id="4faa3-113">-MetricColumn</span></span>
<span data-ttu-id="4faa3-114">Colonna in cui viene aggregato il valore metrico</span><span class="sxs-lookup"><span data-stu-id="4faa3-114">Column on which metric value is being aggregated</span></span>

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

### <span data-ttu-id="4faa3-115">-MetricTriggerType</span><span class="sxs-lookup"><span data-stu-id="4faa3-115">-MetricTriggerType</span></span>
<span data-ttu-id="4faa3-116">Tipo di trigger Metric</span><span class="sxs-lookup"><span data-stu-id="4faa3-116">The metric trigger type</span></span>

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

### <span data-ttu-id="4faa3-117">-Soglia</span><span class="sxs-lookup"><span data-stu-id="4faa3-117">-Threshold</span></span>
<span data-ttu-id="4faa3-118">Valore soglia metrico</span><span class="sxs-lookup"><span data-stu-id="4faa3-118">The metric threshold value</span></span>

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

### <span data-ttu-id="4faa3-119">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="4faa3-119">-ThresholdOperator</span></span>
<span data-ttu-id="4faa3-120">Operatore soglia metrica: GreaterThan, LessThan, uguale</span><span class="sxs-lookup"><span data-stu-id="4faa3-120">The metric threshold operator : GreaterThan, LessThan, Equal</span></span>

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

### <span data-ttu-id="4faa3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4faa3-121">CommonParameters</span></span>
<span data-ttu-id="4faa3-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4faa3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4faa3-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4faa3-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4faa3-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4faa3-124">INPUTS</span></span>

### <span data-ttu-id="4faa3-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4faa3-125">None</span></span>

## <span data-ttu-id="4faa3-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4faa3-126">OUTPUTS</span></span>

### <span data-ttu-id="4faa3-127">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="4faa3-127">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="4faa3-128">Note</span><span class="sxs-lookup"><span data-stu-id="4faa3-128">NOTES</span></span>

## <span data-ttu-id="4faa3-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4faa3-129">RELATED LINKS</span></span>
