---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJob.md
ms.openlocfilehash: eb15991e0bf7aefd60b53dbb02785a1b2004cb22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521782"
---
# <span data-ttu-id="3e383-101">Set-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="3e383-101">Set-AzureBatchJob</span></span>

## <span data-ttu-id="3e383-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3e383-102">SYNOPSIS</span></span>
<span data-ttu-id="3e383-103">Aggiorna un processo batch.</span><span class="sxs-lookup"><span data-stu-id="3e383-103">Updates a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e383-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3e383-104">SYNTAX</span></span>

```
Set-AzureBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e383-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e383-105">DESCRIPTION</span></span>
<span data-ttu-id="3e383-106">Il cmdlet **set-AzureBatchJob** aggiorna un processo batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="3e383-106">The **Set-AzureBatchJob** cmdlet updates an Azure Batch job.</span></span>
<span data-ttu-id="3e383-107">Usa il cmdlet Get-AzureBatchJob per ottenere un oggetto **PSCloudJob** .</span><span class="sxs-lookup"><span data-stu-id="3e383-107">Use the Get-AzureBatchJob cmdlet to get a **PSCloudJob** object.</span></span>
<span data-ttu-id="3e383-108">Modificare le proprietà di tale oggetto e quindi usare il cmdlet corrente per eseguire il commit delle modifiche apportate al servizio batch.</span><span class="sxs-lookup"><span data-stu-id="3e383-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="3e383-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3e383-109">EXAMPLES</span></span>

### <span data-ttu-id="3e383-110">Esempio 1: aggiornare un processo</span><span class="sxs-lookup"><span data-stu-id="3e383-110">Example 1: Update a job</span></span>
```
PS C:\>$Job = Get-AzureBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzureBatchJob -Job $Job -BatchContext $Context
```

<span data-ttu-id="3e383-111">Il primo comando ottiene un pool utilizzando **Get-AzureBatchJob** e lo archivia nella variabile $job.</span><span class="sxs-lookup"><span data-stu-id="3e383-111">The first command gets a pool by using **Get-AzureBatchJob** , and then stores it in the $Job variable.</span></span>

<span data-ttu-id="3e383-112">Il secondo comando modifica la specifica della priorità nell'oggetto $Job.</span><span class="sxs-lookup"><span data-stu-id="3e383-112">The second command modifies the priority specification on the $Job object.</span></span>

<span data-ttu-id="3e383-113">Il comando finale aggiorna il servizio batch in base all'oggetto locale in $Job.</span><span class="sxs-lookup"><span data-stu-id="3e383-113">The final command updates the Batch service to match the local object in $Job.</span></span>

## <span data-ttu-id="3e383-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3e383-114">PARAMETERS</span></span>

### <span data-ttu-id="3e383-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="3e383-115">-BatchContext</span></span>
<span data-ttu-id="3e383-116">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="3e383-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="3e383-117">Per ottenere un oggetto **BatchAccountContext** che contiene i tasti di scelta per l'abbonamento, usare il cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="3e383-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="3e383-118">-Job</span><span class="sxs-lookup"><span data-stu-id="3e383-118">-Job</span></span>
<span data-ttu-id="3e383-119">Specifica un **PSCloudJob** a cui questo cmdlet aggiorna il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="3e383-119">Specifies a **PSCloudJob** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="3e383-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e383-120">-DefaultProfile</span></span>
<span data-ttu-id="3e383-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3e383-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e383-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e383-122">CommonParameters</span></span>
<span data-ttu-id="3e383-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e383-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e383-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e383-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e383-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3e383-125">INPUTS</span></span>

### <span data-ttu-id="3e383-126">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="3e383-126">BatchAccountContext</span></span>
<span data-ttu-id="3e383-127">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="3e383-127">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="3e383-128">PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="3e383-128">PSCloudJob</span></span>
<span data-ttu-id="3e383-129">Il parametro "Job" accetta il valore di tipo "PSCloudJob" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="3e383-129">Parameter 'Job' accepts value of type 'PSCloudJob' from the pipeline</span></span>

## <span data-ttu-id="3e383-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3e383-130">OUTPUTS</span></span>

## <span data-ttu-id="3e383-131">Note</span><span class="sxs-lookup"><span data-stu-id="3e383-131">NOTES</span></span>

## <span data-ttu-id="3e383-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3e383-132">RELATED LINKS</span></span>

[<span data-ttu-id="3e383-133">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="3e383-133">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="3e383-134">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="3e383-134">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="3e383-135">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="3e383-135">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="3e383-136">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="3e383-136">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="3e383-137">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="3e383-137">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="3e383-138">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="3e383-138">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="3e383-139">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="3e383-139">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="3e383-140">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="3e383-140">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


