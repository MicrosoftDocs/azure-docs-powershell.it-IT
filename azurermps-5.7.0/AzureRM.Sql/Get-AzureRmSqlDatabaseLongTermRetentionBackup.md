---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatalongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: da3b47923f39e6910566a210ddbd325d9da76ca7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507887"
---
# Get-AzureRmSqlDatabaseLongTermRetentionBackup

## Sinossi
Ottiene uno o più backup di conservazione a lungo termine.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### Posizione (impostazione predefinita)
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location <String> [-OnlyLatestPerDatabase]
 [[-DatabaseState] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Nomeserver
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location <String> [-ServerName] <String>
 [[-DatabaseName] <String>] [-OnlyLatestPerDatabase] [[-DatabaseState] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NomeBackup
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location <String> [-ServerName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### GetBackupByResourceId
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location <String> [-ResourceId] <String> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### GetBackupsByResourceId
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location <String> [-ResourceId] <String>
 [-OnlyLatestPerDatabase] [[-DatabaseState] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### GetBackupByInputObject
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### GetBackupsByInputObject
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-OnlyLatestPerDatabase]
 [[-DatabaseState] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureRmSqlDatabaseLongTermRetentionBackup** ottiene tutti i backup di conservazione a lungo termine per una posizione, un server o un database o ottiene un backup di conservazione a lungo termine specifico.

## ESEMPI

### Esempio 1: ottenere tutti i backup per una posizione
```powershell
PS C:\> Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location northeurope


BackupExpirationTime : 3/22/2018 11:43:18 PM
BackupName           : 55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
BackupTime           : 3/15/2018 11:43:18 PM
DatabaseName         : database02
DatabaseDeletionTime : 3/18/2018 4:36:00 PM
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server02/longTermRetentionDatabases/database02/longTermRetentionBackups/55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
ServerName           : server02
ServerCreateTime     : 2/28/2018 12:12:19 AM

BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

Questo comando ottiene tutti i backup di conservazione a lungo termine per tutti i database (che potrebbero essere vivi o eliminati) in northeurope.

### Esempio 2: ottenere un backup di conservazione a lungo termine specifico
```powershell
PS C:\> Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000"


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

Questo comando ottiene il backup con il nome 601061b7-D10B-46e0-bf77-a2bfb16a6add; 131655666550000000

### Esempio 3: ottenere tutti i backup di conservazione a lungo termine per un database
```powershell
PS C:\> Get-AzureRmSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Get-AzureRmSqlDatabaseLongTermRetentionBackup


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

Questo comando ottiene tutti i backup di conservazione a lungo termine per Database01

## PARAMETRI

### -BackupName
Nome del backup.

```yaml
Type: String
Parameter Sets: BackupName, GetBackupByResourceId, GetBackupByInputObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DatabaseName
Nome del database SQL di Azure a cui è associato il backup.

```yaml
Type: String
Parameter Sets: ServerName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: BackupName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseState
Lo stato del database di cui si vogliono trovare i backup, attivo, eliminato o tutti.
Impostazione predefinita per tutti

```yaml
Type: String
Parameter Sets: Location, ServerName, GetBackupsByResourceId, GetBackupsByInputObject
Aliases:
Accepted values: All, Deleted, Live

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Oggetto database per cui ottenere i backup.

```yaml
Type: AzureSqlDatabaseModel
Parameter Sets: GetBackupByInputObject, GetBackupsByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Posizione
Posizione del server di origine del backup.

```yaml
Type: String
Parameter Sets: Location, ServerName, BackupName, GetBackupByResourceId, GetBackupsByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OnlyLatestPerDatabase
Se ottenere o meno solo il backup più recente per ogni database.
Il valore predefinito è false.

```yaml
Type: SwitchParameter
Parameter Sets: Location, ServerName, GetBackupsByResourceId, GetBackupsByInputObject
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
ID risorsa database per cui ottenere i backup.

```yaml
Type: String
Parameter Sets: GetBackupByResourceId, GetBackupsByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nomeserver
Nome di Azure SQL Server in cui sono inclusi i backup.

```yaml
Type: String
Parameter Sets: ServerName, BackupName
Aliases:

Required: True
Position: 1
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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.
Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### System. String
Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel

## OUTPUT

### Microsoft. Azure. Commands. SQL. backup. Model. AzureSqlDatabaseLongTermRetentionBackupModel

## Note

## COLLEGAMENTI CORRELATI

[Remove-AzureRmSqlDatabaseLongTermRetentionBackup](./Remove-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy](./Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy](./Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[Documentazione di database SQL](https://docs.microsoft.com/azure/sql-database/)
