---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 6A6D6C7D-EED7-4AD4-ACE6-BFA64404455E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchTask.md
ms.openlocfilehash: b572a7aefc3076671e78895f5fea531929858873
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520790"
---
# <span data-ttu-id="2b7bf-101">Set-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="2b7bf-101">Set-AzureBatchTask</span></span>

## <span data-ttu-id="2b7bf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2b7bf-102">SYNOPSIS</span></span>
<span data-ttu-id="2b7bf-103">Aggiorna le proprietà di un'attività.</span><span class="sxs-lookup"><span data-stu-id="2b7bf-103">Updates the properties of a task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b7bf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2b7bf-104">SYNTAX</span></span>

```
Set-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b7bf-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b7bf-105">DESCRIPTION</span></span>
<span data-ttu-id="2b7bf-106">Il cmdlet **set-AzureBatchTask** aggiorna le proprietà di un'attività nel servizio batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="2b7bf-106">The **Set-AzureBatchTask** cmdlet updates the properties of a task in the Azure Batch service.</span></span>
<span data-ttu-id="2b7bf-107">Usa il cmdlet Get-AzureBatchTask per ottenere un oggetto **PSCloudTask** .</span><span class="sxs-lookup"><span data-stu-id="2b7bf-107">Use the Get-AzureBatchTask cmdlet to get a **PSCloudTask** object.</span></span>
<span data-ttu-id="2b7bf-108">Modificare le proprietà di tale oggetto e quindi usare il cmdlet corrente per eseguire il commit delle modifiche apportate al servizio batch.</span><span class="sxs-lookup"><span data-stu-id="2b7bf-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="2b7bf-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2b7bf-109">EXAMPLES</span></span>

### <span data-ttu-id="2b7bf-110">Esempio 1: aggiornare un'attività</span><span class="sxs-lookup"><span data-stu-id="2b7bf-110">Example 1: Update a task</span></span>
```
PS C:\>$Task = Get-AzureBatchTask -JobId "Job16" -Id "Task22" -BatchContext $Context
PS C:\> $Constraints = New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints -ArgumentList @([TimeSpan}::FromDays(5), [TimeSpan]::FromDays(2), 3)
PS C:\> $Task.Constraints = $Constraints
PS C:\> Set-AzureBatchTask -Task $Task -BatchContext $Context
```

<span data-ttu-id="2b7bf-111">Il primo comando ottiene un'attività usando **Get-AzureBatchTask** e lo archivia nella variabile $Task.</span><span class="sxs-lookup"><span data-stu-id="2b7bf-111">The first command gets a task by using **Get-AzureBatchTask** , and then stores it in the $Task variable.</span></span>

<span data-ttu-id="2b7bf-112">I due comandi successivi modificano i vincoli dell'attività in $Task.</span><span class="sxs-lookup"><span data-stu-id="2b7bf-112">The next two commands modify the constraints of the task in $Task.</span></span>

<span data-ttu-id="2b7bf-113">Il comando finale aggiorna il servizio batch in base all'oggetto locale in $Task.</span><span class="sxs-lookup"><span data-stu-id="2b7bf-113">The final command updates the Batch service to match the local object in $Task.</span></span>

## <span data-ttu-id="2b7bf-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2b7bf-114">PARAMETERS</span></span>

### <span data-ttu-id="2b7bf-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="2b7bf-115">-BatchContext</span></span>
<span data-ttu-id="2b7bf-116">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="2b7bf-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2b7bf-117">Per ottenere un oggetto **BatchAccountContext** che contiene i tasti di scelta per l'abbonamento, usare il cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="2b7bf-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="2b7bf-118">-Attività</span><span class="sxs-lookup"><span data-stu-id="2b7bf-118">-Task</span></span>
<span data-ttu-id="2b7bf-119">Specifica il **PSCloudTask** a cui questo cmdlet aggiorna il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="2b7bf-119">Specifies the **PSCloudTask** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b7bf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b7bf-120">-DefaultProfile</span></span>
<span data-ttu-id="2b7bf-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2b7bf-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b7bf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b7bf-122">CommonParameters</span></span>
<span data-ttu-id="2b7bf-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b7bf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b7bf-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b7bf-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b7bf-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2b7bf-125">INPUTS</span></span>

### <span data-ttu-id="2b7bf-126">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="2b7bf-126">BatchAccountContext</span></span>
<span data-ttu-id="2b7bf-127">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="2b7bf-127">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="2b7bf-128">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="2b7bf-128">PSCloudTask</span></span>
<span data-ttu-id="2b7bf-129">Il parametro ' Task ' accetta il valore di tipo ' PSCloudTask ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="2b7bf-129">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="2b7bf-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2b7bf-130">OUTPUTS</span></span>

## <span data-ttu-id="2b7bf-131">Note</span><span class="sxs-lookup"><span data-stu-id="2b7bf-131">NOTES</span></span>

## <span data-ttu-id="2b7bf-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2b7bf-132">RELATED LINKS</span></span>

[<span data-ttu-id="2b7bf-133">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="2b7bf-133">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="2b7bf-134">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="2b7bf-134">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="2b7bf-135">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="2b7bf-135">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="2b7bf-136">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="2b7bf-136">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="2b7bf-137">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="2b7bf-137">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="2b7bf-138">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="2b7bf-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


