---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8EED9813-5106-4D6C-B869-97BCBD7845AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67e354616161ad7f2d2467a37b92c355c7c8c39e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029773"
---
# Get-AzureSchedulerJob

## Sinossi
Ottiene un elenco dei processi di pianificazione o di un processo di pianificazione specifico.

## SINTASSI

```
Get-AzureSchedulerJob -Location <String> -JobCollectionName <String> [-JobName <String>] [-JobState <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.
Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .

Il cmdlet **Get-AzureSchedulerJobCollection** ottiene un elenco dei processi di pianificazione o di un processo di pianificazione specifico.

## ESEMPI

### Esempio 1: ottenere tutti i processi in una raccolta
```
PS C:\> Get-AzureSchedulerJob -Location "North Central US" -JobCollectionName "JobCollection01"
```

Questo comando ottiene i processi dell'utilità di pianificazione che fanno parte della raccolta processi denominata JobCollection01.

### Esempio 2: ottenere un processo denominato
```
PS C:\> Get-AzureSchedulerJob -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job01"
```

Questo comando ottiene il processo denominato Job01 dalla raccolta denominata JobCollection01 nella posizione specificata.

### Esempio 3: ottenere processi disabilitati in una raccolta
```
PS C:\> Get-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01" -JobState "Disabled"
```

Questo comando ottiene tutti i processi di pianificazione disabilitati che fanno parte di JobCollection01 nella posizione specificata.

## PARAMETRI

### -JobCollectionName
Specifica il nome della raccolta che contiene il processo di pianificazione da ottenere.

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

### -JobName
Specifica il nome di un processo di pianificazione da ottenere.

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

### -JobState
Specifica lo stato dei processi dell'utilità di pianificazione da ottenere.
I valori accettabili per questo parametro sono i seguenti:

- Abilitato
- Disabilitato
- Faulted
- Completato

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

### -Posizione
Specifica il nome della posizione che ospita il servizio cloud.
I valori accettabili per questo parametro sono i seguenti:

- Ovunque in Asia
- Ovunque Europa
- Ovunque negli Stati Uniti
- Asia orientale
- Stati Uniti orientali
- Stati Uniti nord-centrale
- Nord Europa
- Stati Uniti del centro sud
- Asia sud-orientale
- Europa occidentale
- Ovest degli Stati Uniti

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

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

## Note

## COLLEGAMENTI CORRELATI

[Remove-AzureSchedulerJob](./Remove-AzureSchedulerJob.md)


