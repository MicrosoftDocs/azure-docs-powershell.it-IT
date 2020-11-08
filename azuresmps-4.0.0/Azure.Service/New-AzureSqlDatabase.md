---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F4FE79DB-B481-49BD-A33B-7C642A136890
online version: ''
schema: 2.0.0
ms.openlocfilehash: 588fcf73c258364e41117eed05c62de7eaa231e9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023931"
---
# New-AzureSqlDatabase

## Sinossi
Crea un database SQL di Azure.

## SINTASSI

### ByConnectionContext
```
New-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String>
 [-Collation <String>] [-Edition <DatabaseEdition>] [-ServiceObjective <ServiceObjective>] [-MaxSizeGB <Int32>]
 [-MaxSizeBytes <Int64>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByServerName
```
New-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-Collation <String>]
 [-Edition <DatabaseEdition>] [-ServiceObjective <ServiceObjective>] [-MaxSizeGB <Int32>]
 [-MaxSizeBytes <Int64>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzureSqlDatabase** crea un database SQL di Azure.
Puoi specificare il server usando un contesto di connessione del server di database SQL di Azure creato usando il cmdlet **New-AzureSqlDatabaseServerContext** .
In alternativa, se specifichi il nome del server, il cmdlet usa le informazioni correnti sull'abbonamento a Azure per autenticare la richiesta di accesso al server.

Quando si crea un nuovo database specificando un server di database SQL di Azure, il cmdlet **New-AzureSqlDatabase** crea un contesto di connessione temporaneo usando il nome del server specificato e le informazioni correnti sull'abbonamento a Azure per eseguire l'operazione.

## ESEMPI

### Esempio 1: creare un database
```
PS C:\> $Database01 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01" -Edition "Business" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

Questo comando crea un database SQL di Azure denominato database1, per il contesto di connessione del server di database SQL di Azure $Context.

### Esempio 2: creare un database nell'abbonamento corrente
```
PS C:\> $Database01 = New-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01" -Edition "Business" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

Questo esempio crea un database denominato database1, nel server di database SQL di Azure specificato denominato lpqd0zbr8y.
Il cmdlet usa le informazioni correnti sull'abbonamento a Azure per autenticare la richiesta di accesso al server.

## PARAMETRI

### -Regole di confronto
Specifica una regola di confronto per il nuovo database.

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

### -ConnectionContext
Specifica il contesto di connessione di un server in cui questo cmdlet crea un database.

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
Specifica il nome del nuovo database.

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

### -Edition
Specifica l'edizione per il nuovo database SQL di Azure.
I valori validi sono: 

- Nessuno
- Web
- Business
- Base
- Standard
-  Premium

Il valore predefinito è Web.

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Consente di completare l'azione senza richiedere conferma all'utente.

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

### -MaxSizeBytes
Specifica la dimensione massima del database in byte.
Puoi specificare questo parametro o il parametro *MaxSizeGB* .
Vedere la descrizione del parametro *MaxSizeGB* per i valori accettabili in base a Edition.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxSizeGB
Specifica la dimensione massima del database in gigabyte.
Puoi specificare questo parametro o il parametro *MaxSizeBytes* .
I valori accettabili variano in base all'edizione.

Valori di base dell'edizione: 1 o 2

Valori standard dell'edizione: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200 o 250

Valori di edizione Premium: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300, 400 o 500

Valori di Web Edition: 1 o 5

Valori di Business Edition: 10, 20, 30, 40, 50, 100 o 150

```yaml
Type: Int32
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

### -Nomeserver
Specifica il nome del server di database SQL di Azure che contiene il nuovo database.

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

### -ServiceObjective
Specifica un oggetto che rappresenta il nuovo obiettivo del servizio (livello di prestazioni) per il database.
Questo valore rappresenta il livello di risorse assegnate a questo database.
I valori validi sono: 

Basic: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c standard (S0): f1173c43-91bd-4AAA-973C-54e79e15235b standard (S1): 1b1ebd4d-D903-4baa-97f9-4ea675f5e928 standard (S2): 455330e1-00cd-488b-B5FA-177c226f28b7 * standard (S3): 789681b8-CA10-4EB0-bdf2-e0b050601b40 Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0 Premium (P3): a7c4c615-CFB1-464B-b252-925be0a19446

* Standard (S3) fa parte del più recente aggiornamento di database SQL V12 (Preview).
Per altre informazioni, vedere Novità di Azure SQL database V12 Preview https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/ .

```yaml
Type: ServiceObjective
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

## OUTPUT

### Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. database

## Note
* Per eliminare un database creato da **New-AzureSqlDatabase** , usare il cmdlet Remove-AzureSqlDatabase.

## COLLEGAMENTI CORRELATI

[Database SQL di Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Creare un database](https://msdn.microsoft.com/en-us/library/azure/dn505701.aspx)

[Operazioni per i database SQL di Azure](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)

[New-AzureSqlDatabaseServerContext](./New-AzureSqlDatabaseServerContext.md)

[Remove-AzureSqlDatabase](./Remove-AzureSqlDatabase.md)

[Set-AzureSqlDatabase](./Set-AzureSqlDatabase.md)


