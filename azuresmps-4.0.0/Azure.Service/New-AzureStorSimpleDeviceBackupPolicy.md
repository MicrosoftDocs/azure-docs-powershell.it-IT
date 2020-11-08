---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: EFAE7117-9B8B-4CB9-B4D9-3F08DCE1816E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 405b9d427c7e59dfb3628806a878d57a281a6b4e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029670"
---
# <span data-ttu-id="b1bec-101">New-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="b1bec-101">New-AzureStorSimpleDeviceBackupPolicy</span></span>

## <span data-ttu-id="b1bec-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b1bec-102">SYNOPSIS</span></span>
<span data-ttu-id="b1bec-103">Crea un criterio di backup.</span><span class="sxs-lookup"><span data-stu-id="b1bec-103">Creates a backup policy.</span></span>

## <span data-ttu-id="b1bec-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b1bec-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicyName <String>
 -BackupSchedulesToAdd <PSObject[]> -VolumeIdsToAdd <PSObject[]> [-WaitForComplete] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="b1bec-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1bec-105">DESCRIPTION</span></span>
<span data-ttu-id="b1bec-106">Il cmdlet **New-AzureStorSimpleDeviceBackupPolicy** crea un criterio di backup.</span><span class="sxs-lookup"><span data-stu-id="b1bec-106">The **New-AzureStorSimpleDeviceBackupPolicy** cmdlet creates a backup policy.</span></span>
<span data-ttu-id="b1bec-107">Un criterio di backup contiene una o più pianificazioni di backup che possono essere eseguite in uno o più volumi.</span><span class="sxs-lookup"><span data-stu-id="b1bec-107">A backup policy contains one or more backup schedules that can run on one or more volumes.</span></span>
<span data-ttu-id="b1bec-108">Per creare una pianificazione di backup, usare il cmdlet **New-AzureStorSimpleDeviceBackupScheduleAddConfig** .</span><span class="sxs-lookup"><span data-stu-id="b1bec-108">To create a backup schedule, use the **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet.</span></span>

## <span data-ttu-id="b1bec-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b1bec-109">EXAMPLES</span></span>

### <span data-ttu-id="b1bec-110">Esempio 1: creare un criterio di backup</span><span class="sxs-lookup"><span data-stu-id="b1bec-110">Example 1: Create a backup policy</span></span>
```
PS C:\>$Schedule01 = New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType LocalSnapshot -RecurrenceType Daily -RecurrenceValue 10 -RetentionCount 5 -Enabled $True
PS C:\> $Schedule02 = New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType CloudSnapshot -RecurrenceType Hourly -RecurrenceValue 1 -RetentionCount 5 -Enabled $True
PS C:\> $ScheduleArray = @()
PS C:\> $ScheduleArray += $Schedule01
PS C:\> $ScheduleArray += $Schedule02
PS C:\> $DeviceContainer = Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm"
PS C:\> $Volume = $(Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeContainer $DeviceContainer[0])
PS C:\> $VolumeArray = @()
PS C:\> $VolumeArray += $Volume[0].InstanceId
PS C:\> New-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyName "GeneralPolicy07" -BackupSchedulesToAdd $ScheduleArray -VolumeIdsToAdd $VolumeArray
VERBOSE: ClientRequestId: e9d6771e-c323-47b9-b424-cb98f8ed0273_PS
VERBOSE: ClientRequestId: db0e7c86-d0d2-4a5a-b1cb-182494cba027_PS
VERBOSE: ClientRequestId: 77708dfd-a386-4999-b7ed-5d53e288ae83_PS


JobId        : d4ce5340-d5d1-4471-9cc8-013193f021b3
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your add operation has completed successfully. 
VERBOSE: ClientRequestId: bbf7e9b9-b493-40b3-8348-f15bcfc4da8a_PS
BackupSchedules          : {36d21096-bbd1-47b7-91b5-40ad1792d992, 505fc91f-deb5-4dca-bfcb-98c20b75ebcc}
Volumes                  : {volume03}
BackupPolicyCreationType : BySaaS
LastBackup               : 01-01-2010 05:30:00
NextBackup               : 16-12-2014 01:13:43
SchedulesCount           : 2
SSMHostName              : 
VolumesCount             : 1
InstanceId               : 8799c2f0-8850-4e91-aa23-ee18c67da8bd
Name                     : GeneralPolicy07
OperationInProgress      : None
```

<span data-ttu-id="b1bec-111">Il primo comando crea un oggetto di configurazione della pianificazione del backup usando il cmdlet **New-AzureStorSimpleDeviceBackupScheduleAddConfig** e quindi archivia tale oggetto nella variabile $Schedule 01.</span><span class="sxs-lookup"><span data-stu-id="b1bec-111">The first command creates a backup schedule configuration object by using the **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet, and then stores that object in the $Schedule01 variable.</span></span>

<span data-ttu-id="b1bec-112">Il secondo comando crea un altro oggetto di configurazione di backup usando **New-AzureStorSimpleDeviceBackupScheduleAddConfig** , quindi archivia l'oggetto nella variabile $Schedule 02.</span><span class="sxs-lookup"><span data-stu-id="b1bec-112">The second command creates another backup configuration object by using **New-AzureStorSimpleDeviceBackupScheduleAddConfig** , and then stores that object in the $Schedule02 variable.</span></span>

<span data-ttu-id="b1bec-113">Il terzo comando crea una variabile di matrice vuota, denominata $ScheduleArray.</span><span class="sxs-lookup"><span data-stu-id="b1bec-113">The third command creates an empty array variable, named $ScheduleArray.</span></span>
<span data-ttu-id="b1bec-114">I due comandi successivi aggiungono gli oggetti creati nei primi due comandi per $ScheduleArray.</span><span class="sxs-lookup"><span data-stu-id="b1bec-114">The next two commands add the objects created in the first two commands to $ScheduleArray.</span></span>

<span data-ttu-id="b1bec-115">Il sesto comando ottiene un contenitore di volumi per il dispositivo denominato Contoso63-AppVm usando il cmdlet **Get-AzureStorSimpleDeviceVolumeContainer** e quindi archivia l'oggetto contenitore nella variabile $DeviceContainer.</span><span class="sxs-lookup"><span data-stu-id="b1bec-115">The sixth command gets a volume container for the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet, and then stores that container object in the $DeviceContainer variable.</span></span>

<span data-ttu-id="b1bec-116">Il settimo comando ottiene un volume per il contenitore di volumi archiviato nel primo membro di $DeviceContainer usando il cmdlet **Get-AzureStorSimpleDeviceVolume** e quindi archivia tale volume nella variabile $volume.</span><span class="sxs-lookup"><span data-stu-id="b1bec-116">The seventh command gets a volume for the volume container stored in the first member of $DeviceContainer by using the **Get-AzureStorSimpleDeviceVolume** cmdlet, and then stores that volume in the $Volume variable.</span></span>

<span data-ttu-id="b1bec-117">L'ottavo comando crea una variabile di matrice vuota, denominata $VolumeArray.</span><span class="sxs-lookup"><span data-stu-id="b1bec-117">The eighth command creates an empty array variable, named $VolumeArray.</span></span>
<span data-ttu-id="b1bec-118">Il comando successivo aggiunge un ID volume a $VolumeArray.</span><span class="sxs-lookup"><span data-stu-id="b1bec-118">The next command adds a volume ID to $VolumeArray.</span></span>
<span data-ttu-id="b1bec-119">Questo valore identifica il volume, archiviato in $Volume, in cui vengono eseguiti i criteri di backup.</span><span class="sxs-lookup"><span data-stu-id="b1bec-119">This value identifies the volume, stored in $Volume, on which the backup policy runs.</span></span>
<span data-ttu-id="b1bec-120">È possibile aggiungere altri ID di volume a $VolumeArray.</span><span class="sxs-lookup"><span data-stu-id="b1bec-120">You can add additional volume IDs to $VolumeArray.</span></span>

<span data-ttu-id="b1bec-121">Il comando finale crea i criteri di backup denominati GeneralPolicy07 per il dispositivo denominato Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="b1bec-121">The final command creates the backup policy named GeneralPolicy07 for the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="b1bec-122">Il comando specifica gli oggetti di configurazione della pianificazione archiviati in $ScheduleArray.</span><span class="sxs-lookup"><span data-stu-id="b1bec-122">The command specifies the schedule configuration objects stored in $ScheduleArray.</span></span>
<span data-ttu-id="b1bec-123">Il comando specifica il volume o i volumi a cui applicare il criterio in $VolumeArray.</span><span class="sxs-lookup"><span data-stu-id="b1bec-123">The command specifies the volume or volumes to which to apply the policy in $VolumeArray.</span></span>
<span data-ttu-id="b1bec-124">Puoi verificare i criteri di backup usando il cmdlet **Get-AzureStorSimpleDeviceBackupPolicy** .</span><span class="sxs-lookup"><span data-stu-id="b1bec-124">You can verify the backup policy by using the **Get-AzureStorSimpleDeviceBackupPolicy** cmdlet.</span></span>

## <span data-ttu-id="b1bec-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b1bec-125">PARAMETERS</span></span>

### <span data-ttu-id="b1bec-126">-BackupPolicyName</span><span class="sxs-lookup"><span data-stu-id="b1bec-126">-BackupPolicyName</span></span>
<span data-ttu-id="b1bec-127">Specifica il nome del criterio di backup.</span><span class="sxs-lookup"><span data-stu-id="b1bec-127">Specifies the name of the backup policy.</span></span>

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

### <span data-ttu-id="b1bec-128">-BackupSchedulesToAdd</span><span class="sxs-lookup"><span data-stu-id="b1bec-128">-BackupSchedulesToAdd</span></span>
<span data-ttu-id="b1bec-129">Specifica una matrice di oggetti **BackupScheduleBase** da aggiungere al criterio.</span><span class="sxs-lookup"><span data-stu-id="b1bec-129">Specifies an array of **BackupScheduleBase** objects to add to the policy.</span></span>
<span data-ttu-id="b1bec-130">Ogni oggetto rappresenta una programmazione.</span><span class="sxs-lookup"><span data-stu-id="b1bec-130">Each object represents a schedule.</span></span>
<span data-ttu-id="b1bec-131">Un criterio di backup contiene una o più pianificazioni.</span><span class="sxs-lookup"><span data-stu-id="b1bec-131">A backup policy contains one or more schedules.</span></span>
<span data-ttu-id="b1bec-132">Per ottenere un oggetto **BackupScheduleBase** , usa il cmdlet **New-AzureStorSimpleDeviceBackupScheduleAddConfig** .</span><span class="sxs-lookup"><span data-stu-id="b1bec-132">To obtain a **BackupScheduleBase** object, use the **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1bec-133">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="b1bec-133">-DeviceName</span></span>
<span data-ttu-id="b1bec-134">Specifica il nome del dispositivo StorSimple in cui creare i criteri di backup.</span><span class="sxs-lookup"><span data-stu-id="b1bec-134">Specifies the name of the StorSimple device on which to create the backup policy.</span></span>

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

### <span data-ttu-id="b1bec-135">-Profile</span><span class="sxs-lookup"><span data-stu-id="b1bec-135">-Profile</span></span>
<span data-ttu-id="b1bec-136">Specifica un profilo Azure.</span><span class="sxs-lookup"><span data-stu-id="b1bec-136">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="b1bec-137">-VolumeIdsToAdd</span><span class="sxs-lookup"><span data-stu-id="b1bec-137">-VolumeIdsToAdd</span></span>
<span data-ttu-id="b1bec-138">Specifica una matrice di ID dei volumi da aggiungere ai criteri di backup.</span><span class="sxs-lookup"><span data-stu-id="b1bec-138">Specifies an array of the IDs of volumes to add to the backup policy.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1bec-139">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="b1bec-139">-WaitForComplete</span></span>
<span data-ttu-id="b1bec-140">Indica che questo cmdlet attende che l'operazione venga completata prima di restituire il controllo alla console di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b1bec-140">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="b1bec-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1bec-141">CommonParameters</span></span>
<span data-ttu-id="b1bec-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1bec-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1bec-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1bec-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1bec-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b1bec-144">INPUTS</span></span>

### <span data-ttu-id="b1bec-145">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b1bec-145">None</span></span>

## <span data-ttu-id="b1bec-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b1bec-146">OUTPUTS</span></span>

### <span data-ttu-id="b1bec-147">BackupPolicy</span><span class="sxs-lookup"><span data-stu-id="b1bec-147">BackupPolicy</span></span>
<span data-ttu-id="b1bec-148">Questo cmdlet restituisce un oggetto **BackupPolicy** che contiene le nuove pianificazioni e i nuovi volumi.</span><span class="sxs-lookup"><span data-stu-id="b1bec-148">This cmdlet returns a **BackupPolicy** object that contains the new schedules and volumes.</span></span>

## <span data-ttu-id="b1bec-149">Note</span><span class="sxs-lookup"><span data-stu-id="b1bec-149">NOTES</span></span>

## <span data-ttu-id="b1bec-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b1bec-150">RELATED LINKS</span></span>

[<span data-ttu-id="b1bec-151">Get-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="b1bec-151">Get-AzureStorSimpleDeviceBackupPolicy</span></span>](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="b1bec-152">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="b1bec-152">Get-AzureStorSimpleDeviceVolume</span></span>](./Get-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="b1bec-153">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="b1bec-153">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="b1bec-154">Remove-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="b1bec-154">Remove-AzureStorSimpleDeviceBackupPolicy</span></span>](./Remove-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="b1bec-155">Set-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="b1bec-155">Set-AzureStorSimpleDeviceBackupPolicy</span></span>](./Set-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="b1bec-156">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span><span class="sxs-lookup"><span data-stu-id="b1bec-156">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span></span>](./New-AzureStorSimpleDeviceBackupScheduleAddConfig.md)


