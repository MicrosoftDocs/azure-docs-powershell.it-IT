---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 383F36F3-3F52-4FC3-99F7-831096E6037D
online version: ''
schema: 2.0.0
ms.openlocfilehash: ff7c7cd50b06a4110b6af12611f3d91eaedfd227
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023384"
---
# <span data-ttu-id="20dde-101">Start-AzureSqlDatabaseRestore</span><span class="sxs-lookup"><span data-stu-id="20dde-101">Start-AzureSqlDatabaseRestore</span></span>

## <span data-ttu-id="20dde-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="20dde-102">SYNOPSIS</span></span>
<span data-ttu-id="20dde-103">Esegue un ripristino puntuale di un database.</span><span class="sxs-lookup"><span data-stu-id="20dde-103">Performs a point in time restore of a database.</span></span>

## <span data-ttu-id="20dde-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="20dde-104">SYNTAX</span></span>

### <span data-ttu-id="20dde-105">BySourceDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="20dde-105">BySourceDatabaseObject</span></span>
```
Start-AzureSqlDatabaseRestore [-SourceServerName <String>] -SourceDatabase <Database>
 [-TargetServerName <String>] -TargetDatabaseName <String> [-PointInTime <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="20dde-106">BySourceRestorableDroppedDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="20dde-106">BySourceRestorableDroppedDatabaseObject</span></span>
```
Start-AzureSqlDatabaseRestore [-SourceServerName <String>]
 -SourceRestorableDroppedDatabase <RestorableDroppedDatabase> [-TargetServerName <String>]
 -TargetDatabaseName <String> [-PointInTime <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="20dde-107">BySourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="20dde-107">BySourceDatabaseName</span></span>
```
Start-AzureSqlDatabaseRestore -SourceServerName <String> -SourceDatabaseName <String>
 [-TargetServerName <String>] -TargetDatabaseName <String> [-PointInTime <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="20dde-108">BySourceRestorableDroppedDatabaseName</span><span class="sxs-lookup"><span data-stu-id="20dde-108">BySourceRestorableDroppedDatabaseName</span></span>
```
Start-AzureSqlDatabaseRestore -SourceServerName <String> -SourceDatabaseName <String>
 -SourceDatabaseDeletionDate <DateTime> [-TargetServerName <String>] [-RestorableDropped]
 -TargetDatabaseName <String> [-PointInTime <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="20dde-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20dde-109">DESCRIPTION</span></span>
<span data-ttu-id="20dde-110">Il cmdlet **Start-AzureSqlDatabaseRestore** esegue un ripristino puntuale di un database di base, standard o Premium.</span><span class="sxs-lookup"><span data-stu-id="20dde-110">The **Start-AzureSqlDatabaseRestore** cmdlet performs a point in time restore of a Basic, Standard or Premium database.</span></span>
<span data-ttu-id="20dde-111">Database SQL di Azure mantiene i backup del database di base di 7 giorni, standard per 14 giorni e Premium per 35 giorni.</span><span class="sxs-lookup"><span data-stu-id="20dde-111">Azure SQL Database retains Basic database backups 7 days, Standard for 14 days, and Premium for 35 days.</span></span>
<span data-ttu-id="20dde-112">L'operazione di ripristino crea un nuovo database.</span><span class="sxs-lookup"><span data-stu-id="20dde-112">The restore operation creates a new database.</span></span>
<span data-ttu-id="20dde-113">Se il database di origine non viene eliminato, il parametro *sourcedatabasename* e *NomeDatabaseDestinazione* deve avere valori diversi.</span><span class="sxs-lookup"><span data-stu-id="20dde-113">If the source database is not deleted, the *SourceDatabaseName* and *TargetDatabaseName* parameter must have different values.</span></span>

<span data-ttu-id="20dde-114">Il database SQL di Azure attualmente non supporta il ripristino Cross server.</span><span class="sxs-lookup"><span data-stu-id="20dde-114">Azure SQL Database does not currently support cross server restore.</span></span>
<span data-ttu-id="20dde-115">I nomi dei server di origine e di destinazione devono essere uguali.</span><span class="sxs-lookup"><span data-stu-id="20dde-115">The source and target server names must be the same.</span></span>

## <span data-ttu-id="20dde-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="20dde-116">EXAMPLES</span></span>

### <span data-ttu-id="20dde-117">Esempio 1: ripristinare un database specificato come oggetto in un momento</span><span class="sxs-lookup"><span data-stu-id="20dde-117">Example 1: Restore a database specified as an object to a point in time</span></span>
```
PS C:\> $Database = Get-AzureSqlDatabase -ServerName "Server01" -DatabaseName "Database17" 
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceDatabase $Database -TargetDatabaseName "DatabaseRestored" -PointInTime "2013-01-01 06:00:00"
```

<span data-ttu-id="20dde-118">Il primo comando ottiene un oggetto di database per il database denominato Database17 nel server denominato Server01 e lo archivia nella variabile $Database.</span><span class="sxs-lookup"><span data-stu-id="20dde-118">The first command gets a database object for the database named Database17 on the server named Server01, and then stores it in the $Database variable.</span></span>

<span data-ttu-id="20dde-119">Il secondo comando Ripristina il database in un momento specifico.</span><span class="sxs-lookup"><span data-stu-id="20dde-119">The second command restores the database to a specific point in time.</span></span>
<span data-ttu-id="20dde-120">Il comando specifica il nome per il nuovo database.</span><span class="sxs-lookup"><span data-stu-id="20dde-120">The command specifies at name for the new database.</span></span>

### <span data-ttu-id="20dde-121">Esempio 2: ripristinare un database specificato per nome in un momento</span><span class="sxs-lookup"><span data-stu-id="20dde-121">Example 2: Restore a database specified by name to a point in time</span></span>
```
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceServerName "Server01" -SourceDatabaseName "Database17" -TargetDatabaseName "DatabaseRestored" -PointInTime "2013-01-01 06:00:00"
```

<span data-ttu-id="20dde-122">Questo comando Ripristina il database denominato Database17 in un determinato momento.</span><span class="sxs-lookup"><span data-stu-id="20dde-122">This command restores the database named Database17 to a specific point in time.</span></span>
<span data-ttu-id="20dde-123">Il comando specifica il nome per il nuovo database.</span><span class="sxs-lookup"><span data-stu-id="20dde-123">The command specifies at name for the new database.</span></span>

### <span data-ttu-id="20dde-124">Esempio 3: ripristinare un database abbandonato specificato come oggetto in un momento</span><span class="sxs-lookup"><span data-stu-id="20dde-124">Example 3: Restore a dropped database specified as an object to a point in time</span></span>
```
PS C:\> $Database = Get-AzureSqlDatabase -RestorableDropped -ServerName "Server01" -DatabaseName "Database01" -DatabaseDeletionDate "2012-11-09T22:59:43.000Z" 
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceRestorableDroppedDatabase $Database -TargetDatabaseName "DroppedDatabaseRestored"
```

<span data-ttu-id="20dde-125">Il primo comando ottiene un oggetto di database per il database denominato Database01 nel server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="20dde-125">The first command gets a database object for the database named Database01 on the server named Server01.</span></span>
<span data-ttu-id="20dde-126">Il comando specifica il parametro *RestorableDropped* .</span><span class="sxs-lookup"><span data-stu-id="20dde-126">The command specifies the *RestorableDropped* parameter.</span></span>
<span data-ttu-id="20dde-127">Di conseguenza, il cmdlet recupera il database eliminato ripristinabile il punto di ripristino specificato.</span><span class="sxs-lookup"><span data-stu-id="20dde-127">Therefore, the cmdlet gets restorable dropped database the specified restore point.</span></span>
<span data-ttu-id="20dde-128">Il comando Archivia l'oggetto di database nella variabile $Database.</span><span class="sxs-lookup"><span data-stu-id="20dde-128">The command stores that database object in the $Database variable.</span></span>

<span data-ttu-id="20dde-129">Il secondo comando Ripristina il database eliminato specificato da $Database.</span><span class="sxs-lookup"><span data-stu-id="20dde-129">The second command restores the dropped database specified by $Database.</span></span>
<span data-ttu-id="20dde-130">Il comando specifica il nome per il nuovo database.</span><span class="sxs-lookup"><span data-stu-id="20dde-130">The command specifies at name for the new database.</span></span>

## <span data-ttu-id="20dde-131">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="20dde-131">PARAMETERS</span></span>

### <span data-ttu-id="20dde-132">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="20dde-132">-PointInTime</span></span>
<span data-ttu-id="20dde-133">Specifica il punto di ripristino a cui ripristinare il database.</span><span class="sxs-lookup"><span data-stu-id="20dde-133">Specifies the restore point to which to restore the database.</span></span>
<span data-ttu-id="20dde-134">Al termine dell'operazione di ripristino, il database viene ripristinato nello stato in cui si trovava alla data e all'ora specificate da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="20dde-134">When the restore operation finishes, the database is restored to the state it was at the date and time that this parameter specifies.</span></span>
<span data-ttu-id="20dde-135">Per impostazione predefinita, per un database dinamico impostato sull'ora corrente e per un database eliminato, questo cmdlet usa l'ora in cui il database è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="20dde-135">By default, for a live database this set to the current time, and for a dropped database, this cmdlet uses the time when the database was dropped.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20dde-136">-Profile</span><span class="sxs-lookup"><span data-stu-id="20dde-136">-Profile</span></span>
<span data-ttu-id="20dde-137">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20dde-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="20dde-138">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="20dde-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="20dde-139">-RestorableDropped</span><span class="sxs-lookup"><span data-stu-id="20dde-139">-RestorableDropped</span></span>
<span data-ttu-id="20dde-140">Indica che questo cmdlet ripristina un database abbandonato ripristinabile.</span><span class="sxs-lookup"><span data-stu-id="20dde-140">Indicates that this cmdlet restores a restorable dropped database.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20dde-141">-SourceDatabase</span><span class="sxs-lookup"><span data-stu-id="20dde-141">-SourceDatabase</span></span>
<span data-ttu-id="20dde-142">Specifica il nome del database ripristinato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20dde-142">Specifies the name of the database that this cmdlet restores.</span></span>

```yaml
Type: Database
Parameter Sets: BySourceDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20dde-143">-SourceDatabaseDeletionDate</span><span class="sxs-lookup"><span data-stu-id="20dde-143">-SourceDatabaseDeletionDate</span></span>
<span data-ttu-id="20dde-144">Specifica la data e l'ora in cui il database è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="20dde-144">Specifies the date and time when the database was deleted.</span></span>
<span data-ttu-id="20dde-145">È necessario includere millisecondi quando si specifica il tempo per corrispondere al tempo effettivo di eliminazione del database.</span><span class="sxs-lookup"><span data-stu-id="20dde-145">You must include milliseconds when you specify the time to match the actual database deletion time.</span></span>

```yaml
Type: DateTime
Parameter Sets: BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20dde-146">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="20dde-146">-SourceDatabaseName</span></span>
<span data-ttu-id="20dde-147">Specifica il nome del database Live ripristinato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20dde-147">Specifies the name of the live database that this cmdlet restores.</span></span>

```yaml
Type: String
Parameter Sets: BySourceDatabaseName, BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20dde-148">-SourceRestorableDroppedDatabase</span><span class="sxs-lookup"><span data-stu-id="20dde-148">-SourceRestorableDroppedDatabase</span></span>
<span data-ttu-id="20dde-149">Specifica un oggetto che rappresenta il database di cui è stato ripristinato il ripristino di questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20dde-149">Specifies an object that represents the restorable dropped database that this cmdlet restores.</span></span>
<span data-ttu-id="20dde-150">Per ottenere un oggetto **RestorableDroppedDatabase** , usa il cmdlet Get-AzureSqlDatabase e specifica il parametro *RestorableDropped* .</span><span class="sxs-lookup"><span data-stu-id="20dde-150">To obtain a **RestorableDroppedDatabase** object, use the Get-AzureSqlDatabase cmdlet, and specify the *RestorableDropped* parameter.</span></span>

```yaml
Type: RestorableDroppedDatabase
Parameter Sets: BySourceRestorableDroppedDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20dde-151">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="20dde-151">-SourceServerName</span></span>
<span data-ttu-id="20dde-152">Specifica il nome del server in cui il database di origine è in esecuzione o in cui è stato eseguito il database di origine prima dell'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="20dde-152">Specifies the name of the server on which the source database is live and running, or on which the source database ran before it was deleted.</span></span>

```yaml
Type: String
Parameter Sets: BySourceDatabaseObject, BySourceRestorableDroppedDatabaseObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: BySourceDatabaseName, BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20dde-153">-NomeDatabaseDestinazione</span><span class="sxs-lookup"><span data-stu-id="20dde-153">-TargetDatabaseName</span></span>
<span data-ttu-id="20dde-154">Specifica il nome del nuovo database creato dall'operazione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="20dde-154">Specifies the name of the new database that the restore operation creates.</span></span>

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

### <span data-ttu-id="20dde-155">-TargetServerName</span><span class="sxs-lookup"><span data-stu-id="20dde-155">-TargetServerName</span></span>
<span data-ttu-id="20dde-156">Specifica il nome del server a cui questo cmdlet ripristina il database.</span><span class="sxs-lookup"><span data-stu-id="20dde-156">Specifies the name of the server to which this cmdlet restores the database.</span></span>

<span data-ttu-id="20dde-157">Il database SQL di Azure attualmente non supporta il ripristino Cross server.</span><span class="sxs-lookup"><span data-stu-id="20dde-157">Azure SQL Database does not currently support cross server restore.</span></span>
<span data-ttu-id="20dde-158">I nomi dei server di origine e di destinazione devono essere uguali.</span><span class="sxs-lookup"><span data-stu-id="20dde-158">The source and target server names must be the same.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20dde-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20dde-159">CommonParameters</span></span>
<span data-ttu-id="20dde-160">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20dde-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20dde-161">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20dde-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20dde-162">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="20dde-162">INPUTS</span></span>

### <span data-ttu-id="20dde-163">Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. RestorableDroppedDatabase</span><span class="sxs-lookup"><span data-stu-id="20dde-163">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase</span></span>

### <span data-ttu-id="20dde-164">Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. database</span><span class="sxs-lookup"><span data-stu-id="20dde-164">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="20dde-165">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="20dde-165">OUTPUTS</span></span>

### <span data-ttu-id="20dde-166">Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. RestoreDatabaseOperation</span><span class="sxs-lookup"><span data-stu-id="20dde-166">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestoreDatabaseOperation</span></span>

## <span data-ttu-id="20dde-167">Note</span><span class="sxs-lookup"><span data-stu-id="20dde-167">NOTES</span></span>
* <span data-ttu-id="20dde-168">Per eseguire questo cmdlet, è necessario usare l'autenticazione basata su certificati.</span><span class="sxs-lookup"><span data-stu-id="20dde-168">You must use certificate based authentication to run this cmdlet.</span></span> <span data-ttu-id="20dde-169">Eseguire i comandi seguenti nel computer in cui eseguire questo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="20dde-169">Run the following commands on the computer where run this cmdlet:</span></span> 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## <span data-ttu-id="20dde-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="20dde-170">RELATED LINKS</span></span>

[<span data-ttu-id="20dde-171">Database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="20dde-171">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="20dde-172">Creare una richiesta di ripristino di database</span><span class="sxs-lookup"><span data-stu-id="20dde-172">Create Database Restore Request</span></span>](https://msdn.microsoft.com/en-us/library/dn509571.aspx)

[<span data-ttu-id="20dde-173">Operazioni per i database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="20dde-173">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="20dde-174">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="20dde-174">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)


