---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulelogmetrictrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
ms.openlocfilehash: c4d44f266a9966f605e009cc4ce5dece0fa5e2ae
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187390"
---
# <span data-ttu-id="50afe-101">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="50afe-101">New-AzScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="50afe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50afe-102">SYNOPSIS</span></span>
<span data-ttu-id="50afe-103">Crea un oggetto di tipo Trigger metrico log.</span><span class="sxs-lookup"><span data-stu-id="50afe-103">Creates an object of type Log Metric Trigger.</span></span>

## <span data-ttu-id="50afe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="50afe-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator <String> -Threshold <Double>
 -MetricTriggerType <String> -MetricColumn <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="50afe-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="50afe-105">DESCRIPTION</span></span>
<span data-ttu-id="50afe-106">Crea un oggetto di tipo Trigger metrico log ed è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="50afe-106">Creates an object of type Log Metric Trigger and is optional.</span></span>
<span data-ttu-id="50afe-107">Questa è la condizione di attivazione per la regola di query metrica, da usare quando è necessario descrizione del tipo di misura metrica dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="50afe-107">This is the trigger condition for metric query rule, to be used when you need to state metric measurement type of alert.</span></span>

## <span data-ttu-id="50afe-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="50afe-108">EXAMPLES</span></span>

### <span data-ttu-id="50afe-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="50afe-109">Example 1</span></span>
```powershell
PS C:\> $metricTrigger = New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator "GreaterThan" -Threshold 5 -MetricTriggerType "Consecutive" -MetricColumn "Computer"
```

## <span data-ttu-id="50afe-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50afe-110">PARAMETERS</span></span>

### <span data-ttu-id="50afe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50afe-111">-DefaultProfile</span></span>
<span data-ttu-id="50afe-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="50afe-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50afe-113">-MetricColumn</span><span class="sxs-lookup"><span data-stu-id="50afe-113">-MetricColumn</span></span>
<span data-ttu-id="50afe-114">Colonna in cui viene aggregato il valore della metrica.</span><span class="sxs-lookup"><span data-stu-id="50afe-114">Column on which metric value is being aggregated.</span></span>
<span data-ttu-id="50afe-115">L'input non viene convalidato.</span><span class="sxs-lookup"><span data-stu-id="50afe-115">The input is not validated.</span></span> <span data-ttu-id="50afe-116">Verrà convalidato per la prima volta New-AzScheduledQueryRule chiamata.</span><span class="sxs-lookup"><span data-stu-id="50afe-116">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="50afe-117">-MetricTriggerType</span><span class="sxs-lookup"><span data-stu-id="50afe-117">-MetricTriggerType</span></span>
<span data-ttu-id="50afe-118">Tipo di trigger metrico.</span><span class="sxs-lookup"><span data-stu-id="50afe-118">The metric trigger type.</span></span>
<span data-ttu-id="50afe-119">L'input non viene convalidato.</span><span class="sxs-lookup"><span data-stu-id="50afe-119">The input is not validated.</span></span> <span data-ttu-id="50afe-120">Verrà convalidato per la prima volta New-AzScheduledQueryRule chiamata.</span><span class="sxs-lookup"><span data-stu-id="50afe-120">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="50afe-121">-Threshold</span><span class="sxs-lookup"><span data-stu-id="50afe-121">-Threshold</span></span>
<span data-ttu-id="50afe-122">Valore soglia metrico: Consecutivo, Totale.</span><span class="sxs-lookup"><span data-stu-id="50afe-122">The metric threshold value: Consecutive, Total.</span></span>
<span data-ttu-id="50afe-123">L'input non viene convalidato.</span><span class="sxs-lookup"><span data-stu-id="50afe-123">The input is not validated.</span></span> <span data-ttu-id="50afe-124">Verrà convalidato per la prima volta New-AzScheduledQueryRule chiamata.</span><span class="sxs-lookup"><span data-stu-id="50afe-124">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="50afe-125">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="50afe-125">-ThresholdOperator</span></span>
<span data-ttu-id="50afe-126">Operatore soglia metrica: GreaterThan, LessThan, Equal.</span><span class="sxs-lookup"><span data-stu-id="50afe-126">The metric threshold operator : GreaterThan, LessThan, Equal.</span></span>
<span data-ttu-id="50afe-127">L'input non viene convalidato.</span><span class="sxs-lookup"><span data-stu-id="50afe-127">The input is not validated.</span></span> <span data-ttu-id="50afe-128">Verrà convalidato per la prima volta New-AzScheduledQueryRule chiamata.</span><span class="sxs-lookup"><span data-stu-id="50afe-128">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="50afe-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50afe-129">CommonParameters</span></span>
<span data-ttu-id="50afe-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50afe-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50afe-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="50afe-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50afe-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="50afe-132">INPUTS</span></span>

### <span data-ttu-id="50afe-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="50afe-133">None</span></span>

## <span data-ttu-id="50afe-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="50afe-134">OUTPUTS</span></span>

### <span data-ttu-id="50afe-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="50afe-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="50afe-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="50afe-136">NOTES</span></span>

## <span data-ttu-id="50afe-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="50afe-137">RELATED LINKS</span></span>
