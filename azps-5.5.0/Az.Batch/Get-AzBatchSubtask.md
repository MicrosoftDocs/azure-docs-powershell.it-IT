---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 7D0D8B46-4BF0-47D5-9261-3306AEB9E7DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchsubtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSubtask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSubtask.md
ms.openlocfilehash: 4a1278734e6c9f40dc7495acb92f847d7b2cd32d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197095"
---
# <span data-ttu-id="105bd-101">Get-AzBatchSubtask</span><span class="sxs-lookup"><span data-stu-id="105bd-101">Get-AzBatchSubtask</span></span>

## <span data-ttu-id="105bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="105bd-102">SYNOPSIS</span></span>
<span data-ttu-id="105bd-103">Ottiene le informazioni sulle sottoattività dell'attività specificata.</span><span class="sxs-lookup"><span data-stu-id="105bd-103">Gets the subtask information of the specified task.</span></span>

## <span data-ttu-id="105bd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="105bd-104">SYNTAX</span></span>

### <span data-ttu-id="105bd-105">ODataFilter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="105bd-105">ODataFilter (Default)</span></span>
```
Get-AzBatchSubtask [-JobId] <String> [-TaskId] <String> [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="105bd-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="105bd-106">ParentObject</span></span>
```
Get-AzBatchSubtask [[-Task] <PSCloudTask>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="105bd-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="105bd-107">DESCRIPTION</span></span>
<span data-ttu-id="105bd-108">Il cmdlet **Get-AzBatchSubtask** recupera le informazioni sulle sottoattività relative all'attività specificata.</span><span class="sxs-lookup"><span data-stu-id="105bd-108">The **Get-AzBatchSubtask** cmdlet retrieves the subtask information about the specified task.</span></span>
<span data-ttu-id="105bd-109">Le sottoattività forniscono l'elaborazione parallela per le singole attività e consentono di monitorare in modo preciso l'esecuzione e l'avanzamento delle attività.</span><span class="sxs-lookup"><span data-stu-id="105bd-109">Subtasks provide parallel processing for individual tasks, and enable precise monitoring of task execution and progress.</span></span>

## <span data-ttu-id="105bd-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="105bd-110">EXAMPLES</span></span>

### <span data-ttu-id="105bd-111">Esempio 1: Restituire tutte le sottoattività per un'attività specificata</span><span class="sxs-lookup"><span data-stu-id="105bd-111">Example 1: Return all subtasks for a specified task</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchSubtask -JobId "Job-01" -TaskID "myTask" -BatchContext $Context
```

<span data-ttu-id="105bd-112">Questi comandi restituiscono tutte le sottoattività dell'attività con ID attività.</span><span class="sxs-lookup"><span data-stu-id="105bd-112">These commands return all the subtasks for the task with the ID myTask.</span></span>
<span data-ttu-id="105bd-113">A questo scopo, il primo comando dell'esempio crea un riferimento a un oggetto alle chiavi dell'account batch contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="105bd-113">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="105bd-114">Questo riferimento all'oggetto è archiviato in una variabile denominata $context.</span><span class="sxs-lookup"><span data-stu-id="105bd-114">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="105bd-115">Il secondo comando usa quindi il riferimento all'oggetto e il cmdlet **Get-AzBatchSubtask** per restituire tutte le sottoattività di myTask, un'attività che viene eseguita come parte del processo Job-01.</span><span class="sxs-lookup"><span data-stu-id="105bd-115">The second command then uses that object reference and the **Get-AzBatchSubtask** cmdlet to return all the subtasks for myTask, a task that runs as part of job Job-01.</span></span>

## <span data-ttu-id="105bd-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="105bd-116">PARAMETERS</span></span>

### <span data-ttu-id="105bd-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="105bd-117">-BatchContext</span></span>
<span data-ttu-id="105bd-118">Specifica **l'istanza BatchAccountContext** che questo cmdlet usa per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="105bd-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="105bd-119">Se si usa il cmdlet Get-AzBatchAccount per ottenere BatchAccountContext, verrà usata l'autenticazione di Azure Active Directory quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="105bd-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="105bd-120">Per usare invece l'autenticazione della chiave condivisa, usare il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.</span><span class="sxs-lookup"><span data-stu-id="105bd-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="105bd-121">Quando si usa l'autenticazione con chiave condivisa, per impostazione predefinita viene usata la chiave di accesso primario.</span><span class="sxs-lookup"><span data-stu-id="105bd-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="105bd-122">Per modificare la chiave da usare, impostare la proprietà BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="105bd-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="105bd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="105bd-123">-DefaultProfile</span></span>
<span data-ttu-id="105bd-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="105bd-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="105bd-125">-JobId</span><span class="sxs-lookup"><span data-stu-id="105bd-125">-JobId</span></span>
<span data-ttu-id="105bd-126">Specifica l'ID del processo che contiene l'attività per cui vengono recuperate le sottoattività di questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="105bd-126">Specifies the ID of the job that contains the task whose subtasks this cmdlet gets.</span></span>

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

### <span data-ttu-id="105bd-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="105bd-127">-MaxCount</span></span>
<span data-ttu-id="105bd-128">Specifica il numero massimo di sottoattività da restituire.</span><span class="sxs-lookup"><span data-stu-id="105bd-128">Specifies the maximum number of subtasks to return.</span></span>
<span data-ttu-id="105bd-129">Se si specifica un valore uguale o inferiore a zero (0), il cmdlet non usa un limite superiore.</span><span class="sxs-lookup"><span data-stu-id="105bd-129">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="105bd-130">Il valore predefinito è 1000.</span><span class="sxs-lookup"><span data-stu-id="105bd-130">The default value is 1000.</span></span>

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

### <span data-ttu-id="105bd-131">-Attività</span><span class="sxs-lookup"><span data-stu-id="105bd-131">-Task</span></span>
<span data-ttu-id="105bd-132">Specifica un riferimento a un oggetto all'attività che contiene le sottoattività restituite dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="105bd-132">Specifies an object reference to the task that contain the subtasks that this cmdlet returns.</span></span>
<span data-ttu-id="105bd-133">Questo riferimento all'oggetto viene creato usando il cmdlet Get-AzBatchTask e archiviando l'oggetto restituito in una variabile.</span><span class="sxs-lookup"><span data-stu-id="105bd-133">This object reference is created by using the Get-AzBatchTask cmdlet and storing the returned object in a variable.</span></span>

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

### <span data-ttu-id="105bd-134">-TaskId</span><span class="sxs-lookup"><span data-stu-id="105bd-134">-TaskId</span></span>
<span data-ttu-id="105bd-135">Specifica l'ID dell'attività di cui questo cmdlet restituisce le sottoattività.</span><span class="sxs-lookup"><span data-stu-id="105bd-135">Specifies the ID of the task whose subtasks this cmdlet returns.</span></span>

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

### <span data-ttu-id="105bd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="105bd-136">CommonParameters</span></span>
<span data-ttu-id="105bd-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="105bd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="105bd-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="105bd-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="105bd-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="105bd-139">INPUTS</span></span>

### <span data-ttu-id="105bd-140">System.String</span><span class="sxs-lookup"><span data-stu-id="105bd-140">System.String</span></span>

### <span data-ttu-id="105bd-141">Microsoft.Azure.Commands.Batch. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="105bd-141">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="105bd-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="105bd-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="105bd-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="105bd-143">OUTPUTS</span></span>

### <span data-ttu-id="105bd-144">Microsoft.Azure.Commands.Batch. Models.PSSubtaskInformation</span><span class="sxs-lookup"><span data-stu-id="105bd-144">Microsoft.Azure.Commands.Batch.Models.PSSubtaskInformation</span></span>

## <span data-ttu-id="105bd-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="105bd-145">NOTES</span></span>

## <span data-ttu-id="105bd-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="105bd-146">RELATED LINKS</span></span>

[<span data-ttu-id="105bd-147">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="105bd-147">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)


