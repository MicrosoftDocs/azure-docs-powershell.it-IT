---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7F07494-FBCA-4A77-92BF-E0A2D7ACCD21
online version: ''
schema: 2.0.0
ms.openlocfilehash: 35e29655e8447644b6c5449309424595e45ca187
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100413065"
---
# Start-AzureSqlDatabaseCopy

## SYNOPSIS
Avvia un'operazione di copia di un database SQL Azure.

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

## DESCRIZIONE
Il cmdlet **Start-AzureSqlDatabaseCopy** avvia un'operazione di copia unica o di copia continua di uno specifico database SQL Azure.
Questo cmdlet non è transazionale.

Il database originale è il database di origine.
La copia è il database secondario o di destinazione.
Per una copia continua, i database di origine e di destinazione non possono trovarsi nello stesso server e i server che ospitano i database di origine e di destinazione devono far parte della stessa sottoscrizione.

Se non si specifica il parametro *ContinuousCopy,* questo cmdlet crea una copia unica del database di origine.
Una volta ricevuta la risposta, l'operazione può essere ancora in corso.
È possibile monitorare l'operazione usando Get-AzureSqlDatabaseCopy o Get-AzureSqlDatabaseOperation cmdlet.

Se si specifica *ContinuaCopia,* questo cmdlet crea una copia continua del database di origine.
Una volta ricevuta la risposta, l'operazione è in corso.
È possibile monitorare l'operazione usando **Get-AzureSqlDatabaseCopy** **o Get-AzureSqlDatabaseOperation.**

È possibile creare una copia continua come database online o offline.
La copia continua online viene usata per configurare Active Geo-Replication per il database SQL https://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/ Azure.
La copia continua offline viene usata per configurare il servizio Geo-Replication per il database SQL https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/ Azure.

## ESEMPI

### Esempio 1: Pianificare una copia continua del database
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy
```

Questo comando pianifica una copia continua del database denominato Ordini nel server denominato lpqd0zbr8y.
Il comando crea un database di destinazione nel server denominato bk0b8kf658.

### Esempio 2: Creare una copia unica nello stesso server
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerDatabase "OrdersCopy"
```

Questo comando crea una copia unica del database denominato Ordini nel server denominato lpqd0zbr8y.
Il comando crea una copia denominata OrdersCopy nello stesso server.

### Esempio 3: Pianificare una copia continua del database offline
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy -OfflineSecondary
```

Questo comando pianifica una copia continua del database denominato Ordini nel server denominato lpqd0zbr8y.
Questo comando crea un database di destinazione offline nel server denominato bk0b8kf658.

## PARAMETERS

### -ContinuousCopy
Indica che la copia del database sarà una copia continua (un database di replica).
La copia continua non è supportata all'interno dello stesso server.
Se questo parametro non è specificato, viene eseguita una copia unica.
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
Specifica un oggetto che rappresenta l'origine SQL database di Azure.
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

### -OfflineSecondary
Specifica che una copia continua è una copia passiva anziché una copia attiva.
Se il database di origine è un database Standard Edition, questo parametro è obbligatorio.
Se si specifica questo parametro, *deve essere specificata anche* la copia continua.

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
Se si specifica il *parametro ContinuousCopy,* il valore di *PartnerDatabase* deve corrispondere al nome del database di origine.
Se non si specifica *ContinuousCopy,* è necessario specificare un nome per il database di destinazione, che può essere diverso dal nome del database di origine.

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

### Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database

## OUTPUT

### Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy

## NOTE
* Autenticazione: questo cmdlet richiede l'autenticazione basata su certificato. Per un esempio su come usare l'autenticazione basata su certificato per impostare l'abbonamento corrente, vedere New-AzureSqlDatabaseServerContext cmdlet.
* Monitoraggio: per verificare lo stato di una o più relazioni di copia continue attive nel server, usare il cmdlet **Get-AzureSqlDatabaseCopy.** Per verificare lo stato delle operazioni sia nell'origine che nella destinazione della relazione di copia continua, usare il cmdlet **Get-AzureSqlDatabaseOperation.**

## COLLEGAMENTI CORRELATI

[Azure SQL Database](https://azure.microsoft.com/en-us/services/sql-database/)

[Operazioni per i database SQL Azure](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Avvia copia database](https://msdn.microsoft.com/en-us/library/azure/dn509576.aspx)



[Get-AzureSqlDatabaseCopy](./Get-AzureSqlDatabaseCopy.md)

[Stop-AzureSqlDatabaseCopy](./Stop-AzureSqlDatabaseCopy.md)


