---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 07811B64-6A77-452C-B148-DE8C13E73DEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchremoteloginsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
ms.openlocfilehash: 03c37bb1cf70dfefc5373e9211d6365feb133ad4
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2020
ms.locfileid: "93865636"
---
# <span data-ttu-id="f546a-101">Get-AzBatchRemoteLoginSetting</span><span class="sxs-lookup"><span data-stu-id="f546a-101">Get-AzBatchRemoteLoginSetting</span></span>

## <span data-ttu-id="f546a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f546a-102">SYNOPSIS</span></span>
<span data-ttu-id="f546a-103">Ottiene le impostazioni di accesso remoto per un nodo COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="f546a-103">Gets remote logon settings for a compute node.</span></span>

## <span data-ttu-id="f546a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f546a-104">SYNTAX</span></span>

### <span data-ttu-id="f546a-105">ID (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f546a-105">Id (Default)</span></span>
```
Get-AzBatchRemoteLoginSetting [-PoolId] <String> [-ComputeNodeId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f546a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="f546a-106">InputObject</span></span>
```
Get-AzBatchRemoteLoginSetting [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f546a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f546a-107">DESCRIPTION</span></span>
<span data-ttu-id="f546a-108">Il cmdlet **Get-AzBatchRemoteLoginSetting** ottiene le impostazioni di accesso remoto per un nodo COMPUTE in un pool di macchine virtuali basato sull'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="f546a-108">The **Get-AzBatchRemoteLoginSetting** cmdlet gets remote logon settings for a compute node in a virtual machines infrastructure-based pool.</span></span>

## <span data-ttu-id="f546a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f546a-109">EXAMPLES</span></span>

### <span data-ttu-id="f546a-110">Esempio 1: ottenere le impostazioni di accesso remoto per tutti i nodi di un pool</span><span class="sxs-lookup"><span data-stu-id="f546a-110">Example 1: Get remote logon settings for all nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchComputeNode -PoolId "ContosoPool" -BatchContext $Context | Get-AzBatchRemoteLoginSetting -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50002
10.214.75.221   50001
10.214.75.221   50000
```

<span data-ttu-id="f546a-111">Il primo comando ottiene un contesto dell'account batch che contiene i tasti di scelta per l'abbonamento utilizzando **Get-AzBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="f546a-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzBatchAccountKeys**.</span></span>
<span data-ttu-id="f546a-112">Il comando Archivia il contesto nella variabile $Context da usare nel comando successivo.</span><span class="sxs-lookup"><span data-stu-id="f546a-112">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="f546a-113">Il secondo comando ottiene ogni nodo Compute nel pool che contiene l'ID ContosoPool utilizzando **Get-AzBatchComputeNode**.</span><span class="sxs-lookup"><span data-stu-id="f546a-113">The second command gets each compute node in the pool that has the ID ContosoPool by using **Get-AzBatchComputeNode**.</span></span>
<span data-ttu-id="f546a-114">Il comando passa ogni nodo del computer al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="f546a-114">The command passes each computer node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f546a-115">Il comando ottiene le impostazioni di accesso remoto per ogni nodo COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="f546a-115">The command gets the remote logon settings for each compute node.</span></span>

### <span data-ttu-id="f546a-116">Esempio 2: ottenere le impostazioni di accesso remoto per un nodo</span><span class="sxs-lookup"><span data-stu-id="f546a-116">Example 2: Get remote logon settings for a node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchRemoteLoginSetting -PoolId "ContosoPool" -ComputeNodeId "tvm-1900272697_1-20150330t205553z" -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50000
```

<span data-ttu-id="f546a-117">Il primo comando ottiene un contesto dell'account batch che contiene i tasti di scelta per l'abbonamento e lo archivia nella variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="f546a-117">The first command gets a batch account context that contains access keys for your subscription, and then stores it in the $Context variable.</span></span>
<span data-ttu-id="f546a-118">Il secondo comando consente di ottenere le impostazioni di accesso remoto per il nodo COMPUTE con l'ID specificato nel pool che contiene l'ID ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="f546a-118">The second command gets the remote logon settings for the compute node that has the specified ID in the pool that has the ID ContosoPool.</span></span>

## <span data-ttu-id="f546a-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f546a-119">PARAMETERS</span></span>

### <span data-ttu-id="f546a-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f546a-120">-BatchContext</span></span>
<span data-ttu-id="f546a-121">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="f546a-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f546a-122">Per ottenere un **BatchAccountContext** che contiene i tasti di scelta per l'abbonamento, usare il cmdlet Get-AzBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="f546a-122">To obtain a **BatchAccountContext** that contains access keys for your subscription, use the Get-AzBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="f546a-123">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="f546a-123">-ComputeNode</span></span>
<span data-ttu-id="f546a-124">Specifica un nodo COMPUTE, come oggetto **PSComputeNode** , per cui questo cmdlet ottiene le impostazioni di accesso remoto.</span><span class="sxs-lookup"><span data-stu-id="f546a-124">Specifies a compute node, as a **PSComputeNode** object, for which this cmdlet gets remote logon settings.</span></span>
<span data-ttu-id="f546a-125">Per ottenere un oggetto compute node, usa il cmdlet Get-AzBatchComputeNode.</span><span class="sxs-lookup"><span data-stu-id="f546a-125">To obtain a compute node object, use the Get-AzBatchComputeNode cmdlet.</span></span>

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

### <span data-ttu-id="f546a-126">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="f546a-126">-ComputeNodeId</span></span>
<span data-ttu-id="f546a-127">Specifica l'ID del nodo COMPUTE per cui ottenere le impostazioni di accesso remoto.</span><span class="sxs-lookup"><span data-stu-id="f546a-127">Specifies the ID of the compute node for which to get the remote logon settings.</span></span>
<span data-ttu-id="f546a-128">per cui questo cmdlet ottiene le impostazioni di accesso remoto.</span><span class="sxs-lookup"><span data-stu-id="f546a-128">for which this cmdlet gets remote logon settings.</span></span>

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

### <span data-ttu-id="f546a-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f546a-129">-DefaultProfile</span></span>
<span data-ttu-id="f546a-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f546a-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f546a-131">-PoolId</span><span class="sxs-lookup"><span data-stu-id="f546a-131">-PoolId</span></span>
<span data-ttu-id="f546a-132">Specifica l'ID del pool che contiene la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f546a-132">Specifies the ID of the pool that contains the virtual machine.</span></span>

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

### <span data-ttu-id="f546a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f546a-133">CommonParameters</span></span>
<span data-ttu-id="f546a-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f546a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f546a-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f546a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f546a-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f546a-136">INPUTS</span></span>

### <span data-ttu-id="f546a-137">Microsoft.Azure.Commands.Batch. Models. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="f546a-137">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="f546a-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f546a-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="f546a-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f546a-139">OUTPUTS</span></span>

### <span data-ttu-id="f546a-140">Microsoft.Azure.Commands.Batch. Models. PSRemoteLoginSettings</span><span class="sxs-lookup"><span data-stu-id="f546a-140">Microsoft.Azure.Commands.Batch.Models.PSRemoteLoginSettings</span></span>

## <span data-ttu-id="f546a-141">Note</span><span class="sxs-lookup"><span data-stu-id="f546a-141">NOTES</span></span>

## <span data-ttu-id="f546a-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f546a-142">RELATED LINKS</span></span>

[<span data-ttu-id="f546a-143">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="f546a-143">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="f546a-144">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="f546a-144">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="f546a-145">Get-AzBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="f546a-145">Get-AzBatchRemoteDesktopProtocolFile</span></span>](./Get-AzBatchRemoteDesktopProtocolFile.md)

[<span data-ttu-id="f546a-146">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="f546a-146">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


