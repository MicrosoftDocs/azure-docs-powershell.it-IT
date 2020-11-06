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
# <span data-ttu-id="b2994-101">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="b2994-101">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="b2994-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b2994-102">SYNOPSIS</span></span>
<span data-ttu-id="b2994-103">Ottiene uno o più backup di conservazione a lungo termine.</span><span class="sxs-lookup"><span data-stu-id="b2994-103">Gets one or more long term retention backups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2994-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b2994-104">SYNTAX</span></span>

### <span data-ttu-id="b2994-105">Posizione (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b2994-105">Location (Default)</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location <String> [-OnlyLatestPerDatabase]
 [[-DatabaseState] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b2994-106">Nomeserver</span><span class="sxs-lookup"><span data-stu-id="b2994-106">ServerName</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location <String> [-ServerName] <String>
 [[-DatabaseName] <String>] [-OnlyLatestPerDatabase] [[-DatabaseState] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2994-107">NomeBackup</span><span class="sxs-lookup"><span data-stu-id="b2994-107">BackupName</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location <String> [-ServerName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2994-108">GetBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="b2994-108">GetBackupByResourceId</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location <String> [-ResourceId] <String> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2994-109">GetBackupsByResourceId</span><span class="sxs-lookup"><span data-stu-id="b2994-109">GetBackupsByResourceId</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location <String> [-ResourceId] <String>
 [-OnlyLatestPerDatabase] [[-DatabaseState] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2994-110">GetBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="b2994-110">GetBackupByInputObject</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2994-111">GetBackupsByInputObject</span><span class="sxs-lookup"><span data-stu-id="b2994-111">GetBackupsByInputObject</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-OnlyLatestPerDatabase]
 [[-DatabaseState] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b2994-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2994-112">DESCRIPTION</span></span>
<span data-ttu-id="b2994-113">Il cmdlet **Get-AzureRmSqlDatabaseLongTermRetentionBackup** ottiene tutti i backup di conservazione a lungo termine per una posizione, un server o un database o ottiene un backup di conservazione a lungo termine specifico.</span><span class="sxs-lookup"><span data-stu-id="b2994-113">The **Get-AzureRmSqlDatabaseLongTermRetentionBackup** cmdlet gets all long term retention backups for a location, server, or database or gets a specific long term retention backup.</span></span>

## <span data-ttu-id="b2994-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b2994-114">EXAMPLES</span></span>

### <span data-ttu-id="b2994-115">Esempio 1: ottenere tutti i backup per una posizione</span><span class="sxs-lookup"><span data-stu-id="b2994-115">Example 1: Get all backups for a location</span></span>
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

<span data-ttu-id="b2994-116">Questo comando ottiene tutti i backup di conservazione a lungo termine per tutti i database (che potrebbero essere vivi o eliminati) in northeurope.</span><span class="sxs-lookup"><span data-stu-id="b2994-116">This command gets all long term retention backups for all databases (which may be alive or deleted) in northeurope.</span></span>

### <span data-ttu-id="b2994-117">Esempio 2: ottenere un backup di conservazione a lungo termine specifico</span><span class="sxs-lookup"><span data-stu-id="b2994-117">Example 2: Get a specific long term retention backup</span></span>
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

<span data-ttu-id="b2994-118">Questo comando ottiene il backup con il nome 601061b7-D10B-46e0-bf77-a2bfb16a6add; 131655666550000000</span><span class="sxs-lookup"><span data-stu-id="b2994-118">This command gets the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="b2994-119">Esempio 3: ottenere tutti i backup di conservazione a lungo termine per un database</span><span class="sxs-lookup"><span data-stu-id="b2994-119">Example 3: Get all long term retention backups for a database</span></span>
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

<span data-ttu-id="b2994-120">Questo comando ottiene tutti i backup di conservazione a lungo termine per Database01</span><span class="sxs-lookup"><span data-stu-id="b2994-120">This command gets all long term retention backups for database01</span></span>

## <span data-ttu-id="b2994-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b2994-121">PARAMETERS</span></span>

### <span data-ttu-id="b2994-122">-BackupName</span><span class="sxs-lookup"><span data-stu-id="b2994-122">-BackupName</span></span>
<span data-ttu-id="b2994-123">Nome del backup.</span><span class="sxs-lookup"><span data-stu-id="b2994-123">The name of the backup.</span></span>

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

### <span data-ttu-id="b2994-124">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b2994-124">-DatabaseName</span></span>
<span data-ttu-id="b2994-125">Nome del database SQL di Azure a cui è associato il backup.</span><span class="sxs-lookup"><span data-stu-id="b2994-125">The name of the Azure SQL Database the backup is from.</span></span>

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

### <span data-ttu-id="b2994-126">-DatabaseState</span><span class="sxs-lookup"><span data-stu-id="b2994-126">-DatabaseState</span></span>
<span data-ttu-id="b2994-127">Lo stato del database di cui si vogliono trovare i backup, attivo, eliminato o tutti.</span><span class="sxs-lookup"><span data-stu-id="b2994-127">The state of the database whose backups you want to find, Alive, Deleted, or All.</span></span>
<span data-ttu-id="b2994-128">Impostazione predefinita per tutti</span><span class="sxs-lookup"><span data-stu-id="b2994-128">Defaults to All</span></span>

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

### <span data-ttu-id="b2994-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2994-129">-DefaultProfile</span></span>
<span data-ttu-id="b2994-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b2994-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2994-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2994-131">-InputObject</span></span>
<span data-ttu-id="b2994-132">Oggetto database per cui ottenere i backup.</span><span class="sxs-lookup"><span data-stu-id="b2994-132">The database object to get backups for.</span></span>

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

### <span data-ttu-id="b2994-133">-Posizione</span><span class="sxs-lookup"><span data-stu-id="b2994-133">-Location</span></span>
<span data-ttu-id="b2994-134">Posizione del server di origine del backup.</span><span class="sxs-lookup"><span data-stu-id="b2994-134">The location of the backups' source server.</span></span>

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

### <span data-ttu-id="b2994-135">-OnlyLatestPerDatabase</span><span class="sxs-lookup"><span data-stu-id="b2994-135">-OnlyLatestPerDatabase</span></span>
<span data-ttu-id="b2994-136">Se ottenere o meno solo il backup più recente per ogni database.</span><span class="sxs-lookup"><span data-stu-id="b2994-136">Whether or not to only get the latest backup per database.</span></span>
<span data-ttu-id="b2994-137">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="b2994-137">Defaults to false.</span></span>

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

### <span data-ttu-id="b2994-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2994-138">-ResourceId</span></span>
<span data-ttu-id="b2994-139">ID risorsa database per cui ottenere i backup.</span><span class="sxs-lookup"><span data-stu-id="b2994-139">The database Resource ID to get backups for.</span></span>

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

### <span data-ttu-id="b2994-140">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="b2994-140">-ServerName</span></span>
<span data-ttu-id="b2994-141">Nome di Azure SQL Server in cui sono inclusi i backup.</span><span class="sxs-lookup"><span data-stu-id="b2994-141">The name of the Azure SQL Server the backups are under.</span></span>

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

### <span data-ttu-id="b2994-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b2994-142">-Confirm</span></span>
<span data-ttu-id="b2994-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2994-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2994-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2994-144">-WhatIf</span></span>
<span data-ttu-id="b2994-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b2994-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2994-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b2994-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2994-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2994-147">CommonParameters</span></span>
<span data-ttu-id="b2994-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2994-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b2994-149">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2994-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2994-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b2994-150">INPUTS</span></span>

### <span data-ttu-id="b2994-151">System. String</span><span class="sxs-lookup"><span data-stu-id="b2994-151">System.String</span></span>
<span data-ttu-id="b2994-152">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="b2994-152">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="b2994-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b2994-153">OUTPUTS</span></span>

### <span data-ttu-id="b2994-154">Microsoft. Azure. Commands. SQL. backup. Model. AzureSqlDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="b2994-154">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="b2994-155">Note</span><span class="sxs-lookup"><span data-stu-id="b2994-155">NOTES</span></span>

## <span data-ttu-id="b2994-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b2994-156">RELATED LINKS</span></span>

[<span data-ttu-id="b2994-157">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="b2994-157">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="b2994-158">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b2994-158">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="b2994-159">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b2994-159">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="b2994-160">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="b2994-160">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
