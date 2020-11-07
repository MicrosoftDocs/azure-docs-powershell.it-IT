---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 7C79BFF1-41E1-472D-AF67-1C3B39AB7548
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJob.md
ms.openlocfilehash: 665d7b64f3e8d83dd45ebc8de0cc36da960f8c35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688367"
---
# <span data-ttu-id="f88d2-101">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="f88d2-101">Enable-AzureBatchJob</span></span>

## <span data-ttu-id="f88d2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f88d2-102">SYNOPSIS</span></span>
<span data-ttu-id="f88d2-103">Abilita un processo batch.</span><span class="sxs-lookup"><span data-stu-id="f88d2-103">Enables a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f88d2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f88d2-104">SYNTAX</span></span>

```
Enable-AzureBatchJob [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f88d2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f88d2-105">DESCRIPTION</span></span>
<span data-ttu-id="f88d2-106">Il cmdlet **Enable-AzureBatchJob** Abilita un processo batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="f88d2-106">The **Enable-AzureBatchJob** cmdlet enables an Azure Batch job.</span></span>
<span data-ttu-id="f88d2-107">Dopo l'abilitazione di un processo, le nuove attività possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="f88d2-107">After you enable a job, new tasks can run.</span></span>

## <span data-ttu-id="f88d2-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f88d2-108">EXAMPLES</span></span>

### <span data-ttu-id="f88d2-109">Esempio 1: abilitare un processo batch</span><span class="sxs-lookup"><span data-stu-id="f88d2-109">Example 1: Enable a Batch job</span></span>
```
PS C:\>Enable-AzureBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="f88d2-110">Questo comando consente di abilitare il processo con ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="f88d2-110">This command enables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="f88d2-111">Usa il cmdlet Get-AzureRmBatchAccountKeys per assegnare un contesto alla variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="f88d2-111">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="f88d2-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f88d2-112">PARAMETERS</span></span>

### <span data-ttu-id="f88d2-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f88d2-113">-BatchContext</span></span>
<span data-ttu-id="f88d2-114">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="f88d2-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f88d2-115">Per ottenere un oggetto **BatchAccountContext** che contiene i tasti di scelta per l'abbonamento, usare il cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="f88d2-115">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="f88d2-116">-ID</span><span class="sxs-lookup"><span data-stu-id="f88d2-116">-Id</span></span>
<span data-ttu-id="f88d2-117">Specifica l'ID del processo abilitato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f88d2-117">Specifies the ID of the job that this cmdlet enables.</span></span>

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

### <span data-ttu-id="f88d2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f88d2-118">-DefaultProfile</span></span>
<span data-ttu-id="f88d2-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f88d2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f88d2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f88d2-120">CommonParameters</span></span>
<span data-ttu-id="f88d2-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f88d2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f88d2-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f88d2-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f88d2-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f88d2-123">INPUTS</span></span>

### <span data-ttu-id="f88d2-124">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f88d2-124">BatchAccountContext</span></span>
<span data-ttu-id="f88d2-125">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="f88d2-125">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="f88d2-126">Stringa</span><span class="sxs-lookup"><span data-stu-id="f88d2-126">String</span></span>
<span data-ttu-id="f88d2-127">Il parametro "ID" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="f88d2-127">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="f88d2-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f88d2-128">OUTPUTS</span></span>

## <span data-ttu-id="f88d2-129">Note</span><span class="sxs-lookup"><span data-stu-id="f88d2-129">NOTES</span></span>

## <span data-ttu-id="f88d2-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f88d2-130">RELATED LINKS</span></span>

[<span data-ttu-id="f88d2-131">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="f88d2-131">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="f88d2-132">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="f88d2-132">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="f88d2-133">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="f88d2-133">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="f88d2-134">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="f88d2-134">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="f88d2-135">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="f88d2-135">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="f88d2-136">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="f88d2-136">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


