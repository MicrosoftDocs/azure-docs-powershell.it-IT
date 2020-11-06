---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 2B12BC19-EF8F-43F5-AF04-C570FEEA1AE6
online version: ''
schema: 2.0.0
ms.openlocfilehash: d80a8a75082503cf8cde9df7a779ca7f0d7d4b92
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93507024"
---
# New-AzureStorageContainer

## Sinossi
Crea un contenitore di archiviazione di Azure.

## SINTASSI

```
New-AzureStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzureStorageContainer** crea un contenitore di archiviazione di Azure.

## ESEMPI

### Esempio 1: creare un contenitore di archiviazione di Azure
```
PS C:\>New-AzureStorageContainer -Name "ContainerName" -Permission Off
```

Questo comando crea un contenitore di archiviazione.

### Esempio 2: creare più contenitori di archiviazione di Azure
```
PS C:\>"container1 container2 container3".split() | New-AzureStorageContainer -Permission Container
```

Questo esempio crea più contenitori di archiviazione.
Usa il metodo **Split** della classe **String** .NET e quindi passa i nomi sulla pipeline.

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
Specifica un contesto per il nuovo contenitore.

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

### -Nome
Specifica un nome per il nuovo contenitore.

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Autorizzazione
Specifica il livello di accesso pubblico al contenitore.
Per impostazione predefinita, è possibile accedere al contenitore e a qualsiasi BLOB in esso solo dal proprietario dell'account di archiviazione.
Per concedere agli utenti anonimi le autorizzazioni di lettura per un contenitore e i relativi BLOB, è possibile impostare le autorizzazioni del contenitore per consentire l'accesso pubblico.
Gli utenti anonimi possono leggere i BLOB in un contenitore disponibile pubblicamente senza autenticazione della richiesta.
I valori accettabili per questo parametro sono i seguenti:

- Contenitore.
Fornisce l'accesso in lettura completo a un contenitore e ai relativi BLOB.
I client possono enumerare i BLOB nel contenitore tramite una richiesta anonima, ma non possono enumerare i contenitori nell'account di archiviazione. 
- BLOB.
Fornisce l'accesso in lettura ai dati BLOB in un contenitore tramite una richiesta anonima, ma non consente l'accesso ai dati del contenitore.
I client non possono enumerare i BLOB nel contenitore usando la richiesta anonima. 
- Disattivare.
Che limita l'accesso solo al proprietario dell'account di archiviazione.

```yaml
Type: BlobContainerPublicAccessType
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob

Required: False
Position: 1
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

## OUTPUT

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureStorageContainer](./Get-AzureStorageContainer.md)

[Remove-AzureStorageContainer](./Remove-AzureStorageContainer.md)

[Set-AzureStorageContainerAcl](./Set-AzureStorageContainerAcl.md)


