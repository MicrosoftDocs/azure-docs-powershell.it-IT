---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: CB2F472B-C792-4A11-A055-F4161DCFBB28
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJob.md
ms.openlocfilehash: f6a7d03370184b45cc8066e2f17842187cbab98c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521105"
---
# <span data-ttu-id="c6266-101">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="c6266-101">Remove-AzureBatchJob</span></span>

## <span data-ttu-id="c6266-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c6266-102">SYNOPSIS</span></span>
<span data-ttu-id="c6266-103">Elimina un processo batch.</span><span class="sxs-lookup"><span data-stu-id="c6266-103">Deletes a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6266-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c6266-104">SYNTAX</span></span>

```
Remove-AzureBatchJob [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6266-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c6266-105">DESCRIPTION</span></span>
<span data-ttu-id="c6266-106">Il cmdlet **Remove-AzureBatchJob** Elimina un processo batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="c6266-106">The **Remove-AzureBatchJob** cmdlet deletes an Azure Batch job.</span></span>
<span data-ttu-id="c6266-107">Questo cmdlet richiede conferma prima di rimuovere un processo, a meno che non specifichi il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="c6266-107">This cmdlet prompts you for confirmation before it removes a job, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="c6266-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c6266-108">EXAMPLES</span></span>

### <span data-ttu-id="c6266-109">Esempio 1: eliminare un processo batch</span><span class="sxs-lookup"><span data-stu-id="c6266-109">Example 1: Delete a Batch job</span></span>
```
PS C:\>Remove-AzureBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="c6266-110">Questo comando Elimina il processo con ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="c6266-110">This command deletes the job that has the ID Job-000001.</span></span>
<span data-ttu-id="c6266-111">Il comando richiede conferma prima di eliminare il processo.</span><span class="sxs-lookup"><span data-stu-id="c6266-111">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="c6266-112">Usa il cmdlet Get-AzureRmBatchAccountKeys per assegnare un contesto alla variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="c6266-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="c6266-113">Esempio 2: eliminare una procedura batch senza conferma tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="c6266-113">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchJob -Id "Job-000002" -BatchContext $Context | Remove-AzureBatchJob -Force -BatchContext $Context
```

<span data-ttu-id="c6266-114">Questo comando ottiene il processo con l'ID Job-000002 usando il cmdlet Get-AzureBatchJob.</span><span class="sxs-lookup"><span data-stu-id="c6266-114">This command gets the job that has the ID Job-000002 by using the Get-AzureBatchJob cmdlet.</span></span>
<span data-ttu-id="c6266-115">Il comando passa il processo al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="c6266-115">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c6266-116">Il comando Elimina il processo.</span><span class="sxs-lookup"><span data-stu-id="c6266-116">The command deletes that job.</span></span>
<span data-ttu-id="c6266-117">Poiché il comando include il parametro *Force* , non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="c6266-117">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="c6266-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c6266-118">PARAMETERS</span></span>

### <span data-ttu-id="c6266-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c6266-119">-BatchContext</span></span>
<span data-ttu-id="c6266-120">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="c6266-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c6266-121">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="c6266-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c6266-122">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="c6266-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c6266-123">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="c6266-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c6266-124">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="c6266-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6266-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6266-125">-DefaultProfile</span></span>
<span data-ttu-id="c6266-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c6266-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6266-127">-Force</span><span class="sxs-lookup"><span data-stu-id="c6266-127">-Force</span></span>
<span data-ttu-id="c6266-128">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c6266-128">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6266-129">-ID</span><span class="sxs-lookup"><span data-stu-id="c6266-129">-Id</span></span>
<span data-ttu-id="c6266-130">Specifica l'ID del processo eliminato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6266-130">Specifies the ID of the job that this cmdlet deletes.</span></span>
<span data-ttu-id="c6266-131">Non è possibile specificare caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="c6266-131">You cannot specify wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6266-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c6266-132">-Confirm</span></span>
<span data-ttu-id="c6266-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6266-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6266-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6266-134">-WhatIf</span></span>
<span data-ttu-id="c6266-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c6266-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6266-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c6266-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6266-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6266-137">CommonParameters</span></span>
<span data-ttu-id="c6266-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6266-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6266-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6266-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6266-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c6266-140">INPUTS</span></span>

### <span data-ttu-id="c6266-141">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c6266-141">BatchAccountContext</span></span>
<span data-ttu-id="c6266-142">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="c6266-142">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="c6266-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c6266-143">OUTPUTS</span></span>

## <span data-ttu-id="c6266-144">Note</span><span class="sxs-lookup"><span data-stu-id="c6266-144">NOTES</span></span>

## <span data-ttu-id="c6266-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c6266-145">RELATED LINKS</span></span>

[<span data-ttu-id="c6266-146">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="c6266-146">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="c6266-147">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="c6266-147">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="c6266-148">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="c6266-148">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="c6266-149">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c6266-149">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="c6266-150">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="c6266-150">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="c6266-151">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="c6266-151">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="c6266-152">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="c6266-152">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


