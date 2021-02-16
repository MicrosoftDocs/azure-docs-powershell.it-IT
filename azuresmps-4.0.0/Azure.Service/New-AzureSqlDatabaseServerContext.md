---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7B29875-D2E5-4E96-AD4B-83032AB18D02
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5312556cb49d02ea901b4cb2526a36f7237f66d1
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100404174"
---
# New-AzureSqlDatabaseServerContext

## SYNOPSIS
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

## DESCRIZIONE
Il cmdlet **New-AzureSqlDatabaseServerContext** crea un contesto di connessione del server SQL database di Azure.
Usare SQL Server di autenticazione per creare un contesto di connessione a un server SQL database usando le credenziali specificate.
È possibile specificare il SQL server di database in base al nome, al nome completo o all'URL.
Per ottenere le credenziali, usare Get-Credential cmdlet di configurazione che richiede di specificare il nome utente e la password.

Usare il cmdlet **New-AzureSqlDatabaseServerContext** con l'autenticazione basata su certificato per creare un contesto di connessione al server di database SQL specificato usando i dati di sottoscrizione di Azure specificati.
È possibile specificare SQL server di database in base al nome o al nome completo.
È possibile specificare i dati della sottoscrizione come parametro oppure possono essere recuperati dalla sottoscrizione di Azure corrente.
Usare il cmdlet Select-AzureSubscription https://msdn.microsoft.com/library/windowsazure/jj152833.aspx per selezionare la sottoscrizione di Azure corrente.

## ESEMPI

### Esempio 1: Creare un contesto usando l'SQL Server autenticazione
```
PS C:\> $Credential = Get-Credential
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -Credential $Credential
PS C:\> $Database17 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database17" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

Questo esempio usa l'SQL Server autenticazione a più fattori.

Il primo comando richiede le credenziali di amministratore del server e le archivia nella variabile $Credential locale.

Il secondo comando si connette al server SQL database denominato lpqd0zbr8y usando $Credential.

Il comando finale crea un database denominato Database17 nel server che fa parte del contesto in $Context.

### Esempio 2: Creare un contesto usando l'autenticazione basata su certificato
```
PS C:\> $SubscriptionId = <Subscription ID>
PS C:\> $Thumbprint = <Certificate Thumbprint>
PS C:\> $Certificate = Get-Item "Cert:\CurrentUser\My\$Thumbprint"
PS C:\> Set-AzureSubscription -SubscriptionName "Subscription07" -SubscriptionId $SubscriptionId -Certificate $Certificate
PS C:\> Select-AzureSubscription -SubscriptionName "Subscription07"
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -UseSubscription
```

Questo esempio usa l'autenticazione basata su certificato.

I primi due comandi assegnano valori alle variabili $SubscriptionId e $Thumbprint variabili.

Il terzo comando recupera il certificato identificato dall'impronta digitale in $Thumbprint e lo archivia in $Certificate.

Il quarto comando imposta la sottoscrizione su Subscription07 e il quinto comando seleziona la sottoscrizione.

Il comando finale crea un contesto nella sottoscrizione corrente per il server denominato lpqd0zbr8y.

## PARAMETERS

### -Credential
Specifica un oggetto credenziali che fornisce SQL Server'autenticazione per l'accesso al server.

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
Specifica il nome di dominio completo (FQDN) per il server di SQL database di Azure.
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
Specifica l'URL che questo cmdlet usa per accedere al portale DatabaseManagement di Azure SQL per il server.

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
Specifica il profilo di Azure da cui viene letto questo cmdlet.
Se non si specifica un profilo, questo cmdlet legge dal profilo predefinito locale.

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

### -ServerName
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

### -SubscriptionName
Specifica il nome della sottoscrizione di Azure che questo cmdlet usa per creare il contesto di connessione.
Se non si specifica alcun valore per questo parametro, il cmdlet usa la sottoscrizione corrente.
Eseguire il cmdlet Select-AzureSubscription per modificare l'abbonamento corrente.

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
Indica che questo cmdlet usa la sottoscrizione di Azure per creare il contesto di connessione.

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
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

## OUTPUT

### Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.IServerDataServiceContext

## NOTE
* Se si esegue l'autenticazione senza specificare un dominio e si usa Windows PowerShell 2.0, il cmdlet Get-Credential restituisce una barra rovesciata ( ) anteposta al nome utente, ad esempio \\ \utente. Windows PowerShell 3.0 non aggiunge la barra rovesciata. Questa barra rovesciata non viene riconosciuta dal parametro *Credential* del cmdlet **New-AzureSqlDatabaseServerContext.** Per rimuoverla, usare comandi simili ai seguenti:

  `PS C:\\\> $Credential = Get-Credential`
`PS C:\\\> $Credential = New-Object -TypeName 'System.Management.Automation.PSCredential' -ArgumentList $Credential.Username.Replace("\",""),$Credential.Password`

## COLLEGAMENTI CORRELATI



[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)

[New-AzureSqlDatabase](./New-AzureSqlDatabase.md)

[Remove-AzureSqlDatabase](./Remove-AzureSqlDatabase.md)

[Set-AzureSqlDatabase](./Set-AzureSqlDatabase.md)


