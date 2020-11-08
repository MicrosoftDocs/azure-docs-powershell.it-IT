---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulelogmetrictrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
ms.openlocfilehash: c4d44f266a9966f605e009cc4ce5dece0fa5e2ae
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189757"
---
# <span data-ttu-id="61e98-101">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="61e98-101">New-AzScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="61e98-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="61e98-102">SYNOPSIS</span></span>
<span data-ttu-id="61e98-103">Crea un oggetto del trigger di metrica log di tipo.</span><span class="sxs-lookup"><span data-stu-id="61e98-103">Creates an object of type Log Metric Trigger.</span></span>

## <span data-ttu-id="61e98-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="61e98-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator <String> -Threshold <Double>
 -MetricTriggerType <String> -MetricColumn <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="61e98-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61e98-105">DESCRIPTION</span></span>
<span data-ttu-id="61e98-106">Crea un oggetto del trigger di metrica log di tipo ed è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="61e98-106">Creates an object of type Log Metric Trigger and is optional.</span></span>
<span data-ttu-id="61e98-107">Questa è la condizione di trigger per la regola di query metrica, da usare quando è necessario indicare il tipo di misura metrica di avviso.</span><span class="sxs-lookup"><span data-stu-id="61e98-107">This is the trigger condition for metric query rule, to be used when you need to state metric measurement type of alert.</span></span>

## <span data-ttu-id="61e98-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="61e98-108">EXAMPLES</span></span>

### <span data-ttu-id="61e98-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="61e98-109">Example 1</span></span>
```powershell
PS C:\> $metricTrigger = New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator "GreaterThan" -Threshold 5 -MetricTriggerType "Consecutive" -MetricColumn "Computer"
```

## <span data-ttu-id="61e98-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="61e98-110">PARAMETERS</span></span>

### <span data-ttu-id="61e98-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61e98-111">-DefaultProfile</span></span>
<span data-ttu-id="61e98-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="61e98-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61e98-113">-MetricColumn</span><span class="sxs-lookup"><span data-stu-id="61e98-113">-MetricColumn</span></span>
<span data-ttu-id="61e98-114">Colonna in cui viene aggregato il valore Metric.</span><span class="sxs-lookup"><span data-stu-id="61e98-114">Column on which metric value is being aggregated.</span></span>
<span data-ttu-id="61e98-115">L'input non viene convalidato.</span><span class="sxs-lookup"><span data-stu-id="61e98-115">The input is not validated.</span></span> <span data-ttu-id="61e98-116">Verrà prima convalidato quando viene chiamato New-AzScheduledQueryRule.</span><span class="sxs-lookup"><span data-stu-id="61e98-116">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="61e98-117">-MetricTriggerType</span><span class="sxs-lookup"><span data-stu-id="61e98-117">-MetricTriggerType</span></span>
<span data-ttu-id="61e98-118">Il tipo di trigger Metric.</span><span class="sxs-lookup"><span data-stu-id="61e98-118">The metric trigger type.</span></span>
<span data-ttu-id="61e98-119">L'input non viene convalidato.</span><span class="sxs-lookup"><span data-stu-id="61e98-119">The input is not validated.</span></span> <span data-ttu-id="61e98-120">Verrà prima convalidato quando viene chiamato New-AzScheduledQueryRule.</span><span class="sxs-lookup"><span data-stu-id="61e98-120">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="61e98-121">-Soglia</span><span class="sxs-lookup"><span data-stu-id="61e98-121">-Threshold</span></span>
<span data-ttu-id="61e98-122">Valore di soglia metrico: consecutivo, totale.</span><span class="sxs-lookup"><span data-stu-id="61e98-122">The metric threshold value: Consecutive, Total.</span></span>
<span data-ttu-id="61e98-123">L'input non viene convalidato.</span><span class="sxs-lookup"><span data-stu-id="61e98-123">The input is not validated.</span></span> <span data-ttu-id="61e98-124">Verrà prima convalidato quando viene chiamato New-AzScheduledQueryRule.</span><span class="sxs-lookup"><span data-stu-id="61e98-124">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="61e98-125">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="61e98-125">-ThresholdOperator</span></span>
<span data-ttu-id="61e98-126">Operatore soglia metrica: GreaterThan, LessThan, EQUAL.</span><span class="sxs-lookup"><span data-stu-id="61e98-126">The metric threshold operator : GreaterThan, LessThan, Equal.</span></span>
<span data-ttu-id="61e98-127">L'input non viene convalidato.</span><span class="sxs-lookup"><span data-stu-id="61e98-127">The input is not validated.</span></span> <span data-ttu-id="61e98-128">Verrà prima convalidato quando viene chiamato New-AzScheduledQueryRule.</span><span class="sxs-lookup"><span data-stu-id="61e98-128">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="61e98-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61e98-129">CommonParameters</span></span>
<span data-ttu-id="61e98-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61e98-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61e98-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61e98-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61e98-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="61e98-132">INPUTS</span></span>

### <span data-ttu-id="61e98-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="61e98-133">None</span></span>

## <span data-ttu-id="61e98-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="61e98-134">OUTPUTS</span></span>

### <span data-ttu-id="61e98-135">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="61e98-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="61e98-136">Note</span><span class="sxs-lookup"><span data-stu-id="61e98-136">NOTES</span></span>

## <span data-ttu-id="61e98-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="61e98-137">RELATED LINKS</span></span>
