---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7B29875-D2E5-4E96-AD4B-83032AB18D02
online version: ''
schema: 2.0.0
ms.openlocfilehash: cdcd4788e3eefdce858cb88c0bf1885353f8a673
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023928"
---
# New-AzureSqlDatabaseServerContext

## Sinossi
Crea un contesto di connessione al server.

## SINTASSI

### ByServerNameWithSqlAuth (impostazione predefinita)
```
New-AzureSqlDatabaseServerContext -ServerName <String> -Credential <PSCredential> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ByManageUrlWithSqlAuth
```
New-AzureSqlDatabaseServerContext [-ServerName <String>] -ManageUrl <Uri> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByServerNameWithCertAuth
```
New-AzureSqlDatabaseServerContext -ServerName <String> [-UseSubscription] [-SubscriptionName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByFullyQualifiedServerNameWithSqlAuth
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByFullyQualifiedServerNameWithCertAuth
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> [-UseSubscription]
 [-SubscriptionName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzureSqlDatabaseServerContext** crea un contesto di connessione del server di database SQL di Azure.
Usare l'autenticazione di SQL Server per creare un contesto di connessione a un server di database SQL utilizzando le credenziali specificate.
È possibile specificare il server di database SQL per nome, per nome completo o per URL.
Per ottenere una credenziale, usare il cmdlet Get-Credential che chiede di specificare il nome utente e la password.

Usa il cmdlet **New-AzureSqlDatabaseServerContext** con l'autenticazione basata su certificati per creare un contesto di connessione al server di database SQL specificato usando i dati di abbonamento di Azure specificati.
È possibile specificare il server di database SQL per nome o per il nome completo.
Puoi specificare i dati dell'abbonamento come parametro oppure può essere recuperato dall'abbonamento Azure corrente.
Usare il cmdlet Select-AzureSubscription https://msdn.microsoft.com/library/windowsazure/jj152833.aspx per selezionare l'abbonamento Azure corrente.

## ESEMPI

### Esempio 1: creare un contesto usando l'autenticazione di SQL Server
```
PS C:\> $Credential = Get-Credential
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -Credential $Credential
PS C:\> $Database17 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database17" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

Questo esempio usa l'autenticazione di SQL Server.

Il primo comando richiede le credenziali di amministratore del server e archivia le credenziali nella variabile $Credential.

Il secondo comando si connette al server di database SQL denominato lpqd0zbr8y tramite $Credential.

Il comando finale crea un database denominato Database17 nel server che fa parte del contesto in $Context.

### Esempio 2: creare un contesto usando l'autenticazione basata su certificati
```
PS C:\> $SubscriptionId = <Subscription ID>
PS C:\> $Thumbprint = <Certificate Thumbprint>
PS C:\> $Certificate = Get-Item "Cert:\CurrentUser\My\$Thumbprint"
PS C:\> Set-AzureSubscription -SubscriptionName "Subscription07" -SubscriptionId $SubscriptionId -Certificate $Certificate
PS C:\> Select-AzureSubscription -SubscriptionName "Subscription07"
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -UseSubscription
```

Questo esempio usa l'autenticazione basata su certificati.

I primi due comandi assegnano valori alle variabili $SubscriptionId e $Thumbprint.

Il terzo comando ottiene il certificato identificato dall'identificazione personale in $Thumbprint e lo archivia in $Certificate.

Il quarto comando imposta la sottoscrizione come Subscription07 e il quinto comando Seleziona l'abbonamento.

Il comando finale crea un contesto nell'abbonamento corrente per il server denominato lpqd0zbr8y.

## PARAMETRI

### -Credenziale
Specifica un oggetto Credential che fornisce l'autenticazione di SQL Server per l'accesso al server.

```yaml
Type: PSCredential
Parameter Sets: ByServerNameWithSqlAuth, ByManageUrlWithSqlAuth, ByFullyQualifiedServerNameWithSqlAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FullyQualifiedServerName
Specifica il nome di dominio completo (FQDN) per il server di database SQL di Azure.
Ad esempio, Server02.database.windows.net.

```yaml
Type: String
Parameter Sets: ByFullyQualifiedServerNameWithSqlAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManageUrl
Specifica l'URL usato da questo cmdlet per accedere al portale di Azure SQL DatabaseManagement per il server.

```yaml
Type: Uri
Parameter Sets: ByManageUrlWithSqlAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Specifica il profilo Azure da cui viene letto il cmdlet.
Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nomeserver
Specifica il nome del server di database.

```yaml
Type: String
Parameter Sets: ByServerNameWithSqlAuth, ByServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByManageUrlWithSqlAuth
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Subscriptionname
Specifica il nome dell'abbonamento Azure usato da questo cmdlet per creare il contesto di connessione.
Se non specifichi un valore per questo parametro, il cmdlet usa l'abbonamento corrente.
Eseguire il cmdlet Select-AzureSubscription per cambiare l'abbonamento corrente.

```yaml
Type: String
Parameter Sets: ByServerNameWithCertAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UseSubscription
Indica che questo cmdlet usa l'abbonamento Azure per creare il contesto di connessione.

```yaml
Type: SwitchParameter
Parameter Sets: ByServerNameWithCertAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

### Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. IServerDataServiceContext

## Note
* Se si effettua l'autenticazione senza specificare un dominio e se si usa Windows PowerShell 2,0, il cmdlet Get-Credential restituisce una barra rovesciata ( \\ ) anteposto al nome utente, ad esempio \User. Windows PowerShell 3,0 non aggiunge la barra rovesciata. Questa barra rovesciata non viene riconosciuta dal parametro *Credential* del cmdlet **New-AzureSqlDatabaseServerContext** . Per rimuoverlo, usare comandi simili ai seguenti:

  `PS C:\\\> $Credential = Get-Credential`
`PS C:\\\> $Credential = New-Object -TypeName 'System.Management.Automation.PSCredential' -ArgumentList $Credential.Username.Replace("\",""),$Credential.Password`

## COLLEGAMENTI CORRELATI

[Cmdlet di database SQL di Azure](./Azure.SQLDatabase.md)

[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)

[New-AzureSqlDatabase](./New-AzureSqlDatabase.md)

[Remove-AzureSqlDatabase](./Remove-AzureSqlDatabase.md)

[Set-AzureSqlDatabase](./Set-AzureSqlDatabase.md)


