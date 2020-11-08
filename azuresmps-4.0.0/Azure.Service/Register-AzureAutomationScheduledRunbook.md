---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 6D15837A-22A9-4C5A-8064-C3605088EA71
online version: ''
schema: 2.0.0
ms.openlocfilehash: d31a2ef49674054ca6bb257df67d3439f5abe074
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023831"
---
# <span data-ttu-id="70f84-101">Register-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="70f84-101">Register-AzureAutomationScheduledRunbook</span></span>

## <span data-ttu-id="70f84-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="70f84-102">SYNOPSIS</span></span>

<span data-ttu-id="70f84-103">Associa un Runbook a una pianificazione.</span><span class="sxs-lookup"><span data-stu-id="70f84-103">Associates a runbook with a schedule.</span></span>

## <span data-ttu-id="70f84-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="70f84-104">SYNTAX</span></span>

### <span data-ttu-id="70f84-105">ByRunbookName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="70f84-105">ByRunbookName (Default)</span></span>
```
Register-AzureAutomationScheduledRunbook -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="70f84-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="70f84-106">ByRunbookNameAndScheduleName</span></span>
```
Register-AzureAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 [-Parameters <IDictionary>] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="70f84-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="70f84-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="70f84-108">Il cmdlet **Register-AzureAutomationScheduledRunbook** associa un Runbook a una pianificazione.</span><span class="sxs-lookup"><span data-stu-id="70f84-108">The **Register-AzureAutomationScheduledRunbook** cmdlet associates a runbook with a schedule.</span></span>
<span data-ttu-id="70f84-109">Runbook inizia in base alla pianificazione specificata usando il parametro *ScheduleName* .</span><span class="sxs-lookup"><span data-stu-id="70f84-109">The runbook starts based on the schedule you specify using the *ScheduleName* parameter.</span></span>

## <span data-ttu-id="70f84-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="70f84-110">EXAMPLES</span></span>

### <span data-ttu-id="70f84-111">Esempio 1: associare un Runbook a una pianificazione</span><span class="sxs-lookup"><span data-stu-id="70f84-111">Example 1: Associate a runbook with a schedule</span></span>
```
PS C:\> Register-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ScheduleName "Sched01"
```

<span data-ttu-id="70f84-112">Questo comando associa il Runbook denominato Runbk01 con la pianificazione denominata Sched01 nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="70f84-112">This command associates the runbook named Runbk01 with the schedule named Sched01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="70f84-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="70f84-113">PARAMETERS</span></span>

### <span data-ttu-id="70f84-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="70f84-114">-AutomationAccountName</span></span>
<span data-ttu-id="70f84-115">Specifica il nome di un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="70f84-115">Specifies the name of an Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70f84-116">-Parameters</span><span class="sxs-lookup"><span data-stu-id="70f84-116">-Parameters</span></span>
```yaml
Type: IDictionary
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70f84-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="70f84-117">-Profile</span></span>
<span data-ttu-id="70f84-118">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70f84-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="70f84-119">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="70f84-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70f84-120">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="70f84-120">-RunbookName</span></span>
<span data-ttu-id="70f84-121">Specifica il nome di Runbook.</span><span class="sxs-lookup"><span data-stu-id="70f84-121">Specifies the name of the runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70f84-122">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="70f84-122">-ScheduleName</span></span>
<span data-ttu-id="70f84-123">Specifica il nome della pianificazione.</span><span class="sxs-lookup"><span data-stu-id="70f84-123">Specifies the name of the schedule.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70f84-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70f84-124">CommonParameters</span></span>
<span data-ttu-id="70f84-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70f84-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70f84-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70f84-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70f84-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="70f84-127">INPUTS</span></span>

## <span data-ttu-id="70f84-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="70f84-128">OUTPUTS</span></span>

### <span data-ttu-id="70f84-129">Microsoft. Azure. Commands. Automation. Model. JobSchedule</span><span class="sxs-lookup"><span data-stu-id="70f84-129">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="70f84-130">Note</span><span class="sxs-lookup"><span data-stu-id="70f84-130">NOTES</span></span>

## <span data-ttu-id="70f84-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="70f84-131">RELATED LINKS</span></span>

[<span data-ttu-id="70f84-132">New-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="70f84-132">New-AzureAutomationSchedule</span></span>](./New-AzureAutomationSchedule.md)

[<span data-ttu-id="70f84-133">Annullamento della registrazione-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="70f84-133">Unregister-AzureAutomationScheduledRunbook</span></span>](./Unregister-AzureAutomationScheduledRunbook.md)


