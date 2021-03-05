---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azscheduledqueryrulealertingaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
ms.openlocfilehash: 0394aa7c2db880bbb10c8d68c9d502560c1035bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961806"
---
# <span data-ttu-id="1a81d-101">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="1a81d-101">New-AzScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="1a81d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a81d-102">SYNOPSIS</span></span>
<span data-ttu-id="1a81d-103">Crea un oggetto di tipo Azione avviso</span><span class="sxs-lookup"><span data-stu-id="1a81d-103">Creates an object of type Alerting Action</span></span>

## <span data-ttu-id="1a81d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1a81d-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAlertingAction [-AznsAction <PSScheduledQueryRuleAznsAction>] -Severity <String>
 [-ThrottlingInMinutes <Int32>] -Trigger <PSScheduledQueryRuleTriggerCondition>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a81d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1a81d-105">DESCRIPTION</span></span>
<span data-ttu-id="1a81d-106">Crea un oggetto di tipo Azione avviso Questo oggetto deve essere passato al comando che crea la regola di avviso</span><span class="sxs-lookup"><span data-stu-id="1a81d-106">Creates an object of type Alerting Action This object is to be passed to the command that creates Log Alert Rule</span></span>

## <span data-ttu-id="1a81d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1a81d-107">EXAMPLES</span></span>

### <span data-ttu-id="1a81d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1a81d-108">Example 1</span></span>
```powershell
PS C:\> $alertingAction = New-AzScheduledQueryRuleAlertingAction -AznsAction $aznsActionGroup -Severity "1" -Trigger $triggerCondition
```

## <span data-ttu-id="1a81d-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a81d-109">PARAMETERS</span></span>

### <span data-ttu-id="1a81d-110">-AznsAction</span><span class="sxs-lookup"><span data-stu-id="1a81d-110">-AznsAction</span></span>
<span data-ttu-id="1a81d-111">Dettagli dell'azione AzNS</span><span class="sxs-lookup"><span data-stu-id="1a81d-111">The AzNS action details</span></span>

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

### <span data-ttu-id="1a81d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a81d-112">-DefaultProfile</span></span>
<span data-ttu-id="1a81d-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1a81d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a81d-114">-Gravità</span><span class="sxs-lookup"><span data-stu-id="1a81d-114">-Severity</span></span>
<span data-ttu-id="1a81d-115">Gravità dell'avviso</span><span class="sxs-lookup"><span data-stu-id="1a81d-115">The severity for this alert</span></span>

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

### <span data-ttu-id="1a81d-116">-ThrottlingInMinutes</span><span class="sxs-lookup"><span data-stu-id="1a81d-116">-ThrottlingInMinutes</span></span>
<span data-ttu-id="1a81d-117">La durata in minuti per cui deve essere limitato l'avviso</span><span class="sxs-lookup"><span data-stu-id="1a81d-117">The duration in minutes for which alert should be throttled</span></span>

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

### <span data-ttu-id="1a81d-118">-Trigger</span><span class="sxs-lookup"><span data-stu-id="1a81d-118">-Trigger</span></span>
<span data-ttu-id="1a81d-119">Condizione di attivazione dell'avviso</span><span class="sxs-lookup"><span data-stu-id="1a81d-119">The alert trigger condition</span></span>

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

### <span data-ttu-id="1a81d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a81d-120">CommonParameters</span></span>
<span data-ttu-id="1a81d-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a81d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a81d-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1a81d-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a81d-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="1a81d-123">INPUTS</span></span>

### <span data-ttu-id="1a81d-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1a81d-124">None</span></span>

## <span data-ttu-id="1a81d-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1a81d-125">OUTPUTS</span></span>

### <span data-ttu-id="1a81d-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="1a81d-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="1a81d-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="1a81d-127">NOTES</span></span>

## <span data-ttu-id="1a81d-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1a81d-128">RELATED LINKS</span></span>
