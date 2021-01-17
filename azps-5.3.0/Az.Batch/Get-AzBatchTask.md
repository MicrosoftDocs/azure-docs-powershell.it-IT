---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 4B5FE41A-090B-4859-B021-05CF0A8B7882
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTask.md
ms.openlocfilehash: bf1a70dc697366099f1949878e81a25bd3adb0fa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478312"
---
# <span data-ttu-id="5e30c-101">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="5e30c-101">Get-AzBatchTask</span></span>

## <span data-ttu-id="5e30c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5e30c-102">SYNOPSIS</span></span>
<span data-ttu-id="5e30c-103">Ottiene le attività batch per un processo.</span><span class="sxs-lookup"><span data-stu-id="5e30c-103">Gets the Batch tasks for a job.</span></span>

## <span data-ttu-id="5e30c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5e30c-104">SYNTAX</span></span>

### <span data-ttu-id="5e30c-105">ODataFilter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5e30c-105">ODataFilter (Default)</span></span>
```
Get-AzBatchTask [-JobId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e30c-106">ID</span><span class="sxs-lookup"><span data-stu-id="5e30c-106">Id</span></span>
```
Get-AzBatchTask [-JobId] <String> [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e30c-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="5e30c-107">ParentObject</span></span>
```
Get-AzBatchTask [[-Job] <PSCloudJob>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5e30c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e30c-108">DESCRIPTION</span></span>
<span data-ttu-id="5e30c-109">Il cmdlet **Get-AzBatchTask** ottiene le attività batch di Azure per un processo batch.</span><span class="sxs-lookup"><span data-stu-id="5e30c-109">The **Get-AzBatchTask** cmdlet gets Azure Batch tasks for a Batch job.</span></span>
<span data-ttu-id="5e30c-110">Specificare un processo per il parametro *JobID* o per il parametro *Job* .</span><span class="sxs-lookup"><span data-stu-id="5e30c-110">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="5e30c-111">Per ottenere una singola attività, specificare il parametro *ID* .</span><span class="sxs-lookup"><span data-stu-id="5e30c-111">To get a single task, specify the *Id* parameter.</span></span>
<span data-ttu-id="5e30c-112">Puoi specificare il parametro *Filter* per ottenere le attività che corrispondono a un filtro OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="5e30c-112">You can specify the *Filter* parameter to get the tasks that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="5e30c-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5e30c-113">EXAMPLES</span></span>

### <span data-ttu-id="5e30c-114">Esempio 1: ottenere un'attività in base all'ID</span><span class="sxs-lookup"><span data-stu-id="5e30c-114">Example 1: Get a task by ID</span></span>
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

<span data-ttu-id="5e30c-115">Questo comando consente di ottenere l'attività con ID Task03 in Job Job01.</span><span class="sxs-lookup"><span data-stu-id="5e30c-115">This command gets the task with ID Task03 under job Job01.</span></span>
<span data-ttu-id="5e30c-116">Usa il cmdlet Get-AzBatchAccountKey per assegnare un contesto alla variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="5e30c-116">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="5e30c-117">Esempio 2: ottenere tutte le attività completate da un processo specificato</span><span class="sxs-lookup"><span data-stu-id="5e30c-117">Example 2: Get all completed tasks from a specified job</span></span>
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

<span data-ttu-id="5e30c-118">Questo comando consente di ottenere le attività completate dal processo che contiene l'ID Job02.</span><span class="sxs-lookup"><span data-stu-id="5e30c-118">This command gets the completed tasks from the job that has the ID Job02.</span></span>

## <span data-ttu-id="5e30c-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5e30c-119">PARAMETERS</span></span>

### <span data-ttu-id="5e30c-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="5e30c-120">-BatchContext</span></span>
<span data-ttu-id="5e30c-121">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="5e30c-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5e30c-122">Se si usa il cmdlet Get-AzBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="5e30c-122">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="5e30c-123">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="5e30c-123">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="5e30c-124">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="5e30c-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="5e30c-125">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="5e30c-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="5e30c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e30c-126">-DefaultProfile</span></span>
<span data-ttu-id="5e30c-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5e30c-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e30c-128">-Espandi</span><span class="sxs-lookup"><span data-stu-id="5e30c-128">-Expand</span></span>
<span data-ttu-id="5e30c-129">Specifica una clausola di espansione OData.</span><span class="sxs-lookup"><span data-stu-id="5e30c-129">Specifies an OData expand clause.</span></span>
<span data-ttu-id="5e30c-130">Specifica un valore per questo parametro per ottenere le entità associate dell'entità principale da ottenere.</span><span class="sxs-lookup"><span data-stu-id="5e30c-130">Specify a value for this parameter to get associated entities of the main entity to get.</span></span>

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

### <span data-ttu-id="5e30c-131">-Filtro</span><span class="sxs-lookup"><span data-stu-id="5e30c-131">-Filter</span></span>
<span data-ttu-id="5e30c-132">Specifica una clausola di filtro OData per le attività.</span><span class="sxs-lookup"><span data-stu-id="5e30c-132">Specifies an OData filter clause for tasks.</span></span>
<span data-ttu-id="5e30c-133">Se non si specifica un filtro, questo cmdlet restituisce tutte le attività per l'account batch o il processo.</span><span class="sxs-lookup"><span data-stu-id="5e30c-133">If you do not specify a filter, this cmdlet returns all tasks for the Batch account or job.</span></span>

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

### <span data-ttu-id="5e30c-134">-ID</span><span class="sxs-lookup"><span data-stu-id="5e30c-134">-Id</span></span>
<span data-ttu-id="5e30c-135">Specifica l'ID dell'attività ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e30c-135">Specifies the ID of the task that this cmdlet gets.</span></span>
<span data-ttu-id="5e30c-136">Non è possibile specificare caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="5e30c-136">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="5e30c-137">-Job</span><span class="sxs-lookup"><span data-stu-id="5e30c-137">-Job</span></span>
<span data-ttu-id="5e30c-138">Specifica il processo che contiene le attività ottenute da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e30c-138">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="5e30c-139">Per ottenere un oggetto **PSCloudJob** , usa il cmdlet Get-AzBatchJob.</span><span class="sxs-lookup"><span data-stu-id="5e30c-139">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="5e30c-140">-JobId</span><span class="sxs-lookup"><span data-stu-id="5e30c-140">-JobId</span></span>
<span data-ttu-id="5e30c-141">Specifica l'ID del processo che contiene le attività ottenute da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e30c-141">Specifies the ID of the job that contains the tasks that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5e30c-142">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="5e30c-142">-MaxCount</span></span>
<span data-ttu-id="5e30c-143">Specifica il numero massimo di attività da restituire.</span><span class="sxs-lookup"><span data-stu-id="5e30c-143">Specifies the maximum number of tasks to return.</span></span>
<span data-ttu-id="5e30c-144">Se specifichi un valore pari a zero (0) o meno, il cmdlet non usa un limite superiore.</span><span class="sxs-lookup"><span data-stu-id="5e30c-144">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="5e30c-145">Il valore predefinito è 1000.</span><span class="sxs-lookup"><span data-stu-id="5e30c-145">The default value is 1000.</span></span>

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

### <span data-ttu-id="5e30c-146">-Selezionare</span><span class="sxs-lookup"><span data-stu-id="5e30c-146">-Select</span></span>
<span data-ttu-id="5e30c-147">Specifica una clausola di selezione OData.</span><span class="sxs-lookup"><span data-stu-id="5e30c-147">Specifies an OData select clause.</span></span>
<span data-ttu-id="5e30c-148">Specifica un valore per questo parametro per ottenere proprietà specifiche anziché tutte le proprietà dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5e30c-148">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="5e30c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e30c-149">CommonParameters</span></span>
<span data-ttu-id="5e30c-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e30c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e30c-151">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e30c-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e30c-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5e30c-152">INPUTS</span></span>

### <span data-ttu-id="5e30c-153">System. String</span><span class="sxs-lookup"><span data-stu-id="5e30c-153">System.String</span></span>

### <span data-ttu-id="5e30c-154">Microsoft.Azure.Commands.Batch. Models. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="5e30c-154">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="5e30c-155">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5e30c-155">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="5e30c-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5e30c-156">OUTPUTS</span></span>

### <span data-ttu-id="5e30c-157">Microsoft.Azure.Commands.Batch. Models. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="5e30c-157">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

## <span data-ttu-id="5e30c-158">Note</span><span class="sxs-lookup"><span data-stu-id="5e30c-158">NOTES</span></span>

## <span data-ttu-id="5e30c-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5e30c-159">RELATED LINKS</span></span>

[<span data-ttu-id="5e30c-160">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="5e30c-160">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="5e30c-161">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="5e30c-161">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="5e30c-162">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="5e30c-162">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="5e30c-163">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="5e30c-163">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="5e30c-164">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="5e30c-164">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="5e30c-165">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="5e30c-165">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
