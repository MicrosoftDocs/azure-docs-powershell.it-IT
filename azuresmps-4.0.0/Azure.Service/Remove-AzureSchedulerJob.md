---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 22DEC693-32BA-4048-8912-D1626DD511E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2c95fb7f79cdb160bf2dd2014cad49d1bc96eb3b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029591"
---
# <span data-ttu-id="c15b1-101">Remove-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="c15b1-101">Remove-AzureSchedulerJob</span></span>

## <span data-ttu-id="c15b1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c15b1-102">SYNOPSIS</span></span>
<span data-ttu-id="c15b1-103">Elimina un processo di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="c15b1-103">Deletes a scheduler job.</span></span>

## <span data-ttu-id="c15b1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c15b1-104">SYNTAX</span></span>

```
Remove-AzureSchedulerJob [-Force] [-Location <String>] -JobCollectionName <String> -JobName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c15b1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c15b1-105">DESCRIPTION</span></span>
<span data-ttu-id="c15b1-106">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c15b1-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="c15b1-107">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="c15b1-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="c15b1-108">Il cmdlet **Remove-AzureSchedulerJob** Elimina un processo di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="c15b1-108">The **Remove-AzureSchedulerJob** cmdlet deletes a scheduler job.</span></span>

## <span data-ttu-id="c15b1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c15b1-109">EXAMPLES</span></span>

### <span data-ttu-id="c15b1-110">Esempio 1: eliminare un processo di pianificazione</span><span class="sxs-lookup"><span data-stu-id="c15b1-110">Example 1: Delete a scheduler job</span></span>
```
PS C:\> Remove-AzureSchedulerJob -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job17"
```

<span data-ttu-id="c15b1-111">Questo comando Elimina il processo denominato Job17.</span><span class="sxs-lookup"><span data-stu-id="c15b1-111">This command deletes the job named Job17.</span></span>
<span data-ttu-id="c15b1-112">Questo processo fa parte della raccolta processi denominata JobCollection01 e si trova nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="c15b1-112">That job is part of the job collection named JobCollection01 and is in of the specified location.</span></span>

## <span data-ttu-id="c15b1-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c15b1-113">PARAMETERS</span></span>

### <span data-ttu-id="c15b1-114">-Force</span><span class="sxs-lookup"><span data-stu-id="c15b1-114">-Force</span></span>
<span data-ttu-id="c15b1-115">Indica che questo cmdlet rimuove il processo di pianificazione senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="c15b1-115">Indicates that this cmdlet removes the scheduler job without prompting you for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c15b1-116">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="c15b1-116">-JobCollectionName</span></span>
<span data-ttu-id="c15b1-117">Specifica il nome della raccolta che contiene il processo dell'utilità di pianificazione da eliminare.</span><span class="sxs-lookup"><span data-stu-id="c15b1-117">Specifies the name of the collection that contains the scheduler job to delete.</span></span>

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

### <span data-ttu-id="c15b1-118">-JobName</span><span class="sxs-lookup"><span data-stu-id="c15b1-118">-JobName</span></span>
<span data-ttu-id="c15b1-119">Specifica il nome di un processo di pianificazione da eliminare.</span><span class="sxs-lookup"><span data-stu-id="c15b1-119">Specifies the name of a scheduler job to delete.</span></span>

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

### <span data-ttu-id="c15b1-120">-Posizione</span><span class="sxs-lookup"><span data-stu-id="c15b1-120">-Location</span></span>
<span data-ttu-id="c15b1-121">Specifica il nome della posizione che ospita il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="c15b1-121">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="c15b1-122">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="c15b1-122">Valid values are:</span></span> 

- <span data-ttu-id="c15b1-123">Ovunque in Asia</span><span class="sxs-lookup"><span data-stu-id="c15b1-123">Anywhere Asia</span></span>
- <span data-ttu-id="c15b1-124">Ovunque Europa</span><span class="sxs-lookup"><span data-stu-id="c15b1-124">Anywhere Europe</span></span>
- <span data-ttu-id="c15b1-125">Ovunque negli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="c15b1-125">Anywhere US</span></span>
- <span data-ttu-id="c15b1-126">Asia orientale</span><span class="sxs-lookup"><span data-stu-id="c15b1-126">East Asia</span></span>
- <span data-ttu-id="c15b1-127">Stati Uniti orientali</span><span class="sxs-lookup"><span data-stu-id="c15b1-127">East US</span></span>
- <span data-ttu-id="c15b1-128">Stati Uniti nord-centrale</span><span class="sxs-lookup"><span data-stu-id="c15b1-128">North Central US</span></span>
- <span data-ttu-id="c15b1-129">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="c15b1-129">North Europe</span></span>
- <span data-ttu-id="c15b1-130">Stati Uniti del centro sud</span><span class="sxs-lookup"><span data-stu-id="c15b1-130">South Central US</span></span>
- <span data-ttu-id="c15b1-131">Asia sud-orientale</span><span class="sxs-lookup"><span data-stu-id="c15b1-131">Southeast Asia</span></span>
- <span data-ttu-id="c15b1-132">Europa occidentale</span><span class="sxs-lookup"><span data-stu-id="c15b1-132">West Europe</span></span>
- <span data-ttu-id="c15b1-133">Ovest degli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="c15b1-133">West US</span></span>

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

### <span data-ttu-id="c15b1-134">-Profile</span><span class="sxs-lookup"><span data-stu-id="c15b1-134">-Profile</span></span>
<span data-ttu-id="c15b1-135">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c15b1-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c15b1-136">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="c15b1-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c15b1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c15b1-137">CommonParameters</span></span>
<span data-ttu-id="c15b1-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c15b1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c15b1-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c15b1-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c15b1-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c15b1-140">INPUTS</span></span>

## <span data-ttu-id="c15b1-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c15b1-141">OUTPUTS</span></span>

## <span data-ttu-id="c15b1-142">Note</span><span class="sxs-lookup"><span data-stu-id="c15b1-142">NOTES</span></span>

## <span data-ttu-id="c15b1-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c15b1-143">RELATED LINKS</span></span>

[<span data-ttu-id="c15b1-144">Get-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="c15b1-144">Get-AzureSchedulerJob</span></span>](./Get-AzureSchedulerJob.md)


