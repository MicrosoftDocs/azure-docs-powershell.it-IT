---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruleschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
ms.openlocfilehash: 2043a2cf31354c7fc14b1b03794dff6f82af67b8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854061"
---
# <span data-ttu-id="d08d0-101">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="d08d0-101">New-AzScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="d08d0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d08d0-102">SYNOPSIS</span></span>
<span data-ttu-id="d08d0-103">Crea un oggetto di tipo Schedule</span><span class="sxs-lookup"><span data-stu-id="d08d0-103">Creates an object of type Schedule</span></span>

## <span data-ttu-id="d08d0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d08d0-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleSchedule -FrequencyInMinutes <Int32> -TimeWindowInMinutes <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d08d0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d08d0-105">DESCRIPTION</span></span>
<span data-ttu-id="d08d0-106">Crea un oggetto di tipo Schedule.</span><span class="sxs-lookup"><span data-stu-id="d08d0-106">Creates an object of type Schedule.</span></span>
<span data-ttu-id="d08d0-107">Questo oggetto deve essere passato al comando che crea la regola di avviso del log.</span><span class="sxs-lookup"><span data-stu-id="d08d0-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="d08d0-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d08d0-108">EXAMPLES</span></span>

### <span data-ttu-id="d08d0-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d08d0-109">Example 1</span></span>
```powershell
PS C:\>  $schedule = New-AzScheduledQueryRuleSchedule -FrequencyInMinutes 15 -TimeWindowInMinutes 15
```

## <span data-ttu-id="d08d0-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d08d0-110">PARAMETERS</span></span>

### <span data-ttu-id="d08d0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d08d0-111">-DefaultProfile</span></span>
<span data-ttu-id="d08d0-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d08d0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d08d0-113">-FrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="d08d0-113">-FrequencyInMinutes</span></span>
<span data-ttu-id="d08d0-114">Frequenza di avviso</span><span class="sxs-lookup"><span data-stu-id="d08d0-114">The alert frequency</span></span>

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

### <span data-ttu-id="d08d0-115">-TimeWindowInMinutes</span><span class="sxs-lookup"><span data-stu-id="d08d0-115">-TimeWindowInMinutes</span></span>
<span data-ttu-id="d08d0-116">Finestra del tempo di avviso</span><span class="sxs-lookup"><span data-stu-id="d08d0-116">The alert time window</span></span>

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

### <span data-ttu-id="d08d0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d08d0-117">CommonParameters</span></span>
<span data-ttu-id="d08d0-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d08d0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d08d0-119">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d08d0-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d08d0-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d08d0-120">INPUTS</span></span>

### <span data-ttu-id="d08d0-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d08d0-121">None</span></span>

## <span data-ttu-id="d08d0-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d08d0-122">OUTPUTS</span></span>

### <span data-ttu-id="d08d0-123">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="d08d0-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="d08d0-124">Note</span><span class="sxs-lookup"><span data-stu-id="d08d0-124">NOTES</span></span>

## <span data-ttu-id="d08d0-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d08d0-125">RELATED LINKS</span></span>
