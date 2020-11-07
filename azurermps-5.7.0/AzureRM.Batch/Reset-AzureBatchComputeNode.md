---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A202537B-D292-4822-A0B9-27A6A20621D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/reset-azurebatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Reset-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Reset-AzureBatchComputeNode.md
ms.openlocfilehash: 8e1fd78c51a6a41f1f455fc3672a0c340309f76c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688184"
---
# <span data-ttu-id="7a3cf-101">Reset-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="7a3cf-101">Reset-AzureBatchComputeNode</span></span>

## <span data-ttu-id="7a3cf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7a3cf-102">SYNOPSIS</span></span>
<span data-ttu-id="7a3cf-103">Reinstalla il sistema operativo nel nodo Compute specificato.</span><span class="sxs-lookup"><span data-stu-id="7a3cf-103">Reinstalls the operating system on the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a3cf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7a3cf-104">SYNTAX</span></span>

### <span data-ttu-id="7a3cf-105">ID (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7a3cf-105">Id (Default)</span></span>
```
Reset-AzureBatchComputeNode [-PoolId] <String> [-Id] <String> [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a3cf-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="7a3cf-106">InputObject</span></span>
```
Reset-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>] [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a3cf-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a3cf-107">DESCRIPTION</span></span>
<span data-ttu-id="7a3cf-108">Il cmdlet **Reset-AzureBatchComputeNode** reinstalla il sistema operativo nel nodo Compute specificato.</span><span class="sxs-lookup"><span data-stu-id="7a3cf-108">The **Reset-AzureBatchComputeNode** cmdlet reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="7a3cf-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7a3cf-109">EXAMPLES</span></span>

### <span data-ttu-id="7a3cf-110">Esempio 1: riimmagine di un nodo</span><span class="sxs-lookup"><span data-stu-id="7a3cf-110">Example 1: Reimage a node</span></span>
```
PS C:\>Reset-AzureBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="7a3cf-111">Questo comando riimmaginerà il nodo COMPUTE con ID "TVM-3257026573_2-20150813t200938z" nel pool denominato pool.</span><span class="sxs-lookup"><span data-stu-id="7a3cf-111">This command reimages the compute node with ID "tvm-3257026573_2-20150813t200938z" in the pool named MyPool.</span></span>
<span data-ttu-id="7a3cf-112">Usa il cmdlet Get-AzureRmBatchAccountKeys per assegnare un contesto alla variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="7a3cf-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="7a3cf-113">Esempio 2: riimmagine di tutti i nodi in un pool</span><span class="sxs-lookup"><span data-stu-id="7a3cf-113">Example 2: Reimage all nodes in a pool</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Reset-AzureBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="7a3cf-114">Questo comando riimmaginerà tutti i nodi di calcolo nel pool denominato pool.</span><span class="sxs-lookup"><span data-stu-id="7a3cf-114">This command reimages every compute node in the pool named MyPool.</span></span>

## <span data-ttu-id="7a3cf-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7a3cf-115">PARAMETERS</span></span>

### <span data-ttu-id="7a3cf-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="7a3cf-116">-BatchContext</span></span>
<span data-ttu-id="7a3cf-117">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="7a3cf-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="7a3cf-118">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="7a3cf-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="7a3cf-119">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="7a3cf-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="7a3cf-120">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="7a3cf-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="7a3cf-121">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="7a3cf-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="7a3cf-122">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="7a3cf-122">-ComputeNode</span></span>
<span data-ttu-id="7a3cf-123">Specifica l'oggetto **PSComputeNode** che rappresenta il nodo COMPUTE per la riimmagine.</span><span class="sxs-lookup"><span data-stu-id="7a3cf-123">Specifies the **PSComputeNode** object that represents the compute node to reimage.</span></span>

```yaml
Type: PSComputeNode
Parameter Sets: InputObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a3cf-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a3cf-124">-DefaultProfile</span></span>
<span data-ttu-id="7a3cf-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7a3cf-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a3cf-126">-ID</span><span class="sxs-lookup"><span data-stu-id="7a3cf-126">-Id</span></span>
<span data-ttu-id="7a3cf-127">Specifica l'ID del nodo COMPUTE per la riimmagine.</span><span class="sxs-lookup"><span data-stu-id="7a3cf-127">Specifies the ID of the compute node to reimage.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a3cf-128">-PoolId</span><span class="sxs-lookup"><span data-stu-id="7a3cf-128">-PoolId</span></span>
<span data-ttu-id="7a3cf-129">Specifica l'ID del pool che contiene il nodo COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="7a3cf-129">Specifies the ID of the pool that contains the compute node.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a3cf-130">-ReimageOption</span><span class="sxs-lookup"><span data-stu-id="7a3cf-130">-ReimageOption</span></span>
<span data-ttu-id="7a3cf-131">Specifica quando riapplicare il nodo e cosa fare con le attività attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="7a3cf-131">Specifies when to reimage the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="7a3cf-132">L'impostazione predefinita è requeue.</span><span class="sxs-lookup"><span data-stu-id="7a3cf-132">The default is Requeue.</span></span>

```yaml
Type: ComputeNodeReimageOption
Parameter Sets: (All)
Aliases: 
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a3cf-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a3cf-133">CommonParameters</span></span>
<span data-ttu-id="7a3cf-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a3cf-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a3cf-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a3cf-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a3cf-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7a3cf-136">INPUTS</span></span>

### <span data-ttu-id="7a3cf-137">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="7a3cf-137">BatchAccountContext</span></span>
<span data-ttu-id="7a3cf-138">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="7a3cf-138">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="7a3cf-139">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="7a3cf-139">PSComputeNode</span></span>
<span data-ttu-id="7a3cf-140">Il parametro ' ComputeNode ' accetta il valore di tipo ' PSComputeNode ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="7a3cf-140">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="7a3cf-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7a3cf-141">OUTPUTS</span></span>

## <span data-ttu-id="7a3cf-142">Note</span><span class="sxs-lookup"><span data-stu-id="7a3cf-142">NOTES</span></span>

## <span data-ttu-id="7a3cf-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7a3cf-143">RELATED LINKS</span></span>

[<span data-ttu-id="7a3cf-144">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="7a3cf-144">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="7a3cf-145">Riavviare-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="7a3cf-145">Restart-AzureBatchComputeNode</span></span>](./Restart-AzureBatchComputeNode.md)

[<span data-ttu-id="7a3cf-146">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="7a3cf-146">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


