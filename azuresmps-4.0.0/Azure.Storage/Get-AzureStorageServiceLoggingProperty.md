---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: ''
schema: 2.0.0
ms.openlocfilehash: d615c0a807c12640f20a72b97a2c11c2efcd5b28
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93507052"
---
# Get-AzureStorageServiceLoggingProperty

## Sinossi
Ottiene le proprietà di registrazione per i servizi di archiviazione di Azure.

## SINTASSI

```
Get-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureStorageServiceLoggingProperty** ottiene le proprietà di registrazione per i servizi di archiviazione di Azure.

## ESEMPI

### Esempio 1: ottenere le proprietà di registrazione per il servizio BLOB
```
C:\PS>Get-AzureStorageServiceLoggingProperty -ServiceType Blob
```

Questo comando ottiene le proprietà di registrazione per l'archiviazione BLOB.

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

### -ServiceType
Specifica il tipo di servizio di archiviazione.
Questo cmdlet ottiene le proprietà di registrazione per il tipo di servizio specificato da questo parametro.
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

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

## Note

## COLLEGAMENTI CORRELATI

[New-AzureStorageContext](./New-AzureStorageContext.md)

[Set-AzureStorageServiceLoggingProperty](./Set-AzureStorageServiceLoggingProperty.md)


