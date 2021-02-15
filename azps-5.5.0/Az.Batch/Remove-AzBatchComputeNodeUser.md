---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9E423A10-06AF-42F8-AC90-82DB01012AFA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNodeUser.md
ms.openlocfilehash: 52fea755708645173a5f0f3429591a384ec63b01
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197006"
---
# <span data-ttu-id="86f77-101">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="86f77-101">Remove-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="86f77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86f77-102">SYNOPSIS</span></span>
<span data-ttu-id="86f77-103">Elimina un account utente da un nodo di elaborazione batch.</span><span class="sxs-lookup"><span data-stu-id="86f77-103">Deletes a user account from a Batch compute node.</span></span>

## <span data-ttu-id="86f77-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="86f77-104">SYNTAX</span></span>

```
Remove-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="86f77-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="86f77-105">DESCRIPTION</span></span>
<span data-ttu-id="86f77-106">Il cmdlet **Remove-AzBatchComputeNodeUser** elimina un account utente da un nodo di elaborazione batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="86f77-106">The **Remove-AzBatchComputeNodeUser** cmdlet deletes a user account from an Azure Batch compute node.</span></span>

## <span data-ttu-id="86f77-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="86f77-107">EXAMPLES</span></span>

### <span data-ttu-id="86f77-108">Esempio 1: Eliminare un utente da un nodo di elaborazione senza conferma</span><span class="sxs-lookup"><span data-stu-id="86f77-108">Example 1: Delete a user from a compute node without confirmation</span></span>
```
PS C:\>Remove-AzBatchComputeNodeUser -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "User14" -Force -BatchContext $Context
```

<span data-ttu-id="86f77-109">Questo comando elimina l'utente denominato User14 dal nodo di elaborazione denominato ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="86f77-109">This command deletes the user named User14 from compute node named ComputeNode01.</span></span>
<span data-ttu-id="86f77-110">Il nodo di calcolo si trova nel pool denominato Pool01.</span><span class="sxs-lookup"><span data-stu-id="86f77-110">The compute node is in the pool named Pool01.</span></span>
<span data-ttu-id="86f77-111">Questo comando specifica il *parametro Force.*</span><span class="sxs-lookup"><span data-stu-id="86f77-111">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="86f77-112">Di conseguenza, il comando non richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="86f77-112">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="86f77-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86f77-113">PARAMETERS</span></span>

### <span data-ttu-id="86f77-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="86f77-114">-BatchContext</span></span>
<span data-ttu-id="86f77-115">Specifica **l'istanza BatchAccountContext** che questo cmdlet usa per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="86f77-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="86f77-116">Se si usa il cmdlet Get-AzBatchAccount per ottenere BatchAccountContext, verrà usata l'autenticazione di Azure Active Directory quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="86f77-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="86f77-117">Per usare invece l'autenticazione della chiave condivisa, usare il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.</span><span class="sxs-lookup"><span data-stu-id="86f77-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="86f77-118">Quando si usa l'autenticazione con chiave condivisa, per impostazione predefinita viene usata la chiave di accesso primario.</span><span class="sxs-lookup"><span data-stu-id="86f77-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="86f77-119">Per modificare la chiave da usare, impostare la proprietà BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="86f77-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="86f77-120">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="86f77-120">-ComputeNodeId</span></span>
<span data-ttu-id="86f77-121">Specifica l'ID del nodo di calcolo in cui questo cmdlet elimina l'account utente.</span><span class="sxs-lookup"><span data-stu-id="86f77-121">Specifies the ID of the compute node on which this cmdlet deletes the user account.</span></span>

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

### <span data-ttu-id="86f77-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86f77-122">-DefaultProfile</span></span>
<span data-ttu-id="86f77-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="86f77-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86f77-124">-Name</span><span class="sxs-lookup"><span data-stu-id="86f77-124">-Name</span></span>
<span data-ttu-id="86f77-125">Specifica il nome dell'account utente da eliminare.</span><span class="sxs-lookup"><span data-stu-id="86f77-125">Specifies the name of the user account to delete.</span></span>
<span data-ttu-id="86f77-126">Non è possibile specificare caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="86f77-126">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="86f77-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="86f77-127">-PoolId</span></span>
<span data-ttu-id="86f77-128">Specifica l'ID del pool che contiene il nodo di calcolo in cui eliminare l'account utente.</span><span class="sxs-lookup"><span data-stu-id="86f77-128">Specifies the ID of the pool that contains the compute node on which to delete the user account.</span></span>

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

### <span data-ttu-id="86f77-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="86f77-129">-Confirm</span></span>
<span data-ttu-id="86f77-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86f77-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86f77-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86f77-131">-WhatIf</span></span>
<span data-ttu-id="86f77-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="86f77-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86f77-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="86f77-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86f77-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86f77-134">CommonParameters</span></span>
<span data-ttu-id="86f77-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86f77-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86f77-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="86f77-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86f77-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="86f77-137">INPUTS</span></span>

### <span data-ttu-id="86f77-138">System.String</span><span class="sxs-lookup"><span data-stu-id="86f77-138">System.String</span></span>

### <span data-ttu-id="86f77-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="86f77-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="86f77-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="86f77-140">OUTPUTS</span></span>

### <span data-ttu-id="86f77-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="86f77-141">System.Void</span></span>

## <span data-ttu-id="86f77-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="86f77-142">NOTES</span></span>

## <span data-ttu-id="86f77-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="86f77-143">RELATED LINKS</span></span>

[<span data-ttu-id="86f77-144">New-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="86f77-144">New-AzBatchComputeNodeUser</span></span>](./New-AzBatchComputeNodeUser.md)

[<span data-ttu-id="86f77-145">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="86f77-145">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="86f77-146">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="86f77-146">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
