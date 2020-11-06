---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 029361F0-C4E9-4948-9EBA-BFBD1B029909
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Restart-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Restart-AzureBatchComputeNode.md
ms.openlocfilehash: eff141494c2b34622f35b687dd1803c449e8b727
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519633"
---
# <span data-ttu-id="51a18-101">Restart-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="51a18-101">Restart-AzureBatchComputeNode</span></span>

## <span data-ttu-id="51a18-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="51a18-102">SYNOPSIS</span></span>
<span data-ttu-id="51a18-103">Riavvia il nodo Compute specificato.</span><span class="sxs-lookup"><span data-stu-id="51a18-103">Reboots the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51a18-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="51a18-104">SYNTAX</span></span>

### <span data-ttu-id="51a18-105">ID (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="51a18-105">Id (Default)</span></span>
```
Restart-AzureBatchComputeNode [-PoolId] <String> [-Id] <String> [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51a18-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="51a18-106">InputObject</span></span>
```
Restart-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>] [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51a18-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="51a18-107">DESCRIPTION</span></span>
<span data-ttu-id="51a18-108">Il cmdlet **Restart-AzureBatchComputeNode riavvia** il nodo Compute specificato.</span><span class="sxs-lookup"><span data-stu-id="51a18-108">The **Restart-AzureBatchComputeNode** cmdlet reboots the specified compute node.</span></span>

## <span data-ttu-id="51a18-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="51a18-109">EXAMPLES</span></span>

### <span data-ttu-id="51a18-110">Esempio 1: riavviare un nodo Compute</span><span class="sxs-lookup"><span data-stu-id="51a18-110">Example 1: Restart a compute node</span></span>
```
PS C:\>Restart-AzureBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="51a18-111">Questo comando Riavvia il nodo COMPUTE con l'ID "TVM-3257026573_2-20150813t200938z" nello pool pool.</span><span class="sxs-lookup"><span data-stu-id="51a18-111">This command reboots the compute node with the ID "tvm-3257026573_2-20150813t200938z" in the pool MyPool.</span></span>

### <span data-ttu-id="51a18-112">Esempio 2: riavviare ogni nodo di calcolo in un pool</span><span class="sxs-lookup"><span data-stu-id="51a18-112">Example 2: Restart every compute node in a pool</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Restart-AzureBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="51a18-113">Questo comando riavvia tutti i nodi di calcolo nel pool.</span><span class="sxs-lookup"><span data-stu-id="51a18-113">This command reboots every compute node in the pool MyPool.</span></span>

## <span data-ttu-id="51a18-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="51a18-114">PARAMETERS</span></span>

### <span data-ttu-id="51a18-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="51a18-115">-BatchContext</span></span>
<span data-ttu-id="51a18-116">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="51a18-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="51a18-117">Per ottenere un oggetto **BatchAccountContext** che contiene i tasti di scelta per l'abbonamento, usare il cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="51a18-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="51a18-118">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="51a18-118">-ComputeNode</span></span>
<span data-ttu-id="51a18-119">Specifica l'oggetto **PSComputeNode** che rappresenta il nodo Compute da riavviare.</span><span class="sxs-lookup"><span data-stu-id="51a18-119">Specifies the **PSComputeNode** object that represents the compute node to reboot.</span></span>

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

### <span data-ttu-id="51a18-120">-ID</span><span class="sxs-lookup"><span data-stu-id="51a18-120">-Id</span></span>
<span data-ttu-id="51a18-121">Specifica l'ID del nodo Compute da riavviare.</span><span class="sxs-lookup"><span data-stu-id="51a18-121">Specifies the ID of the compute node to reboot.</span></span>

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

### <span data-ttu-id="51a18-122">-PoolId</span><span class="sxs-lookup"><span data-stu-id="51a18-122">-PoolId</span></span>
<span data-ttu-id="51a18-123">Specifica l'ID del pool che contiene il nodo COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="51a18-123">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="51a18-124">-RebootOption</span><span class="sxs-lookup"><span data-stu-id="51a18-124">-RebootOption</span></span>
<span data-ttu-id="51a18-125">Specifica quando riavviare il nodo e cosa fare con le attività attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="51a18-125">Specifies when to reboot the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="51a18-126">L'impostazione predefinita è requeue.</span><span class="sxs-lookup"><span data-stu-id="51a18-126">The default is Requeue.</span></span>

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

### <span data-ttu-id="51a18-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51a18-127">-DefaultProfile</span></span>
<span data-ttu-id="51a18-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="51a18-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51a18-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51a18-129">CommonParameters</span></span>
<span data-ttu-id="51a18-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51a18-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51a18-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51a18-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51a18-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="51a18-132">INPUTS</span></span>

### <span data-ttu-id="51a18-133">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="51a18-133">BatchAccountContext</span></span>
<span data-ttu-id="51a18-134">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="51a18-134">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="51a18-135">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="51a18-135">PSComputeNode</span></span>
<span data-ttu-id="51a18-136">Il parametro ' ComputeNode ' accetta il valore di tipo ' PSComputeNode ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="51a18-136">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="51a18-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="51a18-137">OUTPUTS</span></span>

## <span data-ttu-id="51a18-138">Note</span><span class="sxs-lookup"><span data-stu-id="51a18-138">NOTES</span></span>

## <span data-ttu-id="51a18-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="51a18-139">RELATED LINKS</span></span>

[<span data-ttu-id="51a18-140">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="51a18-140">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="51a18-141">Reset-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="51a18-141">Reset-AzureBatchComputeNode</span></span>](./Reset-AzureBatchComputeNode.md)

[<span data-ttu-id="51a18-142">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="51a18-142">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


