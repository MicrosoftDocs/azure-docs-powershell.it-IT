---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 72E0E558-74D7-4A50-A975-FA7D0C0B301E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/restore-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlDatabase.md
ms.openlocfilehash: e7110511840542b8efed22b1267b76074434b94a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685805"
---
# <span data-ttu-id="2b72f-101">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2b72f-101">Restore-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="2b72f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2b72f-102">SYNOPSIS</span></span>
<span data-ttu-id="2b72f-103">Ripristina un database SQL.</span><span class="sxs-lookup"><span data-stu-id="2b72f-103">Restores a SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b72f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2b72f-104">SYNTAX</span></span>

### <span data-ttu-id="2b72f-105">FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="2b72f-105">FromPointInTimeBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> [-Edition <DatabaseEdition>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b72f-106">FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="2b72f-106">FromDeletedDatabaseBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> [-Edition <DatabaseEdition>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b72f-107">FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="2b72f-107">FromGeoBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <DatabaseEdition>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-AsJob] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b72f-108">FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="2b72f-108">FromLongTermRetentionBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <DatabaseEdition>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-AsJob] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2b72f-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b72f-109">DESCRIPTION</span></span>
<span data-ttu-id="2b72f-110">Il cmdlet **Restore-AzureRmSqlDatabase** ripristina un database SQL da un backup Geo-ridondante, un backup di un database eliminato, un backup a lungo termine o un momento in un database dinamico.</span><span class="sxs-lookup"><span data-stu-id="2b72f-110">The **Restore-AzureRmSqlDatabase** cmdlet restores a SQL database from a geo-redundant backup, a backup of a deleted database, a long term retention backup, or a point in time in a live database.</span></span>
<span data-ttu-id="2b72f-111">Il database ripristinato viene creato come nuovo database.</span><span class="sxs-lookup"><span data-stu-id="2b72f-111">The restored database is created as a new database.</span></span>

<span data-ttu-id="2b72f-112">Puoi creare un database SQL elastico impostando il parametro *ElasticPoolName* su un pool elastico esistente.</span><span class="sxs-lookup"><span data-stu-id="2b72f-112">You can create an elastic SQL database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="2b72f-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2b72f-113">EXAMPLES</span></span>

### <span data-ttu-id="2b72f-114">Esempio 1: ripristinare un database da un momento</span><span class="sxs-lookup"><span data-stu-id="2b72f-114">Example 1: Restore a database from a point in time</span></span>
```
PS C:\>$Database = Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -Edition "Standard" -ServiceObjectiveName "S2"
```

<span data-ttu-id="2b72f-115">Il primo comando ottiene il database SQL denominato Database01 e lo archivia nella variabile $Database.</span><span class="sxs-lookup"><span data-stu-id="2b72f-115">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>

<span data-ttu-id="2b72f-116">Il secondo comando Ripristina il database in $Database dal backup point-in-Time specificato al database denominato RestoredDatabase.</span><span class="sxs-lookup"><span data-stu-id="2b72f-116">The second command restores the database in $Database from the specified point-in-time backup to the database named RestoredDatabase.</span></span>

### <span data-ttu-id="2b72f-117">Esempio 2: ripristinare un database da un momento a un pool elastico</span><span class="sxs-lookup"><span data-stu-id="2b72f-117">Example 2: Restore a database from a point in time to an elastic pool</span></span>
```
PS C:\>$Database = Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="2b72f-118">Il primo comando ottiene il database SQL denominato Database01 e lo archivia nella variabile $Database.</span><span class="sxs-lookup"><span data-stu-id="2b72f-118">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>

<span data-ttu-id="2b72f-119">Il secondo comando Ripristina il database in $Database dal backup point-in-Time specificato al database SQL denominato RestoredDatabase nel pool elastico denominato elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="2b72f-119">The second command restores the database in $Database from the specified point-in-time backup to the SQL database named RestoredDatabase in the elastic pool named elasticpool01.</span></span>

### <span data-ttu-id="2b72f-120">Esempio 3: ripristinare un database eliminato</span><span class="sxs-lookup"><span data-stu-id="2b72f-120">Example 3: Restore a deleted database</span></span>
```
PS C:\>$DeletedDatabase = Get-AzureRmSqlDeletedDatabaseBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -Edition "Standard" -ServiceObjectiveName "S2" -PointInTime UTCDateTime
```

<span data-ttu-id="2b72f-121">Il primo comando ottiene il backup del database eliminato che si vuole ripristinare tramite [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span><span class="sxs-lookup"><span data-stu-id="2b72f-121">The first command gets the deleted database backup that you want to restore by using [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="2b72f-122">Il secondo comando avvia il ripristino dal backup del database eliminato usando il cmdlet [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="2b72f-122">The second command starts the restore from the deleted database backup by using the [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md) cmdlet.</span></span> <span data-ttu-id="2b72f-123">Se il parametro-PointInTime non viene specificato, il database verrà ripristinato all'ora di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="2b72f-123">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="2b72f-124">Esempio 4: ripristinare un database eliminato in un pool elastico</span><span class="sxs-lookup"><span data-stu-id="2b72f-124">Example 4: Restore a deleted database into an elastic pool</span></span>
```
PS C:\>$DeletedDatabase = Get-AzureRmSqlDeletedDatabaseBackup -ResourceGroupName $resourceGroupName -ServerName $sqlServerName -DatabaseName 'DatabaseToRestore'
PS C:\> Restore-AzureRmSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -ElasticPoolName "elasticpool01" -PointInTime UTCDateTime
```

<span data-ttu-id="2b72f-125">Il primo comando ottiene il backup del database eliminato che si vuole ripristinare tramite [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span><span class="sxs-lookup"><span data-stu-id="2b72f-125">The first command gets the deleted database backup that you want to restore by using [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="2b72f-126">Il secondo comando avvia il ripristino dal backup del database eliminato tramite [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md).</span><span class="sxs-lookup"><span data-stu-id="2b72f-126">The second command starts the restore from the deleted database backup by using [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md).</span></span> <span data-ttu-id="2b72f-127">Se il parametro-PointInTime non viene specificato, il database verrà ripristinato all'ora di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="2b72f-127">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="2b72f-128">Esempio 5: Geo-Restore un database</span><span class="sxs-lookup"><span data-stu-id="2b72f-128">Example 5: Geo-Restore a database</span></span>
```
PS C:\>$GeoBackup = Get-AzureRmSqlDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromGeoBackup -ResourceGroupName "TargetResourceGroup" -ServerName "TargetServer" -TargetDatabaseName "RestoredDatabase" -ResourceId $GeoBackup.ResourceID -Edition "Standard" -RequestedServiceObjectiveName "S2"
```

<span data-ttu-id="2b72f-129">Il primo comando ottiene il backup Geo-ridondante per il database denominato Database01 e lo archivia nella variabile $GeoBackup.</span><span class="sxs-lookup"><span data-stu-id="2b72f-129">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>

<span data-ttu-id="2b72f-130">Il secondo comando Ripristina il backup in $GeoBackup al database SQL denominato RestoredDatabase.</span><span class="sxs-lookup"><span data-stu-id="2b72f-130">The second command restores the backup in $GeoBackup to the SQL database named RestoredDatabase.</span></span>

## <span data-ttu-id="2b72f-131">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2b72f-131">PARAMETERS</span></span>

### <span data-ttu-id="2b72f-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2b72f-132">-AsJob</span></span>
<span data-ttu-id="2b72f-133">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="2b72f-133">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="2b72f-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b72f-134">-DefaultProfile</span></span>
<span data-ttu-id="2b72f-135">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2b72f-135">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2b72f-136">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="2b72f-136">-DeletionDate</span></span>
<span data-ttu-id="2b72f-137">Specifica la data di eliminazione come oggetto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="2b72f-137">Specifies the deletion date as a **DateTime** object.</span></span>
<span data-ttu-id="2b72f-138">Per ottenere un oggetto **DateTime** , usa il cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="2b72f-138">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: DateTime
Parameter Sets: FromDeletedDatabaseBackup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b72f-139">-Edition</span><span class="sxs-lookup"><span data-stu-id="2b72f-139">-Edition</span></span>
<span data-ttu-id="2b72f-140">Specifica l'edizione del database SQL.</span><span class="sxs-lookup"><span data-stu-id="2b72f-140">Specifies the edition of the SQL database.</span></span>
<span data-ttu-id="2b72f-141">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="2b72f-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2b72f-142">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2b72f-142">None</span></span>
- <span data-ttu-id="2b72f-143">Premium</span><span class="sxs-lookup"><span data-stu-id="2b72f-143">Premium</span></span>
- <span data-ttu-id="2b72f-144">Base</span><span class="sxs-lookup"><span data-stu-id="2b72f-144">Basic</span></span>
- <span data-ttu-id="2b72f-145">Standard</span><span class="sxs-lookup"><span data-stu-id="2b72f-145">Standard</span></span>
- <span data-ttu-id="2b72f-146">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="2b72f-146">DataWarehouse</span></span>
- <span data-ttu-id="2b72f-147">Gratuito</span><span class="sxs-lookup"><span data-stu-id="2b72f-147">Free</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b72f-148">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="2b72f-148">-ElasticPoolName</span></span>
<span data-ttu-id="2b72f-149">Specifica il nome del pool elastico in cui inserire il database SQL.</span><span class="sxs-lookup"><span data-stu-id="2b72f-149">Specifies the name of the elastic pool in which to put the SQL database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b72f-150">-FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="2b72f-150">-FromDeletedDatabaseBackup</span></span>
<span data-ttu-id="2b72f-151">Indica che questo cmdlet ripristina un database da un backup di un database SQL eliminato.</span><span class="sxs-lookup"><span data-stu-id="2b72f-151">Indicates that this cmdlet restores a database from a backup of a deleted SQL database.</span></span>
<span data-ttu-id="2b72f-152">Puoi usare il cmdlet Get-AzureRMSqlDeletedDatabaseBackup per ottenere il backup di un database SQL eliminato.</span><span class="sxs-lookup"><span data-stu-id="2b72f-152">You can use the Get-AzureRMSqlDeletedDatabaseBackup cmdlet to get the backup of a deleted SQL database.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FromDeletedDatabaseBackup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b72f-153">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="2b72f-153">-FromGeoBackup</span></span>
<span data-ttu-id="2b72f-154">Indica che questo cmdlet ripristina un database SQL da un backup Geo-ridondante.</span><span class="sxs-lookup"><span data-stu-id="2b72f-154">Indicates that this cmdlet restores a SQL database from a geo-redundant backup.</span></span>
<span data-ttu-id="2b72f-155">Puoi usare il cmdlet Get-AzureRMSqlDatabaseGeoBackup per ottenere un backup Geo-ridondante.</span><span class="sxs-lookup"><span data-stu-id="2b72f-155">You can use the Get-AzureRMSqlDatabaseGeoBackup cmdlet to get a geo-redundant backup.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FromGeoBackup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b72f-156">-FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="2b72f-156">-FromLongTermRetentionBackup</span></span>
<span data-ttu-id="2b72f-157">Indica che questo cmdlet ripristina un database SQL da un backup di conservazione a lungo termine.</span><span class="sxs-lookup"><span data-stu-id="2b72f-157">Indicates that this cmdlet restores a SQL database from a long term retention backup.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FromLongTermRetentionBackup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b72f-158">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="2b72f-158">-FromPointInTimeBackup</span></span>
<span data-ttu-id="2b72f-159">Indica che questo cmdlet ripristina un database SQL da un backup puntuale.</span><span class="sxs-lookup"><span data-stu-id="2b72f-159">Indicates that this cmdlet restores a SQL database from a point-in-time backup.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FromPointInTimeBackup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b72f-160">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="2b72f-160">-PointInTime</span></span>
<span data-ttu-id="2b72f-161">Specifica il momento, come oggetto **DateTime** , a cui vuoi ripristinare il database SQL.</span><span class="sxs-lookup"><span data-stu-id="2b72f-161">Specifies the point in time, as a **DateTime** object, that you want to restore your SQL database to.</span></span>
<span data-ttu-id="2b72f-162">Per ottenere un oggetto **DateTime** , USA cmdlet **get-date** .</span><span class="sxs-lookup"><span data-stu-id="2b72f-162">To get a **DateTime** object, use **Get-Date** cmdlet.</span></span>

<span data-ttu-id="2b72f-163">Usa questo parametro insieme al parametro *FromPointInTimeBackup* .</span><span class="sxs-lookup"><span data-stu-id="2b72f-163">Use this parameter together with the *FromPointInTimeBackup* parameter.</span></span>

```yaml
Type: DateTime
Parameter Sets: FromPointInTimeBackup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: DateTime
Parameter Sets: FromDeletedDatabaseBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b72f-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b72f-164">-ResourceGroupName</span></span>
<span data-ttu-id="2b72f-165">Specifica il nome del gruppo di risorse a cui questo cmdlet assegna il database SQL.</span><span class="sxs-lookup"><span data-stu-id="2b72f-165">Specifies the name of the resource group to which this cmdlet assigns the SQL database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b72f-166">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b72f-166">-ResourceId</span></span>
<span data-ttu-id="2b72f-167">Specifica l'ID della risorsa da ripristinare.</span><span class="sxs-lookup"><span data-stu-id="2b72f-167">Specifies the ID of the resource to restore.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b72f-168">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="2b72f-168">-ServerName</span></span>
<span data-ttu-id="2b72f-169">Specifica il nome del server di database SQL.</span><span class="sxs-lookup"><span data-stu-id="2b72f-169">Specifies the name of the SQL database server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b72f-170">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="2b72f-170">-ServiceObjectiveName</span></span>
<span data-ttu-id="2b72f-171">Specifica il nome dell'obiettivo del servizio.</span><span class="sxs-lookup"><span data-stu-id="2b72f-171">Specifies the name of the service objective.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b72f-172">-NomeDatabaseDestinazione</span><span class="sxs-lookup"><span data-stu-id="2b72f-172">-TargetDatabaseName</span></span>
<span data-ttu-id="2b72f-173">Specifica il nome del database a cui eseguire il ripristino.</span><span class="sxs-lookup"><span data-stu-id="2b72f-173">Specifies the name of the database to restore to.</span></span>

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

### <span data-ttu-id="2b72f-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b72f-174">CommonParameters</span></span>
<span data-ttu-id="2b72f-175">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b72f-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b72f-176">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b72f-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b72f-177">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2b72f-177">INPUTS</span></span>

### <span data-ttu-id="2b72f-178">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2b72f-178">None</span></span>
<span data-ttu-id="2b72f-179">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="2b72f-179">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2b72f-180">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2b72f-180">OUTPUTS</span></span>

### <span data-ttu-id="2b72f-181">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="2b72f-181">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="2b72f-182">Note</span><span class="sxs-lookup"><span data-stu-id="2b72f-182">NOTES</span></span>

## <span data-ttu-id="2b72f-183">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2b72f-183">RELATED LINKS</span></span>

[<span data-ttu-id="2b72f-184">Recuperare un database SQL di Azure da un'interruzione</span><span class="sxs-lookup"><span data-stu-id="2b72f-184">Recover an Azure SQL Database from an outage</span></span>](https://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="2b72f-185">Recuperare un database SQL di Azure da un errore utente</span><span class="sxs-lookup"><span data-stu-id="2b72f-185">Recover an Azure SQL Database from a user error</span></span>](https://go.microsoft.com/fwlink/?LinkId=746944)

[<span data-ttu-id="2b72f-186">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2b72f-186">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="2b72f-187">Get-AzureRMSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="2b72f-187">Get-AzureRMSqlDatabaseGeoBackup</span></span>](./Get-AzureRMSqlDatabaseGeoBackup.md)

[<span data-ttu-id="2b72f-188">Get-AzureRMSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="2b72f-188">Get-AzureRMSqlDeletedDatabaseBackup</span></span>](./Get-AzureRMSqlDeletedDatabaseBackup.md)

[<span data-ttu-id="2b72f-189">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="2b72f-189">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

