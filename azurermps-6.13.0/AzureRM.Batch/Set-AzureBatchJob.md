---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJob.md
ms.openlocfilehash: 3baaa7296ab0fdd2c1dcab606b2896b11e5773f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509323"
---
# <span data-ttu-id="16fae-101">Set-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="16fae-101">Set-AzureBatchJob</span></span>

## <span data-ttu-id="16fae-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="16fae-102">SYNOPSIS</span></span>
<span data-ttu-id="16fae-103">Aggiorna un processo batch.</span><span class="sxs-lookup"><span data-stu-id="16fae-103">Updates a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16fae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="16fae-104">SYNTAX</span></span>

```
Set-AzureBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16fae-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16fae-105">DESCRIPTION</span></span>
<span data-ttu-id="16fae-106">Il cmdlet **set-AzureBatchJob** aggiorna un processo batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="16fae-106">The **Set-AzureBatchJob** cmdlet updates an Azure Batch job.</span></span>
<span data-ttu-id="16fae-107">Usa il cmdlet Get-AzureBatchJob per ottenere un oggetto **PSCloudJob** .</span><span class="sxs-lookup"><span data-stu-id="16fae-107">Use the Get-AzureBatchJob cmdlet to get a **PSCloudJob** object.</span></span>
<span data-ttu-id="16fae-108">Modificare le proprietà di tale oggetto e quindi usare il cmdlet corrente per eseguire il commit delle modifiche apportate al servizio batch.</span><span class="sxs-lookup"><span data-stu-id="16fae-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="16fae-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="16fae-109">EXAMPLES</span></span>

### <span data-ttu-id="16fae-110">Esempio 1: aggiornare un processo</span><span class="sxs-lookup"><span data-stu-id="16fae-110">Example 1: Update a job</span></span>
```
PS C:\>$Job = Get-AzureBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzureBatchJob -Job $Job -BatchContext $Context
```

<span data-ttu-id="16fae-111">Il primo comando ottiene un pool utilizzando **Get-AzureBatchJob** e lo archivia nella variabile $job.</span><span class="sxs-lookup"><span data-stu-id="16fae-111">The first command gets a pool by using **Get-AzureBatchJob** , and then stores it in the $Job variable.</span></span>
<span data-ttu-id="16fae-112">Il secondo comando modifica la specifica della priorità nell'oggetto $Job.</span><span class="sxs-lookup"><span data-stu-id="16fae-112">The second command modifies the priority specification on the $Job object.</span></span>
<span data-ttu-id="16fae-113">Il comando finale aggiorna il servizio batch in base all'oggetto locale in $Job.</span><span class="sxs-lookup"><span data-stu-id="16fae-113">The final command updates the Batch service to match the local object in $Job.</span></span>

## <span data-ttu-id="16fae-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="16fae-114">PARAMETERS</span></span>

### <span data-ttu-id="16fae-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="16fae-115">-BatchContext</span></span>
<span data-ttu-id="16fae-116">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="16fae-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="16fae-117">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="16fae-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="16fae-118">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="16fae-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="16fae-119">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="16fae-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="16fae-120">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="16fae-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="16fae-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16fae-121">-DefaultProfile</span></span>
<span data-ttu-id="16fae-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="16fae-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16fae-123">-Job</span><span class="sxs-lookup"><span data-stu-id="16fae-123">-Job</span></span>
<span data-ttu-id="16fae-124">Specifica un **PSCloudJob** a cui questo cmdlet aggiorna il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="16fae-124">Specifies a **PSCloudJob** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16fae-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16fae-125">CommonParameters</span></span>
<span data-ttu-id="16fae-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16fae-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16fae-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16fae-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16fae-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="16fae-128">INPUTS</span></span>

### <span data-ttu-id="16fae-129">Microsoft.Azure.Commands.Batch. Models. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="16fae-129">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>
<span data-ttu-id="16fae-130">Parameters: Job (ByValue)</span><span class="sxs-lookup"><span data-stu-id="16fae-130">Parameters: Job (ByValue)</span></span>

### <span data-ttu-id="16fae-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="16fae-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="16fae-132">Parametri: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="16fae-132">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="16fae-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="16fae-133">OUTPUTS</span></span>

### <span data-ttu-id="16fae-134">System. void</span><span class="sxs-lookup"><span data-stu-id="16fae-134">System.Void</span></span>

## <span data-ttu-id="16fae-135">Note</span><span class="sxs-lookup"><span data-stu-id="16fae-135">NOTES</span></span>

## <span data-ttu-id="16fae-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="16fae-136">RELATED LINKS</span></span>

[<span data-ttu-id="16fae-137">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="16fae-137">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="16fae-138">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="16fae-138">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="16fae-139">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="16fae-139">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="16fae-140">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="16fae-140">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="16fae-141">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="16fae-141">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="16fae-142">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="16fae-142">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="16fae-143">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="16fae-143">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="16fae-144">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="16fae-144">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


