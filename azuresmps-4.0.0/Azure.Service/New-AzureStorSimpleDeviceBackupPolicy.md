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
# New-AzureStorSimpleDeviceBackupPolicy

## Sinossi
Crea un criterio di backup.

## SINTASSI

```
New-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicyName <String>
 -BackupSchedulesToAdd <PSObject[]> -VolumeIdsToAdd <PSObject[]> [-WaitForComplete] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzureStorSimpleDeviceBackupPolicy** crea un criterio di backup.
Un criterio di backup contiene una o più pianificazioni di backup che possono essere eseguite in uno o più volumi.
Per creare una pianificazione di backup, usare il cmdlet **New-AzureStorSimpleDeviceBackupScheduleAddConfig** .

## ESEMPI

### Esempio 1: creare un criterio di backup
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

Il primo comando crea un oggetto di configurazione della pianificazione del backup usando il cmdlet **New-AzureStorSimpleDeviceBackupScheduleAddConfig** e quindi archivia tale oggetto nella variabile $Schedule 01.

Il secondo comando crea un altro oggetto di configurazione di backup usando **New-AzureStorSimpleDeviceBackupScheduleAddConfig** , quindi archivia l'oggetto nella variabile $Schedule 02.

Il terzo comando crea una variabile di matrice vuota, denominata $ScheduleArray.
I due comandi successivi aggiungono gli oggetti creati nei primi due comandi per $ScheduleArray.

Il sesto comando ottiene un contenitore di volumi per il dispositivo denominato Contoso63-AppVm usando il cmdlet **Get-AzureStorSimpleDeviceVolumeContainer** e quindi archivia l'oggetto contenitore nella variabile $DeviceContainer.

Il settimo comando ottiene un volume per il contenitore di volumi archiviato nel primo membro di $DeviceContainer usando il cmdlet **Get-AzureStorSimpleDeviceVolume** e quindi archivia tale volume nella variabile $volume.

L'ottavo comando crea una variabile di matrice vuota, denominata $VolumeArray.
Il comando successivo aggiunge un ID volume a $VolumeArray.
Questo valore identifica il volume, archiviato in $Volume, in cui vengono eseguiti i criteri di backup.
È possibile aggiungere altri ID di volume a $VolumeArray.

Il comando finale crea i criteri di backup denominati GeneralPolicy07 per il dispositivo denominato Contoso63-AppVm.
Il comando specifica gli oggetti di configurazione della pianificazione archiviati in $ScheduleArray.
Il comando specifica il volume o i volumi a cui applicare il criterio in $VolumeArray.
Puoi verificare i criteri di backup usando il cmdlet **Get-AzureStorSimpleDeviceBackupPolicy** .

## PARAMETRI

### -BackupPolicyName
Specifica il nome del criterio di backup.

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

### -BackupSchedulesToAdd
Specifica una matrice di oggetti **BackupScheduleBase** da aggiungere al criterio.
Ogni oggetto rappresenta una programmazione.
Un criterio di backup contiene una o più pianificazioni.
Per ottenere un oggetto **BackupScheduleBase** , usa il cmdlet **New-AzureStorSimpleDeviceBackupScheduleAddConfig** .

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

### -DeviceName
Specifica il nome del dispositivo StorSimple in cui creare i criteri di backup.

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

### -Profile
Specifica un profilo Azure.

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

### -VolumeIdsToAdd
Specifica una matrice di ID dei volumi da aggiungere ai criteri di backup.

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

### -WaitForComplete
Indica che questo cmdlet attende che l'operazione venga completata prima di restituire il controllo alla console di Windows PowerShell.

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

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno

## OUTPUT

### BackupPolicy
Questo cmdlet restituisce un oggetto **BackupPolicy** che contiene le nuove pianificazioni e i nuovi volumi.

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureStorSimpleDeviceBackupPolicy](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[Get-AzureStorSimpleDeviceVolume](./Get-AzureStorSimpleDeviceVolume.md)

[Get-AzureStorSimpleDeviceVolumeContainer](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[Remove-AzureStorSimpleDeviceBackupPolicy](./Remove-AzureStorSimpleDeviceBackupPolicy.md)

[Set-AzureStorSimpleDeviceBackupPolicy](./Set-AzureStorSimpleDeviceBackupPolicy.md)

[New-AzureStorSimpleDeviceBackupScheduleAddConfig](./New-AzureStorSimpleDeviceBackupScheduleAddConfig.md)


