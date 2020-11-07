---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C831F934-7513-4882-A155-816E56CD9807
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJob.md
ms.openlocfilehash: 2e19e6b1733ccc3dfe0a802756e2c0a517232803
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688368"
---
# <span data-ttu-id="71435-101">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="71435-101">Disable-AzureBatchJob</span></span>

## <span data-ttu-id="71435-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="71435-102">SYNOPSIS</span></span>
<span data-ttu-id="71435-103">Disabilita un processo batch.</span><span class="sxs-lookup"><span data-stu-id="71435-103">Disables a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71435-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="71435-104">SYNTAX</span></span>

```
Disable-AzureBatchJob [-Id] <String> [-DisableJobOption] <DisableJobOption> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71435-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71435-105">DESCRIPTION</span></span>
<span data-ttu-id="71435-106">Il cmdlet **Disable-AzureBatchJob Disabilita** un processo batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="71435-106">The **Disable-AzureBatchJob** cmdlet disables an Azure Batch job.</span></span>
<span data-ttu-id="71435-107">Dopo l'abilitazione di un processo, le nuove attività possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="71435-107">After you enable a job, new tasks can run.</span></span>
<span data-ttu-id="71435-108">I processi disabilitati non eseguono nuove attività.</span><span class="sxs-lookup"><span data-stu-id="71435-108">Disabled jobs do not run new tasks.</span></span>
<span data-ttu-id="71435-109">È possibile abilitare un processo disabilitato in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="71435-109">You can enable a disabled job later.</span></span>

## <span data-ttu-id="71435-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="71435-110">EXAMPLES</span></span>

### <span data-ttu-id="71435-111">Esempio 1: disabilitare un processo batch</span><span class="sxs-lookup"><span data-stu-id="71435-111">Example 1: Disable a Batch job</span></span>
```
PS C:\>Disable-AzureBatchJob -Id "Job-000001" -DisableJobOption "Terminate" -BatchContext $Context
```

<span data-ttu-id="71435-112">Questo comando Disabilita il processo con ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="71435-112">This command disables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="71435-113">Il comando termina le attività attive per il processo.</span><span class="sxs-lookup"><span data-stu-id="71435-113">The command terminates active tasks for the job.</span></span>
<span data-ttu-id="71435-114">Usa il cmdlet **Get-AzureRmBatchAccountKeys** per assegnare un contesto alla variabile $context.</span><span class="sxs-lookup"><span data-stu-id="71435-114">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="71435-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="71435-115">PARAMETERS</span></span>

### <span data-ttu-id="71435-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="71435-116">-BatchContext</span></span>
<span data-ttu-id="71435-117">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="71435-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="71435-118">Per ottenere un oggetto **BatchAccountContext** che contiene i tasti di scelta per l'abbonamento, usare il cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="71435-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="71435-119">-DisableJobOption</span><span class="sxs-lookup"><span data-stu-id="71435-119">-DisableJobOption</span></span>
<span data-ttu-id="71435-120">Specifica le operazioni da eseguire con le attività attive associate al processo disabilitato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71435-120">Specifies what to do with active tasks associated with the job that this cmdlet disables.</span></span>
<span data-ttu-id="71435-121">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="71435-121">Valid values are:</span></span> 

- <span data-ttu-id="71435-122">Riaccodare</span><span class="sxs-lookup"><span data-stu-id="71435-122">Requeue</span></span> 
- <span data-ttu-id="71435-123">Terminare</span><span class="sxs-lookup"><span data-stu-id="71435-123">Terminate</span></span> 
- <span data-ttu-id="71435-124">Attendere</span><span class="sxs-lookup"><span data-stu-id="71435-124">Wait</span></span>

```yaml
Type: Microsoft.Azure.Batch.Common.DisableJobOption
Parameter Sets: (All)
Aliases: 
Accepted values: Requeue, Terminate, Wait

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71435-125">-ID</span><span class="sxs-lookup"><span data-stu-id="71435-125">-Id</span></span>
<span data-ttu-id="71435-126">Specifica l'ID del processo disabilitato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71435-126">Specifies the ID of the job that this cmdlet disables.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71435-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71435-127">-DefaultProfile</span></span>
<span data-ttu-id="71435-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="71435-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71435-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71435-129">CommonParameters</span></span>
<span data-ttu-id="71435-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71435-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71435-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71435-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71435-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="71435-132">INPUTS</span></span>

### <span data-ttu-id="71435-133">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="71435-133">BatchAccountContext</span></span>
<span data-ttu-id="71435-134">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="71435-134">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="71435-135">Stringa</span><span class="sxs-lookup"><span data-stu-id="71435-135">String</span></span>
<span data-ttu-id="71435-136">Il parametro "ID" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="71435-136">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="71435-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="71435-137">OUTPUTS</span></span>

## <span data-ttu-id="71435-138">Note</span><span class="sxs-lookup"><span data-stu-id="71435-138">NOTES</span></span>

## <span data-ttu-id="71435-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="71435-139">RELATED LINKS</span></span>

[<span data-ttu-id="71435-140">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="71435-140">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="71435-141">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="71435-141">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="71435-142">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="71435-142">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="71435-143">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="71435-143">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="71435-144">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="71435-144">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="71435-145">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="71435-145">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="71435-146">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="71435-146">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


