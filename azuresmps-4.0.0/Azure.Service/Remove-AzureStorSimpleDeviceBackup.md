---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 47650E39-758C-4D3C-9653-B70576CA0979
online version: ''
schema: 2.0.0
ms.openlocfilehash: a93791e3184fcabacbf90caebcb2170746922b36
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029929"
---
# Remove-AzureStorSimpleDeviceBackup

## Sinossi
Elimina un oggetto di backup.

## SINTASSI

### IdentifyById (impostazione predefinita)
```
Remove-AzureStorSimpleDeviceBackup -DeviceName <String> -BackupId <String> [-Force] [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByObject
```
Remove-AzureStorSimpleDeviceBackup -DeviceName <String> -Backup <Backup> [-Force] [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Remove-AzureStorSimpleDeviceBackup** Elimina un singolo oggetto backup.
Se si tenta di eliminare un backup già eliminato, questo cmdlet restituisce un errore.

## ESEMPI

### Esempio 1: rimuovere un backup per un dispositivo
```
PS C:\>Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupId "dcb5c991-0485-400f-8d0a-03a1341ee989" -Force
The remove job is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId 6c73aff2-f5a1-4b5e-
9a4e-857e128dc216 for tracking the job status
```

Questo comando rimuove il backup con l'ID specificato per il dispositivo denominato Contoso63-AppVm.
Il comando avvia l'operazione che rimuove l'oggetto di **backup** e quindi restituisce un oggetto **TaskResponse** .
Per visualizzare lo stato dell'attività, usa il cmdlet **Get-AzureStorSimpleTask** .

### Esempio 2: rimuovere il primo backup di un dispositivo usando il relativo ID
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm"
PS C:\> Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupId $Backup[0].InstanceId -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 53a656c3-c082-4e1f-afb7-bff3db45c791
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : f4411f38d07f68b88095682dbeedd9e9
```

Il primo comando consente di ottenere i backup per il dispositivo denominato Contoso63-AppVm e quindi di archiviarli nella variabile $Backup.

Il secondo comando Elimina un backup dal dispositivo denominato Contoso63-AppVm.
Il comando usa la notazione standard del punto per fare riferimento alla proprietà **InstanceID** del primo elemento della matrice $backup.
Questo comando specifica il parametro *WaitForComplete* e, di conseguenza, il comando attende fino al completamento dell'operazione e quindi restituisce un oggetto **TaskStatusInfo** .

### Esempio 3: rimuovere il primo backup di un dispositivo usando la pipeline
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso-AppVm" -WaitForComplete
PS C:\> $Backup[0] | Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso-AppVm" -Force -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 48059fd8-e355-4b91-9385-630d24f31df6
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : e1753f3bf68e6e44ab719436b5111e41
```

Il primo comando consente di ottenere i backup per il dispositivo denominato Contoso63-AppVm e quindi di archiviarli nella variabile $Backup.

Il secondo comando passa il primo oggetto archiviato nella matrice $Backup al cmdlet corrente.
Questo cmdlet elimina il backup dal dispositivo denominato Contoso63-AppVm.
Questo comando specifica il parametro *WaitForComplete* e, di conseguenza, il comando attende fino al completamento dell'operazione e quindi restituisce un oggetto **TaskStatusInfo** .

## PARAMETRI

### -Backup
Specifica l'oggetto di **backup** da eliminare.
Per ottenere un oggetto di **backup** , usare il cmdlet **Get-AzureStorSimpleDeviceBackup** .

```yaml
Type: Backup
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -BackupId
Specifica l'ID istanza di un backup da eliminare.

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

### -DeviceName
Specifica il nome del dispositivo StorSimple in cui eliminare un backup.

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

### -Force
Indica che questo cmdlet non richiede la conferma.

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

### Backup

## OUTPUT

### TaskStatusInfo, TaskResponse
Questo cmdlet restituisce un oggetto **TaskStatusInfo** se specifichi il parametro *WaitForComplete* se non specifichi tale parametro, restituisce un oggetto **TaskResponse** .

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureStorSimpleDeviceBackup](./Get-AzureStorSimpleDeviceBackup.md)


