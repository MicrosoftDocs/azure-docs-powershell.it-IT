---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: ''
schema: 2.0.0
ms.openlocfilehash: dd1acb41a6f67fb281500ad8a0d37cb3c2e0a6dd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93507167"
---
# Set-AzureStorageServiceLoggingProperty

## Sinossi
Modifica la registrazione per i servizi di archiviazione di Azure.

## SINTASSI

```
Set-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **set-AzureStorageServiceLoggingProperty** modifica la registrazione per i servizi di archiviazione di Azure.

## ESEMPI

### Esempio 1: modificare le proprietà di registrazione per il servizio BLOB
```
C:\PS>Set-AzureStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

Questo comando modifica la registrazione della versione 1,0 per l'archiviazione BLOB per includere le operazioni di lettura e scrittura.
La registrazione del servizio di archiviazione di Azure mantiene le voci per 10 giorni.
Poiché questo comando specifica il parametro *PassThru* , il comando Visualizza le proprietà di registrazione modificate.

## PARAMETRI

### -Contesto
Specifica un contesto di archiviazione di Azure.
Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -LoggingOperations
Specifica una matrice di operazioni del servizio di archiviazione di Azure.
Azure Storage Services registra le operazioni specificate da questo parametro.
I valori accettabili per questo parametro sono i seguenti:

- Nessuno
- Leggere
- Scrivere
- Eliminare
- Tutti

```yaml
Type: LoggingOperations[]
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read, Write, Delete, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Indica che questo cmdlet restituisce le proprietà di registrazione aggiornate.
Se non specifichi questo parametro, questo cmdlet non restituisce un valore.

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

### -RetentionDays
Specifica il numero di giorni in cui il servizio di archiviazione di Azure mantiene le informazioni registrate.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceType
Specifica il tipo di servizio di archiviazione.
Questo cmdlet modifica le proprietà di registrazione per il tipo di servizio specificato da questo parametro.
I valori accettabili per questo parametro sono i seguenti:

- BLOB 
- tavolo
- Coda
- File

Il valore di file non è attualmente supportato.

```yaml
Type: StorageServiceType
Parameter Sets: (All)
Aliases: 
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Versione
Specifica la versione della registrazione del servizio di archiviazione di Azure.
Il valore predefinito è 1,0.

```yaml
Type: Double
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

[Get-AzureStorageServiceLoggingProperty](./Get-AzureStorageServiceLoggingProperty.md)

[New-AzureStorageContext](./New-AzureStorageContext.md)


