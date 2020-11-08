---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
ms.openlocfilehash: 1a6e96a8b8e030628655bdf95c58b726341dd2cc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202372"
---
# Get-AzMariaDbConnectionString

## Sinossi
Ottenere una stringa di connessione di un MariaDB in un Framework specifico.

## SINTASSI

### Nomeserver (impostazione predefinita)
```
Get-AzMariaDbConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### ServerObject
```
Get-AzMariaDbConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## Descrizione
Ottenere una stringa di connessione di un MariaDB in un Framework specifico.

## ESEMPI

### Esempio 1: ottenere una stringa di connessione di MariaDB
```powershell
PS C:\> Get-AzMariaDbConnectionString -ServerName mariadb-asd-01 -ResourceGroupName mariadb-test-qu5ov0 -Client ADO.NET

Server=mariadb-asd-01.mariadb.database.azure.com; Port=3306; Database={your_database}; Uid=adminuser@mariadb-asd-01; Pwd={your_password}; SslMode=Preferred;
```

Questo comando ottiene una stringa di connessione di MariaDB.

### Esempio 2: ottenere una stringa di connessione di MariaDB
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-gp-t03 -ResourceGroupName lucas-manual-test | Get-AzMariaDbConnectionString -Client PHP

$con=mysqli_init();mysqli_ssl_set($con, NULL, NULL, {ca-cert filename}, NULL, NULL); mysqli_real_connect($con, "mariadb-gp-t03.mariadb.database.azure.com", "adminuser@mariadb-gp-t03", {your_password}, {your_database}, 3306);
```

Questo comando ottiene una stringa di connessione di MariaDB.

## PARAMETRI

### -Client
Connettere il tipo di client

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
Region DefaultParameters le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

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
Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer
Parameter Sets: ServerObject
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
Parameter Sets: ServerName
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nome del gruppo di risorse che contiene la risorsa.

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
L'ID abbonamento fa parte dell'URI per ogni chiamata di servizio

```yaml
Type: System.String
Parameter Sets: ServerName
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

### Microsoft. Azure. PowerShell. Cmdlets. MariaDb. Models. Api20180601Preview. IServer

## OUTPUT

### System. String

## Note

ALIAS

PROPRIETÀ COMPLESSE DI PARAMETRI

Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate. Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.


INPUTOBJECT <IServer> : parametro Identity
  - `Location <String>`: La posizione in cui risiede la risorsa.
  - `[Tag <ITrackedResourceTags>]`: Metadati specifici dell'applicazione sotto forma di coppie chiave-valore.
    - `[(Any) <String>]`: Indica che qualsiasi proprietà può essere aggiunta a questo oggetto.
  - `[AdministratorLogin <String>]`: Nome di accesso dell'amministratore di un server. Può essere specificato solo quando il server viene creato (ed è necessario per la creazione).
  - `[EarliestRestoreDate <DateTime?>]`: Ora di creazione del punto di ripristino più iniziale (formato ISO8601)
  - `[FullyQualifiedDomainName <String>]`: Il nome di dominio completo di un server.
  - `[IdentityType <IdentityType?>]`: Il tipo di identità. Imposta questa opzione su' SystemAssigned ' per creare e assegnare automaticamente un Principal di Azure Active Directory per la risorsa.
  - `[MasterServerId <String>]`: ID server master di un server di replica.
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

