---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 6527FF45-9C16-47E8-8E70-619A0581D2F8
online version: ''
schema: 2.0.0
ms.openlocfilehash: c595779fa8c6b4c246f102a346290e931dc89379
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029831"
---
# <span data-ttu-id="dd4cd-101">Get-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="dd4cd-101">Get-AzureAutomationJob</span></span>

## <span data-ttu-id="dd4cd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dd4cd-102">SYNOPSIS</span></span>

<span data-ttu-id="dd4cd-103">Ottiene uno o più processi di Runbook di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="dd4cd-103">Gets one or more Azure Automation runbook jobs.</span></span>

## <span data-ttu-id="dd4cd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dd4cd-104">SYNTAX</span></span>

### <span data-ttu-id="dd4cd-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dd4cd-105">ByAll (Default)</span></span>
```
Get-AzureAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="dd4cd-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="dd4cd-106">ByJobId</span></span>
```
Get-AzureAutomationJob -Id <Guid> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="dd4cd-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="dd4cd-107">ByRunbookName</span></span>
```
Get-AzureAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="dd4cd-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd4cd-108">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="dd4cd-109">Il cmdlet **Get-AzureAutomationJob** ottiene uno o più processi Runbook in Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="dd4cd-109">The **Get-AzureAutomationJob** cmdlet gets one or more runbook jobs in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="dd4cd-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dd4cd-110">EXAMPLES</span></span>

### <span data-ttu-id="dd4cd-111">Esempio 1: ottenere un processo di Runbook specifico</span><span class="sxs-lookup"><span data-stu-id="dd4cd-111">Example 1: Get a specific runbook job</span></span>
```
PS C:\> Get-AzureAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

<span data-ttu-id="dd4cd-112">Questo comando ottiene il processo con il GUID specificato.</span><span class="sxs-lookup"><span data-stu-id="dd4cd-112">This command gets the job that has the specified GUID.</span></span>

### <span data-ttu-id="dd4cd-113">Esempio 2: ottenere tutti i processi per un Runbook</span><span class="sxs-lookup"><span data-stu-id="dd4cd-113">Example 2: Get all jobs for a runbook</span></span>
```
PS C:\> Get-AzureAutomationJob -AutomationAccountName "Contoso17" -RunbookName "MyRunbook"
```

<span data-ttu-id="dd4cd-114">Questo comando consente di ottenere tutti i processi associati a un Runbook denominato MyRunbook.</span><span class="sxs-lookup"><span data-stu-id="dd4cd-114">This command gets all jobs associated with a runbook named MyRunbook.</span></span>

### <span data-ttu-id="dd4cd-115">Esempio 2: ottenere tutti i processi in uso</span><span class="sxs-lookup"><span data-stu-id="dd4cd-115">Example 2: Get all running jobs</span></span>
```
PS C:\> Get-AzureAutomationJob -AutomationAccountName "Contoso17" -Status "Running"
```

<span data-ttu-id="dd4cd-116">Questo comando consente di ottenere tutti i processi in uso nell'account di automazione con il nome Contoso17.</span><span class="sxs-lookup"><span data-stu-id="dd4cd-116">This command gets all running jobs in the automation account with the name Contoso17.</span></span>

## <span data-ttu-id="dd4cd-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dd4cd-117">PARAMETERS</span></span>

### <span data-ttu-id="dd4cd-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="dd4cd-118">-AutomationAccountName</span></span>
<span data-ttu-id="dd4cd-119">Specifica il nome di un account di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="dd4cd-119">Specifies the name of an Azure Automation account.</span></span>

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

### <span data-ttu-id="dd4cd-120">-EndTime</span><span class="sxs-lookup"><span data-stu-id="dd4cd-120">-EndTime</span></span>
<span data-ttu-id="dd4cd-121">Specifica l'ora di fine per un processo.</span><span class="sxs-lookup"><span data-stu-id="dd4cd-121">Specifies the end time for a job.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByAll, ByRunbookName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd4cd-122">-ID</span><span class="sxs-lookup"><span data-stu-id="dd4cd-122">-Id</span></span>
<span data-ttu-id="dd4cd-123">Specifica l'ID di un processo.</span><span class="sxs-lookup"><span data-stu-id="dd4cd-123">Specifies the ID of a job.</span></span>

```yaml
Type: Guid
Parameter Sets: ByJobId
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd4cd-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="dd4cd-124">-Profile</span></span>
<span data-ttu-id="dd4cd-125">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd4cd-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="dd4cd-126">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="dd4cd-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="dd4cd-127">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="dd4cd-127">-RunbookName</span></span>
<span data-ttu-id="dd4cd-128">Specifica il nome di un Runbook.</span><span class="sxs-lookup"><span data-stu-id="dd4cd-128">Specifies the name of a runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd4cd-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="dd4cd-129">-StartTime</span></span>
<span data-ttu-id="dd4cd-130">Specifica l'ora di inizio di un processo.</span><span class="sxs-lookup"><span data-stu-id="dd4cd-130">Specifies the start time of a job.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByAll, ByRunbookName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd4cd-131">-Stato</span><span class="sxs-lookup"><span data-stu-id="dd4cd-131">-Status</span></span>
<span data-ttu-id="dd4cd-132">Specifica lo stato di un processo.</span><span class="sxs-lookup"><span data-stu-id="dd4cd-132">Specifies the status of a job.</span></span>
<span data-ttu-id="dd4cd-133">Questo cmdlet ottiene i processi che hanno uno stato corrispondente a questo parametro.</span><span class="sxs-lookup"><span data-stu-id="dd4cd-133">This cmdlet gets jobs that have a status matching this parameter.</span></span>
<span data-ttu-id="dd4cd-134">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="dd4cd-134">Valid values are:</span></span> 

- <span data-ttu-id="dd4cd-135">Completato</span><span class="sxs-lookup"><span data-stu-id="dd4cd-135">Completed</span></span>
- <span data-ttu-id="dd4cd-136">Fallito</span><span class="sxs-lookup"><span data-stu-id="dd4cd-136">Failed</span></span>
- <span data-ttu-id="dd4cd-137">Accodati</span><span class="sxs-lookup"><span data-stu-id="dd4cd-137">Queued</span></span>
- <span data-ttu-id="dd4cd-138">Iniziale</span><span class="sxs-lookup"><span data-stu-id="dd4cd-138">Starting</span></span>
- <span data-ttu-id="dd4cd-139">Ripresa</span><span class="sxs-lookup"><span data-stu-id="dd4cd-139">Resuming</span></span>
- <span data-ttu-id="dd4cd-140">Esecuzione</span><span class="sxs-lookup"><span data-stu-id="dd4cd-140">Running</span></span>
- <span data-ttu-id="dd4cd-141">Ha smesso</span><span class="sxs-lookup"><span data-stu-id="dd4cd-141">Stopped</span></span>
- <span data-ttu-id="dd4cd-142">Arresto</span><span class="sxs-lookup"><span data-stu-id="dd4cd-142">Stopping</span></span>
- <span data-ttu-id="dd4cd-143">Sospeso</span><span class="sxs-lookup"><span data-stu-id="dd4cd-143">Suspended</span></span>
- <span data-ttu-id="dd4cd-144">Sospensione</span><span class="sxs-lookup"><span data-stu-id="dd4cd-144">Suspending</span></span>
- <span data-ttu-id="dd4cd-145">L'attivazione</span><span class="sxs-lookup"><span data-stu-id="dd4cd-145">Activating</span></span>

```yaml
Type: String
Parameter Sets: ByAll, ByRunbookName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd4cd-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd4cd-146">CommonParameters</span></span>
<span data-ttu-id="dd4cd-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd4cd-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd4cd-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd4cd-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd4cd-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dd4cd-149">INPUTS</span></span>

## <span data-ttu-id="dd4cd-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dd4cd-150">OUTPUTS</span></span>

### <span data-ttu-id="dd4cd-151">Microsoft. Azure. Commands. Automation. Model. job</span><span class="sxs-lookup"><span data-stu-id="dd4cd-151">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="dd4cd-152">Note</span><span class="sxs-lookup"><span data-stu-id="dd4cd-152">NOTES</span></span>

## <span data-ttu-id="dd4cd-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dd4cd-153">RELATED LINKS</span></span>

[<span data-ttu-id="dd4cd-154">Curriculum vitae-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="dd4cd-154">Resume-AzureAutomationJob</span></span>](./Resume-AzureAutomationJob.md)

[<span data-ttu-id="dd4cd-155">Stop-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="dd4cd-155">Stop-AzureAutomationJob</span></span>](./Stop-AzureAutomationJob.md)

[<span data-ttu-id="dd4cd-156">Suspend-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="dd4cd-156">Suspend-AzureAutomationJob</span></span>](./Suspend-AzureAutomationJob.md)


