---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5FA8A3F3-F52C-40BC-94C2-4CDA00C6F32F
online version: ''
schema: 2.0.0
ms.openlocfilehash: c65daf144708340649b9f7b1566c5e5f2dd81e45
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93507080"
---
# Get-AzureStorageCORSRule

## Sinossi
Ottiene le regole di CORS per un tipo di servizio di archiviazione.

## SINTASSI

```
Get-AzureStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureStorageCORSRule** ottiene le regole CORS (Cross-Origin Resource Sharing) per un tipo di servizio di archiviazione di Azure.

## ESEMPI

### Esempio 1: ottenere le regole di CORS del servizio BLOB
```
PS C:\>Get-AzureStorageCORSRule -ServiceType Blob
```

Questo comando ottiene le regole CORS per il tipo di servizio BLOB.

## PARAMETRI

### -ClientTimeoutPerRequest
Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.
Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.
Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.

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

### -ConcurrentTaskCount
Specifica le chiamate di rete simultanee massime.
Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.
Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.
Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.
Il valore predefinito è 10.

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

### -Contesto
Specifica un contesto di archiviazione di Azure.
Per ottenere un contesto, usare il cmdlet New-AzureStorageContext.

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

### -ServerTimeoutPerRequest
Specifica la lunghezza del periodo di timeout per la parte server di una richiesta.

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
Specifica il tipo di servizio di archiviazione di Azure per cui questo cmdlet ottiene le regole di CORS.
I valori accettabili per questo parametro sono i seguenti:

- BLOB 
- tavolo 
- Coda 
- File

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

###  
Questo cmdlet restituisce una matrice di oggetti **PSCORSRule** che rappresentano le regole CORS attualmente in un servizio.

## Note

## COLLEGAMENTI CORRELATI

[Remove-AzureStorageCORSRule](./Remove-AzureStorageCORSRule.md)

[Set-AzureStorageCORSRule](./Set-AzureStorageCORSRule.md)


