---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 07811B64-6A77-452C-B148-DE8C13E73DEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchremoteloginsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
ms.openlocfilehash: 0e2360e6c4d0ba7d993f1f1aa21feb1b44115e6b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205250"
---
# <span data-ttu-id="d8e1d-101">Get-AzBatchRemoteLoginSetting</span><span class="sxs-lookup"><span data-stu-id="d8e1d-101">Get-AzBatchRemoteLoginSetting</span></span>

## <span data-ttu-id="d8e1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8e1d-102">SYNOPSIS</span></span>
<span data-ttu-id="d8e1d-103">Recupera le impostazioni di accesso remoto per un nodo di calcolo.</span><span class="sxs-lookup"><span data-stu-id="d8e1d-103">Gets remote logon settings for a compute node.</span></span>

## <span data-ttu-id="d8e1d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d8e1d-104">SYNTAX</span></span>

### <span data-ttu-id="d8e1d-105">ID (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d8e1d-105">Id (Default)</span></span>
```
Get-AzBatchRemoteLoginSetting [-PoolId] <String> [-ComputeNodeId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8e1d-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d8e1d-106">InputObject</span></span>
```
Get-AzBatchRemoteLoginSetting [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8e1d-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d8e1d-107">DESCRIPTION</span></span>
<span data-ttu-id="d8e1d-108">Il cmdlet **Get-AzBatchRemoteLoginSetting** ottiene le impostazioni di accesso remoto per un nodo di elaborazione in un pool basato sull'infrastruttura di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="d8e1d-108">The **Get-AzBatchRemoteLoginSetting** cmdlet gets remote logon settings for a compute node in a virtual machines infrastructure-based pool.</span></span>

## <span data-ttu-id="d8e1d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d8e1d-109">EXAMPLES</span></span>

### <span data-ttu-id="d8e1d-110">Esempio 1: Ottenere le impostazioni di accesso remoto per tutti i nodi in un pool</span><span class="sxs-lookup"><span data-stu-id="d8e1d-110">Example 1: Get remote logon settings for all nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchComputeNode -PoolId "ContosoPool" -BatchContext $Context | Get-AzBatchRemoteLoginSetting -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50002
10.214.75.221   50001
10.214.75.221   50000
```

<span data-ttu-id="d8e1d-111">Il primo comando ottiene un contesto di account batch che contiene le chiavi di accesso per l'abbonamento usando **Get-AzBatchAccountKey.**</span><span class="sxs-lookup"><span data-stu-id="d8e1d-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="d8e1d-112">Il comando archivia il contesto nella $Context variabile da usare nel comando successivo.</span><span class="sxs-lookup"><span data-stu-id="d8e1d-112">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="d8e1d-113">Il secondo comando recupera ogni nodo di calcolo nel pool che ha l'ID ContosoPool usando **Get-AzBatchComputeNode.**</span><span class="sxs-lookup"><span data-stu-id="d8e1d-113">The second command gets each compute node in the pool that has the ID ContosoPool by using **Get-AzBatchComputeNode**.</span></span>
<span data-ttu-id="d8e1d-114">Il comando passa ogni nodo di computer al cmdlet corrente usando l'operatore della pipeline.</span><span class="sxs-lookup"><span data-stu-id="d8e1d-114">The command passes each computer node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d8e1d-115">Il comando ottiene le impostazioni di accesso remoto per ogni nodo di calcolo.</span><span class="sxs-lookup"><span data-stu-id="d8e1d-115">The command gets the remote logon settings for each compute node.</span></span>

### <span data-ttu-id="d8e1d-116">Esempio 2: Ottenere le impostazioni di accesso remoto per un nodo</span><span class="sxs-lookup"><span data-stu-id="d8e1d-116">Example 2: Get remote logon settings for a node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchRemoteLoginSetting -PoolId "ContosoPool" -ComputeNodeId "tvm-1900272697_1-20150330t205553z" -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50000
```

<span data-ttu-id="d8e1d-117">Il primo comando ottiene un contesto di account batch contenente i tasti di scelta per l'abbonamento e quindi lo archivia nella $Context variabile.</span><span class="sxs-lookup"><span data-stu-id="d8e1d-117">The first command gets a batch account context that contains access keys for your subscription, and then stores it in the $Context variable.</span></span>
<span data-ttu-id="d8e1d-118">Il secondo comando ottiene le impostazioni di accesso remoto per il nodo di elaborazione con l'ID specificato nel pool con l'ID ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="d8e1d-118">The second command gets the remote logon settings for the compute node that has the specified ID in the pool that has the ID ContosoPool.</span></span>

## <span data-ttu-id="d8e1d-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8e1d-119">PARAMETERS</span></span>

### <span data-ttu-id="d8e1d-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d8e1d-120">-BatchContext</span></span>
<span data-ttu-id="d8e1d-121">Specifica **l'istanza BatchAccountContext** che questo cmdlet usa per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="d8e1d-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d8e1d-122">Per ottenere un **batchAccountContext** che contiene le chiavi di accesso per la sottoscrizione, usare il cmdlet Get-AzBatchAccountKey.</span><span class="sxs-lookup"><span data-stu-id="d8e1d-122">To obtain a **BatchAccountContext** that contains access keys for your subscription, use the Get-AzBatchAccountKey cmdlet.</span></span>

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

### <span data-ttu-id="d8e1d-123">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="d8e1d-123">-ComputeNode</span></span>
<span data-ttu-id="d8e1d-124">Specifica un nodo di calcolo, come oggetto **PSComputeNode,** per cui questo cmdlet ottiene le impostazioni di accesso remoto.</span><span class="sxs-lookup"><span data-stu-id="d8e1d-124">Specifies a compute node, as a **PSComputeNode** object, for which this cmdlet gets remote logon settings.</span></span>
<span data-ttu-id="d8e1d-125">Per ottenere un oggetto nodo di calcolo, usare il cmdlet Get-AzBatchComputeNode di calcolo.</span><span class="sxs-lookup"><span data-stu-id="d8e1d-125">To obtain a compute node object, use the Get-AzBatchComputeNode cmdlet.</span></span>

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

### <span data-ttu-id="d8e1d-126">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="d8e1d-126">-ComputeNodeId</span></span>
<span data-ttu-id="d8e1d-127">Specifica l'ID del nodo di calcolo per cui ottenere le impostazioni di accesso remoto.</span><span class="sxs-lookup"><span data-stu-id="d8e1d-127">Specifies the ID of the compute node for which to get the remote logon settings.</span></span>
<span data-ttu-id="d8e1d-128">per cui questo cmdlet ottiene le impostazioni di accesso remoto.</span><span class="sxs-lookup"><span data-stu-id="d8e1d-128">for which this cmdlet gets remote logon settings.</span></span>

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

### <span data-ttu-id="d8e1d-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8e1d-129">-DefaultProfile</span></span>
<span data-ttu-id="d8e1d-130">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d8e1d-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8e1d-131">-PoolId</span><span class="sxs-lookup"><span data-stu-id="d8e1d-131">-PoolId</span></span>
<span data-ttu-id="d8e1d-132">Specifica l'ID del pool che contiene la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d8e1d-132">Specifies the ID of the pool that contains the virtual machine.</span></span>

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

### <span data-ttu-id="d8e1d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8e1d-133">CommonParameters</span></span>
<span data-ttu-id="d8e1d-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8e1d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8e1d-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d8e1d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8e1d-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="d8e1d-136">INPUTS</span></span>

### <span data-ttu-id="d8e1d-137">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="d8e1d-137">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="d8e1d-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d8e1d-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d8e1d-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d8e1d-139">OUTPUTS</span></span>

### <span data-ttu-id="d8e1d-140">Microsoft.Azure.Commands.Batch. Models.PSRemoteLoginSettings</span><span class="sxs-lookup"><span data-stu-id="d8e1d-140">Microsoft.Azure.Commands.Batch.Models.PSRemoteLoginSettings</span></span>

## <span data-ttu-id="d8e1d-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="d8e1d-141">NOTES</span></span>

## <span data-ttu-id="d8e1d-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d8e1d-142">RELATED LINKS</span></span>

[<span data-ttu-id="d8e1d-143">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="d8e1d-143">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="d8e1d-144">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="d8e1d-144">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="d8e1d-145">Get-AzBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="d8e1d-145">Get-AzBatchRemoteDesktopProtocolFile</span></span>](./Get-AzBatchRemoteDesktopProtocolFile.md)

[<span data-ttu-id="d8e1d-146">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="d8e1d-146">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
