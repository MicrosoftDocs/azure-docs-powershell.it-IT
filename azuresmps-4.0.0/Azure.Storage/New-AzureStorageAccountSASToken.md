---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c888c5e7a4083fd91fdddfd6d2442cb65056d42
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93507028"
---
# New-AzureStorageAccountSASToken

## Sinossi
Crea un token SAS.

## SINTASSI

```
New-AzureStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzureStorageSASToken** crea un token SAS (Shared Access Signature) a livello di account per un account di archiviazione di Azure.

Puoi usare il token SAS per delegare le autorizzazioni per più servizi o per delegare le autorizzazioni per i servizi non disponibili con un token SAS a livello di oggetto.

## ESEMPI

### Esempio 1: creare un token SAS
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

Questo comando crea un token SAS a livello di account con l'autorizzazione completa.

### Esempio 2: creare un token SAS per un intervallo di indirizzi IP
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

Questo comando crea un token SAS per le richieste solo HTTPS dall'intervallo di indirizzi IP specificato.

## PARAMETRI

### -Contesto
Specifica il contesto di archiviazione di Azure.
Puoi usare il cmdlet New-AzureStorageContext per ottenere un oggetto **AzureStorageContext** .

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

### -ExpiryTime
Specifica il momento in cui la firma di accesso condiviso diventa non valida.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IPAddressOrRange
Specifica l'indirizzo IP o l'intervallo di indirizzi IP da cui accettare le richieste, ad esempio 168.1.5.65 o 168.1.5.60-168.1.5.70.
L'intervallo è incluso.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Autorizzazione
Specifica le autorizzazioni per l'account di archiviazione.
Le autorizzazioni sono valide solo se corrispondono al tipo di risorsa specificato.
Per altre informazioni sui valori di autorizzazione accettabili, vedere Creazione di un account SAShttps://go.microsoft.com/fwlink/?LinkId=799514

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocollo
Specifica il protocollo consentito per una richiesta effettuata con l'account SAS.
I valori accettabili per questo parametro sono i seguenti:

- HttpsOnly
- HttpsOrHttp

Il valore predefinito è HttpsOrHttp.

```yaml
Type: SharedAccessProtocol
Parameter Sets: (All)
Aliases: 
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceType
Specifica i tipi di risorsa disponibili con il token SAS.
I valori accettabili per questo parametro sono i seguenti:

- Nessuno
- Servizio
- Contenitore
- Oggetto

```yaml
Type: SharedAccessAccountResourceTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Servizio
Specifica il servizio.
I valori accettabili per questo parametro sono i seguenti:

- Nessuno
- BLOB
- File
- Coda
- tavolo

```yaml
Type: SharedAccessAccountServices
Parameter Sets: (All)
Aliases: 
Accepted values: None, Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartTime
Specifica il tempo, come oggetto **DateTime** , in corrispondenza del quale il SAS diventa valido.
Per ottenere un oggetto **DateTime** , usa il cmdlet Get-Date.

```yaml
Type: DateTime
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

[New-AzureStorageBlobSASToken](./New-AzureStorageBlobSASToken.md)

[New-AzureStorageContainerSASToken](./New-AzureStorageContainerSASToken.md)

[New-AzureStorageFileSASToken](./New-AzureStorageFileSASToken.md)

[New-AzureStorageQueueSASToken](./New-AzureStorageQueueSASToken.md)

[New-AzureStorageShareSASToken](./New-AzureStorageShareSASToken.md)

[New-AzureStorageTableSASToken](./New-AzureStorageTableSASToken.md)


