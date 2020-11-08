---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 22DBB3DD-B02D-4288-89CB-550EBECC2E79
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4373e4eed8524db1dd5311778b3e297e766c74dd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023401"
---
# <span data-ttu-id="d7ee2-101">Set-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d7ee2-101">Set-AzureSchedulerJobCollection</span></span>

## <span data-ttu-id="d7ee2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d7ee2-102">SYNOPSIS</span></span>
<span data-ttu-id="d7ee2-103">Aggiorna una raccolta processi dell'utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="d7ee2-103">Updates a scheduler job collection.</span></span>

## <span data-ttu-id="d7ee2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d7ee2-104">SYNTAX</span></span>

```
Set-AzureSchedulerJobCollection -Location <String> -JobCollectionName <String> [-Plan <String>]
 [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="d7ee2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d7ee2-105">DESCRIPTION</span></span>
<span data-ttu-id="d7ee2-106">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d7ee2-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="d7ee2-107">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="d7ee2-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="d7ee2-108">Il cmdlet **set-AzureSchedulerJobCollection** aggiorna una raccolta processi Scheduler.</span><span class="sxs-lookup"><span data-stu-id="d7ee2-108">The **Set-AzureSchedulerJobCollection** cmdlet updates a scheduler job collection.</span></span>

## <span data-ttu-id="d7ee2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d7ee2-109">EXAMPLES</span></span>

### <span data-ttu-id="d7ee2-110">Esempio 1: cambiare il numero massimo di processi per una raccolta</span><span class="sxs-lookup"><span data-stu-id="d7ee2-110">Example 1: Change the maximum job count for a collection</span></span>
```
PS C:\> Set-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01" -MaxJobCount 30
```

<span data-ttu-id="d7ee2-111">Questo comando consente di modificare il numero massimo di processi in 30 nella raccolta processi dell'utilità di pianificazione esistente denominata JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="d7ee2-111">This command changes the maximum job count to 30 on the existing scheduler job collection named JobCollection01.</span></span>

## <span data-ttu-id="d7ee2-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d7ee2-112">PARAMETERS</span></span>

### <span data-ttu-id="d7ee2-113">-Frequenza</span><span class="sxs-lookup"><span data-stu-id="d7ee2-113">-Frequency</span></span>
<span data-ttu-id="d7ee2-114">Specifica la frequenza massima che può essere specificata in qualsiasi processo in questa raccolta processi dell'utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="d7ee2-114">Specifies the maximum frequency that can be specified on any job in this scheduler job collection.</span></span>
<span data-ttu-id="d7ee2-115">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d7ee2-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d7ee2-116">Minuto</span><span class="sxs-lookup"><span data-stu-id="d7ee2-116">Minute</span></span>
- <span data-ttu-id="d7ee2-117">Ora</span><span class="sxs-lookup"><span data-stu-id="d7ee2-117">Hour</span></span>
- <span data-ttu-id="d7ee2-118">Giorno</span><span class="sxs-lookup"><span data-stu-id="d7ee2-118">Day</span></span>
- <span data-ttu-id="d7ee2-119">Settimana</span><span class="sxs-lookup"><span data-stu-id="d7ee2-119">Week</span></span>
- <span data-ttu-id="d7ee2-120">Mese</span><span class="sxs-lookup"><span data-stu-id="d7ee2-120">Month</span></span>
- <span data-ttu-id="d7ee2-121">Anno</span><span class="sxs-lookup"><span data-stu-id="d7ee2-121">Year</span></span>

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

### <span data-ttu-id="d7ee2-122">-Intervallo</span><span class="sxs-lookup"><span data-stu-id="d7ee2-122">-Interval</span></span>
<span data-ttu-id="d7ee2-123">Specifica l'intervallo di ricorrenza alla frequenza specificata usando il parametro *Frequency* .</span><span class="sxs-lookup"><span data-stu-id="d7ee2-123">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

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

### <span data-ttu-id="d7ee2-124">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="d7ee2-124">-JobCollectionName</span></span>
<span data-ttu-id="d7ee2-125">Specifica il nome della raccolta processi Scheduler da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="d7ee2-125">Specifies the name of scheduler job collection to update.</span></span>

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

### <span data-ttu-id="d7ee2-126">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d7ee2-126">-Location</span></span>
<span data-ttu-id="d7ee2-127">Specifica il nome della posizione che ospita il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="d7ee2-127">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="d7ee2-128">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="d7ee2-128">Valid values are:</span></span> 

- <span data-ttu-id="d7ee2-129">Ovunque in Asia</span><span class="sxs-lookup"><span data-stu-id="d7ee2-129">Anywhere Asia</span></span>
- <span data-ttu-id="d7ee2-130">Ovunque Europa</span><span class="sxs-lookup"><span data-stu-id="d7ee2-130">Anywhere Europe</span></span>
- <span data-ttu-id="d7ee2-131">Ovunque negli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="d7ee2-131">Anywhere US</span></span>
- <span data-ttu-id="d7ee2-132">Asia orientale</span><span class="sxs-lookup"><span data-stu-id="d7ee2-132">East Asia</span></span>
- <span data-ttu-id="d7ee2-133">Stati Uniti orientali</span><span class="sxs-lookup"><span data-stu-id="d7ee2-133">East US</span></span>
- <span data-ttu-id="d7ee2-134">Stati Uniti nord-centrale</span><span class="sxs-lookup"><span data-stu-id="d7ee2-134">North Central US</span></span>
- <span data-ttu-id="d7ee2-135">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="d7ee2-135">North Europe</span></span>
- <span data-ttu-id="d7ee2-136">Stati Uniti del centro sud</span><span class="sxs-lookup"><span data-stu-id="d7ee2-136">South Central US</span></span>
- <span data-ttu-id="d7ee2-137">Asia sud-orientale</span><span class="sxs-lookup"><span data-stu-id="d7ee2-137">Southeast Asia</span></span>
- <span data-ttu-id="d7ee2-138">Europa occidentale</span><span class="sxs-lookup"><span data-stu-id="d7ee2-138">West Europe</span></span>
- <span data-ttu-id="d7ee2-139">Ovest degli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="d7ee2-139">West US</span></span>

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

### <span data-ttu-id="d7ee2-140">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="d7ee2-140">-MaxJobCount</span></span>
<span data-ttu-id="d7ee2-141">Specifica il numero massimo di processi che possono essere creati nella raccolta processi Scheduler.</span><span class="sxs-lookup"><span data-stu-id="d7ee2-141">Specifies the maximum number of jobs that can be created in the scheduler job collection.</span></span>

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

### <span data-ttu-id="d7ee2-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7ee2-142">-PassThru</span></span>
<span data-ttu-id="d7ee2-143">Indica che questo cmdlet restituisce un oggetto che rappresenta l'elemento in cui opera.</span><span class="sxs-lookup"><span data-stu-id="d7ee2-143">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="d7ee2-144">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="d7ee2-144">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d7ee2-145">-Piano</span><span class="sxs-lookup"><span data-stu-id="d7ee2-145">-Plan</span></span>
<span data-ttu-id="d7ee2-146">Specifica il piano di raccolta processi Scheduler.</span><span class="sxs-lookup"><span data-stu-id="d7ee2-146">Specifies the scheduler job collection plan.</span></span>

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

### <span data-ttu-id="d7ee2-147">-Profile</span><span class="sxs-lookup"><span data-stu-id="d7ee2-147">-Profile</span></span>
<span data-ttu-id="d7ee2-148">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7ee2-148">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d7ee2-149">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="d7ee2-149">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d7ee2-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7ee2-150">CommonParameters</span></span>
<span data-ttu-id="d7ee2-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7ee2-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7ee2-152">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7ee2-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7ee2-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d7ee2-153">INPUTS</span></span>

## <span data-ttu-id="d7ee2-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d7ee2-154">OUTPUTS</span></span>

## <span data-ttu-id="d7ee2-155">Note</span><span class="sxs-lookup"><span data-stu-id="d7ee2-155">NOTES</span></span>

## <span data-ttu-id="d7ee2-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d7ee2-156">RELATED LINKS</span></span>

[<span data-ttu-id="d7ee2-157">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d7ee2-157">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)

[<span data-ttu-id="d7ee2-158">New-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d7ee2-158">New-AzureSchedulerJobCollection</span></span>](./New-AzureSchedulerJobCollection.md)

[<span data-ttu-id="d7ee2-159">Remove-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d7ee2-159">Remove-AzureSchedulerJobCollection</span></span>](./Remove-AzureSchedulerJobCollection.md)


