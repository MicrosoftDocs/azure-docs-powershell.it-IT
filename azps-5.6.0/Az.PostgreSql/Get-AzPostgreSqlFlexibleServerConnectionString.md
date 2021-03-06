---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/get-azpostgresqlflexibleserverconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerConnectionString.md
ms.openlocfilehash: 91da9592346e46f8410ceda85a44fddd2e2393f5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976493"
---
# Get-AzPostgreSqlFlexibleServerConnectionString

## SYNOPSIS
Ottenere la stringa di connessione in base al provider di connessione client.

## SINTASSI

### Ottieni (impostazione predefinita)
```
Get-AzPostgreSqlFlexibleServerConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzPostgreSqlFlexibleServerConnectionString -Client <String> -InputObject <IServerAutoGenerated>
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## DESCRIZIONE
Ottenere la stringa di connessione in base al provider di connessione client.

## ESEMPI

### Esempio 1: Ottenere la stringa di connessione in base al nome
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerConnectionString -Client ADO.NET -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test

Server=postgresql-test.postgres.database.azure.com;Database={your_database};Port=5432;User Id=adminuser;Password={your_password};
```

Questo cmdlet mostra la stringa di connessione di un client per nome server.

### Esempio 2: Ottenere la stringa di connessione del server PostgreSql in base all'identità
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Get-AzPostgreSqlFlexibleServerConnectionString -Client PHP

host=postgresqltestserver.postgres.database.azure.com port=5432 dbname={your_database} user=pwsh password={your_password} sslmode=require
```

Questo cmdlet ottiene la stringa di connessione del server PostgreSql in base all'identità.

## PARAMETERS

### -Client
Provider di connessione client.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Il server per la stringa di connessione To construct, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Nome del server.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nome del gruppo di risorse che contiene la risorsa. È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
ID sottoscrizione che identifica una sottoscrizione di Azure.

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated

## OUTPUT

### System.String

## NOTE

ALIAS

PROPRIETÀ DEI PARAMETRI COMPLESSE

Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate. Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.


<IServerAutoGenerated>INPUTOBJECT: server per la stringa di connessione
  - `Location <String>`: posizione geografica in cui si trova la risorsa
  - `[Tag <ITrackedResourceTags>]`: tag di risorsa.
    - `[(Any) <String>]`: indica che è possibile aggiungere qualsiasi proprietà all'oggetto.
  - `[AdministratorLogin <String>]`: nome di accesso di un server da parte dell'amministratore. Può essere specificato solo durante la creazione del server (ed è necessario per la creazione).
  - `[AdministratorLoginPassword <SecureString>]`: password di accesso dell'amministratore (necessaria per la creazione del server).
  - `[AvailabilityZone <String>]`: informazioni sull'area di disponibilità del server.
  - `[CreateMode <CreateMode?>]`: modalità per creare un nuovo server PostgreSQL.
  - `[DelegatedSubnetArgumentSubnetArmResourceId <String>]`: ID risorsa arm subnet delegata.
  - `[DisplayName <String>]`: nome visualizzato di un server.
  - `[HaEnabled <HaEnabledEnum?>]`: il valore stand by count può essere abilitato o disabilitato
  - `[IdentityType <ResourceIdentityType?>]`: tipo di identità.
  - `[MaintenanceWindowCustomWindow <String>]`: indica se la finestra personalizzata è abilitata o disabilitata
  - `[MaintenanceWindowDayOfWeek <Int32?>]`: giorno della settimana per la finestra di manutenzione
  - `[MaintenanceWindowStartHour <Int32?>]`: ora di inizio per la finestra di manutenzione
  - `[MaintenanceWindowStartMinute <Int32?>]`: minuto di inizio per la finestra di manutenzione
  - `[PointInTimeUtc <DateTime?>]`: consente di ripristinare l'ora di creazione del punto (formato ISO8601), specificando l'ora di ripristino.
  - `[PropertiesTag <IServerPropertiesTags>]`: metadati specifici dell'applicazione sotto forma di coppie chiave-valore.
    - `[(Any) <String>]`: indica che è possibile aggiungere qualsiasi proprietà all'oggetto.
  - `[SkuName <String>]`: il nome della SKU, in genere livello + famiglia + core, ad esempio Standard_D4s_v3.
  - `[SkuTier <SkuTier?>]`: il livello dello specifico SKU, ad esempio a scatto esploso.
  - `[SourceServerName <String>]`: il nome del server PostgreSQL di origine da cui eseguire il ripristino.
  - `[StorageProfileBackupRetentionDay <Int32?>]`: giorni di conservazione del backup per il server.
  - `[StorageProfileStorageMb <Int32?>]`: spazio di archiviazione massimo consentito per un server.
  - `[Version <ServerVersion?>]`: versione del server PostgreSQL.

## COLLEGAMENTI CORRELATI

