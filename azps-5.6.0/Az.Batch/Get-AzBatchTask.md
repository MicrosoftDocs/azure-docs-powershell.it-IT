---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 4B5FE41A-090B-4859-B021-05CF0A8B7882
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTask.md
ms.openlocfilehash: 214ee3b030757da9acf632b2768a94b1ab026cc6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012718"
---
# <span data-ttu-id="c6785-101">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="c6785-101">Get-AzBatchTask</span></span>

## <span data-ttu-id="c6785-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6785-102">SYNOPSIS</span></span>
<span data-ttu-id="c6785-103">Recupera le attività batch per un processo.</span><span class="sxs-lookup"><span data-stu-id="c6785-103">Gets the Batch tasks for a job.</span></span>

## <span data-ttu-id="c6785-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c6785-104">SYNTAX</span></span>

### <span data-ttu-id="c6785-105">ODataFilter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c6785-105">ODataFilter (Default)</span></span>
```
Get-AzBatchTask [-JobId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6785-106">ID</span><span class="sxs-lookup"><span data-stu-id="c6785-106">Id</span></span>
```
Get-AzBatchTask [-JobId] <String> [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6785-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="c6785-107">ParentObject</span></span>
```
Get-AzBatchTask [[-Job] <PSCloudJob>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c6785-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c6785-108">DESCRIPTION</span></span>
<span data-ttu-id="c6785-109">Il **cmdlet Get-AzBatchTask** ottiene le attività batch di Azure per un processo batch.</span><span class="sxs-lookup"><span data-stu-id="c6785-109">The **Get-AzBatchTask** cmdlet gets Azure Batch tasks for a Batch job.</span></span>
<span data-ttu-id="c6785-110">Specificare un processo usando il parametro *JobId* o *Job.*</span><span class="sxs-lookup"><span data-stu-id="c6785-110">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="c6785-111">Per ottenere una singola attività, specificare il *parametro ID.*</span><span class="sxs-lookup"><span data-stu-id="c6785-111">To get a single task, specify the *Id* parameter.</span></span>
<span data-ttu-id="c6785-112">È possibile specificare il *parametro Filter* per ottenere le attività che corrispondono a un filtro OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="c6785-112">You can specify the *Filter* parameter to get the tasks that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="c6785-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c6785-113">EXAMPLES</span></span>

### <span data-ttu-id="c6785-114">Esempio 1: Ottenere un'attività in base all'ID</span><span class="sxs-lookup"><span data-stu-id="c6785-114">Example 1: Get a task by ID</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job01" -Id "Task03" -BatchContext $Context
AffinityInformation         :
CommandLine                 : cmd /c dir /s
ComputeNodeInformation      : Microsoft.Azure.Commands.Batch.Models.PSComputeNodeInformation
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
CreationTime                : 7/25/2015 11:24:52 PM
DisplayName                 :
EnvironmentSettings         :
ETag                        : 0x8D295483E08BD9D
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSTaskExecutionInformation
Id                          : Task03
LastModified                : 7/25/2015 11:24:52 PM
PreviousState               : Running
PreviousStateTransitionTime : 7/25/2015 11:24:59 PM
ResourceFiles               :
RunElevated                 : False
State                       : Completed
StateTransitionTime         : 7/25/2015 11:24:59 PM
Statistics                  :
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job01/tasks/Task03
```

<span data-ttu-id="c6785-115">Questo comando recupera l'attività con ID Attività03 nel processo Job01.</span><span class="sxs-lookup"><span data-stu-id="c6785-115">This command gets the task with ID Task03 under job Job01.</span></span>
<span data-ttu-id="c6785-116">Usare il cmdlet Get-AzBatchAccountKey per assegnare un contesto alla $Context variabile.</span><span class="sxs-lookup"><span data-stu-id="c6785-116">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="c6785-117">Esempio 2: Recuperare tutte le attività completate da un processo specificato</span><span class="sxs-lookup"><span data-stu-id="c6785-117">Example 2: Get all completed tasks from a specified job</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job02" -Filter "state eq 'completed'" -BatchContext $Context
AffinityInformation         :
CommandLine                 : cmd /c dir /s
ComputeNodeInformation      : Microsoft.Azure.Commands.Batch.Models.PSComputeNodeInformation
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
CreationTime                : 3/24/2015 10:21:51 PM
EnvironmentSettings         :
ETag                        : 0x8D295483E08BD9D
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSTaskExecutionInformation
Id                          : Task17
LastModified                : 3/24/2015 10:21:51 PM
PreviousState               : Running
PreviousStateTransitionTime : 3/24/2015 10:22:00 PM
ResourceFiles               :
RunElevated                 : False
State                       : Completed
StateTransitionTime         : 3/24/2015 10:22:00 PM
Statistics                  :
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job02/tasks/Task17

AffinityInformation         :
CommandLine                 : cmd /c echo hello > newFile.txt
ComputeNodeInformation      : Microsoft.Azure.Commands.Batch.Models.PSComputeNodeInformation
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
CreationTime                : 3/24/2015 10:21:51 PM
EnvironmentSettings         :
ETag                        : 0x8D295483E08BD9D
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSTaskExecutionInformation
Id                          : Task27
LastModified                : 3/24/2015 10:23:35 PM
PreviousState               : Running
PreviousStateTransitionTime : 3/24/2015 10:23:37 PM
ResourceFiles               :
RunElevated                 : True
State                       : Completed
StateTransitionTime         : 3/24/2015 10:23:37 PM
Statistics                  :
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job02/tasks/Task27
```

<span data-ttu-id="c6785-118">Questo comando recupera le attività completate dal processo con ID Processo02.</span><span class="sxs-lookup"><span data-stu-id="c6785-118">This command gets the completed tasks from the job that has the ID Job02.</span></span>

## <span data-ttu-id="c6785-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6785-119">PARAMETERS</span></span>

### <span data-ttu-id="c6785-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c6785-120">-BatchContext</span></span>
<span data-ttu-id="c6785-121">Specifica **l'istanza BatchAccountContext** che questo cmdlet usa per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="c6785-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c6785-122">Se si usa il cmdlet Get-AzBatchAccount per ottenere BatchAccountContext, verrà usata l'autenticazione di Azure Active Directory quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="c6785-122">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c6785-123">Per usare invece l'autenticazione della chiave condivisa, usare il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.</span><span class="sxs-lookup"><span data-stu-id="c6785-123">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c6785-124">Quando si usa l'autenticazione con chiave condivisa, per impostazione predefinita viene usata la chiave di accesso primario.</span><span class="sxs-lookup"><span data-stu-id="c6785-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c6785-125">Per modificare la chiave da usare, impostare la proprietà BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="c6785-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6785-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6785-126">-DefaultProfile</span></span>
<span data-ttu-id="c6785-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c6785-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6785-128">-Expand</span><span class="sxs-lookup"><span data-stu-id="c6785-128">-Expand</span></span>
<span data-ttu-id="c6785-129">Specifica una clausola di espansione OData.</span><span class="sxs-lookup"><span data-stu-id="c6785-129">Specifies an OData expand clause.</span></span>
<span data-ttu-id="c6785-130">Specificare un valore per questo parametro per ottenere le entità associate dell'entità principale da ottenere.</span><span class="sxs-lookup"><span data-stu-id="c6785-130">Specify a value for this parameter to get associated entities of the main entity to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6785-131">-Filter</span><span class="sxs-lookup"><span data-stu-id="c6785-131">-Filter</span></span>
<span data-ttu-id="c6785-132">Specifica una clausola del filtro OData per le attività.</span><span class="sxs-lookup"><span data-stu-id="c6785-132">Specifies an OData filter clause for tasks.</span></span>
<span data-ttu-id="c6785-133">Se non si specifica un filtro, questo cmdlet restituisce tutte le attività per l'account o il processo Batch.</span><span class="sxs-lookup"><span data-stu-id="c6785-133">If you do not specify a filter, this cmdlet returns all tasks for the Batch account or job.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter, ParentObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6785-134">-Id</span><span class="sxs-lookup"><span data-stu-id="c6785-134">-Id</span></span>
<span data-ttu-id="c6785-135">Specifica l'ID dell'attività che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6785-135">Specifies the ID of the task that this cmdlet gets.</span></span>
<span data-ttu-id="c6785-136">Non è possibile specificare caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="c6785-136">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6785-137">-Job</span><span class="sxs-lookup"><span data-stu-id="c6785-137">-Job</span></span>
<span data-ttu-id="c6785-138">Specifica il processo che contiene le attività recuperate da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6785-138">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="c6785-139">Per ottenere un **oggetto PSCloudJob,** usare il cmdlet Get-AzBatchJob.</span><span class="sxs-lookup"><span data-stu-id="c6785-139">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6785-140">-JobId</span><span class="sxs-lookup"><span data-stu-id="c6785-140">-JobId</span></span>
<span data-ttu-id="c6785-141">Specifica l'ID del processo che contiene le attività che questo cmdlet ottiene.</span><span class="sxs-lookup"><span data-stu-id="c6785-141">Specifies the ID of the job that contains the tasks that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter, Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6785-142">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="c6785-142">-MaxCount</span></span>
<span data-ttu-id="c6785-143">Specifica il numero massimo di attività da restituire.</span><span class="sxs-lookup"><span data-stu-id="c6785-143">Specifies the maximum number of tasks to return.</span></span>
<span data-ttu-id="c6785-144">Se si specifica un valore uguale o inferiore a zero (0), il cmdlet non usa un limite superiore.</span><span class="sxs-lookup"><span data-stu-id="c6785-144">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="c6785-145">Il valore predefinito è 1000.</span><span class="sxs-lookup"><span data-stu-id="c6785-145">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter, ParentObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6785-146">-Select</span><span class="sxs-lookup"><span data-stu-id="c6785-146">-Select</span></span>
<span data-ttu-id="c6785-147">Specifica una clausola di selezione OData.</span><span class="sxs-lookup"><span data-stu-id="c6785-147">Specifies an OData select clause.</span></span>
<span data-ttu-id="c6785-148">Specificare un valore per questo parametro per ottenere proprietà specifiche invece di tutte le proprietà dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c6785-148">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6785-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6785-149">CommonParameters</span></span>
<span data-ttu-id="c6785-150">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6785-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6785-151">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c6785-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6785-152">INPUT</span><span class="sxs-lookup"><span data-stu-id="c6785-152">INPUTS</span></span>

### <span data-ttu-id="c6785-153">System.String</span><span class="sxs-lookup"><span data-stu-id="c6785-153">System.String</span></span>

### <span data-ttu-id="c6785-154">Microsoft.Azure.Commands.Batch. Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="c6785-154">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="c6785-155">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c6785-155">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="c6785-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c6785-156">OUTPUTS</span></span>

### <span data-ttu-id="c6785-157">Microsoft.Azure.Commands.Batch. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="c6785-157">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

## <span data-ttu-id="c6785-158">NOTE</span><span class="sxs-lookup"><span data-stu-id="c6785-158">NOTES</span></span>

## <span data-ttu-id="c6785-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c6785-159">RELATED LINKS</span></span>

[<span data-ttu-id="c6785-160">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="c6785-160">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="c6785-161">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="c6785-161">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="c6785-162">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="c6785-162">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="c6785-163">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="c6785-163">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="c6785-164">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="c6785-164">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="c6785-165">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="c6785-165">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
