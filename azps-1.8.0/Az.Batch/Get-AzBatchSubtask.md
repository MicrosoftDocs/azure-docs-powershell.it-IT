---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 7D0D8B46-4BF0-47D5-9261-3306AEB9E7DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchsubtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSubtask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSubtask.md
ms.openlocfilehash: 463f19b5ed459f0c2b2f4a4fdeff40bf69db2682
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684927"
---
# <span data-ttu-id="09b85-101">Get-AzBatchSubtask</span><span class="sxs-lookup"><span data-stu-id="09b85-101">Get-AzBatchSubtask</span></span>

## <span data-ttu-id="09b85-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="09b85-102">SYNOPSIS</span></span>
<span data-ttu-id="09b85-103">Ottiene le informazioni sulla sottoattività dell'attività specificata.</span><span class="sxs-lookup"><span data-stu-id="09b85-103">Gets the subtask information of the specified task.</span></span>

## <span data-ttu-id="09b85-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="09b85-104">SYNTAX</span></span>

### <span data-ttu-id="09b85-105">ODataFilter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="09b85-105">ODataFilter (Default)</span></span>
```
Get-AzBatchSubtask [-JobId] <String> [-TaskId] <String> [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09b85-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="09b85-106">ParentObject</span></span>
```
Get-AzBatchSubtask [[-Task] <PSCloudTask>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09b85-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="09b85-107">DESCRIPTION</span></span>
<span data-ttu-id="09b85-108">Il cmdlet **Get-AzBatchSubtask** recupera le informazioni sulla sottoattività relative all'attività specificata.</span><span class="sxs-lookup"><span data-stu-id="09b85-108">The **Get-AzBatchSubtask** cmdlet retrieves the subtask information about the specified task.</span></span>
<span data-ttu-id="09b85-109">Le sottoattività offrono l'elaborazione parallela per singole attività e consentono un monitoraggio preciso dell'esecuzione e dello stato di avanzamento delle attività.</span><span class="sxs-lookup"><span data-stu-id="09b85-109">Subtasks provide parallel processing for individual tasks, and enable precise monitoring of task execution and progress.</span></span>

## <span data-ttu-id="09b85-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="09b85-110">EXAMPLES</span></span>

### <span data-ttu-id="09b85-111">Esempio 1: restituire tutte le sottoattività per un'attività specificata</span><span class="sxs-lookup"><span data-stu-id="09b85-111">Example 1: Return all subtasks for a specified task</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchSubtask -JobId "Job-01" -TaskID "myTask" -BatchContext $Context
```

<span data-ttu-id="09b85-112">Questi comandi restituiscono tutte le sottoattività dell'attività con l'ID attività.</span><span class="sxs-lookup"><span data-stu-id="09b85-112">These commands return all the subtasks for the task with the ID myTask.</span></span>
<span data-ttu-id="09b85-113">A questo scopo, il primo comando nell'esempio crea un riferimento a un oggetto alle chiavi dell'account per l'account batch contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="09b85-113">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="09b85-114">Questo riferimento oggetto è archiviato in una variabile denominata $context.</span><span class="sxs-lookup"><span data-stu-id="09b85-114">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="09b85-115">Il secondo comando usa quindi il riferimento oggetto e il cmdlet **Get-AzBatchSubtask** per restituire tutte le sottoattività per la mia attività, un'attività che viene eseguita come parte del processo di job-01.</span><span class="sxs-lookup"><span data-stu-id="09b85-115">The second command then uses that object reference and the **Get-AzBatchSubtask** cmdlet to return all the subtasks for myTask, a task that runs as part of job Job-01.</span></span>

## <span data-ttu-id="09b85-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="09b85-116">PARAMETERS</span></span>

### <span data-ttu-id="09b85-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="09b85-117">-BatchContext</span></span>
<span data-ttu-id="09b85-118">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="09b85-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="09b85-119">Se si usa il cmdlet Get-AzBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="09b85-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="09b85-120">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="09b85-120">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="09b85-121">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="09b85-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="09b85-122">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="09b85-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="09b85-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09b85-123">-DefaultProfile</span></span>
<span data-ttu-id="09b85-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="09b85-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09b85-125">-JobId</span><span class="sxs-lookup"><span data-stu-id="09b85-125">-JobId</span></span>
<span data-ttu-id="09b85-126">Specifica l'ID del processo che contiene l'attività con le sottoattività ottenute da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09b85-126">Specifies the ID of the job that contains the task whose subtasks this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09b85-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="09b85-127">-MaxCount</span></span>
<span data-ttu-id="09b85-128">Specifica il numero massimo di sottoattività da restituire.</span><span class="sxs-lookup"><span data-stu-id="09b85-128">Specifies the maximum number of subtasks to return.</span></span>
<span data-ttu-id="09b85-129">Se specifichi un valore pari a zero (0) o meno, il cmdlet non usa un limite superiore.</span><span class="sxs-lookup"><span data-stu-id="09b85-129">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="09b85-130">Il valore predefinito è 1000.</span><span class="sxs-lookup"><span data-stu-id="09b85-130">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09b85-131">-Attività</span><span class="sxs-lookup"><span data-stu-id="09b85-131">-Task</span></span>
<span data-ttu-id="09b85-132">Specifica un riferimento a un oggetto all'attività che contiene le sottoattività restituite dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09b85-132">Specifies an object reference to the task that contain the subtasks that this cmdlet returns.</span></span>
<span data-ttu-id="09b85-133">Questo riferimento all'oggetto viene creato usando il cmdlet Get-AzBatchTask e archiviando l'oggetto restituito in una variabile.</span><span class="sxs-lookup"><span data-stu-id="09b85-133">This object reference is created by using the Get-AzBatchTask cmdlet and storing the returned object in a variable.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09b85-134">-TaskId</span><span class="sxs-lookup"><span data-stu-id="09b85-134">-TaskId</span></span>
<span data-ttu-id="09b85-135">Specifica l'ID dell'attività di cui viene restituito il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09b85-135">Specifies the ID of the task whose subtasks this cmdlet returns.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09b85-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09b85-136">CommonParameters</span></span>
<span data-ttu-id="09b85-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09b85-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09b85-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09b85-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09b85-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="09b85-139">INPUTS</span></span>

### <span data-ttu-id="09b85-140">System. String</span><span class="sxs-lookup"><span data-stu-id="09b85-140">System.String</span></span>

### <span data-ttu-id="09b85-141">Microsoft.Azure.Commands.Batch. Models. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="09b85-141">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="09b85-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="09b85-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="09b85-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="09b85-143">OUTPUTS</span></span>

### <span data-ttu-id="09b85-144">Microsoft.Azure.Commands.Batch. Models. PSSubtaskInformation</span><span class="sxs-lookup"><span data-stu-id="09b85-144">Microsoft.Azure.Commands.Batch.Models.PSSubtaskInformation</span></span>

## <span data-ttu-id="09b85-145">Note</span><span class="sxs-lookup"><span data-stu-id="09b85-145">NOTES</span></span>

## <span data-ttu-id="09b85-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="09b85-146">RELATED LINKS</span></span>

[<span data-ttu-id="09b85-147">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="09b85-147">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)


