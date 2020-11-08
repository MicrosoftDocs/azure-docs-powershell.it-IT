---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 89B28B7C-CA61-4CAB-A4DD-69363AB48A65
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a33739cfad37269fc2f91654e82d6ea36eb2336
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023570"
---
# <span data-ttu-id="3fb2e-101">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="3fb2e-101">Get-AzureSchedulerJobCollection</span></span>

## <span data-ttu-id="3fb2e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3fb2e-102">SYNOPSIS</span></span>
<span data-ttu-id="3fb2e-103">Ottiene le raccolte processi dell'utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="3fb2e-103">Gets scheduler job collections.</span></span>

## <span data-ttu-id="3fb2e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3fb2e-104">SYNTAX</span></span>

```
Get-AzureSchedulerJobCollection [-Location <String>] [-JobCollectionName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="3fb2e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3fb2e-105">DESCRIPTION</span></span>
<span data-ttu-id="3fb2e-106">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3fb2e-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="3fb2e-107">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="3fb2e-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="3fb2e-108">Il cmdlet **Get-AzureSchedulerJobCollection** ottiene uno o più insiemi di processi dell'utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="3fb2e-108">The **Get-AzureSchedulerJobCollection** cmdlet gets one or more scheduler job collections.</span></span>

## <span data-ttu-id="3fb2e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3fb2e-109">EXAMPLES</span></span>

### <span data-ttu-id="3fb2e-110">Esempio 1: ottenere tutte le raccolte</span><span class="sxs-lookup"><span data-stu-id="3fb2e-110">Example 1: Get all collections</span></span>
```
PS C:\> Get-AzureSchedulerJobCollection
```

<span data-ttu-id="3fb2e-111">Questo comando consente di ottenere tutte le raccolte processi Scheduler in tutte le posizioni della sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="3fb2e-111">This command gets all scheduler job collections across all locations in the current subscription.</span></span>

### <span data-ttu-id="3fb2e-112">Esempio 2: ottenere tutte le raccolte per una posizione</span><span class="sxs-lookup"><span data-stu-id="3fb2e-112">Example 2: Get all collections for a location</span></span>
```
PS C:\> Get-AzureSchedulerJobCollection -Location "North Central US"
```

<span data-ttu-id="3fb2e-113">Questo comando consente di ottenere tutte le raccolte processi dell'utilità di pianificazione nella posizione denominata North Central US.</span><span class="sxs-lookup"><span data-stu-id="3fb2e-113">This command gets all scheduler job collections in the location named North Central US.</span></span>

### <span data-ttu-id="3fb2e-114">Esempio 3: ottenere una raccolta usando un nome</span><span class="sxs-lookup"><span data-stu-id="3fb2e-114">Example 3: Get a collection by using a name</span></span>
```
PS C:\> Get-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01"
```

<span data-ttu-id="3fb2e-115">Questo comando consente di ottenere la raccolta processi Scheduler denominata JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="3fb2e-115">This command gets the scheduler job collection named JobCollection01.</span></span>

## <span data-ttu-id="3fb2e-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3fb2e-116">PARAMETERS</span></span>

### <span data-ttu-id="3fb2e-117">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="3fb2e-117">-JobCollectionName</span></span>
<span data-ttu-id="3fb2e-118">Specifica il nome della raccolta processi Scheduler da ottenere.</span><span class="sxs-lookup"><span data-stu-id="3fb2e-118">Specifies the name of the scheduler job collection to get.</span></span>

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

### <span data-ttu-id="3fb2e-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="3fb2e-119">-Location</span></span>
<span data-ttu-id="3fb2e-120">Specifica il nome della posizione che ospita il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="3fb2e-120">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="3fb2e-121">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="3fb2e-121">Valid values are:</span></span> 

- <span data-ttu-id="3fb2e-122">Ovunque in Asia</span><span class="sxs-lookup"><span data-stu-id="3fb2e-122">Anywhere Asia</span></span>
- <span data-ttu-id="3fb2e-123">Ovunque Europa</span><span class="sxs-lookup"><span data-stu-id="3fb2e-123">Anywhere Europe</span></span>
- <span data-ttu-id="3fb2e-124">Ovunque negli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="3fb2e-124">Anywhere US</span></span>
- <span data-ttu-id="3fb2e-125">Asia orientale</span><span class="sxs-lookup"><span data-stu-id="3fb2e-125">East Asia</span></span>
- <span data-ttu-id="3fb2e-126">Stati Uniti orientali</span><span class="sxs-lookup"><span data-stu-id="3fb2e-126">East US</span></span>
- <span data-ttu-id="3fb2e-127">Stati Uniti nord-centrale</span><span class="sxs-lookup"><span data-stu-id="3fb2e-127">North Central US</span></span>
- <span data-ttu-id="3fb2e-128">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="3fb2e-128">North Europe</span></span>
- <span data-ttu-id="3fb2e-129">Stati Uniti del centro sud</span><span class="sxs-lookup"><span data-stu-id="3fb2e-129">South Central US</span></span>
- <span data-ttu-id="3fb2e-130">Asia sud-orientale</span><span class="sxs-lookup"><span data-stu-id="3fb2e-130">Southeast Asia</span></span>
- <span data-ttu-id="3fb2e-131">Europa occidentale</span><span class="sxs-lookup"><span data-stu-id="3fb2e-131">West Europe</span></span>
- <span data-ttu-id="3fb2e-132">Ovest degli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="3fb2e-132">West US</span></span>

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

### <span data-ttu-id="3fb2e-133">-Profile</span><span class="sxs-lookup"><span data-stu-id="3fb2e-133">-Profile</span></span>
<span data-ttu-id="3fb2e-134">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3fb2e-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3fb2e-135">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="3fb2e-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3fb2e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fb2e-136">CommonParameters</span></span>
<span data-ttu-id="3fb2e-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fb2e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fb2e-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fb2e-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fb2e-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3fb2e-139">INPUTS</span></span>

## <span data-ttu-id="3fb2e-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3fb2e-140">OUTPUTS</span></span>

## <span data-ttu-id="3fb2e-141">Note</span><span class="sxs-lookup"><span data-stu-id="3fb2e-141">NOTES</span></span>

## <span data-ttu-id="3fb2e-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3fb2e-142">RELATED LINKS</span></span>

[<span data-ttu-id="3fb2e-143">New-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="3fb2e-143">New-AzureSchedulerJobCollection</span></span>](./New-AzureSchedulerJobCollection.md)

[<span data-ttu-id="3fb2e-144">Remove-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="3fb2e-144">Remove-AzureSchedulerJobCollection</span></span>](./Remove-AzureSchedulerJobCollection.md)

[<span data-ttu-id="3fb2e-145">Set-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="3fb2e-145">Set-AzureSchedulerJobCollection</span></span>](./Set-AzureSchedulerJobCollection.md)


