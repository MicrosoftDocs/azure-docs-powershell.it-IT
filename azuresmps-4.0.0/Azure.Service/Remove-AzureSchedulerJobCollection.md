---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D4349562-1392-44B6-9353-6231F0CB5C51
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66618c0a684a8e54d41bbe4014ee1e6c893acdbf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029590"
---
# <span data-ttu-id="365f2-101">Remove-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="365f2-101">Remove-AzureSchedulerJobCollection</span></span>

## <span data-ttu-id="365f2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="365f2-102">SYNOPSIS</span></span>
<span data-ttu-id="365f2-103">Elimina una raccolta processi Scheduler.</span><span class="sxs-lookup"><span data-stu-id="365f2-103">Deletes a scheduler job collection.</span></span>

## <span data-ttu-id="365f2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="365f2-104">SYNTAX</span></span>

```
Remove-AzureSchedulerJobCollection [-Force] [-Location <String>] -JobCollectionName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="365f2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="365f2-105">DESCRIPTION</span></span>
<span data-ttu-id="365f2-106">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="365f2-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="365f2-107">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="365f2-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="365f2-108">Il cmdlet **Remove-AzureSchedulerJobCollection** Elimina una raccolta di processi Scheduler e tutti i processi in tale raccolta.</span><span class="sxs-lookup"><span data-stu-id="365f2-108">The **Remove-AzureSchedulerJobCollection** cmdlet deletes a scheduler job collection and any jobs under that collection.</span></span>

## <span data-ttu-id="365f2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="365f2-109">EXAMPLES</span></span>

### <span data-ttu-id="365f2-110">Esempio 1: eliminare una raccolta processi per una posizione</span><span class="sxs-lookup"><span data-stu-id="365f2-110">Example 1: Delete a job collection for a location</span></span>
```
PS C:\> Remove-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01"
```

<span data-ttu-id="365f2-111">Questo comando Elimina la raccolta processi Scheduler denominata JobCollection01 nella posizione North Central US.</span><span class="sxs-lookup"><span data-stu-id="365f2-111">This command deletes the scheduler job collection named JobCollection01 in the North Central US location.</span></span>
<span data-ttu-id="365f2-112">Il comando Elimina anche i processi in JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="365f2-112">The command also deletes the jobs under JobCollection01.</span></span>

### <span data-ttu-id="365f2-113">Esempio 2: eliminare una posizione di processo</span><span class="sxs-lookup"><span data-stu-id="365f2-113">Example 2: Delete a job location</span></span>
```
PS C:\> Remove-AzureSchedulerJobCollection -JobCollectionName "JobCollection02"
```

<span data-ttu-id="365f2-114">Questo comando Elimina la raccolta processi Scheduler denominata JobCollection02.</span><span class="sxs-lookup"><span data-stu-id="365f2-114">This command deletes the scheduler job collection named JobCollection02.</span></span>
<span data-ttu-id="365f2-115">Il comando Elimina anche i processi in JobCollection02.</span><span class="sxs-lookup"><span data-stu-id="365f2-115">The command also deletes the jobs under JobCollection02.</span></span>

## <span data-ttu-id="365f2-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="365f2-116">PARAMETERS</span></span>

### <span data-ttu-id="365f2-117">-Force</span><span class="sxs-lookup"><span data-stu-id="365f2-117">-Force</span></span>
<span data-ttu-id="365f2-118">Indica che questo cmdlet rimuove la raccolta processi Scheduler senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="365f2-118">Indicates that this cmdlet removes the scheduler job collection without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="365f2-119">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="365f2-119">-JobCollectionName</span></span>
<span data-ttu-id="365f2-120">Specifica il nome della raccolta processi Scheduler da eliminare.</span><span class="sxs-lookup"><span data-stu-id="365f2-120">Specifies the name of the scheduler job collection to delete.</span></span>

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

### <span data-ttu-id="365f2-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="365f2-121">-Location</span></span>
<span data-ttu-id="365f2-122">Specifica il nome della posizione che ospita il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="365f2-122">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="365f2-123">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="365f2-123">Valid values are:</span></span> 

- <span data-ttu-id="365f2-124">Ovunque in Asia</span><span class="sxs-lookup"><span data-stu-id="365f2-124">Anywhere Asia</span></span>
- <span data-ttu-id="365f2-125">Ovunque Europa</span><span class="sxs-lookup"><span data-stu-id="365f2-125">Anywhere Europe</span></span>
- <span data-ttu-id="365f2-126">Ovunque negli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="365f2-126">Anywhere US</span></span>
- <span data-ttu-id="365f2-127">Asia orientale</span><span class="sxs-lookup"><span data-stu-id="365f2-127">East Asia</span></span>
- <span data-ttu-id="365f2-128">Stati Uniti orientali</span><span class="sxs-lookup"><span data-stu-id="365f2-128">East US</span></span>
- <span data-ttu-id="365f2-129">Stati Uniti nord-centrale</span><span class="sxs-lookup"><span data-stu-id="365f2-129">North Central US</span></span>
- <span data-ttu-id="365f2-130">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="365f2-130">North Europe</span></span>
- <span data-ttu-id="365f2-131">Stati Uniti del centro sud</span><span class="sxs-lookup"><span data-stu-id="365f2-131">South Central US</span></span>
- <span data-ttu-id="365f2-132">Asia sud-orientale</span><span class="sxs-lookup"><span data-stu-id="365f2-132">Southeast Asia</span></span>
- <span data-ttu-id="365f2-133">Europa occidentale</span><span class="sxs-lookup"><span data-stu-id="365f2-133">West Europe</span></span>
- <span data-ttu-id="365f2-134">Ovest degli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="365f2-134">West US</span></span>

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

### <span data-ttu-id="365f2-135">-Profile</span><span class="sxs-lookup"><span data-stu-id="365f2-135">-Profile</span></span>
<span data-ttu-id="365f2-136">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="365f2-136">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="365f2-137">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="365f2-137">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="365f2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="365f2-138">CommonParameters</span></span>
<span data-ttu-id="365f2-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="365f2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="365f2-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="365f2-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="365f2-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="365f2-141">INPUTS</span></span>

## <span data-ttu-id="365f2-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="365f2-142">OUTPUTS</span></span>

## <span data-ttu-id="365f2-143">Note</span><span class="sxs-lookup"><span data-stu-id="365f2-143">NOTES</span></span>

## <span data-ttu-id="365f2-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="365f2-144">RELATED LINKS</span></span>

[<span data-ttu-id="365f2-145">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="365f2-145">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)

[<span data-ttu-id="365f2-146">New-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="365f2-146">New-AzureSchedulerJobCollection</span></span>](./New-AzureSchedulerJobCollection.md)

[<span data-ttu-id="365f2-147">Set-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="365f2-147">Set-AzureSchedulerJobCollection</span></span>](./Set-AzureSchedulerJobCollection.md)


