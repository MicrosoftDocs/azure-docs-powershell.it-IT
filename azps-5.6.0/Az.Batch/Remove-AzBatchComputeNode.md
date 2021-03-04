---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 0BB79553-26DA-413C-8086-740DB6B31A85
online version: https://docs.microsoft.com/powershell/module/az.batch/remove-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNode.md
ms.openlocfilehash: 7e2b2bca042573ec96fefdf85e5077ec1138d1da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956029"
---
# <span data-ttu-id="a610b-101">Remove-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="a610b-101">Remove-AzBatchComputeNode</span></span>

## <span data-ttu-id="a610b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a610b-102">SYNOPSIS</span></span>
<span data-ttu-id="a610b-103">Rimuove i nodi di elaborazione da un pool.</span><span class="sxs-lookup"><span data-stu-id="a610b-103">Removes compute nodes from a pool.</span></span>

## <span data-ttu-id="a610b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a610b-104">SYNTAX</span></span>

### <span data-ttu-id="a610b-105">ID (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a610b-105">Id (Default)</span></span>
```
Remove-AzBatchComputeNode [-PoolId] <String> [-Ids] <String[]>
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a610b-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a610b-106">InputObject</span></span>
```
Remove-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>]
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a610b-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a610b-107">DESCRIPTION</span></span>
<span data-ttu-id="a610b-108">Il cmdlet **Remove-AzBatchComputeNode rimuove** i nodi di elaborazione batch di Azure da un pool.</span><span class="sxs-lookup"><span data-stu-id="a610b-108">The **Remove-AzBatchComputeNode** cmdlet removes Azure Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="a610b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a610b-109">EXAMPLES</span></span>

### <span data-ttu-id="a610b-110">Esempio 1: Rimuovere un nodo di calcolo</span><span class="sxs-lookup"><span data-stu-id="a610b-110">Example 1: Remove a compute node</span></span>
```
PS C:\>Remove-AzBatchComputeNode -PoolId "Pool07" -Ids "tvm-2316545714_1-20150725t213220z" -DeallocationOption Terminate -ResizeTimeout ([TimeSpan]::FromMinutes(10)) -BatchContext $Context
```

<span data-ttu-id="a610b-111">Questo comando rimuove il nodo di calcolo con l'ID specificato dal pool che ha l'ID Pool07.</span><span class="sxs-lookup"><span data-stu-id="a610b-111">This command removes compute node that has the specified ID from pool that has the ID Pool07.</span></span>
<span data-ttu-id="a610b-112">Il comando specifica l'opzione Disassegnazione.</span><span class="sxs-lookup"><span data-stu-id="a610b-112">The command specifies the Terminate deallocation option.</span></span>
<span data-ttu-id="a610b-113">Il timeout di ridimensionamento è di 10 minuti.</span><span class="sxs-lookup"><span data-stu-id="a610b-113">The resize time-out is of 10 minutes.</span></span>

### <span data-ttu-id="a610b-114">Esempio 2: Rimuovere un nodo di calcolo usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="a610b-114">Example 2: Remove a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool07" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context | Remove-AzBatchComputeNode -Force -BatchContext $Context
```

<span data-ttu-id="a610b-115">Questo comando recupera il nodo di calcolo con l'ID specificato dal pool che contiene l'ID Pool07 usando il cmdlet Get-AzBatchComputeNode> .</span><span class="sxs-lookup"><span data-stu-id="a610b-115">This command gets the compute node that has the specified ID from pool that has the ID Pool07 by using the Get-AzBatchComputeNode cmdlet.</span></span>
<span data-ttu-id="a610b-116">Il comando passa il nodo al cmdlet corrente usando la pipeline.</span><span class="sxs-lookup"><span data-stu-id="a610b-116">The command passes that node to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="a610b-117">Il cmdlet corrente rimuove il nodo di calcolo.</span><span class="sxs-lookup"><span data-stu-id="a610b-117">The current cmdlet removes the compute node.</span></span>
<span data-ttu-id="a610b-118">Il comando specifica il *parametro Force.*</span><span class="sxs-lookup"><span data-stu-id="a610b-118">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="a610b-119">Di conseguenza, il comando non richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="a610b-119">Therefore, the command does not prompt you for confirmation.</span></span>

### <span data-ttu-id="a610b-120">Esempio 3: Rimuovere più nodi</span><span class="sxs-lookup"><span data-stu-id="a610b-120">Example 3: Remove multiple nodes</span></span>
```
PS C:\>Remove-AzBatchComputeNode -PoolId "Pool07" @("tvm-1783593343_28-20151117t214257z","tvm-1783593343_29-20151117t214257z") -Force -BatchContext $Context
```

<span data-ttu-id="a610b-121">Questo comando rimuove due nodi di calcolo dal pool che contiene l'ID Pool07.</span><span class="sxs-lookup"><span data-stu-id="a610b-121">This command removes two compute nodes from the pool that has the ID Pool07.</span></span>
<span data-ttu-id="a610b-122">Il comando non richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="a610b-122">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="a610b-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a610b-123">PARAMETERS</span></span>

### <span data-ttu-id="a610b-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a610b-124">-BatchContext</span></span>
<span data-ttu-id="a610b-125">Specifica **l'istanza BatchAccountContext** che questo cmdlet usa per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="a610b-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a610b-126">Se si usa il cmdlet Get-AzBatchAccount per ottenere BatchAccountContext, verrà usata l'autenticazione di Azure Active Directory quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="a610b-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a610b-127">Per usare invece l'autenticazione della chiave condivisa, usare il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.</span><span class="sxs-lookup"><span data-stu-id="a610b-127">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a610b-128">Quando si usa l'autenticazione con chiave condivisa, per impostazione predefinita viene usata la chiave di accesso primario.</span><span class="sxs-lookup"><span data-stu-id="a610b-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a610b-129">Per modificare la chiave da usare, impostare la proprietà BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="a610b-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a610b-130">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="a610b-130">-ComputeNode</span></span>
<span data-ttu-id="a610b-131">Specifica **l'oggetto PSComputeNode** che rappresenta il nodo di calcolo rimosso dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a610b-131">Specifies the **PSComputeNode** object that represents the compute node that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a610b-132">-DeallocationOption</span><span class="sxs-lookup"><span data-stu-id="a610b-132">-DeallocationOption</span></span>
<span data-ttu-id="a610b-133">Specifica un'opzione di deassegnazione per l'operazione di rimozione avviata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a610b-133">Specifies a deallocation option for the removal operation that this cmdlet starts.</span></span>
<span data-ttu-id="a610b-134">Il valore predefinito è Requeue.</span><span class="sxs-lookup"><span data-stu-id="a610b-134">The default value is Requeue.</span></span>

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

### <span data-ttu-id="a610b-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a610b-135">-DefaultProfile</span></span>
<span data-ttu-id="a610b-136">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a610b-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a610b-137">-Force</span><span class="sxs-lookup"><span data-stu-id="a610b-137">-Force</span></span>
<span data-ttu-id="a610b-138">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="a610b-138">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a610b-139">-ID</span><span class="sxs-lookup"><span data-stu-id="a610b-139">-Ids</span></span>
<span data-ttu-id="a610b-140">Specifica una matrice di ID dei nodi di calcolo rimossi dal cmdlet dal pool.</span><span class="sxs-lookup"><span data-stu-id="a610b-140">Specifies an array of IDs of compute nodes that this cmdlet removes from the pool.</span></span>

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

### <span data-ttu-id="a610b-141">-PoolId</span><span class="sxs-lookup"><span data-stu-id="a610b-141">-PoolId</span></span>
<span data-ttu-id="a610b-142">Specifica l'ID del pool che contiene i nodi di calcolo rimossi dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a610b-142">Specifies the ID of the pool that contains the compute nodes that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a610b-143">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="a610b-143">-ResizeTimeout</span></span>
<span data-ttu-id="a610b-144">Specifica l'intervallo di timeout per la rimozione dei nodi di calcolo dal pool.</span><span class="sxs-lookup"><span data-stu-id="a610b-144">Specifies the time-out interval for removal of the compute nodes from the pool.</span></span>
<span data-ttu-id="a610b-145">Il valore predefinito è 10 minuti.</span><span class="sxs-lookup"><span data-stu-id="a610b-145">The default value is 10 minutes.</span></span>
<span data-ttu-id="a610b-146">Il valore minimo è 5 minuti.</span><span class="sxs-lookup"><span data-stu-id="a610b-146">The minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="a610b-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a610b-147">-Confirm</span></span>
<span data-ttu-id="a610b-148">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a610b-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a610b-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a610b-149">-WhatIf</span></span>
<span data-ttu-id="a610b-150">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a610b-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a610b-151">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a610b-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a610b-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a610b-152">CommonParameters</span></span>
<span data-ttu-id="a610b-153">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a610b-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a610b-154">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a610b-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a610b-155">INPUT</span><span class="sxs-lookup"><span data-stu-id="a610b-155">INPUTS</span></span>

### <span data-ttu-id="a610b-156">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="a610b-156">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="a610b-157">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a610b-157">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="a610b-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a610b-158">OUTPUTS</span></span>

### <span data-ttu-id="a610b-159">System.Void</span><span class="sxs-lookup"><span data-stu-id="a610b-159">System.Void</span></span>

## <span data-ttu-id="a610b-160">NOTE</span><span class="sxs-lookup"><span data-stu-id="a610b-160">NOTES</span></span>

## <span data-ttu-id="a610b-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a610b-161">RELATED LINKS</span></span>

[<span data-ttu-id="a610b-162">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="a610b-162">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="a610b-163">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="a610b-163">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="a610b-164">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="a610b-164">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)


