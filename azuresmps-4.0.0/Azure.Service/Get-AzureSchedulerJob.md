---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8EED9813-5106-4D6C-B869-97BCBD7845AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67e354616161ad7f2d2467a37b92c355c7c8c39e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029773"
---
# <span data-ttu-id="559c9-101">Get-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="559c9-101">Get-AzureSchedulerJob</span></span>

## <span data-ttu-id="559c9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="559c9-102">SYNOPSIS</span></span>
<span data-ttu-id="559c9-103">Ottiene un elenco dei processi di pianificazione o di un processo di pianificazione specifico.</span><span class="sxs-lookup"><span data-stu-id="559c9-103">Gets a list of scheduler jobs or a particular scheduler job.</span></span>

## <span data-ttu-id="559c9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="559c9-104">SYNTAX</span></span>

```
Get-AzureSchedulerJob -Location <String> -JobCollectionName <String> [-JobName <String>] [-JobState <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="559c9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="559c9-105">DESCRIPTION</span></span>
<span data-ttu-id="559c9-106">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="559c9-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="559c9-107">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="559c9-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="559c9-108">Il cmdlet **Get-AzureSchedulerJobCollection** ottiene un elenco dei processi di pianificazione o di un processo di pianificazione specifico.</span><span class="sxs-lookup"><span data-stu-id="559c9-108">The **Get-AzureSchedulerJobCollection** cmdlet gets a list of scheduler jobs or a particular scheduler job.</span></span>

## <span data-ttu-id="559c9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="559c9-109">EXAMPLES</span></span>

### <span data-ttu-id="559c9-110">Esempio 1: ottenere tutti i processi in una raccolta</span><span class="sxs-lookup"><span data-stu-id="559c9-110">Example 1: Get all jobs in a collection</span></span>
```
PS C:\> Get-AzureSchedulerJob -Location "North Central US" -JobCollectionName "JobCollection01"
```

<span data-ttu-id="559c9-111">Questo comando ottiene i processi dell'utilità di pianificazione che fanno parte della raccolta processi denominata JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="559c9-111">This command gets scheduler jobs that are part of the job collection named JobCollection01.</span></span>

### <span data-ttu-id="559c9-112">Esempio 2: ottenere un processo denominato</span><span class="sxs-lookup"><span data-stu-id="559c9-112">Example 2: Get a named job</span></span>
```
PS C:\> Get-AzureSchedulerJob -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job01"
```

<span data-ttu-id="559c9-113">Questo comando ottiene il processo denominato Job01 dalla raccolta denominata JobCollection01 nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="559c9-113">This command gets the job named Job01 from the collection named JobCollection01 in the specified location.</span></span>

### <span data-ttu-id="559c9-114">Esempio 3: ottenere processi disabilitati in una raccolta</span><span class="sxs-lookup"><span data-stu-id="559c9-114">Example 3: Get disabled jobs in a collection</span></span>
```
PS C:\> Get-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01" -JobState "Disabled"
```

<span data-ttu-id="559c9-115">Questo comando ottiene tutti i processi di pianificazione disabilitati che fanno parte di JobCollection01 nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="559c9-115">This command gets all disabled scheduler jobs that are part of JobCollection01 in the specified location.</span></span>

## <span data-ttu-id="559c9-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="559c9-116">PARAMETERS</span></span>

### <span data-ttu-id="559c9-117">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="559c9-117">-JobCollectionName</span></span>
<span data-ttu-id="559c9-118">Specifica il nome della raccolta che contiene il processo di pianificazione da ottenere.</span><span class="sxs-lookup"><span data-stu-id="559c9-118">Specifies the name of the collection that contains the scheduler job to get.</span></span>

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

### <span data-ttu-id="559c9-119">-JobName</span><span class="sxs-lookup"><span data-stu-id="559c9-119">-JobName</span></span>
<span data-ttu-id="559c9-120">Specifica il nome di un processo di pianificazione da ottenere.</span><span class="sxs-lookup"><span data-stu-id="559c9-120">Specifies the name of a scheduler job to get.</span></span>

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

### <span data-ttu-id="559c9-121">-JobState</span><span class="sxs-lookup"><span data-stu-id="559c9-121">-JobState</span></span>
<span data-ttu-id="559c9-122">Specifica lo stato dei processi dell'utilità di pianificazione da ottenere.</span><span class="sxs-lookup"><span data-stu-id="559c9-122">Specifies the state of scheduler jobs to get.</span></span>
<span data-ttu-id="559c9-123">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="559c9-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="559c9-124">Abilitato</span><span class="sxs-lookup"><span data-stu-id="559c9-124">Enabled</span></span>
- <span data-ttu-id="559c9-125">Disabilitato</span><span class="sxs-lookup"><span data-stu-id="559c9-125">Disabled</span></span>
- <span data-ttu-id="559c9-126">Faulted</span><span class="sxs-lookup"><span data-stu-id="559c9-126">Faulted</span></span>
- <span data-ttu-id="559c9-127">Completato</span><span class="sxs-lookup"><span data-stu-id="559c9-127">Completed</span></span>

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

### <span data-ttu-id="559c9-128">-Posizione</span><span class="sxs-lookup"><span data-stu-id="559c9-128">-Location</span></span>
<span data-ttu-id="559c9-129">Specifica il nome della posizione che ospita il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="559c9-129">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="559c9-130">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="559c9-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="559c9-131">Ovunque in Asia</span><span class="sxs-lookup"><span data-stu-id="559c9-131">Anywhere Asia</span></span>
- <span data-ttu-id="559c9-132">Ovunque Europa</span><span class="sxs-lookup"><span data-stu-id="559c9-132">Anywhere Europe</span></span>
- <span data-ttu-id="559c9-133">Ovunque negli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="559c9-133">Anywhere US</span></span>
- <span data-ttu-id="559c9-134">Asia orientale</span><span class="sxs-lookup"><span data-stu-id="559c9-134">East Asia</span></span>
- <span data-ttu-id="559c9-135">Stati Uniti orientali</span><span class="sxs-lookup"><span data-stu-id="559c9-135">East US</span></span>
- <span data-ttu-id="559c9-136">Stati Uniti nord-centrale</span><span class="sxs-lookup"><span data-stu-id="559c9-136">North Central US</span></span>
- <span data-ttu-id="559c9-137">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="559c9-137">North Europe</span></span>
- <span data-ttu-id="559c9-138">Stati Uniti del centro sud</span><span class="sxs-lookup"><span data-stu-id="559c9-138">South Central US</span></span>
- <span data-ttu-id="559c9-139">Asia sud-orientale</span><span class="sxs-lookup"><span data-stu-id="559c9-139">Southeast Asia</span></span>
- <span data-ttu-id="559c9-140">Europa occidentale</span><span class="sxs-lookup"><span data-stu-id="559c9-140">West Europe</span></span>
- <span data-ttu-id="559c9-141">Ovest degli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="559c9-141">West US</span></span>

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

### <span data-ttu-id="559c9-142">-Profile</span><span class="sxs-lookup"><span data-stu-id="559c9-142">-Profile</span></span>
<span data-ttu-id="559c9-143">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="559c9-143">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="559c9-144">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="559c9-144">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="559c9-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="559c9-145">CommonParameters</span></span>
<span data-ttu-id="559c9-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="559c9-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="559c9-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="559c9-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="559c9-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="559c9-148">INPUTS</span></span>

## <span data-ttu-id="559c9-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="559c9-149">OUTPUTS</span></span>

## <span data-ttu-id="559c9-150">Note</span><span class="sxs-lookup"><span data-stu-id="559c9-150">NOTES</span></span>

## <span data-ttu-id="559c9-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="559c9-151">RELATED LINKS</span></span>

[<span data-ttu-id="559c9-152">Remove-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="559c9-152">Remove-AzureSchedulerJob</span></span>](./Remove-AzureSchedulerJob.md)


