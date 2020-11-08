---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2BF5BDF8-3743-46FC-8E04-1A4EA920A2AF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 77b4d184ffbdb1d054f3d14aa3c51c8d2afc928b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029772"
---
# <span data-ttu-id="3413d-101">Get-AzureSchedulerJobHistory</span><span class="sxs-lookup"><span data-stu-id="3413d-101">Get-AzureSchedulerJobHistory</span></span>

## <span data-ttu-id="3413d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3413d-102">SYNOPSIS</span></span>
<span data-ttu-id="3413d-103">Ottiene la cronologia per un processo di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="3413d-103">Gets history for a scheduler job.</span></span>

## <span data-ttu-id="3413d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3413d-104">SYNTAX</span></span>

```
Get-AzureSchedulerJobHistory -Location <String> -JobCollectionName <String> -JobName <String>
 [-JobStatus <String>] [-Profile <AzureSMProfile>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

## <span data-ttu-id="3413d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3413d-105">DESCRIPTION</span></span>
<span data-ttu-id="3413d-106">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3413d-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="3413d-107">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="3413d-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="3413d-108">Il cmdlet **Get-AzureSchedulerJobHistory** ottiene la cronologia per un processo di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="3413d-108">The **Get-AzureSchedulerJobHistory** cmdlet gets the history for a scheduler job.</span></span>

## <span data-ttu-id="3413d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3413d-109">EXAMPLES</span></span>

### <span data-ttu-id="3413d-110">Esempio 1: ottenere la cronologia di un processo usando il relativo nome</span><span class="sxs-lookup"><span data-stu-id="3413d-110">Example 1: Get history for a job by using its name</span></span>
```
PS C:\> Get-AzureSchedulerJobHistory -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job01"
```

<span data-ttu-id="3413d-111">Questo comando consente di ottenere la cronologia del processo denominato Job01.</span><span class="sxs-lookup"><span data-stu-id="3413d-111">This command gets the history of the job named Job01.</span></span>
<span data-ttu-id="3413d-112">Tale processo appartiene alla raccolta processi denominata JobCollection01 nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="3413d-112">That job belongs to the job collection named JobCollection01 in the specified location.</span></span>

### <span data-ttu-id="3413d-113">Esempio 2: ottenere la cronologia per un processo non riuscito usando il relativo nome</span><span class="sxs-lookup"><span data-stu-id="3413d-113">Example 2: Get history for a failed job by using its name</span></span>
```
PS C:\> Get-AzureSchedulerJobHistory -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job12" -JobStatus "Failed"
```

<span data-ttu-id="3413d-114">Questo comando consente di ottenere la cronologia del processo denominato Job12 con stato non riuscito.</span><span class="sxs-lookup"><span data-stu-id="3413d-114">This command gets the history of the job named Job12 that has a status of Failed.</span></span>
<span data-ttu-id="3413d-115">Tale processo appartiene alla raccolta processi denominata JobCollection01 nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="3413d-115">That job belongs to the job collection named JobCollection01 in the specified location.</span></span>

## <span data-ttu-id="3413d-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3413d-116">PARAMETERS</span></span>

### <span data-ttu-id="3413d-117">-Primo</span><span class="sxs-lookup"><span data-stu-id="3413d-117">-First</span></span>
<span data-ttu-id="3413d-118">Ottiene solo il numero di oggetti specificato.</span><span class="sxs-lookup"><span data-stu-id="3413d-118">Gets only the specified number of objects.</span></span>
<span data-ttu-id="3413d-119">Immettere il numero di oggetti da ottenere.</span><span class="sxs-lookup"><span data-stu-id="3413d-119">Enter the number of objects to get.</span></span>

```yaml
Type: UInt64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3413d-120">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="3413d-120">-IncludeTotalCount</span></span>
<span data-ttu-id="3413d-121">Indica il numero totale di oggetti nel set di dati (un numero intero) seguito dagli oggetti selezionati.</span><span class="sxs-lookup"><span data-stu-id="3413d-121">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="3413d-122">Se il cmdlet non riesce a determinare il conteggio totale, Visualizza "numero totale sconosciuto".</span><span class="sxs-lookup"><span data-stu-id="3413d-122">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="3413d-123">Il numero intero ha una proprietà di precisione che indica l'affidabilità del valore di conteggio totale.</span><span class="sxs-lookup"><span data-stu-id="3413d-123">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="3413d-124">Il valore di precisione è compreso tra 0,0 e 1,0, dove 0,0 indica che il cmdlet non ha potuto contare gli oggetti, 1,0 significa che il conteggio è esatto e un valore compreso tra 0,0 e 1,0 è una stima sempre più attendibile.</span><span class="sxs-lookup"><span data-stu-id="3413d-124">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3413d-125">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="3413d-125">-JobCollectionName</span></span>
<span data-ttu-id="3413d-126">Specifica il nome di una raccolta processi dell'utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="3413d-126">Specifies the name of a scheduler job collection.</span></span>
<span data-ttu-id="3413d-127">Questo cmdlet consente di ottenere la cronologia di un processo che appartiene alla raccolta specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="3413d-127">This cmdlet gets the history for a job that belongs to the collection that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3413d-128">-JobName</span><span class="sxs-lookup"><span data-stu-id="3413d-128">-JobName</span></span>
<span data-ttu-id="3413d-129">Specifica il nome di un processo di pianificazione per cui ottenere la cronologia.</span><span class="sxs-lookup"><span data-stu-id="3413d-129">Specifies the name of a scheduler job for which to get the history.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3413d-130">-JobStatus</span><span class="sxs-lookup"><span data-stu-id="3413d-130">-JobStatus</span></span>
<span data-ttu-id="3413d-131">Specifica lo stato del processo di pianificazione per cui ottenere la cronologia.</span><span class="sxs-lookup"><span data-stu-id="3413d-131">Specifies the status of scheduler job for which to get the history.</span></span>
<span data-ttu-id="3413d-132">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="3413d-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3413d-133">Completato</span><span class="sxs-lookup"><span data-stu-id="3413d-133">Completed</span></span>
- <span data-ttu-id="3413d-134">Fallito</span><span class="sxs-lookup"><span data-stu-id="3413d-134">Failed</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3413d-135">-Posizione</span><span class="sxs-lookup"><span data-stu-id="3413d-135">-Location</span></span>
<span data-ttu-id="3413d-136">Specifica il nome della posizione che ospita il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="3413d-136">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="3413d-137">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="3413d-137">Valid values are:</span></span> 

- <span data-ttu-id="3413d-138">Ovunque in Asia</span><span class="sxs-lookup"><span data-stu-id="3413d-138">Anywhere Asia</span></span>
- <span data-ttu-id="3413d-139">Ovunque Europa</span><span class="sxs-lookup"><span data-stu-id="3413d-139">Anywhere Europe</span></span>
- <span data-ttu-id="3413d-140">Ovunque negli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="3413d-140">Anywhere US</span></span>
- <span data-ttu-id="3413d-141">Asia orientale</span><span class="sxs-lookup"><span data-stu-id="3413d-141">East Asia</span></span>
- <span data-ttu-id="3413d-142">Stati Uniti orientali</span><span class="sxs-lookup"><span data-stu-id="3413d-142">East US</span></span>
- <span data-ttu-id="3413d-143">Stati Uniti nord-centrale</span><span class="sxs-lookup"><span data-stu-id="3413d-143">North Central US</span></span>
- <span data-ttu-id="3413d-144">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="3413d-144">North Europe</span></span>
- <span data-ttu-id="3413d-145">Stati Uniti del centro sud</span><span class="sxs-lookup"><span data-stu-id="3413d-145">South Central US</span></span>
- <span data-ttu-id="3413d-146">Asia sud-orientale</span><span class="sxs-lookup"><span data-stu-id="3413d-146">Southeast Asia</span></span>
- <span data-ttu-id="3413d-147">Europa occidentale</span><span class="sxs-lookup"><span data-stu-id="3413d-147">West Europe</span></span>
- <span data-ttu-id="3413d-148">Ovest degli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="3413d-148">West US</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3413d-149">-Profile</span><span class="sxs-lookup"><span data-stu-id="3413d-149">-Profile</span></span>
<span data-ttu-id="3413d-150">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3413d-150">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3413d-151">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="3413d-151">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3413d-152">-Skip</span><span class="sxs-lookup"><span data-stu-id="3413d-152">-Skip</span></span>
<span data-ttu-id="3413d-153">Ignora il numero di oggetti specificato e quindi recupera gli oggetti rimanenti.</span><span class="sxs-lookup"><span data-stu-id="3413d-153">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="3413d-154">Immettere il numero di oggetti da ignorare.</span><span class="sxs-lookup"><span data-stu-id="3413d-154">Enter the number of objects to skip.</span></span>

```yaml
Type: UInt64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3413d-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3413d-155">CommonParameters</span></span>
<span data-ttu-id="3413d-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3413d-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3413d-157">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3413d-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3413d-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3413d-158">INPUTS</span></span>

## <span data-ttu-id="3413d-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3413d-159">OUTPUTS</span></span>

## <span data-ttu-id="3413d-160">Note</span><span class="sxs-lookup"><span data-stu-id="3413d-160">NOTES</span></span>

## <span data-ttu-id="3413d-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3413d-161">RELATED LINKS</span></span>

[<span data-ttu-id="3413d-162">Get-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="3413d-162">Get-AzureSchedulerJob</span></span>](./Get-AzureSchedulerJob.md)

[<span data-ttu-id="3413d-163">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="3413d-163">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)


