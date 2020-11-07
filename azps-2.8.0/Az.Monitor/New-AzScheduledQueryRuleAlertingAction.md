---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulealertingaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
ms.openlocfilehash: 382aa35b9967e016ce87da982b32c97148c9f3c5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854074"
---
# <span data-ttu-id="f4a66-101">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="f4a66-101">New-AzScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="f4a66-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f4a66-102">SYNOPSIS</span></span>
<span data-ttu-id="f4a66-103">Crea un oggetto di tipo azione di avviso</span><span class="sxs-lookup"><span data-stu-id="f4a66-103">Creates an object of type Alerting Action</span></span>

## <span data-ttu-id="f4a66-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f4a66-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAlertingAction [-AznsAction <PSScheduledQueryRuleAznsAction>] -Severity <String>
 [-ThrottlingInMinutes <Int32>] -Trigger <PSScheduledQueryRuleTriggerCondition>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4a66-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4a66-105">DESCRIPTION</span></span>
<span data-ttu-id="f4a66-106">Crea un oggetto di tipo Action Alerting questo oggetto deve essere passato al comando che crea la regola di avviso del log</span><span class="sxs-lookup"><span data-stu-id="f4a66-106">Creates an object of type Alerting Action This object is to be passed to the command that creates Log Alert Rule</span></span>

## <span data-ttu-id="f4a66-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f4a66-107">EXAMPLES</span></span>

### <span data-ttu-id="f4a66-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f4a66-108">Example 1</span></span>
```powershell
PS C:\> $alertingAction = New-AzScheduledQueryRuleAlertingAction -AznsAction $aznsActionGroup -Severity "1" -Trigger $triggerCondition
```

## <span data-ttu-id="f4a66-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f4a66-109">PARAMETERS</span></span>

### <span data-ttu-id="f4a66-110">-AznsAction</span><span class="sxs-lookup"><span data-stu-id="f4a66-110">-AznsAction</span></span>
<span data-ttu-id="f4a66-111">Dettagli dell'azione AzNS</span><span class="sxs-lookup"><span data-stu-id="f4a66-111">The AzNS action details</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4a66-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4a66-112">-DefaultProfile</span></span>
<span data-ttu-id="f4a66-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f4a66-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4a66-114">-Gravità</span><span class="sxs-lookup"><span data-stu-id="f4a66-114">-Severity</span></span>
<span data-ttu-id="f4a66-115">Gravità per l'avviso</span><span class="sxs-lookup"><span data-stu-id="f4a66-115">The severity for this alert</span></span>

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

### <span data-ttu-id="f4a66-116">-ThrottlingInMinutes</span><span class="sxs-lookup"><span data-stu-id="f4a66-116">-ThrottlingInMinutes</span></span>
<span data-ttu-id="f4a66-117">Durata in minuti per cui deve essere strozzata l'allerta</span><span class="sxs-lookup"><span data-stu-id="f4a66-117">The duration in minutes for which alert should be throttled</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4a66-118">-Trigger</span><span class="sxs-lookup"><span data-stu-id="f4a66-118">-Trigger</span></span>
<span data-ttu-id="f4a66-119">Condizione del trigger di avviso</span><span class="sxs-lookup"><span data-stu-id="f4a66-119">The alert trigger condition</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleTriggerCondition
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4a66-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4a66-120">CommonParameters</span></span>
<span data-ttu-id="f4a66-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4a66-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4a66-122">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f4a66-122">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4a66-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f4a66-123">INPUTS</span></span>

### <span data-ttu-id="f4a66-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f4a66-124">None</span></span>

## <span data-ttu-id="f4a66-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f4a66-125">OUTPUTS</span></span>

### <span data-ttu-id="f4a66-126">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="f4a66-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="f4a66-127">Note</span><span class="sxs-lookup"><span data-stu-id="f4a66-127">NOTES</span></span>

## <span data-ttu-id="f4a66-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f4a66-128">RELATED LINKS</span></span>
