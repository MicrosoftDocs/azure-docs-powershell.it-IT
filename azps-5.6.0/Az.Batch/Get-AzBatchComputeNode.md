---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 93614655-A8F2-4A67-887D-43D41AB91F82
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchComputeNode.md
ms.openlocfilehash: 2adaebc28f27d2ea785df5a93510375020bcd542
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990484"
---
# <span data-ttu-id="64ff6-101">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="64ff6-101">Get-AzBatchComputeNode</span></span>

## <span data-ttu-id="64ff6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64ff6-102">SYNOPSIS</span></span>
<span data-ttu-id="64ff6-103">Recupera i nodi di elaborazione batch da un pool.</span><span class="sxs-lookup"><span data-stu-id="64ff6-103">Gets Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="64ff6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="64ff6-104">SYNTAX</span></span>

### <span data-ttu-id="64ff6-105">ODataFilter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="64ff6-105">ODataFilter (Default)</span></span>
```
Get-AzBatchComputeNode [-PoolId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64ff6-106">ID</span><span class="sxs-lookup"><span data-stu-id="64ff6-106">Id</span></span>
```
Get-AzBatchComputeNode [-PoolId] <String> [[-Id] <String>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64ff6-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="64ff6-107">ParentObject</span></span>
```
Get-AzBatchComputeNode [[-Pool] <PSCloudPool>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64ff6-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="64ff6-108">DESCRIPTION</span></span>
<span data-ttu-id="64ff6-109">Il cmdlet **Get-AzBatchComputeNode** ottiene i nodi di elaborazione batch di Azure da un pool.</span><span class="sxs-lookup"><span data-stu-id="64ff6-109">The **Get-AzBatchComputeNode** cmdlet gets Azure Batch compute nodes from a pool.</span></span>
<span data-ttu-id="64ff6-110">Specificare il *parametro PoolID* *o Pool.*</span><span class="sxs-lookup"><span data-stu-id="64ff6-110">Specify either the *PoolID* or *Pool* parameter.</span></span>
<span data-ttu-id="64ff6-111">Specificare il *parametro ID* per ottenere un singolo nodo di calcolo.</span><span class="sxs-lookup"><span data-stu-id="64ff6-111">Specify the *Id* parameter to get a single compute node.</span></span>
<span data-ttu-id="64ff6-112">Specificare il *parametro Filter* per ottenere i nodi di elaborazione che corrispondono a un filtro OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="64ff6-112">Specify the *Filter* parameter to get the compute nodes that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="64ff6-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="64ff6-113">EXAMPLES</span></span>

### <span data-ttu-id="64ff6-114">Esempio 1: Ottenere un nodo di calcolo in base all'ID</span><span class="sxs-lookup"><span data-stu-id="64ff6-114">Example 1: Get a compute node by ID</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool06" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : standard_d1_v2
TotalTasksRun         : 1
StartTaskInformation  :
RecentTasks           : {}
StartTask             :
CertificateReferences :
Errors                :
```

<span data-ttu-id="64ff6-115">Questo comando recupera il nodo di calcolo con ID tvm-2316545714_1-20150725t213220z dal pool che contiene l'ID Pool06.</span><span class="sxs-lookup"><span data-stu-id="64ff6-115">This command gets the compute node that has the ID tvm-2316545714_1-20150725t213220z from the pool that has the ID Pool06.</span></span>
<span data-ttu-id="64ff6-116">Usare il cmdlet Get-AzBatchAccountKey per assegnare un contesto alla $Context variabile.</span><span class="sxs-lookup"><span data-stu-id="64ff6-116">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="64ff6-117">Esempio 2: Recuperare tutti i nodi di elaborazione inattivi da un pool</span><span class="sxs-lookup"><span data-stu-id="64ff6-117">Example 2: Get all idle compute nodes from a pool</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool06" -Filter "state eq 'idle'" -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : standard_d1_v2
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
VirtualMachineSize    : standard_d1_v2
TotalTasksRun         : 0
StartTaskInformation  :
RecentTasks           :
StartTask             :
CertificateReferences :
Errors                :
```

<span data-ttu-id="64ff6-118">Questo comando recupera tutti i nodi di elaborazione inattivi contenuti nel pool con l'ID Pool06.</span><span class="sxs-lookup"><span data-stu-id="64ff6-118">This command gets all idle compute nodes that are contained in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="64ff6-119">Il comando specifica lo stato inattivo usando il *parametro Filter.*</span><span class="sxs-lookup"><span data-stu-id="64ff6-119">The command specifies the idle state by using the *Filter* parameter.</span></span>

### <span data-ttu-id="64ff6-120">Esempio 3: Ottenere tutti i nodi di calcolo in un pool specificato</span><span class="sxs-lookup"><span data-stu-id="64ff6-120">Example 3: Get all compute nodes in a specified pool</span></span>
```
PS C:\>Get-AzBatchPool -Id "Pool07" -BatchContext $Context | Get-AzBatchComputeNode -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : standard_d1_v2
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
VirtualMachineSize    : standard_d1_v2
TotalTasksRun         : 0
StartTaskInformation  :
RecentTasks           :
StartTask             :
CertificateReferences :
Errors                :
```

<span data-ttu-id="64ff6-121">Questo comando ottiene il pool che ha l'ID Pool07 usando il cmdlet Get-AzBatchPool.</span><span class="sxs-lookup"><span data-stu-id="64ff6-121">This command gets the pool that has the ID Pool07 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="64ff6-122">Il comando passa il pool al cmdlet corrente usando l'operatore della pipeline.</span><span class="sxs-lookup"><span data-stu-id="64ff6-122">The command passes that pool to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="64ff6-123">Questo cmdlet recupera tutti i nodi di elaborazione dal pool.</span><span class="sxs-lookup"><span data-stu-id="64ff6-123">That cmdlet gets all compute nodes from that pool.</span></span>

## <span data-ttu-id="64ff6-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64ff6-124">PARAMETERS</span></span>

### <span data-ttu-id="64ff6-125">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="64ff6-125">-BatchContext</span></span>
<span data-ttu-id="64ff6-126">Specifica **l'istanza BatchAccountContext** che questo cmdlet usa per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="64ff6-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="64ff6-127">Se si usa il cmdlet Get-AzBatchAccount per ottenere BatchAccountContext, verrà usata l'autenticazione di Azure Active Directory quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="64ff6-127">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="64ff6-128">Per usare invece l'autenticazione della chiave condivisa, usare il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.</span><span class="sxs-lookup"><span data-stu-id="64ff6-128">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="64ff6-129">Quando si usa l'autenticazione con chiave condivisa, per impostazione predefinita viene usata la chiave di accesso primario.</span><span class="sxs-lookup"><span data-stu-id="64ff6-129">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="64ff6-130">Per modificare la chiave da usare, impostare la proprietà BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="64ff6-130">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="64ff6-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64ff6-131">-DefaultProfile</span></span>
<span data-ttu-id="64ff6-132">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="64ff6-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64ff6-133">-Filter</span><span class="sxs-lookup"><span data-stu-id="64ff6-133">-Filter</span></span>
<span data-ttu-id="64ff6-134">Specifica una clausola del filtro OData.</span><span class="sxs-lookup"><span data-stu-id="64ff6-134">Specifies an OData filter clause.</span></span>
<span data-ttu-id="64ff6-135">Questo cmdlet restituisce i nodi di calcolo che corrispondono al filtro specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="64ff6-135">This cmdlet returns compute nodes that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="64ff6-136">Se non si specifica un filtro, questo cmdlet restituisce tutti i nodi di calcolo per il pool.</span><span class="sxs-lookup"><span data-stu-id="64ff6-136">If you do not specify a filter, this cmdlet returns all compute nodes for the pool.</span></span>

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

### <span data-ttu-id="64ff6-137">-Id</span><span class="sxs-lookup"><span data-stu-id="64ff6-137">-Id</span></span>
<span data-ttu-id="64ff6-138">Specifica l'ID del nodo di calcolo che il cmdlet ottiene dal pool.</span><span class="sxs-lookup"><span data-stu-id="64ff6-138">Specifies the ID of the compute node that this cmdlet gets from the pool.</span></span>
<span data-ttu-id="64ff6-139">Non è possibile specificare caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="64ff6-139">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="64ff6-140">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="64ff6-140">-MaxCount</span></span>
<span data-ttu-id="64ff6-141">Specifica il numero massimo di nodi di calcolo da restituire.</span><span class="sxs-lookup"><span data-stu-id="64ff6-141">Specifies the maximum number of compute nodes to return.</span></span>
<span data-ttu-id="64ff6-142">Se si specifica un valore uguale o inferiore a zero (0), il cmdlet non usa un limite superiore.</span><span class="sxs-lookup"><span data-stu-id="64ff6-142">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="64ff6-143">Il valore predefinito è 1000.</span><span class="sxs-lookup"><span data-stu-id="64ff6-143">The default value is 1000.</span></span>

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

### <span data-ttu-id="64ff6-144">-Pool</span><span class="sxs-lookup"><span data-stu-id="64ff6-144">-Pool</span></span>
<span data-ttu-id="64ff6-145">Specifica il pool, come oggetto **PSCloudPool,** che contiene i nodi di calcolo.</span><span class="sxs-lookup"><span data-stu-id="64ff6-145">Specifies the pool, as a **PSCloudPool** object, that contains the compute nodes.</span></span>
<span data-ttu-id="64ff6-146">Per ottenere un **oggetto PSCloudPool,** usare il cmdlet Get-AzBatchPool.</span><span class="sxs-lookup"><span data-stu-id="64ff6-146">To obtain a **PSCloudPool** object, use the Get-AzBatchPool cmdlet.</span></span>

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

### <span data-ttu-id="64ff6-147">-PoolId</span><span class="sxs-lookup"><span data-stu-id="64ff6-147">-PoolId</span></span>
<span data-ttu-id="64ff6-148">Specifica l'ID del pool che contiene i nodi di calcolo.</span><span class="sxs-lookup"><span data-stu-id="64ff6-148">Specifies the ID of the pool that contains the compute nodes.</span></span>

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

### <span data-ttu-id="64ff6-149">-Select</span><span class="sxs-lookup"><span data-stu-id="64ff6-149">-Select</span></span>
<span data-ttu-id="64ff6-150">Specifica una clausola di selezione OData.</span><span class="sxs-lookup"><span data-stu-id="64ff6-150">Specifies an OData select clause.</span></span>
<span data-ttu-id="64ff6-151">Specificare un valore per questo parametro per ottenere proprietà specifiche invece di tutte le proprietà dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="64ff6-151">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="64ff6-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64ff6-152">CommonParameters</span></span>
<span data-ttu-id="64ff6-153">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64ff6-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64ff6-154">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="64ff6-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64ff6-155">INPUT</span><span class="sxs-lookup"><span data-stu-id="64ff6-155">INPUTS</span></span>

### <span data-ttu-id="64ff6-156">System.String</span><span class="sxs-lookup"><span data-stu-id="64ff6-156">System.String</span></span>

### <span data-ttu-id="64ff6-157">Microsoft.Azure.Commands.Batch. Models.PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="64ff6-157">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="64ff6-158">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="64ff6-158">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="64ff6-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="64ff6-159">OUTPUTS</span></span>

### <span data-ttu-id="64ff6-160">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="64ff6-160">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

## <span data-ttu-id="64ff6-161">NOTE</span><span class="sxs-lookup"><span data-stu-id="64ff6-161">NOTES</span></span>

## <span data-ttu-id="64ff6-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="64ff6-162">RELATED LINKS</span></span>

[<span data-ttu-id="64ff6-163">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="64ff6-163">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="64ff6-164">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="64ff6-164">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="64ff6-165">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="64ff6-165">Get-AzBatchNodeFileContent</span></span>](./Get-AzBatchNodeFileContent.md)

[<span data-ttu-id="64ff6-166">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="64ff6-166">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="64ff6-167">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="64ff6-167">Reset-AzBatchComputeNode</span></span>](./Reset-AzBatchComputeNode.md)

[<span data-ttu-id="64ff6-168">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="64ff6-168">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)

[<span data-ttu-id="64ff6-169">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="64ff6-169">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
