---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJobSchedule.md
ms.openlocfilehash: 58ac726d722959e3ee32bce84c0abe3c771fcbcc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519213"
---
# <span data-ttu-id="99b04-101">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="99b04-101">Stop-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="99b04-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="99b04-102">SYNOPSIS</span></span>
<span data-ttu-id="99b04-103">Interrompe la pianificazione di un processo batch.</span><span class="sxs-lookup"><span data-stu-id="99b04-103">Stops a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99b04-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="99b04-104">SYNTAX</span></span>

```
Stop-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99b04-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="99b04-105">DESCRIPTION</span></span>
<span data-ttu-id="99b04-106">Il cmdlet **Stop-AzureBatchJobSchedule** interrompe la pianificazione di un processo batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="99b04-106">The **Stop-AzureBatchJobSchedule** cmdlet stops an Azure Batch job schedule.</span></span>

## <span data-ttu-id="99b04-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="99b04-107">EXAMPLES</span></span>

### <span data-ttu-id="99b04-108">Esempio 1: interrompere la pianificazione di un processo</span><span class="sxs-lookup"><span data-stu-id="99b04-108">Example 1: Stop a job schedule</span></span>
```
PS C:\>Stop-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="99b04-109">Questo comando interrompe la pianificazione del processo che contiene l'ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="99b04-109">This command stops the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="99b04-110">Usa il cmdlet Get-AzureRmBatchAccountKeys per assegnare un contesto alla variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="99b04-110">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="99b04-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="99b04-111">PARAMETERS</span></span>

### <span data-ttu-id="99b04-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="99b04-112">-BatchContext</span></span>
<span data-ttu-id="99b04-113">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="99b04-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="99b04-114">Per ottenere un oggetto **BatchAccountContext** che contiene i tasti di scelta per l'abbonamento, usare il cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="99b04-114">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="99b04-115">-ID</span><span class="sxs-lookup"><span data-stu-id="99b04-115">-Id</span></span>
<span data-ttu-id="99b04-116">Specifica l'ID della pianificazione del processo arrestata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99b04-116">Specifies the ID of the job schedule that this cmdlet stops.</span></span>

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

### <span data-ttu-id="99b04-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99b04-117">-DefaultProfile</span></span>
<span data-ttu-id="99b04-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="99b04-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99b04-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99b04-119">CommonParameters</span></span>
<span data-ttu-id="99b04-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99b04-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99b04-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99b04-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99b04-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="99b04-122">INPUTS</span></span>

### <span data-ttu-id="99b04-123">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="99b04-123">BatchAccountContext</span></span>
<span data-ttu-id="99b04-124">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="99b04-124">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="99b04-125">Stringa</span><span class="sxs-lookup"><span data-stu-id="99b04-125">String</span></span>
<span data-ttu-id="99b04-126">Il parametro "ID" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="99b04-126">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="99b04-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="99b04-127">OUTPUTS</span></span>

## <span data-ttu-id="99b04-128">Note</span><span class="sxs-lookup"><span data-stu-id="99b04-128">NOTES</span></span>

## <span data-ttu-id="99b04-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="99b04-129">RELATED LINKS</span></span>

[<span data-ttu-id="99b04-130">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="99b04-130">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="99b04-131">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="99b04-131">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="99b04-132">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="99b04-132">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="99b04-133">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="99b04-133">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="99b04-134">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="99b04-134">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="99b04-135">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="99b04-135">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="99b04-136">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="99b04-136">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


