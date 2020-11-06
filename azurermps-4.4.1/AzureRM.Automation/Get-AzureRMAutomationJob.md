---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BD32B909-296B-4E46-A24F-6E2BD4B9764B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJob.md
ms.openlocfilehash: 4509190a8417379c9d5bc9eae9d6d12609def4aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93522003"
---
# <span data-ttu-id="c6e40-101">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="c6e40-101">Get-AzureRmAutomationJob</span></span>

## <span data-ttu-id="c6e40-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c6e40-102">SYNOPSIS</span></span>
<span data-ttu-id="c6e40-103">Ottiene i processi di automazione Runbook.</span><span class="sxs-lookup"><span data-stu-id="c6e40-103">Gets Automation runbook jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6e40-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c6e40-104">SYNTAX</span></span>

### <span data-ttu-id="c6e40-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c6e40-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c6e40-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="c6e40-106">ByJobId</span></span>
```
Get-AzureRmAutomationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6e40-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="c6e40-107">ByRunbookName</span></span>
```
Get-AzureRmAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6e40-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c6e40-108">DESCRIPTION</span></span>
<span data-ttu-id="c6e40-109">Il cmdlet **Get-AzureRmAutomationJob** ottiene i processi Runbook in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="c6e40-109">The **Get-AzureRmAutomationJob** cmdlet gets runbook jobs in Azure Automation.</span></span>

## <span data-ttu-id="c6e40-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c6e40-110">EXAMPLES</span></span>

### <span data-ttu-id="c6e40-111">Esempio 1: ottenere un processo di Runbook specifico</span><span class="sxs-lookup"><span data-stu-id="c6e40-111">Example 1: Get a specific runbook job</span></span>
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

<span data-ttu-id="c6e40-112">Questo comando ottiene il processo con il GUID specificato.</span><span class="sxs-lookup"><span data-stu-id="c6e40-112">This command gets the job that has the specified GUID.</span></span>

### <span data-ttu-id="c6e40-113">Esempio 2: ottenere tutti i processi per un Runbook</span><span class="sxs-lookup"><span data-stu-id="c6e40-113">Example 2: Get all jobs for a runbook</span></span>
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbook02"
```

<span data-ttu-id="c6e40-114">Questo comando consente di ottenere tutti i processi associati a un Runbook denominato Runbook02.</span><span class="sxs-lookup"><span data-stu-id="c6e40-114">This command gets all jobs associated with a runbook named Runbook02.</span></span>

### <span data-ttu-id="c6e40-115">Esempio 3: ottenere tutti i processi in uso</span><span class="sxs-lookup"><span data-stu-id="c6e40-115">Example 3: Get all running jobs</span></span>
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Status "Running"
```

<span data-ttu-id="c6e40-116">Questo comando consente di ottenere tutti i processi in uso nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="c6e40-116">This command gets all running jobs in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="c6e40-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c6e40-117">PARAMETERS</span></span>

### <span data-ttu-id="c6e40-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c6e40-118">-AutomationAccountName</span></span>
<span data-ttu-id="c6e40-119">Specifica il nome di un account di automazione per cui questo cmdlet ottiene i processi.</span><span class="sxs-lookup"><span data-stu-id="c6e40-119">Specifies the name of an Automation account for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="c6e40-120">-EndTime</span><span class="sxs-lookup"><span data-stu-id="c6e40-120">-EndTime</span></span>
<span data-ttu-id="c6e40-121">Specifica l'ora di fine di un processo come oggetto **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="c6e40-121">Specifies the end time for a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="c6e40-122">Puoi specificare una stringa che può essere convertita in un valore **DateTimeOffset** valido.</span><span class="sxs-lookup"><span data-stu-id="c6e40-122">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="c6e40-123">Questo cmdlet ottiene i processi che hanno un'ora di fine in corrispondenza o prima del valore specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="c6e40-123">This cmdlet gets jobs that have an end time at or before the value that this parameter specifies.</span></span>

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

### <span data-ttu-id="c6e40-124">-ID</span><span class="sxs-lookup"><span data-stu-id="c6e40-124">-Id</span></span>
<span data-ttu-id="c6e40-125">Specifica l'ID di un processo ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6e40-125">Specifies the ID of a job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c6e40-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6e40-126">-ResourceGroupName</span></span>
<span data-ttu-id="c6e40-127">Specifica il nome di un gruppo di risorse in cui il cmdlet ottiene i processi.</span><span class="sxs-lookup"><span data-stu-id="c6e40-127">Specifies the name of a resource group in which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="c6e40-128">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="c6e40-128">-RunbookName</span></span>
<span data-ttu-id="c6e40-129">Specifica il nome di un Runbook per cui questo cmdlet ottiene i processi.</span><span class="sxs-lookup"><span data-stu-id="c6e40-129">Specifies the name of a runbook for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="c6e40-130">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c6e40-130">-StartTime</span></span>
<span data-ttu-id="c6e40-131">Specifica l'ora di inizio di un processo come oggetto **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="c6e40-131">Specifies the start time of a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="c6e40-132">Questo cmdlet ottiene i processi che hanno un'ora di inizio o dopo il valore specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="c6e40-132">This cmdlet gets jobs that have a start time at or after the value that this parameter specifies.</span></span>

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

### <span data-ttu-id="c6e40-133">-Stato</span><span class="sxs-lookup"><span data-stu-id="c6e40-133">-Status</span></span>
<span data-ttu-id="c6e40-134">Specifica lo stato di un processo.</span><span class="sxs-lookup"><span data-stu-id="c6e40-134">Specifies the status of a job.</span></span>
<span data-ttu-id="c6e40-135">Questo cmdlet ottiene i processi che hanno uno stato corrispondente a questo parametro.</span><span class="sxs-lookup"><span data-stu-id="c6e40-135">This cmdlet gets jobs that have a status matching this parameter.</span></span>
<span data-ttu-id="c6e40-136">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="c6e40-136">Valid values are:</span></span> 

- <span data-ttu-id="c6e40-137">L'attivazione</span><span class="sxs-lookup"><span data-stu-id="c6e40-137">Activating</span></span>
- <span data-ttu-id="c6e40-138">Completato</span><span class="sxs-lookup"><span data-stu-id="c6e40-138">Completed</span></span>
- <span data-ttu-id="c6e40-139">Fallito</span><span class="sxs-lookup"><span data-stu-id="c6e40-139">Failed</span></span>
- <span data-ttu-id="c6e40-140">Accodati</span><span class="sxs-lookup"><span data-stu-id="c6e40-140">Queued</span></span>
- <span data-ttu-id="c6e40-141">Ripresa</span><span class="sxs-lookup"><span data-stu-id="c6e40-141">Resuming</span></span>
- <span data-ttu-id="c6e40-142">Esecuzione</span><span class="sxs-lookup"><span data-stu-id="c6e40-142">Running</span></span>
- <span data-ttu-id="c6e40-143">Iniziale</span><span class="sxs-lookup"><span data-stu-id="c6e40-143">Starting</span></span>
- <span data-ttu-id="c6e40-144">Ha smesso</span><span class="sxs-lookup"><span data-stu-id="c6e40-144">Stopped</span></span>
- <span data-ttu-id="c6e40-145">Arresto</span><span class="sxs-lookup"><span data-stu-id="c6e40-145">Stopping</span></span>
- <span data-ttu-id="c6e40-146">Sospeso</span><span class="sxs-lookup"><span data-stu-id="c6e40-146">Suspended</span></span>
- <span data-ttu-id="c6e40-147">Sospensione</span><span class="sxs-lookup"><span data-stu-id="c6e40-147">Suspending</span></span>

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

### <span data-ttu-id="c6e40-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6e40-148">-DefaultProfile</span></span>
<span data-ttu-id="c6e40-149">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c6e40-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6e40-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6e40-150">CommonParameters</span></span>
<span data-ttu-id="c6e40-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6e40-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6e40-152">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6e40-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6e40-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c6e40-153">INPUTS</span></span>

## <span data-ttu-id="c6e40-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c6e40-154">OUTPUTS</span></span>

### <span data-ttu-id="c6e40-155">Microsoft. Azure. Commands. Automation. Model. job</span><span class="sxs-lookup"><span data-stu-id="c6e40-155">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="c6e40-156">Note</span><span class="sxs-lookup"><span data-stu-id="c6e40-156">NOTES</span></span>

## <span data-ttu-id="c6e40-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c6e40-157">RELATED LINKS</span></span>

[<span data-ttu-id="c6e40-158">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="c6e40-158">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="c6e40-159">Curriculum vitae-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="c6e40-159">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="c6e40-160">Stop-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="c6e40-160">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="c6e40-161">Suspend-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="c6e40-161">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


