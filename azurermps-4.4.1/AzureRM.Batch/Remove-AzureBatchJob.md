---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: CB2F472B-C792-4A11-A055-F4161DCFBB28
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJob.md
ms.openlocfilehash: 0d210056670baa974c7bf11e9c44142c11f2721e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520129"
---
# <span data-ttu-id="98d44-101">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="98d44-101">Remove-AzureBatchJob</span></span>

## <span data-ttu-id="98d44-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="98d44-102">SYNOPSIS</span></span>
<span data-ttu-id="98d44-103">Elimina un processo batch.</span><span class="sxs-lookup"><span data-stu-id="98d44-103">Deletes a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98d44-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="98d44-104">SYNTAX</span></span>

```
Remove-AzureBatchJob [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98d44-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="98d44-105">DESCRIPTION</span></span>
<span data-ttu-id="98d44-106">Il cmdlet **Remove-AzureBatchJob** Elimina un processo batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="98d44-106">The **Remove-AzureBatchJob** cmdlet deletes an Azure Batch job.</span></span>
<span data-ttu-id="98d44-107">Questo cmdlet richiede conferma prima di rimuovere un processo, a meno che non specifichi il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="98d44-107">This cmdlet prompts you for confirmation before it removes a job, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="98d44-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="98d44-108">EXAMPLES</span></span>

### <span data-ttu-id="98d44-109">Esempio 1: eliminare un processo batch</span><span class="sxs-lookup"><span data-stu-id="98d44-109">Example 1: Delete a Batch job</span></span>
```
PS C:\>Remove-AzureBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="98d44-110">Questo comando Elimina il processo con ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="98d44-110">This command deletes the job that has the ID Job-000001.</span></span>
<span data-ttu-id="98d44-111">Il comando richiede conferma prima di eliminare il processo.</span><span class="sxs-lookup"><span data-stu-id="98d44-111">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="98d44-112">Usa il cmdlet Get-AzureRmBatchAccountKeys per assegnare un contesto alla variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="98d44-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="98d44-113">Esempio 2: eliminare una procedura batch senza conferma tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="98d44-113">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchJob -Id "Job-000002" -BatchContext $Context | Remove-AzureBatchJob -Force -BatchContext $Context
```

<span data-ttu-id="98d44-114">Questo comando ottiene il processo con l'ID Job-000002 usando il cmdlet Get-AzureBatchJob.</span><span class="sxs-lookup"><span data-stu-id="98d44-114">This command gets the job that has the ID Job-000002 by using the Get-AzureBatchJob cmdlet.</span></span>
<span data-ttu-id="98d44-115">Il comando passa il processo al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="98d44-115">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="98d44-116">Il comando Elimina il processo.</span><span class="sxs-lookup"><span data-stu-id="98d44-116">The command deletes that job.</span></span>
<span data-ttu-id="98d44-117">Poiché il comando include il parametro *Force* , non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="98d44-117">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="98d44-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="98d44-118">PARAMETERS</span></span>

### <span data-ttu-id="98d44-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="98d44-119">-BatchContext</span></span>
<span data-ttu-id="98d44-120">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="98d44-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="98d44-121">Per ottenere un oggetto **BatchAccountContext** che contiene i tasti di scelta per l'abbonamento, usare il cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="98d44-121">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="98d44-122">-Force</span><span class="sxs-lookup"><span data-stu-id="98d44-122">-Force</span></span>
<span data-ttu-id="98d44-123">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="98d44-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="98d44-124">-ID</span><span class="sxs-lookup"><span data-stu-id="98d44-124">-Id</span></span>
<span data-ttu-id="98d44-125">Specifica l'ID del processo eliminato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98d44-125">Specifies the ID of the job that this cmdlet deletes.</span></span>
<span data-ttu-id="98d44-126">Non è possibile specificare caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="98d44-126">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="98d44-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="98d44-127">-Confirm</span></span>
<span data-ttu-id="98d44-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98d44-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98d44-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98d44-129">-WhatIf</span></span>
<span data-ttu-id="98d44-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="98d44-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98d44-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="98d44-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98d44-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98d44-132">-DefaultProfile</span></span>
<span data-ttu-id="98d44-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="98d44-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98d44-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98d44-134">CommonParameters</span></span>
<span data-ttu-id="98d44-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98d44-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98d44-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98d44-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98d44-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="98d44-137">INPUTS</span></span>

### <span data-ttu-id="98d44-138">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="98d44-138">BatchAccountContext</span></span>
<span data-ttu-id="98d44-139">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="98d44-139">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="98d44-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="98d44-140">OUTPUTS</span></span>

## <span data-ttu-id="98d44-141">Note</span><span class="sxs-lookup"><span data-stu-id="98d44-141">NOTES</span></span>

## <span data-ttu-id="98d44-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="98d44-142">RELATED LINKS</span></span>

[<span data-ttu-id="98d44-143">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="98d44-143">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="98d44-144">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="98d44-144">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="98d44-145">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="98d44-145">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="98d44-146">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="98d44-146">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="98d44-147">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="98d44-147">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="98d44-148">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="98d44-148">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="98d44-149">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="98d44-149">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


