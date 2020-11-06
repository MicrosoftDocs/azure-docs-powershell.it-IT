---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BD32B909-296B-4E46-A24F-6E2BD4B9764B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJob.md
ms.openlocfilehash: 3183720cbafc9a8feae5c9687dfb92ab325f8b04
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508416"
---
# <span data-ttu-id="7663b-101">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="7663b-101">Get-AzureRmAutomationJob</span></span>

## <span data-ttu-id="7663b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7663b-102">SYNOPSIS</span></span>
<span data-ttu-id="7663b-103">Ottiene i processi di automazione Runbook.</span><span class="sxs-lookup"><span data-stu-id="7663b-103">Gets Automation runbook jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7663b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7663b-104">SYNTAX</span></span>

### <span data-ttu-id="7663b-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7663b-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7663b-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="7663b-106">ByJobId</span></span>
```
Get-AzureRmAutomationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7663b-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="7663b-107">ByRunbookName</span></span>
```
Get-AzureRmAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7663b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7663b-108">DESCRIPTION</span></span>
<span data-ttu-id="7663b-109">Il cmdlet **Get-AzureRmAutomationJob** ottiene i processi Runbook in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="7663b-109">The **Get-AzureRmAutomationJob** cmdlet gets runbook jobs in Azure Automation.</span></span>

## <span data-ttu-id="7663b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7663b-110">EXAMPLES</span></span>

### <span data-ttu-id="7663b-111">Esempio 1: ottenere un processo di Runbook specifico</span><span class="sxs-lookup"><span data-stu-id="7663b-111">Example 1: Get a specific runbook job</span></span>
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

<span data-ttu-id="7663b-112">Questo comando ottiene il processo con il GUID specificato.</span><span class="sxs-lookup"><span data-stu-id="7663b-112">This command gets the job that has the specified GUID.</span></span>

### <span data-ttu-id="7663b-113">Esempio 2: ottenere tutti i processi per un Runbook</span><span class="sxs-lookup"><span data-stu-id="7663b-113">Example 2: Get all jobs for a runbook</span></span>
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbook02"
```

<span data-ttu-id="7663b-114">Questo comando consente di ottenere tutti i processi associati a un Runbook denominato Runbook02.</span><span class="sxs-lookup"><span data-stu-id="7663b-114">This command gets all jobs associated with a runbook named Runbook02.</span></span>

### <span data-ttu-id="7663b-115">Esempio 3: ottenere tutti i processi in uso</span><span class="sxs-lookup"><span data-stu-id="7663b-115">Example 3: Get all running jobs</span></span>
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Status "Running"
```

<span data-ttu-id="7663b-116">Questo comando consente di ottenere tutti i processi in uso nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="7663b-116">This command gets all running jobs in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="7663b-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7663b-117">PARAMETERS</span></span>

### <span data-ttu-id="7663b-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7663b-118">-AutomationAccountName</span></span>
<span data-ttu-id="7663b-119">Specifica il nome di un account di automazione per cui questo cmdlet ottiene i processi.</span><span class="sxs-lookup"><span data-stu-id="7663b-119">Specifies the name of an Automation account for which this cmdlet gets jobs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7663b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7663b-120">-DefaultProfile</span></span>
<span data-ttu-id="7663b-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7663b-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7663b-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="7663b-122">-EndTime</span></span>
<span data-ttu-id="7663b-123">Specifica l'ora di fine di un processo come oggetto **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="7663b-123">Specifies the end time for a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="7663b-124">Puoi specificare una stringa che può essere convertita in un valore **DateTimeOffset** valido.</span><span class="sxs-lookup"><span data-stu-id="7663b-124">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="7663b-125">Questo cmdlet ottiene i processi che hanno un'ora di fine in corrispondenza o prima del valore specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="7663b-125">This cmdlet gets jobs that have an end time at or before the value that this parameter specifies.</span></span>

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

### <span data-ttu-id="7663b-126">-ID</span><span class="sxs-lookup"><span data-stu-id="7663b-126">-Id</span></span>
<span data-ttu-id="7663b-127">Specifica l'ID di un processo ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7663b-127">Specifies the ID of a job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7663b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7663b-128">-ResourceGroupName</span></span>
<span data-ttu-id="7663b-129">Specifica il nome di un gruppo di risorse in cui il cmdlet ottiene i processi.</span><span class="sxs-lookup"><span data-stu-id="7663b-129">Specifies the name of a resource group in which this cmdlet gets jobs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7663b-130">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="7663b-130">-RunbookName</span></span>
<span data-ttu-id="7663b-131">Specifica il nome di un Runbook per cui questo cmdlet ottiene i processi.</span><span class="sxs-lookup"><span data-stu-id="7663b-131">Specifies the name of a runbook for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="7663b-132">-StartTime</span><span class="sxs-lookup"><span data-stu-id="7663b-132">-StartTime</span></span>
<span data-ttu-id="7663b-133">Specifica l'ora di inizio di un processo come oggetto **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="7663b-133">Specifies the start time of a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="7663b-134">Questo cmdlet ottiene i processi che hanno un'ora di inizio o dopo il valore specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="7663b-134">This cmdlet gets jobs that have a start time at or after the value that this parameter specifies.</span></span>

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

### <span data-ttu-id="7663b-135">-Stato</span><span class="sxs-lookup"><span data-stu-id="7663b-135">-Status</span></span>
<span data-ttu-id="7663b-136">Specifica lo stato di un processo.</span><span class="sxs-lookup"><span data-stu-id="7663b-136">Specifies the status of a job.</span></span>
<span data-ttu-id="7663b-137">Questo cmdlet ottiene i processi che hanno uno stato corrispondente a questo parametro.</span><span class="sxs-lookup"><span data-stu-id="7663b-137">This cmdlet gets jobs that have a status matching this parameter.</span></span>
<span data-ttu-id="7663b-138">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="7663b-138">Valid values are:</span></span> 

- <span data-ttu-id="7663b-139">L'attivazione</span><span class="sxs-lookup"><span data-stu-id="7663b-139">Activating</span></span>
- <span data-ttu-id="7663b-140">Completato</span><span class="sxs-lookup"><span data-stu-id="7663b-140">Completed</span></span>
- <span data-ttu-id="7663b-141">Fallito</span><span class="sxs-lookup"><span data-stu-id="7663b-141">Failed</span></span>
- <span data-ttu-id="7663b-142">Accodati</span><span class="sxs-lookup"><span data-stu-id="7663b-142">Queued</span></span>
- <span data-ttu-id="7663b-143">Ripresa</span><span class="sxs-lookup"><span data-stu-id="7663b-143">Resuming</span></span>
- <span data-ttu-id="7663b-144">Esecuzione</span><span class="sxs-lookup"><span data-stu-id="7663b-144">Running</span></span>
- <span data-ttu-id="7663b-145">Iniziale</span><span class="sxs-lookup"><span data-stu-id="7663b-145">Starting</span></span>
- <span data-ttu-id="7663b-146">Ha smesso</span><span class="sxs-lookup"><span data-stu-id="7663b-146">Stopped</span></span>
- <span data-ttu-id="7663b-147">Arresto</span><span class="sxs-lookup"><span data-stu-id="7663b-147">Stopping</span></span>
- <span data-ttu-id="7663b-148">Sospeso</span><span class="sxs-lookup"><span data-stu-id="7663b-148">Suspended</span></span>
- <span data-ttu-id="7663b-149">Sospensione</span><span class="sxs-lookup"><span data-stu-id="7663b-149">Suspending</span></span>

```yaml
Type: String
Parameter Sets: ByAll, ByRunbookName
Aliases: 
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7663b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7663b-150">CommonParameters</span></span>
<span data-ttu-id="7663b-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7663b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7663b-152">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7663b-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7663b-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7663b-153">INPUTS</span></span>

### <span data-ttu-id="7663b-154">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7663b-154">None</span></span>
<span data-ttu-id="7663b-155">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="7663b-155">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7663b-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7663b-156">OUTPUTS</span></span>

### <span data-ttu-id="7663b-157">Microsoft. Azure. Commands. Automation. Model. job</span><span class="sxs-lookup"><span data-stu-id="7663b-157">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="7663b-158">Note</span><span class="sxs-lookup"><span data-stu-id="7663b-158">NOTES</span></span>

## <span data-ttu-id="7663b-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7663b-159">RELATED LINKS</span></span>

[<span data-ttu-id="7663b-160">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="7663b-160">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="7663b-161">Curriculum vitae-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="7663b-161">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="7663b-162">Stop-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="7663b-162">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="7663b-163">Suspend-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="7663b-163">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


