---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2BF5BDF8-3743-46FC-8E04-1A4EA920A2AF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 77b4d184ffbdb1d054f3d14aa3c51c8d2afc928b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029772"
---
# Get-AzureSchedulerJobHistory

## Sinossi
Ottiene la cronologia per un processo di pianificazione.

## SINTASSI

```
Get-AzureSchedulerJobHistory -Location <String> -JobCollectionName <String> -JobName <String>
 [-JobStatus <String>] [-Profile <AzureSMProfile>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

## Descrizione
Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.
Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .

Il cmdlet **Get-AzureSchedulerJobHistory** ottiene la cronologia per un processo di pianificazione.

## ESEMPI

### Esempio 1: ottenere la cronologia di un processo usando il relativo nome
```
PS C:\> Get-AzureSchedulerJobHistory -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job01"
```

Questo comando consente di ottenere la cronologia del processo denominato Job01.
Tale processo appartiene alla raccolta processi denominata JobCollection01 nella posizione specificata.

### Esempio 2: ottenere la cronologia per un processo non riuscito usando il relativo nome
```
PS C:\> Get-AzureSchedulerJobHistory -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job12" -JobStatus "Failed"
```

Questo comando consente di ottenere la cronologia del processo denominato Job12 con stato non riuscito.
Tale processo appartiene alla raccolta processi denominata JobCollection01 nella posizione specificata.

## PARAMETRI

### -Primo
Ottiene solo il numero di oggetti specificato.
Immettere il numero di oggetti da ottenere.

```yaml
Type: UInt64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeTotalCount
Indica il numero totale di oggetti nel set di dati (un numero intero) seguito dagli oggetti selezionati.
Se il cmdlet non riesce a determinare il conteggio totale, Visualizza "numero totale sconosciuto". Il numero intero ha una proprietà di precisione che indica l'affidabilità del valore di conteggio totale.
Il valore di precisione è compreso tra 0,0 e 1,0, dove 0,0 indica che il cmdlet non ha potuto contare gli oggetti, 1,0 significa che il conteggio è esatto e un valore compreso tra 0,0 e 1,0 è una stima sempre più attendibile.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobCollectionName
Specifica il nome di una raccolta processi dell'utilità di pianificazione.
Questo cmdlet consente di ottenere la cronologia di un processo che appartiene alla raccolta specificata da questo parametro.

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
Specifica il nome di un processo di pianificazione per cui ottenere la cronologia.

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

### -JobStatus
Specifica lo stato del processo di pianificazione per cui ottenere la cronologia.
I valori accettabili per questo parametro sono i seguenti:

- Completato
- Fallito

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
I valori validi sono: 

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

### -Skip
Ignora il numero di oggetti specificato e quindi recupera gli oggetti rimanenti.
Immettere il numero di oggetti da ignorare.

```yaml
Type: UInt64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureSchedulerJob](./Get-AzureSchedulerJob.md)

[Get-AzureSchedulerJobCollection](./Get-AzureSchedulerJobCollection.md)


