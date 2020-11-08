---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F63769D6-9A31-4A67-972A-1E0428853C86
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88f61718e363a630b70519590025a6da80364aeb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023381"
---
# Start-AzureSqlDatabaseRecovery

## Sinossi
Avvia una richiesta di ripristino per un database.

## SINTASSI

### BySourceDatabaseName
```
Start-AzureSqlDatabaseRecovery -SourceServerName <String> -SourceDatabaseName <String>
 [-TargetServerName <String>] [-TargetDatabaseName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### BySourceDatabaseObject
```
Start-AzureSqlDatabaseRecovery -SourceDatabase <RecoverableDatabase> [-TargetServerName <String>]
 [-TargetDatabaseName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Start-AzureSqlDatabaseRecovery** avvia una richiesta di ripristino per un database Live o Dropped.
Questo cmdlet supporta il ripristino di base che usa l'ultimo backup disponibile noto per il database.
L'operazione di ripristino crea un nuovo database.
Se si recupera un database Live nello stesso server, è necessario specificare un nome diverso per il nuovo database.

Per eseguire un ripristino puntuale per un database, USA invece il cmdlet **Start-AzureSqlDatabaseRestore** .

## ESEMPI

### Esempio 1: recuperare un database specificato come oggetto
```
PS C:\> $Database = Get-AzureSqlRecoverableDatabase -ServerName "Server01" -DatabaseName "Database17" 
PS C:\> $Operation = Start-AzureSqlDatabaseRecovery -SourceDatabase $Database -TargetDatabaseName "DatabaseRestored"
```

Il primo comando ottiene un oggetto database usando il cmdlet **Get-AzureSqlRecoverableDatabase** .
Il comando Archivia l'oggetto nella variabile $Database.

Il secondo comando Ripristina il database archiviato in $Database.

### Esempio 2: recuperare un database specificato per nome
```
PS C:\> $Operation = Start-AzureSqlDatabaseRecovery -SourceServerName "Server01" -SourceDatabaseName "Database17" -TargetDatabaseName "DatabaseRestored"
```

Questo comando ripristina un database usando il nome del database.

## PARAMETRI

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

### -SourceDatabase
Specifica l'oggetto di database che rappresenta il database che questo cmdlet viene ripristinato.

```yaml
Type: RecoverableDatabase
Parameter Sets: BySourceDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SourceDatabaseName
Specifica il nome del database che questo cmdlet viene ripristinato.

```yaml
Type: String
Parameter Sets: BySourceDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceServerName
Specifica il nome del server in cui il database di origine è in esecuzione o in cui è stato eseguito il database di origine prima dell'eliminazione.

```yaml
Type: String
Parameter Sets: BySourceDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NomeDatabaseDestinazione
Specifica il nome del database recuperato.
Se il database di origine è ancora attivo, per recuperarlo nello stesso server è necessario specificare un nome diverso dal nome del database di origine.

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

### -TargetServerName
Specifica il nome del server a cui ripristinare un database.
È possibile ripristinare un database nello stesso server o in un server diverso.

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

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Microsoft. WindowsAzure. Management. SQL. Models. RecoverableDatabase

## OUTPUT

### Microsoft. WindowsAzure. Management. SQL. Models. RecoverDatabaseOperation

## Note
* Per eseguire questo cmdlet, è necessario usare l'autenticazione basata su certificati. Eseguire i comandi seguenti nel computer in cui si esegue questo cmdlet: 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## COLLEGAMENTI CORRELATI

[Database SQL di Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Creare una richiesta di ripristino di database](https://msdn.microsoft.com/en-us/library/dn800986.aspx)

[Geo-replica in Azure SQL database](https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/)

[Operazioni per i database SQL di Azure](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlRecoverableDatabase](./Get-AzureSqlRecoverableDatabase.md)

[Start-AzureSqlDatabaseRestore](./Start-AzureSqlDatabaseRestore.md)


