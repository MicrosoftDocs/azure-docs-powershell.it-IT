---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: CF3548F6-03FE-44D6-AA2C-1015611C657A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0423fe51a047385ef6395075dd116b4d4189c667
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023510"
---
# <span data-ttu-id="498a5-101">Get-AzureStorSimpleTask</span><span class="sxs-lookup"><span data-stu-id="498a5-101">Get-AzureStorSimpleTask</span></span>

## <span data-ttu-id="498a5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="498a5-102">SYNOPSIS</span></span>
<span data-ttu-id="498a5-103">Ottiene lo stato di un'attività in un dispositivo StorSimple.</span><span class="sxs-lookup"><span data-stu-id="498a5-103">Gets status of a task on a StorSimple device.</span></span>

## <span data-ttu-id="498a5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="498a5-104">SYNTAX</span></span>

```
Get-AzureStorSimpleTask -InstanceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="498a5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="498a5-105">DESCRIPTION</span></span>
<span data-ttu-id="498a5-106">Il cmdlet **Get-AzureStorSimpleTask** recupera lo stato di un'attività che viene eseguita in modo asincrono in un dispositivo StorSimple di Azure.</span><span class="sxs-lookup"><span data-stu-id="498a5-106">The **Get-AzureStorSimpleTask** cmdlet retrieves the status of a task that runs asynchronously on an Azure StorSimple device.</span></span>

<span data-ttu-id="498a5-107">Durante la gestione di un dispositivo StorSimple, la maggior parte delle operazioni di creazione, lettura, aggiornamento ed eliminazione può essere eseguita in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="498a5-107">While you manage a StorSimple device, most create, read, update, and delete actions can run asynchronously.</span></span>
<span data-ttu-id="498a5-108">Windows PowerShell restituisce un **taskId**.</span><span class="sxs-lookup"><span data-stu-id="498a5-108">Windows PowerShell returns a **TaskId**.</span></span>
<span data-ttu-id="498a5-109">Usa l'ID per ottenere lo stato corrente dell'attività.</span><span class="sxs-lookup"><span data-stu-id="498a5-109">Use the ID to get the current status of the task.</span></span>

## <span data-ttu-id="498a5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="498a5-110">EXAMPLES</span></span>

### <span data-ttu-id="498a5-111">Esempio 1: ottenere lo stato di un'attività</span><span class="sxs-lookup"><span data-stu-id="498a5-111">Example 1: Get the status of a task</span></span>
```
PS C:\>Get-AzureStorSimpleTask -TaskId "53816d8d-a8b5-4c1d-a177-e59007608d6d"
VERBOSE: ClientRequestId: d9c1e8a7-994f-4698-8b42-064600b45cad_PS
VERBOSE: ClientRequestId: aae17c82-6fd3-435e-a965-1c66b3c955fe_PS


AsyncTaskAggregatedResult : Succeeded
Error                     : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
Result                    : Succeeded
Status                    : Completed
TaskId                    : 53816d8d-a8b5-4c1d-a177-e59007608d6d
TaskSteps                 : {}
StatusCode                : OK
RequestId                 : e9174990825750bba69383748f23019c
```

<span data-ttu-id="498a5-112">Questo comando ottiene lo stato dell'attività con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="498a5-112">This command gets the status of the task that has the specified ID.</span></span>
<span data-ttu-id="498a5-113">I risultati indicano che l'attività ha uno stato completato e il risultato è riuscito.</span><span class="sxs-lookup"><span data-stu-id="498a5-113">The results show that the task has a status of completed and a result of successful.</span></span>

## <span data-ttu-id="498a5-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="498a5-114">PARAMETERS</span></span>

### <span data-ttu-id="498a5-115">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="498a5-115">-InstanceId</span></span>
<span data-ttu-id="498a5-116">Specifica l'ID dell'attività per cui questo cmdlet tiene traccia dello stato.</span><span class="sxs-lookup"><span data-stu-id="498a5-116">Specifies the ID of the task for which this cmdlet tracks status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TaskId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="498a5-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="498a5-117">-Profile</span></span>
<span data-ttu-id="498a5-118">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="498a5-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="498a5-119">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="498a5-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="498a5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="498a5-120">CommonParameters</span></span>
<span data-ttu-id="498a5-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="498a5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="498a5-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="498a5-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="498a5-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="498a5-123">INPUTS</span></span>

### <span data-ttu-id="498a5-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="498a5-124">None</span></span>

## <span data-ttu-id="498a5-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="498a5-125">OUTPUTS</span></span>

### <span data-ttu-id="498a5-126">JobStatusInfo</span><span class="sxs-lookup"><span data-stu-id="498a5-126">JobStatusInfo</span></span>
<span data-ttu-id="498a5-127">Questo cmdlet restituisce un oggetto **TaskStatusInfo** che contiene i campi seguenti:</span><span class="sxs-lookup"><span data-stu-id="498a5-127">This cmdlet returns a **TaskStatusInfo** object which contains the following fields:</span></span> 

- <span data-ttu-id="498a5-128">**Errore**.</span><span class="sxs-lookup"><span data-stu-id="498a5-128">**Error**.</span></span>
<span data-ttu-id="498a5-129">**ErrorDetails** , che contiene il **codice** e il **messaggio**.</span><span class="sxs-lookup"><span data-stu-id="498a5-129">**ErrorDetails** , which contains **Code** and **Message**.</span></span>
- <span data-ttu-id="498a5-130">**TaskId**.</span><span class="sxs-lookup"><span data-stu-id="498a5-130">**TaskId**.</span></span>
<span data-ttu-id="498a5-131">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="498a5-131">**String**.</span></span>
<span data-ttu-id="498a5-132">ID dell'attività per cui viene restituito lo stato.</span><span class="sxs-lookup"><span data-stu-id="498a5-132">The ID of the task for which status is returned.</span></span>
- <span data-ttu-id="498a5-133">**TaskSteps**.</span><span class="sxs-lookup"><span data-stu-id="498a5-133">**TaskSteps**.</span></span>
<span data-ttu-id="498a5-134">**IList \<TaskStep\>**.</span><span class="sxs-lookup"><span data-stu-id="498a5-134">**IList\<TaskStep\>**.</span></span>
<span data-ttu-id="498a5-135">Ogni oggetto **TaskStep** contiene **Dettagli** , **ErrorCode** , **messaggio** , **risultato** e **stato**.</span><span class="sxs-lookup"><span data-stu-id="498a5-135">Each **TaskStep** object contains **Detail** , **ErrorCode** , **Message** , **Result** , and **Status**.</span></span>
- <span data-ttu-id="498a5-136">**Risultato**.</span><span class="sxs-lookup"><span data-stu-id="498a5-136">**Result**.</span></span>
<span data-ttu-id="498a5-137">**TaskResult** , che contiene il risultato complessivo dell'attività.</span><span class="sxs-lookup"><span data-stu-id="498a5-137">**TaskResult** , which contains the overall result of the task.</span></span>
<span data-ttu-id="498a5-138">I valori validi sono: non riuscito, riuscito, PartialSuccess, annullato e non valido.</span><span class="sxs-lookup"><span data-stu-id="498a5-138">Valid values are: Failed, Succeeded, PartialSuccess, Cancelled, and Invalid.</span></span>
- <span data-ttu-id="498a5-139">**Stato**.</span><span class="sxs-lookup"><span data-stu-id="498a5-139">**Status**.</span></span>
<span data-ttu-id="498a5-140">**TaskStatus** , che contiene lo stato di avanzamento complessivo dell'attività.</span><span class="sxs-lookup"><span data-stu-id="498a5-140">**TaskStatus** , which contains the overall running status of the task.</span></span>
<span data-ttu-id="498a5-141">I valori validi sono: InProgress, non valido e completato.</span><span class="sxs-lookup"><span data-stu-id="498a5-141">Valid values are: Inprogress, Invalid, and Completed.</span></span>
- <span data-ttu-id="498a5-142">**TaskResult**.</span><span class="sxs-lookup"><span data-stu-id="498a5-142">**TaskResult**.</span></span>
<span data-ttu-id="498a5-143">**TaskResult** , un valore calcolato in base al **risultato** e **allo stato**.</span><span class="sxs-lookup"><span data-stu-id="498a5-143">**TaskResult** , a value computed based on **Result** and **Status**.</span></span>
<span data-ttu-id="498a5-144">I valori validi sono: non riuscito, riuscito, InProgress, PartialSuccess, annullato e non valido.</span><span class="sxs-lookup"><span data-stu-id="498a5-144">Valid values are: Failed, Succeeded, InProgress, PartialSuccess, Cancelled, and Invalid.</span></span>

## <span data-ttu-id="498a5-145">Note</span><span class="sxs-lookup"><span data-stu-id="498a5-145">NOTES</span></span>

## <span data-ttu-id="498a5-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="498a5-146">RELATED LINKS</span></span>

