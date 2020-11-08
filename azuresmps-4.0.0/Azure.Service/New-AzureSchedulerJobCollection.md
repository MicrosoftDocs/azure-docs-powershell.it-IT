---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: DF12406D-894C-4732-95EE-D75524023B82
online version: ''
schema: 2.0.0
ms.openlocfilehash: c2e6596c0de702175927f51bfd70fc5271b13bfd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023938"
---
# <span data-ttu-id="b5c7e-101">New-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="b5c7e-101">New-AzureSchedulerJobCollection</span></span>

## <span data-ttu-id="b5c7e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b5c7e-102">SYNOPSIS</span></span>
<span data-ttu-id="b5c7e-103">Crea una raccolta processi Scheduler.</span><span class="sxs-lookup"><span data-stu-id="b5c7e-103">Creates a scheduler job collection.</span></span>

## <span data-ttu-id="b5c7e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b5c7e-104">SYNTAX</span></span>

```
New-AzureSchedulerJobCollection -Location <String> -JobCollectionName <String> [-Plan <String>]
 [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="b5c7e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b5c7e-105">DESCRIPTION</span></span>
<span data-ttu-id="b5c7e-106">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b5c7e-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="b5c7e-107">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="b5c7e-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="b5c7e-108">Il cmdlet **New-AzureSchedulerJobCollection** crea una raccolta processi Scheduler.</span><span class="sxs-lookup"><span data-stu-id="b5c7e-108">The **New-AzureSchedulerJobCollection** cmdlet creates a scheduler job collection.</span></span>
<span data-ttu-id="b5c7e-109">Se non specifichi un valore per il parametro *Plan* , il cmdlet crea una raccolta processi standard.</span><span class="sxs-lookup"><span data-stu-id="b5c7e-109">If you do not specify a value for the *Plan* parameter, the cmdlet creates a standard job collection.</span></span>

## <span data-ttu-id="b5c7e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b5c7e-110">EXAMPLES</span></span>

### <span data-ttu-id="b5c7e-111">Esempio 1: creare una raccolta processi Scheduler che include valori predefiniti</span><span class="sxs-lookup"><span data-stu-id="b5c7e-111">Example 1: Create a scheduler job collection that includes default values</span></span>
```
PS C:\> New-AzureSchedulerJobCollection -JobCollectionName "JobCollection01" -Location "North Central US" -Plan "Standard"
```

<span data-ttu-id="b5c7e-112">Questo comando crea una raccolta di processi di pianificazione standard denominata JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="b5c7e-112">This command creates a standard scheduler job collection named JobCollection01.</span></span>
<span data-ttu-id="b5c7e-113">La nuova raccolta include un conteggio dei processi predefinito e i valori di ricorrenza massimi per una raccolta di processi di pianificazione standard.</span><span class="sxs-lookup"><span data-stu-id="b5c7e-113">The new collection has a default job count and maximum recurrence values for a standard scheduler job collection.</span></span>

### <span data-ttu-id="b5c7e-114">Esempio 2: creare una raccolta processi Scheduler con valori specificati</span><span class="sxs-lookup"><span data-stu-id="b5c7e-114">Example 2: Create a scheduler job collection with specified values</span></span>
```
PS C:\> New-AzureSchedulerJobCollection -JobCollectionName "JobCollection02" -Location "North Central US" -Frequency "Hour" -Interval 12 -MaxJobCount 30 -Plan "Standard"
```

<span data-ttu-id="b5c7e-115">Questo comando crea una raccolta di processi di pianificazione standard denominata JobCollection02.</span><span class="sxs-lookup"><span data-stu-id="b5c7e-115">This command creates a standard scheduler job collection named JobCollection02.</span></span>
<span data-ttu-id="b5c7e-116">La nuova raccolta ha un numero massimo di lavoro di 30 e una ricorrenza massima di 12 per ora.</span><span class="sxs-lookup"><span data-stu-id="b5c7e-116">The new collection has a maximum job count of 30 and a maximum recurrence of 12 per hour.</span></span>

## <span data-ttu-id="b5c7e-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b5c7e-117">PARAMETERS</span></span>

### <span data-ttu-id="b5c7e-118">-Frequenza</span><span class="sxs-lookup"><span data-stu-id="b5c7e-118">-Frequency</span></span>
<span data-ttu-id="b5c7e-119">Specifica la frequenza massima che può essere specificata in qualsiasi processo in questa raccolta processi dell'utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="b5c7e-119">Specifies the maximum frequency that can be specified on any job in this scheduler job collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5c7e-120">-Intervallo</span><span class="sxs-lookup"><span data-stu-id="b5c7e-120">-Interval</span></span>
<span data-ttu-id="b5c7e-121">Specifica l'intervallo di ricorrenza alla frequenza specificata usando il parametro *Frequency* .</span><span class="sxs-lookup"><span data-stu-id="b5c7e-121">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5c7e-122">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="b5c7e-122">-JobCollectionName</span></span>
<span data-ttu-id="b5c7e-123">Specifica il nome per la nuova raccolta processi Scheduler.</span><span class="sxs-lookup"><span data-stu-id="b5c7e-123">Specifies the name for the new scheduler job collection.</span></span>

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

### <span data-ttu-id="b5c7e-124">-Posizione</span><span class="sxs-lookup"><span data-stu-id="b5c7e-124">-Location</span></span>
<span data-ttu-id="b5c7e-125">Specifica il nome della posizione che ospita il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="b5c7e-125">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="b5c7e-126">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="b5c7e-126">Valid values are:</span></span> 

- <span data-ttu-id="b5c7e-127">Ovunque in Asia</span><span class="sxs-lookup"><span data-stu-id="b5c7e-127">Anywhere Asia</span></span>
- <span data-ttu-id="b5c7e-128">Ovunque Europa</span><span class="sxs-lookup"><span data-stu-id="b5c7e-128">Anywhere Europe</span></span>
- <span data-ttu-id="b5c7e-129">Ovunque negli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="b5c7e-129">Anywhere US</span></span>
- <span data-ttu-id="b5c7e-130">Asia orientale</span><span class="sxs-lookup"><span data-stu-id="b5c7e-130">East Asia</span></span>
- <span data-ttu-id="b5c7e-131">Stati Uniti orientali</span><span class="sxs-lookup"><span data-stu-id="b5c7e-131">East US</span></span>
- <span data-ttu-id="b5c7e-132">Stati Uniti nord-centrale</span><span class="sxs-lookup"><span data-stu-id="b5c7e-132">North Central US</span></span>
- <span data-ttu-id="b5c7e-133">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="b5c7e-133">North Europe</span></span>
- <span data-ttu-id="b5c7e-134">Stati Uniti del centro sud</span><span class="sxs-lookup"><span data-stu-id="b5c7e-134">South Central US</span></span>
- <span data-ttu-id="b5c7e-135">Asia sud-orientale</span><span class="sxs-lookup"><span data-stu-id="b5c7e-135">Southeast Asia</span></span>
- <span data-ttu-id="b5c7e-136">Europa occidentale</span><span class="sxs-lookup"><span data-stu-id="b5c7e-136">West Europe</span></span>
- <span data-ttu-id="b5c7e-137">Ovest degli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="b5c7e-137">West US</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5c7e-138">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="b5c7e-138">-MaxJobCount</span></span>
<span data-ttu-id="b5c7e-139">Specifica il numero massimo di processi che possono essere creati nella raccolta processi Scheduler.</span><span class="sxs-lookup"><span data-stu-id="b5c7e-139">Specifies the maximum number of jobs that can be created in the scheduler job collection.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5c7e-140">-Piano</span><span class="sxs-lookup"><span data-stu-id="b5c7e-140">-Plan</span></span>
<span data-ttu-id="b5c7e-141">Specifica il piano di raccolta processi Scheduler.</span><span class="sxs-lookup"><span data-stu-id="b5c7e-141">Specifies the scheduler job collection plan.</span></span>

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

### <span data-ttu-id="b5c7e-142">-Profile</span><span class="sxs-lookup"><span data-stu-id="b5c7e-142">-Profile</span></span>
<span data-ttu-id="b5c7e-143">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5c7e-143">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b5c7e-144">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="b5c7e-144">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b5c7e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5c7e-145">CommonParameters</span></span>
<span data-ttu-id="b5c7e-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5c7e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5c7e-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5c7e-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5c7e-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b5c7e-148">INPUTS</span></span>

## <span data-ttu-id="b5c7e-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b5c7e-149">OUTPUTS</span></span>

## <span data-ttu-id="b5c7e-150">Note</span><span class="sxs-lookup"><span data-stu-id="b5c7e-150">NOTES</span></span>

## <span data-ttu-id="b5c7e-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b5c7e-151">RELATED LINKS</span></span>

[<span data-ttu-id="b5c7e-152">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="b5c7e-152">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)

[<span data-ttu-id="b5c7e-153">Remove-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="b5c7e-153">Remove-AzureSchedulerJobCollection</span></span>](./Remove-AzureSchedulerJobCollection.md)

[<span data-ttu-id="b5c7e-154">Set-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="b5c7e-154">Set-AzureSchedulerJobCollection</span></span>](./Set-AzureSchedulerJobCollection.md)


