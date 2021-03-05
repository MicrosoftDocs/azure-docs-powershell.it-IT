---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 029361F0-C4E9-4948-9EBA-BFBD1B029909
online version: https://docs.microsoft.com/powershell/module/az.batch/restart-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Restart-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Restart-AzBatchComputeNode.md
ms.openlocfilehash: daf89fec73ed18cf5b67c4100556d490795708d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985345"
---
# <span data-ttu-id="4d967-101">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="4d967-101">Restart-AzBatchComputeNode</span></span>

## <span data-ttu-id="4d967-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d967-102">SYNOPSIS</span></span>
<span data-ttu-id="4d967-103">Riavvia il nodo di calcolo specificato.</span><span class="sxs-lookup"><span data-stu-id="4d967-103">Reboots the specified compute node.</span></span>

## <span data-ttu-id="4d967-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4d967-104">SYNTAX</span></span>

### <span data-ttu-id="4d967-105">ID (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4d967-105">Id (Default)</span></span>
```
Restart-AzBatchComputeNode [-PoolId] <String> [-Id] <String> [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d967-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="4d967-106">InputObject</span></span>
```
Restart-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>] [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d967-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4d967-107">DESCRIPTION</span></span>
<span data-ttu-id="4d967-108">Il cmdlet **Restart-AzBatchComputeNode** riavvia il nodo di calcolo specificato.</span><span class="sxs-lookup"><span data-stu-id="4d967-108">The **Restart-AzBatchComputeNode** cmdlet reboots the specified compute node.</span></span>

## <span data-ttu-id="4d967-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4d967-109">EXAMPLES</span></span>

### <span data-ttu-id="4d967-110">Esempio 1: Riavviare un nodo di calcolo</span><span class="sxs-lookup"><span data-stu-id="4d967-110">Example 1: Restart a compute node</span></span>
```
PS C:\>Restart-AzBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="4d967-111">Questo comando riavvia il nodo di calcolo con l'ID "tvm-3257026573_2-20150813t200938z" nel pool MyPool.</span><span class="sxs-lookup"><span data-stu-id="4d967-111">This command reboots the compute node with the ID "tvm-3257026573_2-20150813t200938z" in the pool MyPool.</span></span>

### <span data-ttu-id="4d967-112">Esempio 2: Riavviare ogni nodo di calcolo in un pool</span><span class="sxs-lookup"><span data-stu-id="4d967-112">Example 2: Restart every compute node in a pool</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Restart-AzBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="4d967-113">Questo comando riavvia ogni nodo di calcolo nel pool MyPool.</span><span class="sxs-lookup"><span data-stu-id="4d967-113">This command reboots every compute node in the pool MyPool.</span></span>

## <span data-ttu-id="4d967-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d967-114">PARAMETERS</span></span>

### <span data-ttu-id="4d967-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="4d967-115">-BatchContext</span></span>
<span data-ttu-id="4d967-116">Specifica **l'istanza BatchAccountContext** che questo cmdlet usa per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="4d967-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="4d967-117">Se si usa il cmdlet Get-AzBatchAccount per ottenere BatchAccountContext, verrà usata l'autenticazione di Azure Active Directory quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="4d967-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="4d967-118">Per usare invece l'autenticazione della chiave condivisa, usare il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.</span><span class="sxs-lookup"><span data-stu-id="4d967-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="4d967-119">Quando si usa l'autenticazione con chiave condivisa, per impostazione predefinita viene usata la chiave di accesso primario.</span><span class="sxs-lookup"><span data-stu-id="4d967-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="4d967-120">Per modificare la chiave da usare, impostare la proprietà BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="4d967-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="4d967-121">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="4d967-121">-ComputeNode</span></span>
<span data-ttu-id="4d967-122">Specifica **l'oggetto PSComputeNode** che rappresenta il nodo di calcolo da riavviare.</span><span class="sxs-lookup"><span data-stu-id="4d967-122">Specifies the **PSComputeNode** object that represents the compute node to reboot.</span></span>

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

### <span data-ttu-id="4d967-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d967-123">-DefaultProfile</span></span>
<span data-ttu-id="4d967-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4d967-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d967-125">-Id</span><span class="sxs-lookup"><span data-stu-id="4d967-125">-Id</span></span>
<span data-ttu-id="4d967-126">Specifica l'ID del nodo di calcolo da riavviare.</span><span class="sxs-lookup"><span data-stu-id="4d967-126">Specifies the ID of the compute node to reboot.</span></span>

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

### <span data-ttu-id="4d967-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="4d967-127">-PoolId</span></span>
<span data-ttu-id="4d967-128">Specifica l'ID del pool che contiene il nodo di calcolo.</span><span class="sxs-lookup"><span data-stu-id="4d967-128">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="4d967-129">-RebootOption</span><span class="sxs-lookup"><span data-stu-id="4d967-129">-RebootOption</span></span>
<span data-ttu-id="4d967-130">Specifica quando riavviare il nodo e cosa fare con le attività in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="4d967-130">Specifies when to reboot the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="4d967-131">L'impostazione predefinita è La coda.</span><span class="sxs-lookup"><span data-stu-id="4d967-131">The default is Requeue.</span></span>

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

### <span data-ttu-id="4d967-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d967-132">CommonParameters</span></span>
<span data-ttu-id="4d967-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d967-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d967-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4d967-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d967-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="4d967-135">INPUTS</span></span>

### <span data-ttu-id="4d967-136">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="4d967-136">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="4d967-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4d967-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="4d967-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4d967-138">OUTPUTS</span></span>

### <span data-ttu-id="4d967-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="4d967-139">System.Void</span></span>

## <span data-ttu-id="4d967-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="4d967-140">NOTES</span></span>

## <span data-ttu-id="4d967-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4d967-141">RELATED LINKS</span></span>

[<span data-ttu-id="4d967-142">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="4d967-142">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="4d967-143">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="4d967-143">Reset-AzBatchComputeNode</span></span>](./Reset-AzBatchComputeNode.md)

[<span data-ttu-id="4d967-144">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="4d967-144">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
