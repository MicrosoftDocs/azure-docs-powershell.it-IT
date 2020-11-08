---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruletriggercondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleTriggerCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleTriggerCondition.md
ms.openlocfilehash: 0fffbc11291fcf3cd7d3989e211bcbb0d202ea9b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203383"
---
# <span data-ttu-id="a5066-101">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="a5066-101">New-AzScheduledQueryRuleTriggerCondition</span></span>

## <span data-ttu-id="a5066-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a5066-102">SYNOPSIS</span></span>
<span data-ttu-id="a5066-103">Crea un oggetto di tipo condizione trigger</span><span class="sxs-lookup"><span data-stu-id="a5066-103">Creates an object of type Trigger Condition</span></span>

## <span data-ttu-id="a5066-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a5066-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleTriggerCondition -ThresholdOperator <String> -Threshold <Double>
 [-MetricTrigger <PSScheduledQueryRuleLogMetricTrigger>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a5066-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a5066-105">DESCRIPTION</span></span>
<span data-ttu-id="a5066-106">Crea un oggetto di tipo Condition trigger.</span><span class="sxs-lookup"><span data-stu-id="a5066-106">Creates an object of type Trigger Condition.</span></span>
<span data-ttu-id="a5066-107">Questo oggetto deve essere passato al comando che crea l'oggetto azione di avviso</span><span class="sxs-lookup"><span data-stu-id="a5066-107">This object is to be passed to the command that creates Alerting Action object</span></span>

## <span data-ttu-id="a5066-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a5066-108">EXAMPLES</span></span>

### <span data-ttu-id="a5066-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a5066-109">Example 1</span></span>
```powershell
PS C:\>  $triggerCondition = New-AzScheduledQueryRuleTriggerCondition -ThresholdOperator "GreaterThan" -Threshold 3 -MetricTrigger $metricTrigger
```

## <span data-ttu-id="a5066-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a5066-110">PARAMETERS</span></span>

### <span data-ttu-id="a5066-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5066-111">-DefaultProfile</span></span>
<span data-ttu-id="a5066-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a5066-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5066-113">-MetricTrigger</span><span class="sxs-lookup"><span data-stu-id="a5066-113">-MetricTrigger</span></span>
<span data-ttu-id="a5066-114">Condizione trigger per la regola di query metrica</span><span class="sxs-lookup"><span data-stu-id="a5066-114">Trigger condition for metric query rule</span></span>

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

### <span data-ttu-id="a5066-115">-Soglia</span><span class="sxs-lookup"><span data-stu-id="a5066-115">-Threshold</span></span>
<span data-ttu-id="a5066-116">Soglia sopra la quale viene generato l'avviso</span><span class="sxs-lookup"><span data-stu-id="a5066-116">The threshold above which alert gets fired</span></span>

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

### <span data-ttu-id="a5066-117">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="a5066-117">-ThresholdOperator</span></span>
<span data-ttu-id="a5066-118">Operatore soglia: GreaterThan, LessThan o uguale</span><span class="sxs-lookup"><span data-stu-id="a5066-118">The threshold operator : GreaterThan, LessThan or Equal</span></span>

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

### <span data-ttu-id="a5066-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5066-119">CommonParameters</span></span>
<span data-ttu-id="a5066-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5066-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5066-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5066-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5066-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a5066-122">INPUTS</span></span>

### <span data-ttu-id="a5066-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a5066-123">None</span></span>

## <span data-ttu-id="a5066-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a5066-124">OUTPUTS</span></span>

### <span data-ttu-id="a5066-125">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="a5066-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleTriggerCondition</span></span>

## <span data-ttu-id="a5066-126">Note</span><span class="sxs-lookup"><span data-stu-id="a5066-126">NOTES</span></span>

## <span data-ttu-id="a5066-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a5066-127">RELATED LINKS</span></span>
