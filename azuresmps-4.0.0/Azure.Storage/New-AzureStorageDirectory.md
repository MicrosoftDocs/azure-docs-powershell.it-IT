---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 65962F9A-CC79-4B8B-9208-A993708FD36F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1bd97057cfafc48b3f1edd8539e7808056599117
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491446"
---
# New-AzureStorageDirectory

## Sinossi
Crea una directory.

## SINTASSI

### ShareName (impostazione predefinita)
```
New-AzureStorageDirectory [-ShareName] <String> [-Path] <String> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### Condividi
```
New-AzureStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### Directory
```
New-AzureStorageDirectory [-Directory] <CloudFileDirectory> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzureStorageDirectory** crea una directory.
Questo cmdlet restituisce un oggetto **CloudFileDirectory** .

## ESEMPI

### Esempio 1: creare una cartella in una condivisione file
```
PS C:\>New-AzureStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

Questo comando crea una cartella denominata ContosoWorkingFolder nella condivisione file denominata ContosoShare06.

### Esempio 2: creare una cartella in una condivisione file specificata in un oggetto condivisione file
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" | New-AzureStorageDirectory -Path "ContosoWorkingFolder"
```

Questo comando usa il cmdlet **Get-AzureStorageShare** per ottenere la condivisione di file denominata ContosoShare06 e quindi la passa al cmdlet corrente usando l'operatore pipeline.
Il cmdlet corrente crea la cartella denominata ContosoWorkingFolder in ContosoShare06.

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
Per ottenere un contesto di archiviazione, usare il cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .

```yaml
Type: IStorageContext
Parameter Sets: ShareName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Directory
Specifica una cartella come oggetto **CloudFileDirectory** .
Questo cmdlet crea la cartella nella posizione specificata da questo parametro.
Per ottenere una directory, usare il cmdlet New-AzureStorageDirectory.
Puoi anche usare il cmdlet Get-AzureStorageFile per ottenere una directory.

```yaml
Type: CloudFileDirectory
Parameter Sets: Directory
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Path
Specifica il percorso di una cartella.
Questo cmdlet crea una cartella per il percorso specificato da questo cmdlet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
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

### -Condividi
Specifica un oggetto **CloudFileShare** .
Questo cmdlet crea una cartella nella condivisione file specificata da questo parametro.
Per ottenere un oggetto **CloudFileShare** , usa il cmdlet Get-AzureStorageShare.
Questo oggetto contiene il contesto di archiviazione.
Se specifichi questo parametro, non specificare il parametro *context* .

```yaml
Type: CloudFileShare
Parameter Sets: Share
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ShareName
Specifica il nome della condivisione file.
Questo cmdlet crea una cartella nella condivisione file specificata da questo parametro.

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

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

[Get-AzureStorageFile](./Get-AzureStorageFile.md)

[Get-AzureStorageShare](./Get-AzureStorageShare.md)

[New-AzureStorageContext](./New-AzureStorageContext.md)

[New-AzureStorageDirectory](./New-AzureStorageDirectory.md)

[Remove-AzureStorageDirectory](./Remove-AzureStorageDirectory.md)
