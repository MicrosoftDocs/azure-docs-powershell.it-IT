---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D79AEF8C-F0DC-40F8-9EEE-A2BB6AE5C4BF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchTask.md
ms.openlocfilehash: 3012abfca2ca257ad7b72fb974a8c062bfe196d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685586"
---
# <span data-ttu-id="a3214-101">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="a3214-101">Remove-AzureBatchTask</span></span>

## <span data-ttu-id="a3214-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a3214-102">SYNOPSIS</span></span>
<span data-ttu-id="a3214-103">Elimina un'attività batch.</span><span class="sxs-lookup"><span data-stu-id="a3214-103">Deletes a Batch task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3214-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a3214-104">SYNTAX</span></span>

### <span data-ttu-id="a3214-105">ID</span><span class="sxs-lookup"><span data-stu-id="a3214-105">Id</span></span>
```
Remove-AzureBatchTask [-JobId] <String> [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3214-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a3214-106">InputObject</span></span>
```
Remove-AzureBatchTask [-InputObject] <PSCloudTask> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3214-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a3214-107">DESCRIPTION</span></span>
<span data-ttu-id="a3214-108">Il cmdlet **Remove-AzureBatchTask** Elimina un'attività batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="a3214-108">The **Remove-AzureBatchTask** cmdlet deletes an Azure Batch task.</span></span>
<span data-ttu-id="a3214-109">Questo cmdlet richiede la conferma, a meno che tu non specifichi il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="a3214-109">This cmdlet prompts you for confirmation, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="a3214-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a3214-110">EXAMPLES</span></span>

### <span data-ttu-id="a3214-111">Esempio 1: eliminare un'attività batch in base all'ID</span><span class="sxs-lookup"><span data-stu-id="a3214-111">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Remove-AzureBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="a3214-112">Questo comando Elimina un'attività con ID Task23 sotto il processo con ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="a3214-112">This command deletes a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="a3214-113">Il comando richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="a3214-113">The command prompts you for confirmation.</span></span>
<span data-ttu-id="a3214-114">Usa il cmdlet **Get-AzureRmBatchAccountKeys** per assegnare un contesto alla variabile $context.</span><span class="sxs-lookup"><span data-stu-id="a3214-114">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="a3214-115">Esempio 2: eliminare un'attività batch usando la pipeline senza conferma</span><span class="sxs-lookup"><span data-stu-id="a3214-115">Example 2: Delete a Batch task by using the pipeline without confirmation</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Remove-AzureBatchTask -Force -BatchContext $Context
```

<span data-ttu-id="a3214-116">Questo comando ottiene l'attività batch che contiene l'ID Task26 nel processo con ID Job-000001 tramite il cmdlet **Get-AzureBatchTask** .</span><span class="sxs-lookup"><span data-stu-id="a3214-116">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the **Get-AzureBatchTask** cmdlet.</span></span>
<span data-ttu-id="a3214-117">Il comando passa l'attività al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="a3214-117">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a3214-118">Il comando Elimina l'attività.</span><span class="sxs-lookup"><span data-stu-id="a3214-118">The command deletes that task.</span></span>
<span data-ttu-id="a3214-119">Questo comando specifica il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="a3214-119">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="a3214-120">Di conseguenza, il comando non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="a3214-120">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="a3214-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a3214-121">PARAMETERS</span></span>

### <span data-ttu-id="a3214-122">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a3214-122">-BatchContext</span></span>
<span data-ttu-id="a3214-123">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="a3214-123">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a3214-124">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="a3214-124">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a3214-125">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="a3214-125">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a3214-126">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a3214-126">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a3214-127">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="a3214-127">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a3214-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3214-128">-DefaultProfile</span></span>
<span data-ttu-id="a3214-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a3214-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3214-130">-Force</span><span class="sxs-lookup"><span data-stu-id="a3214-130">-Force</span></span>
<span data-ttu-id="a3214-131">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a3214-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a3214-132">-ID</span><span class="sxs-lookup"><span data-stu-id="a3214-132">-Id</span></span>
<span data-ttu-id="a3214-133">Specifica l'ID dell'attività eliminata dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3214-133">Specifies the ID of the task that this cmdlet deletes.</span></span>
<span data-ttu-id="a3214-134">Non è possibile specificare caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="a3214-134">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3214-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3214-135">-InputObject</span></span>
<span data-ttu-id="a3214-136">Specifica l'attività eliminata dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3214-136">Specifies the task that this cmdlet deletes.</span></span>
<span data-ttu-id="a3214-137">Per ottenere un oggetto **PSCloudTask** , usa il cmdlet Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="a3214-137">To obtain a **PSCloudTask** object, use  the Get-AzureBatchTask cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3214-138">-JobId</span><span class="sxs-lookup"><span data-stu-id="a3214-138">-JobId</span></span>
<span data-ttu-id="a3214-139">Specifica l'ID del processo che contiene l'attività.</span><span class="sxs-lookup"><span data-stu-id="a3214-139">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3214-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a3214-140">-Confirm</span></span>
<span data-ttu-id="a3214-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3214-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3214-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3214-142">-WhatIf</span></span>
<span data-ttu-id="a3214-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a3214-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3214-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a3214-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3214-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3214-145">CommonParameters</span></span>
<span data-ttu-id="a3214-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3214-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3214-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3214-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3214-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a3214-148">INPUTS</span></span>

### <span data-ttu-id="a3214-149">System. String</span><span class="sxs-lookup"><span data-stu-id="a3214-149">System.String</span></span>

### <span data-ttu-id="a3214-150">Microsoft.Azure.Commands.Batch. Models. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="a3214-150">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>
<span data-ttu-id="a3214-151">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a3214-151">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="a3214-152">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a3214-152">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="a3214-153">Parametri: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a3214-153">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="a3214-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a3214-154">OUTPUTS</span></span>

### <span data-ttu-id="a3214-155">System. void</span><span class="sxs-lookup"><span data-stu-id="a3214-155">System.Void</span></span>

## <span data-ttu-id="a3214-156">Note</span><span class="sxs-lookup"><span data-stu-id="a3214-156">NOTES</span></span>

## <span data-ttu-id="a3214-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a3214-157">RELATED LINKS</span></span>

[<span data-ttu-id="a3214-158">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="a3214-158">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="a3214-159">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="a3214-159">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="a3214-160">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="a3214-160">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="a3214-161">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="a3214-161">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="a3214-162">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="a3214-162">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="a3214-163">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="a3214-163">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


