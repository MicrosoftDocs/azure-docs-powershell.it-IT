---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchtaskcount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
ms.openlocfilehash: d1f493556a1ff1007073611338b937ef0715c164
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205226"
---
# <span data-ttu-id="eedfd-101">Get-AzBatchTaskCount</span><span class="sxs-lookup"><span data-stu-id="eedfd-101">Get-AzBatchTaskCount</span></span>

## <span data-ttu-id="eedfd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eedfd-102">SYNOPSIS</span></span>
<span data-ttu-id="eedfd-103">Ottiene il conteggio delle attività per il processo specificato.</span><span class="sxs-lookup"><span data-stu-id="eedfd-103">Gets the task counts for the specified job.</span></span>

## <span data-ttu-id="eedfd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eedfd-104">SYNTAX</span></span>

### <span data-ttu-id="eedfd-105">ID</span><span class="sxs-lookup"><span data-stu-id="eedfd-105">Id</span></span>
```
Get-AzBatchTaskCount [-JobId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eedfd-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="eedfd-106">ParentObject</span></span>
```
Get-AzBatchTaskCount [[-Job] <PSCloudJob>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eedfd-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="eedfd-107">DESCRIPTION</span></span>
<span data-ttu-id="eedfd-108">Il **cmdlet Get-AzBatchTaskCount** ottiene il numero di attività batch di Azure per un processo batch.</span><span class="sxs-lookup"><span data-stu-id="eedfd-108">The **Get-AzBatchTaskCount** cmdlet gets the Azure Batch tasks count for a Batch job.</span></span>
<span data-ttu-id="eedfd-109">Specificare un processo usando il *parametro JobId* o *Job.*</span><span class="sxs-lookup"><span data-stu-id="eedfd-109">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="eedfd-110">Il numero di attività fornisce un conteggio delle attività per stato di attività attive, in esecuzione o completate e un numero di attività che ha avuto esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="eedfd-110">Task counts provide a count of the tasks by active, running or completed task state, and a count of tasks which succeeded or failed.</span></span> <span data-ttu-id="eedfd-111">Le attività in stato di preparazione vengono conteggiate come in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="eedfd-111">Tasks in the preparing state are counted as running.</span></span> <span data-ttu-id="eedfd-112">Se validationStatus non è convalidato, il servizio batch non è stato in grado di controllare il conteggio dello stato rispetto agli stati dell'attività, come riportato nell'API Attività elenco.</span><span class="sxs-lookup"><span data-stu-id="eedfd-112">If the validationStatus is unvalidated, then the Batch service has not been able to check state counts against the task states as reported in the List Tasks API.</span></span> <span data-ttu-id="eedfd-113">Lo stato di convalida potrebbe non essere convalidato se il processo contiene più di 200.000 attività.</span><span class="sxs-lookup"><span data-stu-id="eedfd-113">The validationStatus may be unvalidated if the job contains more than 200,000 tasks.</span></span>

## <span data-ttu-id="eedfd-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eedfd-114">EXAMPLES</span></span>

### <span data-ttu-id="eedfd-115">Esempio 1: Ottenere il conteggio delle attività per ID</span><span class="sxs-lookup"><span data-stu-id="eedfd-115">Example 1: Get task counts by ID</span></span>
```
PS C:\> Get-AzBatchTaskCount -JobId "Job01" -Id "Task03" -BatchContext $Context
Active              : 1
Completed           : 0
Failed              : 0
Running             : 1
Succeeded           : 5
ValidationStatus    : Validated
```

<span data-ttu-id="eedfd-116">Questo comando recupera il conteggio delle attività per il processo Job01.</span><span class="sxs-lookup"><span data-stu-id="eedfd-116">This command gets the task counts for job Job01.</span></span>
<span data-ttu-id="eedfd-117">Usare il cmdlet Get-AzBatchAccountKey per assegnare un contesto alla $Context variabile.</span><span class="sxs-lookup"><span data-stu-id="eedfd-117">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="eedfd-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eedfd-118">PARAMETERS</span></span>

### <span data-ttu-id="eedfd-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="eedfd-119">-BatchContext</span></span>
<span data-ttu-id="eedfd-120">Istanza BatchAccountContext da usare quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="eedfd-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="eedfd-121">Se si usa il cmdlet Get-AzBatchAccount per ottenere BatchAccountContext, verrà usata l'autenticazione di Azure Active Directory quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="eedfd-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="eedfd-122">Per usare invece l'autenticazione della chiave condivisa, usare il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.</span><span class="sxs-lookup"><span data-stu-id="eedfd-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="eedfd-123">Quando si usa l'autenticazione con chiave condivisa, per impostazione predefinita viene usata la chiave di accesso primario.</span><span class="sxs-lookup"><span data-stu-id="eedfd-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="eedfd-124">Per modificare la chiave da usare, impostare la proprietà BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="eedfd-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="eedfd-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eedfd-125">-DefaultProfile</span></span>
<span data-ttu-id="eedfd-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eedfd-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eedfd-127">-Job</span><span class="sxs-lookup"><span data-stu-id="eedfd-127">-Job</span></span>
<span data-ttu-id="eedfd-128">Specifica il processo che contiene le attività recuperate da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eedfd-128">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="eedfd-129">Per ottenere un **oggetto PSCloudJob,** usare il cmdlet Get-AzBatchJob.</span><span class="sxs-lookup"><span data-stu-id="eedfd-129">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="eedfd-130">-JobId</span><span class="sxs-lookup"><span data-stu-id="eedfd-130">-JobId</span></span>
<span data-ttu-id="eedfd-131">ID del processo per cui ottenere il conteggio delle attività.</span><span class="sxs-lookup"><span data-stu-id="eedfd-131">The id of the job for which to get task counts.</span></span>

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

### <span data-ttu-id="eedfd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eedfd-132">CommonParameters</span></span>
<span data-ttu-id="eedfd-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eedfd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eedfd-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="eedfd-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eedfd-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="eedfd-135">INPUTS</span></span>

### <span data-ttu-id="eedfd-136">System.String</span><span class="sxs-lookup"><span data-stu-id="eedfd-136">System.String</span></span>

### <span data-ttu-id="eedfd-137">Microsoft.Azure.Commands.Batch. Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="eedfd-137">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="eedfd-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="eedfd-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="eedfd-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eedfd-139">OUTPUTS</span></span>

### <span data-ttu-id="eedfd-140">Microsoft.Azure.Commands.Batch. Models.PSTaskCounts</span><span class="sxs-lookup"><span data-stu-id="eedfd-140">Microsoft.Azure.Commands.Batch.Models.PSTaskCounts</span></span>

## <span data-ttu-id="eedfd-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="eedfd-141">NOTES</span></span>

## <span data-ttu-id="eedfd-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eedfd-142">RELATED LINKS</span></span>

[<span data-ttu-id="eedfd-143">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="eedfd-143">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="eedfd-144">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="eedfd-144">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="eedfd-145">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="eedfd-145">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
