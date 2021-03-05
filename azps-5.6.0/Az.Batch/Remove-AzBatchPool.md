---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DB0A8E4B-AD3F-4BAC-A0B2-031913E019D4
online version: https://docs.microsoft.com/powershell/module/az.batch/remove-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchPool.md
ms.openlocfilehash: 6dd5082485d8028a0f1593db9c84bdc571b8c6bf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998967"
---
# <span data-ttu-id="91025-101">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="91025-101">Remove-AzBatchPool</span></span>

## <span data-ttu-id="91025-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91025-102">SYNOPSIS</span></span>
<span data-ttu-id="91025-103">Elimina il pool batch specificato.</span><span class="sxs-lookup"><span data-stu-id="91025-103">Deletes the specified Batch pool.</span></span>

## <span data-ttu-id="91025-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="91025-104">SYNTAX</span></span>

```
Remove-AzBatchPool [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91025-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="91025-105">DESCRIPTION</span></span>
<span data-ttu-id="91025-106">Il cmdlet **Remove-AzBatchPool** elimina il pool batch di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="91025-106">The **Remove-AzBatchPool** cmdlet deletes the specified Azure Batch pool.</span></span>
<span data-ttu-id="91025-107">Viene richiesta una conferma, a meno che non si usi il *parametro Force.*</span><span class="sxs-lookup"><span data-stu-id="91025-107">You are prompted for confirmation unless you use the *Force* parameter.</span></span>

## <span data-ttu-id="91025-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="91025-108">EXAMPLES</span></span>

### <span data-ttu-id="91025-109">Esempio 1: Eliminare un pool batch in base all'ID pool</span><span class="sxs-lookup"><span data-stu-id="91025-109">Example 1: Delete a Batch pool by pool ID</span></span>
```
PS C:\>Remove-AzBatchPool -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="91025-110">Questo comando elimina il pool con ID MyPool.</span><span class="sxs-lookup"><span data-stu-id="91025-110">This command deletes the pool with ID MyPool.</span></span>
<span data-ttu-id="91025-111">All'utente viene chiesto di confermare l'esecuzione dell'operazione di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="91025-111">The user is prompted for confirmation before the delete operation takes place.</span></span>

### <span data-ttu-id="91025-112">Esempio 2: Eliminare tutti i pool di batch forzati</span><span class="sxs-lookup"><span data-stu-id="91025-112">Example 2: Delete all Batch pools by force</span></span>
```
PS C:\>Get-AzBatchPool -BatchContext $Context | Remove-AzBatchPool -Force -BatchContext $Context
```

<span data-ttu-id="91025-113">Questo comando elimina tutti i pool di batch.</span><span class="sxs-lookup"><span data-stu-id="91025-113">This command deletes all Batch pools.</span></span>
<span data-ttu-id="91025-114">Poiché il *parametro Force* è presente, la richiesta di conferma viene eliminata.</span><span class="sxs-lookup"><span data-stu-id="91025-114">Because the *Force* parameter is present, the confirmation prompt is suppressed.</span></span>

## <span data-ttu-id="91025-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91025-115">PARAMETERS</span></span>

### <span data-ttu-id="91025-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="91025-116">-BatchContext</span></span>
<span data-ttu-id="91025-117">Specifica **l'istanza BatchAccountContext** che questo cmdlet usa per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="91025-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="91025-118">Se si usa il cmdlet Get-AzBatchAccount per ottenere BatchAccountContext, verrà usata l'autenticazione di Azure Active Directory quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="91025-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="91025-119">Per usare invece l'autenticazione della chiave condivisa, usare il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.</span><span class="sxs-lookup"><span data-stu-id="91025-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="91025-120">Quando si usa l'autenticazione con chiave condivisa, per impostazione predefinita viene usata la chiave di accesso primario.</span><span class="sxs-lookup"><span data-stu-id="91025-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="91025-121">Per modificare la chiave da usare, impostare la proprietà BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="91025-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="91025-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91025-122">-DefaultProfile</span></span>
<span data-ttu-id="91025-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="91025-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91025-124">-Force</span><span class="sxs-lookup"><span data-stu-id="91025-124">-Force</span></span>
<span data-ttu-id="91025-125">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="91025-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="91025-126">-Id</span><span class="sxs-lookup"><span data-stu-id="91025-126">-Id</span></span>
<span data-ttu-id="91025-127">Specifica l'ID del pool da eliminare.</span><span class="sxs-lookup"><span data-stu-id="91025-127">Specifies the ID of the pool to delete.</span></span>
<span data-ttu-id="91025-128">Non è possibile specificare caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="91025-128">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="91025-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="91025-129">-Confirm</span></span>
<span data-ttu-id="91025-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91025-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91025-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91025-131">-WhatIf</span></span>
<span data-ttu-id="91025-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="91025-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91025-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="91025-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91025-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91025-134">CommonParameters</span></span>
<span data-ttu-id="91025-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91025-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91025-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="91025-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91025-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="91025-137">INPUTS</span></span>

### <span data-ttu-id="91025-138">System.String</span><span class="sxs-lookup"><span data-stu-id="91025-138">System.String</span></span>

### <span data-ttu-id="91025-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="91025-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="91025-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="91025-140">OUTPUTS</span></span>

### <span data-ttu-id="91025-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="91025-141">System.Void</span></span>

## <span data-ttu-id="91025-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="91025-142">NOTES</span></span>

## <span data-ttu-id="91025-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="91025-143">RELATED LINKS</span></span>

[<span data-ttu-id="91025-144">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="91025-144">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="91025-145">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="91025-145">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="91025-146">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="91025-146">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="91025-147">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="91025-147">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
