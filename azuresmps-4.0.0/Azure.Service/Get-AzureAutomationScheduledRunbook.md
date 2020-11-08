---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 2F66B0F2-37F3-4046-9FB0-B8C4B90D84A3
online version: ''
schema: 2.0.0
ms.openlocfilehash: d03364038a7a0563e5a8ab2f2f88d36b24da0ebc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029819"
---
# <span data-ttu-id="30d4b-101">Get-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="30d4b-101">Get-AzureAutomationScheduledRunbook</span></span>

## <span data-ttu-id="30d4b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="30d4b-102">SYNOPSIS</span></span>

<span data-ttu-id="30d4b-103">Ottiene le manuali operativi di automazione Azure e le pianificazioni associate.</span><span class="sxs-lookup"><span data-stu-id="30d4b-103">Gets Azure Automation runbooks and associated schedules.</span></span>

## <span data-ttu-id="30d4b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="30d4b-104">SYNTAX</span></span>

### <span data-ttu-id="30d4b-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="30d4b-105">ByAll (Default)</span></span>
```
Get-AzureAutomationScheduledRunbook -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="30d4b-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="30d4b-106">ByJobScheduleId</span></span>
```
Get-AzureAutomationScheduledRunbook -JobScheduleId <Guid> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="30d4b-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="30d4b-107">ByRunbookName</span></span>
```
Get-AzureAutomationScheduledRunbook -RunbookName <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="30d4b-108">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="30d4b-108">ByRunbookNameAndScheduleName</span></span>
```
Get-AzureAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="30d4b-109">ByScheduleName</span><span class="sxs-lookup"><span data-stu-id="30d4b-109">ByScheduleName</span></span>
```
Get-AzureAutomationScheduledRunbook -ScheduleName <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="30d4b-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="30d4b-110">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="30d4b-111">**Get-AzureAutomationScheduledRunbook** ottiene uno o più manuali operativi di automazione Azure e pianificazioni associate.</span><span class="sxs-lookup"><span data-stu-id="30d4b-111">The **Get-AzureAutomationScheduledRunbook** gets one or more Azure Automation runbooks and associated schedules.</span></span>
<span data-ttu-id="30d4b-112">Per impostazione predefinita, vengono restituiti tutti i manuali operativi pianificati.</span><span class="sxs-lookup"><span data-stu-id="30d4b-112">By default, all scheduled runbooks are returned.</span></span>

<span data-ttu-id="30d4b-113">Per ottenere un Runbook programmato specifico, specificare il nome di Runbook e il nome della pianificazione.</span><span class="sxs-lookup"><span data-stu-id="30d4b-113">To get a specific scheduled runbook, specify the runbook name and the schedule name.</span></span>
<span data-ttu-id="30d4b-114">Per ottenere tutte le pianificazioni associate a un Runbook, specificare solo il nome Runbook.</span><span class="sxs-lookup"><span data-stu-id="30d4b-114">To get all schedules associated with a runbook, specify just the runbook name.</span></span>
<span data-ttu-id="30d4b-115">Per ottenere tutti i manuali operativi associati a una pianificazione, specificare solo il nome della pianificazione.</span><span class="sxs-lookup"><span data-stu-id="30d4b-115">To get all runbooks associated with a schedule, specify just the schedule name.</span></span>

## <span data-ttu-id="30d4b-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="30d4b-116">EXAMPLES</span></span>

### <span data-ttu-id="30d4b-117">Esempio 1: ottenere tutte le manuali operativi pianificate</span><span class="sxs-lookup"><span data-stu-id="30d4b-117">Example 1: Get all scheduled runbooks</span></span>
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17"
```

<span data-ttu-id="30d4b-118">Questo comando consente di ottenere tutte le manuali operativi pianificate nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="30d4b-118">This command gets all scheduled runbooks in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="30d4b-119">Esempio 2: ottenere tutte le pianificazioni associate a un Runbook</span><span class="sxs-lookup"><span data-stu-id="30d4b-119">Example 2: Get all schedules associated with a runbook</span></span>
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -RunbookName "Runbk01"
```

<span data-ttu-id="30d4b-120">Questo comando consente di ottenere tutte le manuali operativi pianificate per Runbook Runbk01 nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="30d4b-120">This command gets all scheduled runbooks for the runbook Runbk01 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="30d4b-121">Esempio 3: ottenere tutti i manuali operativi associati a una pianificazione</span><span class="sxs-lookup"><span data-stu-id="30d4b-121">Example 3: Get all runbooks associated with a schedule</span></span>
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ScheduleName "Schedule01"
```

<span data-ttu-id="30d4b-122">Questo comando consente di ottenere tutte le manuali operativi pianificate per la programmazione Schedule01 nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="30d4b-122">This command gets all scheduled runbooks for the schedule Schedule01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="30d4b-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="30d4b-123">PARAMETERS</span></span>

### <span data-ttu-id="30d4b-124">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="30d4b-124">-AutomationAccountName</span></span>
<span data-ttu-id="30d4b-125">Specifica il nome di un account di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="30d4b-125">Specifies the name of an Azure Automation account.</span></span>

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

### <span data-ttu-id="30d4b-126">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="30d4b-126">-JobScheduleId</span></span>
<span data-ttu-id="30d4b-127">Specifica l'ID di un processo programmato.</span><span class="sxs-lookup"><span data-stu-id="30d4b-127">Specifies the ID of a scheduled job.</span></span>

```yaml
Type: Guid
Parameter Sets: ByJobScheduleId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30d4b-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="30d4b-128">-Profile</span></span>
<span data-ttu-id="30d4b-129">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30d4b-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="30d4b-130">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="30d4b-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="30d4b-131">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="30d4b-131">-RunbookName</span></span>
<span data-ttu-id="30d4b-132">Specifica il nome di un Runbook.</span><span class="sxs-lookup"><span data-stu-id="30d4b-132">Specifies the name of a runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookName, ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30d4b-133">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="30d4b-133">-ScheduleName</span></span>
<span data-ttu-id="30d4b-134">Specifica il nome di una pianificazione.</span><span class="sxs-lookup"><span data-stu-id="30d4b-134">Specifies the name of a schedule.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName, ByScheduleName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30d4b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30d4b-135">CommonParameters</span></span>
<span data-ttu-id="30d4b-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30d4b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30d4b-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30d4b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30d4b-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="30d4b-138">INPUTS</span></span>

## <span data-ttu-id="30d4b-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="30d4b-139">OUTPUTS</span></span>

### <span data-ttu-id="30d4b-140">Microsoft. Azure. Commands. Automation. Model. JobSchedule</span><span class="sxs-lookup"><span data-stu-id="30d4b-140">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="30d4b-141">Note</span><span class="sxs-lookup"><span data-stu-id="30d4b-141">NOTES</span></span>

## <span data-ttu-id="30d4b-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="30d4b-142">RELATED LINKS</span></span>

[<span data-ttu-id="30d4b-143">Registro-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="30d4b-143">Register-AzureAutomationScheduledRunbook</span></span>](./Register-AzureAutomationScheduledRunbook.md)

[<span data-ttu-id="30d4b-144">Annullamento della registrazione-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="30d4b-144">Unregister-AzureAutomationScheduledRunbook</span></span>](./Unregister-AzureAutomationScheduledRunbook.md)


