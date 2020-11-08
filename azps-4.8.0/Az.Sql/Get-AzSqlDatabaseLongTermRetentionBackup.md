---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: e97143f282bc01bbdd9c5d6186f0ccb5532b1df1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189321"
---
# <span data-ttu-id="2fc47-101">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="2fc47-101">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="2fc47-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2fc47-102">SYNOPSIS</span></span>
<span data-ttu-id="2fc47-103">Ottiene uno o più backup di conservazione a lungo termine.</span><span class="sxs-lookup"><span data-stu-id="2fc47-103">Gets one or more long term retention backups.</span></span>

## <span data-ttu-id="2fc47-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2fc47-104">SYNTAX</span></span>

### <span data-ttu-id="2fc47-105">Posizione (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2fc47-105">Location (Default)</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceGroupName <String>]
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fc47-106">Nomeserver</span><span class="sxs-lookup"><span data-stu-id="2fc47-106">ServerName</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String> [-DatabaseName <String>]
 [-ResourceGroupName <String>] [-OnlyLatestPerDatabase] [-DatabaseState <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fc47-107">NomeBackup</span><span class="sxs-lookup"><span data-stu-id="2fc47-107">BackupName</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String> -DatabaseName <String>
 [-BackupName] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fc47-108">GetBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="2fc47-108">GetBackupByResourceId</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fc47-109">GetBackupsByResourceId</span><span class="sxs-lookup"><span data-stu-id="2fc47-109">GetBackupsByResourceId</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fc47-110">GetBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="2fc47-110">GetBackupByInputObject</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fc47-111">GetBackupsByInputObject</span><span class="sxs-lookup"><span data-stu-id="2fc47-111">GetBackupsByInputObject</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fc47-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2fc47-112">DESCRIPTION</span></span>
<span data-ttu-id="2fc47-113">Il cmdlet **Get-AzSqlDatabaseLongTermRetentionBackup** ottiene tutti i backup di conservazione a lungo termine per una posizione, un server o un database o ottiene un backup di conservazione a lungo termine specifico.</span><span class="sxs-lookup"><span data-stu-id="2fc47-113">The **Get-AzSqlDatabaseLongTermRetentionBackup** cmdlet gets all long term retention backups for a location, server, or database or gets a specific long term retention backup.</span></span>

## <span data-ttu-id="2fc47-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2fc47-114">EXAMPLES</span></span>

### <span data-ttu-id="2fc47-115">Esempio 1: ottenere tutti i backup per una posizione</span><span class="sxs-lookup"><span data-stu-id="2fc47-115">Example 1: Get all backups for a location</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM

BackupExpirationTime : 3/22/2018 11:43:18 PM
BackupName           : 55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
BackupTime           : 3/15/2018 11:43:18 PM
DatabaseName         : database02
DatabaseDeletionTime : 3/18/2018 4:36:00 PM
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server02/longTermRetentionDatabases/database02/longTermRetentionBackups/55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
ServerName           : server02
ServerCreateTime     : 2/28/2018 12:12:19 AM
```

<span data-ttu-id="2fc47-116">Questo comando ottiene tutti i backup di conservazione a lungo termine per tutti i database (che potrebbero essere vivi o eliminati) in northeurope, il gruppo di risorse verrà impostato solo se il server è attivo.</span><span class="sxs-lookup"><span data-stu-id="2fc47-116">This command gets all long term retention backups for all databases (which may be alive or deleted) in northeurope, resource group will be set only if server is live.</span></span>

### <span data-ttu-id="2fc47-117">Esempio 2: ottenere tutti i backup per una posizione in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="2fc47-117">Example 2: Get all backups for a location under a resource group</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ResourceGroup resourceGroup01


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="2fc47-118">Questo comando ottiene tutti i backup di conservazione a lungo termine per tutti i database (che potrebbero essere vivi o eliminati) in un gruppo di risorse in northeurope.</span><span class="sxs-lookup"><span data-stu-id="2fc47-118">This command gets all long term retention backups for all databases (which may be alive or deleted) under a resource group in northeurope.</span></span>

### <span data-ttu-id="2fc47-119">Esempio 3: ottenere un backup di conservazione a lungo termine specifico</span><span class="sxs-lookup"><span data-stu-id="2fc47-119">Example 3: Get a specific long term retention backup</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000"


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="2fc47-120">Questo comando ottiene il backup con il nome 601061b7-D10B-46e0-bf77-a2bfb16a6add; 131655666550000000</span><span class="sxs-lookup"><span data-stu-id="2fc47-120">This command gets the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="2fc47-121">Esempio 4: ottenere tutti i backup di conservazione a lungo termine per un database</span><span class="sxs-lookup"><span data-stu-id="2fc47-121">Example 4: Get all long term retention backups for a database</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Get-AzSqlDatabaseLongTermRetentionBackup


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="2fc47-122">Questo comando ottiene tutti i backup di conservazione a lungo termine per Database01</span><span class="sxs-lookup"><span data-stu-id="2fc47-122">This command gets all long term retention backups for database01</span></span>

### <span data-ttu-id="2fc47-123">Esempio 5: ottenere backup di conservazione a lungo termine tramite filtro</span><span class="sxs-lookup"><span data-stu-id="2fc47-123">Example 5: Get long term retention backups using filtering</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7*"

BackupExpirationTime : 3/22/2018 11:43:18 PM
BackupName           : 601061b7-164c-4a4a-88e5-7158d092d503;131656309980000000
BackupTime           : 3/15/2018 11:43:18 PM
DatabaseName         : database02
DatabaseDeletionTime : 3/18/2018 4:36:00 PM
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database02/longTermRetentionBackups/601061b7-164c-4a4a-88e5-7158d092d503;131656309980000000
ServerName           : server01
ServerCreateTime     : 2/28/2018 12:12:19 AM

BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="2fc47-124">Questo comando ottiene tutti i backup con il nome che inizia con "601061b7"</span><span class="sxs-lookup"><span data-stu-id="2fc47-124">This command gets all backups with name that starts with "601061b7"</span></span>

## <span data-ttu-id="2fc47-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2fc47-125">PARAMETERS</span></span>

### <span data-ttu-id="2fc47-126">-BackupName</span><span class="sxs-lookup"><span data-stu-id="2fc47-126">-BackupName</span></span>
<span data-ttu-id="2fc47-127">Nome del backup.</span><span class="sxs-lookup"><span data-stu-id="2fc47-127">The name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: BackupName, GetBackupByResourceId, GetBackupByInputObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fc47-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2fc47-128">-DatabaseName</span></span>
<span data-ttu-id="2fc47-129">Nome del database SQL di Azure a cui è associato il backup.</span><span class="sxs-lookup"><span data-stu-id="2fc47-129">The name of the Azure SQL Database the backup is from.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: BackupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fc47-130">-DatabaseState</span><span class="sxs-lookup"><span data-stu-id="2fc47-130">-DatabaseState</span></span>
<span data-ttu-id="2fc47-131">Lo stato del database di cui si vogliono trovare i backup, attivo, eliminato o tutti.</span><span class="sxs-lookup"><span data-stu-id="2fc47-131">The state of the database whose backups you want to find, Alive, Deleted, or All.</span></span>
<span data-ttu-id="2fc47-132">Impostazione predefinita per tutti</span><span class="sxs-lookup"><span data-stu-id="2fc47-132">Defaults to All</span></span>

```yaml
Type: System.String
Parameter Sets: Location, ServerName, GetBackupsByResourceId, GetBackupsByInputObject
Aliases:
Accepted values: All, Deleted, Live

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fc47-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fc47-133">-DefaultProfile</span></span>
<span data-ttu-id="2fc47-134">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2fc47-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fc47-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2fc47-135">-InputObject</span></span>
<span data-ttu-id="2fc47-136">Oggetto database per cui ottenere i backup.</span><span class="sxs-lookup"><span data-stu-id="2fc47-136">The database object to get backups for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: GetBackupByInputObject, GetBackupsByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2fc47-137">-Posizione</span><span class="sxs-lookup"><span data-stu-id="2fc47-137">-Location</span></span>
<span data-ttu-id="2fc47-138">Posizione del server di origine del backup.</span><span class="sxs-lookup"><span data-stu-id="2fc47-138">The location of the backups' source server.</span></span>

```yaml
Type: System.String
Parameter Sets: Location, ServerName, BackupName, GetBackupByResourceId, GetBackupsByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fc47-139">-OnlyLatestPerDatabase</span><span class="sxs-lookup"><span data-stu-id="2fc47-139">-OnlyLatestPerDatabase</span></span>
<span data-ttu-id="2fc47-140">Se ottenere o meno solo il backup più recente per ogni database.</span><span class="sxs-lookup"><span data-stu-id="2fc47-140">Whether or not to only get the latest backup per database.</span></span>
<span data-ttu-id="2fc47-141">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="2fc47-141">Defaults to false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Location, ServerName, GetBackupsByResourceId, GetBackupsByInputObject
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fc47-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fc47-142">-ResourceGroupName</span></span>
<span data-ttu-id="2fc47-143">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2fc47-143">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Location, ServerName, BackupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fc47-144">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2fc47-144">-ResourceId</span></span>
<span data-ttu-id="2fc47-145">ID risorsa database per cui ottenere i backup.</span><span class="sxs-lookup"><span data-stu-id="2fc47-145">The database Resource ID to get backups for.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBackupByResourceId, GetBackupsByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fc47-146">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="2fc47-146">-ServerName</span></span>
<span data-ttu-id="2fc47-147">Nome di Azure SQL Server in cui sono inclusi i backup.</span><span class="sxs-lookup"><span data-stu-id="2fc47-147">The name of the Azure SQL Server the backups are under.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName, BackupName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fc47-148">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2fc47-148">-Confirm</span></span>
<span data-ttu-id="2fc47-149">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2fc47-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fc47-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fc47-150">-WhatIf</span></span>
<span data-ttu-id="2fc47-151">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2fc47-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fc47-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2fc47-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fc47-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fc47-153">CommonParameters</span></span>
<span data-ttu-id="2fc47-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fc47-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fc47-155">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2fc47-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fc47-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2fc47-156">INPUTS</span></span>

### <span data-ttu-id="2fc47-157">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="2fc47-157">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="2fc47-158">System. String</span><span class="sxs-lookup"><span data-stu-id="2fc47-158">System.String</span></span>

## <span data-ttu-id="2fc47-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2fc47-159">OUTPUTS</span></span>

### <span data-ttu-id="2fc47-160">Microsoft. Azure. Commands. SQL. backup. Model. AzureSqlDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="2fc47-160">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="2fc47-161">Note</span><span class="sxs-lookup"><span data-stu-id="2fc47-161">NOTES</span></span>

## <span data-ttu-id="2fc47-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2fc47-162">RELATED LINKS</span></span>

[<span data-ttu-id="2fc47-163">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="2fc47-163">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="2fc47-164">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2fc47-164">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="2fc47-165">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2fc47-165">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="2fc47-166">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="2fc47-166">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)