---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 029361F0-C4E9-4948-9EBA-BFBD1B029909
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/restart-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Restart-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Restart-AzBatchComputeNode.md
ms.openlocfilehash: 41c6ea8e069e03a759c04f39018e2fa3a4d16834
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199882"
---
# <span data-ttu-id="b6fc3-101">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="b6fc3-101">Restart-AzBatchComputeNode</span></span>

## <span data-ttu-id="b6fc3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b6fc3-102">SYNOPSIS</span></span>
<span data-ttu-id="b6fc3-103">Riavvia il nodo Compute specificato.</span><span class="sxs-lookup"><span data-stu-id="b6fc3-103">Reboots the specified compute node.</span></span>

## <span data-ttu-id="b6fc3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b6fc3-104">SYNTAX</span></span>

### <span data-ttu-id="b6fc3-105">ID (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b6fc3-105">Id (Default)</span></span>
```
Restart-AzBatchComputeNode [-PoolId] <String> [-Id] <String> [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6fc3-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b6fc3-106">InputObject</span></span>
```
Restart-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>] [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6fc3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b6fc3-107">DESCRIPTION</span></span>
<span data-ttu-id="b6fc3-108">Il cmdlet **Restart-AzBatchComputeNode riavvia** il nodo Compute specificato.</span><span class="sxs-lookup"><span data-stu-id="b6fc3-108">The **Restart-AzBatchComputeNode** cmdlet reboots the specified compute node.</span></span>

## <span data-ttu-id="b6fc3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b6fc3-109">EXAMPLES</span></span>

### <span data-ttu-id="b6fc3-110">Esempio 1: riavviare un nodo Compute</span><span class="sxs-lookup"><span data-stu-id="b6fc3-110">Example 1: Restart a compute node</span></span>
```
PS C:\>Restart-AzBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="b6fc3-111">Questo comando Riavvia il nodo COMPUTE con l'ID "TVM-3257026573_2-20150813t200938z" nello pool pool.</span><span class="sxs-lookup"><span data-stu-id="b6fc3-111">This command reboots the compute node with the ID "tvm-3257026573_2-20150813t200938z" in the pool MyPool.</span></span>

### <span data-ttu-id="b6fc3-112">Esempio 2: riavviare ogni nodo di calcolo in un pool</span><span class="sxs-lookup"><span data-stu-id="b6fc3-112">Example 2: Restart every compute node in a pool</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Restart-AzBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="b6fc3-113">Questo comando riavvia tutti i nodi di calcolo nel pool.</span><span class="sxs-lookup"><span data-stu-id="b6fc3-113">This command reboots every compute node in the pool MyPool.</span></span>

## <span data-ttu-id="b6fc3-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b6fc3-114">PARAMETERS</span></span>

### <span data-ttu-id="b6fc3-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b6fc3-115">-BatchContext</span></span>
<span data-ttu-id="b6fc3-116">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="b6fc3-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b6fc3-117">Se si usa il cmdlet Get-AzBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="b6fc3-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b6fc3-118">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="b6fc3-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b6fc3-119">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="b6fc3-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b6fc3-120">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="b6fc3-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b6fc3-121">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="b6fc3-121">-ComputeNode</span></span>
<span data-ttu-id="b6fc3-122">Specifica l'oggetto **PSComputeNode** che rappresenta il nodo Compute da riavviare.</span><span class="sxs-lookup"><span data-stu-id="b6fc3-122">Specifies the **PSComputeNode** object that represents the compute node to reboot.</span></span>

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

### <span data-ttu-id="b6fc3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6fc3-123">-DefaultProfile</span></span>
<span data-ttu-id="b6fc3-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b6fc3-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6fc3-125">-ID</span><span class="sxs-lookup"><span data-stu-id="b6fc3-125">-Id</span></span>
<span data-ttu-id="b6fc3-126">Specifica l'ID del nodo Compute da riavviare.</span><span class="sxs-lookup"><span data-stu-id="b6fc3-126">Specifies the ID of the compute node to reboot.</span></span>

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

### <span data-ttu-id="b6fc3-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="b6fc3-127">-PoolId</span></span>
<span data-ttu-id="b6fc3-128">Specifica l'ID del pool che contiene il nodo COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="b6fc3-128">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="b6fc3-129">-RebootOption</span><span class="sxs-lookup"><span data-stu-id="b6fc3-129">-RebootOption</span></span>
<span data-ttu-id="b6fc3-130">Specifica quando riavviare il nodo e cosa fare con le attività attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="b6fc3-130">Specifies when to reboot the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="b6fc3-131">L'impostazione predefinita è requeue.</span><span class="sxs-lookup"><span data-stu-id="b6fc3-131">The default is Requeue.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.ComputeNodeRebootOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6fc3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6fc3-132">CommonParameters</span></span>
<span data-ttu-id="b6fc3-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6fc3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6fc3-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b6fc3-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6fc3-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b6fc3-135">INPUTS</span></span>

### <span data-ttu-id="b6fc3-136">Microsoft.Azure.Commands.Batch. Models. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="b6fc3-136">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="b6fc3-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b6fc3-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="b6fc3-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b6fc3-138">OUTPUTS</span></span>

### <span data-ttu-id="b6fc3-139">System. void</span><span class="sxs-lookup"><span data-stu-id="b6fc3-139">System.Void</span></span>

## <span data-ttu-id="b6fc3-140">Note</span><span class="sxs-lookup"><span data-stu-id="b6fc3-140">NOTES</span></span>

## <span data-ttu-id="b6fc3-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b6fc3-141">RELATED LINKS</span></span>

[<span data-ttu-id="b6fc3-142">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="b6fc3-142">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="b6fc3-143">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="b6fc3-143">Reset-AzBatchComputeNode</span></span>](./Reset-AzBatchComputeNode.md)

[<span data-ttu-id="b6fc3-144">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="b6fc3-144">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
