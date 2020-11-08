---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruleschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
ms.openlocfilehash: 52f929cea9f2017ad6a2c2ea16475ec7d5d8a5a0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200750"
---
# <span data-ttu-id="6f600-101">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="6f600-101">New-AzScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="6f600-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6f600-102">SYNOPSIS</span></span>
<span data-ttu-id="6f600-103">Crea un oggetto di tipo Schedule</span><span class="sxs-lookup"><span data-stu-id="6f600-103">Creates an object of type Schedule</span></span>

## <span data-ttu-id="6f600-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6f600-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleSchedule -FrequencyInMinutes <Int32> -TimeWindowInMinutes <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f600-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6f600-105">DESCRIPTION</span></span>
<span data-ttu-id="6f600-106">Crea un oggetto di tipo Schedule.</span><span class="sxs-lookup"><span data-stu-id="6f600-106">Creates an object of type Schedule.</span></span>
<span data-ttu-id="6f600-107">Questo oggetto deve essere passato al comando che crea la regola di avviso del log.</span><span class="sxs-lookup"><span data-stu-id="6f600-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="6f600-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6f600-108">EXAMPLES</span></span>

### <span data-ttu-id="6f600-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6f600-109">Example 1</span></span>
```powershell
PS C:\>  $schedule = New-AzScheduledQueryRuleSchedule -FrequencyInMinutes 15 -TimeWindowInMinutes 15
```

## <span data-ttu-id="6f600-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6f600-110">PARAMETERS</span></span>

### <span data-ttu-id="6f600-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f600-111">-DefaultProfile</span></span>
<span data-ttu-id="6f600-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6f600-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f600-113">-FrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="6f600-113">-FrequencyInMinutes</span></span>
<span data-ttu-id="6f600-114">Frequenza di avviso</span><span class="sxs-lookup"><span data-stu-id="6f600-114">The alert frequency</span></span>

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

### <span data-ttu-id="6f600-115">-TimeWindowInMinutes</span><span class="sxs-lookup"><span data-stu-id="6f600-115">-TimeWindowInMinutes</span></span>
<span data-ttu-id="6f600-116">Finestra del tempo di avviso</span><span class="sxs-lookup"><span data-stu-id="6f600-116">The alert time window</span></span>

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

### <span data-ttu-id="6f600-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f600-117">CommonParameters</span></span>
<span data-ttu-id="6f600-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f600-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f600-119">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6f600-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f600-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6f600-120">INPUTS</span></span>

### <span data-ttu-id="6f600-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6f600-121">None</span></span>

## <span data-ttu-id="6f600-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6f600-122">OUTPUTS</span></span>

### <span data-ttu-id="6f600-123">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="6f600-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="6f600-124">Note</span><span class="sxs-lookup"><span data-stu-id="6f600-124">NOTES</span></span>

## <span data-ttu-id="6f600-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6f600-125">RELATED LINKS</span></span>