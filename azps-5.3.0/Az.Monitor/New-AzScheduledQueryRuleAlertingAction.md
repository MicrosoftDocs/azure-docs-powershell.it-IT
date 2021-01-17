---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulealertingaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
ms.openlocfilehash: 41ce3c066651cb2bc6ea13ddd0a7a3bb15d28879
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486840"
---
# <span data-ttu-id="3900e-101">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="3900e-101">New-AzScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="3900e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3900e-102">SYNOPSIS</span></span>
<span data-ttu-id="3900e-103">Crea un oggetto di tipo azione di avviso</span><span class="sxs-lookup"><span data-stu-id="3900e-103">Creates an object of type Alerting Action</span></span>

## <span data-ttu-id="3900e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3900e-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAlertingAction [-AznsAction <PSScheduledQueryRuleAznsAction>] -Severity <String>
 [-ThrottlingInMinutes <Int32>] -Trigger <PSScheduledQueryRuleTriggerCondition>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3900e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3900e-105">DESCRIPTION</span></span>
<span data-ttu-id="3900e-106">Crea un oggetto di tipo Action Alerting questo oggetto deve essere passato al comando che crea la regola di avviso del log</span><span class="sxs-lookup"><span data-stu-id="3900e-106">Creates an object of type Alerting Action This object is to be passed to the command that creates Log Alert Rule</span></span>

## <span data-ttu-id="3900e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3900e-107">EXAMPLES</span></span>

### <span data-ttu-id="3900e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3900e-108">Example 1</span></span>
```powershell
PS C:\> $alertingAction = New-AzScheduledQueryRuleAlertingAction -AznsAction $aznsActionGroup -Severity "1" -Trigger $triggerCondition
```

## <span data-ttu-id="3900e-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3900e-109">PARAMETERS</span></span>

### <span data-ttu-id="3900e-110">-AznsAction</span><span class="sxs-lookup"><span data-stu-id="3900e-110">-AznsAction</span></span>
<span data-ttu-id="3900e-111">Dettagli dell'azione AzNS</span><span class="sxs-lookup"><span data-stu-id="3900e-111">The AzNS action details</span></span>

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

### <span data-ttu-id="3900e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3900e-112">-DefaultProfile</span></span>
<span data-ttu-id="3900e-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3900e-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3900e-114">-Gravità</span><span class="sxs-lookup"><span data-stu-id="3900e-114">-Severity</span></span>
<span data-ttu-id="3900e-115">Gravità per l'avviso</span><span class="sxs-lookup"><span data-stu-id="3900e-115">The severity for this alert</span></span>

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

### <span data-ttu-id="3900e-116">-ThrottlingInMinutes</span><span class="sxs-lookup"><span data-stu-id="3900e-116">-ThrottlingInMinutes</span></span>
<span data-ttu-id="3900e-117">Durata in minuti per cui deve essere strozzata l'allerta</span><span class="sxs-lookup"><span data-stu-id="3900e-117">The duration in minutes for which alert should be throttled</span></span>

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

### <span data-ttu-id="3900e-118">-Trigger</span><span class="sxs-lookup"><span data-stu-id="3900e-118">-Trigger</span></span>
<span data-ttu-id="3900e-119">Condizione del trigger di avviso</span><span class="sxs-lookup"><span data-stu-id="3900e-119">The alert trigger condition</span></span>

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

### <span data-ttu-id="3900e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3900e-120">CommonParameters</span></span>
<span data-ttu-id="3900e-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3900e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3900e-122">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3900e-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3900e-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3900e-123">INPUTS</span></span>

### <span data-ttu-id="3900e-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3900e-124">None</span></span>

## <span data-ttu-id="3900e-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3900e-125">OUTPUTS</span></span>

### <span data-ttu-id="3900e-126">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="3900e-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="3900e-127">Note</span><span class="sxs-lookup"><span data-stu-id="3900e-127">NOTES</span></span>

## <span data-ttu-id="3900e-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3900e-128">RELATED LINKS</span></span>
