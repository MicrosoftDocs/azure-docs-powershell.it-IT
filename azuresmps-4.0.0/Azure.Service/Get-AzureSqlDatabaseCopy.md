---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5AEF7D44-624D-4794-86FF-156E6729BB56
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8752766572975ef97094a3915446086c903a7fd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029757"
---
# Get-AzureSqlDatabaseCopy

## Sinossi
Controlla lo stato delle relazioni di copia.

## SINTASSI

### ByServerNameOnly (impostazione predefinita)
```
Get-AzureSqlDatabaseCopy -ServerName <String> [-DatabaseName <String>] [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByInputObject
```
Get-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ByDatabase
```
Get-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureSqlDatabaseCopy** controlla lo stato di una o più relazioni di copia attive.
Eseguire questo cmdlet dopo aver eseguito il cmdlet Start-AzureSqlDatabaseCopy o Stop-AzureSqlDatabaseCopy.
È possibile controllare una relazione di copia specifica, tutte le relazioni di copia o un elenco filtrato delle relazioni di copia, ad esempio tutte le copie in uno specifico server di destinazione.
Puoi eseguire questo cmdlet nel server che ospita il database di origine o di destinazione.

Questo cmdlet è sincrono.
Il cmdlet blocca la console di Azure PowerShell fino a quando non restituisce un oggetto stato.

I parametri *PartnerServer* e *PartnerDatabase* sono facoltativi.
Se non specifichi un parametro, questo cmdlet restituisce una tabella di risultati.
Per visualizzare lo stato di un solo database specifico, specificare entrambi i parametri.

## ESEMPI

### Esempio 1: ottenere lo stato di copia di un database
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

Questo comando ottiene lo stato del database denominato Orders nel server denominato lpqd0zbr8y.
Il parametro *PartnerServer* limita questo comando al server bk0b8kf658.

### Esempio 2: ottenere lo stato di tutte le copie in un serverGet lo stato di tutte le copie in un server
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y"
```

Questo comando consente di ottenere lo stato di tutte le copie attive nel server denominato lpqd0zbr8y.

## PARAMETRI

### -Database
Specifica un oggetto che rappresenta il database SQL di Azure di origine.
Questo cmdlet ottiene lo stato di copia del database specificato da questo parametro.

```yaml
Type: Database
Parameter Sets: ByDatabase
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseCopy
Specifica un oggetto che rappresenta un database.
Questo cmdlet ottiene lo stato di copia del database specificato da questo parametro.
Questo parametro accetta l'input della pipeline.

```yaml
Type: DatabaseCopy
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
Specifica il nome del database di origine.
Questo cmdlet ottiene lo stato di copia del database specificato da questo parametro.

```yaml
Type: String
Parameter Sets: ByServerNameOnly
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerDatabase
Specifica il nome del database secondario.
Se il database non viene trovato nella sys.dm_database_copies visualizzazione a gestione dinamica, questo cmdlet restituisce un oggetto stato vuoto.

```yaml
Type: String
Parameter Sets: ByServerNameOnly, ByDatabase
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerServer
Specifica il nome del server che ospita il database di destinazione.
Se il server non viene trovato nella sys.dm_database_copies visualizzazione a gestione dinamica, questo cmdlet restituisce un oggetto stato vuoto.

```yaml
Type: String
Parameter Sets: ByServerNameOnly, ByDatabase
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

### -Nomeserver
Specifica il nome del server in cui risiede la copia del database.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Microsoft. WindowsAzure. Commands. SqlDatabase. Model. DatabaseCopy

### Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. database

## OUTPUT

### Microsoft. WindowsAzure. Commands. SqlDatabase. Model. DatabaseCopy

## Note
* Autenticazione: questo cmdlet richiede l'autenticazione basata su certificati. Per un esempio di come usare l'autenticazione basata su certificati per impostare la sottoscrizione corrente, vedere il cmdlet New-AzureSqlDatabaseServerContext.

## COLLEGAMENTI CORRELATI

[Database SQL di Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Operazioni per i database SQL di Azure](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Cmdlet di database SQL di Azure](./Azure.SQLDatabase.md)

[Start-AzureSqlDatabaseCopy](./Start-AzureSqlDatabaseCopy.md)

[Stop-AzureSqlDatabaseCopy](./Stop-AzureSqlDatabaseCopy.md)


