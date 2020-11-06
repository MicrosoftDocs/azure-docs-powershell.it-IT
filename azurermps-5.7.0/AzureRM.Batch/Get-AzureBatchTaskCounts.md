---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchtaskcounts
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTaskCounts.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTaskCounts.md
ms.openlocfilehash: d0b98081675cd11d8d3eb60a6495ac87a1111034
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510128"
---
# <span data-ttu-id="4f24e-101">Get-AzureBatchTaskCounts</span><span class="sxs-lookup"><span data-stu-id="4f24e-101">Get-AzureBatchTaskCounts</span></span>

## <span data-ttu-id="4f24e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4f24e-102">SYNOPSIS</span></span>
<span data-ttu-id="4f24e-103">Ottiene i conteggi delle attività per il processo specificato.</span><span class="sxs-lookup"><span data-stu-id="4f24e-103">Gets the task counts for the specified job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f24e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4f24e-104">SYNTAX</span></span>

### <span data-ttu-id="4f24e-105">ID</span><span class="sxs-lookup"><span data-stu-id="4f24e-105">Id</span></span>
```
Get-AzureBatchTaskCounts [-JobId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="4f24e-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="4f24e-106">ParentObject</span></span>
```
Get-AzureBatchTaskCounts [[-Job] <PSCloudJob>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="4f24e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4f24e-107">DESCRIPTION</span></span>
<span data-ttu-id="4f24e-108">Il cmdlet **Get-AzureBatchTaskCounts** ottiene il conteggio delle attività batch di Azure per un processo batch.</span><span class="sxs-lookup"><span data-stu-id="4f24e-108">The **Get-AzureBatchTaskCounts** cmdlet gets the Azure Batch tasks count for a Batch job.</span></span>
<span data-ttu-id="4f24e-109">Specificare un processo per il parametro *JobID* o per il parametro *Job* .</span><span class="sxs-lookup"><span data-stu-id="4f24e-109">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="4f24e-110">I conteggi delle attività offrono un conteggio delle attività tramite lo stato dell'attività attivo, in corso o completato e un conteggio delle attività che hanno avuto esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="4f24e-110">Task counts provide a count of the tasks by active, running or completed task state, and a count of tasks which succeeded or failed.</span></span> <span data-ttu-id="4f24e-111">Le attività nello stato di preparazione vengono conteggiate come in corso.</span><span class="sxs-lookup"><span data-stu-id="4f24e-111">Tasks in the preparing state are counted as running.</span></span> <span data-ttu-id="4f24e-112">Se validationStatus non è convalidato, il servizio batch non è stato in grado di controllare i conteggi degli Stati in base agli Stati delle attività riportati nell'API elenco attività.</span><span class="sxs-lookup"><span data-stu-id="4f24e-112">If the validationStatus is unvalidated, then the Batch service has not been able to check state counts against the task states as reported in the List Tasks API.</span></span> <span data-ttu-id="4f24e-113">ValidationStatus potrebbe non essere convalidato se il processo contiene più di 200.000 attività.</span><span class="sxs-lookup"><span data-stu-id="4f24e-113">The validationStatus may be unvalidated if the job contains more than 200,000 tasks.</span></span>

## <span data-ttu-id="4f24e-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4f24e-114">EXAMPLES</span></span>

### <span data-ttu-id="4f24e-115">Esempio 1: ottenere i conteggi delle attività in base all'ID</span><span class="sxs-lookup"><span data-stu-id="4f24e-115">Example 1: Get task counts by ID</span></span>
```
PS C:\> Get-AzureBatchTaskCounts -JobId "Job01" -Id "Task03" -BatchContext $Context
Active              : 1
Completed           : 0
Failed              : 0
Running             : 1
Succeeded           : 5
ValidationStatus    : Validated
```

<span data-ttu-id="4f24e-116">Questo comando consente di ottenere i conteggi delle attività per Job Job01.</span><span class="sxs-lookup"><span data-stu-id="4f24e-116">This command gets the task counts for job Job01.</span></span>
<span data-ttu-id="4f24e-117">Usa il cmdlet Get-AzureRmBatchAccountKeys per assegnare un contesto alla variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="4f24e-117">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="4f24e-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4f24e-118">PARAMETERS</span></span>

### <span data-ttu-id="4f24e-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="4f24e-119">-BatchContext</span></span>
<span data-ttu-id="4f24e-120">Istanza di BatchAccountContext da usare per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="4f24e-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="4f24e-121">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="4f24e-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="4f24e-122">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="4f24e-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="4f24e-123">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="4f24e-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="4f24e-124">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="4f24e-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f24e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f24e-125">-DefaultProfile</span></span>
<span data-ttu-id="4f24e-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4f24e-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f24e-127">-Job</span><span class="sxs-lookup"><span data-stu-id="4f24e-127">-Job</span></span>
<span data-ttu-id="4f24e-128">Specifica il processo che contiene le attività ottenute da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f24e-128">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="4f24e-129">Per ottenere un oggetto **PSCloudJob** , usa il cmdlet Get-AzureBatchJob.</span><span class="sxs-lookup"><span data-stu-id="4f24e-129">To obtain a **PSCloudJob** object, use the Get-AzureBatchJob cmdlet.</span></span>

```yaml
Type: PSCloudJob
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f24e-130">-JobId</span><span class="sxs-lookup"><span data-stu-id="4f24e-130">-JobId</span></span>
<span data-ttu-id="4f24e-131">ID del processo per cui viene conteggiato l'attività.</span><span class="sxs-lookup"><span data-stu-id="4f24e-131">The id of the job for which to get task counts.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="4f24e-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4f24e-132">INPUTS</span></span>

### <span data-ttu-id="4f24e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4f24e-133">System.String</span></span>
<span data-ttu-id="4f24e-134">Microsoft.Azure.Commands.Batch. Models. PSCloudJob Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4f24e-134">Microsoft.Azure.Commands.Batch.Models.PSCloudJob Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>


## <span data-ttu-id="4f24e-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4f24e-135">OUTPUTS</span></span>

### <span data-ttu-id="4f24e-136">Microsoft.Azure.Commands.Batch. Models. PSTaskCounts</span><span class="sxs-lookup"><span data-stu-id="4f24e-136">Microsoft.Azure.Commands.Batch.Models.PSTaskCounts</span></span>


## <span data-ttu-id="4f24e-137">Note</span><span class="sxs-lookup"><span data-stu-id="4f24e-137">NOTES</span></span>

## <span data-ttu-id="4f24e-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4f24e-138">RELATED LINKS</span></span>

[<span data-ttu-id="4f24e-139">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="4f24e-139">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="4f24e-140">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="4f24e-140">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="4f24e-141">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="4f24e-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)
