---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 975B707C-5001-43ED-81AB-9BB6665135BA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJob.md
ms.openlocfilehash: f67660cdc64c814d04ec4a987b711c802ca222d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517551"
---
# <span data-ttu-id="a0b34-101">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a0b34-101">Stop-AzureBatchJob</span></span>

## <span data-ttu-id="a0b34-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a0b34-102">SYNOPSIS</span></span>
<span data-ttu-id="a0b34-103">Interrompe un processo batch.</span><span class="sxs-lookup"><span data-stu-id="a0b34-103">Stops a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0b34-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a0b34-104">SYNTAX</span></span>

```
Stop-AzureBatchJob [-Id] <String> [[-TerminateReason] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0b34-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0b34-105">DESCRIPTION</span></span>
<span data-ttu-id="a0b34-106">Il cmdlet **Stop-AzureBatchJob** interrompe un processo batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="a0b34-106">The **Stop-AzureBatchJob** cmdlet stops an Azure Batch job.</span></span>
<span data-ttu-id="a0b34-107">Questo comando contrassegna il processo come completato.</span><span class="sxs-lookup"><span data-stu-id="a0b34-107">This command marks the job as completed.</span></span>

## <span data-ttu-id="a0b34-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a0b34-108">EXAMPLES</span></span>

### <span data-ttu-id="a0b34-109">Esempio 1: interrompere un processo batch</span><span class="sxs-lookup"><span data-stu-id="a0b34-109">Example 1: Stop a Batch job</span></span>
```
PS C:\>Stop-AzureBatchJob -Id "Job-000001" -TerminateReason "No more tasks to run" -BatchContext $Context
```

<span data-ttu-id="a0b34-110">Questo comando Arresta il processo con ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="a0b34-110">This command stops the job that has the ID Job-000001.</span></span>
<span data-ttu-id="a0b34-111">Il comando specifica un motivo per cui si è scelto di interrompere il processo.</span><span class="sxs-lookup"><span data-stu-id="a0b34-111">The command specifies a reason that you chose to stop the job.</span></span>
<span data-ttu-id="a0b34-112">Usa il cmdlet Get-AzureRmBatchAccountKeys per assegnare un contesto alla variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="a0b34-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="a0b34-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a0b34-113">PARAMETERS</span></span>

### <span data-ttu-id="a0b34-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a0b34-114">-BatchContext</span></span>
<span data-ttu-id="a0b34-115">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="a0b34-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a0b34-116">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="a0b34-116">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a0b34-117">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="a0b34-117">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a0b34-118">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a0b34-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a0b34-119">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="a0b34-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a0b34-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0b34-120">-DefaultProfile</span></span>
<span data-ttu-id="a0b34-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a0b34-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0b34-122">-ID</span><span class="sxs-lookup"><span data-stu-id="a0b34-122">-Id</span></span>
<span data-ttu-id="a0b34-123">Specifica l'ID del processo interrotto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0b34-123">Specifies the ID of the job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="a0b34-124">-TerminateReason</span><span class="sxs-lookup"><span data-stu-id="a0b34-124">-TerminateReason</span></span>
<span data-ttu-id="a0b34-125">Specifica il motivo per cui hai deciso di interrompere il processo.</span><span class="sxs-lookup"><span data-stu-id="a0b34-125">Specifies the reason that you decided to stop the job.</span></span>
<span data-ttu-id="a0b34-126">Questo cmdlet archivia il testo come proprietà **TerminateReason** del processo.</span><span class="sxs-lookup"><span data-stu-id="a0b34-126">This cmdlet stores this text as the **TerminateReason** property of the job.</span></span>

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

### <span data-ttu-id="a0b34-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0b34-127">CommonParameters</span></span>
<span data-ttu-id="a0b34-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0b34-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0b34-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0b34-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0b34-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a0b34-130">INPUTS</span></span>

### <span data-ttu-id="a0b34-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a0b34-131">System.String</span></span>

### <span data-ttu-id="a0b34-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a0b34-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="a0b34-133">Parametri: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a0b34-133">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="a0b34-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a0b34-134">OUTPUTS</span></span>

### <span data-ttu-id="a0b34-135">System. void</span><span class="sxs-lookup"><span data-stu-id="a0b34-135">System.Void</span></span>

## <span data-ttu-id="a0b34-136">Note</span><span class="sxs-lookup"><span data-stu-id="a0b34-136">NOTES</span></span>

## <span data-ttu-id="a0b34-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a0b34-137">RELATED LINKS</span></span>

[<span data-ttu-id="a0b34-138">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a0b34-138">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="a0b34-139">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a0b34-139">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="a0b34-140">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="a0b34-140">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="a0b34-141">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a0b34-141">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="a0b34-142">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a0b34-142">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="a0b34-143">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a0b34-143">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="a0b34-144">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="a0b34-144">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


