---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F619B52A-6BFD-43E4-B313-F4C8D95EA966
online version: ''
schema: 2.0.0
ms.openlocfilehash: 570fdc21d650666e1cededbea597a5ef34023596
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023810"
---
# <span data-ttu-id="0f284-101">Set-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="0f284-101">Set-AzureStorSimpleDeviceBackupPolicy</span></span>

## <span data-ttu-id="0f284-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0f284-102">SYNOPSIS</span></span>
<span data-ttu-id="0f284-103">Aggiorna un criterio di backup esistente.</span><span class="sxs-lookup"><span data-stu-id="0f284-103">Updates an existing backup policy.</span></span>

## <span data-ttu-id="0f284-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0f284-104">SYNTAX</span></span>

```
Set-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicyId <String> -BackupPolicyName <String>
 [-BackupSchedulesToAdd <PSObject[]>] [-BackupSchedulesToUpdate <PSObject[]>]
 [-BackupScheduleIdsToDelete <PSObject[]>] [-VolumeIdsToUpdate <PSObject[]>] [-WaitForComplete]
 [-NewName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0f284-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0f284-105">DESCRIPTION</span></span>
<span data-ttu-id="0f284-106">Il cmdlet **set-AzureStorSimpleDeviceBackupPolicy** aggiorna un criterio di backup esistente.</span><span class="sxs-lookup"><span data-stu-id="0f284-106">The **Set-AzureStorSimpleDeviceBackupPolicy** cmdlet updates an existing backup policy.</span></span>
<span data-ttu-id="0f284-107">È possibile rinominare i criteri, aggiungere, aggiornare o eliminare le pianificazioni e aggiornare i volumi associati al criterio.</span><span class="sxs-lookup"><span data-stu-id="0f284-107">You can rename the policy, add, update or delete schedules, and update the volumes associated with the policy.</span></span>

## <span data-ttu-id="0f284-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0f284-108">EXAMPLES</span></span>

### <span data-ttu-id="0f284-109">Esempio 1: cambiare il nome di un criterio di backup</span><span class="sxs-lookup"><span data-stu-id="0f284-109">Example 1: Change the name of a backup policy</span></span>
```
PS C:\>Set-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyId "e6d9f1b3-a250-4d57-966a-039c8eaef9e9" -BackupPolicyName "UpdatedGeneralPolicy07" -WaitForComplete
VERBOSE: ClientRequestId: f4465b46-26cc-40ff-88da-7a28df88c35c_PS
VERBOSE: ClientRequestId: 5e33a35c-e089-47c1-b760-474635b1ead8_PS
VERBOSE: About to run a task to update your backuppolicy! 
VERBOSE: ClientRequestId: e379ebdb-667f-45a9-aafa-a6cd61e5f6f6_PS


JobId        : 9d621bfd-3faa-4d1c-b28b-45c5f4a96975
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your update operation has completed successfully. 
VERBOSE: ClientRequestId: 4fe965ea-4e12-4869-9d67-e42a24b6c5d8_PS
BackupSchedules          : {58e9cd7c-4c6a-4e33-9109-5ec0b8fcb2cc, b10e1bf4-ef0a-4ad3-8fde-eecfc9971dd2}
Volumes                  : {testvolume03}
BackupPolicyCreationType : BySaaS
LastBackup               : 12/16/2014 2:13:28 PM
NextBackup               : 12/16/2014 3:13:43 PM
SchedulesCount           : 2
SSMHostName              : 
VolumesCount             : 1
InstanceId               : e6d9f1b3-a250-4d57-966a-039c8eaef9e9
Name                     : UpdatedGeneralPolicy07
OperationInProgress      : None
```

<span data-ttu-id="0f284-110">Questo comando modifica il nome del criterio di backup con l'ID specificato in UpdatedGeneralPolicy07.</span><span class="sxs-lookup"><span data-stu-id="0f284-110">This command changes the name of the backup policy that has the specified ID to UpdatedGeneralPolicy07.</span></span>
<span data-ttu-id="0f284-111">Questo comando specifica il parametro *WaitForComplete* , quindi il comando completa l'attività e quindi restituisce un oggetto **TaskStatusInfo** per l'attività.</span><span class="sxs-lookup"><span data-stu-id="0f284-111">This command specifies the *WaitForComplete* parameter, so the command completes the task, and then returns a **TaskStatusInfo** object for the task.</span></span>

### <span data-ttu-id="0f284-112">Esempio 2: aggiornare la pianificazione per un criterio di backup</span><span class="sxs-lookup"><span data-stu-id="0f284-112">Example 2: Update the schedule for a backup policy</span></span>
```
PS C:\>$UpdateConfig = New-AzureStorSimpleDeviceBackupScheduleUpdateConfig -Id "3a6c6247-6b4d-42e2-aa87-16f4f21476ea" -BackupType CloudSnapshot -RecurrenceType Daily -RecurrenceValue 3 -RetentionCount 2 -Enabled $True
PS C:\> $UpdateArray = @()
PS C:\> $UpdateArray += $UpdateConfig
PS C:\> Set-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyId "712605f6-eb03-4db8-8f79-e0ce64b2cce1" -BackupSchedulesToUpdate $UpdateArray
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 7b265417-a5f1-45ad-8fbc-33bad4f63ec9
JobSteps   : {Microsoft.WindowsAzure.Management.StorSimple.Models.JobStep, 
             Microsoft.WindowsAzure.Management.StorSimple.Models.JobStep, 
             Microsoft.WindowsAzure.Management.StorSimple.Models.JobStep, 
             Microsoft.WindowsAzure.Management.StorSimple.Models.JobStep...} 
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : d2e10d44e699b371a84db44d19daf1c3
```

<span data-ttu-id="0f284-113">Il primo comando crea un oggetto di configurazione di aggiornamento usando il cmdlet **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** e lo archivia nella variabile $UpdateConfig.</span><span class="sxs-lookup"><span data-stu-id="0f284-113">The first command creates an update configuration object by using the **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** cmdlet, and then stores it in the $UpdateConfig variable.</span></span>

<span data-ttu-id="0f284-114">Il secondo comando crea una nuova variabile di matrice, denominata $UpdateArray.</span><span class="sxs-lookup"><span data-stu-id="0f284-114">The second command creates a new array variable, named $UpdateArray.</span></span>
<span data-ttu-id="0f284-115">Il comando successivo aggiunge l'aggiornamento archiviato in $UpdateConfig alla matrice.</span><span class="sxs-lookup"><span data-stu-id="0f284-115">The next command adds the update stored in $UpdateConfig to that array.</span></span>
<span data-ttu-id="0f284-116">È possibile aggiungere più di un aggiornamento alla matrice.</span><span class="sxs-lookup"><span data-stu-id="0f284-116">You can add more than one update to the array.</span></span>

<span data-ttu-id="0f284-117">Il comando finale aggiorna i criteri di backup con l'ID specificato nel dispositivo denominato Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="0f284-117">The final command updates the backup policy that has the specified ID on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="0f284-118">Il criterio ha ora la pianificazione aggiornata archiviata in $UpdateArray.</span><span class="sxs-lookup"><span data-stu-id="0f284-118">The policy now has the updated schedule stored in $UpdateArray.</span></span>

## <span data-ttu-id="0f284-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0f284-119">PARAMETERS</span></span>

### <span data-ttu-id="0f284-120">-BackupPolicyId</span><span class="sxs-lookup"><span data-stu-id="0f284-120">-BackupPolicyId</span></span>
<span data-ttu-id="0f284-121">Specifica l'ID istanza dell'oggetto **BackupPolicy** da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="0f284-121">Specifies the instance ID of the **BackupPolicy** object to update.</span></span>

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

### <span data-ttu-id="0f284-122">-BackupPolicyName</span><span class="sxs-lookup"><span data-stu-id="0f284-122">-BackupPolicyName</span></span>
<span data-ttu-id="0f284-123">Specifica un nuovo nome per i criteri di backup.</span><span class="sxs-lookup"><span data-stu-id="0f284-123">Specifies a new name for the backup policy.</span></span>

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

### <span data-ttu-id="0f284-124">-BackupScheduleIdsToDelete</span><span class="sxs-lookup"><span data-stu-id="0f284-124">-BackupScheduleIdsToDelete</span></span>
<span data-ttu-id="0f284-125">Specifica una matrice di ID di istanza degli oggetti **BackupSchedule** da eliminare.</span><span class="sxs-lookup"><span data-stu-id="0f284-125">Specifies an array of instance IDs of **BackupSchedule** objects to delete.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f284-126">-BackupSchedulesToAdd</span><span class="sxs-lookup"><span data-stu-id="0f284-126">-BackupSchedulesToAdd</span></span>
<span data-ttu-id="0f284-127">Specifica una matrice di oggetti **BackupScheduleBase** da aggiungere al criterio.</span><span class="sxs-lookup"><span data-stu-id="0f284-127">Specifies an array of **BackupScheduleBase** objects to add to the policy.</span></span>
<span data-ttu-id="0f284-128">Per ottenere un oggetto **BackupScheduleBase** , usa il cmdlet **New-AzureStorSimpleDeviceBackupScheduleAddConfig** .</span><span class="sxs-lookup"><span data-stu-id="0f284-128">To obtain a **BackupScheduleBase** object, use the **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f284-129">-BackupSchedulesToUpdate</span><span class="sxs-lookup"><span data-stu-id="0f284-129">-BackupSchedulesToUpdate</span></span>
<span data-ttu-id="0f284-130">Specifica una matrice di oggetti **BackupScheduleUpdateRequest** da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="0f284-130">Specifies an array of **BackupScheduleUpdateRequest** objects to update.</span></span>
<span data-ttu-id="0f284-131">Per ottenere un oggetto **BackupScheduleUpdateRequest** , usa il cmdlet **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** .</span><span class="sxs-lookup"><span data-stu-id="0f284-131">To obtain a **BackupScheduleUpdateRequest** object, use the **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** cmdlet.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f284-132">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="0f284-132">-DeviceName</span></span>
<span data-ttu-id="0f284-133">Specifica il nome del dispositivo StorSimple per il quale aggiornare i criteri di backup.</span><span class="sxs-lookup"><span data-stu-id="0f284-133">Specifies the name of the StorSimple device for which to update the backup policy.</span></span>

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

### <span data-ttu-id="0f284-134">-NewName</span><span class="sxs-lookup"><span data-stu-id="0f284-134">-NewName</span></span>
<span data-ttu-id="0f284-135">Specifica un nome per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0f284-135">Specifies a name for the device.</span></span>

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

### <span data-ttu-id="0f284-136">-Profile</span><span class="sxs-lookup"><span data-stu-id="0f284-136">-Profile</span></span>
<span data-ttu-id="0f284-137">Specifica un profilo Azure.</span><span class="sxs-lookup"><span data-stu-id="0f284-137">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="0f284-138">-VolumeIdsToUpdate</span><span class="sxs-lookup"><span data-stu-id="0f284-138">-VolumeIdsToUpdate</span></span>
<span data-ttu-id="0f284-139">Specifica una matrice di ID di volumi per cui aggiornare i criteri di backup.</span><span class="sxs-lookup"><span data-stu-id="0f284-139">Specifies an array of IDs of volumes for which to update backup policies.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f284-140">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="0f284-140">-WaitForComplete</span></span>
<span data-ttu-id="0f284-141">Indica che questo cmdlet attende che l'operazione venga completata prima di restituire il controllo alla console di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0f284-141">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="0f284-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f284-142">CommonParameters</span></span>
<span data-ttu-id="0f284-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f284-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f284-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f284-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f284-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0f284-145">INPUTS</span></span>

### <span data-ttu-id="0f284-146">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0f284-146">None</span></span>

## <span data-ttu-id="0f284-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0f284-147">OUTPUTS</span></span>

### <span data-ttu-id="0f284-148">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="0f284-148">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="0f284-149">Questo cmdlet restituisce un oggetto **TaskStatusInfo** se specifichi il parametro *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="0f284-149">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="0f284-150">Se non specifichi tale parametro, restituisce un oggetto **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="0f284-150">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="0f284-151">Note</span><span class="sxs-lookup"><span data-stu-id="0f284-151">NOTES</span></span>

## <span data-ttu-id="0f284-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0f284-152">RELATED LINKS</span></span>

[<span data-ttu-id="0f284-153">Get-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="0f284-153">Get-AzureStorSimpleDeviceBackupPolicy</span></span>](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="0f284-154">New-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="0f284-154">New-AzureStorSimpleDeviceBackupPolicy</span></span>](./New-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="0f284-155">Remove-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="0f284-155">Remove-AzureStorSimpleDeviceBackupPolicy</span></span>](./Remove-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="0f284-156">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="0f284-156">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span></span>](./New-AzureStorSimpleDeviceBackupScheduleUpdateConfig.md)


