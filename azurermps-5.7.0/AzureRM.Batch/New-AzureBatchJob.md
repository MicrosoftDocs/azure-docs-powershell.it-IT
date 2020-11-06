---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B6229D26-D38C-44CD-B9CA-7F39365C8B9D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJob.md
ms.openlocfilehash: bf96b5930895332de2e78ffdee71f9f6a2654b83
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521930"
---
# <span data-ttu-id="12c8f-101">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="12c8f-101">New-AzureBatchJob</span></span>

## <span data-ttu-id="12c8f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="12c8f-102">SYNOPSIS</span></span>
<span data-ttu-id="12c8f-103">Crea un processo nel servizio batch.</span><span class="sxs-lookup"><span data-stu-id="12c8f-103">Creates a job in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12c8f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="12c8f-104">SYNTAX</span></span>

```
New-AzureBatchJob [-Id] <String> [-CommonEnvironmentSettings <IDictionary>] [-DisplayName <String>]
 [-Constraints <PSJobConstraints>] [-JobManagerTask <PSJobManagerTask>]
 [-JobPreparationTask <PSJobPreparationTask>] [-JobReleaseTask <PSJobReleaseTask>] [-Metadata <IDictionary>]
 -PoolInformation <PSPoolInformation> [-Priority <Int32>] [-UsesTaskDependencies]
 [-OnTaskFailure <OnTaskFailure>] [-OnAllTasksComplete <OnAllTasksComplete>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12c8f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12c8f-105">DESCRIPTION</span></span>
<span data-ttu-id="12c8f-106">Il cmdlet **New-AzureBatchJob** crea un processo nel servizio batch di Azure nell'account specificato dal parametro *BatchAccountContext* .</span><span class="sxs-lookup"><span data-stu-id="12c8f-106">The **New-AzureBatchJob** cmdlet creates a job in the Azure Batch service in the account specified by the *BatchAccountContext* parameter.</span></span>

## <span data-ttu-id="12c8f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="12c8f-107">EXAMPLES</span></span>

### <span data-ttu-id="12c8f-108">Esempio 1: creare un processo</span><span class="sxs-lookup"><span data-stu-id="12c8f-108">Example 1: Create a job</span></span>
```
PS C:\>$PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation" 
PS C:\> $PoolInformation.PoolId = "Pool22" 
PS C:\> New-AzureBatchJob -Id "ContosoJob35" -PoolInformation $PoolInformation -BatchContext $Context
```

<span data-ttu-id="12c8f-109">Il primo comando crea un oggetto **PSPoolInformation** usando il cmdlet New-Object.</span><span class="sxs-lookup"><span data-stu-id="12c8f-109">The first command creates a **PSPoolInformation** object by using the New-Object cmdlet.</span></span>
<span data-ttu-id="12c8f-110">Il comando Archivia l'oggetto nella variabile $PoolInformation.</span><span class="sxs-lookup"><span data-stu-id="12c8f-110">The command stores that object in the $PoolInformation variable.</span></span>

<span data-ttu-id="12c8f-111">Il secondo comando assegna l'ID Pool22 alla proprietà **PoolId** dell'oggetto in $PoolInformation.</span><span class="sxs-lookup"><span data-stu-id="12c8f-111">The second command assigns the ID Pool22 to the **PoolId** property of the object in $PoolInformation.</span></span>

<span data-ttu-id="12c8f-112">Il comando finale crea un processo con ID ContosoJob35.</span><span class="sxs-lookup"><span data-stu-id="12c8f-112">The final command creates a job that has the ID ContosoJob35.</span></span>
<span data-ttu-id="12c8f-113">Le attività aggiunte al processo vengono eseguite nel pool che contiene l'ID Pool22.</span><span class="sxs-lookup"><span data-stu-id="12c8f-113">Tasks added to the job run on the pool that has the ID Pool22.</span></span>
<span data-ttu-id="12c8f-114">Usa il cmdlet Get-AzureRmBatchAccountKeys per assegnare un contesto alla variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="12c8f-114">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="12c8f-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="12c8f-115">PARAMETERS</span></span>

### <span data-ttu-id="12c8f-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="12c8f-116">-BatchContext</span></span>
<span data-ttu-id="12c8f-117">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="12c8f-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="12c8f-118">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="12c8f-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="12c8f-119">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="12c8f-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="12c8f-120">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="12c8f-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="12c8f-121">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="12c8f-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12c8f-122">-CommonEnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="12c8f-122">-CommonEnvironmentSettings</span></span>
<span data-ttu-id="12c8f-123">Specifica le variabili di ambiente comuni, come coppie chiave/valore, che questo cmdlet imposta per tutte le attività del processo.</span><span class="sxs-lookup"><span data-stu-id="12c8f-123">Specifies the common environment variables, as key/value pairs, that this cmdlet sets for all tasks in the job.</span></span>
<span data-ttu-id="12c8f-124">La chiave è il nome della variabile di ambiente.</span><span class="sxs-lookup"><span data-stu-id="12c8f-124">The key is the environment variable name.</span></span>
<span data-ttu-id="12c8f-125">Il valore è il valore della variabile di ambiente.</span><span class="sxs-lookup"><span data-stu-id="12c8f-125">The value is the environment variable value.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: CommonEnvironmentSetting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c8f-126">-Vincoli</span><span class="sxs-lookup"><span data-stu-id="12c8f-126">-Constraints</span></span>
<span data-ttu-id="12c8f-127">Specifica i vincoli di esecuzione per il processo.</span><span class="sxs-lookup"><span data-stu-id="12c8f-127">Specifies the execution constraints for the job.</span></span>

```yaml
Type: PSJobConstraints
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c8f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12c8f-128">-DefaultProfile</span></span>
<span data-ttu-id="12c8f-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="12c8f-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12c8f-130">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="12c8f-130">-DisplayName</span></span>
<span data-ttu-id="12c8f-131">Specifica il nome visualizzato per il processo.</span><span class="sxs-lookup"><span data-stu-id="12c8f-131">Specifies the display name for the job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c8f-132">-ID</span><span class="sxs-lookup"><span data-stu-id="12c8f-132">-Id</span></span>
<span data-ttu-id="12c8f-133">Specifica un ID per il processo.</span><span class="sxs-lookup"><span data-stu-id="12c8f-133">Specifies an ID for the job.</span></span>

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

### <span data-ttu-id="12c8f-134">-JobManagerTask</span><span class="sxs-lookup"><span data-stu-id="12c8f-134">-JobManagerTask</span></span>
<span data-ttu-id="12c8f-135">Specifica l'attività di gestione processi.</span><span class="sxs-lookup"><span data-stu-id="12c8f-135">Specifies the Job Manager task.</span></span>
<span data-ttu-id="12c8f-136">Il servizio batch esegue l'attività di gestione processi quando il processo viene avviato.</span><span class="sxs-lookup"><span data-stu-id="12c8f-136">The Batch service runs the Job Manager task when the job is started.</span></span>

```yaml
Type: PSJobManagerTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c8f-137">-JobPreparationTask</span><span class="sxs-lookup"><span data-stu-id="12c8f-137">-JobPreparationTask</span></span>
<span data-ttu-id="12c8f-138">Specifica l'attività di preparazione processo.</span><span class="sxs-lookup"><span data-stu-id="12c8f-138">Specifies the Job Preparation task.</span></span>
<span data-ttu-id="12c8f-139">Il servizio batch esegue l'attività di preparazione del processo su un nodo Compute prima di avviare tutte le attività del processo in tale nodo COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="12c8f-139">The Batch service runs the Job Preparation task on a compute node before it starts any tasks of that job on that compute node.</span></span>

```yaml
Type: PSJobPreparationTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c8f-140">-JobReleaseTask</span><span class="sxs-lookup"><span data-stu-id="12c8f-140">-JobReleaseTask</span></span>
<span data-ttu-id="12c8f-141">Specifica l'attività di rilascio del processo.</span><span class="sxs-lookup"><span data-stu-id="12c8f-141">Specifies the Job Release task.</span></span>
<span data-ttu-id="12c8f-142">Il servizio batch esegue l'attività di rilascio del processo al termine del processo.</span><span class="sxs-lookup"><span data-stu-id="12c8f-142">The Batch service runs the Job Release task when the job ends.</span></span>
<span data-ttu-id="12c8f-143">Il servizio batch esegue l'attività di rilascio del processo in ogni nodo COMPUTE in cui è stata eseguita un'attività del processo.</span><span class="sxs-lookup"><span data-stu-id="12c8f-143">The Batch service runs the Job Release task on each compute node where it ran any task of the job.</span></span>

```yaml
Type: PSJobReleaseTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c8f-144">-Metadata</span><span class="sxs-lookup"><span data-stu-id="12c8f-144">-Metadata</span></span>
<span data-ttu-id="12c8f-145">Specifica i metadati, come coppie chiave/valore, da aggiungere al processo.</span><span class="sxs-lookup"><span data-stu-id="12c8f-145">Specifies metadata, as key/value pairs, to add to the job.</span></span>
<span data-ttu-id="12c8f-146">La chiave è il nome dei metadati.</span><span class="sxs-lookup"><span data-stu-id="12c8f-146">The key is the metadata name.</span></span>
<span data-ttu-id="12c8f-147">Il valore è il valore Metadata.</span><span class="sxs-lookup"><span data-stu-id="12c8f-147">The value is the metadata value.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c8f-148">-OnAllTasksComplete</span><span class="sxs-lookup"><span data-stu-id="12c8f-148">-OnAllTasksComplete</span></span>
<span data-ttu-id="12c8f-149">Specifica un'azione eseguita dal servizio batch se tutte le attività del processo si trovano nello stato completato.</span><span class="sxs-lookup"><span data-stu-id="12c8f-149">Specifies an action the Batch service takes if all tasks in the job are in the completed state.</span></span>

```yaml
Type: OnAllTasksComplete
Parameter Sets: (All)
Aliases: 
Accepted values: NoAction, TerminateJob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c8f-150">-OnTaskFailure</span><span class="sxs-lookup"><span data-stu-id="12c8f-150">-OnTaskFailure</span></span>
<span data-ttu-id="12c8f-151">Specifica un'azione che il servizio batch accetta se un'attività nel processo non riesce.</span><span class="sxs-lookup"><span data-stu-id="12c8f-151">Specifies an action the Batch service takes if any task in the job fails.</span></span>

```yaml
Type: OnTaskFailure
Parameter Sets: (All)
Aliases: 
Accepted values: NoAction, PerformExitOptionsJobAction

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c8f-152">-PoolInformation</span><span class="sxs-lookup"><span data-stu-id="12c8f-152">-PoolInformation</span></span>
<span data-ttu-id="12c8f-153">Specifica i dettagli del pool in cui il servizio batch esegue le attività del processo.</span><span class="sxs-lookup"><span data-stu-id="12c8f-153">Specifies the details of the pool on which the Batch service runs the tasks of the job.</span></span>

```yaml
Type: PSPoolInformation
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c8f-154">-Priorità</span><span class="sxs-lookup"><span data-stu-id="12c8f-154">-Priority</span></span>
<span data-ttu-id="12c8f-155">Specifica la priorità del processo.</span><span class="sxs-lookup"><span data-stu-id="12c8f-155">Specifies the priority of the job.</span></span>
<span data-ttu-id="12c8f-156">I valori validi sono: numeri interi da-1000 a 1000.</span><span class="sxs-lookup"><span data-stu-id="12c8f-156">Valid values are: integers from -1000 to 1000.</span></span>
<span data-ttu-id="12c8f-157">Il valore di-1000 è la priorità più bassa.</span><span class="sxs-lookup"><span data-stu-id="12c8f-157">A value of -1000 is the lowest priority.</span></span>
<span data-ttu-id="12c8f-158">Il valore di 1000 è la priorità più alta.</span><span class="sxs-lookup"><span data-stu-id="12c8f-158">A value of 1000 is the highest priority.</span></span>
<span data-ttu-id="12c8f-159">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="12c8f-159">The default value is 0.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c8f-160">-UsesTaskDependencies</span><span class="sxs-lookup"><span data-stu-id="12c8f-160">-UsesTaskDependencies</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c8f-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12c8f-161">CommonParameters</span></span>
<span data-ttu-id="12c8f-162">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12c8f-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12c8f-163">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12c8f-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12c8f-164">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="12c8f-164">INPUTS</span></span>

### <span data-ttu-id="12c8f-165">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="12c8f-165">BatchAccountContext</span></span>
<span data-ttu-id="12c8f-166">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="12c8f-166">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="12c8f-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="12c8f-167">OUTPUTS</span></span>

## <span data-ttu-id="12c8f-168">Note</span><span class="sxs-lookup"><span data-stu-id="12c8f-168">NOTES</span></span>

## <span data-ttu-id="12c8f-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="12c8f-169">RELATED LINKS</span></span>

[<span data-ttu-id="12c8f-170">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="12c8f-170">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="12c8f-171">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="12c8f-171">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="12c8f-172">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="12c8f-172">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="12c8f-173">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="12c8f-173">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="12c8f-174">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="12c8f-174">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="12c8f-175">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="12c8f-175">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="12c8f-176">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="12c8f-176">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="12c8f-177">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="12c8f-177">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


