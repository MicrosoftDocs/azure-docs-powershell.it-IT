---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 1EA57372-6FA5-45C9-94A1-50D53830FC10
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchTask.md
ms.openlocfilehash: ac63bbdb95551ff5ff08661a92f0924d5853ade5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519210"
---
# <span data-ttu-id="3051b-101">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="3051b-101">Stop-AzureBatchTask</span></span>

## <span data-ttu-id="3051b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3051b-102">SYNOPSIS</span></span>
<span data-ttu-id="3051b-103">Interrompe un'attività batch.</span><span class="sxs-lookup"><span data-stu-id="3051b-103">Stops a Batch task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3051b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3051b-104">SYNTAX</span></span>

### <span data-ttu-id="3051b-105">ID</span><span class="sxs-lookup"><span data-stu-id="3051b-105">Id</span></span>
```
Stop-AzureBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3051b-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="3051b-106">InputObject</span></span>
```
Stop-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3051b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3051b-107">DESCRIPTION</span></span>
<span data-ttu-id="3051b-108">Il cmdlet **Stop-AzureBatchTask** interrompe un'attività batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="3051b-108">The **Stop-AzureBatchTask** cmdlet stops an Azure Batch task.</span></span>

## <span data-ttu-id="3051b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3051b-109">EXAMPLES</span></span>

### <span data-ttu-id="3051b-110">Esempio 1: eliminare un'attività batch in base all'ID</span><span class="sxs-lookup"><span data-stu-id="3051b-110">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Stop-AzureBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="3051b-111">Questo comando Arresta un'attività con ID Task23 sotto il processo con ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="3051b-111">This command stops a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="3051b-112">Il comando richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="3051b-112">The command prompts you for confirmation.</span></span>
<span data-ttu-id="3051b-113">Usa il cmdlet Get-AzureRmBatchAccountKeys per assegnare un contesto alla variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="3051b-113">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="3051b-114">Esempio 2: arrestare un'attività batch usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="3051b-114">Example 2: Stop a Batch task by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Stop-AzureBatchTask -BatchContext $Context
```

<span data-ttu-id="3051b-115">Questo comando ottiene l'attività batch che contiene l'ID Task26 nel processo con l'ID Job-000001 usando il cmdlet Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="3051b-115">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the Get-AzureBatchTask cmdlet.</span></span>
<span data-ttu-id="3051b-116">Il comando passa l'attività al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="3051b-116">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3051b-117">Il comando interrompe l'attività.</span><span class="sxs-lookup"><span data-stu-id="3051b-117">The command stops that task.</span></span>

## <span data-ttu-id="3051b-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3051b-118">PARAMETERS</span></span>

### <span data-ttu-id="3051b-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="3051b-119">-BatchContext</span></span>
<span data-ttu-id="3051b-120">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="3051b-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="3051b-121">Per ottenere un oggetto **BatchAccountContext** che contiene i tasti di scelta per l'abbonamento, usare il cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="3051b-121">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="3051b-122">-ID</span><span class="sxs-lookup"><span data-stu-id="3051b-122">-Id</span></span>
<span data-ttu-id="3051b-123">Specifica l'ID dell'attività arrestata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3051b-123">Specifies the ID of the task that this cmdlet stops.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3051b-124">-JobId</span><span class="sxs-lookup"><span data-stu-id="3051b-124">-JobId</span></span>
<span data-ttu-id="3051b-125">Specifica l'ID del processo che contiene l'attività.</span><span class="sxs-lookup"><span data-stu-id="3051b-125">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3051b-126">-Attività</span><span class="sxs-lookup"><span data-stu-id="3051b-126">-Task</span></span>
<span data-ttu-id="3051b-127">Specifica l'attività arrestata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3051b-127">Specifies the task that this cmdlet stops.</span></span>
<span data-ttu-id="3051b-128">Per ottenere un oggetto **PSCloudTask** , usa il cmdlet Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="3051b-128">To obtain a **PSCloudTask** object, use the Get-AzureBatchTask cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: InputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3051b-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3051b-129">-DefaultProfile</span></span>
<span data-ttu-id="3051b-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3051b-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3051b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3051b-131">CommonParameters</span></span>
<span data-ttu-id="3051b-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3051b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3051b-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3051b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3051b-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3051b-134">INPUTS</span></span>

### <span data-ttu-id="3051b-135">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="3051b-135">BatchAccountContext</span></span>
<span data-ttu-id="3051b-136">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="3051b-136">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="3051b-137">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="3051b-137">PSCloudTask</span></span>
<span data-ttu-id="3051b-138">Il parametro ' Task ' accetta il valore di tipo ' PSCloudTask ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="3051b-138">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="3051b-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3051b-139">OUTPUTS</span></span>

## <span data-ttu-id="3051b-140">Note</span><span class="sxs-lookup"><span data-stu-id="3051b-140">NOTES</span></span>

## <span data-ttu-id="3051b-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3051b-141">RELATED LINKS</span></span>

[<span data-ttu-id="3051b-142">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="3051b-142">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="3051b-143">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="3051b-143">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="3051b-144">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="3051b-144">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="3051b-145">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="3051b-145">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


