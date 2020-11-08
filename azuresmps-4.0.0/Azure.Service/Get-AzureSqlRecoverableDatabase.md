---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 83E8DAD8-151A-408D-819F-274CB813ABDA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6f9a5753fdf4f87afc6baacbe9fc4c33c9be08ef
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94030021"
---
# Get-AzureSqlRecoverableDatabase

## Sinossi
Ottiene i database recuperabili da un server specificato.

## SINTASSI

### AllDatabasesOnGivenServer (impostazione predefinita)
```
Get-AzureSqlRecoverableDatabase -ServerName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### GivenDatabaseOnGivenServer
```
Get-AzureSqlRecoverableDatabase -ServerName <String> -DatabaseName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### GivenDatabaseObject
```
Get-AzureSqlRecoverableDatabase -Database <RecoverableDatabase> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureSqlRecoverableDatabase** ottiene i database recuperabili da un server specificato.
Questo cmdlet ottiene uno specifico database reversibile o tutti i database recuperabili in un server.

## ESEMPI

### Esempio 1: ottenere tutti i database recuperabili
```
PS C:\> Get-AzureSqlRecoverableDatabase -ServerName "Server01"
```

Questo comando consente di ottenere tutti i database recuperabili nel server denominato Server01.

### Esempio 2: ottenere uno specifico database reversibile
```
PS C:\> Get-AzureSqlRecoverableDatabase -ServerName "Server01" -DatabaseName "Database17"
```

Questo comando ottiene Recupera il database denominato Database17 nel server denominato Server01.

## PARAMETRI

### -Database
Specifica un oggetto che rappresenta il database recuperabile ottenuto da questo cmdlet.

```yaml
Type: RecoverableDatabase
Parameter Sets: GivenDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
Specifica il nome del database recuperabile ottenuto da questo cmdlet.

```yaml
Type: String
Parameter Sets: GivenDatabaseOnGivenServer
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
Specifica il nome del server da cui questo cmdlet ottiene i database recuperabili.

```yaml
Type: String
Parameter Sets: AllDatabasesOnGivenServer, GivenDatabaseOnGivenServer
Aliases: 

Required: True
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

### IEnumerable\<Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase\>

## Note
* Per eseguire questo cmdlet, è necessario usare l'autenticazione basata su certificati. Eseguire i comandi seguenti nel computer in cui eseguire questo cmdlet: 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## COLLEGAMENTI CORRELATI

[Database SQL di Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Ottenere un database reversibile](https://msdn.microsoft.com/en-us/library/azure/dn800985.aspx)

[Operazioni per i database SQL di Azure](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Start-AzureSqlDatabaseRecovery](./Start-AzureSqlDatabaseRecovery.md)


