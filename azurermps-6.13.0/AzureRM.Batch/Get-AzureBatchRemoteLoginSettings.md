---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 07811B64-6A77-452C-B148-DE8C13E73DEF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchremoteloginsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteLoginSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteLoginSettings.md
ms.openlocfilehash: d25e9aeb75c58bcce560043d87f5ce9eef065b97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519300"
---
# <span data-ttu-id="adde5-101">Get-AzureBatchRemoteLoginSettings</span><span class="sxs-lookup"><span data-stu-id="adde5-101">Get-AzureBatchRemoteLoginSettings</span></span>

## <span data-ttu-id="adde5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="adde5-102">SYNOPSIS</span></span>
<span data-ttu-id="adde5-103">Ottiene le impostazioni di accesso remoto per un nodo COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="adde5-103">Gets remote logon settings for a compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="adde5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="adde5-104">SYNTAX</span></span>

### <span data-ttu-id="adde5-105">ID (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="adde5-105">Id (Default)</span></span>
```
Get-AzureBatchRemoteLoginSettings [-PoolId] <String> [-ComputeNodeId] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="adde5-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="adde5-106">InputObject</span></span>
```
Get-AzureBatchRemoteLoginSettings [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="adde5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="adde5-107">DESCRIPTION</span></span>
<span data-ttu-id="adde5-108">Il cmdlet **Get-AzureBatchRemoteLoginSettings** ottiene le impostazioni di accesso remoto per un nodo COMPUTE in un pool di macchine virtuali basato sull'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="adde5-108">The **Get-AzureBatchRemoteLoginSettings** cmdlet gets remote logon settings for a compute node in a virtual machines infrastructure-based pool.</span></span>

## <span data-ttu-id="adde5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="adde5-109">EXAMPLES</span></span>

### <span data-ttu-id="adde5-110">Esempio 1: ottenere le impostazioni di accesso remoto per tutti i nodi di un pool</span><span class="sxs-lookup"><span data-stu-id="adde5-110">Example 1: Get remote logon settings for all nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzureBatchComputeNode -PoolId "ContosoPool" -BatchContext $Context | Get-AzureBatchRemoteLoginSettings -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50002
10.214.75.221   50001
10.214.75.221   50000
```

<span data-ttu-id="adde5-111">Il primo comando ottiene un contesto dell'account batch che contiene i tasti di scelta per l'abbonamento utilizzando **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="adde5-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="adde5-112">Il comando Archivia il contesto nella variabile $Context da usare nel comando successivo.</span><span class="sxs-lookup"><span data-stu-id="adde5-112">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="adde5-113">Il secondo comando ottiene ogni nodo Compute nel pool che contiene l'ID ContosoPool utilizzando **Get-AzureBatchComputeNode**.</span><span class="sxs-lookup"><span data-stu-id="adde5-113">The second command gets each compute node in the pool that has the ID ContosoPool by using **Get-AzureBatchComputeNode**.</span></span>
<span data-ttu-id="adde5-114">Il comando passa ogni nodo del computer al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="adde5-114">The command passes each computer node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="adde5-115">Il comando ottiene le impostazioni di accesso remoto per ogni nodo COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="adde5-115">The command gets the remote logon settings for each compute node.</span></span>

### <span data-ttu-id="adde5-116">Esempio 2: ottenere le impostazioni di accesso remoto per un nodo</span><span class="sxs-lookup"><span data-stu-id="adde5-116">Example 2: Get remote logon settings for a node</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzureBatchRemoteLoginSettings -PoolId "ContosoPool" -ComputeNodeId "tvm-1900272697_1-20150330t205553z" -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50000
```

<span data-ttu-id="adde5-117">Il primo comando ottiene un contesto dell'account batch che contiene i tasti di scelta per l'abbonamento e lo archivia nella variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="adde5-117">The first command gets a batch account context that contains access keys for your subscription, and then stores it in the $Context variable.</span></span>
<span data-ttu-id="adde5-118">Il secondo comando consente di ottenere le impostazioni di accesso remoto per il nodo COMPUTE con l'ID specificato nel pool che contiene l'ID ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="adde5-118">The second command gets the remote logon settings for the compute node that has the specified ID in the pool that has the ID ContosoPool.</span></span>

## <span data-ttu-id="adde5-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="adde5-119">PARAMETERS</span></span>

### <span data-ttu-id="adde5-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="adde5-120">-BatchContext</span></span>
<span data-ttu-id="adde5-121">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="adde5-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="adde5-122">Per ottenere un **BatchAccountContext** che contiene i tasti di scelta per l'abbonamento, usare il cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="adde5-122">To obtain a **BatchAccountContext** that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="adde5-123">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="adde5-123">-ComputeNode</span></span>
<span data-ttu-id="adde5-124">Specifica un nodo COMPUTE, come oggetto **PSComputeNode** , per cui questo cmdlet ottiene le impostazioni di accesso remoto.</span><span class="sxs-lookup"><span data-stu-id="adde5-124">Specifies a compute node, as a **PSComputeNode** object, for which this cmdlet gets remote logon settings.</span></span>
<span data-ttu-id="adde5-125">Per ottenere un oggetto compute node, usa il cmdlet Get-AzureBatchComputeNode.</span><span class="sxs-lookup"><span data-stu-id="adde5-125">To obtain a compute node object, use the Get-AzureBatchComputeNode cmdlet.</span></span>

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

### <span data-ttu-id="adde5-126">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="adde5-126">-ComputeNodeId</span></span>
<span data-ttu-id="adde5-127">Specifica l'ID del nodo COMPUTE per cui ottenere le impostazioni di accesso remoto.</span><span class="sxs-lookup"><span data-stu-id="adde5-127">Specifies the ID of the compute node for which to get the remote logon settings.</span></span>
<span data-ttu-id="adde5-128">per cui questo cmdlet ottiene le impostazioni di accesso remoto.</span><span class="sxs-lookup"><span data-stu-id="adde5-128">for which this cmdlet gets remote logon settings.</span></span>

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

### <span data-ttu-id="adde5-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adde5-129">-DefaultProfile</span></span>
<span data-ttu-id="adde5-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="adde5-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="adde5-131">-PoolId</span><span class="sxs-lookup"><span data-stu-id="adde5-131">-PoolId</span></span>
<span data-ttu-id="adde5-132">Specifica l'ID del pool che contiene la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="adde5-132">Specifies the ID of the pool that contains the virtual machine.</span></span>

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

### <span data-ttu-id="adde5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adde5-133">CommonParameters</span></span>
<span data-ttu-id="adde5-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adde5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adde5-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adde5-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adde5-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="adde5-136">INPUTS</span></span>

### <span data-ttu-id="adde5-137">Microsoft.Azure.Commands.Batch. Models. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="adde5-137">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>
<span data-ttu-id="adde5-138">Parametri: ComputeNode (ByValue)</span><span class="sxs-lookup"><span data-stu-id="adde5-138">Parameters: ComputeNode (ByValue)</span></span>

### <span data-ttu-id="adde5-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="adde5-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="adde5-140">Parametri: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="adde5-140">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="adde5-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="adde5-141">OUTPUTS</span></span>

### <span data-ttu-id="adde5-142">Microsoft.Azure.Commands.Batch. Models. PSRemoteLoginSettings</span><span class="sxs-lookup"><span data-stu-id="adde5-142">Microsoft.Azure.Commands.Batch.Models.PSRemoteLoginSettings</span></span>

## <span data-ttu-id="adde5-143">Note</span><span class="sxs-lookup"><span data-stu-id="adde5-143">NOTES</span></span>

## <span data-ttu-id="adde5-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="adde5-144">RELATED LINKS</span></span>

[<span data-ttu-id="adde5-145">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="adde5-145">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="adde5-146">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="adde5-146">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="adde5-147">Get-AzureBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="adde5-147">Get-AzureBatchRemoteDesktopProtocolFile</span></span>](./Get-AzureBatchRemoteDesktopProtocolFile.md)

[<span data-ttu-id="adde5-148">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="adde5-148">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


