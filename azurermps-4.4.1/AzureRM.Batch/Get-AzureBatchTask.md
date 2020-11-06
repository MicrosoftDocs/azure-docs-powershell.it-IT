---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 4B5FE41A-090B-4859-B021-05CF0A8B7882
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTask.md
ms.openlocfilehash: fb01af87d28323e3e25c46868f94e892b835afc7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520551"
---
# <span data-ttu-id="36cf0-101">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="36cf0-101">Get-AzureBatchTask</span></span>

## <span data-ttu-id="36cf0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="36cf0-102">SYNOPSIS</span></span>
<span data-ttu-id="36cf0-103">Ottiene le attività batch per un processo.</span><span class="sxs-lookup"><span data-stu-id="36cf0-103">Gets the Batch tasks for a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36cf0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="36cf0-104">SYNTAX</span></span>

### <span data-ttu-id="36cf0-105">ODataFilter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="36cf0-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchTask [-JobId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="36cf0-106">ID</span><span class="sxs-lookup"><span data-stu-id="36cf0-106">Id</span></span>
```
Get-AzureBatchTask [-JobId] <String> [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36cf0-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="36cf0-107">ParentObject</span></span>
```
Get-AzureBatchTask [[-Job] <PSCloudJob>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="36cf0-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="36cf0-108">DESCRIPTION</span></span>
<span data-ttu-id="36cf0-109">Il cmdlet **Get-AzureBatchTask** ottiene le attività batch di Azure per un processo batch.</span><span class="sxs-lookup"><span data-stu-id="36cf0-109">The **Get-AzureBatchTask** cmdlet gets Azure Batch tasks for a Batch job.</span></span>
<span data-ttu-id="36cf0-110">Specificare un processo per il parametro *JobID* o per il parametro *Job* .</span><span class="sxs-lookup"><span data-stu-id="36cf0-110">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="36cf0-111">Per ottenere una singola attività, specificare il parametro *ID* .</span><span class="sxs-lookup"><span data-stu-id="36cf0-111">To get a single task, specify the *Id* parameter.</span></span>
<span data-ttu-id="36cf0-112">Puoi specificare il parametro *Filter* per ottenere le attività che corrispondono a un filtro OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="36cf0-112">You can specify the *Filter* parameter to get the tasks that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="36cf0-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="36cf0-113">EXAMPLES</span></span>

### <span data-ttu-id="36cf0-114">Esempio 1: ottenere un'attività in base all'ID</span><span class="sxs-lookup"><span data-stu-id="36cf0-114">Example 1: Get a task by ID</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job01" -Id "Task03" -BatchContext $Context
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

<span data-ttu-id="36cf0-115">Questo comando consente di ottenere l'attività con ID Task03 in Job Job01.</span><span class="sxs-lookup"><span data-stu-id="36cf0-115">This command gets the task with ID Task03 under job Job01.</span></span>
<span data-ttu-id="36cf0-116">Usa il cmdlet Get-AzureRmBatchAccountKeys per assegnare un contesto alla variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="36cf0-116">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="36cf0-117">Esempio 2: ottenere tutte le attività completate da un processo specificato</span><span class="sxs-lookup"><span data-stu-id="36cf0-117">Example 2: Get all completed tasks from a specified job</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job02" -Filter "state eq 'completed'" -BatchContext $Context
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

<span data-ttu-id="36cf0-118">Questo comando consente di ottenere le attività completate dal processo che contiene l'ID Job02.</span><span class="sxs-lookup"><span data-stu-id="36cf0-118">This command gets the completed tasks from the job that has the ID Job02.</span></span>

## <span data-ttu-id="36cf0-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="36cf0-119">PARAMETERS</span></span>

### <span data-ttu-id="36cf0-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="36cf0-120">-BatchContext</span></span>
<span data-ttu-id="36cf0-121">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="36cf0-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="36cf0-122">Per ottenere un oggetto **BatchAccountContext** che contiene i tasti di scelta per l'abbonamento, usare il cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="36cf0-122">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="36cf0-123">-Espandi</span><span class="sxs-lookup"><span data-stu-id="36cf0-123">-Expand</span></span>
<span data-ttu-id="36cf0-124">Specifica una clausola di espansione OData.</span><span class="sxs-lookup"><span data-stu-id="36cf0-124">Specifies an OData expand clause.</span></span>
<span data-ttu-id="36cf0-125">Specifica un valore per questo parametro per ottenere le entità associate dell'entità principale da ottenere.</span><span class="sxs-lookup"><span data-stu-id="36cf0-125">Specify a value for this parameter to get associated entities of the main entity to get.</span></span>

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

### <span data-ttu-id="36cf0-126">-Filtro</span><span class="sxs-lookup"><span data-stu-id="36cf0-126">-Filter</span></span>
<span data-ttu-id="36cf0-127">Specifica una clausola di filtro OData per le attività.</span><span class="sxs-lookup"><span data-stu-id="36cf0-127">Specifies an OData filter clause for tasks.</span></span>
<span data-ttu-id="36cf0-128">Se non si specifica un filtro, questo cmdlet restituisce tutte le attività per l'account batch o il processo.</span><span class="sxs-lookup"><span data-stu-id="36cf0-128">If you do not specify a filter, this cmdlet returns all tasks for the Batch account or job.</span></span>

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

### <span data-ttu-id="36cf0-129">-ID</span><span class="sxs-lookup"><span data-stu-id="36cf0-129">-Id</span></span>
<span data-ttu-id="36cf0-130">Specifica l'ID dell'attività ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36cf0-130">Specifies the ID of the task that this cmdlet gets.</span></span>
<span data-ttu-id="36cf0-131">Non è possibile specificare caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="36cf0-131">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="36cf0-132">-Job</span><span class="sxs-lookup"><span data-stu-id="36cf0-132">-Job</span></span>
<span data-ttu-id="36cf0-133">Specifica il processo che contiene le attività ottenute da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36cf0-133">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="36cf0-134">Per ottenere un oggetto **PSCloudJob** , usa il cmdlet Get-AzureBatchJob.</span><span class="sxs-lookup"><span data-stu-id="36cf0-134">To obtain a **PSCloudJob** object, use the Get-AzureBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="36cf0-135">-JobId</span><span class="sxs-lookup"><span data-stu-id="36cf0-135">-JobId</span></span>
<span data-ttu-id="36cf0-136">Specifica l'ID del processo che contiene le attività ottenute da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36cf0-136">Specifies the ID of the job that contains the tasks that this cmdlet gets.</span></span>

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

### <span data-ttu-id="36cf0-137">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="36cf0-137">-MaxCount</span></span>
<span data-ttu-id="36cf0-138">Specifica il numero massimo di attività da restituire.</span><span class="sxs-lookup"><span data-stu-id="36cf0-138">Specifies the maximum number of tasks to return.</span></span>
<span data-ttu-id="36cf0-139">Se specifichi un valore pari a zero (0) o meno, il cmdlet non usa un limite superiore.</span><span class="sxs-lookup"><span data-stu-id="36cf0-139">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="36cf0-140">Il valore predefinito è 1000.</span><span class="sxs-lookup"><span data-stu-id="36cf0-140">The default value is 1000.</span></span>

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

### <span data-ttu-id="36cf0-141">-Selezionare</span><span class="sxs-lookup"><span data-stu-id="36cf0-141">-Select</span></span>
<span data-ttu-id="36cf0-142">Specifica una clausola di selezione OData.</span><span class="sxs-lookup"><span data-stu-id="36cf0-142">Specifies an OData select clause.</span></span>
<span data-ttu-id="36cf0-143">Specifica un valore per questo parametro per ottenere proprietà specifiche anziché tutte le proprietà dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="36cf0-143">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="36cf0-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36cf0-144">-DefaultProfile</span></span>
<span data-ttu-id="36cf0-145">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="36cf0-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36cf0-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36cf0-146">CommonParameters</span></span>
<span data-ttu-id="36cf0-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36cf0-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36cf0-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36cf0-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36cf0-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="36cf0-149">INPUTS</span></span>

### <span data-ttu-id="36cf0-150">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="36cf0-150">BatchAccountContext</span></span>
<span data-ttu-id="36cf0-151">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="36cf0-151">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="36cf0-152">PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="36cf0-152">PSCloudJob</span></span>
<span data-ttu-id="36cf0-153">Il parametro "Job" accetta il valore di tipo "PSCloudJob" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="36cf0-153">Parameter 'Job' accepts value of type 'PSCloudJob' from the pipeline</span></span>

## <span data-ttu-id="36cf0-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="36cf0-154">OUTPUTS</span></span>

### <span data-ttu-id="36cf0-155">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="36cf0-155">PSCloudTask</span></span>

## <span data-ttu-id="36cf0-156">Note</span><span class="sxs-lookup"><span data-stu-id="36cf0-156">NOTES</span></span>

## <span data-ttu-id="36cf0-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="36cf0-157">RELATED LINKS</span></span>

[<span data-ttu-id="36cf0-158">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="36cf0-158">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="36cf0-159">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="36cf0-159">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="36cf0-160">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="36cf0-160">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="36cf0-161">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="36cf0-161">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="36cf0-162">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="36cf0-162">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="36cf0-163">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="36cf0-163">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


