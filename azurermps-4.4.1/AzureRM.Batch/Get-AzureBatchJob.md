---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 8BF49C4D-E7CD-4FD0-AFAC-9856239D24EC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJob.md
ms.openlocfilehash: c2aa673b9cd0f8cccc3f1a8721313f5a3236270d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516295"
---
# <span data-ttu-id="b99b0-101">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="b99b0-101">Get-AzureBatchJob</span></span>

## <span data-ttu-id="b99b0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b99b0-102">SYNOPSIS</span></span>
<span data-ttu-id="b99b0-103">Consente di ottenere processi batch per un account batch o una pianificazione processi.</span><span class="sxs-lookup"><span data-stu-id="b99b0-103">Gets Batch jobs for a Batch account or job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b99b0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b99b0-104">SYNTAX</span></span>

### <span data-ttu-id="b99b0-105">ODataFilter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b99b0-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchJob [-JobScheduleId <String>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b99b0-106">ID</span><span class="sxs-lookup"><span data-stu-id="b99b0-106">Id</span></span>
```
Get-AzureBatchJob [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b99b0-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="b99b0-107">ParentObject</span></span>
```
Get-AzureBatchJob [[-JobSchedule] <PSCloudJobSchedule>] [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b99b0-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b99b0-108">DESCRIPTION</span></span>
<span data-ttu-id="b99b0-109">Il cmdlet **Get-AzureBatchJob** ottiene i processi batch di Azure per l'account batch specificato dal parametro *BatchAccountContext* .</span><span class="sxs-lookup"><span data-stu-id="b99b0-109">The **Get-AzureBatchJob** cmdlet gets the Azure Batch jobs for the Batch account specified by the *BatchAccountContext* parameter.</span></span>
<span data-ttu-id="b99b0-110">Puoi usare il parametro *ID* per ottenere un singolo processo.</span><span class="sxs-lookup"><span data-stu-id="b99b0-110">You can use the *Id* parameter to get a single job.</span></span>
<span data-ttu-id="b99b0-111">Puoi usare il parametro *Filter* per ottenere i processi che corrispondono a un filtro OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="b99b0-111">You can use the *Filter* parameter to get the jobs that match an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="b99b0-112">Se si specifica un ID pianificazione processi o un'istanza di **PSCloudJobSchedule** , questo cmdlet restituisce solo i processi per la pianificazione del processo.</span><span class="sxs-lookup"><span data-stu-id="b99b0-112">If you supply a job schedule ID or **PSCloudJobSchedule** instance, this cmdlet returns only the jobs for that job schedule.</span></span>

## <span data-ttu-id="b99b0-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b99b0-113">EXAMPLES</span></span>

### <span data-ttu-id="b99b0-114">Esempio 1: ottenere un processo batch per ID</span><span class="sxs-lookup"><span data-stu-id="b99b0-114">Example 1: Get a Batch job by ID</span></span>
```
PS C:\>Get-AzureBatchJob -Id "Job01" -BatchContext $Context
CommonEnvironmentSettings   : 
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
CreationTime                : 7/25/2015 9:12:07 PM
DisplayName                 : 
ETag                        : 0x8D29535B2941439
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobExecutionInformation
Id                          : Job01
JobManagerTask              : 
JobPreparationTask          : 
JobReleaseTask              : 
LastModified                : 7/25/2015 9:12:07 PM
Metadata                    : 
PoolInformation             : Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
PreviousState               : 
PreviousStateTransitionTime : 
Priority                    : 0
State                       : Active
StateTransitionTime         : 7/25/2015 9:12:07 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job01
```

<span data-ttu-id="b99b0-115">Questo comando ottiene il processo con ID Job01.</span><span class="sxs-lookup"><span data-stu-id="b99b0-115">This command gets the job that has the ID Job01.</span></span>
<span data-ttu-id="b99b0-116">Usa il cmdlet Get-AzureRmBatchAccountKeys per assegnare un contesto alla variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="b99b0-116">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="b99b0-117">Esempio 2: ottenere tutti i processi attivi per una pianificazione del processo</span><span class="sxs-lookup"><span data-stu-id="b99b0-117">Example 2: Get all active jobs for a job schedule</span></span>
```
PS C:\>Get-AzureBatchJob -JobScheduleId "JobSchedule27" -Filter "state eq 'active'" -BatchContext $Context
CommonEnvironmentSettings   : 
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
CreationTime                : 7/25/2015 9:15:44 PM
DisplayName                 : 
ETag                        : 0x8D2953633DD13E1
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobExecutionInformation
Id                          : JobSchedule27:job-1
JobManagerTask              : 
JobPreparationTask          : 
JobReleaseTask              : 
LastModified                : 7/25/2015 9:15:44 PM
Metadata                    : 
PoolInformation             : Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
PreviousState               : 
PreviousStateTransitionTime : 
Priority                    : 0
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:44 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/JobSchedule27:job-1
```

<span data-ttu-id="b99b0-118">Questo comando consente di ottenere i processi attivi per la pianificazione del processo con ID JobSchedule27.</span><span class="sxs-lookup"><span data-stu-id="b99b0-118">This command gets the active jobs for the job schedule that has the ID JobSchedule27.</span></span>

### <span data-ttu-id="b99b0-119">Esempio 3: ottiene tutti i processi in una pianificazione processo tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="b99b0-119">Example 3: Gets all jobs under a job schedule by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchJobSchedule -Id "JobSchedule27" -BatchContext $Context | Get-AzureBatchJob -BatchContext $Context
CommonEnvironmentSettings   : 
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
CreationTime                : 7/25/2015 9:15:44 PM
DisplayName                 : 
ETag                        : 0x8D2953633DD13E1
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobExecutionInformation
Id                          : JobSchedule27:job-1
JobManagerTask              : 
JobPreparationTask          : 
JobReleaseTask              : 
LastModified                : 7/25/2015 9:15:44 PM
Metadata                    : 
PoolInformation             : Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
PreviousState               : 
PreviousStateTransitionTime : 
Priority                    : 0
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:44 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/JobSchedule27:job-1
```

<span data-ttu-id="b99b0-120">Questo comando consente di ottenere la pianificazione del processo che contiene l'ID JobSchedule27 usando il cmdlet Get-AzureBatchJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="b99b0-120">This command gets the job schedule that has the ID JobSchedule27 by using the Get-AzureBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="b99b0-121">Il comando passa la pianificazione del processo al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="b99b0-121">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b99b0-122">Il comando ottiene tutti i processi per la pianificazione del processo.</span><span class="sxs-lookup"><span data-stu-id="b99b0-122">The command gets all jobs for that job schedule.</span></span>

## <span data-ttu-id="b99b0-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b99b0-123">PARAMETERS</span></span>

### <span data-ttu-id="b99b0-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b99b0-124">-BatchContext</span></span>
<span data-ttu-id="b99b0-125">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="b99b0-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b99b0-126">Per ottenere un oggetto **BatchAccountContext** che contiene i tasti di scelta per l'abbonamento, usare il cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="b99b0-126">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="b99b0-127">-Espandi</span><span class="sxs-lookup"><span data-stu-id="b99b0-127">-Expand</span></span>
<span data-ttu-id="b99b0-128">Specifica una clausola di espansione OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="b99b0-128">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="b99b0-129">Specifica un valore per questo parametro per ottenere le entità associate dell'entità principale che ottieni.</span><span class="sxs-lookup"><span data-stu-id="b99b0-129">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="b99b0-130">-Filtro</span><span class="sxs-lookup"><span data-stu-id="b99b0-130">-Filter</span></span>
<span data-ttu-id="b99b0-131">Specifica una clausola di filtro OData per i processi.</span><span class="sxs-lookup"><span data-stu-id="b99b0-131">Specifies an OData filter clause for jobs.</span></span>
<span data-ttu-id="b99b0-132">Se non si specifica un filtro, questo cmdlet restituisce tutti i processi per l'account batch o per la pianificazione del processo.</span><span class="sxs-lookup"><span data-stu-id="b99b0-132">If you do not specify a filter, this cmdlet returns all jobs for the Batch account or job schedule.</span></span>

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

### <span data-ttu-id="b99b0-133">-ID</span><span class="sxs-lookup"><span data-stu-id="b99b0-133">-Id</span></span>
<span data-ttu-id="b99b0-134">Specifica l'ID del processo ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b99b0-134">Specifies the ID of the job that this cmdlet gets.</span></span>
<span data-ttu-id="b99b0-135">Non è possibile specificare caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="b99b0-135">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b99b0-136">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="b99b0-136">-JobSchedule</span></span>
<span data-ttu-id="b99b0-137">Specifica un oggetto **PSCloudJobSchedule** che rappresenta la pianificazione del processo che contiene i processi.</span><span class="sxs-lookup"><span data-stu-id="b99b0-137">Specifies a **PSCloudJobSchedule** object that represents the job schedule which contains the jobs.</span></span>
<span data-ttu-id="b99b0-138">Per ottenere un oggetto **PSCloudJobSchedule** , usa il cmdlet Get-AzureBatchJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="b99b0-138">To obtain a **PSCloudJobSchedule** object, use the Get-AzureBatchJobSchedule cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b99b0-139">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="b99b0-139">-JobScheduleId</span></span>
<span data-ttu-id="b99b0-140">Specifica l'ID della pianificazione del processo che contiene i processi.</span><span class="sxs-lookup"><span data-stu-id="b99b0-140">Specifies the ID of the job schedule which contains the jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b99b0-141">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="b99b0-141">-MaxCount</span></span>
<span data-ttu-id="b99b0-142">Specifica il numero massimo di processi da restituire.</span><span class="sxs-lookup"><span data-stu-id="b99b0-142">Specifies the maximum number of jobs to return.</span></span>
<span data-ttu-id="b99b0-143">Se specifichi un valore pari a zero (0) o meno, il cmdlet non usa un limite superiore.</span><span class="sxs-lookup"><span data-stu-id="b99b0-143">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="b99b0-144">Il valore predefinito è 1000.</span><span class="sxs-lookup"><span data-stu-id="b99b0-144">The default value is 1000.</span></span>

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

### <span data-ttu-id="b99b0-145">-Selezionare</span><span class="sxs-lookup"><span data-stu-id="b99b0-145">-Select</span></span>
<span data-ttu-id="b99b0-146">Specifica una clausola di selezione OData.</span><span class="sxs-lookup"><span data-stu-id="b99b0-146">Specifies an OData select clause.</span></span>
<span data-ttu-id="b99b0-147">Specifica un valore per questo parametro per ottenere proprietà specifiche anziché tutte le proprietà dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b99b0-147">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="b99b0-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b99b0-148">-DefaultProfile</span></span>
<span data-ttu-id="b99b0-149">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b99b0-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b99b0-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b99b0-150">CommonParameters</span></span>
<span data-ttu-id="b99b0-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b99b0-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b99b0-152">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b99b0-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b99b0-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b99b0-153">INPUTS</span></span>

### <span data-ttu-id="b99b0-154">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b99b0-154">BatchAccountContext</span></span>
<span data-ttu-id="b99b0-155">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="b99b0-155">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="b99b0-156">PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b99b0-156">PSCloudJobSchedule</span></span>
<span data-ttu-id="b99b0-157">Il parametro ' JobSchedule ' accetta il valore di tipo ' PSCloudJobSchedule ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="b99b0-157">Parameter 'JobSchedule' accepts value of type 'PSCloudJobSchedule' from the pipeline</span></span>

## <span data-ttu-id="b99b0-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b99b0-158">OUTPUTS</span></span>

### <span data-ttu-id="b99b0-159">PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="b99b0-159">PSCloudJob</span></span>

## <span data-ttu-id="b99b0-160">Note</span><span class="sxs-lookup"><span data-stu-id="b99b0-160">NOTES</span></span>

## <span data-ttu-id="b99b0-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b99b0-161">RELATED LINKS</span></span>

[<span data-ttu-id="b99b0-162">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="b99b0-162">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="b99b0-163">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="b99b0-163">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="b99b0-164">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b99b0-164">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="b99b0-165">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b99b0-165">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="b99b0-166">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="b99b0-166">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="b99b0-167">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="b99b0-167">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="b99b0-168">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="b99b0-168">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="b99b0-169">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="b99b0-169">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


