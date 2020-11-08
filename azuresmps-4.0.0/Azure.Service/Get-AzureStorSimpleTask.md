---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: CF3548F6-03FE-44D6-AA2C-1015611C657A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0423fe51a047385ef6395075dd116b4d4189c667
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023510"
---
# Get-AzureStorSimpleTask

## Sinossi
Ottiene lo stato di un'attività in un dispositivo StorSimple.

## SINTASSI

```
Get-AzureStorSimpleTask -InstanceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureStorSimpleTask** recupera lo stato di un'attività che viene eseguita in modo asincrono in un dispositivo StorSimple di Azure.

Durante la gestione di un dispositivo StorSimple, la maggior parte delle operazioni di creazione, lettura, aggiornamento ed eliminazione può essere eseguita in modo asincrono.
Windows PowerShell restituisce un **taskId**.
Usa l'ID per ottenere lo stato corrente dell'attività.

## ESEMPI

### Esempio 1: ottenere lo stato di un'attività
```
PS C:\>Get-AzureStorSimpleTask -TaskId "53816d8d-a8b5-4c1d-a177-e59007608d6d"
VERBOSE: ClientRequestId: d9c1e8a7-994f-4698-8b42-064600b45cad_PS
VERBOSE: ClientRequestId: aae17c82-6fd3-435e-a965-1c66b3c955fe_PS


AsyncTaskAggregatedResult : Succeeded
Error                     : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
Result                    : Succeeded
Status                    : Completed
TaskId                    : 53816d8d-a8b5-4c1d-a177-e59007608d6d
TaskSteps                 : {}
StatusCode                : OK
RequestId                 : e9174990825750bba69383748f23019c
```

Questo comando ottiene lo stato dell'attività con l'ID specificato.
I risultati indicano che l'attività ha uno stato completato e il risultato è riuscito.

## PARAMETRI

### -InstanceId
Specifica l'ID dell'attività per cui questo cmdlet tiene traccia dello stato.

```yaml
Type: String
Parameter Sets: (All)
Aliases: TaskId

Required: True
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

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno

## OUTPUT

### JobStatusInfo
Questo cmdlet restituisce un oggetto **TaskStatusInfo** che contiene i campi seguenti: 

- **Errore**.
**ErrorDetails** , che contiene il **codice** e il **messaggio**.
- **TaskId**.
**Stringa**.
ID dell'attività per cui viene restituito lo stato.
- **TaskSteps**.
**IList \<TaskStep\>**.
Ogni oggetto **TaskStep** contiene **Dettagli** , **ErrorCode** , **messaggio** , **risultato** e **stato**.
- **Risultato**.
**TaskResult** , che contiene il risultato complessivo dell'attività.
I valori validi sono: non riuscito, riuscito, PartialSuccess, annullato e non valido.
- **Stato**.
**TaskStatus** , che contiene lo stato di avanzamento complessivo dell'attività.
I valori validi sono: InProgress, non valido e completato.
- **TaskResult**.
**TaskResult** , un valore calcolato in base al **risultato** e **allo stato**.
I valori validi sono: non riuscito, riuscito, InProgress, PartialSuccess, annullato e non valido.

## Note

## COLLEGAMENTI CORRELATI

