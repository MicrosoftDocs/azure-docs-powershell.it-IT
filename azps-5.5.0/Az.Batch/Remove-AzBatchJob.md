---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: CB2F472B-C792-4A11-A055-F4161DCFBB28
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJob.md
ms.openlocfilehash: 1b55aae98db72f7c4d4fe262329889182a189c80
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199535"
---
# <span data-ttu-id="11b30-101">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="11b30-101">Remove-AzBatchJob</span></span>

## <span data-ttu-id="11b30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11b30-102">SYNOPSIS</span></span>
<span data-ttu-id="11b30-103">Elimina un processo batch.</span><span class="sxs-lookup"><span data-stu-id="11b30-103">Deletes a Batch job.</span></span>

## <span data-ttu-id="11b30-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="11b30-104">SYNTAX</span></span>

```
Remove-AzBatchJob [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11b30-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="11b30-105">DESCRIPTION</span></span>
<span data-ttu-id="11b30-106">Il cmdlet **Remove-AzBatchJob** elimina un processo batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="11b30-106">The **Remove-AzBatchJob** cmdlet deletes an Azure Batch job.</span></span>
<span data-ttu-id="11b30-107">Questo cmdlet richiede conferma prima di rimuovere un processo, a meno che non si specifica *il parametro Force.*</span><span class="sxs-lookup"><span data-stu-id="11b30-107">This cmdlet prompts you for confirmation before it removes a job, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="11b30-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="11b30-108">EXAMPLES</span></span>

### <span data-ttu-id="11b30-109">Esempio 1: Eliminare un processo batch</span><span class="sxs-lookup"><span data-stu-id="11b30-109">Example 1: Delete a Batch job</span></span>
```
PS C:\>Remove-AzBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="11b30-110">Questo comando elimina il processo con ID Processo-000001.</span><span class="sxs-lookup"><span data-stu-id="11b30-110">This command deletes the job that has the ID Job-000001.</span></span>
<span data-ttu-id="11b30-111">Il comando chiede conferma prima di eliminare il processo.</span><span class="sxs-lookup"><span data-stu-id="11b30-111">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="11b30-112">Usare il cmdlet Get-AzBatchAccountKey per assegnare un contesto alla $Context variabile.</span><span class="sxs-lookup"><span data-stu-id="11b30-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="11b30-113">Esempio 2: Eliminare un processo batch senza conferma usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="11b30-113">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJob -Id "Job-000002" -BatchContext $Context | Remove-AzBatchJob -Force -BatchContext $Context
```

<span data-ttu-id="11b30-114">Questo comando recupera il processo con l'ID Processo-000002 usando il cmdlet Get-AzBatchJob processo.</span><span class="sxs-lookup"><span data-stu-id="11b30-114">This command gets the job that has the ID Job-000002 by using the Get-AzBatchJob cmdlet.</span></span>
<span data-ttu-id="11b30-115">Il comando passa il processo al cmdlet corrente usando l'operatore della pipeline.</span><span class="sxs-lookup"><span data-stu-id="11b30-115">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="11b30-116">Il comando elimina il processo.</span><span class="sxs-lookup"><span data-stu-id="11b30-116">The command deletes that job.</span></span>
<span data-ttu-id="11b30-117">Poiché il comando include il *parametro Force,* non richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="11b30-117">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="11b30-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11b30-118">PARAMETERS</span></span>

### <span data-ttu-id="11b30-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="11b30-119">-BatchContext</span></span>
<span data-ttu-id="11b30-120">Specifica **l'istanza BatchAccountContext** che questo cmdlet usa per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="11b30-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="11b30-121">Se si usa il cmdlet Get-AzBatchAccount per ottenere BatchAccountContext, verrà usata l'autenticazione di Azure Active Directory quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="11b30-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="11b30-122">Per usare invece l'autenticazione della chiave condivisa, usare il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.</span><span class="sxs-lookup"><span data-stu-id="11b30-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="11b30-123">Quando si usa l'autenticazione con chiave condivisa, per impostazione predefinita viene usata la chiave di accesso primario.</span><span class="sxs-lookup"><span data-stu-id="11b30-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="11b30-124">Per modificare la chiave da usare, impostare la proprietà BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="11b30-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="11b30-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11b30-125">-DefaultProfile</span></span>
<span data-ttu-id="11b30-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="11b30-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11b30-127">-Force</span><span class="sxs-lookup"><span data-stu-id="11b30-127">-Force</span></span>
<span data-ttu-id="11b30-128">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="11b30-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="11b30-129">-Id</span><span class="sxs-lookup"><span data-stu-id="11b30-129">-Id</span></span>
<span data-ttu-id="11b30-130">Specifica l'ID del processo eliminato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11b30-130">Specifies the ID of the job that this cmdlet deletes.</span></span>
<span data-ttu-id="11b30-131">Non è possibile specificare caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="11b30-131">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="11b30-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="11b30-132">-Confirm</span></span>
<span data-ttu-id="11b30-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11b30-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11b30-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11b30-134">-WhatIf</span></span>
<span data-ttu-id="11b30-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="11b30-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11b30-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="11b30-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11b30-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11b30-137">CommonParameters</span></span>
<span data-ttu-id="11b30-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11b30-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11b30-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="11b30-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11b30-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="11b30-140">INPUTS</span></span>

### <span data-ttu-id="11b30-141">System.String</span><span class="sxs-lookup"><span data-stu-id="11b30-141">System.String</span></span>

### <span data-ttu-id="11b30-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="11b30-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="11b30-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="11b30-143">OUTPUTS</span></span>

### <span data-ttu-id="11b30-144">System.Void</span><span class="sxs-lookup"><span data-stu-id="11b30-144">System.Void</span></span>

## <span data-ttu-id="11b30-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="11b30-145">NOTES</span></span>

## <span data-ttu-id="11b30-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="11b30-146">RELATED LINKS</span></span>

[<span data-ttu-id="11b30-147">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="11b30-147">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="11b30-148">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="11b30-148">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="11b30-149">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="11b30-149">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="11b30-150">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="11b30-150">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="11b30-151">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="11b30-151">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="11b30-152">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="11b30-152">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="11b30-153">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="11b30-153">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
