---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 93614655-A8F2-4A67-887D-43D41AB91F82
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchComputeNode.md
ms.openlocfilehash: d5cbd8c37f6d527a741f5bb92211d6b4f90b8113
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520474"
---
# <span data-ttu-id="27ee8-101">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="27ee8-101">Get-AzureBatchComputeNode</span></span>

## <span data-ttu-id="27ee8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="27ee8-102">SYNOPSIS</span></span>
<span data-ttu-id="27ee8-103">Ottiene i nodi di calcolo batch da un pool.</span><span class="sxs-lookup"><span data-stu-id="27ee8-103">Gets Batch compute nodes from a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27ee8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="27ee8-104">SYNTAX</span></span>

### <span data-ttu-id="27ee8-105">ODataFilter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="27ee8-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchComputeNode [-PoolId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27ee8-106">ID</span><span class="sxs-lookup"><span data-stu-id="27ee8-106">Id</span></span>
```
Get-AzureBatchComputeNode [-PoolId] <String> [[-Id] <String>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27ee8-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="27ee8-107">ParentObject</span></span>
```
Get-AzureBatchComputeNode [[-Pool] <PSCloudPool>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27ee8-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="27ee8-108">DESCRIPTION</span></span>
<span data-ttu-id="27ee8-109">Il cmdlet **Get-AzureBatchComputeNode** ottiene i nodi di calcolo batch di Azure da un pool.</span><span class="sxs-lookup"><span data-stu-id="27ee8-109">The **Get-AzureBatchComputeNode** cmdlet gets Azure Batch compute nodes from a pool.</span></span>
<span data-ttu-id="27ee8-110">Specifica il parametro *PoolID* o *pool* .</span><span class="sxs-lookup"><span data-stu-id="27ee8-110">Specify either the *PoolID* or *Pool* parameter.</span></span>
<span data-ttu-id="27ee8-111">Specifica il parametro *ID* per ottenere un singolo nodo COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="27ee8-111">Specify the *Id* parameter to get a single compute node.</span></span>
<span data-ttu-id="27ee8-112">Specifica il parametro *Filter* per ottenere i nodi compute che corrispondono a un filtro OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="27ee8-112">Specify the *Filter* parameter to get the compute nodes that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="27ee8-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="27ee8-113">EXAMPLES</span></span>

### <span data-ttu-id="27ee8-114">Esempio 1: ottenere un nodo COMPUTE in base all'ID</span><span class="sxs-lookup"><span data-stu-id="27ee8-114">Example 1: Get a compute node by ID</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "Pool06" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : small
TotalTasksRun         : 1
StartTaskInformation  : 
RecentTasks           : {}
StartTask             : 
CertificateReferences : 
Errors                :
```

<span data-ttu-id="27ee8-115">Questo comando ottiene il nodo Compute che contiene l'ID TVM-2316545714_1-20150725t213220z dal pool con ID Pool06.</span><span class="sxs-lookup"><span data-stu-id="27ee8-115">This command gets the compute node that has the ID tvm-2316545714_1-20150725t213220z from the pool that has the ID Pool06.</span></span>
<span data-ttu-id="27ee8-116">Usa il cmdlet Get-AzureRmBatchAccountKeys per assegnare un contesto alla variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="27ee8-116">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="27ee8-117">Esempio 2: ottenere tutti i nodi di calcolo inattivi da un pool</span><span class="sxs-lookup"><span data-stu-id="27ee8-117">Example 2: Get all idle compute nodes from a pool</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "Pool06" -Filter "state eq 'idle'" -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : small
TotalTasksRun         : 1
StartTaskInformation  : 
RecentTasks           : {}
StartTask             : 
CertificateReferences : 
Errors                : 

Id                    : tvm-2316545714_2-20150726t172920z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_2-20150726t172920z
State                 : Idle
StateTransitionTime   : 7/26/2015 5:33:58 PM
LastBootTime          : 7/26/2015 5:33:58 PM
AllocationTime        : 7/26/2015 5:29:20 PM
IPAddress             : 10.14.121.38
AffinityId            : TVM:tvm-2316545714_2-20150726t172920z
VirtualMachineSize    : small
TotalTasksRun         : 0
StartTaskInformation  : 
RecentTasks           : 
StartTask             : 
CertificateReferences : 
Errors                :
```

<span data-ttu-id="27ee8-118">Questo comando ottiene tutti i nodi di calcolo inattivi contenuti nel pool che contiene l'ID Pool06.</span><span class="sxs-lookup"><span data-stu-id="27ee8-118">This command gets all idle compute nodes that are contained in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="27ee8-119">Il comando specifica lo stato inattivo usando il parametro *Filter* .</span><span class="sxs-lookup"><span data-stu-id="27ee8-119">The command specifies the idle state by using the *Filter* parameter.</span></span>

### <span data-ttu-id="27ee8-120">Esempio 3: ottenere tutti i nodi di calcolo in un pool specificato</span><span class="sxs-lookup"><span data-stu-id="27ee8-120">Example 3: Get all compute nodes in a specified pool</span></span>
```
PS C:\>Get-AzureBatchPool -Id "Pool07" -BatchContext $Context | Get-AzureBatchComputeNode -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : small
TotalTasksRun         : 1
StartTaskInformation  : 
RecentTasks           : {}
StartTask             : 
CertificateReferences : 
Errors                : 


Id                    : tvm-2316545714_2-20150726t172920z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_2-20150726t172920z
State                 : Idle
StateTransitionTime   : 7/26/2015 5:33:58 PM
LastBootTime          : 7/26/2015 5:33:58 PM
AllocationTime        : 7/26/2015 5:29:20 PM

IPAddress             : 10.14.121.38
AffinityId            : TVM:tvm-2316545714_2-20150726t172920z
VirtualMachineSize    : small
TotalTasksRun         : 0
StartTaskInformation  : 
RecentTasks           : 
StartTask             : 
CertificateReferences : 
Errors                :
```

<span data-ttu-id="27ee8-121">Questo comando ottiene il pool con ID Pool07 usando il cmdlet Get-AzureBatchPool.</span><span class="sxs-lookup"><span data-stu-id="27ee8-121">This command gets the pool that has the ID Pool07 by using the Get-AzureBatchPool cmdlet.</span></span>
<span data-ttu-id="27ee8-122">Il comando passa il pool al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="27ee8-122">The command passes that pool to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="27ee8-123">Questo cmdlet recupera tutti i nodi compute da tale pool.</span><span class="sxs-lookup"><span data-stu-id="27ee8-123">That cmdlet gets all compute nodes from that pool.</span></span>

## <span data-ttu-id="27ee8-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="27ee8-124">PARAMETERS</span></span>

### <span data-ttu-id="27ee8-125">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="27ee8-125">-BatchContext</span></span>
<span data-ttu-id="27ee8-126">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="27ee8-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="27ee8-127">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="27ee8-127">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="27ee8-128">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="27ee8-128">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="27ee8-129">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="27ee8-129">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="27ee8-130">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="27ee8-130">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="27ee8-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27ee8-131">-DefaultProfile</span></span>
<span data-ttu-id="27ee8-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="27ee8-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27ee8-133">-Filtro</span><span class="sxs-lookup"><span data-stu-id="27ee8-133">-Filter</span></span>
<span data-ttu-id="27ee8-134">Specifica una clausola di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="27ee8-134">Specifies an OData filter clause.</span></span>
<span data-ttu-id="27ee8-135">Questo cmdlet restituisce i nodi compute che corrispondono al filtro specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="27ee8-135">This cmdlet returns compute nodes that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="27ee8-136">Se non specifichi un filtro, questo cmdlet restituisce tutti i nodi compute per il pool.</span><span class="sxs-lookup"><span data-stu-id="27ee8-136">If you do not specify a filter, this cmdlet returns all compute nodes for the pool.</span></span>

```yaml
Type: String
Parameter Sets: ODataFilter, ParentObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27ee8-137">-ID</span><span class="sxs-lookup"><span data-stu-id="27ee8-137">-Id</span></span>
<span data-ttu-id="27ee8-138">Specifica l'ID del nodo Compute che questo cmdlet ottiene dal pool.</span><span class="sxs-lookup"><span data-stu-id="27ee8-138">Specifies the ID of the compute node that this cmdlet gets from the pool.</span></span>
<span data-ttu-id="27ee8-139">Non è possibile specificare caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="27ee8-139">You cannot specify wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27ee8-140">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="27ee8-140">-MaxCount</span></span>
<span data-ttu-id="27ee8-141">Specifica il numero massimo di nodi compute da restituire.</span><span class="sxs-lookup"><span data-stu-id="27ee8-141">Specifies the maximum number of compute nodes to return.</span></span>
<span data-ttu-id="27ee8-142">Se specifichi un valore pari a zero (0) o meno, il cmdlet non usa un limite superiore.</span><span class="sxs-lookup"><span data-stu-id="27ee8-142">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="27ee8-143">Il valore predefinito è 1000.</span><span class="sxs-lookup"><span data-stu-id="27ee8-143">The default value is 1000.</span></span>

```yaml
Type: Int32
Parameter Sets: ODataFilter, ParentObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27ee8-144">-Pool</span><span class="sxs-lookup"><span data-stu-id="27ee8-144">-Pool</span></span>
<span data-ttu-id="27ee8-145">Specifica il pool, come oggetto **PSCloudPool** , che contiene i nodi compute.</span><span class="sxs-lookup"><span data-stu-id="27ee8-145">Specifies the pool, as a **PSCloudPool** object, that contains the compute nodes.</span></span>
<span data-ttu-id="27ee8-146">Per ottenere un oggetto **PSCloudPool** , usa il cmdlet Get-AzureBatchPool.</span><span class="sxs-lookup"><span data-stu-id="27ee8-146">To obtain a **PSCloudPool** object, use the Get-AzureBatchPool cmdlet.</span></span>

```yaml
Type: PSCloudPool
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27ee8-147">-PoolId</span><span class="sxs-lookup"><span data-stu-id="27ee8-147">-PoolId</span></span>
<span data-ttu-id="27ee8-148">Specifica l'ID del pool che contiene i nodi compute.</span><span class="sxs-lookup"><span data-stu-id="27ee8-148">Specifies the ID of the pool that contains the compute nodes.</span></span>

```yaml
Type: String
Parameter Sets: ODataFilter, Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27ee8-149">-Selezionare</span><span class="sxs-lookup"><span data-stu-id="27ee8-149">-Select</span></span>
<span data-ttu-id="27ee8-150">Specifica una clausola di selezione OData.</span><span class="sxs-lookup"><span data-stu-id="27ee8-150">Specifies an OData select clause.</span></span>
<span data-ttu-id="27ee8-151">Specifica un valore per questo parametro per ottenere proprietà specifiche anziché tutte le proprietà dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="27ee8-151">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="27ee8-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27ee8-152">CommonParameters</span></span>
<span data-ttu-id="27ee8-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27ee8-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27ee8-154">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27ee8-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27ee8-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="27ee8-155">INPUTS</span></span>

### <span data-ttu-id="27ee8-156">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="27ee8-156">BatchAccountContext</span></span>
<span data-ttu-id="27ee8-157">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="27ee8-157">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="27ee8-158">PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="27ee8-158">PSCloudPool</span></span>
<span data-ttu-id="27ee8-159">Il parametro "pool" accetta il valore di tipo "PSCloudPool" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="27ee8-159">Parameter 'Pool' accepts value of type 'PSCloudPool' from the pipeline</span></span>

## <span data-ttu-id="27ee8-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="27ee8-160">OUTPUTS</span></span>

### <span data-ttu-id="27ee8-161">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="27ee8-161">PSComputeNode</span></span>

## <span data-ttu-id="27ee8-162">Note</span><span class="sxs-lookup"><span data-stu-id="27ee8-162">NOTES</span></span>

## <span data-ttu-id="27ee8-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="27ee8-163">RELATED LINKS</span></span>

[<span data-ttu-id="27ee8-164">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="27ee8-164">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="27ee8-165">Get-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="27ee8-165">Get-AzureBatchNodeFile</span></span>](./Get-AzureBatchNodeFile.md)

[<span data-ttu-id="27ee8-166">Get-AzureBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="27ee8-166">Get-AzureBatchNodeFileContent</span></span>](./Get-AzureBatchNodeFileContent.md)

[<span data-ttu-id="27ee8-167">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="27ee8-167">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="27ee8-168">Reset-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="27ee8-168">Reset-AzureBatchComputeNode</span></span>](./Reset-AzureBatchComputeNode.md)

[<span data-ttu-id="27ee8-169">Riavviare-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="27ee8-169">Restart-AzureBatchComputeNode</span></span>](./Restart-AzureBatchComputeNode.md)

[<span data-ttu-id="27ee8-170">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="27ee8-170">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


