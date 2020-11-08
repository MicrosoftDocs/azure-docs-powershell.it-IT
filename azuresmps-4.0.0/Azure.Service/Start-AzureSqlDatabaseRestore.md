---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 383F36F3-3F52-4FC3-99F7-831096E6037D
online version: ''
schema: 2.0.0
ms.openlocfilehash: ff7c7cd50b06a4110b6af12611f3d91eaedfd227
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023384"
---
# Start-AzureSqlDatabaseRestore

## Sinossi
Esegue un ripristino puntuale di un database.

## SINTASSI

### BySourceDatabaseObject
```
Start-AzureSqlDatabaseRestore [-SourceServerName <String>] -SourceDatabase <Database>
 [-TargetServerName <String>] -TargetDatabaseName <String> [-PointInTime <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### BySourceRestorableDroppedDatabaseObject
```
Start-AzureSqlDatabaseRestore [-SourceServerName <String>]
 -SourceRestorableDroppedDatabase <RestorableDroppedDatabase> [-TargetServerName <String>]
 -TargetDatabaseName <String> [-PointInTime <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### BySourceDatabaseName
```
Start-AzureSqlDatabaseRestore -SourceServerName <String> -SourceDatabaseName <String>
 [-TargetServerName <String>] -TargetDatabaseName <String> [-PointInTime <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### BySourceRestorableDroppedDatabaseName
```
Start-AzureSqlDatabaseRestore -SourceServerName <String> -SourceDatabaseName <String>
 -SourceDatabaseDeletionDate <DateTime> [-TargetServerName <String>] [-RestorableDropped]
 -TargetDatabaseName <String> [-PointInTime <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Start-AzureSqlDatabaseRestore** esegue un ripristino puntuale di un database di base, standard o Premium.
Database SQL di Azure mantiene i backup del database di base di 7 giorni, standard per 14 giorni e Premium per 35 giorni.
L'operazione di ripristino crea un nuovo database.
Se il database di origine non viene eliminato, il parametro *sourcedatabasename* e *NomeDatabaseDestinazione* deve avere valori diversi.

Il database SQL di Azure attualmente non supporta il ripristino Cross server.
I nomi dei server di origine e di destinazione devono essere uguali.

## ESEMPI

### Esempio 1: ripristinare un database specificato come oggetto in un momento
```
PS C:\> $Database = Get-AzureSqlDatabase -ServerName "Server01" -DatabaseName "Database17" 
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceDatabase $Database -TargetDatabaseName "DatabaseRestored" -PointInTime "2013-01-01 06:00:00"
```

Il primo comando ottiene un oggetto di database per il database denominato Database17 nel server denominato Server01 e lo archivia nella variabile $Database.

Il secondo comando Ripristina il database in un momento specifico.
Il comando specifica il nome per il nuovo database.

### Esempio 2: ripristinare un database specificato per nome in un momento
```
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceServerName "Server01" -SourceDatabaseName "Database17" -TargetDatabaseName "DatabaseRestored" -PointInTime "2013-01-01 06:00:00"
```

Questo comando Ripristina il database denominato Database17 in un determinato momento.
Il comando specifica il nome per il nuovo database.

### Esempio 3: ripristinare un database abbandonato specificato come oggetto in un momento
```
PS C:\> $Database = Get-AzureSqlDatabase -RestorableDropped -ServerName "Server01" -DatabaseName "Database01" -DatabaseDeletionDate "2012-11-09T22:59:43.000Z" 
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceRestorableDroppedDatabase $Database -TargetDatabaseName "DroppedDatabaseRestored"
```

Il primo comando ottiene un oggetto di database per il database denominato Database01 nel server denominato Server01.
Il comando specifica il parametro *RestorableDropped* .
Di conseguenza, il cmdlet recupera il database eliminato ripristinabile il punto di ripristino specificato.
Il comando Archivia l'oggetto di database nella variabile $Database.

Il secondo comando Ripristina il database eliminato specificato da $Database.
Il comando specifica il nome per il nuovo database.

## PARAMETRI

### -PointInTime
Specifica il punto di ripristino a cui ripristinare il database.
Al termine dell'operazione di ripristino, il database viene ripristinato nello stato in cui si trovava alla data e all'ora specificate da questo parametro.
Per impostazione predefinita, per un database dinamico impostato sull'ora corrente e per un database eliminato, questo cmdlet usa l'ora in cui il database è stato eliminato.

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

### -RestorableDropped
Indica che questo cmdlet ripristina un database abbandonato ripristinabile.

```yaml
Type: SwitchParameter
Parameter Sets: BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceDatabase
Specifica il nome del database ripristinato da questo cmdlet.

```yaml
Type: Database
Parameter Sets: BySourceDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SourceDatabaseDeletionDate
Specifica la data e l'ora in cui il database è stato eliminato.
È necessario includere millisecondi quando si specifica il tempo per corrispondere al tempo effettivo di eliminazione del database.

```yaml
Type: DateTime
Parameter Sets: BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceDatabaseName
Specifica il nome del database Live ripristinato da questo cmdlet.

```yaml
Type: String
Parameter Sets: BySourceDatabaseName, BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceRestorableDroppedDatabase
Specifica un oggetto che rappresenta il database di cui è stato ripristinato il ripristino di questo cmdlet.
Per ottenere un oggetto **RestorableDroppedDatabase** , usa il cmdlet Get-AzureSqlDatabase e specifica il parametro *RestorableDropped* .

```yaml
Type: RestorableDroppedDatabase
Parameter Sets: BySourceRestorableDroppedDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SourceServerName
Specifica il nome del server in cui il database di origine è in esecuzione o in cui è stato eseguito il database di origine prima dell'eliminazione.

```yaml
Type: String
Parameter Sets: BySourceDatabaseObject, BySourceRestorableDroppedDatabaseObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: BySourceDatabaseName, BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NomeDatabaseDestinazione
Specifica il nome del nuovo database creato dall'operazione di ripristino.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetServerName
Specifica il nome del server a cui questo cmdlet ripristina il database.

Il database SQL di Azure attualmente non supporta il ripristino Cross server.
I nomi dei server di origine e di destinazione devono essere uguali.

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

### Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. RestorableDroppedDatabase

### Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. database

## OUTPUT

### Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. RestoreDatabaseOperation

## Note
* Per eseguire questo cmdlet, è necessario usare l'autenticazione basata su certificati. Eseguire i comandi seguenti nel computer in cui eseguire questo cmdlet: 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## COLLEGAMENTI CORRELATI

[Database SQL di Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Creare una richiesta di ripristino di database](https://msdn.microsoft.com/en-us/library/dn509571.aspx)

[Operazioni per i database SQL di Azure](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)


