---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchtaskcount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
ms.openlocfilehash: 51e9053737b95113144d5421492f64623b425ff6
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2020
ms.locfileid: "93685331"
---
# <span data-ttu-id="0f660-101">Get-AzBatchTaskCount</span><span class="sxs-lookup"><span data-stu-id="0f660-101">Get-AzBatchTaskCount</span></span>

## <span data-ttu-id="0f660-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0f660-102">SYNOPSIS</span></span>
<span data-ttu-id="0f660-103">Ottiene i conteggi delle attività per il processo specificato.</span><span class="sxs-lookup"><span data-stu-id="0f660-103">Gets the task counts for the specified job.</span></span>

## <span data-ttu-id="0f660-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0f660-104">SYNTAX</span></span>

### <span data-ttu-id="0f660-105">ID</span><span class="sxs-lookup"><span data-stu-id="0f660-105">Id</span></span>
```
Get-AzBatchTaskCount [-JobId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f660-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="0f660-106">ParentObject</span></span>
```
Get-AzBatchTaskCount [[-Job] <PSCloudJob>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f660-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0f660-107">DESCRIPTION</span></span>
<span data-ttu-id="0f660-108">Il cmdlet **Get-AzBatchTaskCount** ottiene il conteggio delle attività batch di Azure per un processo batch.</span><span class="sxs-lookup"><span data-stu-id="0f660-108">The **Get-AzBatchTaskCount** cmdlet gets the Azure Batch tasks count for a Batch job.</span></span>
<span data-ttu-id="0f660-109">Specificare un processo per il parametro *JobID* o per il parametro *Job* .</span><span class="sxs-lookup"><span data-stu-id="0f660-109">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="0f660-110">I conteggi delle attività offrono un conteggio delle attività tramite lo stato dell'attività attivo, in corso o completato e un conteggio delle attività che hanno avuto esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="0f660-110">Task counts provide a count of the tasks by active, running or completed task state, and a count of tasks which succeeded or failed.</span></span> <span data-ttu-id="0f660-111">Le attività nello stato di preparazione vengono conteggiate come in corso.</span><span class="sxs-lookup"><span data-stu-id="0f660-111">Tasks in the preparing state are counted as running.</span></span> <span data-ttu-id="0f660-112">Se validationStatus non è convalidato, il servizio batch non è stato in grado di controllare i conteggi degli Stati in base agli Stati delle attività riportati nell'API elenco attività.</span><span class="sxs-lookup"><span data-stu-id="0f660-112">If the validationStatus is unvalidated, then the Batch service has not been able to check state counts against the task states as reported in the List Tasks API.</span></span> <span data-ttu-id="0f660-113">ValidationStatus potrebbe non essere convalidato se il processo contiene più di 200.000 attività.</span><span class="sxs-lookup"><span data-stu-id="0f660-113">The validationStatus may be unvalidated if the job contains more than 200,000 tasks.</span></span>

## <span data-ttu-id="0f660-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0f660-114">EXAMPLES</span></span>

### <span data-ttu-id="0f660-115">Esempio 1: ottenere i conteggi delle attività in base all'ID</span><span class="sxs-lookup"><span data-stu-id="0f660-115">Example 1: Get task counts by ID</span></span>
```
PS C:\> Get-AzBatchTaskCount -JobId "Job01" -Id "Task03" -BatchContext $Context
Active              : 1
Completed           : 0
Failed              : 0
Running             : 1
Succeeded           : 5
ValidationStatus    : Validated
```

<span data-ttu-id="0f660-116">Questo comando consente di ottenere i conteggi delle attività per Job Job01.</span><span class="sxs-lookup"><span data-stu-id="0f660-116">This command gets the task counts for job Job01.</span></span>
<span data-ttu-id="0f660-117">Usa il cmdlet Get-AzBatchAccountKeys per assegnare un contesto alla variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="0f660-117">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="0f660-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0f660-118">PARAMETERS</span></span>

### <span data-ttu-id="0f660-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="0f660-119">-BatchContext</span></span>
<span data-ttu-id="0f660-120">Istanza di BatchAccountContext da usare per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="0f660-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="0f660-121">Se si usa il cmdlet Get-AzBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="0f660-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="0f660-122">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="0f660-122">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="0f660-123">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="0f660-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="0f660-124">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="0f660-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="0f660-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f660-125">-DefaultProfile</span></span>
<span data-ttu-id="0f660-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0f660-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f660-127">-Job</span><span class="sxs-lookup"><span data-stu-id="0f660-127">-Job</span></span>
<span data-ttu-id="0f660-128">Specifica il processo che contiene le attività ottenute da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f660-128">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="0f660-129">Per ottenere un oggetto **PSCloudJob** , usa il cmdlet Get-AzBatchJob.</span><span class="sxs-lookup"><span data-stu-id="0f660-129">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f660-130">-JobId</span><span class="sxs-lookup"><span data-stu-id="0f660-130">-JobId</span></span>
<span data-ttu-id="0f660-131">ID del processo per cui viene conteggiato l'attività.</span><span class="sxs-lookup"><span data-stu-id="0f660-131">The id of the job for which to get task counts.</span></span>

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

### <span data-ttu-id="0f660-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f660-132">CommonParameters</span></span>
<span data-ttu-id="0f660-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f660-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f660-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f660-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f660-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0f660-135">INPUTS</span></span>

### <span data-ttu-id="0f660-136">System. String</span><span class="sxs-lookup"><span data-stu-id="0f660-136">System.String</span></span>

### <span data-ttu-id="0f660-137">Microsoft.Azure.Commands.Batch. Models. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="0f660-137">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="0f660-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0f660-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="0f660-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0f660-139">OUTPUTS</span></span>

### <span data-ttu-id="0f660-140">Microsoft.Azure.Commands.Batch. Models. PSTaskCounts</span><span class="sxs-lookup"><span data-stu-id="0f660-140">Microsoft.Azure.Commands.Batch.Models.PSTaskCounts</span></span>

## <span data-ttu-id="0f660-141">Note</span><span class="sxs-lookup"><span data-stu-id="0f660-141">NOTES</span></span>

## <span data-ttu-id="0f660-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0f660-142">RELATED LINKS</span></span>

[<span data-ttu-id="0f660-143">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="0f660-143">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="0f660-144">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="0f660-144">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="0f660-145">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="0f660-145">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)
