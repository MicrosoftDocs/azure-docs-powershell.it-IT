---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: CB601E21-424D-4B09-85E5-A4B2A5068267
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7716587787515221a6e016436a6e3d030c1ab0eb
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405619"
---
# Stop-AzureSqlDatabaseCopy

## SYNOPSIS
Termina una relazione di copia continua.

## SINTASSI

### ByInputObject
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-ForcedTermination] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### PerDatabase
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByDatabaseName
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIZIONE
Il **cmdlet Stop-AzureSqlDatabaseCopy** termina una relazione di copia continua.
Questo cmdlet interrompe lo spostamento di dati tra il database di origine e il database secondario o di destinazione e quindi modifica lo stato del database secondario in un database online autonomo.

Esistono due modi per terminare una relazione continua con la copia, la risoluzione o la risoluzione pianificata e la risoluzione forzata con possibile perdita di dati.
Nel server che ospita il database di origine è possibile eseguire questo cmdlet in modalità di terminazione forzata o di terminazione forzata.
Nel server che ospita il database secondario è necessario usare la modalità di terminazione forzata.

Una terminazione pianificata attende che tutte le transazioni commit nel database di origine, nel momento in cui si esegue il cmdlet, vengano replicate nel database secondario.
La terminazione forzata non attende la replica delle transazioni in sospeso e può causare la perdita di dati nel database secondario.

Mentre lo stato della replica è IN SOSPESO, solo la terminazione forzata può terminare correttamente una relazione di copia continua.
Se lo stato della replica è IN SOSPESO, la terminazione non forzata non è supportata.

## ESEMPI

### Esempio 1: Terminare una relazione di copia continua
```
PS C:\>Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

Questo comando termina la relazione di copia continua del database denominato Ordini nel server denominato lpqd0zbr8y.
Il server bk0b8kf658 ospita il database secondario.

### Esempio 2: Interrompere forzatamente una relazione di copia continua
```
PS C:\>$DatabaseCopy = Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders"
PS C:\> $DatabaseCopy | Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -ForcedTermination
```

Il primo comando recupera la relazione di copia del database per il database denominato Ordini nel server denominato lpqd0zbr8y.

Il secondo comando termina forzatamente una relazione di copia continua dal server che ospita il database secondario.

## PARAMETERS

### -Database
Specifica un oggetto che rappresenta l'origine SQL database di Azure.
Questo cmdlet termina la relazione di copia continua del database specificata da questo parametro.

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
Questo cmdlet termina la relazione di copia continua del database specificata da questo parametro.
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
Specifica il nome di un database.
Questo cmdlet termina la relazione di copia continua del database specificata da questo parametro.

```yaml
Type: String
Parameter Sets: ByDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Forza l'esecuzione del comando senza chiedere conferma all'utente.

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

### -ForcedTermination
Indica che questo cmdlet causa la terminazione forzata della relazione di copia continua.
La risoluzione forzata può causare la perdita di dati.
Per eseguire questo cmdlet in un server che ospita il database di destinazione, è necessario specificare questo parametro.
Per eseguire questo cmdlet in un server che ospita il database di origine, se il database secondario non è disponibile, è necessario specificare questo parametro.

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

### -PartnerDatabase
Specifica il nome del database secondario.
Se si specifica un nome, questo deve corrispondere al nome del database di origine.

```yaml
Type: String
Parameter Sets: ByDatabase, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerServer
Specifica il nome del server che ospita il database di destinazione.

```yaml
Type: String
Parameter Sets: ByDatabase, ByDatabaseName
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
Specifica il nome del server in cui si trova il database di origine.

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

### -Confirm
Chiede conferma prima di eseguire il cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa accadrebbe se il cmdlet viene eseguito.
Il cmdlet non viene eseguito.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy

### Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database

## OUTPUT

### Nessuno

## NOTE
* Autenticazione: questo cmdlet richiede l'autenticazione basata su certificato. Per un esempio su come usare l'autenticazione basata su certificato per impostare la sottoscrizione corrente, vedere il cmdlet **New-AzureSqlDatabaseServerContext.**
* Restrizioni: nel server che ospita il database secondario è supportata solo la terminazione forzata.
* Impatto della terminazione sul database secondario precedente: dopo la terminazione, il database secondario diventa un database indipendente. Se il seeding è già stato completato nel database secondario, dopo la chiusura il database è aperto per l'accesso completo. Se il database di origine è un database di lettura/scrittura, anche il database secondario precedente diventa un database di lettura-scrittura.

  Se il seeding è in corso, il seeding viene interrotto e il database secondario precedente non diventa mai visibile nel server che ospita il database secondario.

* È possibile impostare il database di origine sulla modalità di sola lettura. Questo garantisce la sincronizzazione dei database di origine e secondari dopo la terminazione e garantisce che nessuna transazione sia commessa durante la chiusura. Al termine dell'interruzione, impostare di nuovo l'origine sulla modalità di lettura-scrittura. Facoltativamente, è anche possibile impostare l'ex database secondario sulla modalità di lettura-scrittura.
* Monitoraggio: per verificare lo stato delle operazioni sia nell'origine che nella destinazione della relazione di copia continua, usare il cmdlet **Get-AzureSqlDatabaseOperation.**

## COLLEGAMENTI CORRELATI

[Azure SQL Database](https://azure.microsoft.com/en-us/services/sql-database/)

[Operazioni per i database SQL Azure](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Interrompi copia database](https://msdn.microsoft.com/en-us/library/dn509573.aspx)



[Get-AzureSqlDatabaseCopy](./Get-AzureSqlDatabaseCopy.md)

[Start-AzureSqlDatabaseCopy](./Start-AzureSqlDatabaseCopy.md)


