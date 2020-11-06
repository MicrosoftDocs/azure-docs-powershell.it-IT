---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 2DF5FB4D-A5CB-439C-AC6F-DF2130AF33EC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/disable-azurebatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchComputeNodeScheduling.md
ms.openlocfilehash: 281e8a883474b3cb0f42b22de1bb00ef2f6e7249
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507640"
---
# <span data-ttu-id="c6d94-101">Disable-AzureBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="c6d94-101">Disable-AzureBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="c6d94-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c6d94-102">SYNOPSIS</span></span>
<span data-ttu-id="c6d94-103">Disabilita la pianificazione delle attività nel nodo Compute specificato.</span><span class="sxs-lookup"><span data-stu-id="c6d94-103">Disables task scheduling on the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6d94-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c6d94-104">SYNTAX</span></span>

### <span data-ttu-id="c6d94-105">ID (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c6d94-105">Id (Default)</span></span>
```
Disable-AzureBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String>
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6d94-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="c6d94-106">InputObject</span></span>
```
Disable-AzureBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>]
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6d94-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c6d94-107">DESCRIPTION</span></span>
<span data-ttu-id="c6d94-108">Il cmdlet **Disable-AzureBatchComputeNodeScheduling Disabilita** la pianificazione delle attività nel nodo Compute specificato.</span><span class="sxs-lookup"><span data-stu-id="c6d94-108">The **Disable-AzureBatchComputeNodeScheduling** cmdlet disables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="c6d94-109">Un nodo COMPUTE è una macchina virtuale di Azure dedicata a un carico di lavoro specifico dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c6d94-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>
<span data-ttu-id="c6d94-110">Quando si disattiva la programmazione delle attività in un nodo di calcolo, si avrà anche la possibilità di determinare le operazioni da eseguire sui processi attualmente presenti nella coda delle attività del nodo.</span><span class="sxs-lookup"><span data-stu-id="c6d94-110">When you disable task scheduling on a compute node you will also have the option of determining what to do about jobs currently in the node's task queue.</span></span>
<span data-ttu-id="c6d94-111">**Disable-AzureBatchComputeNodeScheduling** consente di eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="c6d94-111">**Disable-AzureBatchComputeNodeScheduling** lets you do the following:</span></span> 
- <span data-ttu-id="c6d94-112">Terminare le attività e riportarle nella coda processi.</span><span class="sxs-lookup"><span data-stu-id="c6d94-112">Terminate the tasks and put them back in the job queue.</span></span>
<span data-ttu-id="c6d94-113">Ciò consente di ripianificare le attività in un altro nodo COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="c6d94-113">This enables those tasks to be rescheduled on another compute node.</span></span> 
- <span data-ttu-id="c6d94-114">Terminare le attività e rimuoverle dalla coda processi.</span><span class="sxs-lookup"><span data-stu-id="c6d94-114">Terminate the tasks and remove them from the job queue.</span></span>
<span data-ttu-id="c6d94-115">Le attività interrotte in questo modo non verranno riprogrammate.</span><span class="sxs-lookup"><span data-stu-id="c6d94-115">Tasks stopped in this manner will not be rescheduled.</span></span> 
- <span data-ttu-id="c6d94-116">Attendere che tutte le attività attualmente in esecuzione vengano completate e quindi disabilitare la programmazione delle attività nel nodo COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="c6d94-116">Wait for all the tasks currently being executed to complete and then disable task scheduling on the compute node.</span></span> 
- <span data-ttu-id="c6d94-117">Attendere che tutte le attività in esecuzione vengano completate e tutti i periodi di conservazione dei dati scadano e quindi disabilitare la programmazione delle attività nel nodo COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="c6d94-117">Wait for all the running tasks to complete and all the data retention periods to expire, and then disable task scheduling on the compute node.</span></span>

## <span data-ttu-id="c6d94-118">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c6d94-118">EXAMPLES</span></span>

### <span data-ttu-id="c6d94-119">Esempio 1: disabilitare la pianificazione delle attività in un nodo Compute</span><span class="sxs-lookup"><span data-stu-id="c6d94-119">Example 1: Disable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Disable-AzureBatchComputeNodeScheduling -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="c6d94-120">Questi comandi disabilitano la programmazione delle attività nel nodo di calcolo TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="c6d94-120">These commands disable task schedule on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="c6d94-121">A questo scopo, il primo comando nell'esempio crea un riferimento a un oggetto alle chiavi dell'account per l'account batch contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="c6d94-121">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="c6d94-122">Questo riferimento oggetto è archiviato in una variabile denominata $context.</span><span class="sxs-lookup"><span data-stu-id="c6d94-122">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="c6d94-123">Il secondo comando usa quindi questo riferimento di oggetto e il cmdlet **Disable-AzureBatchComputeNodeScheduling** per connettersi al pool e disabilitare la programmazione delle attività nel nodo TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="c6d94-123">The second command then uses this object reference and the **Disable-AzureBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and disable task scheduling on node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="c6d94-124">Dato che il parametro *DisableComputeNodeSchedulingOptions* non è stato incluso, le attività attualmente in uso nel nodo COMPUTE verranno accodate.</span><span class="sxs-lookup"><span data-stu-id="c6d94-124">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute node will be requeued.</span></span>

### <span data-ttu-id="c6d94-125">Esempio 2: disabilitare la programmazione delle attività in tutti i nodi di calcolo in un pool</span><span class="sxs-lookup"><span data-stu-id="c6d94-125">Example 2: Disable task scheduling on all compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Disable-AzureBatchComputeNodeScheduling -BatchContext $Context
```

<span data-ttu-id="c6d94-126">Questi comandi disabilitano la programmazione delle attività in tutti i nodi del computer nel pool di Pool06.</span><span class="sxs-lookup"><span data-stu-id="c6d94-126">These commands disable task scheduling on all the computer nodes in the batch pool Pool06.</span></span>
<span data-ttu-id="c6d94-127">Per eseguire questa attività, il primo comando nell'esempio crea un riferimento a un oggetto alle chiavi dell'account per l'account batch contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="c6d94-127">To perform this task, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="c6d94-128">Questo riferimento oggetto è archiviato in una variabile denominata $context.</span><span class="sxs-lookup"><span data-stu-id="c6d94-128">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="c6d94-129">Il secondo comando nell'esempio usa quindi questo riferimento di oggetto e **Get-AzureBatchComputeNode** per restituire una raccolta di tutti i nodi di calcolo trovati in Pool06.</span><span class="sxs-lookup"><span data-stu-id="c6d94-129">The second command in the example then uses this object reference and **Get-AzureBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="c6d94-130">La raccolta viene quindi inviata tramite pipe al cmdlet **Disable-AzureBatchComputeNodeScheduling** per disabilitare la pianificazione delle attività in ogni nodo COMPUTE della raccolta.</span><span class="sxs-lookup"><span data-stu-id="c6d94-130">That collection is then piped to then **Disable-AzureBatchComputeNodeScheduling** cmdlet to disable task scheduling on each compute node in the collection.</span></span>
<span data-ttu-id="c6d94-131">Dato che il parametro *DisableComputeNodeSchedulingOptions* non è stato incluso, le attività in corso sui nodi COMPUTE verranno accodate.</span><span class="sxs-lookup"><span data-stu-id="c6d94-131">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute nodes will be requeued.</span></span>

## <span data-ttu-id="c6d94-132">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c6d94-132">PARAMETERS</span></span>

### <span data-ttu-id="c6d94-133">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c6d94-133">-BatchContext</span></span>
<span data-ttu-id="c6d94-134">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="c6d94-134">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c6d94-135">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="c6d94-135">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c6d94-136">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="c6d94-136">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c6d94-137">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="c6d94-137">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c6d94-138">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="c6d94-138">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c6d94-139">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="c6d94-139">-ComputeNode</span></span>
<span data-ttu-id="c6d94-140">Specifica un riferimento a un oggetto al nodo COMPUTE in cui la pianificazione delle attività è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="c6d94-140">Specifies an object reference to the compute node where task scheduling is disabled.</span></span>
<span data-ttu-id="c6d94-141">Questo riferimento all'oggetto viene creato usando il cmdlet Get-AzureBatchComputeNode e archiviando l'oggetto compute node restituito in una variabile.</span><span class="sxs-lookup"><span data-stu-id="c6d94-141">This object reference is created by using the Get-AzureBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6d94-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6d94-142">-DefaultProfile</span></span>
<span data-ttu-id="c6d94-143">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c6d94-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6d94-144">-DisableSchedulingOption</span><span class="sxs-lookup"><span data-stu-id="c6d94-144">-DisableSchedulingOption</span></span>
<span data-ttu-id="c6d94-145">Specifica il modo in cui questo cmdlet tratta le attività attualmente in uso nel nodo del computer in cui viene disabilitata la pianificazione.</span><span class="sxs-lookup"><span data-stu-id="c6d94-145">Specifies how this cmdlet deals with any tasks currently running on the computer node where scheduling is being disabled.</span></span>
<span data-ttu-id="c6d94-146">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c6d94-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c6d94-147">Riaccodare.</span><span class="sxs-lookup"><span data-stu-id="c6d94-147">Requeue.</span></span>
<span data-ttu-id="c6d94-148">Le attività vengono interrotte immediatamente e restituite alla coda processi.</span><span class="sxs-lookup"><span data-stu-id="c6d94-148">Tasks are stopped immediately and returned to the job queue.</span></span>
<span data-ttu-id="c6d94-149">Ciò consente di ripianificare le attività in un altro nodo COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="c6d94-149">This enables the tasks to be rescheduled on another compute node.</span></span>
<span data-ttu-id="c6d94-150">Questo è il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="c6d94-150">This is the default value.</span></span> 
- <span data-ttu-id="c6d94-151">Terminare.</span><span class="sxs-lookup"><span data-stu-id="c6d94-151">Terminate.</span></span>
<span data-ttu-id="c6d94-152">Le attività vengono arrestate immediatamente e rimosse dalla coda processi.</span><span class="sxs-lookup"><span data-stu-id="c6d94-152">Tasks are stopped immediately and removed from the job queue.</span></span>
<span data-ttu-id="c6d94-153">Queste attività non verranno riprogrammate.</span><span class="sxs-lookup"><span data-stu-id="c6d94-153">These tasks will not be rescheduled.</span></span> 
- <span data-ttu-id="c6d94-154">TaskCompletion.</span><span class="sxs-lookup"><span data-stu-id="c6d94-154">TaskCompletion.</span></span>
<span data-ttu-id="c6d94-155">Le attività in esecuzione saranno in grado di completare prima della disattivazione della pianificazione delle attività nel nodo COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="c6d94-155">Currently running tasks will be able to complete before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="c6d94-156">In questo nodo non verranno pianificate nuove attività.</span><span class="sxs-lookup"><span data-stu-id="c6d94-156">No new tasks will be scheduled on this node.</span></span> 
- <span data-ttu-id="c6d94-157">RetainedData.</span><span class="sxs-lookup"><span data-stu-id="c6d94-157">RetainedData.</span></span>
<span data-ttu-id="c6d94-158">Le attività in esecuzione saranno in grado di completare e i periodi di conservazione dei dati potranno scadere prima che la pianificazione delle attività sia disabilitata nel nodo COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="c6d94-158">Currently running tasks will be able to complete and data retention periods will be able to expire before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="c6d94-159">In questo nodo non verranno pianificate nuove attività.</span><span class="sxs-lookup"><span data-stu-id="c6d94-159">No new tasks will be scheduled on this node.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.DisableComputeNodeSchedulingOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6d94-160">-ID</span><span class="sxs-lookup"><span data-stu-id="c6d94-160">-Id</span></span>
<span data-ttu-id="c6d94-161">Specifica l'ID del nodo COMPUTE in cui la pianificazione delle attività è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="c6d94-161">Specifies the ID of the compute node where task scheduling is disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6d94-162">-PoolId</span><span class="sxs-lookup"><span data-stu-id="c6d94-162">-PoolId</span></span>
<span data-ttu-id="c6d94-163">Specifica l'ID del pool di batch che contiene il nodo COMPUTE in cui la pianificazione delle attività è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="c6d94-163">Specifies the ID of the batch pool that contains the compute node where task scheduling is disabled.</span></span>
<span data-ttu-id="c6d94-164">Se usi il parametro *PoolId* , non usare il parametro *ComputeNode* nello stesso comando.</span><span class="sxs-lookup"><span data-stu-id="c6d94-164">If you use the *PoolId* parameter, do not use the *ComputeNode* parameter in that same command.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6d94-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6d94-165">CommonParameters</span></span>
<span data-ttu-id="c6d94-166">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6d94-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6d94-167">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6d94-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6d94-168">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c6d94-168">INPUTS</span></span>

### <span data-ttu-id="c6d94-169">Microsoft.Azure.Commands.Batch. Models. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="c6d94-169">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>
<span data-ttu-id="c6d94-170">Parametri: ComputeNode (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c6d94-170">Parameters: ComputeNode (ByValue)</span></span>

### <span data-ttu-id="c6d94-171">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c6d94-171">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="c6d94-172">Parametri: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c6d94-172">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="c6d94-173">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c6d94-173">OUTPUTS</span></span>

### <span data-ttu-id="c6d94-174">System. void</span><span class="sxs-lookup"><span data-stu-id="c6d94-174">System.Void</span></span>

## <span data-ttu-id="c6d94-175">Note</span><span class="sxs-lookup"><span data-stu-id="c6d94-175">NOTES</span></span>

## <span data-ttu-id="c6d94-176">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c6d94-176">RELATED LINKS</span></span>

[<span data-ttu-id="c6d94-177">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c6d94-177">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="c6d94-178">Enable-AzureBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="c6d94-178">Enable-AzureBatchComputeNodeScheduling</span></span>](./Enable-AzureBatchComputeNodeScheduling.md)

