---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7F07494-FBCA-4A77-92BF-E0A2D7ACCD21
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc350cdf117ebbf72b023f64895f4c563e73566b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023803"
---
# Start-AzureSqlDatabaseCopy

## Sinossi
Avvia un'operazione di copia di un database SQL di Azure.

## SINTASSI

### ByInputObject
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByInputObjectContinuous
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByDatabaseName
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByDatabaseNameContinuous
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Start-AzureSqlDatabaseCopy** avvia un'operazione di copia unica o un'operazione di copia continua di un database SQL di Azure specifico.
Questo cmdlet non è transazionale.

Il database originale è il database di origine.
La copia è il database secondario o di destinazione.
Per una copia continua, i database di origine e di destinazione non possono trovarsi nello stesso server e i server che ospitano i database di origine e di destinazione devono far parte della stessa sottoscrizione.

Se non specifichi il parametro *ContinuousCopy* , questo cmdlet crea una copia unica del database di origine.
Quando la risposta viene ricevuta, l'operazione può essere ancora in corso.
Puoi monitorare l'operazione usando il cmdlet Get-AzureSqlDatabaseCopy o Get-AzureSqlDatabaseOperation.

Se specifichi *ContinuousCopy* , questo cmdlet crea una copia continua del database di origine.
Quando la risposta viene ricevuta, l'operazione sarà in corso.
Puoi monitorare l'operazione usando **Get-AzureSqlDatabaseCopy** o **Get-AzureSqlDatabaseOperation**.

È possibile creare una copia continua come database online o offline.
La copia continua online viene usata per configurare Active Geo-Replication for Azure SQL database https://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/ .
La copia continua offline viene usata per configurare Geo-Replication standard per il database SQL di Azure https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/ .

## ESEMPI

### Esempio 1: pianificare una copia di un database continuo
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy
```

Questo comando Pianifica una copia continua del database denominata Orders sul server denominato lpqd0zbr8y.
Il comando crea un database di destinazione nel server denominato bk0b8kf658.

### Esempio 2: creare una copia unica nello stesso server
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerDatabase "OrdersCopy"
```

Questo comando crea una copia unica del database denominata Orders sul server denominato lpqd0zbr8y.
Il comando crea una copia denominata OrdersCopy nello stesso server.

### Esempio 3: pianificare una copia del database offline continua
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy -OfflineSecondary
```

Questo comando Pianifica una copia continua del database denominata Orders sul server denominato lpqd0zbr8y.
Questo comando crea un database di destinazione offline nel server denominato bk0b8kf658.

## PARAMETRI

### -ContinuousCopy
Indica che la copia del database sarà una copia continua (un database di replica).
La copia continua non è supportata nello stesso server.
Se questo parametro non viene specificato, viene eseguita una copia unica.
Per una copia unica, i database di origine e partner devono essere nello stesso server.

```yaml
Type: SwitchParameter
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Database
Specifica un oggetto che rappresenta il database SQL di Azure di origine.
Questo parametro accetta l'input della pipeline.

```yaml
Type: Database
Parameter Sets: ByInputObject, ByInputObjectContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
Specifica il nome del database di origine.

```yaml
Type: String
Parameter Sets: ByDatabaseName, ByDatabaseNameContinuous
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

### -OfflineSecondary
Specifica che una copia continua è una copia passiva anziché una copia attiva.
Se il database di origine è un database Standard Edition, questo parametro è obbligatorio.
Se questo parametro viene specificato, deve essere specificato anche *ContinuousCopy* .

```yaml
Type: SwitchParameter
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerDatabase
Specifica il nome del database di destinazione.
Se specifichi il parametro *ContinuousCopy* , il valore di *PartnerDatabase* deve corrispondere al nome del database di origine.
Se non specifichi *ContinuousCopy* , devi specificare un nome per il database di destinazione, che può essere diverso dal nome del database di origine.

```yaml
Type: String
Parameter Sets: ByInputObject, ByDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerServer
Specifica il nome del server che ospita il database di destinazione.
Questo server deve essere nella stessa sottoscrizione di Azure del server di database di origine.

```yaml
Type: String
Parameter Sets: ByInputObject, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: True
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

### Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. database

## OUTPUT

### Microsoft. WindowsAzure. Commands. SqlDatabase. Model. DatabaseCopy

## Note
* Autenticazione: questo cmdlet richiede l'autenticazione basata su certificati. Per un esempio di come usare l'autenticazione basata su certificati per impostare la sottoscrizione corrente, vedere cmdlet New-AzureSqlDatabaseServerContext.
* Monitoraggio: per verificare lo stato di una o più relazioni di copia continue attive nel server, usare il cmdlet **Get-AzureSqlDatabaseCopy** . Per verificare lo stato delle operazioni sia per l'origine che per la destinazione della relazione di copia continua, usare il cmdlet **Get-AzureSqlDatabaseOperation** .

## COLLEGAMENTI CORRELATI

[Database SQL di Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Operazioni per i database SQL di Azure](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Avviare la copia del database](https://msdn.microsoft.com/en-us/library/azure/dn509576.aspx)

[Cmdlet di database SQL di Azure](./Azure.SQLDatabase.md)

[Get-AzureSqlDatabaseCopy](./Get-AzureSqlDatabaseCopy.md)

[Stop-AzureSqlDatabaseCopy](./Stop-AzureSqlDatabaseCopy.md)


