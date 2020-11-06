---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4db0b752e8bf887e899a4de6a8e4175eaa2d9855
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491445"
---
# New-AzureStorageContext

## Sinossi
Crea un contesto di archiviazione di Azure.

## SINTASSI

### AccountNameAndKey (impostazione predefinita)
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### AccountNameAndKeyEnvironment
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### AnonymousAccount
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### AnonymousAccountEnvironment
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### SasToken
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### SasTokenWithAzureEnvironment
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### ConnectionString
```
New-AzureStorageContext -ConnectionString <String> [<CommonParameters>]
```

### LocalDevelopment
```
New-AzureStorageContext [-Local] [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzureStorageContext** crea un contesto di archiviazione di Azure.

## ESEMPI

### Esempio 1: creare un contesto specificando un nome e una chiave dell'account di archiviazione
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

Questo comando crea un contesto per l'account denominato ContosoGeneral che usa la chiave specificata.

### Esempio 2: creare un contesto specificando una stringa di connessione
```
C:\PS>New-AzureStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

Questo comando crea un contesto basato sulla stringa di connessione specificata per l'account ContosoGeneral.

### Esempio 3: creare un contesto per un account di archiviazione Anonimo
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

Questo comando crea un contesto per l'uso anonimo per l'account denominato ContosoGeneral.
Il comando specifica HTTP come protocollo di connessione.

### Esempio 4: creare un contesto usando l'account di archiviazione dello sviluppo locale
```
C:\PS>New-AzureStorageContext -Local
```

Questo comando crea un contesto usando l'account di archiviazione dello sviluppo locale.
Il comando specifica il parametro *local* .

### Esempio 5: ottenere il contenitore per l'account di archiviazione dello sviluppatore locale
```
C:\PS>New-AzureStorageContext -Local | Get-AzureStorageContainer
```

Questo comando crea un contesto usando l'account di archiviazione dello sviluppo locale e quindi passa il nuovo contesto al cmdlet **Get-AzureStorageContainer** usando l'operatore pipeline.
Il comando ottiene il contenitore di archiviazione di Azure per l'account di archiviazione dello sviluppatore locale.

### Esempio 6: ottenere più contenitori
```
C:\PS>$Context01 = New-AzureStorageContext -Local 
PS C:\> $Context02 = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzureStorageContainer
```

Con il primo comando viene creato un contesto utilizzando l'account di archiviazione dello sviluppo locale e il contesto viene archiviato nella variabile $Context 01.

Il secondo comando crea un contesto per l'account denominato ContosoGeneral che usa la chiave specificata e quindi archivia tale contesto nella variabile $Context 02.

Il comando finale recupera i contenitori per i contesti archiviati in $Context 01 e $Context 02 usando **Get-AzureStorageContainer**.

### Esempio 7: creare un contesto con un endpoint
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

Questo comando crea un contesto di archiviazione di Azure con l'endpoint di archiviazione specificato.
Il comando crea il contesto per l'account denominato ContosoGeneral che usa la chiave specificata.

### Esempio 8: creare un contesto con un ambiente specificato
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

Questo comando crea un contesto di archiviazione di Azure con l'ambiente Azure specificato.
Il comando crea il contesto per l'account denominato ContosoGeneral che usa la chiave specificata.

### Esempio 9: creare un contesto usando un token SAS
```
C:\PS>$SasToken = New-AzureStorageContainerSASToken -Name "ContosoMain" -Permission "raud"
PS C:\> $Context = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzureStorageBlob -Container "ContosoMain"
```

Il primo comando genera un token SAS usando il cmdlet **New-AzureStorageContainerSASToken** per il contenitore denominato ContosoMain e quindi archivia tale token nella variabile $SasToken.
Il token è per le autorizzazioni di lettura, aggiunta, aggiornamento ed eliminazione.

Il secondo comando crea un contesto per l'account denominato ContosoGeneral che usa il token SAS archiviato in $SasToken e quindi archivia tale contesto nella variabile $Context.

Il comando finale elenca tutti i BLOB associati al contenitore denominato ContosoMain usando il contesto archiviato in $Context.

## PARAMETRI

### -Anonimo
Indica che questo cmdlet crea un contesto di archiviazione di Azure per l'accesso anonimo.

```yaml
Type: SwitchParameter
Parameter Sets: AnonymousAccount, AnonymousAccountEnvironment
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConnectionString
Specifica una stringa di connessione per il contesto di archiviazione di Azure.

```yaml
Type: String
Parameter Sets: ConnectionString
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Endpoint
Specifica l'endpoint per il contesto di archiviazione di Azure.

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AnonymousAccount, SasToken
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ambiente
Specifica l'ambiente Azure.
I valori accettabili per questo parametro sono: AzureCloud e AzureChinaCloud.
Per altre informazioni, digitare `Get-Help Get-AzureEnvironment` .

```yaml
Type: String
Parameter Sets: AccountNameAndKeyEnvironment, AnonymousAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SasTokenWithAzureEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Local
Indica che questo cmdlet crea un contesto utilizzando l'account di archiviazione dello sviluppo locale.

```yaml
Type: SwitchParameter
Parameter Sets: LocalDevelopment
Aliases: 

Required: True
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
Type: String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken
Aliases: 
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SasToken
Specifica un token SAS (Shared Access Signature) per il contesto.

```yaml
Type: String
Parameter Sets: SasToken, SasTokenWithAzureEnvironment
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountKey
Specifica una chiave dell'account di archiviazione di Azure.
Questo cmdlet crea un contesto per la chiave specificata da questo parametro.

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountName
Specifica un nome dell'account di archiviazione di Azure.
Questo cmdlet crea un contesto per l'account specificato da questo parametro.

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, SasTokenWithAzureEnvironment
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

### AzureStorageContext

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureStorageBlob](./Get-AzureStorageBlob.md)

[New-AzureStorageContainerSASToken](./New-AzureStorageContainerSASToken.md)


