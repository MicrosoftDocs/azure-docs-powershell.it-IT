---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 93614655-A8F2-4A67-887D-43D41AB91F82
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchComputeNode.md
ms.openlocfilehash: f503352352c31369e594325c060cf0ab68490095
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521786"
---
# <span data-ttu-id="ad360-101">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="ad360-101">Get-AzureBatchComputeNode</span></span>

## <span data-ttu-id="ad360-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ad360-102">SYNOPSIS</span></span>
<span data-ttu-id="ad360-103">Ottiene i nodi di calcolo batch da un pool.</span><span class="sxs-lookup"><span data-stu-id="ad360-103">Gets Batch compute nodes from a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad360-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ad360-104">SYNTAX</span></span>

### <span data-ttu-id="ad360-105">ODataFilter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ad360-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchComputeNode [-PoolId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad360-106">ID</span><span class="sxs-lookup"><span data-stu-id="ad360-106">Id</span></span>
```
Get-AzureBatchComputeNode [-PoolId] <String> [[-Id] <String>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad360-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="ad360-107">ParentObject</span></span>
```
Get-AzureBatchComputeNode [[-Pool] <PSCloudPool>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad360-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad360-108">DESCRIPTION</span></span>
<span data-ttu-id="ad360-109">Il cmdlet **Get-AzureBatchComputeNode** ottiene i nodi di calcolo batch di Azure da un pool.</span><span class="sxs-lookup"><span data-stu-id="ad360-109">The **Get-AzureBatchComputeNode** cmdlet gets Azure Batch compute nodes from a pool.</span></span>
<span data-ttu-id="ad360-110">Specifica il parametro *PoolID* o *pool* .</span><span class="sxs-lookup"><span data-stu-id="ad360-110">Specify either the *PoolID* or *Pool* parameter.</span></span>
<span data-ttu-id="ad360-111">Specifica il parametro *ID* per ottenere un singolo nodo COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="ad360-111">Specify the *Id* parameter to get a single compute node.</span></span>
<span data-ttu-id="ad360-112">Specifica il parametro *Filter* per ottenere i nodi compute che corrispondono a un filtro OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="ad360-112">Specify the *Filter* parameter to get the compute nodes that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="ad360-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ad360-113">EXAMPLES</span></span>

### <span data-ttu-id="ad360-114">Esempio 1: ottenere un nodo COMPUTE in base all'ID</span><span class="sxs-lookup"><span data-stu-id="ad360-114">Example 1: Get a compute node by ID</span></span>
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

<span data-ttu-id="ad360-115">Questo comando ottiene il nodo Compute che contiene l'ID TVM-2316545714_1-20150725t213220z dal pool con ID Pool06.</span><span class="sxs-lookup"><span data-stu-id="ad360-115">This command gets the compute node that has the ID tvm-2316545714_1-20150725t213220z from the pool that has the ID Pool06.</span></span>
<span data-ttu-id="ad360-116">Usa il cmdlet Get-AzureRmBatchAccountKeys per assegnare un contesto alla variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="ad360-116">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="ad360-117">Esempio 2: ottenere tutti i nodi di calcolo inattivi da un pool</span><span class="sxs-lookup"><span data-stu-id="ad360-117">Example 2: Get all idle compute nodes from a pool</span></span>
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

<span data-ttu-id="ad360-118">Questo comando ottiene tutti i nodi di calcolo inattivi contenuti nel pool che contiene l'ID Pool06.</span><span class="sxs-lookup"><span data-stu-id="ad360-118">This command gets all idle compute nodes that are contained in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="ad360-119">Il comando specifica lo stato inattivo usando il parametro *Filter* .</span><span class="sxs-lookup"><span data-stu-id="ad360-119">The command specifies the idle state by using the *Filter* parameter.</span></span>

### <span data-ttu-id="ad360-120">Esempio 3: ottenere tutti i nodi di calcolo in un pool specificato</span><span class="sxs-lookup"><span data-stu-id="ad360-120">Example 3: Get all compute nodes in a specified pool</span></span>
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

<span data-ttu-id="ad360-121">Questo comando ottiene il pool con ID Pool07 usando il cmdlet Get-AzureBatchPool.</span><span class="sxs-lookup"><span data-stu-id="ad360-121">This command gets the pool that has the ID Pool07 by using the Get-AzureBatchPool cmdlet.</span></span>
<span data-ttu-id="ad360-122">Il comando passa il pool al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="ad360-122">The command passes that pool to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ad360-123">Questo cmdlet recupera tutti i nodi compute da tale pool.</span><span class="sxs-lookup"><span data-stu-id="ad360-123">That cmdlet gets all compute nodes from that pool.</span></span>

## <span data-ttu-id="ad360-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ad360-124">PARAMETERS</span></span>

### <span data-ttu-id="ad360-125">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ad360-125">-BatchContext</span></span>
<span data-ttu-id="ad360-126">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="ad360-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ad360-127">Per ottenere un oggetto **BatchAccountContext** che contiene i tasti di scelta per l'abbonamento, usare il cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="ad360-127">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="ad360-128">-Filtro</span><span class="sxs-lookup"><span data-stu-id="ad360-128">-Filter</span></span>
<span data-ttu-id="ad360-129">Specifica una clausola di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="ad360-129">Specifies an OData filter clause.</span></span>
<span data-ttu-id="ad360-130">Questo cmdlet restituisce i nodi compute che corrispondono al filtro specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="ad360-130">This cmdlet returns compute nodes that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="ad360-131">Se non specifichi un filtro, questo cmdlet restituisce tutti i nodi compute per il pool.</span><span class="sxs-lookup"><span data-stu-id="ad360-131">If you do not specify a filter, this cmdlet returns all compute nodes for the pool.</span></span>

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

### <span data-ttu-id="ad360-132">-ID</span><span class="sxs-lookup"><span data-stu-id="ad360-132">-Id</span></span>
<span data-ttu-id="ad360-133">Specifica l'ID del nodo Compute che questo cmdlet ottiene dal pool.</span><span class="sxs-lookup"><span data-stu-id="ad360-133">Specifies the ID of the compute node that this cmdlet gets from the pool.</span></span>
<span data-ttu-id="ad360-134">Non è possibile specificare caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="ad360-134">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad360-135">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="ad360-135">-MaxCount</span></span>
<span data-ttu-id="ad360-136">Specifica il numero massimo di nodi compute da restituire.</span><span class="sxs-lookup"><span data-stu-id="ad360-136">Specifies the maximum number of compute nodes to return.</span></span>
<span data-ttu-id="ad360-137">Se specifichi un valore pari a zero (0) o meno, il cmdlet non usa un limite superiore.</span><span class="sxs-lookup"><span data-stu-id="ad360-137">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="ad360-138">Il valore predefinito è 1000.</span><span class="sxs-lookup"><span data-stu-id="ad360-138">The default value is 1000.</span></span>

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

### <span data-ttu-id="ad360-139">-Pool</span><span class="sxs-lookup"><span data-stu-id="ad360-139">-Pool</span></span>
<span data-ttu-id="ad360-140">Specifica il pool, come oggetto **PSCloudPool** , che contiene i nodi compute.</span><span class="sxs-lookup"><span data-stu-id="ad360-140">Specifies the pool, as a **PSCloudPool** object, that contains the compute nodes.</span></span>
<span data-ttu-id="ad360-141">Per ottenere un oggetto **PSCloudPool** , usa il cmdlet Get-AzureBatchPool.</span><span class="sxs-lookup"><span data-stu-id="ad360-141">To obtain a **PSCloudPool** object, use the Get-AzureBatchPool cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudPool
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad360-142">-PoolId</span><span class="sxs-lookup"><span data-stu-id="ad360-142">-PoolId</span></span>
<span data-ttu-id="ad360-143">Specifica l'ID del pool che contiene i nodi compute.</span><span class="sxs-lookup"><span data-stu-id="ad360-143">Specifies the ID of the pool that contains the compute nodes.</span></span>

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

### <span data-ttu-id="ad360-144">-Selezionare</span><span class="sxs-lookup"><span data-stu-id="ad360-144">-Select</span></span>
<span data-ttu-id="ad360-145">Specifica una clausola di selezione OData.</span><span class="sxs-lookup"><span data-stu-id="ad360-145">Specifies an OData select clause.</span></span>
<span data-ttu-id="ad360-146">Specifica un valore per questo parametro per ottenere proprietà specifiche anziché tutte le proprietà dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ad360-146">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="ad360-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad360-147">-DefaultProfile</span></span>
<span data-ttu-id="ad360-148">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ad360-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad360-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad360-149">CommonParameters</span></span>
<span data-ttu-id="ad360-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad360-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad360-151">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad360-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad360-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ad360-152">INPUTS</span></span>

### <span data-ttu-id="ad360-153">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ad360-153">BatchAccountContext</span></span>
<span data-ttu-id="ad360-154">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="ad360-154">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="ad360-155">PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="ad360-155">PSCloudPool</span></span>
<span data-ttu-id="ad360-156">Il parametro "pool" accetta il valore di tipo "PSCloudPool" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="ad360-156">Parameter 'Pool' accepts value of type 'PSCloudPool' from the pipeline</span></span>

## <span data-ttu-id="ad360-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ad360-157">OUTPUTS</span></span>

### <span data-ttu-id="ad360-158">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="ad360-158">PSComputeNode</span></span>

## <span data-ttu-id="ad360-159">Note</span><span class="sxs-lookup"><span data-stu-id="ad360-159">NOTES</span></span>

## <span data-ttu-id="ad360-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ad360-160">RELATED LINKS</span></span>

[<span data-ttu-id="ad360-161">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="ad360-161">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="ad360-162">Get-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="ad360-162">Get-AzureBatchNodeFile</span></span>](./Get-AzureBatchNodeFile.md)

[<span data-ttu-id="ad360-163">Get-AzureBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="ad360-163">Get-AzureBatchNodeFileContent</span></span>](./Get-AzureBatchNodeFileContent.md)

[<span data-ttu-id="ad360-164">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="ad360-164">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="ad360-165">Reset-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="ad360-165">Reset-AzureBatchComputeNode</span></span>](./Reset-AzureBatchComputeNode.md)

[<span data-ttu-id="ad360-166">Riavviare-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="ad360-166">Restart-AzureBatchComputeNode</span></span>](./Restart-AzureBatchComputeNode.md)

[<span data-ttu-id="ad360-167">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="ad360-167">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


