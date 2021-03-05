---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azscheduledqueryrulelogmetrictrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
ms.openlocfilehash: 0270c9bf6d543455772095a6d0fe3f0f1a55a416
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978429"
---
# <span data-ttu-id="ef4dd-101">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="ef4dd-101">New-AzScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="ef4dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef4dd-102">SYNOPSIS</span></span>
<span data-ttu-id="ef4dd-103">Crea un oggetto di tipo Trigger metrico log.</span><span class="sxs-lookup"><span data-stu-id="ef4dd-103">Creates an object of type Log Metric Trigger.</span></span>

## <span data-ttu-id="ef4dd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ef4dd-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator <String> -Threshold <Double>
 -MetricTriggerType <String> -MetricColumn <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ef4dd-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ef4dd-105">DESCRIPTION</span></span>
<span data-ttu-id="ef4dd-106">Crea un oggetto di tipo Trigger metrico log ed è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="ef4dd-106">Creates an object of type Log Metric Trigger and is optional.</span></span>
<span data-ttu-id="ef4dd-107">Questa è la condizione di attivazione per la regola della query metrica, da usare quando è necessario descrizione del tipo di misura metrica dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="ef4dd-107">This is the trigger condition for metric query rule, to be used when you need to state metric measurement type of alert.</span></span>

## <span data-ttu-id="ef4dd-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ef4dd-108">EXAMPLES</span></span>

### <span data-ttu-id="ef4dd-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ef4dd-109">Example 1</span></span>
```powershell
PS C:\> $metricTrigger = New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator "GreaterThan" -Threshold 5 -MetricTriggerType "Consecutive" -MetricColumn "Computer"
```

## <span data-ttu-id="ef4dd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef4dd-110">PARAMETERS</span></span>

### <span data-ttu-id="ef4dd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef4dd-111">-DefaultProfile</span></span>
<span data-ttu-id="ef4dd-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ef4dd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef4dd-113">-MetricColumn</span><span class="sxs-lookup"><span data-stu-id="ef4dd-113">-MetricColumn</span></span>
<span data-ttu-id="ef4dd-114">Colonna in cui viene aggregato il valore della metrica.</span><span class="sxs-lookup"><span data-stu-id="ef4dd-114">Column on which metric value is being aggregated.</span></span>
<span data-ttu-id="ef4dd-115">L'input non viene convalidato.</span><span class="sxs-lookup"><span data-stu-id="ef4dd-115">The input is not validated.</span></span> <span data-ttu-id="ef4dd-116">Verrà convalidato per la prima volta New-AzScheduledQueryRule chiamata.</span><span class="sxs-lookup"><span data-stu-id="ef4dd-116">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="ef4dd-117">-MetricTriggerType</span><span class="sxs-lookup"><span data-stu-id="ef4dd-117">-MetricTriggerType</span></span>
<span data-ttu-id="ef4dd-118">Tipo di trigger metrico.</span><span class="sxs-lookup"><span data-stu-id="ef4dd-118">The metric trigger type.</span></span>
<span data-ttu-id="ef4dd-119">L'input non viene convalidato.</span><span class="sxs-lookup"><span data-stu-id="ef4dd-119">The input is not validated.</span></span> <span data-ttu-id="ef4dd-120">Verrà convalidato per la prima volta New-AzScheduledQueryRule chiamata.</span><span class="sxs-lookup"><span data-stu-id="ef4dd-120">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="ef4dd-121">-Threshold</span><span class="sxs-lookup"><span data-stu-id="ef4dd-121">-Threshold</span></span>
<span data-ttu-id="ef4dd-122">Valore soglia metrico: Consecutivo, Totale.</span><span class="sxs-lookup"><span data-stu-id="ef4dd-122">The metric threshold value: Consecutive, Total.</span></span>
<span data-ttu-id="ef4dd-123">L'input non viene convalidato.</span><span class="sxs-lookup"><span data-stu-id="ef4dd-123">The input is not validated.</span></span> <span data-ttu-id="ef4dd-124">Verrà convalidato per la prima volta New-AzScheduledQueryRule chiamata.</span><span class="sxs-lookup"><span data-stu-id="ef4dd-124">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="ef4dd-125">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="ef4dd-125">-ThresholdOperator</span></span>
<span data-ttu-id="ef4dd-126">Operatore soglia metrica: GreaterThan, LessThan, Equal.</span><span class="sxs-lookup"><span data-stu-id="ef4dd-126">The metric threshold operator : GreaterThan, LessThan, Equal.</span></span>
<span data-ttu-id="ef4dd-127">L'input non viene convalidato.</span><span class="sxs-lookup"><span data-stu-id="ef4dd-127">The input is not validated.</span></span> <span data-ttu-id="ef4dd-128">Verrà convalidato per la prima volta New-AzScheduledQueryRule chiamata.</span><span class="sxs-lookup"><span data-stu-id="ef4dd-128">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="ef4dd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef4dd-129">CommonParameters</span></span>
<span data-ttu-id="ef4dd-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef4dd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef4dd-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ef4dd-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef4dd-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="ef4dd-132">INPUTS</span></span>

### <span data-ttu-id="ef4dd-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ef4dd-133">None</span></span>

## <span data-ttu-id="ef4dd-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ef4dd-134">OUTPUTS</span></span>

### <span data-ttu-id="ef4dd-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="ef4dd-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="ef4dd-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="ef4dd-136">NOTES</span></span>

## <span data-ttu-id="ef4dd-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ef4dd-137">RELATED LINKS</span></span>
