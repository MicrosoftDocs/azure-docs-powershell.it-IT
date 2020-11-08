---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 2001E040-5551-40C3-81D2-9A8334DE02BF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7692d4407df8fb4af8647ee0b4490abe73b2c937
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023516"
---
# <span data-ttu-id="0256f-101">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="0256f-101">Get-AzureStorSimpleJob</span></span>

## <span data-ttu-id="0256f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0256f-102">SYNOPSIS</span></span>
<span data-ttu-id="0256f-103">Ottiene i processi di StorSimple.</span><span class="sxs-lookup"><span data-stu-id="0256f-103">Gets StorSimple jobs.</span></span>

## <span data-ttu-id="0256f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0256f-104">SYNTAX</span></span>

```
Get-AzureStorSimpleJob [-DeviceName <String>] [-InstanceId <String>] [-Status <String>] [-Type <String>]
 [-From <DateTime>] [-To <DateTime>] [-Skip <Int32>] [-First <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="0256f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0256f-105">DESCRIPTION</span></span>
<span data-ttu-id="0256f-106">Il cmdlet **Get-AzureStorSimpleJob** ottiene i processi di Azure StorSimple.</span><span class="sxs-lookup"><span data-stu-id="0256f-106">The **Get-AzureStorSimpleJob** cmdlet gets Azure StorSimple jobs.</span></span>
<span data-ttu-id="0256f-107">Specificare un ID istanza per ottenere un processo specifico.</span><span class="sxs-lookup"><span data-stu-id="0256f-107">Specify an instance ID to get a specific job.</span></span>
<span data-ttu-id="0256f-108">Specificare altri parametri per limitare i processi ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0256f-108">Specify other parameters to limit the jobs that this cmdlet gets.</span></span>

<span data-ttu-id="0256f-109">Questo cmdlet restituisce un massimo di 200 processi.</span><span class="sxs-lookup"><span data-stu-id="0256f-109">This cmdlet returns a maximum of 200 jobs.</span></span>
<span data-ttu-id="0256f-110">Se sono presenti più di 200 processi, ottenere i processi rimanenti usando i parametri *First* e *Skip* .</span><span class="sxs-lookup"><span data-stu-id="0256f-110">If more than 200 jobs exist, get the remaining jobs by using the *First* and *Skip* parameters.</span></span>
<span data-ttu-id="0256f-111">Se si specifica un valore di 100 per *Skip* e 50 per *First* , questo cmdlet non restituisce i primi 100 risultati.</span><span class="sxs-lookup"><span data-stu-id="0256f-111">If you specify a value of 100 for *Skip* and 50 for *First* , this cmdlet does not return the first 100 results.</span></span>
<span data-ttu-id="0256f-112">Restituisce i risultati successivi di 50 dopo il 100 che viene saltato.</span><span class="sxs-lookup"><span data-stu-id="0256f-112">It returns the next 50 results after the 100 that it skips.</span></span>

## <span data-ttu-id="0256f-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0256f-113">EXAMPLES</span></span>

### <span data-ttu-id="0256f-114">Esempio 1: ottenere un processo usando un ID</span><span class="sxs-lookup"><span data-stu-id="0256f-114">Example 1: Get a job by using an ID</span></span>
```
PS C:\>Get-AzureStorSimpleJob -InstanceId "574f47e0-44e9-495c-b8a5-0203c57ebf6d"
BackupPolicy             : 
BackupTimeStamp          : 1/1/0001 12:00:00 AM
BackupType               : CloudSnapshot
DataStats                : Microsoft.WindowsAzure.Management.StorSimple.Models.DataStatistics
Device                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
Entity                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
ErrorDetails             : {}
HideProgressDetails      : False
InstanceId               : 574f47e0-44e9-495c-b8a5-0203c57ebf6d
IsInstantRestoreComplete : False
IsJobCancellable         : True
JobDetails               : Microsoft.WindowsAzure.Management.StorSimple.Models.JobStatusInfo
Name                     : 26447caf-59bb-41c9-a028-3224d296c7dc
Progress                 : 100
SourceDevice             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
SourceEntity             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
SourceVolume             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
Status                   : Completed
TimeStats                : Microsoft.WindowsAzure.Management.StorSimple.Models.TimeStatistics
Type                     : Backup
Volume                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
```

<span data-ttu-id="0256f-115">Questo comando ottiene le informazioni per il processo con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="0256f-115">This command gets information for the job that has the specified ID.</span></span>

### <span data-ttu-id="0256f-116">Esempio 2: ottenere processi usando un nome di dispositivo</span><span class="sxs-lookup"><span data-stu-id="0256f-116">Example 2: Get jobs by using a device name</span></span>
```
PS C:\>Get-AzureStorSimpleJob -DeviceName "8600-Bravo 001" -First 2
InstanceId                           Type                         Status                                          DeviceName                                      StartTime                                       Progress                                       
----------                           ----                         ------                                          ----------                                      ---------                                       --------                                       
1997c33f-bfcc-4d08-9aba-28068340a1f9 Backup                       Running                                         8600-Bravo 001                                  4/15/2015 1:30:02 PM                            92                                             
85074062-ef6a-408a-b6c9-2a0904bb99ca Backup                       Completed                                       8600-Bravo 001                                  4/15/2015 1:30:02 PM                            100
```

<span data-ttu-id="0256f-117">Questo comando ottiene le informazioni per i processi per il dispositivo denominato 8600-bravo 001.</span><span class="sxs-lookup"><span data-stu-id="0256f-117">This command gets information for the jobs for the device named 8600-Bravo 001.</span></span>
<span data-ttu-id="0256f-118">Il comando ottiene i primi due processi per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0256f-118">The command gets the first two jobs for the device.</span></span>

### <span data-ttu-id="0256f-119">Esempio 3: ottenere processi completati</span><span class="sxs-lookup"><span data-stu-id="0256f-119">Example 3: Get completed jobs</span></span>
```
PS C:\>Get-AzureStorSimpleJob -Status "Completed" -Skip 10 -First 2
```

<span data-ttu-id="0256f-120">Questo comando ottiene i processi completati.</span><span class="sxs-lookup"><span data-stu-id="0256f-120">This command gets completed jobs.</span></span>
<span data-ttu-id="0256f-121">Il comando ottiene solo i primi due processi dopo che i primi dieci processi vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="0256f-121">The command gets only the first two jobs after it skips the first ten jobs.</span></span>

### <span data-ttu-id="0256f-122">Esempio 4: ottenere processi di backup manuali</span><span class="sxs-lookup"><span data-stu-id="0256f-122">Example 4: Get manual backup jobs</span></span>
```
PS C:\>Get-AzureStorSimpleJob -Type "ManualBackup"
```

<span data-ttu-id="0256f-123">Questo comando consente di ottenere i processi del tipo di backup manuale.</span><span class="sxs-lookup"><span data-stu-id="0256f-123">This command gets jobs of the manual backup type.</span></span>

### <span data-ttu-id="0256f-124">Esempio 5: ottenere processi tra orari specificati</span><span class="sxs-lookup"><span data-stu-id="0256f-124">Example 5: Get jobs between specified times</span></span>
```
PS C:\>$StartTime = Get-Date -Year 2015 -Month 3 -Day 10
PS C:\> $EndTime = Get-Date -Year 2015 -Month 3 -Day 11 -Hour 12 -Minute 15
PS C:\>Get-AzureStorSimpleJob -DeviceName "Device07" -From $StartTime -To $EndTime
```

<span data-ttu-id="0256f-125">I primi due comandi creano oggetti **DateTime** usando il cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="0256f-125">The first two commands create **DateTime** objects by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="0256f-126">I comandi archiviano i nuovi orari nelle variabili $StartTime e $EndTime.</span><span class="sxs-lookup"><span data-stu-id="0256f-126">The commands store the new times in the $StartTime and $EndTime variables.</span></span>
<span data-ttu-id="0256f-127">Per altre informazioni, digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="0256f-127">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="0256f-128">Il comando finale consente di ottenere i processi per il dispositivo denominato Device07 tra gli orari archiviati in $StartTime e $EndTime.</span><span class="sxs-lookup"><span data-stu-id="0256f-128">The final command gets jobs for the device named Device07 between the times stored in $StartTime and $EndTime.</span></span>

## <span data-ttu-id="0256f-129">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0256f-129">PARAMETERS</span></span>

### <span data-ttu-id="0256f-130">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="0256f-130">-DeviceName</span></span>
<span data-ttu-id="0256f-131">Specifica il nome di un dispositivo StorSimple.</span><span class="sxs-lookup"><span data-stu-id="0256f-131">Specifies the name of a StorSimple device.</span></span>

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

### <span data-ttu-id="0256f-132">-Primo</span><span class="sxs-lookup"><span data-stu-id="0256f-132">-First</span></span>
<span data-ttu-id="0256f-133">Ottiene solo il numero di oggetti specificato.</span><span class="sxs-lookup"><span data-stu-id="0256f-133">Gets only the specified number of objects.</span></span>
<span data-ttu-id="0256f-134">Immettere il numero di oggetti da ottenere.</span><span class="sxs-lookup"><span data-stu-id="0256f-134">Enter the number of objects to get.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0256f-135">-Da</span><span class="sxs-lookup"><span data-stu-id="0256f-135">-From</span></span>
<span data-ttu-id="0256f-136">Specifica la data e l'ora di inizio per i processi ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0256f-136">Specifies the start date and time for the jobs that this cmdlet gets.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0256f-137">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="0256f-137">-InstanceId</span></span>
<span data-ttu-id="0256f-138">Specifica l'ID del processo da ottenere.</span><span class="sxs-lookup"><span data-stu-id="0256f-138">Specifies the ID of the job to get.</span></span>

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

### <span data-ttu-id="0256f-139">-Profile</span><span class="sxs-lookup"><span data-stu-id="0256f-139">-Profile</span></span>
<span data-ttu-id="0256f-140">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0256f-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0256f-141">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="0256f-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0256f-142">-Skip</span><span class="sxs-lookup"><span data-stu-id="0256f-142">-Skip</span></span>
<span data-ttu-id="0256f-143">Ignora il numero di oggetti specificato e quindi recupera gli oggetti rimanenti.</span><span class="sxs-lookup"><span data-stu-id="0256f-143">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="0256f-144">Immettere il numero di oggetti da ignorare.</span><span class="sxs-lookup"><span data-stu-id="0256f-144">Enter the number of objects to skip.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0256f-145">-Stato</span><span class="sxs-lookup"><span data-stu-id="0256f-145">-Status</span></span>
<span data-ttu-id="0256f-146">Specifica lo stato.</span><span class="sxs-lookup"><span data-stu-id="0256f-146">Specifies the status.</span></span>
<span data-ttu-id="0256f-147">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="0256f-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0256f-148">Esecuzione</span><span class="sxs-lookup"><span data-stu-id="0256f-148">Running</span></span>
- <span data-ttu-id="0256f-149">Completato</span><span class="sxs-lookup"><span data-stu-id="0256f-149">Completed</span></span>
- <span data-ttu-id="0256f-150">Annullata</span><span class="sxs-lookup"><span data-stu-id="0256f-150">Cancelled</span></span>
- <span data-ttu-id="0256f-151">Fallito</span><span class="sxs-lookup"><span data-stu-id="0256f-151">Failed</span></span>
- <span data-ttu-id="0256f-152">Annullamento</span><span class="sxs-lookup"><span data-stu-id="0256f-152">Canceling</span></span>
- <span data-ttu-id="0256f-153">CompletedWithErrors</span><span class="sxs-lookup"><span data-stu-id="0256f-153">CompletedWithErrors</span></span>

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

### <span data-ttu-id="0256f-154">-To</span><span class="sxs-lookup"><span data-stu-id="0256f-154">-To</span></span>
<span data-ttu-id="0256f-155">Specifica la data e l'ora di fine per i processi ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0256f-155">Specifies the end date and time for the jobs that this cmdlet gets.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0256f-156">-Digitare</span><span class="sxs-lookup"><span data-stu-id="0256f-156">-Type</span></span>
<span data-ttu-id="0256f-157">Specifica il tipo di processo.</span><span class="sxs-lookup"><span data-stu-id="0256f-157">Specifies the job type.</span></span>
<span data-ttu-id="0256f-158">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="0256f-158">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0256f-159">Backup</span><span class="sxs-lookup"><span data-stu-id="0256f-159">Backup</span></span>
- <span data-ttu-id="0256f-160">ManualBackup</span><span class="sxs-lookup"><span data-stu-id="0256f-160">ManualBackup</span></span>
- <span data-ttu-id="0256f-161">Ripristinare</span><span class="sxs-lookup"><span data-stu-id="0256f-161">Restore</span></span>
- <span data-ttu-id="0256f-162">CloneWorkflow</span><span class="sxs-lookup"><span data-stu-id="0256f-162">CloneWorkflow</span></span>
- <span data-ttu-id="0256f-163">DeviceRestore</span><span class="sxs-lookup"><span data-stu-id="0256f-163">DeviceRestore</span></span>
- <span data-ttu-id="0256f-164">Aggiornamento</span><span class="sxs-lookup"><span data-stu-id="0256f-164">Update</span></span>
- <span data-ttu-id="0256f-165">SupportPackage</span><span class="sxs-lookup"><span data-stu-id="0256f-165">SupportPackage</span></span>
- <span data-ttu-id="0256f-166">VirtualApplianceProvisioning</span><span class="sxs-lookup"><span data-stu-id="0256f-166">VirtualApplianceProvisioning</span></span>

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

### <span data-ttu-id="0256f-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0256f-167">CommonParameters</span></span>
<span data-ttu-id="0256f-168">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0256f-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0256f-169">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0256f-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0256f-170">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0256f-170">INPUTS</span></span>

### <span data-ttu-id="0256f-171">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0256f-171">None</span></span>
<span data-ttu-id="0256f-172">Non è possibile reindirizzare l'input a questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0256f-172">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="0256f-173">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0256f-173">OUTPUTS</span></span>

### <span data-ttu-id="0256f-174">IList \<DeviceJobDetails\> , DeviceJobDetails</span><span class="sxs-lookup"><span data-stu-id="0256f-174">IList\<DeviceJobDetails\>, DeviceJobDetails</span></span>
<span data-ttu-id="0256f-175">Questo cmdlet restituisce un elenco di oggetti dettagli del processo oppure, se specifichi il parametro *InstanceID* , restituisce un singolo oggetto dettaglio processo.</span><span class="sxs-lookup"><span data-stu-id="0256f-175">This cmdlet returns a list of job details objects, or, if you specify the *InstanceID* parameter, it returns a single job detail object.</span></span>

## <span data-ttu-id="0256f-176">Note</span><span class="sxs-lookup"><span data-stu-id="0256f-176">NOTES</span></span>

## <span data-ttu-id="0256f-177">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0256f-177">RELATED LINKS</span></span>

[<span data-ttu-id="0256f-178">Stop-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="0256f-178">Stop-AzureStorSimpleJob</span></span>](./Stop-AzureStorSimpleJob.md)


