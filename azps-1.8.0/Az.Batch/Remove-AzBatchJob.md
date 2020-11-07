---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: CB2F472B-C792-4A11-A055-F4161DCFBB28
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJob.md
ms.openlocfilehash: 4d15680902cb324561983877fef317d20ed94704
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2020
ms.locfileid: "93685300"
---
# <span data-ttu-id="b39d4-101">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="b39d4-101">Remove-AzBatchJob</span></span>

## <span data-ttu-id="b39d4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b39d4-102">SYNOPSIS</span></span>
<span data-ttu-id="b39d4-103">Elimina un processo batch.</span><span class="sxs-lookup"><span data-stu-id="b39d4-103">Deletes a Batch job.</span></span>

## <span data-ttu-id="b39d4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b39d4-104">SYNTAX</span></span>

```
Remove-AzBatchJob [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b39d4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b39d4-105">DESCRIPTION</span></span>
<span data-ttu-id="b39d4-106">Il cmdlet **Remove-AzBatchJob** Elimina un processo batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="b39d4-106">The **Remove-AzBatchJob** cmdlet deletes an Azure Batch job.</span></span>
<span data-ttu-id="b39d4-107">Questo cmdlet richiede conferma prima di rimuovere un processo, a meno che non specifichi il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="b39d4-107">This cmdlet prompts you for confirmation before it removes a job, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="b39d4-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b39d4-108">EXAMPLES</span></span>

### <span data-ttu-id="b39d4-109">Esempio 1: eliminare un processo batch</span><span class="sxs-lookup"><span data-stu-id="b39d4-109">Example 1: Delete a Batch job</span></span>
```
PS C:\>Remove-AzBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="b39d4-110">Questo comando Elimina il processo con ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="b39d4-110">This command deletes the job that has the ID Job-000001.</span></span>
<span data-ttu-id="b39d4-111">Il comando richiede conferma prima di eliminare il processo.</span><span class="sxs-lookup"><span data-stu-id="b39d4-111">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="b39d4-112">Usa il cmdlet Get-AzBatchAccountKeys per assegnare un contesto alla variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="b39d4-112">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="b39d4-113">Esempio 2: eliminare una procedura batch senza conferma tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="b39d4-113">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJob -Id "Job-000002" -BatchContext $Context | Remove-AzBatchJob -Force -BatchContext $Context
```

<span data-ttu-id="b39d4-114">Questo comando ottiene il processo con l'ID Job-000002 usando il cmdlet Get-AzBatchJob.</span><span class="sxs-lookup"><span data-stu-id="b39d4-114">This command gets the job that has the ID Job-000002 by using the Get-AzBatchJob cmdlet.</span></span>
<span data-ttu-id="b39d4-115">Il comando passa il processo al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="b39d4-115">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b39d4-116">Il comando Elimina il processo.</span><span class="sxs-lookup"><span data-stu-id="b39d4-116">The command deletes that job.</span></span>
<span data-ttu-id="b39d4-117">Poiché il comando include il parametro *Force* , non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="b39d4-117">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="b39d4-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b39d4-118">PARAMETERS</span></span>

### <span data-ttu-id="b39d4-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b39d4-119">-BatchContext</span></span>
<span data-ttu-id="b39d4-120">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="b39d4-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b39d4-121">Se si usa il cmdlet Get-AzBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="b39d4-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b39d4-122">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="b39d4-122">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b39d4-123">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="b39d4-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b39d4-124">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="b39d4-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b39d4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b39d4-125">-DefaultProfile</span></span>
<span data-ttu-id="b39d4-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b39d4-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b39d4-127">-Force</span><span class="sxs-lookup"><span data-stu-id="b39d4-127">-Force</span></span>
<span data-ttu-id="b39d4-128">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b39d4-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b39d4-129">-ID</span><span class="sxs-lookup"><span data-stu-id="b39d4-129">-Id</span></span>
<span data-ttu-id="b39d4-130">Specifica l'ID del processo eliminato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b39d4-130">Specifies the ID of the job that this cmdlet deletes.</span></span>
<span data-ttu-id="b39d4-131">Non è possibile specificare caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="b39d4-131">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="b39d4-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b39d4-132">-Confirm</span></span>
<span data-ttu-id="b39d4-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b39d4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b39d4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b39d4-134">-WhatIf</span></span>
<span data-ttu-id="b39d4-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b39d4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b39d4-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b39d4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b39d4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b39d4-137">CommonParameters</span></span>
<span data-ttu-id="b39d4-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b39d4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b39d4-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b39d4-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b39d4-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b39d4-140">INPUTS</span></span>

### <span data-ttu-id="b39d4-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b39d4-141">System.String</span></span>

### <span data-ttu-id="b39d4-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b39d4-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="b39d4-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b39d4-143">OUTPUTS</span></span>

### <span data-ttu-id="b39d4-144">System. void</span><span class="sxs-lookup"><span data-stu-id="b39d4-144">System.Void</span></span>

## <span data-ttu-id="b39d4-145">Note</span><span class="sxs-lookup"><span data-stu-id="b39d4-145">NOTES</span></span>

## <span data-ttu-id="b39d4-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b39d4-146">RELATED LINKS</span></span>

[<span data-ttu-id="b39d4-147">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="b39d4-147">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="b39d4-148">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="b39d4-148">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="b39d4-149">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="b39d4-149">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="b39d4-150">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b39d4-150">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="b39d4-151">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="b39d4-151">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="b39d4-152">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="b39d4-152">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="b39d4-153">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="b39d4-153">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


