---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 8BF49C4D-E7CD-4FD0-AFAC-9856239D24EC
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJob.md
ms.openlocfilehash: 4b570f78ddb73c7f0ab6dedcd4eca3ac26ff12df
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986241"
---
# <span data-ttu-id="b4bb6-101">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="b4bb6-101">Get-AzBatchJob</span></span>

## <span data-ttu-id="b4bb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4bb6-102">SYNOPSIS</span></span>
<span data-ttu-id="b4bb6-103">Recupera i processi batch per un account batch o una pianificazione di processo.</span><span class="sxs-lookup"><span data-stu-id="b4bb6-103">Gets Batch jobs for a Batch account or job schedule.</span></span>

## <span data-ttu-id="b4bb6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b4bb6-104">SYNTAX</span></span>

### <span data-ttu-id="b4bb6-105">ODataFilter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b4bb6-105">ODataFilter (Default)</span></span>
```
Get-AzBatchJob [-JobScheduleId <String>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b4bb6-106">ID</span><span class="sxs-lookup"><span data-stu-id="b4bb6-106">Id</span></span>
```
Get-AzBatchJob [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4bb6-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="b4bb6-107">ParentObject</span></span>
```
Get-AzBatchJob [[-JobSchedule] <PSCloudJobSchedule>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b4bb6-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b4bb6-108">DESCRIPTION</span></span>
<span data-ttu-id="b4bb6-109">Il cmdlet **Get-AzBatchJob** ottiene i processi batch di Azure per l'account batch specificato dal *parametro BatchAccountContext.*</span><span class="sxs-lookup"><span data-stu-id="b4bb6-109">The **Get-AzBatchJob** cmdlet gets the Azure Batch jobs for the Batch account specified by the *BatchAccountContext* parameter.</span></span>
<span data-ttu-id="b4bb6-110">È possibile usare il *parametro ID* per ottenere un singolo processo.</span><span class="sxs-lookup"><span data-stu-id="b4bb6-110">You can use the *Id* parameter to get a single job.</span></span>
<span data-ttu-id="b4bb6-111">È possibile usare il *parametro Filter* per ottenere i processi corrispondenti a un filtro OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="b4bb6-111">You can use the *Filter* parameter to get the jobs that match an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="b4bb6-112">Se si specifica un ID pianificazione processo o **un'istanza PSCloudJobSchedule,** questo cmdlet restituisce solo i processi per tale pianificazione.</span><span class="sxs-lookup"><span data-stu-id="b4bb6-112">If you supply a job schedule ID or **PSCloudJobSchedule** instance, this cmdlet returns only the jobs for that job schedule.</span></span>

## <span data-ttu-id="b4bb6-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b4bb6-113">EXAMPLES</span></span>

### <span data-ttu-id="b4bb6-114">Esempio 1: Ottenere un processo batch in base all'ID</span><span class="sxs-lookup"><span data-stu-id="b4bb6-114">Example 1: Get a Batch job by ID</span></span>
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

<span data-ttu-id="b4bb6-115">Questo comando recupera il processo con ID Job01.</span><span class="sxs-lookup"><span data-stu-id="b4bb6-115">This command gets the job that has the ID Job01.</span></span>
<span data-ttu-id="b4bb6-116">Usare il cmdlet Get-AzBatchAccountKey per assegnare un contesto alla $Context variabile.</span><span class="sxs-lookup"><span data-stu-id="b4bb6-116">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="b4bb6-117">Esempio 2: Recuperare tutti i processi attivi per una pianificazione di un processo</span><span class="sxs-lookup"><span data-stu-id="b4bb6-117">Example 2: Get all active jobs for a job schedule</span></span>
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

<span data-ttu-id="b4bb6-118">Questo comando recupera i processi attivi per la pianificazione dei processi con ID JobSchedule27.</span><span class="sxs-lookup"><span data-stu-id="b4bb6-118">This command gets the active jobs for the job schedule that has the ID JobSchedule27.</span></span>

### <span data-ttu-id="b4bb6-119">Esempio 3: Recupera tutti i processi sotto una pianificazione di processo tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="b4bb6-119">Example 3: Gets all jobs under a job schedule by using the pipeline</span></span>
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

<span data-ttu-id="b4bb6-120">Questo comando recupera la pianificazione del processo con l'ID JobSchedule27 usando il cmdlet Get-AzBatchJobSchedule processo.</span><span class="sxs-lookup"><span data-stu-id="b4bb6-120">This command gets the job schedule that has the ID JobSchedule27 by using the Get-AzBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="b4bb6-121">Il comando passa la pianificazione del processo al cmdlet corrente usando l'operatore della pipeline.</span><span class="sxs-lookup"><span data-stu-id="b4bb6-121">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b4bb6-122">Il comando recupera tutti i processi per la pianificazione del processo.</span><span class="sxs-lookup"><span data-stu-id="b4bb6-122">The command gets all jobs for that job schedule.</span></span>

## <span data-ttu-id="b4bb6-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4bb6-123">PARAMETERS</span></span>

### <span data-ttu-id="b4bb6-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b4bb6-124">-BatchContext</span></span>
<span data-ttu-id="b4bb6-125">Specifica **l'istanza BatchAccountContext** che questo cmdlet usa per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="b4bb6-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b4bb6-126">Se si usa il cmdlet Get-AzBatchAccount per ottenere BatchAccountContext, verrà usata l'autenticazione di Azure Active Directory quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="b4bb6-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b4bb6-127">Per usare invece l'autenticazione della chiave condivisa, usare il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.</span><span class="sxs-lookup"><span data-stu-id="b4bb6-127">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b4bb6-128">Quando si usa l'autenticazione con chiave condivisa, per impostazione predefinita viene usata la chiave di accesso primario.</span><span class="sxs-lookup"><span data-stu-id="b4bb6-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b4bb6-129">Per modificare la chiave da usare, impostare la proprietà BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="b4bb6-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b4bb6-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4bb6-130">-DefaultProfile</span></span>
<span data-ttu-id="b4bb6-131">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b4bb6-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4bb6-132">-Expand</span><span class="sxs-lookup"><span data-stu-id="b4bb6-132">-Expand</span></span>
<span data-ttu-id="b4bb6-133">Specifica una clausola di espansione OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="b4bb6-133">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="b4bb6-134">Specificare un valore per questo parametro per ottenere entità associate dell'entità principale da ottenere.</span><span class="sxs-lookup"><span data-stu-id="b4bb6-134">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="b4bb6-135">-Filter</span><span class="sxs-lookup"><span data-stu-id="b4bb6-135">-Filter</span></span>
<span data-ttu-id="b4bb6-136">Specifica una clausola del filtro OData per i processi.</span><span class="sxs-lookup"><span data-stu-id="b4bb6-136">Specifies an OData filter clause for jobs.</span></span>
<span data-ttu-id="b4bb6-137">Se non si specifica un filtro, questo cmdlet restituisce tutti i processi per l'account batch o la pianificazione del processo.</span><span class="sxs-lookup"><span data-stu-id="b4bb6-137">If you do not specify a filter, this cmdlet returns all jobs for the Batch account or job schedule.</span></span>

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

### <span data-ttu-id="b4bb6-138">-Id</span><span class="sxs-lookup"><span data-stu-id="b4bb6-138">-Id</span></span>
<span data-ttu-id="b4bb6-139">Specifica l'ID del processo che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4bb6-139">Specifies the ID of the job that this cmdlet gets.</span></span>
<span data-ttu-id="b4bb6-140">Non è possibile specificare caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="b4bb6-140">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="b4bb6-141">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="b4bb6-141">-JobSchedule</span></span>
<span data-ttu-id="b4bb6-142">Specifica un oggetto **PSCloudJobSchedule** che rappresenta la pianificazione del processo che contiene i processi.</span><span class="sxs-lookup"><span data-stu-id="b4bb6-142">Specifies a **PSCloudJobSchedule** object that represents the job schedule which contains the jobs.</span></span>
<span data-ttu-id="b4bb6-143">Per ottenere un **oggetto PSCloudJobSchedule,** usare il cmdlet Get-AzBatchJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="b4bb6-143">To obtain a **PSCloudJobSchedule** object, use the Get-AzBatchJobSchedule cmdlet.</span></span>

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

### <span data-ttu-id="b4bb6-144">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="b4bb6-144">-JobScheduleId</span></span>
<span data-ttu-id="b4bb6-145">Specifica l'ID della pianificazione del processo che contiene i processi.</span><span class="sxs-lookup"><span data-stu-id="b4bb6-145">Specifies the ID of the job schedule which contains the jobs.</span></span>

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

### <span data-ttu-id="b4bb6-146">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="b4bb6-146">-MaxCount</span></span>
<span data-ttu-id="b4bb6-147">Specifica il numero massimo di processi da restituire.</span><span class="sxs-lookup"><span data-stu-id="b4bb6-147">Specifies the maximum number of jobs to return.</span></span>
<span data-ttu-id="b4bb6-148">Se si specifica un valore uguale o inferiore a zero (0), il cmdlet non usa un limite superiore.</span><span class="sxs-lookup"><span data-stu-id="b4bb6-148">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="b4bb6-149">Il valore predefinito è 1000.</span><span class="sxs-lookup"><span data-stu-id="b4bb6-149">The default value is 1000.</span></span>

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

### <span data-ttu-id="b4bb6-150">-Select</span><span class="sxs-lookup"><span data-stu-id="b4bb6-150">-Select</span></span>
<span data-ttu-id="b4bb6-151">Specifica una clausola di selezione OData.</span><span class="sxs-lookup"><span data-stu-id="b4bb6-151">Specifies an OData select clause.</span></span>
<span data-ttu-id="b4bb6-152">Specificare un valore per questo parametro per ottenere proprietà specifiche invece di tutte le proprietà dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b4bb6-152">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="b4bb6-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4bb6-153">CommonParameters</span></span>
<span data-ttu-id="b4bb6-154">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4bb6-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4bb6-155">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b4bb6-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4bb6-156">INPUT</span><span class="sxs-lookup"><span data-stu-id="b4bb6-156">INPUTS</span></span>

### <span data-ttu-id="b4bb6-157">System.String</span><span class="sxs-lookup"><span data-stu-id="b4bb6-157">System.String</span></span>

### <span data-ttu-id="b4bb6-158">Microsoft.Azure.Commands.Batch. Models.PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b4bb6-158">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

### <span data-ttu-id="b4bb6-159">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b4bb6-159">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="b4bb6-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b4bb6-160">OUTPUTS</span></span>

### <span data-ttu-id="b4bb6-161">Microsoft.Azure.Commands.Batch. Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="b4bb6-161">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

## <span data-ttu-id="b4bb6-162">NOTE</span><span class="sxs-lookup"><span data-stu-id="b4bb6-162">NOTES</span></span>

## <span data-ttu-id="b4bb6-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b4bb6-163">RELATED LINKS</span></span>

[<span data-ttu-id="b4bb6-164">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="b4bb6-164">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="b4bb6-165">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="b4bb6-165">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="b4bb6-166">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="b4bb6-166">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="b4bb6-167">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b4bb6-167">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="b4bb6-168">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="b4bb6-168">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="b4bb6-169">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="b4bb6-169">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="b4bb6-170">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="b4bb6-170">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="b4bb6-171">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="b4bb6-171">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
