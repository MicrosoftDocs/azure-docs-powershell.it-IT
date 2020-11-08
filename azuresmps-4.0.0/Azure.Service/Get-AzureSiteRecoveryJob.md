---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2957C0DE-3A2F-4337-A778-2B95654972E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: d0b272732cf6c1e1b2025c8e7f48b58e4807cdb3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023553"
---
# <span data-ttu-id="47131-101">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="47131-101">Get-AzureSiteRecoveryJob</span></span>

## <span data-ttu-id="47131-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="47131-102">SYNOPSIS</span></span>
<span data-ttu-id="47131-103">Ottiene le informazioni sull'operazione per un Vault di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="47131-103">Gets the operation information for a Site Recovery vault.</span></span>

## <span data-ttu-id="47131-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="47131-104">SYNTAX</span></span>

### <span data-ttu-id="47131-105">ByParam (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="47131-105">ByParam (Default)</span></span>
```
Get-AzureSiteRecoveryJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="47131-106">ById</span><span class="sxs-lookup"><span data-stu-id="47131-106">ById</span></span>
```
Get-AzureSiteRecoveryJob -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="47131-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="47131-107">ByObject</span></span>
```
Get-AzureSiteRecoveryJob -Job <ASRJob> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="47131-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="47131-108">DESCRIPTION</span></span>
<span data-ttu-id="47131-109">Il cmdlet **Get-AzureSiteRecoveryJob** ottiene i processi di ripristino dei siti di Azure.</span><span class="sxs-lookup"><span data-stu-id="47131-109">The **Get-AzureSiteRecoveryJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="47131-110">Puoi usare questo cmdlet per visualizzare le informazioni sull'operazione per il Vault di ripristino del sito corrente.</span><span class="sxs-lookup"><span data-stu-id="47131-110">You can use this cmdlet to view the operation information for the current Site Recovery vault.</span></span>

## <span data-ttu-id="47131-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="47131-111">EXAMPLES</span></span>

### <span data-ttu-id="47131-112">Esempio 1: ottenere un processo specificando un ID</span><span class="sxs-lookup"><span data-stu-id="47131-112">Example 1: Get a job by specifying an ID</span></span>
```
PS C:\> Get-AzureSiteRecoveryJob -Id "033785cc-9f72-4f07-8e78-e4d1e942a7ae" 
Name             : SaveRecoveryPlan
ID               : 033785cc-9f72-4f07-8e78-e4d1e942a7ae
ClientRequestId  : d604206b-32e1-4d5b-9a23-32b118d14a1e-2015-02-20 07:20:42Z-P
State            : Succeeded
StateDescription : Completed
StartTime        : 20-02-2015 07:20:45 +05:30
EndTime          : 20-02-2015 07:20:46 +05:30
TargetObjectId   : cfb445bf-fd14-4b5d-b9ac-5154e1415ef2
TargetObjectType : RecoveryPlan
TargetObjectName : RP
AllowedActions   : {Cancel}
Tasks            : {Save a recovery plan task}
Errors           : {}
```

<span data-ttu-id="47131-113">Questo comando ottiene il processo di ripristino del sito di Azure con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="47131-113">This command gets the  Azure Site Recovery job that has the specified ID.</span></span>

### <span data-ttu-id="47131-114">Esempio 2: ottiene un processo in base al tempo</span><span class="sxs-lookup"><span data-stu-id="47131-114">Example 2: Gets a job based on time</span></span>
```
PS C:\> Get-AzureSiteRecoveryJob -StartTime "20-02-2015 01:00:00" -EndTime "21-02-2015 01:00:00"
Name             : SaveRecoveryPlan
ID               : 033785cc-9f72-4f07-8e78-e4d1e942a7ae
ClientRequestId  : d604206b-32e1-4d5b-9a23-32b118d14a1e-2015-02-20 07:20:42Z-P
State            : Succeeded
StateDescription : Completed
StartTime        : 20-02-2015 07:20:45 +05:30
EndTime          : 20-02-2015 07:20:46 +05:30
TargetObjectId   : cfb445bf-fd14-4b5d-b9ac-5154e1415ef2
TargetObjectType : RecoveryPlan
TargetObjectName : RP
AllowedActions   : {Cancel}
Tasks            : {Save a recovery plan task}
Errors           : {}
```

<span data-ttu-id="47131-115">Questo comando ottiene i processi di ripristino del sito che rientrano tra l'ora di inizio e l'ora di fine specificati.</span><span class="sxs-lookup"><span data-stu-id="47131-115">This command gets Site Recovery jobs that fall between the specified start time and end time.</span></span>

## <span data-ttu-id="47131-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="47131-116">PARAMETERS</span></span>

### <span data-ttu-id="47131-117">-EndTime</span><span class="sxs-lookup"><span data-stu-id="47131-117">-EndTime</span></span>
<span data-ttu-id="47131-118">Specifica l'ora di fine per i processi.</span><span class="sxs-lookup"><span data-stu-id="47131-118">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="47131-119">Questo cmdlet ottiene tutti i processi avviati prima del tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="47131-119">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="47131-120">Per ottenere un oggetto **DateTime** , usare il cmdlet **get-date** .</span><span class="sxs-lookup"><span data-stu-id="47131-120">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="47131-121">Per altre informazioni, digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="47131-121">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47131-122">-ID</span><span class="sxs-lookup"><span data-stu-id="47131-122">-Id</span></span>
<span data-ttu-id="47131-123">Specifica l'ID di un processo da ottenere.</span><span class="sxs-lookup"><span data-stu-id="47131-123">Specifies the ID of a job to get.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47131-124">-Job</span><span class="sxs-lookup"><span data-stu-id="47131-124">-Job</span></span>
<span data-ttu-id="47131-125">Specifica un processo da ottenere.</span><span class="sxs-lookup"><span data-stu-id="47131-125">Specifies a job to get.</span></span>

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47131-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="47131-126">-Profile</span></span>
<span data-ttu-id="47131-127">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47131-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="47131-128">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="47131-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="47131-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="47131-129">-StartTime</span></span>
<span data-ttu-id="47131-130">Specifica l'ora di inizio per i processi.</span><span class="sxs-lookup"><span data-stu-id="47131-130">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="47131-131">Questo cmdlet ottiene tutti i processi avviati dopo il periodo di tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="47131-131">This cmdlet gets all jobs that started after the specified time.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47131-132">-Stato</span><span class="sxs-lookup"><span data-stu-id="47131-132">-State</span></span>
<span data-ttu-id="47131-133">Specifica lo stato di input per un processo di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="47131-133">Specifies the input state for a Site Recovery job.</span></span>
<span data-ttu-id="47131-134">Questo cmdlet ottiene tutti i processi che corrispondono allo stato specificato.</span><span class="sxs-lookup"><span data-stu-id="47131-134">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="47131-135">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="47131-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="47131-136">NotStarted</span><span class="sxs-lookup"><span data-stu-id="47131-136">NotStarted</span></span>
- <span data-ttu-id="47131-137">InProgress</span><span class="sxs-lookup"><span data-stu-id="47131-137">InProgress</span></span>
- <span data-ttu-id="47131-138">Succeeded</span><span class="sxs-lookup"><span data-stu-id="47131-138">Succeeded</span></span>
- <span data-ttu-id="47131-139">Altri</span><span class="sxs-lookup"><span data-stu-id="47131-139">Other</span></span>
- <span data-ttu-id="47131-140">Fallito</span><span class="sxs-lookup"><span data-stu-id="47131-140">Failed</span></span>
- <span data-ttu-id="47131-141">Annullata</span><span class="sxs-lookup"><span data-stu-id="47131-141">Cancelled</span></span>
- <span data-ttu-id="47131-142">Sospeso</span><span class="sxs-lookup"><span data-stu-id="47131-142">Suspended</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47131-143">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="47131-143">-TargetObjectId</span></span>
<span data-ttu-id="47131-144">Specifica l'ID dell'oggetto di destinazione del processo.</span><span class="sxs-lookup"><span data-stu-id="47131-144">Specifies the ID of the object targeted by the job.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47131-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47131-145">CommonParameters</span></span>
<span data-ttu-id="47131-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47131-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47131-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47131-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47131-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="47131-148">INPUTS</span></span>

## <span data-ttu-id="47131-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="47131-149">OUTPUTS</span></span>

## <span data-ttu-id="47131-150">Note</span><span class="sxs-lookup"><span data-stu-id="47131-150">NOTES</span></span>

## <span data-ttu-id="47131-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="47131-151">RELATED LINKS</span></span>

[<span data-ttu-id="47131-152">Cmdlet di servizi di ripristino siti di Azure</span><span class="sxs-lookup"><span data-stu-id="47131-152">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)

[<span data-ttu-id="47131-153">Riavviare-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="47131-153">Restart-AzureSiteRecoveryJob</span></span>](./Restart-AzureSiteRecoveryJob.md)

[<span data-ttu-id="47131-154">Curriculum vitae-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="47131-154">Resume-AzureSiteRecoveryJob</span></span>](./Resume-AzureSiteRecoveryJob.md)

[<span data-ttu-id="47131-155">Stop-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="47131-155">Stop-AzureSiteRecoveryJob</span></span>](./Stop-AzureSiteRecoveryJob.md)


