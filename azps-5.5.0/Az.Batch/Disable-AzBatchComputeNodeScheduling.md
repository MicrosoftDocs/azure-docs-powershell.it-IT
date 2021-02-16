---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2DF5FB4D-A5CB-439C-AC6F-DF2130AF33EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 9e93d6fd17d4ba308e6d5752554fb03639fce769
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199574"
---
# <span data-ttu-id="2fc47-101">Disable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="2fc47-101">Disable-AzBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="2fc47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fc47-102">SYNOPSIS</span></span>
<span data-ttu-id="2fc47-103">Disabilita la programmazione delle attività nel nodo di elaborazione specificato.</span><span class="sxs-lookup"><span data-stu-id="2fc47-103">Disables task scheduling on the specified compute node.</span></span>

## <span data-ttu-id="2fc47-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2fc47-104">SYNTAX</span></span>

### <span data-ttu-id="2fc47-105">ID (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2fc47-105">Id (Default)</span></span>
```
Disable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String>
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2fc47-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="2fc47-106">InputObject</span></span>
```
Disable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>]
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2fc47-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2fc47-107">DESCRIPTION</span></span>
<span data-ttu-id="2fc47-108">Il cmdlet **Disable-AzBatchComputeNodeScheduling** disabilita la pianificazione delle attività nel nodo di elaborazione specificato.</span><span class="sxs-lookup"><span data-stu-id="2fc47-108">The **Disable-AzBatchComputeNodeScheduling** cmdlet disables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="2fc47-109">Un nodo di elaborazione è una macchina virtuale di Azure dedicata a un carico di lavoro specifico dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2fc47-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>
<span data-ttu-id="2fc47-110">Quando si disabilita la pianificazione delle attività in un nodo di elaborazione, si avrà anche la possibilità di determinare cosa fare sui processi attualmente nella coda di attività del nodo.</span><span class="sxs-lookup"><span data-stu-id="2fc47-110">When you disable task scheduling on a compute node you will also have the option of determining what to do about jobs currently in the node's task queue.</span></span>
<span data-ttu-id="2fc47-111">**Disable-AzBatchComputeNodeScheduling** consente di eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="2fc47-111">**Disable-AzBatchComputeNodeScheduling** lets you do the following:</span></span> 
- <span data-ttu-id="2fc47-112">Terminare le attività e rimessarle nella coda di processi.</span><span class="sxs-lookup"><span data-stu-id="2fc47-112">Terminate the tasks and put them back in the job queue.</span></span>
<span data-ttu-id="2fc47-113">In questo modo queste attività possono essere riprogrammate in un altro nodo di calcolo.</span><span class="sxs-lookup"><span data-stu-id="2fc47-113">This enables those tasks to be rescheduled on another compute node.</span></span> 
- <span data-ttu-id="2fc47-114">Terminare le attività e rimuoverle dalla coda di processi.</span><span class="sxs-lookup"><span data-stu-id="2fc47-114">Terminate the tasks and remove them from the job queue.</span></span>
<span data-ttu-id="2fc47-115">Le attività arrestate in questo modo non verranno ripianificate.</span><span class="sxs-lookup"><span data-stu-id="2fc47-115">Tasks stopped in this manner will not be rescheduled.</span></span> 
- <span data-ttu-id="2fc47-116">Attendere il completamento di tutte le attività attualmente in esecuzione e quindi disabilitare la programmazione delle attività nel nodo di calcolo.</span><span class="sxs-lookup"><span data-stu-id="2fc47-116">Wait for all the tasks currently being executed to complete and then disable task scheduling on the compute node.</span></span> 
- <span data-ttu-id="2fc47-117">Attendere il completamento di tutte le attività in esecuzione e la scadenza di tutti i periodi di conservazione dei dati, quindi disabilitare la programmazione delle attività nel nodo di calcolo.</span><span class="sxs-lookup"><span data-stu-id="2fc47-117">Wait for all the running tasks to complete and all the data retention periods to expire, and then disable task scheduling on the compute node.</span></span>

## <span data-ttu-id="2fc47-118">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2fc47-118">EXAMPLES</span></span>

### <span data-ttu-id="2fc47-119">Esempio 1: Disabilitare la programmazione delle attività in un nodo di calcolo</span><span class="sxs-lookup"><span data-stu-id="2fc47-119">Example 1: Disable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Disable-AzBatchComputeNodeScheduling -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="2fc47-120">Questi comandi disabilitano la pianificazione delle attività nel nodo di calcolo tvm-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="2fc47-120">These commands disable task schedule on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="2fc47-121">A questo scopo, il primo comando dell'esempio crea un riferimento a un oggetto alle chiavi dell'account batch contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="2fc47-121">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="2fc47-122">Questo riferimento all'oggetto è archiviato in una variabile denominata $context.</span><span class="sxs-lookup"><span data-stu-id="2fc47-122">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="2fc47-123">Il secondo comando usa quindi questo riferimento all'oggetto e il cmdlet **Disable-AzBatchComputeNodeScheduling** per connettersi al pool myPool e disabilitare la pianificazione delle attività nel nodo tvm-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="2fc47-123">The second command then uses this object reference and the **Disable-AzBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and disable task scheduling on node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="2fc47-124">Poiché il *parametro DisableComputeNodeSchedulingOptions* non è stato incluso, le attività attualmente in esecuzione nel nodo di calcolo verranno di nuovo in coda.</span><span class="sxs-lookup"><span data-stu-id="2fc47-124">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute node will be requeued.</span></span>

### <span data-ttu-id="2fc47-125">Esempio 2: Disabilitare la pianificazione delle attività in tutti i nodi di calcolo in un pool</span><span class="sxs-lookup"><span data-stu-id="2fc47-125">Example 2: Disable task scheduling on all compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Disable-AzBatchComputeNodeScheduling -BatchContext $Context
```

<span data-ttu-id="2fc47-126">Questi comandi disabilitano la pianificazione delle attività in tutti i nodi del computer nel pool batch06.</span><span class="sxs-lookup"><span data-stu-id="2fc47-126">These commands disable task scheduling on all the computer nodes in the batch pool Pool06.</span></span>
<span data-ttu-id="2fc47-127">Per eseguire questa attività, il primo comando dell'esempio crea un riferimento a un oggetto alle chiavi dell'account batch contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="2fc47-127">To perform this task, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="2fc47-128">Questo riferimento all'oggetto è archiviato in una variabile denominata $context.</span><span class="sxs-lookup"><span data-stu-id="2fc47-128">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="2fc47-129">Il secondo comando nell'esempio usa quindi questo riferimento all'oggetto e **Get-AzBatchComputeNode** per restituire una raccolta di tutti i nodi di calcolo trovati in Pool06.</span><span class="sxs-lookup"><span data-stu-id="2fc47-129">The second command in the example then uses this object reference and **Get-AzBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="2fc47-130">Viene quindi eseguito il piping di questa raccolta al cmdlet **Disable-AzBatchComputeNodeScheduling** per disabilitare la pianificazione delle attività in ogni nodo di calcolo nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="2fc47-130">That collection is then piped to then **Disable-AzBatchComputeNodeScheduling** cmdlet to disable task scheduling on each compute node in the collection.</span></span>
<span data-ttu-id="2fc47-131">Poiché il *parametro DisableComputeNodeSchedulingOptions* non è stato incluso, le attività attualmente in esecuzione nei nodi di calcolo verranno di nuovo in coda.</span><span class="sxs-lookup"><span data-stu-id="2fc47-131">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute nodes will be requeued.</span></span>

## <span data-ttu-id="2fc47-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2fc47-132">PARAMETERS</span></span>

### <span data-ttu-id="2fc47-133">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="2fc47-133">-BatchContext</span></span>
<span data-ttu-id="2fc47-134">Specifica **l'istanza BatchAccountContext** che questo cmdlet usa per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="2fc47-134">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2fc47-135">Se si usa il cmdlet Get-AzBatchAccount per ottenere BatchAccountContext, verrà usata l'autenticazione di Azure Active Directory quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="2fc47-135">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="2fc47-136">Per usare invece l'autenticazione della chiave condivisa, usare il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.</span><span class="sxs-lookup"><span data-stu-id="2fc47-136">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="2fc47-137">Quando si usa l'autenticazione con chiave condivisa, per impostazione predefinita viene usata la chiave di accesso primario.</span><span class="sxs-lookup"><span data-stu-id="2fc47-137">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="2fc47-138">Per modificare la chiave da usare, impostare la proprietà BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="2fc47-138">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="2fc47-139">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="2fc47-139">-ComputeNode</span></span>
<span data-ttu-id="2fc47-140">Specifica un riferimento a un oggetto al nodo di calcolo in cui la programmazione delle attività è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="2fc47-140">Specifies an object reference to the compute node where task scheduling is disabled.</span></span>
<span data-ttu-id="2fc47-141">Questo riferimento all'oggetto viene creato usando il cmdlet Get-AzBatchComputeNode e archiviando l'oggetto nodo di calcolo restituito in una variabile.</span><span class="sxs-lookup"><span data-stu-id="2fc47-141">This object reference is created by using the Get-AzBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

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

### <span data-ttu-id="2fc47-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fc47-142">-DefaultProfile</span></span>
<span data-ttu-id="2fc47-143">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2fc47-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2fc47-144">-DisableSchedulingOption</span><span class="sxs-lookup"><span data-stu-id="2fc47-144">-DisableSchedulingOption</span></span>
<span data-ttu-id="2fc47-145">Specifica in che modo questo cmdlet gestisce le attività attualmente in esecuzione nel nodo del computer in cui la pianificazione è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="2fc47-145">Specifies how this cmdlet deals with any tasks currently running on the computer node where scheduling is being disabled.</span></span>
<span data-ttu-id="2fc47-146">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="2fc47-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2fc47-147">In coda.</span><span class="sxs-lookup"><span data-stu-id="2fc47-147">Requeue.</span></span>
<span data-ttu-id="2fc47-148">Le attività vengono arrestate immediatamente e restituite alla coda di processi.</span><span class="sxs-lookup"><span data-stu-id="2fc47-148">Tasks are stopped immediately and returned to the job queue.</span></span>
<span data-ttu-id="2fc47-149">In questo modo le attività possono essere riprogrammate in un altro nodo di calcolo.</span><span class="sxs-lookup"><span data-stu-id="2fc47-149">This enables the tasks to be rescheduled on another compute node.</span></span>
<span data-ttu-id="2fc47-150">Questo è il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="2fc47-150">This is the default value.</span></span> 
- <span data-ttu-id="2fc47-151">Termina.</span><span class="sxs-lookup"><span data-stu-id="2fc47-151">Terminate.</span></span>
<span data-ttu-id="2fc47-152">Le attività vengono arrestate immediatamente e rimosse dalla coda di processi.</span><span class="sxs-lookup"><span data-stu-id="2fc47-152">Tasks are stopped immediately and removed from the job queue.</span></span>
<span data-ttu-id="2fc47-153">Queste attività non verranno ripianificate.</span><span class="sxs-lookup"><span data-stu-id="2fc47-153">These tasks will not be rescheduled.</span></span> 
- <span data-ttu-id="2fc47-154">TaskCompletion.</span><span class="sxs-lookup"><span data-stu-id="2fc47-154">TaskCompletion.</span></span>
<span data-ttu-id="2fc47-155">Le attività attualmente in esecuzione possono essere completate prima che la programmazione delle attività venga disabilitata nel nodo di calcolo.</span><span class="sxs-lookup"><span data-stu-id="2fc47-155">Currently running tasks will be able to complete before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="2fc47-156">Non verranno programmate nuove attività in questo nodo.</span><span class="sxs-lookup"><span data-stu-id="2fc47-156">No new tasks will be scheduled on this node.</span></span> 
- <span data-ttu-id="2fc47-157">RetainedData.</span><span class="sxs-lookup"><span data-stu-id="2fc47-157">RetainedData.</span></span>
<span data-ttu-id="2fc47-158">Le attività in esecuzione potranno essere completate e i periodi di conservazione dei dati scadranno prima che la programmazione delle attività venga disabilitata nel nodo di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="2fc47-158">Currently running tasks will be able to complete and data retention periods will be able to expire before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="2fc47-159">Non verranno programmate nuove attività in questo nodo.</span><span class="sxs-lookup"><span data-stu-id="2fc47-159">No new tasks will be scheduled on this node.</span></span>

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

### <span data-ttu-id="2fc47-160">-Id</span><span class="sxs-lookup"><span data-stu-id="2fc47-160">-Id</span></span>
<span data-ttu-id="2fc47-161">Specifica l'ID del nodo di calcolo in cui la programmazione delle attività è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="2fc47-161">Specifies the ID of the compute node where task scheduling is disabled.</span></span>

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

### <span data-ttu-id="2fc47-162">-PoolId</span><span class="sxs-lookup"><span data-stu-id="2fc47-162">-PoolId</span></span>
<span data-ttu-id="2fc47-163">Specifica l'ID del pool batch che contiene il nodo di calcolo in cui la programmazione delle attività è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="2fc47-163">Specifies the ID of the batch pool that contains the compute node where task scheduling is disabled.</span></span>
<span data-ttu-id="2fc47-164">Se si usa il *parametro PoolId,* non usare il parametro *ComputeNode* nello stesso comando.</span><span class="sxs-lookup"><span data-stu-id="2fc47-164">If you use the *PoolId* parameter, do not use the *ComputeNode* parameter in that same command.</span></span>

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

### <span data-ttu-id="2fc47-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fc47-165">CommonParameters</span></span>
<span data-ttu-id="2fc47-166">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fc47-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fc47-167">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2fc47-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fc47-168">INPUT</span><span class="sxs-lookup"><span data-stu-id="2fc47-168">INPUTS</span></span>

### <span data-ttu-id="2fc47-169">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="2fc47-169">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="2fc47-170">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="2fc47-170">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="2fc47-171">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2fc47-171">OUTPUTS</span></span>

### <span data-ttu-id="2fc47-172">System.Void</span><span class="sxs-lookup"><span data-stu-id="2fc47-172">System.Void</span></span>

## <span data-ttu-id="2fc47-173">NOTE</span><span class="sxs-lookup"><span data-stu-id="2fc47-173">NOTES</span></span>

## <span data-ttu-id="2fc47-174">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2fc47-174">RELATED LINKS</span></span>

[<span data-ttu-id="2fc47-175">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="2fc47-175">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="2fc47-176">Enable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="2fc47-176">Enable-AzBatchComputeNodeScheduling</span></span>](./Enable-AzBatchComputeNodeScheduling.md)


