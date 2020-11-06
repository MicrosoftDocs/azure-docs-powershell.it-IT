---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E54BFD3A-CD54-4E6B-9574-92B8D3E88FF3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlob.md
gitcommit: https://github.com/Azure/azure-powershell/blob/f8503a90f782f51c8baa0360f98adb33f2a6f26f
ms.openlocfilehash: e05dc3ed962e7d1d4610663dd129c0977b784280
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517276"
---
# Get-AzureStorageBlob

## Sinossi
Elenca i BLOB in un contenitore.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### Blobname (impostazione predefinita)
```
Get-AzureStorageBlob [[-Blob] <String>] [-Container] <String> [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### BlobPrefix
```
Get-AzureStorageBlob [-Prefix <String>] [-Container] <String> [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureStorageBlob** elenca i BLOB nel contenitore specificato in un account di archiviazione di Azure.

## ESEMPI

### Esempio 1: ottenere un BLOB per nome BLOB
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Blob blob*
```

Questo comando usa un nome BLOB e un carattere jolly per ottenere un BLOB.

### Esempio 2: ottenere un BLOB usando la pipeline
```
PS C:\>Get-AzureStorageContainer -Name container* | Get-AzureStorageBlob
```

Questo comando usa la pipeline per ottenere un BLOB.

### Esempio 3: ottenere un prefisso BLOB per nome
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Prefix "blob"
```

Questo comando usa un prefisso di nome per ottenere un BLOB.

### Esempio 4: elencare i BLOB in più batch
```
PS C:\>$MaxReturn = 10000
PS C:\> $ContainerName = "abc"
PS C:\> $Total = 0
PS C:\> $Token = $Null
PS C:\> do
 {
     $Blobs = Get-AzureStorageBlob -Container $ContainerName -MaxCount $MaxReturn  -ContinuationToken $Token
     $Total += $Blobs.Count
     if($Blobs.Length -le 0) { Break;}
     $Token = $Blobs[$blobs.Count -1].ContinuationToken;
 }
 While ($Token -ne $Null)
PS C:\> Echo "Total $Total blobs in container $ContainerName"
```

Questo esempio usa i parametri *maxCount* e *ContinuationToken* per elencare i BLOB di archiviazione di Azure in più batch.
I primi quattro comandi assegnano valori alle variabili da usare nell'esempio.

Il quinto comando specifica un'istruzione **do-while** che usa il cmdlet **Get-AzureStorageBlob** per ottenere i BLOB.
L'istruzione include il token di continuazione archiviato nella variabile $Token.
$Token cambia il valore durante l'esecuzione del ciclo.
Per altre informazioni, digitare `Get-Help About_Do` .

Il comando finale usa il comando **echo** per visualizzare il totale.

## PARAMETRI

### -BLOB
Specifica un nome o un modello di nome, che può essere usato per una ricerca con caratteri jolly.
Se non viene specificato alcun nome BLOB, il cmdlet elenca tutti i BLOB nel contenitore specificato.
Se viene specificato un valore per questo parametro, il cmdlet elenca tutti i BLOB con i nomi che corrispondono a questo parametro.

```yaml
Type: String
Parameter Sets: BlobName
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

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

### -Contenitore
Specifica il nome del contenitore.

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Contesto
Specifica l'account di archiviazione di Azure da cui si vuole ottenere un elenco di BLOB.
Puoi usare il cmdlet New-AzureStorageContext per creare un contesto di archiviazione.

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

### -ContinuationToken
Specifica un token di continuazione per l'elenco di BLOB.
Usa questo parametro e il parametro *maxCount* per elencare i BLOB in più batch.

```yaml
Type: BlobContinuationToken
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxCount
Specifica il numero massimo di oggetti restituiti da questo cmdlet.

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

### -Prefisso
Specifica un prefisso per i nomi di BLOB che si desidera ottenere.
Questo parametro non supporta l'uso di espressioni regolari o caratteri jolly per la ricerca.
Questo significa che se il contenitore contiene solo oggetti BLOB denominati "My", "MyBlob1" e "MyBlob2" e specifichi "-prefix My *", il cmdlet non restituisce alcun BLOB.
Se invece specifichi "-prefix My", il cmdlet restituirà "My", "MyBlob1" e "MyBlob2".

```yaml
Type: String
Parameter Sets: BlobPrefix
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Specifica l'intervallo di timeout lato servizio, in secondi, per una richiesta.
Se l'intervallo specificato trascorre prima che il servizio elabora la richiesta, il servizio di archiviazione restituisce un errore.

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

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### IStorageContext

Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline

## OUTPUT

### AzureStorageBlob

## Note


## COLLEGAMENTI CORRELATI

[Get-AzureStorageBlobContent](./Get-AzureStorageBlobContent.md)

[Remove-AzureStorageBlob](./Remove-AzureStorageBlob.md)

[Set-AzureStorageBlobContent](./Set-AzureStorageBlobContent.md)


