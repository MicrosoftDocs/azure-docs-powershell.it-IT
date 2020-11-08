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
# Get-AzureStorSimpleJob

## Sinossi
Ottiene i processi di StorSimple.

## SINTASSI

```
Get-AzureStorSimpleJob [-DeviceName <String>] [-InstanceId <String>] [-Status <String>] [-Type <String>]
 [-From <DateTime>] [-To <DateTime>] [-Skip <Int32>] [-First <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureStorSimpleJob** ottiene i processi di Azure StorSimple.
Specificare un ID istanza per ottenere un processo specifico.
Specificare altri parametri per limitare i processi ottenuti da questo cmdlet.

Questo cmdlet restituisce un massimo di 200 processi.
Se sono presenti più di 200 processi, ottenere i processi rimanenti usando i parametri *First* e *Skip* .
Se si specifica un valore di 100 per *Skip* e 50 per *First* , questo cmdlet non restituisce i primi 100 risultati.
Restituisce i risultati successivi di 50 dopo il 100 che viene saltato.

## ESEMPI

### Esempio 1: ottenere un processo usando un ID
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

Questo comando ottiene le informazioni per il processo con l'ID specificato.

### Esempio 2: ottenere processi usando un nome di dispositivo
```
PS C:\>Get-AzureStorSimpleJob -DeviceName "8600-Bravo 001" -First 2
InstanceId                           Type                         Status                                          DeviceName                                      StartTime                                       Progress                                       
----------                           ----                         ------                                          ----------                                      ---------                                       --------                                       
1997c33f-bfcc-4d08-9aba-28068340a1f9 Backup                       Running                                         8600-Bravo 001                                  4/15/2015 1:30:02 PM                            92                                             
85074062-ef6a-408a-b6c9-2a0904bb99ca Backup                       Completed                                       8600-Bravo 001                                  4/15/2015 1:30:02 PM                            100
```

Questo comando ottiene le informazioni per i processi per il dispositivo denominato 8600-bravo 001.
Il comando ottiene i primi due processi per il dispositivo.

### Esempio 3: ottenere processi completati
```
PS C:\>Get-AzureStorSimpleJob -Status "Completed" -Skip 10 -First 2
```

Questo comando ottiene i processi completati.
Il comando ottiene solo i primi due processi dopo che i primi dieci processi vengono ignorati.

### Esempio 4: ottenere processi di backup manuali
```
PS C:\>Get-AzureStorSimpleJob -Type "ManualBackup"
```

Questo comando consente di ottenere i processi del tipo di backup manuale.

### Esempio 5: ottenere processi tra orari specificati
```
PS C:\>$StartTime = Get-Date -Year 2015 -Month 3 -Day 10
PS C:\> $EndTime = Get-Date -Year 2015 -Month 3 -Day 11 -Hour 12 -Minute 15
PS C:\>Get-AzureStorSimpleJob -DeviceName "Device07" -From $StartTime -To $EndTime
```

I primi due comandi creano oggetti **DateTime** usando il cmdlet Get-Date.
I comandi archiviano i nuovi orari nelle variabili $StartTime e $EndTime.
Per altre informazioni, digitare `Get-Help Get-Date` .

Il comando finale consente di ottenere i processi per il dispositivo denominato Device07 tra gli orari archiviati in $StartTime e $EndTime.

## PARAMETRI

### -DeviceName
Specifica il nome di un dispositivo StorSimple.

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

### -Primo
Ottiene solo il numero di oggetti specificato.
Immettere il numero di oggetti da ottenere.

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

### -Da
Specifica la data e l'ora di inizio per i processi ottenuti da questo cmdlet.

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

### -InstanceId
Specifica l'ID del processo da ottenere.

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

### -Profile
Specifica il profilo Azure da cui viene letto il cmdlet.
Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.

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

### -Skip
Ignora il numero di oggetti specificato e quindi recupera gli oggetti rimanenti.
Immettere il numero di oggetti da ignorare.

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

### -Stato
Specifica lo stato.
I valori accettabili per questo parametro sono i seguenti:

- Esecuzione
- Completato
- Annullata
- Fallito
- Annullamento
- CompletedWithErrors

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

### -To
Specifica la data e l'ora di fine per i processi ottenuti da questo cmdlet.

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

### -Digitare
Specifica il tipo di processo.
I valori accettabili per questo parametro sono i seguenti:

- Backup
- ManualBackup
- Ripristinare
- CloneWorkflow
- DeviceRestore
- Aggiornamento
- SupportPackage
- VirtualApplianceProvisioning

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

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno
Non è possibile reindirizzare l'input a questo cmdlet.

## OUTPUT

### IList \<DeviceJobDetails\> , DeviceJobDetails
Questo cmdlet restituisce un elenco di oggetti dettagli del processo oppure, se specifichi il parametro *InstanceID* , restituisce un singolo oggetto dettaglio processo.

## Note

## COLLEGAMENTI CORRELATI

[Stop-AzureStorSimpleJob](./Stop-AzureStorSimpleJob.md)


