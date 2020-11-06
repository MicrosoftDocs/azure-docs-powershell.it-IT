---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B4737AE8-F57C-4B95-B81E-74802EF8E7AE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJobSchedule.md
ms.openlocfilehash: 73d80d3547ea895e5cbd35b2d514d9a757164bed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521795"
---
# <span data-ttu-id="54f87-101">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="54f87-101">Disable-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="54f87-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="54f87-102">SYNOPSIS</span></span>
<span data-ttu-id="54f87-103">Disabilita la pianificazione di un processo batch.</span><span class="sxs-lookup"><span data-stu-id="54f87-103">Disables a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54f87-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="54f87-104">SYNTAX</span></span>

```
Disable-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54f87-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="54f87-105">DESCRIPTION</span></span>
<span data-ttu-id="54f87-106">Il cmdlet **Disable-AzureBatchJobSchedule Disabilita** una pianificazione dei processi batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="54f87-106">The **Disable-AzureBatchJobSchedule** cmdlet disables an Azure Batch job schedule.</span></span>
<span data-ttu-id="54f87-107">Se si disattiva una programmazione, i processi non vengono creati in base a tale programmazione.</span><span class="sxs-lookup"><span data-stu-id="54f87-107">If you disable a schedule, jobs are not created according to that schedule.</span></span>
<span data-ttu-id="54f87-108">È possibile abilitare una pianificazione disabilitata in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="54f87-108">You can enable a disabled schedule later.</span></span>

## <span data-ttu-id="54f87-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="54f87-109">EXAMPLES</span></span>

### <span data-ttu-id="54f87-110">Esempio 1: disabilitare una pianificazione del processo</span><span class="sxs-lookup"><span data-stu-id="54f87-110">Example 1: Disable a job schedule</span></span>
```
PS C:\>Disable-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="54f87-111">Questo comando Disabilita la pianificazione del processo con ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="54f87-111">This command disables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="54f87-112">Usa il cmdlet **Get-AzureRmBatchAccountKeys** per assegnare un contesto alla variabile $context.</span><span class="sxs-lookup"><span data-stu-id="54f87-112">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="54f87-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="54f87-113">PARAMETERS</span></span>

### <span data-ttu-id="54f87-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="54f87-114">-BatchContext</span></span>
<span data-ttu-id="54f87-115">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="54f87-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="54f87-116">Per ottenere un oggetto **BatchAccountContext** che contiene i tasti di scelta per l'abbonamento, usare il cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="54f87-116">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="54f87-117">-ID</span><span class="sxs-lookup"><span data-stu-id="54f87-117">-Id</span></span>
<span data-ttu-id="54f87-118">Specifica l'ID della pianificazione del processo disabilitata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54f87-118">Specifies the ID of the job schedule that this cmdlet disables.</span></span>

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

### <span data-ttu-id="54f87-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54f87-119">-DefaultProfile</span></span>
<span data-ttu-id="54f87-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="54f87-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54f87-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54f87-121">CommonParameters</span></span>
<span data-ttu-id="54f87-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54f87-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54f87-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54f87-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54f87-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="54f87-124">INPUTS</span></span>

### <span data-ttu-id="54f87-125">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="54f87-125">BatchAccountContext</span></span>
<span data-ttu-id="54f87-126">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="54f87-126">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="54f87-127">Stringa</span><span class="sxs-lookup"><span data-stu-id="54f87-127">String</span></span>
<span data-ttu-id="54f87-128">Il parametro "ID" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="54f87-128">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="54f87-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="54f87-129">OUTPUTS</span></span>

## <span data-ttu-id="54f87-130">Note</span><span class="sxs-lookup"><span data-stu-id="54f87-130">NOTES</span></span>

## <span data-ttu-id="54f87-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="54f87-131">RELATED LINKS</span></span>

[<span data-ttu-id="54f87-132">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="54f87-132">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="54f87-133">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="54f87-133">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="54f87-134">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="54f87-134">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="54f87-135">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="54f87-135">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="54f87-136">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="54f87-136">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="54f87-137">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="54f87-137">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="54f87-138">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="54f87-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


