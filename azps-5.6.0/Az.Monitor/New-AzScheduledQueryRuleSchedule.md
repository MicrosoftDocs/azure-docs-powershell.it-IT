---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azscheduledqueryruleschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
ms.openlocfilehash: 231b9250509ed463f7f9b2a2d9563dbb1e378ee0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978414"
---
# <span data-ttu-id="d8d05-101">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="d8d05-101">New-AzScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="d8d05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8d05-102">SYNOPSIS</span></span>
<span data-ttu-id="d8d05-103">Crea un oggetto di tipo Pianificazione</span><span class="sxs-lookup"><span data-stu-id="d8d05-103">Creates an object of type Schedule</span></span>

## <span data-ttu-id="d8d05-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d8d05-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleSchedule -FrequencyInMinutes <Int32> -TimeWindowInMinutes <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8d05-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d8d05-105">DESCRIPTION</span></span>
<span data-ttu-id="d8d05-106">Crea un oggetto di tipo Pianificazione.</span><span class="sxs-lookup"><span data-stu-id="d8d05-106">Creates an object of type Schedule.</span></span>
<span data-ttu-id="d8d05-107">Questo oggetto deve essere passato al comando che crea la regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="d8d05-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="d8d05-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d8d05-108">EXAMPLES</span></span>

### <span data-ttu-id="d8d05-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d8d05-109">Example 1</span></span>
```powershell
PS C:\>  $schedule = New-AzScheduledQueryRuleSchedule -FrequencyInMinutes 15 -TimeWindowInMinutes 15
```

## <span data-ttu-id="d8d05-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8d05-110">PARAMETERS</span></span>

### <span data-ttu-id="d8d05-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8d05-111">-DefaultProfile</span></span>
<span data-ttu-id="d8d05-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d8d05-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8d05-113">-FrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="d8d05-113">-FrequencyInMinutes</span></span>
<span data-ttu-id="d8d05-114">Frequenza degli avvisi</span><span class="sxs-lookup"><span data-stu-id="d8d05-114">The alert frequency</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8d05-115">-TimeWindowInMinutes</span><span class="sxs-lookup"><span data-stu-id="d8d05-115">-TimeWindowInMinutes</span></span>
<span data-ttu-id="d8d05-116">Intervallo di tempo dell'avviso</span><span class="sxs-lookup"><span data-stu-id="d8d05-116">The alert time window</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8d05-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8d05-117">CommonParameters</span></span>
<span data-ttu-id="d8d05-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8d05-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8d05-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d8d05-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8d05-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="d8d05-120">INPUTS</span></span>

### <span data-ttu-id="d8d05-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d8d05-121">None</span></span>

## <span data-ttu-id="d8d05-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d8d05-122">OUTPUTS</span></span>

### <span data-ttu-id="d8d05-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="d8d05-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="d8d05-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="d8d05-124">NOTES</span></span>

## <span data-ttu-id="d8d05-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d8d05-125">RELATED LINKS</span></span>
