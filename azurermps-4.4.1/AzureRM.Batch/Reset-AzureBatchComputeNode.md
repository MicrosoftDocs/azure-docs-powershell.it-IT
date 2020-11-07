---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A202537B-D292-4822-A0B9-27A6A20621D4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Reset-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Reset-AzureBatchComputeNode.md
ms.openlocfilehash: b90a70bb6b4a8104597056715c75f5699db5a24e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686344"
---
# <span data-ttu-id="fe943-101">Reset-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="fe943-101">Reset-AzureBatchComputeNode</span></span>

## <span data-ttu-id="fe943-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fe943-102">SYNOPSIS</span></span>
<span data-ttu-id="fe943-103">Reinstalla il sistema operativo nel nodo Compute specificato.</span><span class="sxs-lookup"><span data-stu-id="fe943-103">Reinstalls the operating system on the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe943-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fe943-104">SYNTAX</span></span>

### <span data-ttu-id="fe943-105">ID (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fe943-105">Id (Default)</span></span>
```
Reset-AzureBatchComputeNode [-PoolId] <String> [-Id] <String> [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe943-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="fe943-106">InputObject</span></span>
```
Reset-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>] [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe943-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fe943-107">DESCRIPTION</span></span>
<span data-ttu-id="fe943-108">Il cmdlet **Reset-AzureBatchComputeNode** reinstalla il sistema operativo nel nodo Compute specificato.</span><span class="sxs-lookup"><span data-stu-id="fe943-108">The **Reset-AzureBatchComputeNode** cmdlet reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="fe943-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fe943-109">EXAMPLES</span></span>

### <span data-ttu-id="fe943-110">Esempio 1: riimmagine di un nodo</span><span class="sxs-lookup"><span data-stu-id="fe943-110">Example 1: Reimage a node</span></span>
```
PS C:\>Reset-AzureBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="fe943-111">Questo comando riimmaginerà il nodo COMPUTE con ID "TVM-3257026573_2-20150813t200938z" nel pool denominato pool.</span><span class="sxs-lookup"><span data-stu-id="fe943-111">This command reimages the compute node with ID "tvm-3257026573_2-20150813t200938z" in the pool named MyPool.</span></span>
<span data-ttu-id="fe943-112">Usa il cmdlet Get-AzureRmBatchAccountKeys per assegnare un contesto alla variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="fe943-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="fe943-113">Esempio 2: riimmagine di tutti i nodi in un pool</span><span class="sxs-lookup"><span data-stu-id="fe943-113">Example 2: Reimage all nodes in a pool</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Reset-AzureBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="fe943-114">Questo comando riimmaginerà tutti i nodi di calcolo nel pool denominato pool.</span><span class="sxs-lookup"><span data-stu-id="fe943-114">This command reimages every compute node in the pool named MyPool.</span></span>

## <span data-ttu-id="fe943-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fe943-115">PARAMETERS</span></span>

### <span data-ttu-id="fe943-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="fe943-116">-BatchContext</span></span>
<span data-ttu-id="fe943-117">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="fe943-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="fe943-118">Per ottenere un oggetto **BatchAccountContext** che contiene i tasti di scelta per l'abbonamento, usare il cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="fe943-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="fe943-119">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="fe943-119">-ComputeNode</span></span>
<span data-ttu-id="fe943-120">Specifica l'oggetto **PSComputeNode** che rappresenta il nodo COMPUTE per la riimmagine.</span><span class="sxs-lookup"><span data-stu-id="fe943-120">Specifies the **PSComputeNode** object that represents the compute node to reimage.</span></span>

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

### <span data-ttu-id="fe943-121">-ID</span><span class="sxs-lookup"><span data-stu-id="fe943-121">-Id</span></span>
<span data-ttu-id="fe943-122">Specifica l'ID del nodo COMPUTE per la riimmagine.</span><span class="sxs-lookup"><span data-stu-id="fe943-122">Specifies the ID of the compute node to reimage.</span></span>

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

### <span data-ttu-id="fe943-123">-PoolId</span><span class="sxs-lookup"><span data-stu-id="fe943-123">-PoolId</span></span>
<span data-ttu-id="fe943-124">Specifica l'ID del pool che contiene il nodo COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="fe943-124">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="fe943-125">-ReimageOption</span><span class="sxs-lookup"><span data-stu-id="fe943-125">-ReimageOption</span></span>
<span data-ttu-id="fe943-126">Specifica quando riapplicare il nodo e cosa fare con le attività attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="fe943-126">Specifies when to reimage the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="fe943-127">L'impostazione predefinita è requeue.</span><span class="sxs-lookup"><span data-stu-id="fe943-127">The default is Requeue.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.ComputeNodeReimageOption]
Parameter Sets: (All)
Aliases: 
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe943-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe943-128">-DefaultProfile</span></span>
<span data-ttu-id="fe943-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fe943-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe943-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe943-130">CommonParameters</span></span>
<span data-ttu-id="fe943-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe943-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe943-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe943-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe943-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fe943-133">INPUTS</span></span>

### <span data-ttu-id="fe943-134">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="fe943-134">BatchAccountContext</span></span>
<span data-ttu-id="fe943-135">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="fe943-135">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="fe943-136">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="fe943-136">PSComputeNode</span></span>
<span data-ttu-id="fe943-137">Il parametro ' ComputeNode ' accetta il valore di tipo ' PSComputeNode ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="fe943-137">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="fe943-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fe943-138">OUTPUTS</span></span>

## <span data-ttu-id="fe943-139">Note</span><span class="sxs-lookup"><span data-stu-id="fe943-139">NOTES</span></span>

## <span data-ttu-id="fe943-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fe943-140">RELATED LINKS</span></span>

[<span data-ttu-id="fe943-141">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="fe943-141">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="fe943-142">Riavviare-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="fe943-142">Restart-AzureBatchComputeNode</span></span>](./Restart-AzureBatchComputeNode.md)

[<span data-ttu-id="fe943-143">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="fe943-143">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


