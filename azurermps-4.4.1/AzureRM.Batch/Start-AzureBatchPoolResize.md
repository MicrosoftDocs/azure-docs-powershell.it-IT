---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 82DC8DC4-D8EC-4847-A54C-B779256FD590
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchPoolResize.md
ms.openlocfilehash: 558f8c062e60f6e9f7c18c05be8f1ccb2eafa9fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518355"
---
# <span data-ttu-id="f3831-101">Start-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="f3831-101">Start-AzureBatchPoolResize</span></span>

## <span data-ttu-id="f3831-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f3831-102">SYNOPSIS</span></span>
<span data-ttu-id="f3831-103">Inizia a ridimensionare un pool.</span><span class="sxs-lookup"><span data-stu-id="f3831-103">Starts to resize a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3831-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f3831-104">SYNTAX</span></span>

```
Start-AzureBatchPoolResize [-Id] <String> -TargetDedicated <Int32> [-ResizeTimeout <TimeSpan>]
 [-ComputeNodeDeallocationOption <ComputeNodeDeallocationOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3831-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3831-105">DESCRIPTION</span></span>
<span data-ttu-id="f3831-106">Il cmdlet **Start-AzureBatchPoolResize** avvia un'operazione di ridimensionamento batch di Azure in un pool.</span><span class="sxs-lookup"><span data-stu-id="f3831-106">The **Start-AzureBatchPoolResize** cmdlet starts an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="f3831-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f3831-107">EXAMPLES</span></span>

### <span data-ttu-id="f3831-108">Esempio 1: ridimensionare un pool in 12 nodi</span><span class="sxs-lookup"><span data-stu-id="f3831-108">Example 1: Resize a pool to 12 nodes</span></span>
```
PS C:\>Start-AzureBatchPoolResize -Id "ContosoPool06" -TargetDedicated 12 -BatchContext $Context
```

<span data-ttu-id="f3831-109">Questo comando avvia un'operazione di ridimensionamento nel pool che contiene l'ID ContosoPool06.</span><span class="sxs-lookup"><span data-stu-id="f3831-109">This command starts a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="f3831-110">La destinazione per l'operazione è 12 nodi di calcolo dedicati.</span><span class="sxs-lookup"><span data-stu-id="f3831-110">The target for the operation is 12 dedicated compute nodes.</span></span>
<span data-ttu-id="f3831-111">Usa il cmdlet Get-AzureRmBatchAccountKeys per assegnare un contesto alla variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="f3831-111">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="f3831-112">Esempio 2: ridimensionare un pool usando un'opzione di deallocazione</span><span class="sxs-lookup"><span data-stu-id="f3831-112">Example 2: Resize a pool using a deallocation option</span></span>
```
PS C:\>Get-AzureBatchPool -Id "ContosoPool06" -BatchContext $Context | Start-AzureBatchPoolResize -TargetDedicated 5 -ResizeTimeout ([TimeSpan]::FromHours(1)) -ComputeNodeDeallocationOption ([Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]::Terminate) -BatchContext $Context
```

<span data-ttu-id="f3831-113">Questo cmdlet consente di ridimensionare un pool in cinque nodi di calcolo dedicati.</span><span class="sxs-lookup"><span data-stu-id="f3831-113">This cmdlet resizes a pool to five dedicated compute nodes.</span></span>
<span data-ttu-id="f3831-114">Il comando ottiene il pool con ID ContosoPool06 usando il cmdlet Get-AzureBatchPool.</span><span class="sxs-lookup"><span data-stu-id="f3831-114">The command gets the pool that has the ID ContosoPool06 by using the Get-AzureBatchPool cmdlet.</span></span>
<span data-ttu-id="f3831-115">Il comando passa l'oggetto pool al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="f3831-115">The command passes that pool object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f3831-116">Il comando avvia un'operazione di ridimensionamento nel pool.</span><span class="sxs-lookup"><span data-stu-id="f3831-116">The command starts a resize operation on the pool.</span></span>
<span data-ttu-id="f3831-117">La destinazione è cinque nodi di calcolo dedicati.</span><span class="sxs-lookup"><span data-stu-id="f3831-117">The target is five dedicated compute nodes.</span></span>
<span data-ttu-id="f3831-118">Il comando specifica il periodo di timeout di un'ora.</span><span class="sxs-lookup"><span data-stu-id="f3831-118">The command specifies time-out period of one hour.</span></span>
<span data-ttu-id="f3831-119">Il comando specifica un'opzione di disallocazione di terminate.</span><span class="sxs-lookup"><span data-stu-id="f3831-119">The command specifies a deallocation option of Terminate.</span></span>

## <span data-ttu-id="f3831-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f3831-120">PARAMETERS</span></span>

### <span data-ttu-id="f3831-121">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f3831-121">-BatchContext</span></span>
<span data-ttu-id="f3831-122">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="f3831-122">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f3831-123">Per ottenere un oggetto **BatchAccountContext** che contiene i tasti di scelta per l'abbonamento, usare il cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="f3831-123">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="f3831-124">-ComputeNodeDeallocationOption</span><span class="sxs-lookup"><span data-stu-id="f3831-124">-ComputeNodeDeallocationOption</span></span>
<span data-ttu-id="f3831-125">Specifica un'opzione di deallocazione per l'operazione di ridimensionamento avviata dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3831-125">Specifies a deallocation option for the resizing operation that this cmdlet starts.</span></span>

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

### <span data-ttu-id="f3831-126">-ID</span><span class="sxs-lookup"><span data-stu-id="f3831-126">-Id</span></span>
<span data-ttu-id="f3831-127">Specifica l'ID del pool di cui viene ridimensionato il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3831-127">Specifies the ID of the pool that this cmdlet resizes.</span></span>

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

### <span data-ttu-id="f3831-128">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="f3831-128">-ResizeTimeout</span></span>
<span data-ttu-id="f3831-129">Specifica un periodo di timeout per l'operazione di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="f3831-129">Specifies a time-out period for the resizing operation.</span></span>
<span data-ttu-id="f3831-130">Se il pool non raggiunge le dimensioni di destinazione in questo momento, l'operazione di ridimensionamento si arresta.</span><span class="sxs-lookup"><span data-stu-id="f3831-130">If the pool does not reach the target size by this time, the resize operation stops.</span></span>

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

### <span data-ttu-id="f3831-131">-TargetDedicated</span><span class="sxs-lookup"><span data-stu-id="f3831-131">-TargetDedicated</span></span>
<span data-ttu-id="f3831-132">Specifica il numero di destinazione dei nodi di calcolo dedicati.</span><span class="sxs-lookup"><span data-stu-id="f3831-132">Specifies the target number of dedicated compute nodes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3831-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3831-133">-DefaultProfile</span></span>
<span data-ttu-id="f3831-134">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f3831-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3831-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3831-135">CommonParameters</span></span>
<span data-ttu-id="f3831-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3831-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3831-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3831-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3831-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f3831-138">INPUTS</span></span>

### <span data-ttu-id="f3831-139">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f3831-139">BatchAccountContext</span></span>
<span data-ttu-id="f3831-140">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="f3831-140">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="f3831-141">Stringa</span><span class="sxs-lookup"><span data-stu-id="f3831-141">String</span></span>
<span data-ttu-id="f3831-142">Il parametro "ID" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="f3831-142">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="f3831-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f3831-143">OUTPUTS</span></span>

## <span data-ttu-id="f3831-144">Note</span><span class="sxs-lookup"><span data-stu-id="f3831-144">NOTES</span></span>

## <span data-ttu-id="f3831-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f3831-145">RELATED LINKS</span></span>

[<span data-ttu-id="f3831-146">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="f3831-146">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="f3831-147">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="f3831-147">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="f3831-148">Stop-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="f3831-148">Stop-AzureBatchPoolResize</span></span>](./Stop-AzureBatchPoolResize.md)

[<span data-ttu-id="f3831-149">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="f3831-149">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)

