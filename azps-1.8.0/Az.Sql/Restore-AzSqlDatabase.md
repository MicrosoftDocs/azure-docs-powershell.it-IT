---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 72E0E558-74D7-4A50-A975-FA7D0C0B301E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/restore-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlDatabase.md
ms.openlocfilehash: 262d4266a41cd9072ff9109819a2268999d26d7f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676774"
---
# <span data-ttu-id="b93ce-101">Restore-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b93ce-101">Restore-AzSqlDatabase</span></span>

## <span data-ttu-id="b93ce-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b93ce-102">SYNOPSIS</span></span>
<span data-ttu-id="b93ce-103">Ripristina un database SQL.</span><span class="sxs-lookup"><span data-stu-id="b93ce-103">Restores a SQL database.</span></span>

## <span data-ttu-id="b93ce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b93ce-104">SYNTAX</span></span>

### <span data-ttu-id="b93ce-105">FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="b93ce-105">FromPointInTimeBackup</span></span>
```
Restore-AzSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b93ce-106">FromPointInTimeBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="b93ce-106">FromPointInTimeBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String>
 -VCore <Int32> [-LicenseType <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b93ce-107">FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="b93ce-107">FromDeletedDatabaseBackup</span></span>
```
Restore-AzSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> [-Edition <String>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b93ce-108">FromDeletedDatabaseBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="b93ce-108">FromDeletedDatabaseBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob]
 -ComputeGeneration <String> -VCore <Int32> [-LicenseType <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b93ce-109">FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="b93ce-109">FromGeoBackup</span></span>
```
Restore-AzSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String> -TargetDatabaseName <String>
 [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob]
 [-LicenseType <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b93ce-110">FromGeoBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="b93ce-110">FromGeoBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String> -TargetDatabaseName <String>
 -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32> [-LicenseType <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b93ce-111">FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="b93ce-111">FromLongTermRetentionBackup</span></span>
```
Restore-AzSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>]
 [-AsJob] [-LicenseType <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b93ce-112">FromLongTermRetentionBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="b93ce-112">FromLongTermRetentionBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32>
 [-LicenseType <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b93ce-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b93ce-113">DESCRIPTION</span></span>
<span data-ttu-id="b93ce-114">Il cmdlet **Restore-AzSqlDatabase** ripristina un database SQL da un backup Geo-ridondante, un backup di un database eliminato, un backup a lungo termine o un momento in un database dinamico.</span><span class="sxs-lookup"><span data-stu-id="b93ce-114">The **Restore-AzSqlDatabase** cmdlet restores a SQL database from a geo-redundant backup, a backup of a deleted database, a long term retention backup, or a point in time in a live database.</span></span>
<span data-ttu-id="b93ce-115">Il database ripristinato viene creato come nuovo database.</span><span class="sxs-lookup"><span data-stu-id="b93ce-115">The restored database is created as a new database.</span></span>
<span data-ttu-id="b93ce-116">Puoi creare un database SQL elastico impostando il parametro *ElasticPoolName* su un pool elastico esistente.</span><span class="sxs-lookup"><span data-stu-id="b93ce-116">You can create an elastic SQL database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="b93ce-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b93ce-117">EXAMPLES</span></span>

### <span data-ttu-id="b93ce-118">Esempio 1: ripristinare un database da un momento</span><span class="sxs-lookup"><span data-stu-id="b93ce-118">Example 1: Restore a database from a point in time</span></span>
```
PS C:\>$Database = Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -Edition "Standard" -ServiceObjectiveName "S2"
```

<span data-ttu-id="b93ce-119">Il primo comando ottiene il database SQL denominato Database01 e lo archivia nella variabile $Database.</span><span class="sxs-lookup"><span data-stu-id="b93ce-119">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="b93ce-120">Il secondo comando Ripristina il database in $Database dal backup point-in-Time specificato al database denominato RestoredDatabase.</span><span class="sxs-lookup"><span data-stu-id="b93ce-120">The second command restores the database in $Database from the specified point-in-time backup to the database named RestoredDatabase.</span></span>

### <span data-ttu-id="b93ce-121">Esempio 2: ripristinare un database da un momento a un pool elastico</span><span class="sxs-lookup"><span data-stu-id="b93ce-121">Example 2: Restore a database from a point in time to an elastic pool</span></span>
```
PS C:\>$Database = Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="b93ce-122">Il primo comando ottiene il database SQL denominato Database01 e lo archivia nella variabile $Database.</span><span class="sxs-lookup"><span data-stu-id="b93ce-122">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="b93ce-123">Il secondo comando Ripristina il database in $Database dal backup point-in-Time specificato al database SQL denominato RestoredDatabase nel pool elastico denominato elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="b93ce-123">The second command restores the database in $Database from the specified point-in-time backup to the SQL database named RestoredDatabase in the elastic pool named elasticpool01.</span></span>

### <span data-ttu-id="b93ce-124">Esempio 3: ripristinare un database eliminato</span><span class="sxs-lookup"><span data-stu-id="b93ce-124">Example 3: Restore a deleted database</span></span>
```
PS C:\>$DeletedDatabase = Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -Edition "Standard" -ServiceObjectiveName "S2" -PointInTime UTCDateTime
```

<span data-ttu-id="b93ce-125">Il primo comando ottiene il backup del database eliminato che si vuole ripristinare tramite [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span><span class="sxs-lookup"><span data-stu-id="b93ce-125">The first command gets the deleted database backup that you want to restore by using [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="b93ce-126">Il secondo comando avvia il ripristino dal backup del database eliminato usando il cmdlet [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="b93ce-126">The second command starts the restore from the deleted database backup by using the [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md) cmdlet.</span></span> <span data-ttu-id="b93ce-127">Se il parametro-PointInTime non viene specificato, il database verrà ripristinato all'ora di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="b93ce-127">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="b93ce-128">Esempio 4: ripristinare un database eliminato in un pool elastico</span><span class="sxs-lookup"><span data-stu-id="b93ce-128">Example 4: Restore a deleted database into an elastic pool</span></span>
```
PS C:\>$DeletedDatabase = Get-AzSqlDeletedDatabaseBackup -ResourceGroupName $resourceGroupName -ServerName $sqlServerName -DatabaseName 'DatabaseToRestore'
PS C:\> Restore-AzSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -ElasticPoolName "elasticpool01" -PointInTime UTCDateTime
```

<span data-ttu-id="b93ce-129">Il primo comando ottiene il backup del database eliminato che si vuole ripristinare tramite [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span><span class="sxs-lookup"><span data-stu-id="b93ce-129">The first command gets the deleted database backup that you want to restore by using [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="b93ce-130">Il secondo comando avvia il ripristino dal backup del database eliminato tramite [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md).</span><span class="sxs-lookup"><span data-stu-id="b93ce-130">The second command starts the restore from the deleted database backup by using [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md).</span></span> <span data-ttu-id="b93ce-131">Se il parametro-PointInTime non viene specificato, il database verrà ripristinato all'ora di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="b93ce-131">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="b93ce-132">Esempio 5: Geo-Restore un database</span><span class="sxs-lookup"><span data-stu-id="b93ce-132">Example 5: Geo-Restore a database</span></span>
```
PS C:\>$GeoBackup = Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromGeoBackup -ResourceGroupName "TargetResourceGroup" -ServerName "TargetServer" -TargetDatabaseName "RestoredDatabase" -ResourceId $GeoBackup.ResourceID -Edition "Standard" -RequestedServiceObjectiveName "S2"
```

<span data-ttu-id="b93ce-133">Il primo comando ottiene il backup Geo-ridondante per il database denominato Database01 e lo archivia nella variabile $GeoBackup.</span><span class="sxs-lookup"><span data-stu-id="b93ce-133">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>
<span data-ttu-id="b93ce-134">Il secondo comando Ripristina il backup in $GeoBackup al database SQL denominato RestoredDatabase.</span><span class="sxs-lookup"><span data-stu-id="b93ce-134">The second command restores the backup in $GeoBackup to the SQL database named RestoredDatabase.</span></span>

## <span data-ttu-id="b93ce-135">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b93ce-135">PARAMETERS</span></span>

### <span data-ttu-id="b93ce-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b93ce-136">-AsJob</span></span>
<span data-ttu-id="b93ce-137">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="b93ce-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b93ce-138">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="b93ce-138">-ComputeGeneration</span></span>
<span data-ttu-id="b93ce-139">Generazione di Compute da assegnare al database ripristinato</span><span class="sxs-lookup"><span data-stu-id="b93ce-139">The compute generation to assign to the restored database</span></span>

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

### <span data-ttu-id="b93ce-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b93ce-140">-DefaultProfile</span></span>
<span data-ttu-id="b93ce-141">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b93ce-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b93ce-142">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="b93ce-142">-DeletionDate</span></span>
<span data-ttu-id="b93ce-143">Specifica la data di eliminazione come oggetto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="b93ce-143">Specifies the deletion date as a **DateTime** object.</span></span>
<span data-ttu-id="b93ce-144">Per ottenere un oggetto **DateTime** , usa il cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="b93ce-144">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="b93ce-145">-Edition</span><span class="sxs-lookup"><span data-stu-id="b93ce-145">-Edition</span></span>
<span data-ttu-id="b93ce-146">Specifica l'edizione del database SQL.</span><span class="sxs-lookup"><span data-stu-id="b93ce-146">Specifies the edition of the SQL database.</span></span>
<span data-ttu-id="b93ce-147">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b93ce-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b93ce-148">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b93ce-148">None</span></span>
- <span data-ttu-id="b93ce-149">Base</span><span class="sxs-lookup"><span data-stu-id="b93ce-149">Basic</span></span>
- <span data-ttu-id="b93ce-150">Standard</span><span class="sxs-lookup"><span data-stu-id="b93ce-150">Standard</span></span>
- <span data-ttu-id="b93ce-151">Premium</span><span class="sxs-lookup"><span data-stu-id="b93ce-151">Premium</span></span>
- <span data-ttu-id="b93ce-152">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="b93ce-152">DataWarehouse</span></span>
- <span data-ttu-id="b93ce-153">Gratuito</span><span class="sxs-lookup"><span data-stu-id="b93ce-153">Free</span></span>
- <span data-ttu-id="b93ce-154">Tratto</span><span class="sxs-lookup"><span data-stu-id="b93ce-154">Stretch</span></span>
- <span data-ttu-id="b93ce-155">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="b93ce-155">GeneralPurpose</span></span>
- <span data-ttu-id="b93ce-156">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="b93ce-156">BusinessCritical</span></span>

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

### <span data-ttu-id="b93ce-157">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="b93ce-157">-ElasticPoolName</span></span>
<span data-ttu-id="b93ce-158">Specifica il nome del pool elastico in cui inserire il database SQL.</span><span class="sxs-lookup"><span data-stu-id="b93ce-158">Specifies the name of the elastic pool in which to put the SQL database.</span></span>

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

### <span data-ttu-id="b93ce-159">-FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="b93ce-159">-FromDeletedDatabaseBackup</span></span>
<span data-ttu-id="b93ce-160">Indica che questo cmdlet ripristina un database da un backup di un database SQL eliminato.</span><span class="sxs-lookup"><span data-stu-id="b93ce-160">Indicates that this cmdlet restores a database from a backup of a deleted SQL database.</span></span>
<span data-ttu-id="b93ce-161">Puoi usare il cmdlet Get-AzSqlDeletedDatabaseBackup per ottenere il backup di un database SQL eliminato.</span><span class="sxs-lookup"><span data-stu-id="b93ce-161">You can use the Get-AzSqlDeletedDatabaseBackup cmdlet to get the backup of a deleted SQL database.</span></span>

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

### <span data-ttu-id="b93ce-162">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="b93ce-162">-FromGeoBackup</span></span>
<span data-ttu-id="b93ce-163">Indica che questo cmdlet ripristina un database SQL da un backup Geo-ridondante.</span><span class="sxs-lookup"><span data-stu-id="b93ce-163">Indicates that this cmdlet restores a SQL database from a geo-redundant backup.</span></span>
<span data-ttu-id="b93ce-164">Puoi usare il cmdlet Get-AzSqlDatabaseGeoBackup per ottenere un backup Geo-ridondante.</span><span class="sxs-lookup"><span data-stu-id="b93ce-164">You can use the Get-AzSqlDatabaseGeoBackup cmdlet to get a geo-redundant backup.</span></span>

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

### <span data-ttu-id="b93ce-165">-FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="b93ce-165">-FromLongTermRetentionBackup</span></span>
<span data-ttu-id="b93ce-166">Indica che questo cmdlet ripristina un database SQL da un backup di conservazione a lungo termine.</span><span class="sxs-lookup"><span data-stu-id="b93ce-166">Indicates that this cmdlet restores a SQL database from a long term retention backup.</span></span>

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

### <span data-ttu-id="b93ce-167">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="b93ce-167">-FromPointInTimeBackup</span></span>
<span data-ttu-id="b93ce-168">Indica che questo cmdlet ripristina un database SQL da un backup puntuale.</span><span class="sxs-lookup"><span data-stu-id="b93ce-168">Indicates that this cmdlet restores a SQL database from a point-in-time backup.</span></span>

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

### <span data-ttu-id="b93ce-169">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="b93ce-169">-LicenseType</span></span>
<span data-ttu-id="b93ce-170">Tipo di licenza per il database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="b93ce-170">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="b93ce-171">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="b93ce-171">-PointInTime</span></span>
<span data-ttu-id="b93ce-172">Specifica il momento, come oggetto **DateTime** , a cui vuoi ripristinare il database SQL.</span><span class="sxs-lookup"><span data-stu-id="b93ce-172">Specifies the point in time, as a **DateTime** object, that you want to restore your SQL database to.</span></span>
<span data-ttu-id="b93ce-173">Per ottenere un oggetto **DateTime** , USA cmdlet **get-date** .</span><span class="sxs-lookup"><span data-stu-id="b93ce-173">To get a **DateTime** object, use **Get-Date** cmdlet.</span></span>
<span data-ttu-id="b93ce-174">Usa questo parametro insieme al parametro *FromPointInTimeBackup* .</span><span class="sxs-lookup"><span data-stu-id="b93ce-174">Use this parameter together with the *FromPointInTimeBackup* parameter.</span></span>

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

### <span data-ttu-id="b93ce-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b93ce-175">-ResourceGroupName</span></span>
<span data-ttu-id="b93ce-176">Specifica il nome del gruppo di risorse a cui questo cmdlet assegna il database SQL.</span><span class="sxs-lookup"><span data-stu-id="b93ce-176">Specifies the name of the resource group to which this cmdlet assigns the SQL database.</span></span>

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

### <span data-ttu-id="b93ce-177">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b93ce-177">-ResourceId</span></span>
<span data-ttu-id="b93ce-178">Specifica l'ID della risorsa da ripristinare.</span><span class="sxs-lookup"><span data-stu-id="b93ce-178">Specifies the ID of the resource to restore.</span></span>

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

### <span data-ttu-id="b93ce-179">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="b93ce-179">-ServerName</span></span>
<span data-ttu-id="b93ce-180">Specifica il nome del server di database SQL.</span><span class="sxs-lookup"><span data-stu-id="b93ce-180">Specifies the name of the SQL database server.</span></span>

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

### <span data-ttu-id="b93ce-181">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="b93ce-181">-ServiceObjectiveName</span></span>
<span data-ttu-id="b93ce-182">Specifica il nome dell'obiettivo del servizio.</span><span class="sxs-lookup"><span data-stu-id="b93ce-182">Specifies the name of the service objective.</span></span>

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

### <span data-ttu-id="b93ce-183">-NomeDatabaseDestinazione</span><span class="sxs-lookup"><span data-stu-id="b93ce-183">-TargetDatabaseName</span></span>
<span data-ttu-id="b93ce-184">Specifica il nome del database a cui eseguire il ripristino.</span><span class="sxs-lookup"><span data-stu-id="b93ce-184">Specifies the name of the database to restore to.</span></span>

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

### <span data-ttu-id="b93ce-185">-VCore</span><span class="sxs-lookup"><span data-stu-id="b93ce-185">-VCore</span></span>
<span data-ttu-id="b93ce-186">I numeri Vcore del database SQL di Azure ripristinato.</span><span class="sxs-lookup"><span data-stu-id="b93ce-186">The Vcore numbers of the restored Azure Sql Database.</span></span>

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

### <span data-ttu-id="b93ce-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b93ce-187">CommonParameters</span></span>
<span data-ttu-id="b93ce-188">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b93ce-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b93ce-189">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b93ce-189">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b93ce-190">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b93ce-190">INPUTS</span></span>

### <span data-ttu-id="b93ce-191">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="b93ce-191">System.DateTime</span></span>

### <span data-ttu-id="b93ce-192">System. String</span><span class="sxs-lookup"><span data-stu-id="b93ce-192">System.String</span></span>

## <span data-ttu-id="b93ce-193">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b93ce-193">OUTPUTS</span></span>

### <span data-ttu-id="b93ce-194">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="b93ce-194">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="b93ce-195">Note</span><span class="sxs-lookup"><span data-stu-id="b93ce-195">NOTES</span></span>

## <span data-ttu-id="b93ce-196">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b93ce-196">RELATED LINKS</span></span>

[<span data-ttu-id="b93ce-197">Recuperare un database SQL di Azure da un'interruzione</span><span class="sxs-lookup"><span data-stu-id="b93ce-197">Recover an Azure SQL Database from an outage</span></span>](https://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="b93ce-198">Recuperare un database SQL di Azure da un errore utente</span><span class="sxs-lookup"><span data-stu-id="b93ce-198">Recover an Azure SQL Database from a user error</span></span>](https://go.microsoft.com/fwlink/?LinkId=746944)

[<span data-ttu-id="b93ce-199">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b93ce-199">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="b93ce-200">Get-AzSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="b93ce-200">Get-AzSqlDatabaseGeoBackup</span></span>](./Get-AzSqlDatabaseGeoBackup.md)

[<span data-ttu-id="b93ce-201">Get-AzSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="b93ce-201">Get-AzSqlDeletedDatabaseBackup</span></span>](./Get-AzSqlDeletedDatabaseBackup.md)

[<span data-ttu-id="b93ce-202">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="b93ce-202">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

