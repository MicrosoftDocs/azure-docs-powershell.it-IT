---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 403AD2BF-5D03-4B48-A635-E08216FFFC0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 07df96f59b2278d804312d1076965ffed43c2569
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023706"
---
# <span data-ttu-id="2c7ce-101">Start-AzureStorSimpleBackupCloneJob</span><span class="sxs-lookup"><span data-stu-id="2c7ce-101">Start-AzureStorSimpleBackupCloneJob</span></span>

## <span data-ttu-id="2c7ce-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2c7ce-102">SYNOPSIS</span></span>
<span data-ttu-id="2c7ce-103">Avvia un processo che clona un backup in un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2c7ce-103">Starts a job that clones a backup on a device.</span></span>

## <span data-ttu-id="2c7ce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2c7ce-104">SYNTAX</span></span>

### <span data-ttu-id="2c7ce-105">Empty (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2c7ce-105">Empty (Default)</span></span>
```
Start-AzureStorSimpleBackupCloneJob -BackupId <String> -Snapshot <Snapshot> -CloneVolumeName <String>
 [-TargetAccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="2c7ce-106">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="2c7ce-106">IdentifyByName</span></span>
```
Start-AzureStorSimpleBackupCloneJob -SourceDeviceName <String> -TargetDeviceName <String> -BackupId <String>
 -Snapshot <Snapshot> -CloneVolumeName <String>
 [-TargetAccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="2c7ce-107">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="2c7ce-107">IdentifyById</span></span>
```
Start-AzureStorSimpleBackupCloneJob -SourceDeviceId <String> -TargetDeviceId <String> -BackupId <String>
 -Snapshot <Snapshot> -CloneVolumeName <String>
 [-TargetAccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2c7ce-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c7ce-108">DESCRIPTION</span></span>
<span data-ttu-id="2c7ce-109">Il cmdlet **Start-AzureStorSimpleBackupCloneJob** avvia un processo che clona un backup esistente in un dispositivo StorSimple.</span><span class="sxs-lookup"><span data-stu-id="2c7ce-109">The **Start-AzureStorSimpleBackupCloneJob** cmdlet starts a job that clones an existing backup on a StorSimple device.</span></span>

## <span data-ttu-id="2c7ce-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2c7ce-110">EXAMPLES</span></span>

### <span data-ttu-id="2c7ce-111">Esempio 1: duplicare un backup in un volume diverso usando i nomi dei dispositivi</span><span class="sxs-lookup"><span data-stu-id="2c7ce-111">Example 1: Clone a backup to a different volume by using device names</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "ContosoDev07" -First 1
PS C:\> $Acrs = Get-AzureStorSimpleAccessControlRecord -ACRName "Acr01"
PS C:\> Start-AzureStorSimpleBackupCloneJob -SourceDeviceName "ContosoDev07 -TargetDeviceName "ContosoDev07" -BackupId $Backup.InstanceId -Snapshot $Backup.Snapshots[0] -CloneVolumeName "cloned_volume11" -TargetAccessControlRecords $Acrs
VERBOSE: ClientRequestId: 43d8b4dc-39da-4ec5-92f6-be1f499155e9_PS
VERBOSE: ClientRequestId: be7a73a7-980c-4ba2-82d4-f6a7ee0eac0a_PS
VERBOSE: ClientRequestId: ee02aaae-d366-43d2-a229-8761d6db39f1_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 9b81d9f9-3e31-49be-a8cd-1b1c6afdb744_PS
bd05baee-36d0-48f4-8b1e-8119c4133446
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId bd05baee-36d0-48f4-8b1e-8119c4133446 for tracking the job's status
```

<span data-ttu-id="2c7ce-112">Il primo comando ottiene il primo backup per il dispositivo denominato ContosoDev07 usando il cmdlet **Get-AzureStorSimpleDeviceBackup** .</span><span class="sxs-lookup"><span data-stu-id="2c7ce-112">The first command gets the first backup for the device named ContosoDev07 by using the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>
<span data-ttu-id="2c7ce-113">Il comando Archivia il backup nella variabile $Backup.</span><span class="sxs-lookup"><span data-stu-id="2c7ce-113">The command stores that backup in the $Backup variable.</span></span>

<span data-ttu-id="2c7ce-114">Il secondo comando ottiene i record di controllo di accesso usando il cmdlet **Get-AzureStorSimpleAccessControlRecord** .</span><span class="sxs-lookup"><span data-stu-id="2c7ce-114">The second command gets access control records by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="2c7ce-115">Il comando Archivia il risultato nella variabile $Acrs.</span><span class="sxs-lookup"><span data-stu-id="2c7ce-115">The command stores the result in the $Acrs variable.</span></span>

<span data-ttu-id="2c7ce-116">Il comando finale avvia un processo che clona un backup specificato di un volume su un dispositivo con un volume diverso nello stesso dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2c7ce-116">The final command begins a job that clones a specified backup of a volume on a device to a different volume on the same device.</span></span>
<span data-ttu-id="2c7ce-117">Questo esempio specifica il dispositivo per nome.</span><span class="sxs-lookup"><span data-stu-id="2c7ce-117">This example specifies the device by name.</span></span>
<span data-ttu-id="2c7ce-118">Il comando usa i valori archiviati in $Backup e $Acrs.</span><span class="sxs-lookup"><span data-stu-id="2c7ce-118">The command uses the values stored in $Backup and $Acrs.</span></span>
<span data-ttu-id="2c7ce-119">Il comando restituisce l'ID del processo.</span><span class="sxs-lookup"><span data-stu-id="2c7ce-119">The command returns the ID of the job.</span></span>

### <span data-ttu-id="2c7ce-120">Esempio 2: duplicare un backup in un volume diverso usando gli ID dispositivo</span><span class="sxs-lookup"><span data-stu-id="2c7ce-120">Example 2: Clone a backup to a different volume by using device IDs</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName ContosoDev07 -First 1
PS C:\> $Acrs = Get-AzureStorSimpleAccessControlRecord -ACRName "Acr01"
PS C:\> Start-AzureStorSimpleBackupCloneJob -SourceDeviceId "be7a73a7-980c-4ba2-82d4-f6a7ee0eacbb" -TargetDeviceId "be7a73a7-980c-4ba2-82d4-f6a7ee0eacbb" -BackupId $Backup.InstanceId -Snapshot $Backup.Snapshots[0] -CloneVolumeName "cloned_volume11" -TargetAccessControlRecords $Acrs
VERBOSE: ClientRequestId: 43d8b4dc-39da-4ec5-92f6-be1f499155e9_PS
VERBOSE: ClientRequestId: be7a73a7-980c-4ba2-82d4-f6a7ee0eac0a_PS
VERBOSE: ClientRequestId: ee02aaae-d366-43d2-a229-8761d6db39f1_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 9b81d9f9-3e31-49be-a8cd-1b1c6afdb744_PS
bd05baee-36d0-48f4-8b1e-8119c4133446
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId bd05baee-36d0-48f4-8b1e-8119c4133446 for tracking the job's status
```

<span data-ttu-id="2c7ce-121">Il primo comando ottiene il primo backup per il dispositivo denominato ContosoDev07 usando il cmdlet **Get-AzureStorSimpleDeviceBackup** .</span><span class="sxs-lookup"><span data-stu-id="2c7ce-121">The first command gets the first backup for the device named ContosoDev07 by using the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>
<span data-ttu-id="2c7ce-122">Il comando Archivia il backup nella variabile $Backup.</span><span class="sxs-lookup"><span data-stu-id="2c7ce-122">The command stores that backup in the $Backup variable.</span></span>

<span data-ttu-id="2c7ce-123">Il secondo comando ottiene i record di controllo di accesso usando il cmdlet **Get-AzureStorSimpleAccessControlRecord** .</span><span class="sxs-lookup"><span data-stu-id="2c7ce-123">The second command gets access control records by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="2c7ce-124">Il comando Archivia il risultato nella variabile $Acrs.</span><span class="sxs-lookup"><span data-stu-id="2c7ce-124">The command stores the result in the $Acrs variable.</span></span>

<span data-ttu-id="2c7ce-125">Il comando finale avvia un processo che clona un backup specificato di un volume su un dispositivo con un volume diverso nello stesso dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2c7ce-125">The final command begins a job that clones a specified backup of a volume on a device to a different volume on the same device.</span></span>
<span data-ttu-id="2c7ce-126">Questo esempio specifica il dispositivo per ID dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2c7ce-126">This example specifies the device by device ID.</span></span>
<span data-ttu-id="2c7ce-127">Il comando usa i valori archiviati in $Backup e $Acrs.</span><span class="sxs-lookup"><span data-stu-id="2c7ce-127">The command uses the values stored in $Backup and $Acrs.</span></span>
<span data-ttu-id="2c7ce-128">Il comando restituisce l'ID del processo.</span><span class="sxs-lookup"><span data-stu-id="2c7ce-128">The command returns the ID of the job.</span></span>

### <span data-ttu-id="2c7ce-129">Esempio 3: duplicare un backup in un volume in un dispositivo diverso usando i nomi dei dispositivi</span><span class="sxs-lookup"><span data-stu-id="2c7ce-129">Example 3: Clone a backup to a volume on a different device by using device names</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "ContosoDev07" -First 1
PS C:\> $Acrs = Get-AzureStorSimpleAccessControlRecord -ACRName "Acr01"
PS C:\> Start-AzureStorSimpleBackupCloneJob -SourceDeviceName "ContosoDev07" -TargetDeviceName "ContosoDev12" -BackupId $Backup.InstanceId -Snapshot $Backup.Snapshots[0] -CloneVolumeName "cloned_volume11" -TargetAccessControlRecords $Acrs
VERBOSE: ClientRequestId: 43d8b4dc-39da-4ec5-92f6-be1f499155e9_PS
VERBOSE: ClientRequestId: be7a73a7-980c-4ba2-82d4-f6a7ee0eac0a_PS
VERBOSE: ClientRequestId: ee02aaae-d366-43d2-a229-8761d6db39f1_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 9b81d9f9-3e31-49be-a8cd-1b1c6afdb744_PS
bd05baee-36d0-48f4-8b1e-8119c4133446
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId bd05baee-36d0-48f4-8b1e-8119c4133446 for tracking the job's status
```

<span data-ttu-id="2c7ce-130">Il primo comando ottiene il primo backup per il dispositivo denominato ContosoDev07 usando il cmdlet **Get-AzureStorSimpleDeviceBackup** .</span><span class="sxs-lookup"><span data-stu-id="2c7ce-130">The first command gets the first backup for the device named ContosoDev07 by using the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>
<span data-ttu-id="2c7ce-131">Il comando Archivia il backup nella variabile $Backup.</span><span class="sxs-lookup"><span data-stu-id="2c7ce-131">The command stores that backup in the $Backup variable.</span></span>

<span data-ttu-id="2c7ce-132">Il secondo comando ottiene i record di controllo di accesso usando il cmdlet **Get-AzureStorSimpleAccessControlRecord** .</span><span class="sxs-lookup"><span data-stu-id="2c7ce-132">The second command gets access control records by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="2c7ce-133">Il comando Archivia il risultato nella variabile $Acrs.</span><span class="sxs-lookup"><span data-stu-id="2c7ce-133">The command stores the result in the $Acrs variable.</span></span>

<span data-ttu-id="2c7ce-134">Il comando finale avvia un processo che clona un backup specificato di un volume su un dispositivo in un dispositivo diverso.</span><span class="sxs-lookup"><span data-stu-id="2c7ce-134">The final command begins a job that clones a specified backup of a volume on a device to a volume on a different device.</span></span>
<span data-ttu-id="2c7ce-135">Questo esempio specifica i dispositivi per nome.</span><span class="sxs-lookup"><span data-stu-id="2c7ce-135">This example specifies the devices by name.</span></span>
<span data-ttu-id="2c7ce-136">Il comando usa i valori archiviati in $Backup e $Acrs.</span><span class="sxs-lookup"><span data-stu-id="2c7ce-136">The command uses the values stored in $Backup and $Acrs.</span></span>
<span data-ttu-id="2c7ce-137">Il comando restituisce l'ID del processo.</span><span class="sxs-lookup"><span data-stu-id="2c7ce-137">The command returns the ID of the job.</span></span>

### <span data-ttu-id="2c7ce-138">Esempio 4: duplicare un backup in un volume diverso usando i nomi dei dispositivi e l'operatore della pipeline</span><span class="sxs-lookup"><span data-stu-id="2c7ce-138">Example 4: Clone a backup to a different volume by using device names and the pipeline operator</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName ContosoDev1 -First 1
PS C:\> Get-AzureStorSimpleAccessControlRecord -ACRName acr1 | Start-AzureStorSimpleBackupCloneJob -SourceDeviceName ContosoDev1 -TargetDeviceName ContosoDev1 -BackupId $backup.InstanceId -Snapshot $backup.Snapshots[0] -CloneVolumeName "cloned_vol1" 
VERBOSE: ClientRequestId: 1183a29d-63a9-408a-9065-032c92d317ee_PS
VERBOSE: ClientRequestId: e195717c-5920-4133-bdf0-c1201ebabf6f_PS
VERBOSE: ClientRequestId: ac16644d-bfd8-4edf-b1ad-f5df4ceb4df7_PS
VERBOSE: ClientRequestId: dcdcab7f-2aaa-496d-8a18-2e7449a70227_PS
VERBOSE: ClientRequestId: 6f92e422-eda9-4087-aefb-2257a49f5beb_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 646b280c-b51c-4812-b5c5-b7ca215f1c90_PS
a747d2dc-2876-474e-aea6-6546b255427e
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId a747d2dc-2876-474e-aea6-6546b255427e for tracking the job's status
VERBOSE: Access Control Record with given name acr11 is found!
```

<span data-ttu-id="2c7ce-139">Il primo comando ottiene il primo backup per il dispositivo denominato ContosoDev07 usando il cmdlet **Get-AzureStorSimpleDeviceBackup** .</span><span class="sxs-lookup"><span data-stu-id="2c7ce-139">The first command gets the first backup for the device named ContosoDev07 by using the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>
<span data-ttu-id="2c7ce-140">Il comando Archivia il backup nella variabile $Backup.</span><span class="sxs-lookup"><span data-stu-id="2c7ce-140">The command stores that backup in the $Backup variable.</span></span>

<span data-ttu-id="2c7ce-141">Il secondo comando ottiene i record di controllo di accesso usando il cmdlet **Get-AzureStorSimpleAccessControlRecord** .</span><span class="sxs-lookup"><span data-stu-id="2c7ce-141">The second command gets access control records by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="2c7ce-142">Il comando passa i risultati al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="2c7ce-142">The command passes its results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2c7ce-143">Il cmdlet corrente avvia un processo che clona un backup specificato di un volume su un dispositivo, con un volume diverso nello stesso dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2c7ce-143">The current cmdlet begins a job that clones a specified backup of a volume on a device, to a different volume on the same device.</span></span>
<span data-ttu-id="2c7ce-144">Questo esempio specifica il dispositivo per nome.</span><span class="sxs-lookup"><span data-stu-id="2c7ce-144">This example specifies the device by name.</span></span>
<span data-ttu-id="2c7ce-145">Il comando usa il valore archiviato in $Backup.</span><span class="sxs-lookup"><span data-stu-id="2c7ce-145">The command uses the value stored in $Backup.</span></span>
<span data-ttu-id="2c7ce-146">Il comando accetta il valore del parametro *TargetAccessControlRecords* dalla pipeline.</span><span class="sxs-lookup"><span data-stu-id="2c7ce-146">The command takes the value of the *TargetAccessControlRecords* parameter from the pipeline.</span></span>
<span data-ttu-id="2c7ce-147">Il comando restituisce l'ID del processo.</span><span class="sxs-lookup"><span data-stu-id="2c7ce-147">The command returns the ID of the job.</span></span>

## <span data-ttu-id="2c7ce-148">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2c7ce-148">PARAMETERS</span></span>

### <span data-ttu-id="2c7ce-149">-BackupId</span><span class="sxs-lookup"><span data-stu-id="2c7ce-149">-BackupId</span></span>
<span data-ttu-id="2c7ce-150">Specifica l'ID istanza del backup da duplicare.</span><span class="sxs-lookup"><span data-stu-id="2c7ce-150">Specifies the instance ID of the backup to clone.</span></span>

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

### <span data-ttu-id="2c7ce-151">-CloneVolumeName</span><span class="sxs-lookup"><span data-stu-id="2c7ce-151">-CloneVolumeName</span></span>
<span data-ttu-id="2c7ce-152">Specifica il nome del nuovo volume clonato nel dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2c7ce-152">Specifies the name for the new cloned volume on the target device.</span></span>

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

### <span data-ttu-id="2c7ce-153">-Force</span><span class="sxs-lookup"><span data-stu-id="2c7ce-153">-Force</span></span>
<span data-ttu-id="2c7ce-154">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="2c7ce-154">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2c7ce-155">-Profile</span><span class="sxs-lookup"><span data-stu-id="2c7ce-155">-Profile</span></span>
<span data-ttu-id="2c7ce-156">Specifica un profilo Azure.</span><span class="sxs-lookup"><span data-stu-id="2c7ce-156">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="2c7ce-157">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="2c7ce-157">-Snapshot</span></span>
<span data-ttu-id="2c7ce-158">Specifica l'oggetto snapshot clonato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c7ce-158">Specifies the snapshot object that this cmdlet clones.</span></span>

```yaml
Type: Snapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c7ce-159">-SourceDeviceId</span><span class="sxs-lookup"><span data-stu-id="2c7ce-159">-SourceDeviceId</span></span>
<span data-ttu-id="2c7ce-160">Specifica l'ID istanza del dispositivo di origine.</span><span class="sxs-lookup"><span data-stu-id="2c7ce-160">Specifies the instance ID of the source device.</span></span>
<span data-ttu-id="2c7ce-161">Questo cmdlet clona il dorso dal dispositivo di origine.</span><span class="sxs-lookup"><span data-stu-id="2c7ce-161">This cmdlet clones the back from the source device.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c7ce-162">-SourceDeviceName</span><span class="sxs-lookup"><span data-stu-id="2c7ce-162">-SourceDeviceName</span></span>
<span data-ttu-id="2c7ce-163">Specifica il nome del dispositivo di origine.</span><span class="sxs-lookup"><span data-stu-id="2c7ce-163">Specifies the name of the source device.</span></span>
<span data-ttu-id="2c7ce-164">Questo cmdlet clona il dorso dal dispositivo di origine.</span><span class="sxs-lookup"><span data-stu-id="2c7ce-164">This cmdlet clones the back from the source device.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c7ce-165">-TargetAccessControlRecords</span><span class="sxs-lookup"><span data-stu-id="2c7ce-165">-TargetAccessControlRecords</span></span>
<span data-ttu-id="2c7ce-166">Specifica i record di controllo di Access.</span><span class="sxs-lookup"><span data-stu-id="2c7ce-166">Specifies the access control records.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c7ce-167">-TargetDeviceId</span><span class="sxs-lookup"><span data-stu-id="2c7ce-167">-TargetDeviceId</span></span>
<span data-ttu-id="2c7ce-168">Specifica l'ID istanza del dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2c7ce-168">Specifies the instance ID of the target device.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c7ce-169">-TargetDeviceName</span><span class="sxs-lookup"><span data-stu-id="2c7ce-169">-TargetDeviceName</span></span>
<span data-ttu-id="2c7ce-170">Specifica il nome del dispositivo a cui questo cmdlet clona il backup.</span><span class="sxs-lookup"><span data-stu-id="2c7ce-170">Specifies the name of the device to which this cmdlet clones the backup.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c7ce-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c7ce-171">CommonParameters</span></span>
<span data-ttu-id="2c7ce-172">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c7ce-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c7ce-173">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c7ce-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c7ce-174">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2c7ce-174">INPUTS</span></span>

### <span data-ttu-id="2c7ce-175">Snapshot, elenco di AccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="2c7ce-175">Snapshot, List of AccessControlRecord</span></span>
<span data-ttu-id="2c7ce-176">È possibile reindirizzare oggetti **snapshot** o un elenco di oggetti **AccessControlRecord** a questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c7ce-176">You can pipe **Snapshot** objects or a list of **AccessControlRecord** objects to this cmdlet.</span></span>

## <span data-ttu-id="2c7ce-177">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2c7ce-177">OUTPUTS</span></span>

## <span data-ttu-id="2c7ce-178">Note</span><span class="sxs-lookup"><span data-stu-id="2c7ce-178">NOTES</span></span>

## <span data-ttu-id="2c7ce-179">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2c7ce-179">RELATED LINKS</span></span>

[<span data-ttu-id="2c7ce-180">Get-AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="2c7ce-180">Get-AzureStorSimpleDeviceBackup</span></span>](./Get-AzureStorSimpleDeviceBackup.md)

[<span data-ttu-id="2c7ce-181">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="2c7ce-181">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)


