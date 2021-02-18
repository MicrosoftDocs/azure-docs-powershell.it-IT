---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A202537B-D292-4822-A0B9-27A6A20621D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/reset-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Reset-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Reset-AzBatchComputeNode.md
ms.openlocfilehash: ff8c758b5e384fbab8f690030eb8a7fbe35c79f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200983"
---
# <span data-ttu-id="b9e2f-101">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="b9e2f-101">Reset-AzBatchComputeNode</span></span>

## <span data-ttu-id="b9e2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9e2f-102">SYNOPSIS</span></span>
<span data-ttu-id="b9e2f-103">Reinstalla il sistema operativo nel nodo di elaborazione specificato.</span><span class="sxs-lookup"><span data-stu-id="b9e2f-103">Reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="b9e2f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b9e2f-104">SYNTAX</span></span>

### <span data-ttu-id="b9e2f-105">ID (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b9e2f-105">Id (Default)</span></span>
```
Reset-AzBatchComputeNode [-PoolId] <String> [-Id] <String> [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9e2f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b9e2f-106">InputObject</span></span>
```
Reset-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>] [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9e2f-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b9e2f-107">DESCRIPTION</span></span>
<span data-ttu-id="b9e2f-108">Il cmdlet **Reset-AzBatchComputeNode** reinstalla il sistema operativo nel nodo di elaborazione specificato.</span><span class="sxs-lookup"><span data-stu-id="b9e2f-108">The **Reset-AzBatchComputeNode** cmdlet reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="b9e2f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b9e2f-109">EXAMPLES</span></span>

### <span data-ttu-id="b9e2f-110">Esempio 1: Ricreare l'immagine di un nodo</span><span class="sxs-lookup"><span data-stu-id="b9e2f-110">Example 1: Reimage a node</span></span>
```
PS C:\>Reset-AzBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="b9e2f-111">Questo comando mostra nuovamente il nodo di calcolo con ID "tvm-3257026573_2-20150813t200938z" nel pool denominato MyPool.</span><span class="sxs-lookup"><span data-stu-id="b9e2f-111">This command reimages the compute node with ID "tvm-3257026573_2-20150813t200938z" in the pool named MyPool.</span></span>
<span data-ttu-id="b9e2f-112">Usare il cmdlet Get-AzBatchAccountKey per assegnare un contesto alla $Context variabile.</span><span class="sxs-lookup"><span data-stu-id="b9e2f-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="b9e2f-113">Esempio 2: Visualizzare nuovamente tutti i nodi in un pool</span><span class="sxs-lookup"><span data-stu-id="b9e2f-113">Example 2: Reimage all nodes in a pool</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Reset-AzBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="b9e2f-114">Questo comando mostra di nuovo ogni nodo di calcolo nel pool denominato MyPool.</span><span class="sxs-lookup"><span data-stu-id="b9e2f-114">This command reimages every compute node in the pool named MyPool.</span></span>

## <span data-ttu-id="b9e2f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9e2f-115">PARAMETERS</span></span>

### <span data-ttu-id="b9e2f-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b9e2f-116">-BatchContext</span></span>
<span data-ttu-id="b9e2f-117">Specifica **l'istanza BatchAccountContext** che questo cmdlet usa per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="b9e2f-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b9e2f-118">Se si usa il cmdlet Get-AzBatchAccount per ottenere BatchAccountContext, verrà usata l'autenticazione di Azure Active Directory quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="b9e2f-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b9e2f-119">Per usare invece l'autenticazione della chiave condivisa, usare il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.</span><span class="sxs-lookup"><span data-stu-id="b9e2f-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b9e2f-120">Quando si usa l'autenticazione con chiave condivisa, per impostazione predefinita viene usata la chiave di accesso primario.</span><span class="sxs-lookup"><span data-stu-id="b9e2f-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b9e2f-121">Per modificare la chiave da usare, impostare la proprietà BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="b9e2f-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b9e2f-122">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="b9e2f-122">-ComputeNode</span></span>
<span data-ttu-id="b9e2f-123">Specifica **l'oggetto PSComputeNode** che rappresenta il nodo di calcolo per la nuova immagine.</span><span class="sxs-lookup"><span data-stu-id="b9e2f-123">Specifies the **PSComputeNode** object that represents the compute node to reimage.</span></span>

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

### <span data-ttu-id="b9e2f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9e2f-124">-DefaultProfile</span></span>
<span data-ttu-id="b9e2f-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b9e2f-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9e2f-126">-Id</span><span class="sxs-lookup"><span data-stu-id="b9e2f-126">-Id</span></span>
<span data-ttu-id="b9e2f-127">Specifica l'ID del nodo di calcolo di cui visualizzare di nuovo l'immagine.</span><span class="sxs-lookup"><span data-stu-id="b9e2f-127">Specifies the ID of the compute node to reimage.</span></span>

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

### <span data-ttu-id="b9e2f-128">-PoolId</span><span class="sxs-lookup"><span data-stu-id="b9e2f-128">-PoolId</span></span>
<span data-ttu-id="b9e2f-129">Specifica l'ID del pool che contiene il nodo di calcolo.</span><span class="sxs-lookup"><span data-stu-id="b9e2f-129">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="b9e2f-130">-ReimageOption</span><span class="sxs-lookup"><span data-stu-id="b9e2f-130">-ReimageOption</span></span>
<span data-ttu-id="b9e2f-131">Specifica quando visualizzare nuovamente il nodo e cosa fare con le attività attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="b9e2f-131">Specifies when to reimage the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="b9e2f-132">L'impostazione predefinita è La coda.</span><span class="sxs-lookup"><span data-stu-id="b9e2f-132">The default is Requeue.</span></span>

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

### <span data-ttu-id="b9e2f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9e2f-133">CommonParameters</span></span>
<span data-ttu-id="b9e2f-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9e2f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9e2f-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b9e2f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9e2f-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="b9e2f-136">INPUTS</span></span>

### <span data-ttu-id="b9e2f-137">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="b9e2f-137">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="b9e2f-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b9e2f-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="b9e2f-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b9e2f-139">OUTPUTS</span></span>

### <span data-ttu-id="b9e2f-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="b9e2f-140">System.Void</span></span>

## <span data-ttu-id="b9e2f-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="b9e2f-141">NOTES</span></span>

## <span data-ttu-id="b9e2f-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b9e2f-142">RELATED LINKS</span></span>

[<span data-ttu-id="b9e2f-143">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="b9e2f-143">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="b9e2f-144">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="b9e2f-144">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)

[<span data-ttu-id="b9e2f-145">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="b9e2f-145">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
