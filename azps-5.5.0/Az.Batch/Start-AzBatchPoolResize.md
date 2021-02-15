---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 82DC8DC4-D8EC-4847-A54C-B779256FD590
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/start-azbatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchPoolResize.md
ms.openlocfilehash: d8b03aee736456e549a6c88a0aacfeac1d78744c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182039"
---
# <span data-ttu-id="c02db-101">Start-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="c02db-101">Start-AzBatchPoolResize</span></span>

## <span data-ttu-id="c02db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c02db-102">SYNOPSIS</span></span>
<span data-ttu-id="c02db-103">Inizia a ridimensionare una pool.</span><span class="sxs-lookup"><span data-stu-id="c02db-103">Starts to resize a pool.</span></span>

## <span data-ttu-id="c02db-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c02db-104">SYNTAX</span></span>

```
Start-AzBatchPoolResize [-Id] <String> [-TargetDedicatedComputeNodes <Int32>]
 [-TargetLowPriorityComputeNodes <Int32>] [-ResizeTimeout <TimeSpan>]
 [-ComputeNodeDeallocationOption <ComputeNodeDeallocationOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c02db-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c02db-105">DESCRIPTION</span></span>
<span data-ttu-id="c02db-106">Il cmdlet **Start-AzBatchPoolResize avvia** un'operazione di ridimensionamento batch di Azure in un pool.</span><span class="sxs-lookup"><span data-stu-id="c02db-106">The **Start-AzBatchPoolResize** cmdlet starts an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="c02db-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c02db-107">EXAMPLES</span></span>

### <span data-ttu-id="c02db-108">Esempio 1: Ridimensionare un pool in 12 nodi</span><span class="sxs-lookup"><span data-stu-id="c02db-108">Example 1: Resize a pool to 12 nodes</span></span>
```
PS C:\>Start-AzBatchPoolResize -Id "ContosoPool06" -TargetDedicatedComputeNodes 12 -BatchContext $Context
```

<span data-ttu-id="c02db-109">Questo comando avvia un'operazione di ridimensionamento nel pool con l'ID ContosoPool06.</span><span class="sxs-lookup"><span data-stu-id="c02db-109">This command starts a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="c02db-110">La destinazione per l'operazione è 12 nodi di calcolo dedicati.</span><span class="sxs-lookup"><span data-stu-id="c02db-110">The target for the operation is 12 dedicated compute nodes.</span></span>
<span data-ttu-id="c02db-111">Usare il cmdlet Get-AzBatchAccountKey per assegnare un contesto alla $Context variabile.</span><span class="sxs-lookup"><span data-stu-id="c02db-111">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="c02db-112">Esempio 2: Ridimensionare un pool usando un'opzione di deassegnazione</span><span class="sxs-lookup"><span data-stu-id="c02db-112">Example 2: Resize a pool using a deallocation option</span></span>
```
PS C:\>Get-AzBatchPool -Id "ContosoPool06" -BatchContext $Context | Start-AzBatchPoolResize -TargetDedicatedComputeNodes 5 -ResizeTimeout ([TimeSpan]::FromHours(1)) -ComputeNodeDeallocationOption ([Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]::Terminate) -BatchContext $Context
```

<span data-ttu-id="c02db-113">Questo cmdlet ridimensiona un pool in cinque nodi di elaborazione dedicati.</span><span class="sxs-lookup"><span data-stu-id="c02db-113">This cmdlet resizes a pool to five dedicated compute nodes.</span></span>
<span data-ttu-id="c02db-114">Il comando ottiene il pool con l'ID ContosoPool06 usando il cmdlet Get-AzBatchPool></span><span class="sxs-lookup"><span data-stu-id="c02db-114">The command gets the pool that has the ID ContosoPool06 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="c02db-115">Il comando passa l'oggetto pool al cmdlet corrente usando l'operatore della pipeline.</span><span class="sxs-lookup"><span data-stu-id="c02db-115">The command passes that pool object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c02db-116">Il comando avvia un'operazione di ridimensionamento nel pool.</span><span class="sxs-lookup"><span data-stu-id="c02db-116">The command starts a resize operation on the pool.</span></span>
<span data-ttu-id="c02db-117">La destinazione è cinque nodi di calcolo dedicati.</span><span class="sxs-lookup"><span data-stu-id="c02db-117">The target is five dedicated compute nodes.</span></span>
<span data-ttu-id="c02db-118">Il comando specifica il periodo di timeout di un'ora.</span><span class="sxs-lookup"><span data-stu-id="c02db-118">The command specifies time-out period of one hour.</span></span>
<span data-ttu-id="c02db-119">Il comando specifica un'opzione di deallocation di Terminate.</span><span class="sxs-lookup"><span data-stu-id="c02db-119">The command specifies a deallocation option of Terminate.</span></span>

## <span data-ttu-id="c02db-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c02db-120">PARAMETERS</span></span>

### <span data-ttu-id="c02db-121">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c02db-121">-BatchContext</span></span>
<span data-ttu-id="c02db-122">Specifica **l'istanza BatchAccountContext** che questo cmdlet usa per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="c02db-122">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c02db-123">Se si usa il cmdlet Get-AzBatchAccount per ottenere BatchAccountContext, verrà usata l'autenticazione di Azure Active Directory quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="c02db-123">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c02db-124">Per usare invece l'autenticazione della chiave condivisa, usare il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.</span><span class="sxs-lookup"><span data-stu-id="c02db-124">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c02db-125">Quando si usa l'autenticazione con chiave condivisa, per impostazione predefinita viene usata la chiave di accesso primario.</span><span class="sxs-lookup"><span data-stu-id="c02db-125">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c02db-126">Per modificare la chiave da usare, impostare la proprietà BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="c02db-126">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c02db-127">-ComputeNodeDeallocationOption</span><span class="sxs-lookup"><span data-stu-id="c02db-127">-ComputeNodeDeallocationOption</span></span>
<span data-ttu-id="c02db-128">Specifica un'opzione di deassegnazione per l'operazione di ridimensionamento avviata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c02db-128">Specifies a deallocation option for the resizing operation that this cmdlet starts.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c02db-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c02db-129">-DefaultProfile</span></span>
<span data-ttu-id="c02db-130">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c02db-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c02db-131">-Id</span><span class="sxs-lookup"><span data-stu-id="c02db-131">-Id</span></span>
<span data-ttu-id="c02db-132">Specifica l'ID del pool ridimensionato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c02db-132">Specifies the ID of the pool that this cmdlet resizes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c02db-133">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="c02db-133">-ResizeTimeout</span></span>
<span data-ttu-id="c02db-134">Specifica un periodo di timeout per l'operazione di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="c02db-134">Specifies a time-out period for the resizing operation.</span></span>
<span data-ttu-id="c02db-135">Se al momento il pool non raggiunge le dimensioni di destinazione, l'operazione di ridimensionamento si interrompe.</span><span class="sxs-lookup"><span data-stu-id="c02db-135">If the pool does not reach the target size by this time, the resize operation stops.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c02db-136">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="c02db-136">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="c02db-137">Numero di nodi di elaborazione dedicati di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c02db-137">The number of target dedicated compute nodes.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: TargetDedicated

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c02db-138">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="c02db-138">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="c02db-139">Numero di nodi di calcolo di destinazione con priorità bassa.</span><span class="sxs-lookup"><span data-stu-id="c02db-139">The number of target low-priority compute nodes.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c02db-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c02db-140">CommonParameters</span></span>
<span data-ttu-id="c02db-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c02db-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c02db-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c02db-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c02db-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="c02db-143">INPUTS</span></span>

### <span data-ttu-id="c02db-144">System.String</span><span class="sxs-lookup"><span data-stu-id="c02db-144">System.String</span></span>

### <span data-ttu-id="c02db-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c02db-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="c02db-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c02db-146">OUTPUTS</span></span>

### <span data-ttu-id="c02db-147">System.Void</span><span class="sxs-lookup"><span data-stu-id="c02db-147">System.Void</span></span>

## <span data-ttu-id="c02db-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="c02db-148">NOTES</span></span>

## <span data-ttu-id="c02db-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c02db-149">RELATED LINKS</span></span>

[<span data-ttu-id="c02db-150">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="c02db-150">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="c02db-151">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="c02db-151">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="c02db-152">Stop-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="c02db-152">Stop-AzBatchPoolResize</span></span>](./Stop-AzBatchPoolResize.md)

[<span data-ttu-id="c02db-153">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="c02db-153">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
