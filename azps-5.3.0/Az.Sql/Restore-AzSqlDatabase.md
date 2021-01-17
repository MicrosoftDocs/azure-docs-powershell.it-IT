---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 72E0E558-74D7-4A50-A975-FA7D0C0B301E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/restore-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlDatabase.md
ms.openlocfilehash: c4bca877138f07c5bd3b0b5303ab09c39eb700a2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376501"
---
# <span data-ttu-id="95044-101">Restore-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="95044-101">Restore-AzSqlDatabase</span></span>

## <span data-ttu-id="95044-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="95044-102">SYNOPSIS</span></span>
<span data-ttu-id="95044-103">Ripristina un database SQL.</span><span class="sxs-lookup"><span data-stu-id="95044-103">Restores a SQL database.</span></span>

## <span data-ttu-id="95044-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="95044-104">SYNTAX</span></span>

### <span data-ttu-id="95044-105">FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="95044-105">FromPointInTimeBackup</span></span>
```
Restore-AzSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>] [-BackupStorageRedundancy <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="95044-106">FromPointInTimeBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="95044-106">FromPointInTimeBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String>
 -VCore <Int32> [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95044-107">FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="95044-107">FromDeletedDatabaseBackup</span></span>
```
Restore-AzSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> [-Edition <String>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95044-108">FromDeletedDatabaseBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="95044-108">FromDeletedDatabaseBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob]
 -ComputeGeneration <String> -VCore <Int32> [-LicenseType <String>] [-BackupStorageRedundancy <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="95044-109">FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="95044-109">FromGeoBackup</span></span>
```
Restore-AzSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String> -TargetDatabaseName <String>
 [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob]
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95044-110">FromGeoBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="95044-110">FromGeoBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String> -TargetDatabaseName <String>
 -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32> [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95044-111">FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="95044-111">FromLongTermRetentionBackup</span></span>
```
Restore-AzSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>]
 [-AsJob] [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95044-112">FromLongTermRetentionBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="95044-112">FromLongTermRetentionBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32>
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95044-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95044-113">DESCRIPTION</span></span>
<span data-ttu-id="95044-114">Il cmdlet **Restore-AzSqlDatabase** ripristina un database SQL da un backup Geo-ridondante, un backup di un database eliminato, un backup a lungo termine o un momento in un database dinamico.</span><span class="sxs-lookup"><span data-stu-id="95044-114">The **Restore-AzSqlDatabase** cmdlet restores a SQL database from a geo-redundant backup, a backup of a deleted database, a long term retention backup, or a point in time in a live database.</span></span>
<span data-ttu-id="95044-115">Il database ripristinato viene creato come nuovo database.</span><span class="sxs-lookup"><span data-stu-id="95044-115">The restored database is created as a new database.</span></span>
<span data-ttu-id="95044-116">Puoi creare un database SQL elastico impostando il parametro *ElasticPoolName* su un pool elastico esistente.</span><span class="sxs-lookup"><span data-stu-id="95044-116">You can create an elastic SQL database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="95044-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="95044-117">EXAMPLES</span></span>

### <span data-ttu-id="95044-118">Esempio 1: ripristinare un database da un momento</span><span class="sxs-lookup"><span data-stu-id="95044-118">Example 1: Restore a database from a point in time</span></span>
```
PS C:\>$Database = Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -Edition "Standard" -ServiceObjectiveName "S2"
```

<span data-ttu-id="95044-119">Il primo comando ottiene il database SQL denominato Database01 e lo archivia nella variabile $Database.</span><span class="sxs-lookup"><span data-stu-id="95044-119">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="95044-120">Il secondo comando Ripristina il database in $Database dal backup point-in-Time specificato al database denominato RestoredDatabase.</span><span class="sxs-lookup"><span data-stu-id="95044-120">The second command restores the database in $Database from the specified point-in-time backup to the database named RestoredDatabase.</span></span>

### <span data-ttu-id="95044-121">Esempio 2: ripristinare un database da un momento a un pool elastico</span><span class="sxs-lookup"><span data-stu-id="95044-121">Example 2: Restore a database from a point in time to an elastic pool</span></span>
```
PS C:\>$Database = Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="95044-122">Il primo comando ottiene il database SQL denominato Database01 e lo archivia nella variabile $Database.</span><span class="sxs-lookup"><span data-stu-id="95044-122">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="95044-123">Il secondo comando Ripristina il database in $Database dal backup point-in-Time specificato al database SQL denominato RestoredDatabase nel pool elastico denominato elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="95044-123">The second command restores the database in $Database from the specified point-in-time backup to the SQL database named RestoredDatabase in the elastic pool named elasticpool01.</span></span>

### <span data-ttu-id="95044-124">Esempio 3: ripristinare un database eliminato</span><span class="sxs-lookup"><span data-stu-id="95044-124">Example 3: Restore a deleted database</span></span>
```
PS C:\>$DeletedDatabase = Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -Edition "Standard" -ServiceObjectiveName "S2" -PointInTime UTCDateTime
```

<span data-ttu-id="95044-125">Il primo comando ottiene il backup del database eliminato che si vuole ripristinare tramite [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span><span class="sxs-lookup"><span data-stu-id="95044-125">The first command gets the deleted database backup that you want to restore by using [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="95044-126">Il secondo comando avvia il ripristino dal backup del database eliminato usando il cmdlet [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="95044-126">The second command starts the restore from the deleted database backup by using the [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md) cmdlet.</span></span> <span data-ttu-id="95044-127">Se il parametro-PointInTime non viene specificato, il database verrà ripristinato all'ora di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="95044-127">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="95044-128">Esempio 4: ripristinare un database eliminato in un pool elastico</span><span class="sxs-lookup"><span data-stu-id="95044-128">Example 4: Restore a deleted database into an elastic pool</span></span>
```
PS C:\>$DeletedDatabase = Get-AzSqlDeletedDatabaseBackup -ResourceGroupName $resourceGroupName -ServerName $sqlServerName -DatabaseName 'DatabaseToRestore'
PS C:\> Restore-AzSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -ElasticPoolName "elasticpool01" -PointInTime UTCDateTime
```

<span data-ttu-id="95044-129">Il primo comando ottiene il backup del database eliminato che si vuole ripristinare tramite [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span><span class="sxs-lookup"><span data-stu-id="95044-129">The first command gets the deleted database backup that you want to restore by using [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="95044-130">Il secondo comando avvia il ripristino dal backup del database eliminato tramite [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md).</span><span class="sxs-lookup"><span data-stu-id="95044-130">The second command starts the restore from the deleted database backup by using [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md).</span></span> <span data-ttu-id="95044-131">Se il parametro-PointInTime non viene specificato, il database verrà ripristinato all'ora di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="95044-131">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="95044-132">Esempio 5: Geo-Restore un database</span><span class="sxs-lookup"><span data-stu-id="95044-132">Example 5: Geo-Restore a database</span></span>
```
PS C:\>$GeoBackup = Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromGeoBackup -ResourceGroupName "TargetResourceGroup" -ServerName "TargetServer" -TargetDatabaseName "RestoredDatabase" -ResourceId $GeoBackup.ResourceID -Edition "Standard" -RequestedServiceObjectiveName "S2"
```

<span data-ttu-id="95044-133">Il primo comando ottiene il backup Geo-ridondante per il database denominato Database01 e lo archivia nella variabile $GeoBackup.</span><span class="sxs-lookup"><span data-stu-id="95044-133">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>
<span data-ttu-id="95044-134">Il secondo comando Ripristina il backup in $GeoBackup al database SQL denominato RestoredDatabase.</span><span class="sxs-lookup"><span data-stu-id="95044-134">The second command restores the backup in $GeoBackup to the SQL database named RestoredDatabase.</span></span>

## <span data-ttu-id="95044-135">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="95044-135">PARAMETERS</span></span>

### <span data-ttu-id="95044-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95044-136">-AsJob</span></span>
<span data-ttu-id="95044-137">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="95044-137">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95044-138">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="95044-138">-BackupStorageRedundancy</span></span>
<span data-ttu-id="95044-139">Ridondanza dello spazio di archiviazione di backup utilizzata per archiviare i backup per il database SQL.</span><span class="sxs-lookup"><span data-stu-id="95044-139">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="95044-140">Le opzioni disponibili sono: locale, zona e geo.</span><span class="sxs-lookup"><span data-stu-id="95044-140">Options are: Local, Zone and Geo.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Zone, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95044-141">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="95044-141">-ComputeGeneration</span></span>
<span data-ttu-id="95044-142">Generazione di Compute da assegnare al database ripristinato</span><span class="sxs-lookup"><span data-stu-id="95044-142">The compute generation to assign to the restored database</span></span>

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackupWithVcore, FromDeletedDatabaseBackupWithVcore, FromGeoBackupWithVcore, FromLongTermRetentionBackupWithVcore
Aliases: Family

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95044-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95044-143">-DefaultProfile</span></span>
<span data-ttu-id="95044-144">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="95044-144">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="95044-145">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="95044-145">-DeletionDate</span></span>
<span data-ttu-id="95044-146">Specifica la data di eliminazione come oggetto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="95044-146">Specifies the deletion date as a **DateTime** object.</span></span>
<span data-ttu-id="95044-147">Per ottenere un oggetto **DateTime** , usa il cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="95044-147">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: FromDeletedDatabaseBackup, FromDeletedDatabaseBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95044-148">-Edition</span><span class="sxs-lookup"><span data-stu-id="95044-148">-Edition</span></span>
<span data-ttu-id="95044-149">Specifica l'edizione del database SQL.</span><span class="sxs-lookup"><span data-stu-id="95044-149">Specifies the edition of the SQL database.</span></span>
<span data-ttu-id="95044-150">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="95044-150">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="95044-151">Nessuno</span><span class="sxs-lookup"><span data-stu-id="95044-151">None</span></span>
- <span data-ttu-id="95044-152">Base</span><span class="sxs-lookup"><span data-stu-id="95044-152">Basic</span></span>
- <span data-ttu-id="95044-153">Standard</span><span class="sxs-lookup"><span data-stu-id="95044-153">Standard</span></span>
- <span data-ttu-id="95044-154">Premium</span><span class="sxs-lookup"><span data-stu-id="95044-154">Premium</span></span>
- <span data-ttu-id="95044-155">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="95044-155">DataWarehouse</span></span>
- <span data-ttu-id="95044-156">Gratuito</span><span class="sxs-lookup"><span data-stu-id="95044-156">Free</span></span>
- <span data-ttu-id="95044-157">Tratto</span><span class="sxs-lookup"><span data-stu-id="95044-157">Stretch</span></span>
- <span data-ttu-id="95044-158">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="95044-158">GeneralPurpose</span></span>
- <span data-ttu-id="95044-159">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="95044-159">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackup, FromDeletedDatabaseBackup, FromGeoBackup, FromLongTermRetentionBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackupWithVcore, FromDeletedDatabaseBackupWithVcore, FromGeoBackupWithVcore, FromLongTermRetentionBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95044-160">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="95044-160">-ElasticPoolName</span></span>
<span data-ttu-id="95044-161">Specifica il nome del pool elastico in cui inserire il database SQL.</span><span class="sxs-lookup"><span data-stu-id="95044-161">Specifies the name of the elastic pool in which to put the SQL database.</span></span>

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackup, FromDeletedDatabaseBackup, FromGeoBackup, FromLongTermRetentionBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95044-162">-FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="95044-162">-FromDeletedDatabaseBackup</span></span>
<span data-ttu-id="95044-163">Indica che questo cmdlet ripristina un database da un backup di un database SQL eliminato.</span><span class="sxs-lookup"><span data-stu-id="95044-163">Indicates that this cmdlet restores a database from a backup of a deleted SQL database.</span></span>
<span data-ttu-id="95044-164">Puoi usare il cmdlet Get-AzSqlDeletedDatabaseBackup per ottenere il backup di un database SQL eliminato.</span><span class="sxs-lookup"><span data-stu-id="95044-164">You can use the Get-AzSqlDeletedDatabaseBackup cmdlet to get the backup of a deleted SQL database.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromDeletedDatabaseBackup, FromDeletedDatabaseBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95044-165">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="95044-165">-FromGeoBackup</span></span>
<span data-ttu-id="95044-166">Indica che questo cmdlet ripristina un database SQL da un backup Geo-ridondante.</span><span class="sxs-lookup"><span data-stu-id="95044-166">Indicates that this cmdlet restores a SQL database from a geo-redundant backup.</span></span>
<span data-ttu-id="95044-167">Puoi usare il cmdlet Get-AzSqlDatabaseGeoBackup per ottenere un backup Geo-ridondante.</span><span class="sxs-lookup"><span data-stu-id="95044-167">You can use the Get-AzSqlDatabaseGeoBackup cmdlet to get a geo-redundant backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromGeoBackup, FromGeoBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95044-168">-FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="95044-168">-FromLongTermRetentionBackup</span></span>
<span data-ttu-id="95044-169">Indica che questo cmdlet ripristina un database SQL da un backup di conservazione a lungo termine.</span><span class="sxs-lookup"><span data-stu-id="95044-169">Indicates that this cmdlet restores a SQL database from a long term retention backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromLongTermRetentionBackup, FromLongTermRetentionBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95044-170">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="95044-170">-FromPointInTimeBackup</span></span>
<span data-ttu-id="95044-171">Indica che questo cmdlet ripristina un database SQL da un backup puntuale.</span><span class="sxs-lookup"><span data-stu-id="95044-171">Indicates that this cmdlet restores a SQL database from a point-in-time backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromPointInTimeBackup, FromPointInTimeBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95044-172">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="95044-172">-LicenseType</span></span>
<span data-ttu-id="95044-173">Tipo di licenza per il database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="95044-173">The license type for the Azure Sql database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95044-174">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="95044-174">-PointInTime</span></span>
<span data-ttu-id="95044-175">Specifica il momento, come oggetto **DateTime** , a cui vuoi ripristinare il database SQL.</span><span class="sxs-lookup"><span data-stu-id="95044-175">Specifies the point in time, as a **DateTime** object, that you want to restore your SQL database to.</span></span>
<span data-ttu-id="95044-176">Per ottenere un oggetto **DateTime** , USA cmdlet **get-date** .</span><span class="sxs-lookup"><span data-stu-id="95044-176">To get a **DateTime** object, use **Get-Date** cmdlet.</span></span>
<span data-ttu-id="95044-177">Usa questo parametro insieme al parametro *FromPointInTimeBackup* .</span><span class="sxs-lookup"><span data-stu-id="95044-177">Use this parameter together with the *FromPointInTimeBackup* parameter.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: FromPointInTimeBackup, FromPointInTimeBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: FromDeletedDatabaseBackup, FromDeletedDatabaseBackupWithVcore
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95044-178">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95044-178">-ResourceGroupName</span></span>
<span data-ttu-id="95044-179">Specifica il nome del gruppo di risorse a cui questo cmdlet assegna il database SQL.</span><span class="sxs-lookup"><span data-stu-id="95044-179">Specifies the name of the resource group to which this cmdlet assigns the SQL database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95044-180">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="95044-180">-ResourceId</span></span>
<span data-ttu-id="95044-181">Specifica l'ID della risorsa da ripristinare.</span><span class="sxs-lookup"><span data-stu-id="95044-181">Specifies the ID of the resource to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95044-182">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="95044-182">-ServerName</span></span>
<span data-ttu-id="95044-183">Specifica il nome del server di database SQL.</span><span class="sxs-lookup"><span data-stu-id="95044-183">Specifies the name of the SQL database server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95044-184">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="95044-184">-ServiceObjectiveName</span></span>
<span data-ttu-id="95044-185">Specifica il nome dell'obiettivo del servizio.</span><span class="sxs-lookup"><span data-stu-id="95044-185">Specifies the name of the service objective.</span></span>

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackup, FromDeletedDatabaseBackup, FromGeoBackup, FromLongTermRetentionBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95044-186">-NomeDatabaseDestinazione</span><span class="sxs-lookup"><span data-stu-id="95044-186">-TargetDatabaseName</span></span>
<span data-ttu-id="95044-187">Specifica il nome del database a cui eseguire il ripristino.</span><span class="sxs-lookup"><span data-stu-id="95044-187">Specifies the name of the database to restore to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95044-188">-VCore</span><span class="sxs-lookup"><span data-stu-id="95044-188">-VCore</span></span>
<span data-ttu-id="95044-189">I numeri Vcore del database SQL di Azure ripristinato.</span><span class="sxs-lookup"><span data-stu-id="95044-189">The Vcore numbers of the restored Azure Sql Database.</span></span>

```yaml
Type: System.Int32
Parameter Sets: FromPointInTimeBackupWithVcore, FromDeletedDatabaseBackupWithVcore, FromGeoBackupWithVcore, FromLongTermRetentionBackupWithVcore
Aliases: Capacity

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95044-190">-Confermare</span><span class="sxs-lookup"><span data-stu-id="95044-190">-Confirm</span></span>
<span data-ttu-id="95044-191">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95044-191">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95044-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95044-192">-WhatIf</span></span>
<span data-ttu-id="95044-193">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="95044-193">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="95044-194">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="95044-194">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95044-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95044-195">CommonParameters</span></span>
<span data-ttu-id="95044-196">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95044-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95044-197">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="95044-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95044-198">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="95044-198">INPUTS</span></span>

### <span data-ttu-id="95044-199">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="95044-199">System.DateTime</span></span>

### <span data-ttu-id="95044-200">System. String</span><span class="sxs-lookup"><span data-stu-id="95044-200">System.String</span></span>

## <span data-ttu-id="95044-201">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="95044-201">OUTPUTS</span></span>

### <span data-ttu-id="95044-202">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="95044-202">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="95044-203">Note</span><span class="sxs-lookup"><span data-stu-id="95044-203">NOTES</span></span>

## <span data-ttu-id="95044-204">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="95044-204">RELATED LINKS</span></span>

[<span data-ttu-id="95044-205">Recuperare un database SQL di Azure da un'interruzione</span><span class="sxs-lookup"><span data-stu-id="95044-205">Recover an Azure SQL Database from an outage</span></span>](http://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="95044-206">Recuperare un database SQL di Azure da un errore utente</span><span class="sxs-lookup"><span data-stu-id="95044-206">Recover an Azure SQL Database from a user error</span></span>](http://go.microsoft.com/fwlink/?LinkId=746944)

[<span data-ttu-id="95044-207">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="95044-207">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="95044-208">Get-AzSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="95044-208">Get-AzSqlDatabaseGeoBackup</span></span>](./Get-AzSqlDatabaseGeoBackup.md)

[<span data-ttu-id="95044-209">Get-AzSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="95044-209">Get-AzSqlDeletedDatabaseBackup</span></span>](./Get-AzSqlDeletedDatabaseBackup.md)

[<span data-ttu-id="95044-210">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="95044-210">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

