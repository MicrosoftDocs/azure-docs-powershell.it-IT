---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 8BF49C4D-E7CD-4FD0-AFAC-9856239D24EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJob.md
ms.openlocfilehash: 332bdb8d32b42d391518d50aef82436675cf3f9e
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2020
ms.locfileid: "93685354"
---
# <span data-ttu-id="2b58c-101">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2b58c-101">Get-AzBatchJob</span></span>

## <span data-ttu-id="2b58c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2b58c-102">SYNOPSIS</span></span>
<span data-ttu-id="2b58c-103">Consente di ottenere processi batch per un account batch o una pianificazione processi.</span><span class="sxs-lookup"><span data-stu-id="2b58c-103">Gets Batch jobs for a Batch account or job schedule.</span></span>

## <span data-ttu-id="2b58c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2b58c-104">SYNTAX</span></span>

### <span data-ttu-id="2b58c-105">ODataFilter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2b58c-105">ODataFilter (Default)</span></span>
```
Get-AzBatchJob [-JobScheduleId <String>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b58c-106">ID</span><span class="sxs-lookup"><span data-stu-id="2b58c-106">Id</span></span>
```
Get-AzBatchJob [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b58c-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="2b58c-107">ParentObject</span></span>
```
Get-AzBatchJob [[-JobSchedule] <PSCloudJobSchedule>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2b58c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b58c-108">DESCRIPTION</span></span>
<span data-ttu-id="2b58c-109">Il cmdlet **Get-AzBatchJob** ottiene i processi batch di Azure per l'account batch specificato dal parametro *BatchAccountContext* .</span><span class="sxs-lookup"><span data-stu-id="2b58c-109">The **Get-AzBatchJob** cmdlet gets the Azure Batch jobs for the Batch account specified by the *BatchAccountContext* parameter.</span></span>
<span data-ttu-id="2b58c-110">Puoi usare il parametro *ID* per ottenere un singolo processo.</span><span class="sxs-lookup"><span data-stu-id="2b58c-110">You can use the *Id* parameter to get a single job.</span></span>
<span data-ttu-id="2b58c-111">Puoi usare il parametro *Filter* per ottenere i processi che corrispondono a un filtro OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="2b58c-111">You can use the *Filter* parameter to get the jobs that match an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="2b58c-112">Se si specifica un ID pianificazione processi o un'istanza di **PSCloudJobSchedule** , questo cmdlet restituisce solo i processi per la pianificazione del processo.</span><span class="sxs-lookup"><span data-stu-id="2b58c-112">If you supply a job schedule ID or **PSCloudJobSchedule** instance, this cmdlet returns only the jobs for that job schedule.</span></span>

## <span data-ttu-id="2b58c-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2b58c-113">EXAMPLES</span></span>

### <span data-ttu-id="2b58c-114">Esempio 1: ottenere un processo batch per ID</span><span class="sxs-lookup"><span data-stu-id="2b58c-114">Example 1: Get a Batch job by ID</span></span>
```
PS C:\>Get-AzBatchJob -Id "Job01" -BatchContext $Context
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

<span data-ttu-id="2b58c-115">Questo comando ottiene il processo con ID Job01.</span><span class="sxs-lookup"><span data-stu-id="2b58c-115">This command gets the job that has the ID Job01.</span></span>
<span data-ttu-id="2b58c-116">Usa il cmdlet Get-AzBatchAccountKeys per assegnare un contesto alla variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="2b58c-116">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="2b58c-117">Esempio 2: ottenere tutti i processi attivi per una pianificazione del processo</span><span class="sxs-lookup"><span data-stu-id="2b58c-117">Example 2: Get all active jobs for a job schedule</span></span>
```
PS C:\>Get-AzBatchJob -JobScheduleId "JobSchedule27" -Filter "state eq 'active'" -BatchContext $Context
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

<span data-ttu-id="2b58c-118">Questo comando consente di ottenere i processi attivi per la pianificazione del processo con ID JobSchedule27.</span><span class="sxs-lookup"><span data-stu-id="2b58c-118">This command gets the active jobs for the job schedule that has the ID JobSchedule27.</span></span>

### <span data-ttu-id="2b58c-119">Esempio 3: ottiene tutti i processi in una pianificazione processo tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="2b58c-119">Example 3: Gets all jobs under a job schedule by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJobSchedule -Id "JobSchedule27" -BatchContext $Context | Get-AzBatchJob -BatchContext $Context
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

<span data-ttu-id="2b58c-120">Questo comando consente di ottenere la pianificazione del processo che contiene l'ID JobSchedule27 usando il cmdlet Get-AzBatchJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="2b58c-120">This command gets the job schedule that has the ID JobSchedule27 by using the Get-AzBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="2b58c-121">Il comando passa la pianificazione del processo al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="2b58c-121">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2b58c-122">Il comando ottiene tutti i processi per la pianificazione del processo.</span><span class="sxs-lookup"><span data-stu-id="2b58c-122">The command gets all jobs for that job schedule.</span></span>

## <span data-ttu-id="2b58c-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2b58c-123">PARAMETERS</span></span>

### <span data-ttu-id="2b58c-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="2b58c-124">-BatchContext</span></span>
<span data-ttu-id="2b58c-125">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="2b58c-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2b58c-126">Se si usa il cmdlet Get-AzBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="2b58c-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="2b58c-127">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="2b58c-127">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="2b58c-128">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="2b58c-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="2b58c-129">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="2b58c-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="2b58c-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b58c-130">-DefaultProfile</span></span>
<span data-ttu-id="2b58c-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2b58c-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b58c-132">-Espandi</span><span class="sxs-lookup"><span data-stu-id="2b58c-132">-Expand</span></span>
<span data-ttu-id="2b58c-133">Specifica una clausola di espansione OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="2b58c-133">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="2b58c-134">Specifica un valore per questo parametro per ottenere le entità associate dell'entità principale che ottieni.</span><span class="sxs-lookup"><span data-stu-id="2b58c-134">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="2b58c-135">-Filtro</span><span class="sxs-lookup"><span data-stu-id="2b58c-135">-Filter</span></span>
<span data-ttu-id="2b58c-136">Specifica una clausola di filtro OData per i processi.</span><span class="sxs-lookup"><span data-stu-id="2b58c-136">Specifies an OData filter clause for jobs.</span></span>
<span data-ttu-id="2b58c-137">Se non si specifica un filtro, questo cmdlet restituisce tutti i processi per l'account batch o per la pianificazione del processo.</span><span class="sxs-lookup"><span data-stu-id="2b58c-137">If you do not specify a filter, this cmdlet returns all jobs for the Batch account or job schedule.</span></span>

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

### <span data-ttu-id="2b58c-138">-ID</span><span class="sxs-lookup"><span data-stu-id="2b58c-138">-Id</span></span>
<span data-ttu-id="2b58c-139">Specifica l'ID del processo ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b58c-139">Specifies the ID of the job that this cmdlet gets.</span></span>
<span data-ttu-id="2b58c-140">Non è possibile specificare caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="2b58c-140">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="2b58c-141">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="2b58c-141">-JobSchedule</span></span>
<span data-ttu-id="2b58c-142">Specifica un oggetto **PSCloudJobSchedule** che rappresenta la pianificazione del processo che contiene i processi.</span><span class="sxs-lookup"><span data-stu-id="2b58c-142">Specifies a **PSCloudJobSchedule** object that represents the job schedule which contains the jobs.</span></span>
<span data-ttu-id="2b58c-143">Per ottenere un oggetto **PSCloudJobSchedule** , usa il cmdlet Get-AzBatchJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="2b58c-143">To obtain a **PSCloudJobSchedule** object, use the Get-AzBatchJobSchedule cmdlet.</span></span>

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

### <span data-ttu-id="2b58c-144">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="2b58c-144">-JobScheduleId</span></span>
<span data-ttu-id="2b58c-145">Specifica l'ID della pianificazione del processo che contiene i processi.</span><span class="sxs-lookup"><span data-stu-id="2b58c-145">Specifies the ID of the job schedule which contains the jobs.</span></span>

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

### <span data-ttu-id="2b58c-146">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="2b58c-146">-MaxCount</span></span>
<span data-ttu-id="2b58c-147">Specifica il numero massimo di processi da restituire.</span><span class="sxs-lookup"><span data-stu-id="2b58c-147">Specifies the maximum number of jobs to return.</span></span>
<span data-ttu-id="2b58c-148">Se specifichi un valore pari a zero (0) o meno, il cmdlet non usa un limite superiore.</span><span class="sxs-lookup"><span data-stu-id="2b58c-148">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="2b58c-149">Il valore predefinito è 1000.</span><span class="sxs-lookup"><span data-stu-id="2b58c-149">The default value is 1000.</span></span>

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

### <span data-ttu-id="2b58c-150">-Selezionare</span><span class="sxs-lookup"><span data-stu-id="2b58c-150">-Select</span></span>
<span data-ttu-id="2b58c-151">Specifica una clausola di selezione OData.</span><span class="sxs-lookup"><span data-stu-id="2b58c-151">Specifies an OData select clause.</span></span>
<span data-ttu-id="2b58c-152">Specifica un valore per questo parametro per ottenere proprietà specifiche anziché tutte le proprietà dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2b58c-152">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="2b58c-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b58c-153">CommonParameters</span></span>
<span data-ttu-id="2b58c-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b58c-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b58c-155">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b58c-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b58c-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2b58c-156">INPUTS</span></span>

### <span data-ttu-id="2b58c-157">System. String</span><span class="sxs-lookup"><span data-stu-id="2b58c-157">System.String</span></span>

### <span data-ttu-id="2b58c-158">Microsoft.Azure.Commands.Batch. Models. PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="2b58c-158">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

### <span data-ttu-id="2b58c-159">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="2b58c-159">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="2b58c-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2b58c-160">OUTPUTS</span></span>

### <span data-ttu-id="2b58c-161">Microsoft.Azure.Commands.Batch. Models. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="2b58c-161">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

## <span data-ttu-id="2b58c-162">Note</span><span class="sxs-lookup"><span data-stu-id="2b58c-162">NOTES</span></span>

## <span data-ttu-id="2b58c-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2b58c-163">RELATED LINKS</span></span>

[<span data-ttu-id="2b58c-164">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2b58c-164">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="2b58c-165">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2b58c-165">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="2b58c-166">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="2b58c-166">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="2b58c-167">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="2b58c-167">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="2b58c-168">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2b58c-168">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="2b58c-169">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2b58c-169">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="2b58c-170">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2b58c-170">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="2b58c-171">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="2b58c-171">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


