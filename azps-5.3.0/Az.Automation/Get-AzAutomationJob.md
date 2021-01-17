---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BD32B909-296B-4E46-A24F-6E2BD4B9764B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
ms.openlocfilehash: 31390ccb19574b6b88c26828bf504dbc8ac5d924
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478707"
---
# <span data-ttu-id="5ac19-101">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="5ac19-101">Get-AzAutomationJob</span></span>

## <span data-ttu-id="5ac19-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5ac19-102">SYNOPSIS</span></span>
<span data-ttu-id="5ac19-103">Ottiene i processi di automazione Runbook.</span><span class="sxs-lookup"><span data-stu-id="5ac19-103">Gets Automation runbook jobs.</span></span>

## <span data-ttu-id="5ac19-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5ac19-104">SYNTAX</span></span>

### <span data-ttu-id="5ac19-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5ac19-105">ByAll (Default)</span></span>
```
Get-AzAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5ac19-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="5ac19-106">ByJobId</span></span>
```
Get-AzAutomationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ac19-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="5ac19-107">ByRunbookName</span></span>
```
Get-AzAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ac19-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ac19-108">DESCRIPTION</span></span>
<span data-ttu-id="5ac19-109">Il cmdlet **Get-AzAutomationJob** ottiene i processi Runbook in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="5ac19-109">The **Get-AzAutomationJob** cmdlet gets runbook jobs in Azure Automation.</span></span>

## <span data-ttu-id="5ac19-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5ac19-110">EXAMPLES</span></span>

### <span data-ttu-id="5ac19-111">Esempio 1: ottenere un processo di Runbook specifico</span><span class="sxs-lookup"><span data-stu-id="5ac19-111">Example 1: Get a specific runbook job</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

<span data-ttu-id="5ac19-112">Questo comando ottiene il processo con il GUID specificato.</span><span class="sxs-lookup"><span data-stu-id="5ac19-112">This command gets the job that has the specified GUID.</span></span>

### <span data-ttu-id="5ac19-113">Esempio 2: ottenere tutti i processi per un Runbook</span><span class="sxs-lookup"><span data-stu-id="5ac19-113">Example 2: Get all jobs for a runbook</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbook02"
```

<span data-ttu-id="5ac19-114">Questo comando consente di ottenere tutti i processi associati a un Runbook denominato Runbook02.</span><span class="sxs-lookup"><span data-stu-id="5ac19-114">This command gets all jobs associated with a runbook named Runbook02.</span></span>

### <span data-ttu-id="5ac19-115">Esempio 3: ottenere tutti i processi in uso</span><span class="sxs-lookup"><span data-stu-id="5ac19-115">Example 3: Get all running jobs</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Status "Running"
```

<span data-ttu-id="5ac19-116">Questo comando consente di ottenere tutti i processi in uso nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="5ac19-116">This command gets all running jobs in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="5ac19-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5ac19-117">PARAMETERS</span></span>

### <span data-ttu-id="5ac19-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5ac19-118">-AutomationAccountName</span></span>
<span data-ttu-id="5ac19-119">Specifica il nome di un account di automazione per cui questo cmdlet ottiene i processi.</span><span class="sxs-lookup"><span data-stu-id="5ac19-119">Specifies the name of an Automation account for which this cmdlet gets jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ac19-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ac19-120">-DefaultProfile</span></span>
<span data-ttu-id="5ac19-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5ac19-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ac19-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="5ac19-122">-EndTime</span></span>
<span data-ttu-id="5ac19-123">Specifica l'ora di fine di un processo come oggetto **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="5ac19-123">Specifies the end time for a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="5ac19-124">Puoi specificare una stringa che può essere convertita in un valore **DateTimeOffset** valido.</span><span class="sxs-lookup"><span data-stu-id="5ac19-124">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="5ac19-125">Questo cmdlet ottiene i processi che hanno un'ora di fine in corrispondenza o prima del valore specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="5ac19-125">This cmdlet gets jobs that have an end time at or before the value that this parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByRunbookName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ac19-126">-ID</span><span class="sxs-lookup"><span data-stu-id="5ac19-126">-Id</span></span>
<span data-ttu-id="5ac19-127">Specifica l'ID di un processo ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ac19-127">Specifies the ID of a job that this cmdlet gets.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ac19-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ac19-128">-ResourceGroupName</span></span>
<span data-ttu-id="5ac19-129">Specifica il nome di un gruppo di risorse in cui il cmdlet ottiene i processi.</span><span class="sxs-lookup"><span data-stu-id="5ac19-129">Specifies the name of a resource group in which this cmdlet gets jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ac19-130">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="5ac19-130">-RunbookName</span></span>
<span data-ttu-id="5ac19-131">Specifica il nome di un Runbook per cui questo cmdlet ottiene i processi.</span><span class="sxs-lookup"><span data-stu-id="5ac19-131">Specifies the name of a runbook for which this cmdlet gets jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ac19-132">-StartTime</span><span class="sxs-lookup"><span data-stu-id="5ac19-132">-StartTime</span></span>
<span data-ttu-id="5ac19-133">Specifica l'ora di inizio di un processo come oggetto **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="5ac19-133">Specifies the start time of a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="5ac19-134">Questo cmdlet ottiene i processi che hanno un'ora di inizio o dopo il valore specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="5ac19-134">This cmdlet gets jobs that have a start time at or after the value that this parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByRunbookName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ac19-135">-Stato</span><span class="sxs-lookup"><span data-stu-id="5ac19-135">-Status</span></span>
<span data-ttu-id="5ac19-136">Specifica lo stato di un processo.</span><span class="sxs-lookup"><span data-stu-id="5ac19-136">Specifies the status of a job.</span></span>
<span data-ttu-id="5ac19-137">Questo cmdlet ottiene i processi che hanno uno stato corrispondente a questo parametro.</span><span class="sxs-lookup"><span data-stu-id="5ac19-137">This cmdlet gets jobs that have a status matching this parameter.</span></span>
<span data-ttu-id="5ac19-138">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="5ac19-138">Valid values are:</span></span> 
- <span data-ttu-id="5ac19-139">L'attivazione</span><span class="sxs-lookup"><span data-stu-id="5ac19-139">Activating</span></span>
- <span data-ttu-id="5ac19-140">Completato</span><span class="sxs-lookup"><span data-stu-id="5ac19-140">Completed</span></span>
- <span data-ttu-id="5ac19-141">Fallito</span><span class="sxs-lookup"><span data-stu-id="5ac19-141">Failed</span></span>
- <span data-ttu-id="5ac19-142">Accodati</span><span class="sxs-lookup"><span data-stu-id="5ac19-142">Queued</span></span>
- <span data-ttu-id="5ac19-143">Ripresa</span><span class="sxs-lookup"><span data-stu-id="5ac19-143">Resuming</span></span>
- <span data-ttu-id="5ac19-144">Esecuzione</span><span class="sxs-lookup"><span data-stu-id="5ac19-144">Running</span></span>
- <span data-ttu-id="5ac19-145">Iniziale</span><span class="sxs-lookup"><span data-stu-id="5ac19-145">Starting</span></span>
- <span data-ttu-id="5ac19-146">Ha smesso</span><span class="sxs-lookup"><span data-stu-id="5ac19-146">Stopped</span></span>
- <span data-ttu-id="5ac19-147">Arresto</span><span class="sxs-lookup"><span data-stu-id="5ac19-147">Stopping</span></span>
- <span data-ttu-id="5ac19-148">Sospeso</span><span class="sxs-lookup"><span data-stu-id="5ac19-148">Suspended</span></span>
- <span data-ttu-id="5ac19-149">Sospensione</span><span class="sxs-lookup"><span data-stu-id="5ac19-149">Suspending</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, ByRunbookName
Aliases:
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ac19-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ac19-150">CommonParameters</span></span>
<span data-ttu-id="5ac19-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ac19-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ac19-152">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ac19-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ac19-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5ac19-153">INPUTS</span></span>

### <span data-ttu-id="5ac19-154">System. Guid</span><span class="sxs-lookup"><span data-stu-id="5ac19-154">System.Guid</span></span>

### <span data-ttu-id="5ac19-155">System. String</span><span class="sxs-lookup"><span data-stu-id="5ac19-155">System.String</span></span>

## <span data-ttu-id="5ac19-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5ac19-156">OUTPUTS</span></span>

### <span data-ttu-id="5ac19-157">Microsoft. Azure. Commands. Automation. Model. job</span><span class="sxs-lookup"><span data-stu-id="5ac19-157">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="5ac19-158">Note</span><span class="sxs-lookup"><span data-stu-id="5ac19-158">NOTES</span></span>

## <span data-ttu-id="5ac19-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5ac19-159">RELATED LINKS</span></span>

[<span data-ttu-id="5ac19-160">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="5ac19-160">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="5ac19-161">Curriculum vitae-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="5ac19-161">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="5ac19-162">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="5ac19-162">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="5ac19-163">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="5ac19-163">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


