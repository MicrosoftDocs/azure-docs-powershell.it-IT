---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 7427A101-9439-45B9-B72E-F8C2DA85E412
online version: ''
schema: 2.0.0
ms.openlocfilehash: c10ae808d105079b9739516bf9eaf316241b1b11
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029760"
---
# Get-AzureSqlDatabase

## Sinossi
Recupera uno o più database.

## SINTASSI

### ByConnectionContext (impostazione predefinita)
```
Get-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> [-Database <Database>]
 [-DatabaseName <String>] [-RestorableDropped] [-RestorableDroppedDatabase <RestorableDroppedDatabase>]
 [-DatabaseDeletionDate <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByServerName
```
Get-AzureSqlDatabase -ServerName <String> [-Database <Database>] [-DatabaseName <String>] [-RestorableDropped]
 [-RestorableDroppedDatabase <RestorableDroppedDatabase>] [-DatabaseDeletionDate <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureSqlDatabase** recupera una o più istanze di un database SQL di Azure da un server di database SQL di Azure.
Puoi specificare il server con un contesto di connessione del server di database SQL di Azure creato usando il cmdlet **New-AzureSqlDatabaseServerContext** .
In alternativa, se specifichi il nome del server di database SQL di Azure, il cmdlet usa le informazioni correnti sull'abbonamento a Azure per autenticare la richiesta di accesso al server.

Se non specifichi un database, il cmdlet **Get-AzureSqlDatabase** restituirà tutti i database del server specificato.

Recupero di database rilasciati ripristinabili:

Recuperare i database rilasciati ripristinabili usando il parametro *RestorableDropped* .
Per restituire tutti i database rilasciati ripristinabili, usare il parametro *RestorableDropped* senza *DatabaseName* e *DatabaseDeletionDate*.
Per restituire un database abbandonato ripristinabile specifico, usare il parametro *RestorableDropped* con i parametri *DatabaseName* e *DatabaseDeletionDate* .
Quando si recupera un database rilasciabile specifico per il ripristino tramite il parametro *DatabaseName* , è necessario includere anche il parametro *DatabaseDeletionDate* e il valore *DatabaseDeletionDate* specificato deve includere millisecondi per corrispondere al database desiderato.

Il cmdlet **Get-AzureSqlDatabase** restituisce tutti i database rilasciati ripristinabili in un server o un database specifico che corrisponde sia a *DatabaseName* che a *DatabaseDeletionDate*.
Per restituire i database rilasciati ripristinabili che soddisfano criteri diversi, ad esempio tutti i database rilasciati ripristinabili di un nome specifico, è necessario restituire tutti i database rimossi ripristinabili e quindi filtrare i risultati nel client.

## ESEMPI

### Esempio 1: recuperare tutti i database in un server
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y"
```

Questo comando recupera tutti i database nel server denominato lpqd0zbr8y.

### Esempio 2: recuperare tutti i database rilasciati ripristinabili in un server
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -RestorableDropped
```

Questo comando recupera tutti i database rilasciati ripristinabili nel server denominato lpqd0zbr8y.

### Esempio 3: recuperare un database da un server specificato da un contesto di connessione
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
```

Questo comando Recupera il database denominato Database01 dal server specificato dal contesto di connessione $Context.

### Esempio 4: archiviare un oggetto di database in una variabile
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
```

Questo comando Recupera il database denominato Database01 dal server denominato lpqd0zbr8y.
Il comando Archivia l'oggetto di database nella variabile $Database 01.

### Esempio 5: recuperare un database abbandonato ripristinabile
```
PS C:\> $DroppedDB = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01" -DatabaseDeletionDate "2012-11-09T22:59:43.000Z" -RestorableDropped
```

Questo comando Recupera il database abbandonato ripristinabile denominato Database01 che è stato eliminato in 11/9/2012 dal server denominato lpqd0zbr8y.
Questo comando Archivia i risultati nella variabile $DroppedDB.

### Esempio 6: recuperare tutti i database rilasciati ripristinati in un server e filtrare i risultati
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -RestorableDropped | Where-Object {$_.Name -eq "ContactDB"}
```

Questo comando recupera tutti i database rilasciati ripristinati nel server denominato lpqd0zbr8y e quindi filtra i risultati solo nei database denominati ContactDB.

## PARAMETRI

### -ConnectionContext
Specifica il contesto di connessione di un server da cui recuperare un database.

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Database
Specifica un oggetto che rappresenta il database recuperato da questo cmdlet.

```yaml
Type: Database
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseDeletionDate
Specifica la data e l'ora di un'eliminazione.
Se specifichi il parametro *RestorableDropped* , specifica questo parametro per recuperare un database abbandonato ripristinabile in base alla data e all'ora di eliminazione.

Il parametro *DatabaseDeletionDate* deve includere millisecondi per corrispondere all'ora del database desiderato.
Se si specifica un valore senza millisecondi, il database non viene trovato.

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

### -DatabaseName
Specifica il nome del database recuperato da questo cmdlet.

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
Indica che questo cmdlet restituisce gli oggetti *RestorableDroppedDatabase* anziché gli oggetti di *database* .
Puoi usare il parametro *DatabaseDeletionDate* per selezionare un database rilasciabile ripristinato specifico.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestorableDroppedDatabase
Specifica un oggetto che rappresenta il database rilasciabile ripristinato recuperato da questo cmdlet.

```yaml
Type: RestorableDroppedDatabase
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nomeserver
Specifica il nome del server che contiene il database recuperato da questo cmdlet.
Il cmdlet usa l'abbonamento Azure corrente per accedere al server.

```yaml
Type: String
Parameter Sets: ByServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. database

### Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. RestorableDroppedDatabase

## OUTPUT

### IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database\>
Questo cmdlet restituisce un oggetto *database* se non specifichi il parametro *RestorableDropped* .

### IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase\>
Questo cmdlet restituisce un oggetto *RestorableDroppedDatabase* se specifichi il parametro *RestorableDropped* .

## Note

## COLLEGAMENTI CORRELATI

[Database SQL di Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Operazioni per i database SQL di Azure](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[New-AzureSqlDatabase](./New-AzureSqlDatabase.md)

[New-AzureSqlDatabaseServerContext](./New-AzureSqlDatabaseServerContext.md)

[Remove-AzureSqlDatabase](./Remove-AzureSqlDatabase.md)

[Set-AzureSqlDatabase](./Set-AzureSqlDatabase.md)


