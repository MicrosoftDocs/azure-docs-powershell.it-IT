---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: CB601E21-424D-4B09-85E5-A4B2A5068267
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2b7674cb5b7abc489dc6aa6d3746f499b9686312
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029865"
---
# Stop-AzureSqlDatabaseCopy

## Sinossi
Termina una relazione di copia continua.

## SINTASSI

### ByInputObject
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-ForcedTermination] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByDatabase
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

## Descrizione
Il cmdlet **Stop-AzureSqlDatabaseCopy** termina una relazione di copia continua.
Questo cmdlet interrompe lo spostamento dei dati tra il database di origine e il database secondario o di destinazione e quindi modifica lo stato del database secondario in un database online autonomo.

Esistono due modi per terminare una relazione di copia continua, una terminazione o una terminazione pianificata e una terminazione forzata con possibili perdite di dati.
Nel server che ospita il database di origine è possibile eseguire questo cmdlet in modalità terminazione o terminazione forzata.
Nel server che ospita il database secondario è necessario usare la modalità di terminazione forzata.

Una terminazione pianificata attende che tutte le transazioni impegnate nel database di origine, al momento dell'esecuzione del cmdlet, siano state replicate nel database secondario.
La terminazione forzata non attende la replica delle transazioni di cui è stato eseguito il commit in sospeso e può causare possibili perdite di dati nel database secondario.

Mentre lo stato di replica è in sospeso, solo la terminazione forzata può terminare correttamente una relazione di copia continua.
Se lo stato di replica è in sospeso, la terminazione non forzata non è supportata.

## ESEMPI

### Esempio 1: terminare una relazione di copia continua
```
PS C:\>Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

Questo comando termina la relazione di copia continua del database denominata Orders sul server denominato lpqd0zbr8y.
Il server denominato bk0b8kf658 ospita il database secondario.

### Esempio 2: terminazione forzata di una relazione di copia continua
```
PS C:\>$DatabaseCopy = Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders"
PS C:\> $DatabaseCopy | Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -ForcedTermination
```

Il primo comando ottiene la relazione di copia del database per il database denominato Orders nel server denominato lpqd0zbr8y.

Il secondo comando termina con forza una relazione di copia continua dal server che ospita il database secondario.

## PARAMETRI

### -Database
Specifica un oggetto che rappresenta il database SQL di Azure di origine.
Questo cmdlet termina la relazione di copia continua del database specificato da questo parametro.

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
Questo cmdlet termina la relazione di copia continua del database specificato da questo parametro.
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
Questo cmdlet termina la relazione di copia continua del database specificato da questo parametro.

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
Impone l'esecuzione del comando senza richiedere la conferma dell'utente.

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
La terminazione forzata può causare la perdita di dati.
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
Se specifichi un nome, deve corrispondere al nome del database di origine.

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
Specifica il nome del server in cui risiede il database di origine.

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

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

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
Mostra cosa succede se il cmdlet viene eseguito.
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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Microsoft. WindowsAzure. Commands. SqlDatabase. Model. DatabaseCopy

### Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. database

## OUTPUT

### Nessuno

## Note
* Autenticazione: questo cmdlet richiede l'autenticazione basata su certificati. Per un esempio di come usare l'autenticazione basata su certificati per impostare la sottoscrizione corrente, vedere il cmdlet **New-AzureSqlDatabaseServerContext** .
* Restrizioni: nel server che ospita il database secondario è supportata solo la terminazione forzata.
* Impatto della terminazione nell'ex database secondario: dopo la terminazione, il database secondario diventa un database indipendente. Se i seeding sono già stati completati nel database secondario, dopo la terminazione questo database è aperto per l'accesso completo. Se il database di origine è un database di lettura e scrittura, anche il database secondario precedente diventa un database di lettura e scrittura.

  Se il seeding è attualmente in corso, il seeding viene interrotto e il database secondario precedente non diventa mai visibile nel server che ospita il database secondario.

* Puoi impostare il database di origine in modalità di sola lettura. Questo garantisce che i database di origine e secondari vengano sincronizzati dopo la terminazione e che non vengano commessi transazioni durante la terminazione. Una volta terminata la terminazione, riportare la sorgente in modalità di lettura-scrittura. Facoltativamente, è anche possibile impostare il database secondario precedente in modalità di lettura-scrittura.
* Monitoraggio: per verificare lo stato delle operazioni sia per l'origine che per la destinazione della relazione di copia continua, usare il cmdlet **Get-AzureSqlDatabaseOperation** .

## COLLEGAMENTI CORRELATI

[Database SQL di Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Operazioni per i database SQL di Azure](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Interrompi copia database](https://msdn.microsoft.com/en-us/library/dn509573.aspx)

[Cmdlet di database SQL di Azure](./Azure.SQLDatabase.md)

[Get-AzureSqlDatabaseCopy](./Get-AzureSqlDatabaseCopy.md)

[Start-AzureSqlDatabaseCopy](./Start-AzureSqlDatabaseCopy.md)


