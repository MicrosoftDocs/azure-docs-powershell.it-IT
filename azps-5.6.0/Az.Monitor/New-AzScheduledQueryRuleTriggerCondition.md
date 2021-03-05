---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azscheduledqueryruletriggercondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleTriggerCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleTriggerCondition.md
ms.openlocfilehash: 1fcafb0eb9e4bd1cfb0cf5b3f5ec770c35ea92d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996588"
---
# <span data-ttu-id="de40a-101">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="de40a-101">New-AzScheduledQueryRuleTriggerCondition</span></span>

## <span data-ttu-id="de40a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de40a-102">SYNOPSIS</span></span>
<span data-ttu-id="de40a-103">Crea un oggetto di tipo Condizione di attivazione</span><span class="sxs-lookup"><span data-stu-id="de40a-103">Creates an object of type Trigger Condition</span></span>

## <span data-ttu-id="de40a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="de40a-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleTriggerCondition -ThresholdOperator <String> -Threshold <Double>
 [-MetricTrigger <PSScheduledQueryRuleLogMetricTrigger>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="de40a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="de40a-105">DESCRIPTION</span></span>
<span data-ttu-id="de40a-106">Crea un oggetto di tipo Condizione di attivazione.</span><span class="sxs-lookup"><span data-stu-id="de40a-106">Creates an object of type Trigger Condition.</span></span>
<span data-ttu-id="de40a-107">Questo oggetto deve essere passato al comando che crea l'oggetto Azione avviso</span><span class="sxs-lookup"><span data-stu-id="de40a-107">This object is to be passed to the command that creates Alerting Action object</span></span>

## <span data-ttu-id="de40a-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="de40a-108">EXAMPLES</span></span>

### <span data-ttu-id="de40a-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="de40a-109">Example 1</span></span>
```powershell
PS C:\>  $triggerCondition = New-AzScheduledQueryRuleTriggerCondition -ThresholdOperator "GreaterThan" -Threshold 3 -MetricTrigger $metricTrigger
```

## <span data-ttu-id="de40a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de40a-110">PARAMETERS</span></span>

### <span data-ttu-id="de40a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de40a-111">-DefaultProfile</span></span>
<span data-ttu-id="de40a-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="de40a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de40a-113">-MetricTrigger</span><span class="sxs-lookup"><span data-stu-id="de40a-113">-MetricTrigger</span></span>
<span data-ttu-id="de40a-114">Condizione di attivazione per una regola di query metrica</span><span class="sxs-lookup"><span data-stu-id="de40a-114">Trigger condition for metric query rule</span></span>

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

### <span data-ttu-id="de40a-115">-Threshold</span><span class="sxs-lookup"><span data-stu-id="de40a-115">-Threshold</span></span>
<span data-ttu-id="de40a-116">Soglia superiore alla soglia di visualizzazione dell'avviso</span><span class="sxs-lookup"><span data-stu-id="de40a-116">The threshold above which alert gets fired</span></span>

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

### <span data-ttu-id="de40a-117">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="de40a-117">-ThresholdOperator</span></span>
<span data-ttu-id="de40a-118">Operatore soglia: GreaterThan, LessThan o Equal</span><span class="sxs-lookup"><span data-stu-id="de40a-118">The threshold operator : GreaterThan, LessThan or Equal</span></span>

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

### <span data-ttu-id="de40a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de40a-119">CommonParameters</span></span>
<span data-ttu-id="de40a-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de40a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de40a-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="de40a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de40a-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="de40a-122">INPUTS</span></span>

### <span data-ttu-id="de40a-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="de40a-123">None</span></span>

## <span data-ttu-id="de40a-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="de40a-124">OUTPUTS</span></span>

### <span data-ttu-id="de40a-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="de40a-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleTriggerCondition</span></span>

## <span data-ttu-id="de40a-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="de40a-126">NOTES</span></span>

## <span data-ttu-id="de40a-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="de40a-127">RELATED LINKS</span></span>
