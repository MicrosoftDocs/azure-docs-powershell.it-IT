---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9E423A10-06AF-42F8-AC90-82DB01012AFA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNodeUser.md
ms.openlocfilehash: 52fea755708645173a5f0f3429591a384ec63b01
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200533"
---
# <span data-ttu-id="4ea46-101">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="4ea46-101">Remove-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="4ea46-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4ea46-102">SYNOPSIS</span></span>
<span data-ttu-id="4ea46-103">Elimina un account utente da un nodo di calcolo batch.</span><span class="sxs-lookup"><span data-stu-id="4ea46-103">Deletes a user account from a Batch compute node.</span></span>

## <span data-ttu-id="4ea46-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4ea46-104">SYNTAX</span></span>

```
Remove-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4ea46-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4ea46-105">DESCRIPTION</span></span>
<span data-ttu-id="4ea46-106">Il cmdlet **Remove-AzBatchComputeNodeUser** Elimina un account utente da un nodo di calcolo batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="4ea46-106">The **Remove-AzBatchComputeNodeUser** cmdlet deletes a user account from an Azure Batch compute node.</span></span>

## <span data-ttu-id="4ea46-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4ea46-107">EXAMPLES</span></span>

### <span data-ttu-id="4ea46-108">Esempio 1: eliminare un utente da un nodo Compute senza conferma</span><span class="sxs-lookup"><span data-stu-id="4ea46-108">Example 1: Delete a user from a compute node without confirmation</span></span>
```
PS C:\>Remove-AzBatchComputeNodeUser -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "User14" -Force -BatchContext $Context
```

<span data-ttu-id="4ea46-109">Questo comando Elimina l'utente denominato User14 dal nodo Compute denominato ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="4ea46-109">This command deletes the user named User14 from compute node named ComputeNode01.</span></span>
<span data-ttu-id="4ea46-110">Il nodo Compute si trova nel pool denominato pool01.</span><span class="sxs-lookup"><span data-stu-id="4ea46-110">The compute node is in the pool named Pool01.</span></span>
<span data-ttu-id="4ea46-111">Questo comando specifica il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="4ea46-111">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="4ea46-112">Di conseguenza, il comando non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="4ea46-112">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="4ea46-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4ea46-113">PARAMETERS</span></span>

### <span data-ttu-id="4ea46-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="4ea46-114">-BatchContext</span></span>
<span data-ttu-id="4ea46-115">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="4ea46-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="4ea46-116">Se si usa il cmdlet Get-AzBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="4ea46-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="4ea46-117">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="4ea46-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="4ea46-118">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="4ea46-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="4ea46-119">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="4ea46-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="4ea46-120">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="4ea46-120">-ComputeNodeId</span></span>
<span data-ttu-id="4ea46-121">Specifica l'ID del nodo COMPUTE in cui questo cmdlet elimina l'account utente.</span><span class="sxs-lookup"><span data-stu-id="4ea46-121">Specifies the ID of the compute node on which this cmdlet deletes the user account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ea46-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ea46-122">-DefaultProfile</span></span>
<span data-ttu-id="4ea46-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4ea46-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ea46-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="4ea46-124">-Name</span></span>
<span data-ttu-id="4ea46-125">Specifica il nome dell'account utente da eliminare.</span><span class="sxs-lookup"><span data-stu-id="4ea46-125">Specifies the name of the user account to delete.</span></span>
<span data-ttu-id="4ea46-126">Non è possibile specificare caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="4ea46-126">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ea46-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="4ea46-127">-PoolId</span></span>
<span data-ttu-id="4ea46-128">Specifica l'ID del pool che contiene il nodo COMPUTE in cui eliminare l'account utente.</span><span class="sxs-lookup"><span data-stu-id="4ea46-128">Specifies the ID of the pool that contains the compute node on which to delete the user account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ea46-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4ea46-129">-Confirm</span></span>
<span data-ttu-id="4ea46-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ea46-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ea46-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ea46-131">-WhatIf</span></span>
<span data-ttu-id="4ea46-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4ea46-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ea46-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4ea46-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ea46-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ea46-134">CommonParameters</span></span>
<span data-ttu-id="4ea46-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ea46-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ea46-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4ea46-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ea46-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4ea46-137">INPUTS</span></span>

### <span data-ttu-id="4ea46-138">System. String</span><span class="sxs-lookup"><span data-stu-id="4ea46-138">System.String</span></span>

### <span data-ttu-id="4ea46-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4ea46-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="4ea46-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4ea46-140">OUTPUTS</span></span>

### <span data-ttu-id="4ea46-141">System. void</span><span class="sxs-lookup"><span data-stu-id="4ea46-141">System.Void</span></span>

## <span data-ttu-id="4ea46-142">Note</span><span class="sxs-lookup"><span data-stu-id="4ea46-142">NOTES</span></span>

## <span data-ttu-id="4ea46-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4ea46-143">RELATED LINKS</span></span>

[<span data-ttu-id="4ea46-144">New-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="4ea46-144">New-AzBatchComputeNodeUser</span></span>](./New-AzBatchComputeNodeUser.md)

[<span data-ttu-id="4ea46-145">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="4ea46-145">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="4ea46-146">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="4ea46-146">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
