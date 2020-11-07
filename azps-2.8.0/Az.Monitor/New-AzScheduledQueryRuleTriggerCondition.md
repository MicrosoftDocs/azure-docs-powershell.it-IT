---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruletriggercondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleTriggerCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleTriggerCondition.md
ms.openlocfilehash: ccc81854cf2f1075a6973fa8ed4685faba713a2f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854050"
---
# <span data-ttu-id="03636-101">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="03636-101">New-AzScheduledQueryRuleTriggerCondition</span></span>

## <span data-ttu-id="03636-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="03636-102">SYNOPSIS</span></span>
<span data-ttu-id="03636-103">Crea un oggetto di tipo condizione trigger</span><span class="sxs-lookup"><span data-stu-id="03636-103">Creates an object of type Trigger Condition</span></span>

## <span data-ttu-id="03636-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="03636-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleTriggerCondition -ThresholdOperator <String> -Threshold <Double>
 [-MetricTrigger <PSScheduledQueryRuleLogMetricTrigger>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="03636-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="03636-105">DESCRIPTION</span></span>
<span data-ttu-id="03636-106">Crea un oggetto di tipo Condition trigger.</span><span class="sxs-lookup"><span data-stu-id="03636-106">Creates an object of type Trigger Condition.</span></span>
<span data-ttu-id="03636-107">Questo oggetto deve essere passato al comando che crea l'oggetto azione di avviso</span><span class="sxs-lookup"><span data-stu-id="03636-107">This object is to be passed to the command that creates Alerting Action object</span></span>

## <span data-ttu-id="03636-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="03636-108">EXAMPLES</span></span>

### <span data-ttu-id="03636-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="03636-109">Example 1</span></span>
```powershell
PS C:\>  $triggerCondition = New-AzScheduledQueryRuleTriggerCondition -ThresholdOperator "GreaterThan" -Threshold 3 -MetricTrigger $metricTrigger
```

## <span data-ttu-id="03636-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="03636-110">PARAMETERS</span></span>

### <span data-ttu-id="03636-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03636-111">-DefaultProfile</span></span>
<span data-ttu-id="03636-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="03636-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03636-113">-MetricTrigger</span><span class="sxs-lookup"><span data-stu-id="03636-113">-MetricTrigger</span></span>
<span data-ttu-id="03636-114">Condizione trigger per la regola di query metrica</span><span class="sxs-lookup"><span data-stu-id="03636-114">Trigger condition for metric query rule</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03636-115">-Soglia</span><span class="sxs-lookup"><span data-stu-id="03636-115">-Threshold</span></span>
<span data-ttu-id="03636-116">Soglia sopra la quale viene generato l'avviso</span><span class="sxs-lookup"><span data-stu-id="03636-116">The threshold above which alert gets fired</span></span>

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

### <span data-ttu-id="03636-117">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="03636-117">-ThresholdOperator</span></span>
<span data-ttu-id="03636-118">Operatore soglia: GreaterThan, LessThan o uguale</span><span class="sxs-lookup"><span data-stu-id="03636-118">The threshold operator : GreaterThan, LessThan or Equal</span></span>

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

### <span data-ttu-id="03636-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03636-119">CommonParameters</span></span>
<span data-ttu-id="03636-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03636-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03636-121">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="03636-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03636-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="03636-122">INPUTS</span></span>

### <span data-ttu-id="03636-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="03636-123">None</span></span>

## <span data-ttu-id="03636-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="03636-124">OUTPUTS</span></span>

### <span data-ttu-id="03636-125">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="03636-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleTriggerCondition</span></span>

## <span data-ttu-id="03636-126">Note</span><span class="sxs-lookup"><span data-stu-id="03636-126">NOTES</span></span>

## <span data-ttu-id="03636-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="03636-127">RELATED LINKS</span></span>
