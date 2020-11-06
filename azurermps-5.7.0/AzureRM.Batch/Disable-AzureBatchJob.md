---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C831F934-7513-4882-A155-816E56CD9807
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/disable-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJob.md
ms.openlocfilehash: fcb3586d1c27fd95c6bf386943830b92635162e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93522058"
---
# <span data-ttu-id="1c5f1-101">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="1c5f1-101">Disable-AzureBatchJob</span></span>

## <span data-ttu-id="1c5f1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1c5f1-102">SYNOPSIS</span></span>
<span data-ttu-id="1c5f1-103">Disabilita un processo batch.</span><span class="sxs-lookup"><span data-stu-id="1c5f1-103">Disables a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c5f1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1c5f1-104">SYNTAX</span></span>

```
Disable-AzureBatchJob [-Id] <String> [-DisableJobOption] <DisableJobOption> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c5f1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1c5f1-105">DESCRIPTION</span></span>
<span data-ttu-id="1c5f1-106">Il cmdlet **Disable-AzureBatchJob Disabilita** un processo batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="1c5f1-106">The **Disable-AzureBatchJob** cmdlet disables an Azure Batch job.</span></span>
<span data-ttu-id="1c5f1-107">Dopo l'abilitazione di un processo, le nuove attività possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="1c5f1-107">After you enable a job, new tasks can run.</span></span>
<span data-ttu-id="1c5f1-108">I processi disabilitati non eseguono nuove attività.</span><span class="sxs-lookup"><span data-stu-id="1c5f1-108">Disabled jobs do not run new tasks.</span></span>
<span data-ttu-id="1c5f1-109">È possibile abilitare un processo disabilitato in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="1c5f1-109">You can enable a disabled job later.</span></span>

## <span data-ttu-id="1c5f1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1c5f1-110">EXAMPLES</span></span>

### <span data-ttu-id="1c5f1-111">Esempio 1: disabilitare un processo batch</span><span class="sxs-lookup"><span data-stu-id="1c5f1-111">Example 1: Disable a Batch job</span></span>
```
PS C:\>Disable-AzureBatchJob -Id "Job-000001" -DisableJobOption "Terminate" -BatchContext $Context
```

<span data-ttu-id="1c5f1-112">Questo comando Disabilita il processo con ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="1c5f1-112">This command disables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="1c5f1-113">Il comando termina le attività attive per il processo.</span><span class="sxs-lookup"><span data-stu-id="1c5f1-113">The command terminates active tasks for the job.</span></span>
<span data-ttu-id="1c5f1-114">Usa il cmdlet **Get-AzureRmBatchAccountKeys** per assegnare un contesto alla variabile $context.</span><span class="sxs-lookup"><span data-stu-id="1c5f1-114">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="1c5f1-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1c5f1-115">PARAMETERS</span></span>

### <span data-ttu-id="1c5f1-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="1c5f1-116">-BatchContext</span></span>
<span data-ttu-id="1c5f1-117">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="1c5f1-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="1c5f1-118">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="1c5f1-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="1c5f1-119">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="1c5f1-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="1c5f1-120">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="1c5f1-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="1c5f1-121">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="1c5f1-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="1c5f1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c5f1-122">-DefaultProfile</span></span>
<span data-ttu-id="1c5f1-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1c5f1-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c5f1-124">-DisableJobOption</span><span class="sxs-lookup"><span data-stu-id="1c5f1-124">-DisableJobOption</span></span>
<span data-ttu-id="1c5f1-125">Specifica le operazioni da eseguire con le attività attive associate al processo disabilitato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c5f1-125">Specifies what to do with active tasks associated with the job that this cmdlet disables.</span></span>
<span data-ttu-id="1c5f1-126">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="1c5f1-126">Valid values are:</span></span> 

- <span data-ttu-id="1c5f1-127">Riaccodare</span><span class="sxs-lookup"><span data-stu-id="1c5f1-127">Requeue</span></span> 
- <span data-ttu-id="1c5f1-128">Terminare</span><span class="sxs-lookup"><span data-stu-id="1c5f1-128">Terminate</span></span> 
- <span data-ttu-id="1c5f1-129">Attendere</span><span class="sxs-lookup"><span data-stu-id="1c5f1-129">Wait</span></span>

```yaml
Type: DisableJobOption
Parameter Sets: (All)
Aliases: 
Accepted values: Requeue, Terminate, Wait

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c5f1-130">-ID</span><span class="sxs-lookup"><span data-stu-id="1c5f1-130">-Id</span></span>
<span data-ttu-id="1c5f1-131">Specifica l'ID del processo disabilitato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c5f1-131">Specifies the ID of the job that this cmdlet disables.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c5f1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c5f1-132">CommonParameters</span></span>
<span data-ttu-id="1c5f1-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c5f1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c5f1-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c5f1-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c5f1-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1c5f1-135">INPUTS</span></span>

### <span data-ttu-id="1c5f1-136">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="1c5f1-136">BatchAccountContext</span></span>
<span data-ttu-id="1c5f1-137">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="1c5f1-137">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="1c5f1-138">Stringa</span><span class="sxs-lookup"><span data-stu-id="1c5f1-138">String</span></span>
<span data-ttu-id="1c5f1-139">Il parametro "ID" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="1c5f1-139">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="1c5f1-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1c5f1-140">OUTPUTS</span></span>

## <span data-ttu-id="1c5f1-141">Note</span><span class="sxs-lookup"><span data-stu-id="1c5f1-141">NOTES</span></span>

## <span data-ttu-id="1c5f1-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1c5f1-142">RELATED LINKS</span></span>

[<span data-ttu-id="1c5f1-143">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="1c5f1-143">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="1c5f1-144">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="1c5f1-144">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="1c5f1-145">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="1c5f1-145">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="1c5f1-146">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="1c5f1-146">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="1c5f1-147">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="1c5f1-147">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="1c5f1-148">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="1c5f1-148">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="1c5f1-149">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="1c5f1-149">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


