---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 0BB79553-26DA-413C-8086-740DB6B31A85
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNode.md
ms.openlocfilehash: 39bbc9102d72c469730fe494869bffe5f726b41a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517575"
---
# <span data-ttu-id="a8d18-101">Remove-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="a8d18-101">Remove-AzureBatchComputeNode</span></span>

## <span data-ttu-id="a8d18-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a8d18-102">SYNOPSIS</span></span>
<span data-ttu-id="a8d18-103">Rimuove i nodi compute da un pool.</span><span class="sxs-lookup"><span data-stu-id="a8d18-103">Removes compute nodes from a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8d18-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a8d18-104">SYNTAX</span></span>

### <span data-ttu-id="a8d18-105">ID (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a8d18-105">Id (Default)</span></span>
```
Remove-AzureBatchComputeNode [-PoolId] <String> [-Ids] <String[]>
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8d18-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a8d18-106">InputObject</span></span>
```
Remove-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>]
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a8d18-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8d18-107">DESCRIPTION</span></span>
<span data-ttu-id="a8d18-108">Il cmdlet **Remove-AzureBatchComputeNode** rimuove i nodi compute batch di Azure da un pool.</span><span class="sxs-lookup"><span data-stu-id="a8d18-108">The **Remove-AzureBatchComputeNode** cmdlet removes Azure Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="a8d18-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a8d18-109">EXAMPLES</span></span>

### <span data-ttu-id="a8d18-110">Esempio 1: rimuovere un nodo Compute</span><span class="sxs-lookup"><span data-stu-id="a8d18-110">Example 1: Remove a compute node</span></span>
```
PS C:\>Remove-AzureBatchComputeNode -PoolId "Pool07" -Ids "tvm-2316545714_1-20150725t213220z" -DeallocationOption Terminate -ResizeTimeout ([TimeSpan]::FromMinutes(10)) -BatchContext $Context
```

<span data-ttu-id="a8d18-111">Questo comando rimuove il nodo COMPUTE con l'ID specificato da pool che contiene l'ID Pool07.</span><span class="sxs-lookup"><span data-stu-id="a8d18-111">This command removes compute node that has the specified ID from pool that has the ID Pool07.</span></span>
<span data-ttu-id="a8d18-112">Il comando specifica l'opzione termina disallocazione.</span><span class="sxs-lookup"><span data-stu-id="a8d18-112">The command specifies the Terminate deallocation option.</span></span>
<span data-ttu-id="a8d18-113">Il timeout di ridimensionamento è di 10 minuti.</span><span class="sxs-lookup"><span data-stu-id="a8d18-113">The resize time-out is of 10 minutes.</span></span>

### <span data-ttu-id="a8d18-114">Esempio 2: rimuovere un nodo Compute tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="a8d18-114">Example 2: Remove a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "Pool07" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context | Remove-AzureBatchComputeNode -Force -BatchContext $Context
```

<span data-ttu-id="a8d18-115">Questo comando ottiene il nodo COMPUTE con l'ID specificato da pool che contiene l'ID Pool07 usando il cmdlet Get-AzureBatchComputeNode.</span><span class="sxs-lookup"><span data-stu-id="a8d18-115">This command gets the compute node that has the specified ID from pool that has the ID Pool07 by using the Get-AzureBatchComputeNode cmdlet.</span></span>
<span data-ttu-id="a8d18-116">Il comando passa il nodo al cmdlet corrente tramite la pipeline.</span><span class="sxs-lookup"><span data-stu-id="a8d18-116">The command passes that node to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="a8d18-117">Il cmdlet corrente rimuove il nodo COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="a8d18-117">The current cmdlet removes the compute node.</span></span>
<span data-ttu-id="a8d18-118">Il comando specifica il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="a8d18-118">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="a8d18-119">Di conseguenza, il comando non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="a8d18-119">Therefore, the command does not prompt you for confirmation.</span></span>

### <span data-ttu-id="a8d18-120">Esempio 3: rimuovere più nodi</span><span class="sxs-lookup"><span data-stu-id="a8d18-120">Example 3: Remove multiple nodes</span></span>
```
PS C:\>Remove-AzureBatchComputeNode -PoolId "Pool07" @("tvm-1783593343_28-20151117t214257z","tvm-1783593343_29-20151117t214257z") -Force -BatchContext $Context
```

<span data-ttu-id="a8d18-121">Questo comando rimuove due nodi compute dal pool che contiene l'ID Pool07.</span><span class="sxs-lookup"><span data-stu-id="a8d18-121">This command removes two compute nodes from the pool that has the ID Pool07.</span></span>
<span data-ttu-id="a8d18-122">Il comando non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="a8d18-122">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="a8d18-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a8d18-123">PARAMETERS</span></span>

### <span data-ttu-id="a8d18-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a8d18-124">-BatchContext</span></span>
<span data-ttu-id="a8d18-125">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="a8d18-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a8d18-126">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="a8d18-126">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a8d18-127">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="a8d18-127">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a8d18-128">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a8d18-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a8d18-129">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="a8d18-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a8d18-130">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="a8d18-130">-ComputeNode</span></span>
<span data-ttu-id="a8d18-131">Specifica l'oggetto **PSComputeNode** che rappresenta il nodo Compute rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8d18-131">Specifies the **PSComputeNode** object that represents the compute node that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a8d18-132">-DeallocationOption</span><span class="sxs-lookup"><span data-stu-id="a8d18-132">-DeallocationOption</span></span>
<span data-ttu-id="a8d18-133">Specifica un'opzione di deallocazione per l'operazione di rimozione avviata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8d18-133">Specifies a deallocation option for the removal operation that this cmdlet starts.</span></span>
<span data-ttu-id="a8d18-134">Il valore predefinito è requeue.</span><span class="sxs-lookup"><span data-stu-id="a8d18-134">The default value is Requeue.</span></span>

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

### <span data-ttu-id="a8d18-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8d18-135">-DefaultProfile</span></span>
<span data-ttu-id="a8d18-136">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a8d18-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8d18-137">-Force</span><span class="sxs-lookup"><span data-stu-id="a8d18-137">-Force</span></span>
<span data-ttu-id="a8d18-138">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a8d18-138">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8d18-139">-IDS</span><span class="sxs-lookup"><span data-stu-id="a8d18-139">-Ids</span></span>
<span data-ttu-id="a8d18-140">Specifica una matrice di ID dei nodi compute rimossi dal cmdlet dal pool.</span><span class="sxs-lookup"><span data-stu-id="a8d18-140">Specifies an array of IDs of compute nodes that this cmdlet removes from the pool.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Id
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8d18-141">-PoolId</span><span class="sxs-lookup"><span data-stu-id="a8d18-141">-PoolId</span></span>
<span data-ttu-id="a8d18-142">Specifica l'ID del pool che contiene i nodi compute rimossi da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8d18-142">Specifies the ID of the pool that contains the compute nodes that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a8d18-143">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="a8d18-143">-ResizeTimeout</span></span>
<span data-ttu-id="a8d18-144">Specifica l'intervallo di timeout per la rimozione dei nodi di calcolo dal pool.</span><span class="sxs-lookup"><span data-stu-id="a8d18-144">Specifies the time-out interval for removal of the compute nodes from the pool.</span></span>
<span data-ttu-id="a8d18-145">Il valore predefinito è di 10 minuti.</span><span class="sxs-lookup"><span data-stu-id="a8d18-145">The default value is 10 minutes.</span></span>
<span data-ttu-id="a8d18-146">Il valore minimo è di 5 minuti.</span><span class="sxs-lookup"><span data-stu-id="a8d18-146">The minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="a8d18-147">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a8d18-147">-Confirm</span></span>
<span data-ttu-id="a8d18-148">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8d18-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8d18-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8d18-149">-WhatIf</span></span>
<span data-ttu-id="a8d18-150">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a8d18-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8d18-151">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a8d18-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8d18-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8d18-152">CommonParameters</span></span>
<span data-ttu-id="a8d18-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8d18-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8d18-154">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8d18-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8d18-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a8d18-155">INPUTS</span></span>

### <span data-ttu-id="a8d18-156">Microsoft.Azure.Commands.Batch. Models. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="a8d18-156">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>
<span data-ttu-id="a8d18-157">Parametri: ComputeNode (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a8d18-157">Parameters: ComputeNode (ByValue)</span></span>

### <span data-ttu-id="a8d18-158">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a8d18-158">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="a8d18-159">Parametri: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a8d18-159">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="a8d18-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a8d18-160">OUTPUTS</span></span>

### <span data-ttu-id="a8d18-161">System. void</span><span class="sxs-lookup"><span data-stu-id="a8d18-161">System.Void</span></span>

## <span data-ttu-id="a8d18-162">Note</span><span class="sxs-lookup"><span data-stu-id="a8d18-162">NOTES</span></span>

## <span data-ttu-id="a8d18-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a8d18-163">RELATED LINKS</span></span>

[<span data-ttu-id="a8d18-164">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="a8d18-164">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="a8d18-165">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="a8d18-165">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="a8d18-166">Riavviare-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="a8d18-166">Restart-AzureBatchComputeNode</span></span>](./Restart-AzureBatchComputeNode.md)


