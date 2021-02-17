---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
ms.openlocfilehash: ae12bb509773f36ecfd94ad6907499f0b5feb02d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207795"
---
# New-AzStorageContext

## SYNOPSIS
Crea un contesto di Archiviazione di Azure.

## SINTASSI

### OAuthAccount (impostazione predefinita)
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### AccountNameAndKey
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### AccountNameAndKeyEnvironment
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### AnonymousAccount
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### AnonymousAccountEnvironment
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### SasToken
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### SasTokenWithAzureEnvironment
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### OAuthAccountEnvironment
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### ConnectionString
```
New-AzStorageContext -ConnectionString <String> [<CommonParameters>]
```

### LocalDevelopment
```
New-AzStorageContext [-Local] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **New-AzStorageContext** crea un contesto di Archiviazione di Azure.
L'autenticazione predefinita di un contesto di archiviazione è OAuth (Azure AD), se solo il nome dell'account di archiviazione di input.
Vedere i dettagli dell'autenticazione del servizio di archiviazione in https://docs.microsoft.com/en-us/rest/api/storageservices/authorization-for-the-azure-storage-services .

## ESEMPI

### Esempio 1: Creare un contesto specificando il nome di un account di archiviazione e una chiave
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

Questo comando crea un contesto per l'account contosoGeneral che usa la chiave specificata.

### Esempio 2: Creare un contesto specificando una stringa di connessione
```
PS C:\>New-AzStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

Questo comando crea un contesto in base alla stringa di connessione specificata per l'account ContosoGeneral.

### Esempio 3: Creare un contesto per un account di archiviazione anonimo
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

Questo comando crea un contesto per l'uso anonimo per l'account contosoGeneral.
Il comando specifica HTTP come protocollo di connessione.

### Esempio 4: Creare un contesto usando l'account di archiviazione di sviluppo locale
```
PS C:\>New-AzStorageContext -Local
```

Questo comando crea un contesto usando l'account di archiviazione di sviluppo locale.
Il comando specifica il *parametro* Local.

### Esempio 5: Ottenere il contenitore per l'account di archiviazione per sviluppatori locale
```
PS C:\>New-AzStorageContext -Local | Get-AzStorageContainer
```

Questo comando crea un contesto usando l'account di archiviazione di sviluppo locale e quindi passa il nuovo contesto al cmdlet **Get-AzStorageContainer** usando l'operatore della pipeline.
Il comando ottiene il contenitore Archiviazione di Azure per l'account di archiviazione per sviluppatori locale.

### Esempio 6: Ottenere più contenitori
```
PS C:\>$Context01 = New-AzStorageContext -Local 
PS C:\> $Context02 = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzStorageContainer
```

Il primo comando crea un contesto usando l'account di archiviazione di sviluppo locale e quindi lo archivia nella variabile $Context 01.
Il secondo comando crea un contesto per l'account contosoGeneral che usa la chiave specificata e quindi lo archivia nella variabile $Context 02.
Il comando finale recupera i contenitori per i contesti archiviati in $Context 01 e $Context 02 usando **Get-AzStorageContainer.**

### Esempio 7: Creare un contesto con un endpoint
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

Questo comando crea un contesto di Archiviazione di Azure con l'endpoint di archiviazione specificato.
Il comando crea il contesto per l'account denominato ContosoGeneral che usa la chiave specificata.

### Esempio 8: Creare un contesto con un ambiente specificato
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

Questo comando crea un contesto di archiviazione di Azure con l'ambiente Azure specificato.
Il comando crea il contesto per l'account denominato ContosoGeneral che usa la chiave specificata.

### Esempio 9: Creare un contesto usando un token di firma di accesso condiviso
```
PS C:\>$SasToken = New-AzStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzStorageBlob -Container "ContosoMain"
```

Il primo comando genera un token di firma di accesso condiviso usando il cmdlet **New-AzStorageContainerSASToken** per il contenitore denominato ContosoMain, quindi archivia il token nella variabile $SasToken.
Questo token è per le autorizzazioni di lettura, aggiunta, aggiornamento ed eliminazione.
Il secondo comando crea un contesto per l'account contosoGeneral che usa il token di firma di accesso condiviso archiviato in $SasToken e quindi lo archivia nella variabile $Context variabile.
Il comando finale elenca tutti i BLOB associati al contenitore denominato ContosoMain usando il contesto archiviato in $Context.

### Esempio 10: Creare un contesto usando l'autenticazione OAuth
```
PS C:\>Connect-AzAccount
PS C:\> $Context = New-AzStorageContext -StorageAccountName "myaccountname" -UseConnectedAccount
```

Questo comando crea un contesto usando l'autenticazione OAuth (Azure AD).

## PARAMETERS

### -Anonimo
Indica che questo cmdlet crea un contesto di Archiviazione di Azure per l'accesso anonimo.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AnonymousAccount, AnonymousAccountEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConnectionString
Specifica una stringa di connessione per il contesto di Archiviazione di Azure.

```yaml
Type: System.String
Parameter Sets: ConnectionString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Endpoint
Specifica l'endpoint per il contesto di Archiviazione di Azure.

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AnonymousAccount, SasToken
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Environment
Specifica l'ambiente di Azure.
I valori accettabili per questo parametro sono: AzureCloud e AzureChinaCloud.
Per altre informazioni, digitare `Get-Help Get-AzEnvironment` .

```yaml
Type: System.String
Parameter Sets: AccountNameAndKeyEnvironment, AnonymousAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SasTokenWithAzureEnvironment, OAuthAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Local
Indica che questo cmdlet crea un contesto usando l'account di archiviazione di sviluppo locale.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LocalDevelopment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocol
Transfer Protocol (https/http).

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, OAuthAccountEnvironment
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SasToken
Specifica un token di firma di accesso condiviso per il contesto.

```yaml
Type: System.String
Parameter Sets: SasToken, SasTokenWithAzureEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountKey
Specifica una chiave di account di archiviazione di Azure.
Questo cmdlet crea un contesto per la chiave specificata da questo parametro.

```yaml
Type: System.String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountName
Specifica il nome di un account di archiviazione di Azure.
Questo cmdlet crea un contesto per l'account specificato da questo parametro.

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, SasTokenWithAzureEnvironment, OAuthAccountEnvironment
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseConnectedAccount
Indica che questo cmdlet crea un contesto di Archiviazione di Azure con l'autenticazione OAuth (Azure AD).
Il cmdlet userà l'autenticazione OAuth per impostazione predefinita, quando non sono specificate altre opzioni di autenticazione.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OAuthAccount, OAuthAccountEnvironment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### System.String

## OUTPUT

### Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AzStorageBlob](./Get-AzStorageBlob.md)

[New-azStorageContainersASToken](./New-AzStorageContainerSASToken.md)


