---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: FD3A0013-4365-4E65-891C-5C50A9D5658C
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageShare.md
ms.openlocfilehash: 31a8d6cbb205b451233bdc72793fb45443350fdd
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "93688675"
---
# Get-AzureStorageShare

## Sinossi
Ottiene un elenco di condivisioni file.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### MatchingPrefix (impostazione predefinita)
```
Get-AzureStorageShare [[-Prefix] <String>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### Specifico
```
Get-AzureStorageShare [-Name] <String> [[-SnapshotTime] <DateTimeOffset>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureStorageShare** ottiene un elenco di condivisioni di file per un account di archiviazione.

## ESEMPI

### Esempio 1: ottenere una condivisione file
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06"
```

Questo comando consente di ottenere la condivisione di file denominata ContosoShare06.

### Esempio 2: ottenere tutte le condivisioni di file che iniziano con una stringa
```
PS C:\>Get-AzureStorageShare -Prefix "Contoso"
```

Questo comando consente di ottenere tutte le condivisioni file con nomi che iniziano con contoso.

### Esempio 3: ottenere tutte le condivisioni di file in un contesto specificato
```
PS C:\>$Context = New-AzureStorageContext -Local
PS C:\> Get-AzureStorageShare -Context $Context
```

Il primo comando usa il cmdlet **New-AzureStorageContext** per creare un contesto usando il parametro *local* e quindi archivia tale oggetto Context nella variabile $context.
Il secondo comando consente di ottenere le condivisioni file per l'oggetto context archiviato in $Context.

### Esempio 4: ottenere uno snapshot della condivisione file con un nome di condivisione specifico e SnapshotTime
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" -SnapshotTime "6/16/2017 9:48:41 AM +00:00"
```

Questo comando ottiene uno snapshot della condivisione file con un nome di condivisione specifico e SnapshotTime.

## PARAMETRI

### -ClientTimeoutPerRequest
Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.
Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.
Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.

```yaml
Type: System.Nullable`1[System.Int32]
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
Type: System.Nullable`1[System.Int32]
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
Per ottenere un contesto, usa il cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Specifica il nome della condivisione file.
Questo cmdlet ottiene la condivisione di file specificata da questo parametro oppure Nothing se si specifica il nome di una condivisione file che non esiste.

```yaml
Type: System.String
Parameter Sets: Specific
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Prefisso
Specifica il prefisso per le condivisioni file.
Questo cmdlet ottiene le condivisioni di file che corrispondono al prefisso specificato da questo parametro oppure non condivide file se nessuna delle condivisioni file corrisponde al prefisso indicato.

```yaml
Type: System.String
Parameter Sets: MatchingPrefix
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Specifica la lunghezza del periodo di timeout per la parte server di una richiesta.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SnapshotTime
SnapshotTime dello snapshot della condivisione file da ricevere.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: Specific
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext

## OUTPUT

### Microsoft. WindowsAzure. storage. file. CloudFileShare

## Note

## COLLEGAMENTI CORRELATI

[New-AzureStorageShare](./New-AzureStorageShare.md)

[Remove-AzureStorageShare](./Remove-AzureStorageShare.md)
