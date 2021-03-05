---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 72E0E558-74D7-4A50-A975-FA7D0C0B301E
online version: https://docs.microsoft.com/powershell/module/az.sql/restore-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlDatabase.md
ms.openlocfilehash: bfe2abe8a59114f69ec27f28ba0b270bfbbd72a1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995048"
---
# <span data-ttu-id="ee729-101">Restore-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ee729-101">Restore-AzSqlDatabase</span></span>

## <span data-ttu-id="ee729-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee729-102">SYNOPSIS</span></span>
<span data-ttu-id="ee729-103">Ripristina un database SQL database.</span><span class="sxs-lookup"><span data-stu-id="ee729-103">Restores a SQL database.</span></span>

## <span data-ttu-id="ee729-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ee729-104">SYNTAX</span></span>

### <span data-ttu-id="ee729-105">FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="ee729-105">FromPointInTimeBackup</span></span>
```
Restore-AzSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>] [-BackupStorageRedundancy <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ee729-106">FromPointInTimeBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="ee729-106">FromPointInTimeBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String>
 -VCore <Int32> [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee729-107">FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="ee729-107">FromDeletedDatabaseBackup</span></span>
```
Restore-AzSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> [-Edition <String>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee729-108">FromDeletedDatabaseBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="ee729-108">FromDeletedDatabaseBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob]
 -ComputeGeneration <String> -VCore <Int32> [-LicenseType <String>] [-BackupStorageRedundancy <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ee729-109">FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="ee729-109">FromGeoBackup</span></span>
```
Restore-AzSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String> -TargetDatabaseName <String>
 [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob]
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee729-110">FromGeoBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="ee729-110">FromGeoBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String> -TargetDatabaseName <String>
 -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32> [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee729-111">FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="ee729-111">FromLongTermRetentionBackup</span></span>
```
Restore-AzSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>]
 [-AsJob] [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee729-112">FromLongTermRetentionBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="ee729-112">FromLongTermRetentionBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32>
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee729-113">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ee729-113">DESCRIPTION</span></span>
<span data-ttu-id="ee729-114">Il cmdlet **Restore-AzSqlDatabase** ripristina un database SQL da un backup geo-ridondante, un backup di un database eliminato, un backup di conservazione a lungo termine o un momento nel tempo in un database live.</span><span class="sxs-lookup"><span data-stu-id="ee729-114">The **Restore-AzSqlDatabase** cmdlet restores a SQL database from a geo-redundant backup, a backup of a deleted database, a long term retention backup, or a point in time in a live database.</span></span>
<span data-ttu-id="ee729-115">Il database ripristinato viene creato come nuovo database.</span><span class="sxs-lookup"><span data-stu-id="ee729-115">The restored database is created as a new database.</span></span>
<span data-ttu-id="ee729-116">È possibile creare un database SQL elastico impostando il parametro *ElasticPoolName* su un pool elastico esistente.</span><span class="sxs-lookup"><span data-stu-id="ee729-116">You can create an elastic SQL database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="ee729-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ee729-117">EXAMPLES</span></span>

### <span data-ttu-id="ee729-118">Esempio 1: Ripristinare un database da un momento all'altro</span><span class="sxs-lookup"><span data-stu-id="ee729-118">Example 1: Restore a database from a point in time</span></span>
```
PS C:\>$Database = Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -Edition "Standard" -ServiceObjectiveName "S2"
```

<span data-ttu-id="ee729-119">Il primo comando recupera SQL database denominato Database01 e quindi lo archivia nella $Database variabile.</span><span class="sxs-lookup"><span data-stu-id="ee729-119">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="ee729-120">Il secondo comando ripristina il database $Database dal backup temporato specificato al database denominato Database Ripristinato.</span><span class="sxs-lookup"><span data-stu-id="ee729-120">The second command restores the database in $Database from the specified point-in-time backup to the database named RestoredDatabase.</span></span>

### <span data-ttu-id="ee729-121">Esempio 2: Ripristinare un database da un momento all'altro in un pool flessibile</span><span class="sxs-lookup"><span data-stu-id="ee729-121">Example 2: Restore a database from a point in time to an elastic pool</span></span>
```
PS C:\>$Database = Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="ee729-122">Il primo comando recupera SQL database denominato Database01 e quindi lo archivia nella $Database variabile.</span><span class="sxs-lookup"><span data-stu-id="ee729-122">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="ee729-123">Il secondo comando ripristina il database di $Database dal backup temporato specificato al database SQL denominato RestoredDatabase nel pool di elastici denominato elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="ee729-123">The second command restores the database in $Database from the specified point-in-time backup to the SQL database named RestoredDatabase in the elastic pool named elasticpool01.</span></span>

### <span data-ttu-id="ee729-124">Esempio 3: Ripristinare un database eliminato</span><span class="sxs-lookup"><span data-stu-id="ee729-124">Example 3: Restore a deleted database</span></span>
```
PS C:\>$DeletedDatabase = Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -Edition "Standard" -ServiceObjectiveName "S2" -PointInTime UTCDateTime
```

<span data-ttu-id="ee729-125">Il primo comando ottiene il backup del database eliminato che si vuole ripristinare usando [Get-AzSqlDeletedDatabaseBackup.](./Get-AzSqlDeletedDatabaseBackup.md)</span><span class="sxs-lookup"><span data-stu-id="ee729-125">The first command gets the deleted database backup that you want to restore by using [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="ee729-126">Il secondo comando avvia il ripristino dal backup del database eliminato usando il cmdlet [Restore-AzSqlDatabase.](./Restore-AzSqlDatabase.md)</span><span class="sxs-lookup"><span data-stu-id="ee729-126">The second command starts the restore from the deleted database backup by using the [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md) cmdlet.</span></span> <span data-ttu-id="ee729-127">Se il parametro -PointInTime non è specificato, il database verrà ripristinato all'ora di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="ee729-127">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="ee729-128">Esempio 4: Ripristinare un database eliminato in un pool flessibile</span><span class="sxs-lookup"><span data-stu-id="ee729-128">Example 4: Restore a deleted database into an elastic pool</span></span>
```
PS C:\>$DeletedDatabase = Get-AzSqlDeletedDatabaseBackup -ResourceGroupName $resourceGroupName -ServerName $sqlServerName -DatabaseName 'DatabaseToRestore'
PS C:\> Restore-AzSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -ElasticPoolName "elasticpool01" -PointInTime UTCDateTime
```

<span data-ttu-id="ee729-129">Il primo comando ottiene il backup del database eliminato che si vuole ripristinare usando [Get-AzSqlDeletedDatabaseBackup.](./Get-AzSqlDeletedDatabaseBackup.md)</span><span class="sxs-lookup"><span data-stu-id="ee729-129">The first command gets the deleted database backup that you want to restore by using [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="ee729-130">Il secondo comando avvia il ripristino dal backup del database eliminato [usando Restore-AzSqlDatabase.](./Restore-AzSqlDatabase.md)</span><span class="sxs-lookup"><span data-stu-id="ee729-130">The second command starts the restore from the deleted database backup by using [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md).</span></span> <span data-ttu-id="ee729-131">Se il parametro -PointInTime non è specificato, il database verrà ripristinato all'ora di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="ee729-131">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="ee729-132">Esempio 5: Geo-Restore un database</span><span class="sxs-lookup"><span data-stu-id="ee729-132">Example 5: Geo-Restore a database</span></span>
```
PS C:\>$GeoBackup = Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromGeoBackup -ResourceGroupName "TargetResourceGroup" -ServerName "TargetServer" -TargetDatabaseName "RestoredDatabase" -ResourceId $GeoBackup.ResourceID -Edition "Standard" -RequestedServiceObjectiveName "S2"
```

<span data-ttu-id="ee729-133">Il primo comando recupera il backup geo-ridondante per il database denominato Database01 e quindi lo archivia nella $GeoBackup variabile.</span><span class="sxs-lookup"><span data-stu-id="ee729-133">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>
<span data-ttu-id="ee729-134">Il secondo comando ripristina il backup di $GeoBackup nel database SQL denominato Database Ripristinato.</span><span class="sxs-lookup"><span data-stu-id="ee729-134">The second command restores the backup in $GeoBackup to the SQL database named RestoredDatabase.</span></span>

## <span data-ttu-id="ee729-135">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee729-135">PARAMETERS</span></span>

### <span data-ttu-id="ee729-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ee729-136">-AsJob</span></span>
<span data-ttu-id="ee729-137">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ee729-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ee729-138">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="ee729-138">-BackupStorageRedundancy</span></span>
<span data-ttu-id="ee729-139">Ridondanza di archiviazione di backup usata per archiviare i backup per SQL database.</span><span class="sxs-lookup"><span data-stu-id="ee729-139">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="ee729-140">Le opzioni disponibili sono: Locale, Area e Geo.</span><span class="sxs-lookup"><span data-stu-id="ee729-140">Options are: Local, Zone and Geo.</span></span>

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

### <span data-ttu-id="ee729-141">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="ee729-141">-ComputeGeneration</span></span>
<span data-ttu-id="ee729-142">Generazione di elaborazione da assegnare al database ripristinato</span><span class="sxs-lookup"><span data-stu-id="ee729-142">The compute generation to assign to the restored database</span></span>

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

### <span data-ttu-id="ee729-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee729-143">-DefaultProfile</span></span>
<span data-ttu-id="ee729-144">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ee729-144">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ee729-145">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="ee729-145">-DeletionDate</span></span>
<span data-ttu-id="ee729-146">Specifica la data di eliminazione come **oggetto DateTime.**</span><span class="sxs-lookup"><span data-stu-id="ee729-146">Specifies the deletion date as a **DateTime** object.</span></span>
<span data-ttu-id="ee729-147">Per ottenere un **oggetto DateTime,** usare il cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="ee729-147">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="ee729-148">-Edition</span><span class="sxs-lookup"><span data-stu-id="ee729-148">-Edition</span></span>
<span data-ttu-id="ee729-149">Specifica l'edizione del SQL database.</span><span class="sxs-lookup"><span data-stu-id="ee729-149">Specifies the edition of the SQL database.</span></span>
<span data-ttu-id="ee729-150">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="ee729-150">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ee729-151">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ee729-151">None</span></span>
- <span data-ttu-id="ee729-152">Di base</span><span class="sxs-lookup"><span data-stu-id="ee729-152">Basic</span></span>
- <span data-ttu-id="ee729-153">Standard</span><span class="sxs-lookup"><span data-stu-id="ee729-153">Standard</span></span>
- <span data-ttu-id="ee729-154">Premium</span><span class="sxs-lookup"><span data-stu-id="ee729-154">Premium</span></span>
- <span data-ttu-id="ee729-155">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="ee729-155">DataWarehouse</span></span>
- <span data-ttu-id="ee729-156">Gratis</span><span class="sxs-lookup"><span data-stu-id="ee729-156">Free</span></span>
- <span data-ttu-id="ee729-157">Estendamento</span><span class="sxs-lookup"><span data-stu-id="ee729-157">Stretch</span></span>
- <span data-ttu-id="ee729-158">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="ee729-158">GeneralPurpose</span></span>
- <span data-ttu-id="ee729-159">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="ee729-159">BusinessCritical</span></span>

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

### <span data-ttu-id="ee729-160">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="ee729-160">-ElasticPoolName</span></span>
<span data-ttu-id="ee729-161">Specifica il nome del pool flessibile in cui inserire il SQL database.</span><span class="sxs-lookup"><span data-stu-id="ee729-161">Specifies the name of the elastic pool in which to put the SQL database.</span></span>

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

### <span data-ttu-id="ee729-162">-FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="ee729-162">-FromDeletedDatabaseBackup</span></span>
<span data-ttu-id="ee729-163">Indica che questo cmdlet ripristina un database da un backup di un database SQL eliminato.</span><span class="sxs-lookup"><span data-stu-id="ee729-163">Indicates that this cmdlet restores a database from a backup of a deleted SQL database.</span></span>
<span data-ttu-id="ee729-164">È possibile usare il cmdlet Get-AzSqlDeletedDatabaseBackup per ottenere il backup di un database SQL eliminato.</span><span class="sxs-lookup"><span data-stu-id="ee729-164">You can use the Get-AzSqlDeletedDatabaseBackup cmdlet to get the backup of a deleted SQL database.</span></span>

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

### <span data-ttu-id="ee729-165">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="ee729-165">-FromGeoBackup</span></span>
<span data-ttu-id="ee729-166">Indica che questo cmdlet ripristina un database SQL da un backup geo-ridondante.</span><span class="sxs-lookup"><span data-stu-id="ee729-166">Indicates that this cmdlet restores a SQL database from a geo-redundant backup.</span></span>
<span data-ttu-id="ee729-167">È possibile usare il cmdlet Get-AzSqlDatabaseGeoBackup per ottenere un backup geo-ridondante.</span><span class="sxs-lookup"><span data-stu-id="ee729-167">You can use the Get-AzSqlDatabaseGeoBackup cmdlet to get a geo-redundant backup.</span></span>

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

### <span data-ttu-id="ee729-168">-FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="ee729-168">-FromLongTermRetentionBackup</span></span>
<span data-ttu-id="ee729-169">Indica che questo cmdlet ripristina un SQL database da un backup di conservazione a lungo termine.</span><span class="sxs-lookup"><span data-stu-id="ee729-169">Indicates that this cmdlet restores a SQL database from a long term retention backup.</span></span>

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

### <span data-ttu-id="ee729-170">- FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="ee729-170">-FromPointInTimeBackup</span></span>
<span data-ttu-id="ee729-171">Indica che questo cmdlet ripristina SQL database da un backup temporato.</span><span class="sxs-lookup"><span data-stu-id="ee729-171">Indicates that this cmdlet restores a SQL database from a point-in-time backup.</span></span>

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

### <span data-ttu-id="ee729-172">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="ee729-172">-LicenseType</span></span>
<span data-ttu-id="ee729-173">Il tipo di licenza per il database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="ee729-173">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="ee729-174">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="ee729-174">-PointInTime</span></span>
<span data-ttu-id="ee729-175">Specifica il momento, come oggetto **DateTime,** in cui si vuole ripristinare SQL database.</span><span class="sxs-lookup"><span data-stu-id="ee729-175">Specifies the point in time, as a **DateTime** object, that you want to restore your SQL database to.</span></span>
<span data-ttu-id="ee729-176">Per ottenere un **oggetto DateTime,** usare il cmdlet **Get-Date.**</span><span class="sxs-lookup"><span data-stu-id="ee729-176">To get a **DateTime** object, use **Get-Date** cmdlet.</span></span>
<span data-ttu-id="ee729-177">Usare questo parametro insieme al *parametro FromPointInTimeBackup.*</span><span class="sxs-lookup"><span data-stu-id="ee729-177">Use this parameter together with the *FromPointInTimeBackup* parameter.</span></span>

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

### <span data-ttu-id="ee729-178">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee729-178">-ResourceGroupName</span></span>
<span data-ttu-id="ee729-179">Specifica il nome del gruppo di risorse a cui il cmdlet assegna SQL database.</span><span class="sxs-lookup"><span data-stu-id="ee729-179">Specifies the name of the resource group to which this cmdlet assigns the SQL database.</span></span>

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

### <span data-ttu-id="ee729-180">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee729-180">-ResourceId</span></span>
<span data-ttu-id="ee729-181">Specifica l'ID della risorsa da ripristinare.</span><span class="sxs-lookup"><span data-stu-id="ee729-181">Specifies the ID of the resource to restore.</span></span>

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

### <span data-ttu-id="ee729-182">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ee729-182">-ServerName</span></span>
<span data-ttu-id="ee729-183">Specifica il nome del server di database SQL server di database.</span><span class="sxs-lookup"><span data-stu-id="ee729-183">Specifies the name of the SQL database server.</span></span>

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

### <span data-ttu-id="ee729-184">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="ee729-184">-ServiceObjectiveName</span></span>
<span data-ttu-id="ee729-185">Specifica il nome dell'obiettivo del servizio.</span><span class="sxs-lookup"><span data-stu-id="ee729-185">Specifies the name of the service objective.</span></span>

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

### <span data-ttu-id="ee729-186">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="ee729-186">-TargetDatabaseName</span></span>
<span data-ttu-id="ee729-187">Specifica il nome del database in cui eseguire il ripristino.</span><span class="sxs-lookup"><span data-stu-id="ee729-187">Specifies the name of the database to restore to.</span></span>

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

### <span data-ttu-id="ee729-188">-VCore</span><span class="sxs-lookup"><span data-stu-id="ee729-188">-VCore</span></span>
<span data-ttu-id="ee729-189">Numeri Vcore del database SQL di Azure ripristinato.</span><span class="sxs-lookup"><span data-stu-id="ee729-189">The Vcore numbers of the restored Azure Sql Database.</span></span>

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

### <span data-ttu-id="ee729-190">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ee729-190">-Confirm</span></span>
<span data-ttu-id="ee729-191">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee729-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee729-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee729-192">-WhatIf</span></span>
<span data-ttu-id="ee729-193">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ee729-193">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ee729-194">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ee729-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee729-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee729-195">CommonParameters</span></span>
<span data-ttu-id="ee729-196">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee729-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee729-197">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ee729-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee729-198">INPUT</span><span class="sxs-lookup"><span data-stu-id="ee729-198">INPUTS</span></span>

### <span data-ttu-id="ee729-199">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="ee729-199">System.DateTime</span></span>

### <span data-ttu-id="ee729-200">System.String</span><span class="sxs-lookup"><span data-stu-id="ee729-200">System.String</span></span>

## <span data-ttu-id="ee729-201">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ee729-201">OUTPUTS</span></span>

### <span data-ttu-id="ee729-202">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="ee729-202">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="ee729-203">NOTE</span><span class="sxs-lookup"><span data-stu-id="ee729-203">NOTES</span></span>

## <span data-ttu-id="ee729-204">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ee729-204">RELATED LINKS</span></span>

[<span data-ttu-id="ee729-205">Recuperare un database SQL Azure da un'interruzione</span><span class="sxs-lookup"><span data-stu-id="ee729-205">Recover an Azure SQL Database from an outage</span></span>](http://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="ee729-206">Recuperare un database SQL Azure da un errore utente</span><span class="sxs-lookup"><span data-stu-id="ee729-206">Recover an Azure SQL Database from a user error</span></span>](http://go.microsoft.com/fwlink/?LinkId=746944)

[<span data-ttu-id="ee729-207">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ee729-207">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="ee729-208">Get-AzSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="ee729-208">Get-AzSqlDatabaseGeoBackup</span></span>](./Get-AzSqlDatabaseGeoBackup.md)

[<span data-ttu-id="ee729-209">Get-AzSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="ee729-209">Get-AzSqlDeletedDatabaseBackup</span></span>](./Get-AzSqlDeletedDatabaseBackup.md)

[<span data-ttu-id="ee729-210">documentazione SQL database</span><span class="sxs-lookup"><span data-stu-id="ee729-210">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

