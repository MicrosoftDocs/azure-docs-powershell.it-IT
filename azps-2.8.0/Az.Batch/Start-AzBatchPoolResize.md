---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 82DC8DC4-D8EC-4847-A54C-B779256FD590
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/start-azbatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchPoolResize.md
ms.openlocfilehash: c68911de8d01a654593e72b98ba5d53bf40c76ed
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2020
ms.locfileid: "93865664"
---
# <span data-ttu-id="60074-101">Start-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="60074-101">Start-AzBatchPoolResize</span></span>

## <span data-ttu-id="60074-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="60074-102">SYNOPSIS</span></span>
<span data-ttu-id="60074-103">Inizia a ridimensionare un pool.</span><span class="sxs-lookup"><span data-stu-id="60074-103">Starts to resize a pool.</span></span>

## <span data-ttu-id="60074-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="60074-104">SYNTAX</span></span>

```
Start-AzBatchPoolResize [-Id] <String> [-TargetDedicatedComputeNodes <Int32>]
 [-TargetLowPriorityComputeNodes <Int32>] [-ResizeTimeout <TimeSpan>]
 [-ComputeNodeDeallocationOption <ComputeNodeDeallocationOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60074-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60074-105">DESCRIPTION</span></span>
<span data-ttu-id="60074-106">Il cmdlet **Start-AzBatchPoolResize** avvia un'operazione di ridimensionamento batch di Azure in un pool.</span><span class="sxs-lookup"><span data-stu-id="60074-106">The **Start-AzBatchPoolResize** cmdlet starts an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="60074-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="60074-107">EXAMPLES</span></span>

### <span data-ttu-id="60074-108">Esempio 1: ridimensionare un pool in 12 nodi</span><span class="sxs-lookup"><span data-stu-id="60074-108">Example 1: Resize a pool to 12 nodes</span></span>
```
PS C:\>Start-AzBatchPoolResize -Id "ContosoPool06" -TargetDedicatedComputeNodes 12 -BatchContext $Context
```

<span data-ttu-id="60074-109">Questo comando avvia un'operazione di ridimensionamento nel pool che contiene l'ID ContosoPool06.</span><span class="sxs-lookup"><span data-stu-id="60074-109">This command starts a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="60074-110">La destinazione per l'operazione è 12 nodi di calcolo dedicati.</span><span class="sxs-lookup"><span data-stu-id="60074-110">The target for the operation is 12 dedicated compute nodes.</span></span>
<span data-ttu-id="60074-111">Usa il cmdlet Get-AzBatchAccountKeys per assegnare un contesto alla variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="60074-111">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="60074-112">Esempio 2: ridimensionare un pool usando un'opzione di deallocazione</span><span class="sxs-lookup"><span data-stu-id="60074-112">Example 2: Resize a pool using a deallocation option</span></span>
```
PS C:\>Get-AzBatchPool -Id "ContosoPool06" -BatchContext $Context | Start-AzBatchPoolResize -TargetDedicatedComputeNodes 5 -ResizeTimeout ([TimeSpan]::FromHours(1)) -ComputeNodeDeallocationOption ([Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]::Terminate) -BatchContext $Context
```

<span data-ttu-id="60074-113">Questo cmdlet consente di ridimensionare un pool in cinque nodi di calcolo dedicati.</span><span class="sxs-lookup"><span data-stu-id="60074-113">This cmdlet resizes a pool to five dedicated compute nodes.</span></span>
<span data-ttu-id="60074-114">Il comando ottiene il pool con ID ContosoPool06 usando il cmdlet Get-AzBatchPool.</span><span class="sxs-lookup"><span data-stu-id="60074-114">The command gets the pool that has the ID ContosoPool06 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="60074-115">Il comando passa l'oggetto pool al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="60074-115">The command passes that pool object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="60074-116">Il comando avvia un'operazione di ridimensionamento nel pool.</span><span class="sxs-lookup"><span data-stu-id="60074-116">The command starts a resize operation on the pool.</span></span>
<span data-ttu-id="60074-117">La destinazione è cinque nodi di calcolo dedicati.</span><span class="sxs-lookup"><span data-stu-id="60074-117">The target is five dedicated compute nodes.</span></span>
<span data-ttu-id="60074-118">Il comando specifica il periodo di timeout di un'ora.</span><span class="sxs-lookup"><span data-stu-id="60074-118">The command specifies time-out period of one hour.</span></span>
<span data-ttu-id="60074-119">Il comando specifica un'opzione di disallocazione di terminate.</span><span class="sxs-lookup"><span data-stu-id="60074-119">The command specifies a deallocation option of Terminate.</span></span>

## <span data-ttu-id="60074-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="60074-120">PARAMETERS</span></span>

### <span data-ttu-id="60074-121">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="60074-121">-BatchContext</span></span>
<span data-ttu-id="60074-122">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="60074-122">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="60074-123">Se si usa il cmdlet Get-AzBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="60074-123">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="60074-124">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="60074-124">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="60074-125">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="60074-125">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="60074-126">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="60074-126">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="60074-127">-ComputeNodeDeallocationOption</span><span class="sxs-lookup"><span data-stu-id="60074-127">-ComputeNodeDeallocationOption</span></span>
<span data-ttu-id="60074-128">Specifica un'opzione di deallocazione per l'operazione di ridimensionamento avviata dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60074-128">Specifies a deallocation option for the resizing operation that this cmdlet starts.</span></span>

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

### <span data-ttu-id="60074-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60074-129">-DefaultProfile</span></span>
<span data-ttu-id="60074-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="60074-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60074-131">-ID</span><span class="sxs-lookup"><span data-stu-id="60074-131">-Id</span></span>
<span data-ttu-id="60074-132">Specifica l'ID del pool di cui viene ridimensionato il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60074-132">Specifies the ID of the pool that this cmdlet resizes.</span></span>

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

### <span data-ttu-id="60074-133">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="60074-133">-ResizeTimeout</span></span>
<span data-ttu-id="60074-134">Specifica un periodo di timeout per l'operazione di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="60074-134">Specifies a time-out period for the resizing operation.</span></span>
<span data-ttu-id="60074-135">Se il pool non raggiunge le dimensioni di destinazione in questo momento, l'operazione di ridimensionamento si arresta.</span><span class="sxs-lookup"><span data-stu-id="60074-135">If the pool does not reach the target size by this time, the resize operation stops.</span></span>

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

### <span data-ttu-id="60074-136">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="60074-136">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="60074-137">Numero di nodi di calcolo dedicati alla destinazione.</span><span class="sxs-lookup"><span data-stu-id="60074-137">The number of target dedicated compute nodes.</span></span>

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

### <span data-ttu-id="60074-138">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="60074-138">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="60074-139">Numero di nodi di calcolo con priorità bassa di destinazione.</span><span class="sxs-lookup"><span data-stu-id="60074-139">The number of target low-priority compute nodes.</span></span>

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

### <span data-ttu-id="60074-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60074-140">CommonParameters</span></span>
<span data-ttu-id="60074-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60074-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60074-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60074-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60074-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="60074-143">INPUTS</span></span>

### <span data-ttu-id="60074-144">System. String</span><span class="sxs-lookup"><span data-stu-id="60074-144">System.String</span></span>

### <span data-ttu-id="60074-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="60074-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="60074-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="60074-146">OUTPUTS</span></span>

### <span data-ttu-id="60074-147">System. void</span><span class="sxs-lookup"><span data-stu-id="60074-147">System.Void</span></span>

## <span data-ttu-id="60074-148">Note</span><span class="sxs-lookup"><span data-stu-id="60074-148">NOTES</span></span>

## <span data-ttu-id="60074-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="60074-149">RELATED LINKS</span></span>

[<span data-ttu-id="60074-150">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="60074-150">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="60074-151">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="60074-151">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="60074-152">Stop-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="60074-152">Stop-AzBatchPoolResize</span></span>](./Stop-AzBatchPoolResize.md)

[<span data-ttu-id="60074-153">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="60074-153">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


