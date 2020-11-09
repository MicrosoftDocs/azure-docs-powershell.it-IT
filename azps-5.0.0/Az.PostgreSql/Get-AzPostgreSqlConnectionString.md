---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConnectionString.md
ms.openlocfilehash: 8df35a38889e2c91bd74625ae916fd10739d9db1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311173"
---
# Get-AzPostgreSqlConnectionString

## Sinossi
Ottenere la stringa di connessione in base al provider di connessione client.

## SINTASSI

### Get (impostazione predefinita)
```
Get-AzPostgreSqlConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzPostgreSqlConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## Descrizione
Ottenere la stringa di connessione in base al provider di connessione client.

## ESEMPI

### Esempio 1: ottenere la stringa di connessione del server PostgreSql in base al gruppo di risorse e al nome del server
```powershell
PS C:\> Get-AzPostgreSqlConnectionString -Client ADO.NET -Name PostgreSqlTestServer -ResourceGroupName PostgreSqlTestRG

Server=postgresqltestserver.postgres.database.azure.com;Database={your_database};Port=5432;User Id=pwsh@postgresqltestserver;Password={your_password};Ssl Mode=Require;
```

Questo cmdlet ottiene la stringa di connessione del server PostgreSql in base al gruppo di risorse e al nome del server.

### Esempio 2: ottenere la stringa di connessione del server PostgreSql per identità
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Get-AzPostgreSqlConnectionString -Client PHP

host=postgresqltestserver.postgres.database.azure.com port=5432 dbname={your_database} user=pwsh@postgresqltestserver password={your_password} sslmode=require
```

Questo cmdlet ottiene la stringa di connessione del server PostgreSql per identità.

## PARAMETRI

### -Client
Provider di connessioni client.

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
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

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
Oggetto server di origine per cui creare la replica.
Per costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nome
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
Nome del gruppo di risorse che contiene la risorsa, è possibile ottenere questo valore dall'API di gestione risorse di Azure o dal portale.

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
ID sottoscrizione che identifica un abbonamento a Azure.

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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### Microsoft. Azure. PowerShell. Cmdlets. PostgreSql. Models. Api20171201. IServer

## OUTPUT

### System. String

## Note

ALIAS

PROPRIETÀ COMPLESSE DI PARAMETRI

Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate. Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.


INPUTOBJECT <IServer> : oggetto server di origine da cui creare la replica.
  - `Location <String>`: La posizione in cui risiede la risorsa.
  - `[Tag <ITrackedResourceTags>]`: Metadati specifici dell'applicazione sotto forma di coppie chiave-valore.
    - `[(Any) <String>]`: Indica che qualsiasi proprietà può essere aggiunta a questo oggetto.
  - `[AdministratorLogin <String>]`: Nome di accesso dell'amministratore di un server. Può essere specificato solo quando il server viene creato (ed è necessario per la creazione).
  - `[EarliestRestoreDate <DateTime?>]`: Ora di creazione del punto di ripristino più iniziale (formato ISO8601)
  - `[FullyQualifiedDomainName <String>]`: Il nome di dominio completo di un server.
  - `[IdentityType <IdentityType?>]`: Il tipo di identità. Imposta questa opzione su' SystemAssigned ' per creare e assegnare automaticamente un Principal di Azure Active Directory per la risorsa.
  - `[InfrastructureEncryption <InfrastructureEncryption?>]`: Stato che indica se il server ha abilitato la crittografia dell'infrastruttura.
  - `[MasterServerId <String>]`: ID server master di un server di replica.
  - `[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Applicare una versione TLS minima per il server.
  - `[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Se l'accesso alla rete pubblica è consentito per il server. Il valore è facoltativo ma, se passato, deve essere "Enabled" o "disabled"
  - `[ReplicaCapacity <Int32?>]`: Il numero massimo di repliche che un server master può avere.
  - `[ReplicationRole <String>]`: Il ruolo di replica del server.
  - `[SkuCapacity <Int32?>]`: La capacità di scala su/fuori, che rappresenta le unità di calcolo del server.
  - `[SkuFamily <String>]`: La famiglia di hardware.
  - `[SkuName <String>]`: Nome della SKU, in genere, livello + famiglia + Core, ad esempio B_Gen4_1, GP_Gen5_8.
  - `[SkuSize <String>]`: Il codice delle dimensioni, che deve essere interpretato dalla risorsa in base alle esigenze.
  - `[SkuTier <SkuTier?>]`: Il livello del particolare SKU, ad esempio Basic.
  - `[SslEnforcement <SslEnforcementEnum?>]`: Abilitare l'applicazione SSL o meno quando si connette al server.
  - `[StorageProfileBackupRetentionDay <Int32?>]`: Giorni di conservazione del backup per il server.
  - `[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Abilitare il backup Geo-ridondante o meno per il server.
  - `[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Abilitare l'espansione automatica dello spazio di archiviazione.
  - `[StorageProfileStorageMb <Int32?>]`: Spazio di archiviazione max consentito per un server.
  - `[UserVisibleState <ServerState?>]`: Uno stato di un server visibile per l'utente.
  - `[Version <ServerVersion?>]`: Versione server.

## COLLEGAMENTI CORRELATI

