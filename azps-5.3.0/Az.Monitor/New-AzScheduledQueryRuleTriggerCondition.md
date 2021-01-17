---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruletriggercondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleTriggerCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleTriggerCondition.md
ms.openlocfilehash: 0fffbc11291fcf3cd7d3989e211bcbb0d202ea9b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475195"
---
# <span data-ttu-id="5fe38-101">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="5fe38-101">New-AzScheduledQueryRuleTriggerCondition</span></span>

## <span data-ttu-id="5fe38-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5fe38-102">SYNOPSIS</span></span>
<span data-ttu-id="5fe38-103">Crea un oggetto di tipo condizione trigger</span><span class="sxs-lookup"><span data-stu-id="5fe38-103">Creates an object of type Trigger Condition</span></span>

## <span data-ttu-id="5fe38-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5fe38-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleTriggerCondition -ThresholdOperator <String> -Threshold <Double>
 [-MetricTrigger <PSScheduledQueryRuleLogMetricTrigger>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5fe38-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5fe38-105">DESCRIPTION</span></span>
<span data-ttu-id="5fe38-106">Crea un oggetto di tipo Condition trigger.</span><span class="sxs-lookup"><span data-stu-id="5fe38-106">Creates an object of type Trigger Condition.</span></span>
<span data-ttu-id="5fe38-107">Questo oggetto deve essere passato al comando che crea l'oggetto azione di avviso</span><span class="sxs-lookup"><span data-stu-id="5fe38-107">This object is to be passed to the command that creates Alerting Action object</span></span>

## <span data-ttu-id="5fe38-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5fe38-108">EXAMPLES</span></span>

### <span data-ttu-id="5fe38-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5fe38-109">Example 1</span></span>
```powershell
PS C:\>  $triggerCondition = New-AzScheduledQueryRuleTriggerCondition -ThresholdOperator "GreaterThan" -Threshold 3 -MetricTrigger $metricTrigger
```

## <span data-ttu-id="5fe38-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5fe38-110">PARAMETERS</span></span>

### <span data-ttu-id="5fe38-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fe38-111">-DefaultProfile</span></span>
<span data-ttu-id="5fe38-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5fe38-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fe38-113">-MetricTrigger</span><span class="sxs-lookup"><span data-stu-id="5fe38-113">-MetricTrigger</span></span>
<span data-ttu-id="5fe38-114">Condizione trigger per la regola di query metrica</span><span class="sxs-lookup"><span data-stu-id="5fe38-114">Trigger condition for metric query rule</span></span>

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

### <span data-ttu-id="5fe38-115">-Soglia</span><span class="sxs-lookup"><span data-stu-id="5fe38-115">-Threshold</span></span>
<span data-ttu-id="5fe38-116">Soglia sopra la quale viene generato l'avviso</span><span class="sxs-lookup"><span data-stu-id="5fe38-116">The threshold above which alert gets fired</span></span>

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

### <span data-ttu-id="5fe38-117">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="5fe38-117">-ThresholdOperator</span></span>
<span data-ttu-id="5fe38-118">Operatore soglia: GreaterThan, LessThan o uguale</span><span class="sxs-lookup"><span data-stu-id="5fe38-118">The threshold operator : GreaterThan, LessThan or Equal</span></span>

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

### <span data-ttu-id="5fe38-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fe38-119">CommonParameters</span></span>
<span data-ttu-id="5fe38-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fe38-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fe38-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5fe38-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fe38-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5fe38-122">INPUTS</span></span>

### <span data-ttu-id="5fe38-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5fe38-123">None</span></span>

## <span data-ttu-id="5fe38-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5fe38-124">OUTPUTS</span></span>

### <span data-ttu-id="5fe38-125">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="5fe38-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleTriggerCondition</span></span>

## <span data-ttu-id="5fe38-126">Note</span><span class="sxs-lookup"><span data-stu-id="5fe38-126">NOTES</span></span>

## <span data-ttu-id="5fe38-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5fe38-127">RELATED LINKS</span></span>
