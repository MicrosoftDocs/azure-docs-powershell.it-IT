---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 975B707C-5001-43ED-81AB-9BB6665135BA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJob.md
ms.openlocfilehash: 8893ed4002e576e257cd9b885d5773c5851edde0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519214"
---
# <span data-ttu-id="6c5b9-101">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="6c5b9-101">Stop-AzureBatchJob</span></span>

## <span data-ttu-id="6c5b9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6c5b9-102">SYNOPSIS</span></span>
<span data-ttu-id="6c5b9-103">Interrompe un processo batch.</span><span class="sxs-lookup"><span data-stu-id="6c5b9-103">Stops a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c5b9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6c5b9-104">SYNTAX</span></span>

```
Stop-AzureBatchJob [-Id] <String> [[-TerminateReason] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c5b9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6c5b9-105">DESCRIPTION</span></span>
<span data-ttu-id="6c5b9-106">Il cmdlet **Stop-AzureBatchJob** interrompe un processo batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="6c5b9-106">The **Stop-AzureBatchJob** cmdlet stops an Azure Batch job.</span></span>
<span data-ttu-id="6c5b9-107">Questo comando contrassegna il processo come completato.</span><span class="sxs-lookup"><span data-stu-id="6c5b9-107">This command marks the job as completed.</span></span>

## <span data-ttu-id="6c5b9-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6c5b9-108">EXAMPLES</span></span>

### <span data-ttu-id="6c5b9-109">Esempio 1: interrompere un processo batch</span><span class="sxs-lookup"><span data-stu-id="6c5b9-109">Example 1: Stop a Batch job</span></span>
```
PS C:\>Stop-AzureBatchJob -Id "Job-000001" -TerminateReason "No more tasks to run" -BatchContext $Context
```

<span data-ttu-id="6c5b9-110">Questo comando Arresta il processo con ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="6c5b9-110">This command stops the job that has the ID Job-000001.</span></span>
<span data-ttu-id="6c5b9-111">Il comando specifica un motivo per cui si è scelto di interrompere il processo.</span><span class="sxs-lookup"><span data-stu-id="6c5b9-111">The command specifies a reason that you chose to stop the job.</span></span>
<span data-ttu-id="6c5b9-112">Usa il cmdlet Get-AzureRmBatchAccountKeys per assegnare un contesto alla variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="6c5b9-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="6c5b9-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6c5b9-113">PARAMETERS</span></span>

### <span data-ttu-id="6c5b9-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6c5b9-114">-BatchContext</span></span>
<span data-ttu-id="6c5b9-115">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="6c5b9-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6c5b9-116">Per ottenere un oggetto **BatchAccountContext** che contiene i tasti di scelta per l'abbonamento, usare il cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="6c5b9-116">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="6c5b9-117">-ID</span><span class="sxs-lookup"><span data-stu-id="6c5b9-117">-Id</span></span>
<span data-ttu-id="6c5b9-118">Specifica l'ID del processo interrotto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c5b9-118">Specifies the ID of the job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="6c5b9-119">-TerminateReason</span><span class="sxs-lookup"><span data-stu-id="6c5b9-119">-TerminateReason</span></span>
<span data-ttu-id="6c5b9-120">Specifica il motivo per cui hai deciso di interrompere il processo.</span><span class="sxs-lookup"><span data-stu-id="6c5b9-120">Specifies the reason that you decided to stop the job.</span></span>
<span data-ttu-id="6c5b9-121">Questo cmdlet archivia il testo come proprietà **TerminateReason** del processo.</span><span class="sxs-lookup"><span data-stu-id="6c5b9-121">This cmdlet stores this text as the **TerminateReason** property of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c5b9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c5b9-122">-DefaultProfile</span></span>
<span data-ttu-id="6c5b9-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6c5b9-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c5b9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c5b9-124">CommonParameters</span></span>
<span data-ttu-id="6c5b9-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c5b9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c5b9-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c5b9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c5b9-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6c5b9-127">INPUTS</span></span>

### <span data-ttu-id="6c5b9-128">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6c5b9-128">BatchAccountContext</span></span>
<span data-ttu-id="6c5b9-129">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="6c5b9-129">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="6c5b9-130">Stringa</span><span class="sxs-lookup"><span data-stu-id="6c5b9-130">String</span></span>
<span data-ttu-id="6c5b9-131">Il parametro "ID" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="6c5b9-131">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="6c5b9-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6c5b9-132">OUTPUTS</span></span>

## <span data-ttu-id="6c5b9-133">Note</span><span class="sxs-lookup"><span data-stu-id="6c5b9-133">NOTES</span></span>

## <span data-ttu-id="6c5b9-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6c5b9-134">RELATED LINKS</span></span>

[<span data-ttu-id="6c5b9-135">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="6c5b9-135">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="6c5b9-136">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="6c5b9-136">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="6c5b9-137">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="6c5b9-137">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="6c5b9-138">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="6c5b9-138">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="6c5b9-139">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="6c5b9-139">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="6c5b9-140">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="6c5b9-140">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="6c5b9-141">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="6c5b9-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


