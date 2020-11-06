---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: CBD157D2-37C5-491F-A806-6B39F1D0415A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3191d7369597fbfb0781b550a57f0032f9aaad4f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93507084"
---
# Get-AzureStorageBlobCopyState

## Sinossi
Ottiene lo stato di copia di un BLOB di archiviazione di Azure.

## SINTASSI

### NamePipeline (impostazione predefinita)
```
Get-AzureStorageBlobCopyState [-Blob] <String> [-Container] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### BlobPipeline
```
Get-AzureStorageBlobCopyState -CloudBlob <CloudBlob> [-WaitForComplete] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### ContainerPipeline
```
Get-AzureStorageBlobCopyState -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureStorageBlobCopyState** ottiene lo stato di copia di un BLOB di archiviazione di Azure.

## ESEMPI

### Esempio 1: ottenere lo stato di copia di un BLOB
```
C:\PS>Get-AzureStorageBlobCopyState -Blob "ContosoPlanning2015" -Container "ContosoUploads"
```

Questo comando ottiene lo stato di copia del BLOB denominato ContosoPlanning2015 nel contenitore ContosoUploads.

### Esempio 2: ottenere lo stato di copia di un BLOB usando la pipeline
```
C:\PS>Get-AzureStorageBlob -Blob "ContosoPlanning2015" -Container "ContosoUploads" | Get-AzureStorageBlobCopyState
```

Questo comando ottiene il BLOB denominato ContosoPlanning2015 nel contenitore denominato ContosoUploads usando il cmdlet **Get-AzureStorageBlob** e quindi passa il risultato al cmdlet corrente usando l'operatore pipeline.
Il cmdlet **Get-AzureStorageBlobCopyState** ottiene lo stato di copia per il BLOB.

### Esempio 3: ottenere lo stato di copia di un BLOB in un contenitore usando la pipeline
```
C:\PS>Get-AzureStorageContainer -Name "ContosoUploads" | Get-AzureStorageBlobCopyState -Blob "ContosoPlanning2015"
```

Questo comando ottiene il contenitore denominato usando il cmdlet **Get-AzureStorageBlob** e quindi passa il risultato al cmdlet corrente.
Il cmdlet **Get-AzureStorageContainer** ottiene lo stato di copia per il BLOB denominato ContosoPlanning2015 in tale contenitore.

## PARAMETRI

### -BLOB
Specifica il nome di un BLOB.
Questo cmdlet ottiene lo stato dell'operazione di copia BLOB per il BLOB di archiviazione di Azure specificato da questo parametro.

```yaml
Type: String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
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

### -CloudBlob
Specifica un oggetto **CloudBlob** dalla libreria client di archiviazione di Azure.
Per ottenere un oggetto **CloudBlob** , usa il cmdlet Get-AzureStorageBlob.

```yaml
Type: CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CloudBlobContainer
Specifica un oggetto **CloudBlobContainer** dalla raccolta client di archiviazione di Azure.
Questo cmdlet ottiene lo stato di copia di un BLOB nel contenitore specificato da questo parametro.
Per ottenere un oggetto **CloudBlobContainer** , usa il cmdlet Get-AzureStorageContainer.

```yaml
Type: CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Specifica il nome di un contenitore.
Questo cmdlet ottiene lo stato di copia di un BLOB nel contenitore specificato da questo parametro.

```yaml
Type: String
Parameter Sets: NamePipeline
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -WaitForComplete
Indica che questo cmdlet attende che la copia finisca.
Se non specifichi questo parametro, questo cmdlet restituisce immediatamente un risultato.

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

## OUTPUT

### CopyState

## Note

## COLLEGAMENTI CORRELATI

[Start-AzureStorageBlobCopy](./Start-AzureStorageBlobCopy.md)

[Stop-AzureStorageBlobCopy](./Stop-AzureStorageBlobCopy.md)


