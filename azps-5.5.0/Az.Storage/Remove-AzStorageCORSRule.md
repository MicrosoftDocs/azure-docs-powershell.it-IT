---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 26E06BA3-C550-40A5-B8E3-FEC8E9BF3867
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageCORSRule.md
ms.openlocfilehash: aeae25ab3a8ff0b1fa3eb91db90497b44555631f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197519"
---
# Remove-AzStorageCORSRule

## SYNOPSIS
Rimuove cors per un servizio di archiviazione.

## SINTASSI

```
Remove-AzStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Remove-AzStorageCORSRule** rimuove la condivisione di risorse tra origini (CORS) per un servizio di archiviazione di Azure.
Questo cmdlet elimina tutte le regole CORS in un tipo di servizio di archiviazione.
I tipi di servizi di archiviazione per questo cmdlet sono BLOB, tabella, coda e file.

## ESEMPI

### Esempio 1: Rimuovere le regole CORS per il servizio BLOB
```
PS C:\>Remove-AzStorageCORSRule -ServiceType Blob
```

Questo comando rimuove le regole CORS per il tipo di servizio BLOB.

## PARAMETERS

### -ClientTimeoutPerRequest
Specifica l'intervallo di timeout sul lato client, in secondi, per una richiesta di servizio.
Se la chiamata precedente non riesce nell'intervallo specificato, il cmdlet riprova la richiesta.
Se questo cmdlet non riceve una risposta corretta prima che sia trascorso l'intervallo, il cmdlet restituisce un errore.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConcurrentTaskCount
Specifica il numero massimo di chiamate di rete simultanee.
È possibile usare questo parametro per limitare la simultaneità alla limitazione dell'utilizzo di CPU e larghezza di banda locale specificando il numero massimo di chiamate di rete simultanee.
Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero principale.
Questo parametro consente di ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.
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

### -Context
Specifica il contesto di archiviazione di Azure.
Per ottenere il contesto di archiviazione, il cmdlet New-AzStorageContext archiviazione.

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
Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Specifica la durata del periodo di timeout per la parte server di una richiesta.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceType
Specifica il tipo di servizio di archiviazione di Azure per cui questo cmdlet rimuove le regole.
I valori accettabili per questo parametro sono:
- BLOB 
- tavolo 
- Coda 
- File

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
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
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## OUTPUT

### System.Void

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AzStorageCORSRule](./Get-AzStorageCORSRule.md)

[Set-AzStorageCORSRule](./Set-AzStorageCORSRule.md)


