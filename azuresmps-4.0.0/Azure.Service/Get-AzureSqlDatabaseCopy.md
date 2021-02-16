---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5AEF7D44-624D-4794-86FF-156E6729BB56
online version: ''
schema: 2.0.0
ms.openlocfilehash: 95e276bf6af11698a4b3b82077175ec2ede2d7dc
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402423"
---
# Get-AzureSqlDatabaseCopy

## SYNOPSIS
Controlla lo stato delle relazioni di copia.

## SINTASSI

### ByServerNameOnly (Default)
```
Get-AzureSqlDatabaseCopy -ServerName <String> [-DatabaseName <String>] [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByInputObject
```
Get-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### PerDatabase
```
Get-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRIZIONE
Il **cmdlet Get-AzureSqlDatabaseCopy** controlla lo stato di una o più relazioni di copia attive.
Eseguire questo cmdlet dopo aver eseguito il cmdlet Start-AzureSqlDatabaseCopy o Stop-AzureSqlDatabaseCopy cmdlet.
È possibile verificare una relazione di copia specifica, tutte le relazioni di copia o un elenco filtrato di relazioni di copia, ad esempio tutte le copie in uno specifico server di destinazione.
È possibile eseguire questo cmdlet nel server che ospita il database di origine o di destinazione.

Questo cmdlet è sincrono.
Il cmdlet blocca la console di Azure PowerShell finché non restituisce un oggetto di stato.

I *parametri PartnerServer* e *PartnerDatabase* sono facoltativi.
Se nessuno dei due parametri viene specificato, questo cmdlet restituisce una tabella dei risultati.
Per visualizzare lo stato solo per un database specifico, specificare entrambi i parametri.

## ESEMPI

### Esempio 1: Ottenere lo stato di copia di un database
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

Questo comando ottiene lo stato del database denominato Ordini nel server denominato lpqd0zbr8y.
Il *parametro PartnerServer* limita questo comando al server bk0b8kf658.

### Esempio 2: Ottenere lo stato di tutte le copie in un serverGet lo stato di tutte le copie in un server
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y"
```

Questo comando ottiene lo stato di tutte le copie attive nel server denominato lpqd0zbr8y.

## PARAMETERS

### -Database
Specifica un oggetto che rappresenta l'origine SQL database di Azure.
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
Questo cmdlet ottiene lo stato della copia del database specificato da questo parametro.

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
Se il database non viene trovato nella visualizzazione sys.dm_database_copies gestione dinamica, questo cmdlet restituisce un oggetto di stato vuoto.

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
Se il server non viene trovato nella visualizzazione sys.dm_database_copies gestione dinamica, questo cmdlet restituisce un oggetto di stato vuoto.

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
Specifica il nome del server in cui si trova la copia del database.

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
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy

### Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database

## OUTPUT

### Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy

## NOTE
* Autenticazione: questo cmdlet richiede l'autenticazione basata su certificato. Per un esempio su come usare l'autenticazione basata su certificato per impostare l'abbonamento corrente, vedere il cmdlet New-AzureSqlDatabaseServerContext certificato.

## COLLEGAMENTI CORRELATI

[Azure SQL Database](https://azure.microsoft.com/en-us/services/sql-database/)

[Operazioni per i database SQL Azure](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)



[Start-AzureSqlDatabaseCopy](./Start-AzureSqlDatabaseCopy.md)

[Stop-AzureSqlDatabaseCopy](./Stop-AzureSqlDatabaseCopy.md)


