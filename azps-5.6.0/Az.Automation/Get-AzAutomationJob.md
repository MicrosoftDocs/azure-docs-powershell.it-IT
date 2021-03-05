---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BD32B909-296B-4E46-A24F-6E2BD4B9764B
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
ms.openlocfilehash: 378bab1d62d5abcfb1eb2506e41d22bf26b217b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996952"
---
# <span data-ttu-id="b5b9c-101">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="b5b9c-101">Get-AzAutomationJob</span></span>

## <span data-ttu-id="b5b9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5b9c-102">SYNOPSIS</span></span>
<span data-ttu-id="b5b9c-103">Recupera i processi di runbook di automazione.</span><span class="sxs-lookup"><span data-stu-id="b5b9c-103">Gets Automation runbook jobs.</span></span>

## <span data-ttu-id="b5b9c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b5b9c-104">SYNTAX</span></span>

### <span data-ttu-id="b5b9c-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b5b9c-105">ByAll (Default)</span></span>
```
Get-AzAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b5b9c-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="b5b9c-106">ByJobId</span></span>
```
Get-AzAutomationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5b9c-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="b5b9c-107">ByRunbookName</span></span>
```
Get-AzAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5b9c-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b5b9c-108">DESCRIPTION</span></span>
<span data-ttu-id="b5b9c-109">Il cmdlet **Get-AzAutomationJob** ottiene i processi di runbook in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="b5b9c-109">The **Get-AzAutomationJob** cmdlet gets runbook jobs in Azure Automation.</span></span>

## <span data-ttu-id="b5b9c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b5b9c-110">EXAMPLES</span></span>

### <span data-ttu-id="b5b9c-111">Esempio 1: Ottenere un processo di runbook specifico</span><span class="sxs-lookup"><span data-stu-id="b5b9c-111">Example 1: Get a specific runbook job</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

<span data-ttu-id="b5b9c-112">Questo comando recupera il processo con il GUID specificato.</span><span class="sxs-lookup"><span data-stu-id="b5b9c-112">This command gets the job that has the specified GUID.</span></span>

### <span data-ttu-id="b5b9c-113">Esempio 2: Ottenere tutti i processi per un runbook</span><span class="sxs-lookup"><span data-stu-id="b5b9c-113">Example 2: Get all jobs for a runbook</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbook02"
```

<span data-ttu-id="b5b9c-114">Questo comando recupera tutti i processi associati a un runbook denominato Runbook02.</span><span class="sxs-lookup"><span data-stu-id="b5b9c-114">This command gets all jobs associated with a runbook named Runbook02.</span></span>

### <span data-ttu-id="b5b9c-115">Esempio 3: Ottenere tutti i processi in esecuzione</span><span class="sxs-lookup"><span data-stu-id="b5b9c-115">Example 3: Get all running jobs</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Status "Running"
```

<span data-ttu-id="b5b9c-116">Questo comando recupera tutti i processi in esecuzione nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="b5b9c-116">This command gets all running jobs in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="b5b9c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5b9c-117">PARAMETERS</span></span>

### <span data-ttu-id="b5b9c-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b5b9c-118">-AutomationAccountName</span></span>
<span data-ttu-id="b5b9c-119">Specifica il nome di un account di automazione per cui il cmdlet ottiene processi.</span><span class="sxs-lookup"><span data-stu-id="b5b9c-119">Specifies the name of an Automation account for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="b5b9c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5b9c-120">-DefaultProfile</span></span>
<span data-ttu-id="b5b9c-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b5b9c-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5b9c-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="b5b9c-122">-EndTime</span></span>
<span data-ttu-id="b5b9c-123">Specifica l'ora di fine per un processo come **oggetto DateTime Offset.**</span><span class="sxs-lookup"><span data-stu-id="b5b9c-123">Specifies the end time for a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="b5b9c-124">È possibile specificare una stringa che può essere convertita in **un valore DateTime Offset valido.**</span><span class="sxs-lookup"><span data-stu-id="b5b9c-124">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="b5b9c-125">Questo cmdlet ottiene i processi che hanno un'ora di fine in corrispondenza o prima del valore specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="b5b9c-125">This cmdlet gets jobs that have an end time at or before the value that this parameter specifies.</span></span>

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

### <span data-ttu-id="b5b9c-126">-Id</span><span class="sxs-lookup"><span data-stu-id="b5b9c-126">-Id</span></span>
<span data-ttu-id="b5b9c-127">Specifica l'ID di un processo che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5b9c-127">Specifies the ID of a job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b5b9c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5b9c-128">-ResourceGroupName</span></span>
<span data-ttu-id="b5b9c-129">Specifica il nome di un gruppo di risorse in cui il cmdlet riceve i processi.</span><span class="sxs-lookup"><span data-stu-id="b5b9c-129">Specifies the name of a resource group in which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="b5b9c-130">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="b5b9c-130">-RunbookName</span></span>
<span data-ttu-id="b5b9c-131">Specifica il nome di un runbook per cui il cmdlet ottiene processi.</span><span class="sxs-lookup"><span data-stu-id="b5b9c-131">Specifies the name of a runbook for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="b5b9c-132">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b5b9c-132">-StartTime</span></span>
<span data-ttu-id="b5b9c-133">Specifica l'ora di inizio di un processo come **oggetto DateTime Offset.**</span><span class="sxs-lookup"><span data-stu-id="b5b9c-133">Specifies the start time of a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="b5b9c-134">Questo cmdlet ottiene processi che hanno un'ora di inizio in corrispondenza o dopo il valore specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="b5b9c-134">This cmdlet gets jobs that have a start time at or after the value that this parameter specifies.</span></span>

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

### <span data-ttu-id="b5b9c-135">-Stato</span><span class="sxs-lookup"><span data-stu-id="b5b9c-135">-Status</span></span>
<span data-ttu-id="b5b9c-136">Specifica lo stato di un processo.</span><span class="sxs-lookup"><span data-stu-id="b5b9c-136">Specifies the status of a job.</span></span>
<span data-ttu-id="b5b9c-137">Questo cmdlet recupera i processi con stato corrispondente a questo parametro.</span><span class="sxs-lookup"><span data-stu-id="b5b9c-137">This cmdlet gets jobs that have a status matching this parameter.</span></span>
<span data-ttu-id="b5b9c-138">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="b5b9c-138">Valid values are:</span></span> 
- <span data-ttu-id="b5b9c-139">Attivazione</span><span class="sxs-lookup"><span data-stu-id="b5b9c-139">Activating</span></span>
- <span data-ttu-id="b5b9c-140">Completato</span><span class="sxs-lookup"><span data-stu-id="b5b9c-140">Completed</span></span>
- <span data-ttu-id="b5b9c-141">Operazione non riuscita</span><span class="sxs-lookup"><span data-stu-id="b5b9c-141">Failed</span></span>
- <span data-ttu-id="b5b9c-142">In coda</span><span class="sxs-lookup"><span data-stu-id="b5b9c-142">Queued</span></span>
- <span data-ttu-id="b5b9c-143">Ripresa</span><span class="sxs-lookup"><span data-stu-id="b5b9c-143">Resuming</span></span>
- <span data-ttu-id="b5b9c-144">In esecuzione</span><span class="sxs-lookup"><span data-stu-id="b5b9c-144">Running</span></span>
- <span data-ttu-id="b5b9c-145">Avvio in corso</span><span class="sxs-lookup"><span data-stu-id="b5b9c-145">Starting</span></span>
- <span data-ttu-id="b5b9c-146">Arrestato</span><span class="sxs-lookup"><span data-stu-id="b5b9c-146">Stopped</span></span>
- <span data-ttu-id="b5b9c-147">Arresto in corso</span><span class="sxs-lookup"><span data-stu-id="b5b9c-147">Stopping</span></span>
- <span data-ttu-id="b5b9c-148">Sospeso</span><span class="sxs-lookup"><span data-stu-id="b5b9c-148">Suspended</span></span>
- <span data-ttu-id="b5b9c-149">Sospensione</span><span class="sxs-lookup"><span data-stu-id="b5b9c-149">Suspending</span></span>

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

### <span data-ttu-id="b5b9c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5b9c-150">CommonParameters</span></span>
<span data-ttu-id="b5b9c-151">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5b9c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5b9c-152">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5b9c-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5b9c-153">INPUT</span><span class="sxs-lookup"><span data-stu-id="b5b9c-153">INPUTS</span></span>

### <span data-ttu-id="b5b9c-154">System.Guid</span><span class="sxs-lookup"><span data-stu-id="b5b9c-154">System.Guid</span></span>

### <span data-ttu-id="b5b9c-155">System.String</span><span class="sxs-lookup"><span data-stu-id="b5b9c-155">System.String</span></span>

## <span data-ttu-id="b5b9c-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b5b9c-156">OUTPUTS</span></span>

### <span data-ttu-id="b5b9c-157">Microsoft.Azure.Commands.Automation.Model.Job</span><span class="sxs-lookup"><span data-stu-id="b5b9c-157">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="b5b9c-158">NOTE</span><span class="sxs-lookup"><span data-stu-id="b5b9c-158">NOTES</span></span>

## <span data-ttu-id="b5b9c-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b5b9c-159">RELATED LINKS</span></span>

[<span data-ttu-id="b5b9c-160">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="b5b9c-160">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="b5b9c-161">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="b5b9c-161">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="b5b9c-162">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="b5b9c-162">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="b5b9c-163">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="b5b9c-163">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


