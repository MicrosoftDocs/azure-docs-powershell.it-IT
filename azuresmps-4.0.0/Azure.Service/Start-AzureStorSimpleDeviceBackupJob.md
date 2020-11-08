---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 76826524-480F-458E-A996-A9DBACB8BA9E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4aa220334c75d3e6832698ec10fbad71896473d2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029489"
---
# Start-AzureStorSimpleDeviceBackupJob

## Sinossi
Avvia un nuovo processo che crea un backup da un criterio di backup esistente.

## SINTASSI

### Empty (impostazione predefinita)
```
Start-AzureStorSimpleDeviceBackupJob -DeviceName <String> -BackupPolicyId <String> [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### BackupTypeGiven
```
Start-AzureStorSimpleDeviceBackupJob -DeviceName <String> -BackupPolicyId <String> -BackupType <String>
 [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Start-AzureStorSimpleDeviceBackupJob** avvia un nuovo processo che crea un backup da un criterio di backup esistente in un dispositivo StorSimple.
Per impostazione predefinita, questo cmdlet crea un backup dello snapshot locale.
Per creare un backup cloud, specificare un valore di CloudSnapshot per il parametro *BackupType* .

## ESEMPI

### Esempio 1: creare un backup dello snapshot locale
```
PS C:\>Start-AzureStorSimpleDeviceBackupJob -DeviceName "Contoso63-AppVm" -BackupPolicyId "de088eac-b283-4d92-b501-a759845fdf3f"
JobId                                                                StatusCode RequestId
-----                                                                ---------- ---------
fb9acdca-ed6f-4b69-93f2-5c0bce0a1e08                                 Accepted   456cf6bafd427103b71c07145e26d35c

VERBOSE: Your backup operation has been submitted for processing. Use commandlet "Get-AzureStorSimpleJob -JobId
fb9acdca-ed6f-4b69-93f2-5c0bce0a1e08" to track status.
```

Questo comando crea un backup dello snapshot locale per l'ID dei criteri specificato.
Questo comando avvia il processo e quindi restituisce un oggetto **TaskResponse** .
Per visualizzare lo stato del processo, usare il cmdlet **Get-AzureStorSimpleTask** .

### Esempio 2: creare un backup snapshot del cloud e attendere la fine
```
PS C:\>Start-AzureStorSimpleDeviceBackupJob -DeviceName "Contoso63-AppVm" -BackupPolicyId "de088eac-b283-4d92-b501-a759845fdf3f" -BackupType CloudSnapshot -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : fb9acdca-ed6f-4b69-93f2-5c0bce0a1e08
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : f28ecf6cf75a7f128ca18e6ae14f9003
```

Questo comando crea un backup snapshot del cloud per l'ID dei criteri specificato.
Questo comando specifica il parametro *WaitForComplete* , quindi il comando completa l'attività e quindi restituisce un oggetto **TaskStatusInfo** per il processo.

## PARAMETRI

### -BackupPolicyId
Specifica l'ID dei criteri di backup da usare per creare il backup.

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

### -BackupType
Specifica il tipo di backup.
I valori validi sono: LocalSnapshot e CloudSnapshot.

```yaml
Type: String
Parameter Sets: BackupTypeGiven
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName
Specifica il nome del dispositivo StorSimple in cui avviare il processo di backup.

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

### TaskStatusInfo, TaskResponse
Questo cmdlet restituisce un oggetto **TaskStatusInfo** se specifichi il parametro *WaitForComplete* .
Se non specifichi tale parametro, restituisce un oggetto **TaskResponse** .

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureStorSimpleJob](./Get-AzureStorSimpleJob.md)

[Start-AzureStorSimpleDeviceBackupRestoreJob](./Start-AzureStorSimpleDeviceBackupRestoreJob.md)


