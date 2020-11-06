---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 02F91510-F14F-4401-BC5F-06B0874AEB4B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJobSchedule.md
ms.openlocfilehash: c012fe266bc25752729b14192c4d9c0a42cd8961
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521791"
---
# <span data-ttu-id="8dd4e-101">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8dd4e-101">Enable-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="8dd4e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8dd4e-102">SYNOPSIS</span></span>
<span data-ttu-id="8dd4e-103">Abilita una pianificazione processo batch.</span><span class="sxs-lookup"><span data-stu-id="8dd4e-103">Enables a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8dd4e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8dd4e-104">SYNTAX</span></span>

```
Enable-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8dd4e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8dd4e-105">DESCRIPTION</span></span>
<span data-ttu-id="8dd4e-106">Il cmdlet **Enable-AzureBatchJobSchedule** Abilita una pianificazione del processo batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="8dd4e-106">The **Enable-AzureBatchJobSchedule** cmdlet enables an Azure Batch job schedule.</span></span>
<span data-ttu-id="8dd4e-107">Dopo l'abilitazione di una pianificazione processo, i processi possono essere creati in base a tale programmazione.</span><span class="sxs-lookup"><span data-stu-id="8dd4e-107">After you enable a job schedule, jobs can be created according to that schedule.</span></span>

## <span data-ttu-id="8dd4e-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8dd4e-108">EXAMPLES</span></span>

### <span data-ttu-id="8dd4e-109">Esempio 1: abilitare una pianificazione del processo</span><span class="sxs-lookup"><span data-stu-id="8dd4e-109">Example 1: Enable a job schedule</span></span>
```
PS C:\>Enable-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="8dd4e-110">Questo comando Abilita la pianificazione del processo con ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="8dd4e-110">This command enables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="8dd4e-111">Usa il cmdlet **Get-AzureRmBatchAccountKeys** per assegnare un contesto alla variabile $context.</span><span class="sxs-lookup"><span data-stu-id="8dd4e-111">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="8dd4e-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8dd4e-112">PARAMETERS</span></span>

### <span data-ttu-id="8dd4e-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="8dd4e-113">-BatchContext</span></span>
<span data-ttu-id="8dd4e-114">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="8dd4e-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8dd4e-115">Per ottenere un oggetto **BatchAccountContext** che contiene i tasti di scelta per l'abbonamento, usare il cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="8dd4e-115">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="8dd4e-116">-ID</span><span class="sxs-lookup"><span data-stu-id="8dd4e-116">-Id</span></span>
<span data-ttu-id="8dd4e-117">Specifica l'ID della pianificazione del processo abilitata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8dd4e-117">Specifies the ID of the job schedule that this cmdlet enables.</span></span>

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

### <span data-ttu-id="8dd4e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dd4e-118">-DefaultProfile</span></span>
<span data-ttu-id="8dd4e-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8dd4e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8dd4e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dd4e-120">CommonParameters</span></span>
<span data-ttu-id="8dd4e-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dd4e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dd4e-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8dd4e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dd4e-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8dd4e-123">INPUTS</span></span>

### <span data-ttu-id="8dd4e-124">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8dd4e-124">BatchAccountContext</span></span>
<span data-ttu-id="8dd4e-125">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="8dd4e-125">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="8dd4e-126">Stringa</span><span class="sxs-lookup"><span data-stu-id="8dd4e-126">String</span></span>
<span data-ttu-id="8dd4e-127">Il parametro "ID" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="8dd4e-127">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="8dd4e-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8dd4e-128">OUTPUTS</span></span>

## <span data-ttu-id="8dd4e-129">Note</span><span class="sxs-lookup"><span data-stu-id="8dd4e-129">NOTES</span></span>

## <span data-ttu-id="8dd4e-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8dd4e-130">RELATED LINKS</span></span>

[<span data-ttu-id="8dd4e-131">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8dd4e-131">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="8dd4e-132">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="8dd4e-132">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="8dd4e-133">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8dd4e-133">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="8dd4e-134">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8dd4e-134">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="8dd4e-135">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8dd4e-135">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="8dd4e-136">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8dd4e-136">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="8dd4e-137">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="8dd4e-137">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


