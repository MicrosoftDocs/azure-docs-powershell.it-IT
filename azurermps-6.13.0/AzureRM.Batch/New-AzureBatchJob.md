---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B6229D26-D38C-44CD-B9CA-7F39365C8B9D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJob.md
ms.openlocfilehash: 3fd4861ed70a010839edbe7bcdffb61961d0bdf6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519299"
---
# <span data-ttu-id="f3d88-101">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="f3d88-101">New-AzureBatchJob</span></span>

## <span data-ttu-id="f3d88-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f3d88-102">SYNOPSIS</span></span>
<span data-ttu-id="f3d88-103">Crea un processo nel servizio batch.</span><span class="sxs-lookup"><span data-stu-id="f3d88-103">Creates a job in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3d88-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f3d88-104">SYNTAX</span></span>

```
New-AzureBatchJob [-Id] <String> [-CommonEnvironmentSettings <IDictionary>] [-DisplayName <String>]
 [-Constraints <PSJobConstraints>] [-JobManagerTask <PSJobManagerTask>]
 [-JobPreparationTask <PSJobPreparationTask>] [-JobReleaseTask <PSJobReleaseTask>] [-Metadata <IDictionary>]
 -PoolInformation <PSPoolInformation> [-Priority <Int32>] [-UsesTaskDependencies]
 [-OnTaskFailure <OnTaskFailure>] [-OnAllTasksComplete <OnAllTasksComplete>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3d88-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3d88-105">DESCRIPTION</span></span>
<span data-ttu-id="f3d88-106">Il cmdlet **New-AzureBatchJob** crea un processo nel servizio batch di Azure nell'account specificato dal parametro *BatchAccountContext* .</span><span class="sxs-lookup"><span data-stu-id="f3d88-106">The **New-AzureBatchJob** cmdlet creates a job in the Azure Batch service in the account specified by the *BatchAccountContext* parameter.</span></span>

## <span data-ttu-id="f3d88-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f3d88-107">EXAMPLES</span></span>

### <span data-ttu-id="f3d88-108">Esempio 1: creare un processo</span><span class="sxs-lookup"><span data-stu-id="f3d88-108">Example 1: Create a job</span></span>
```
PS C:\>$PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation" 
PS C:\> $PoolInformation.PoolId = "Pool22" 
PS C:\> New-AzureBatchJob -Id "ContosoJob35" -PoolInformation $PoolInformation -BatchContext $Context
```

<span data-ttu-id="f3d88-109">Il primo comando crea un oggetto **PSPoolInformation** usando il cmdlet New-Object.</span><span class="sxs-lookup"><span data-stu-id="f3d88-109">The first command creates a **PSPoolInformation** object by using the New-Object cmdlet.</span></span>
<span data-ttu-id="f3d88-110">Il comando Archivia l'oggetto nella variabile $PoolInformation.</span><span class="sxs-lookup"><span data-stu-id="f3d88-110">The command stores that object in the $PoolInformation variable.</span></span>
<span data-ttu-id="f3d88-111">Il secondo comando assegna l'ID Pool22 alla proprietà **PoolId** dell'oggetto in $PoolInformation.</span><span class="sxs-lookup"><span data-stu-id="f3d88-111">The second command assigns the ID Pool22 to the **PoolId** property of the object in $PoolInformation.</span></span>
<span data-ttu-id="f3d88-112">Il comando finale crea un processo con ID ContosoJob35.</span><span class="sxs-lookup"><span data-stu-id="f3d88-112">The final command creates a job that has the ID ContosoJob35.</span></span>
<span data-ttu-id="f3d88-113">Le attività aggiunte al processo vengono eseguite nel pool che contiene l'ID Pool22.</span><span class="sxs-lookup"><span data-stu-id="f3d88-113">Tasks added to the job run on the pool that has the ID Pool22.</span></span>
<span data-ttu-id="f3d88-114">Usa il cmdlet Get-AzureRmBatchAccountKeys per assegnare un contesto alla variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="f3d88-114">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="f3d88-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f3d88-115">PARAMETERS</span></span>

### <span data-ttu-id="f3d88-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f3d88-116">-BatchContext</span></span>
<span data-ttu-id="f3d88-117">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="f3d88-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f3d88-118">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="f3d88-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f3d88-119">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="f3d88-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f3d88-120">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="f3d88-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f3d88-121">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="f3d88-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f3d88-122">-CommonEnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="f3d88-122">-CommonEnvironmentSettings</span></span>
<span data-ttu-id="f3d88-123">Specifica le variabili di ambiente comuni, come coppie chiave/valore, che questo cmdlet imposta per tutte le attività del processo.</span><span class="sxs-lookup"><span data-stu-id="f3d88-123">Specifies the common environment variables, as key/value pairs, that this cmdlet sets for all tasks in the job.</span></span>
<span data-ttu-id="f3d88-124">La chiave è il nome della variabile di ambiente.</span><span class="sxs-lookup"><span data-stu-id="f3d88-124">The key is the environment variable name.</span></span>
<span data-ttu-id="f3d88-125">Il valore è il valore della variabile di ambiente.</span><span class="sxs-lookup"><span data-stu-id="f3d88-125">The value is the environment variable value.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: CommonEnvironmentSetting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3d88-126">-Vincoli</span><span class="sxs-lookup"><span data-stu-id="f3d88-126">-Constraints</span></span>
<span data-ttu-id="f3d88-127">Specifica i vincoli di esecuzione per il processo.</span><span class="sxs-lookup"><span data-stu-id="f3d88-127">Specifies the execution constraints for the job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3d88-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3d88-128">-DefaultProfile</span></span>
<span data-ttu-id="f3d88-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f3d88-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3d88-130">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f3d88-130">-DisplayName</span></span>
<span data-ttu-id="f3d88-131">Specifica il nome visualizzato per il processo.</span><span class="sxs-lookup"><span data-stu-id="f3d88-131">Specifies the display name for the job.</span></span>

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

### <span data-ttu-id="f3d88-132">-ID</span><span class="sxs-lookup"><span data-stu-id="f3d88-132">-Id</span></span>
<span data-ttu-id="f3d88-133">Specifica un ID per il processo.</span><span class="sxs-lookup"><span data-stu-id="f3d88-133">Specifies an ID for the job.</span></span>

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

### <span data-ttu-id="f3d88-134">-JobManagerTask</span><span class="sxs-lookup"><span data-stu-id="f3d88-134">-JobManagerTask</span></span>
<span data-ttu-id="f3d88-135">Specifica l'attività di gestione processi.</span><span class="sxs-lookup"><span data-stu-id="f3d88-135">Specifies the Job Manager task.</span></span>
<span data-ttu-id="f3d88-136">Il servizio batch esegue l'attività di gestione processi quando il processo viene avviato.</span><span class="sxs-lookup"><span data-stu-id="f3d88-136">The Batch service runs the Job Manager task when the job is started.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobManagerTask
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3d88-137">-JobPreparationTask</span><span class="sxs-lookup"><span data-stu-id="f3d88-137">-JobPreparationTask</span></span>
<span data-ttu-id="f3d88-138">Specifica l'attività di preparazione processo.</span><span class="sxs-lookup"><span data-stu-id="f3d88-138">Specifies the Job Preparation task.</span></span>
<span data-ttu-id="f3d88-139">Il servizio batch esegue l'attività di preparazione del processo su un nodo Compute prima di avviare tutte le attività del processo in tale nodo COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="f3d88-139">The Batch service runs the Job Preparation task on a compute node before it starts any tasks of that job on that compute node.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTask
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3d88-140">-JobReleaseTask</span><span class="sxs-lookup"><span data-stu-id="f3d88-140">-JobReleaseTask</span></span>
<span data-ttu-id="f3d88-141">Specifica l'attività di rilascio del processo.</span><span class="sxs-lookup"><span data-stu-id="f3d88-141">Specifies the Job Release task.</span></span>
<span data-ttu-id="f3d88-142">Il servizio batch esegue l'attività di rilascio del processo al termine del processo.</span><span class="sxs-lookup"><span data-stu-id="f3d88-142">The Batch service runs the Job Release task when the job ends.</span></span>
<span data-ttu-id="f3d88-143">Il servizio batch esegue l'attività di rilascio del processo in ogni nodo COMPUTE in cui è stata eseguita un'attività del processo.</span><span class="sxs-lookup"><span data-stu-id="f3d88-143">The Batch service runs the Job Release task on each compute node where it ran any task of the job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobReleaseTask
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3d88-144">-Metadata</span><span class="sxs-lookup"><span data-stu-id="f3d88-144">-Metadata</span></span>
<span data-ttu-id="f3d88-145">Specifica i metadati, come coppie chiave/valore, da aggiungere al processo.</span><span class="sxs-lookup"><span data-stu-id="f3d88-145">Specifies metadata, as key/value pairs, to add to the job.</span></span>
<span data-ttu-id="f3d88-146">La chiave è il nome dei metadati.</span><span class="sxs-lookup"><span data-stu-id="f3d88-146">The key is the metadata name.</span></span>
<span data-ttu-id="f3d88-147">Il valore è il valore Metadata.</span><span class="sxs-lookup"><span data-stu-id="f3d88-147">The value is the metadata value.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3d88-148">-OnAllTasksComplete</span><span class="sxs-lookup"><span data-stu-id="f3d88-148">-OnAllTasksComplete</span></span>
<span data-ttu-id="f3d88-149">Specifica un'azione eseguita dal servizio batch se tutte le attività del processo si trovano nello stato completato.</span><span class="sxs-lookup"><span data-stu-id="f3d88-149">Specifies an action the Batch service takes if all tasks in the job are in the completed state.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.OnAllTasksComplete]
Parameter Sets: (All)
Aliases:
Accepted values: NoAction, TerminateJob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3d88-150">-OnTaskFailure</span><span class="sxs-lookup"><span data-stu-id="f3d88-150">-OnTaskFailure</span></span>
<span data-ttu-id="f3d88-151">Specifica un'azione che il servizio batch accetta se un'attività nel processo non riesce.</span><span class="sxs-lookup"><span data-stu-id="f3d88-151">Specifies an action the Batch service takes if any task in the job fails.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.OnTaskFailure]
Parameter Sets: (All)
Aliases:
Accepted values: NoAction, PerformExitOptionsJobAction

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3d88-152">-PoolInformation</span><span class="sxs-lookup"><span data-stu-id="f3d88-152">-PoolInformation</span></span>
<span data-ttu-id="f3d88-153">Specifica i dettagli del pool in cui il servizio batch esegue le attività del processo.</span><span class="sxs-lookup"><span data-stu-id="f3d88-153">Specifies the details of the pool on which the Batch service runs the tasks of the job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3d88-154">-Priorità</span><span class="sxs-lookup"><span data-stu-id="f3d88-154">-Priority</span></span>
<span data-ttu-id="f3d88-155">Specifica la priorità del processo.</span><span class="sxs-lookup"><span data-stu-id="f3d88-155">Specifies the priority of the job.</span></span>
<span data-ttu-id="f3d88-156">I valori validi sono: numeri interi da-1000 a 1000.</span><span class="sxs-lookup"><span data-stu-id="f3d88-156">Valid values are: integers from -1000 to 1000.</span></span>
<span data-ttu-id="f3d88-157">Il valore di-1000 è la priorità più bassa.</span><span class="sxs-lookup"><span data-stu-id="f3d88-157">A value of -1000 is the lowest priority.</span></span>
<span data-ttu-id="f3d88-158">Il valore di 1000 è la priorità più alta.</span><span class="sxs-lookup"><span data-stu-id="f3d88-158">A value of 1000 is the highest priority.</span></span>
<span data-ttu-id="f3d88-159">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="f3d88-159">The default value is 0.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3d88-160">-UsesTaskDependencies</span><span class="sxs-lookup"><span data-stu-id="f3d88-160">-UsesTaskDependencies</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3d88-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3d88-161">CommonParameters</span></span>
<span data-ttu-id="f3d88-162">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3d88-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3d88-163">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3d88-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3d88-164">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f3d88-164">INPUTS</span></span>

### <span data-ttu-id="f3d88-165">System. String</span><span class="sxs-lookup"><span data-stu-id="f3d88-165">System.String</span></span>

### <span data-ttu-id="f3d88-166">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f3d88-166">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="f3d88-167">Parametri: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f3d88-167">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="f3d88-168">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f3d88-168">OUTPUTS</span></span>

### <span data-ttu-id="f3d88-169">System. void</span><span class="sxs-lookup"><span data-stu-id="f3d88-169">System.Void</span></span>

## <span data-ttu-id="f3d88-170">Note</span><span class="sxs-lookup"><span data-stu-id="f3d88-170">NOTES</span></span>

## <span data-ttu-id="f3d88-171">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f3d88-171">RELATED LINKS</span></span>

[<span data-ttu-id="f3d88-172">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="f3d88-172">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="f3d88-173">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="f3d88-173">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="f3d88-174">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="f3d88-174">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="f3d88-175">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="f3d88-175">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="f3d88-176">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f3d88-176">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="f3d88-177">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="f3d88-177">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="f3d88-178">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="f3d88-178">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="f3d88-179">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="f3d88-179">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


