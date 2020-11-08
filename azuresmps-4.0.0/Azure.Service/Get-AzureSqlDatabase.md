---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 7427A101-9439-45B9-B72E-F8C2DA85E412
online version: ''
schema: 2.0.0
ms.openlocfilehash: c10ae808d105079b9739516bf9eaf316241b1b11
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029760"
---
# <span data-ttu-id="55c47-101">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="55c47-101">Get-AzureSqlDatabase</span></span>

## <span data-ttu-id="55c47-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="55c47-102">SYNOPSIS</span></span>
<span data-ttu-id="55c47-103">Recupera uno o più database.</span><span class="sxs-lookup"><span data-stu-id="55c47-103">Retrieves one or more databases.</span></span>

## <span data-ttu-id="55c47-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="55c47-104">SYNTAX</span></span>

### <span data-ttu-id="55c47-105">ByConnectionContext (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="55c47-105">ByConnectionContext (Default)</span></span>
```
Get-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> [-Database <Database>]
 [-DatabaseName <String>] [-RestorableDropped] [-RestorableDroppedDatabase <RestorableDroppedDatabase>]
 [-DatabaseDeletionDate <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="55c47-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="55c47-106">ByServerName</span></span>
```
Get-AzureSqlDatabase -ServerName <String> [-Database <Database>] [-DatabaseName <String>] [-RestorableDropped]
 [-RestorableDroppedDatabase <RestorableDroppedDatabase>] [-DatabaseDeletionDate <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="55c47-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="55c47-107">DESCRIPTION</span></span>
<span data-ttu-id="55c47-108">Il cmdlet **Get-AzureSqlDatabase** recupera una o più istanze di un database SQL di Azure da un server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="55c47-108">The **Get-AzureSqlDatabase** cmdlet retrieves one or more instances of an Azure SQL Database from an Azure SQL Database server.</span></span>
<span data-ttu-id="55c47-109">Puoi specificare il server con un contesto di connessione del server di database SQL di Azure creato usando il cmdlet **New-AzureSqlDatabaseServerContext** .</span><span class="sxs-lookup"><span data-stu-id="55c47-109">You can specify the server with an Azure SQL Database server connection context that you create using the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
<span data-ttu-id="55c47-110">In alternativa, se specifichi il nome del server di database SQL di Azure, il cmdlet usa le informazioni correnti sull'abbonamento a Azure per autenticare la richiesta di accesso al server.</span><span class="sxs-lookup"><span data-stu-id="55c47-110">Or, if you specify the Azure SQL Database server name, the cmdlet uses the current Azure subscription information to authenticate the request to access the server.</span></span>

<span data-ttu-id="55c47-111">Se non specifichi un database, il cmdlet **Get-AzureSqlDatabase** restituirà tutti i database del server specificato.</span><span class="sxs-lookup"><span data-stu-id="55c47-111">If you do not specify a database, the **Get-AzureSqlDatabase** cmdlet returns all databases from the specified server.</span></span>

<span data-ttu-id="55c47-112">Recupero di database rilasciati ripristinabili:</span><span class="sxs-lookup"><span data-stu-id="55c47-112">Retrieving restorable dropped databases:</span></span>

<span data-ttu-id="55c47-113">Recuperare i database rilasciati ripristinabili usando il parametro *RestorableDropped* .</span><span class="sxs-lookup"><span data-stu-id="55c47-113">Retrieve restorable dropped databases by using the *RestorableDropped* parameter.</span></span>
<span data-ttu-id="55c47-114">Per restituire tutti i database rilasciati ripristinabili, usare il parametro *RestorableDropped* senza *DatabaseName* e *DatabaseDeletionDate*.</span><span class="sxs-lookup"><span data-stu-id="55c47-114">To return all restorable dropped databases use the *RestorableDropped* parameter without *DatabaseName* and *DatabaseDeletionDate*.</span></span>
<span data-ttu-id="55c47-115">Per restituire un database abbandonato ripristinabile specifico, usare il parametro *RestorableDropped* con i parametri *DatabaseName* e *DatabaseDeletionDate* .</span><span class="sxs-lookup"><span data-stu-id="55c47-115">To return a specific restorable dropped database use the *RestorableDropped* parameter with the *DatabaseName* and *DatabaseDeletionDate* parameters.</span></span>
<span data-ttu-id="55c47-116">Quando si recupera un database rilasciabile specifico per il ripristino tramite il parametro *DatabaseName* , è necessario includere anche il parametro *DatabaseDeletionDate* e il valore *DatabaseDeletionDate* specificato deve includere millisecondi per corrispondere al database desiderato.</span><span class="sxs-lookup"><span data-stu-id="55c47-116">When retrieving a specific restorable dropped database by using the *DatabaseName* parameter you must also include the *DatabaseDeletionDate* parameter and the specified *DatabaseDeletionDate* value must include milliseconds to match the desired database.</span></span>

<span data-ttu-id="55c47-117">Il cmdlet **Get-AzureSqlDatabase** restituisce tutti i database rilasciati ripristinabili in un server o un database specifico che corrisponde sia a *DatabaseName* che a *DatabaseDeletionDate*.</span><span class="sxs-lookup"><span data-stu-id="55c47-117">The **Get-AzureSqlDatabase** cmdlet returns either all restorable dropped databases on a server, or one specific database that matches both *DatabaseName* and *DatabaseDeletionDate*.</span></span>
<span data-ttu-id="55c47-118">Per restituire i database rilasciati ripristinabili che soddisfano criteri diversi, ad esempio tutti i database rilasciati ripristinabili di un nome specifico, è necessario restituire tutti i database rimossi ripristinabili e quindi filtrare i risultati nel client.</span><span class="sxs-lookup"><span data-stu-id="55c47-118">To return restorable dropped databases that satisfy different criteria, such as all restorable dropped databases of a specific name, you must return all restorable dropped databases, and then filter the results on the client.</span></span>

## <span data-ttu-id="55c47-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="55c47-119">EXAMPLES</span></span>

### <span data-ttu-id="55c47-120">Esempio 1: recuperare tutti i database in un server</span><span class="sxs-lookup"><span data-stu-id="55c47-120">Example 1: Retrieve all databases on a server</span></span>
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="55c47-121">Questo comando recupera tutti i database nel server denominato lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="55c47-121">This command retrieves all databases on the server named lpqd0zbr8y.</span></span>

### <span data-ttu-id="55c47-122">Esempio 2: recuperare tutti i database rilasciati ripristinabili in un server</span><span class="sxs-lookup"><span data-stu-id="55c47-122">Example 2: Retrieve all restorable dropped databases on a server</span></span>
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -RestorableDropped
```

<span data-ttu-id="55c47-123">Questo comando recupera tutti i database rilasciati ripristinabili nel server denominato lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="55c47-123">This command retrieves all restorable dropped databases on the server named lpqd0zbr8y.</span></span>

### <span data-ttu-id="55c47-124">Esempio 3: recuperare un database da un server specificato da un contesto di connessione</span><span class="sxs-lookup"><span data-stu-id="55c47-124">Example 3: Retrieve a database from a server specified by a connection context</span></span>
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
```

<span data-ttu-id="55c47-125">Questo comando Recupera il database denominato Database01 dal server specificato dal contesto di connessione $Context.</span><span class="sxs-lookup"><span data-stu-id="55c47-125">This command retrieves database named Database01 from the server specified by the connection context $Context.</span></span>

### <span data-ttu-id="55c47-126">Esempio 4: archiviare un oggetto di database in una variabile</span><span class="sxs-lookup"><span data-stu-id="55c47-126">Example 4: Store a database object in a variable</span></span>
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
```

<span data-ttu-id="55c47-127">Questo comando Recupera il database denominato Database01 dal server denominato lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="55c47-127">This command retrieves database named Database01 from the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="55c47-128">Il comando Archivia l'oggetto di database nella variabile $Database 01.</span><span class="sxs-lookup"><span data-stu-id="55c47-128">The command stores the database object in the $Database01 variable.</span></span>

### <span data-ttu-id="55c47-129">Esempio 5: recuperare un database abbandonato ripristinabile</span><span class="sxs-lookup"><span data-stu-id="55c47-129">Example 5: Retrieve a restorable dropped database</span></span>
```
PS C:\> $DroppedDB = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01" -DatabaseDeletionDate "2012-11-09T22:59:43.000Z" -RestorableDropped
```

<span data-ttu-id="55c47-130">Questo comando Recupera il database abbandonato ripristinabile denominato Database01 che è stato eliminato in 11/9/2012 dal server denominato lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="55c47-130">This command retrieves the restorable dropped database named Database01 that was deleted on 11/9/2012 from the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="55c47-131">Questo comando Archivia i risultati nella variabile $DroppedDB.</span><span class="sxs-lookup"><span data-stu-id="55c47-131">This command stores the results in the $DroppedDB variable.</span></span>

### <span data-ttu-id="55c47-132">Esempio 6: recuperare tutti i database rilasciati ripristinati in un server e filtrare i risultati</span><span class="sxs-lookup"><span data-stu-id="55c47-132">Example 6: Retrieve all restorable dropped databases on a server and filter the results</span></span>
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -RestorableDropped | Where-Object {$_.Name -eq "ContactDB"}
```

<span data-ttu-id="55c47-133">Questo comando recupera tutti i database rilasciati ripristinati nel server denominato lpqd0zbr8y e quindi filtra i risultati solo nei database denominati ContactDB.</span><span class="sxs-lookup"><span data-stu-id="55c47-133">This command retrieves all restorable dropped databases on the server named lpqd0zbr8y, and then filters the results to only the databases named ContactDB.</span></span>

## <span data-ttu-id="55c47-134">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="55c47-134">PARAMETERS</span></span>

### <span data-ttu-id="55c47-135">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="55c47-135">-ConnectionContext</span></span>
<span data-ttu-id="55c47-136">Specifica il contesto di connessione di un server da cui recuperare un database.</span><span class="sxs-lookup"><span data-stu-id="55c47-136">Specifies the connection context of a server from which to retrieve a database.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55c47-137">-Database</span><span class="sxs-lookup"><span data-stu-id="55c47-137">-Database</span></span>
<span data-ttu-id="55c47-138">Specifica un oggetto che rappresenta il database recuperato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55c47-138">Specifies an object that represents the database that this cmdlet retrieves.</span></span>

```yaml
Type: Database
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55c47-139">-DatabaseDeletionDate</span><span class="sxs-lookup"><span data-stu-id="55c47-139">-DatabaseDeletionDate</span></span>
<span data-ttu-id="55c47-140">Specifica la data e l'ora di un'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="55c47-140">Specifies the date and time of a deletion.</span></span>
<span data-ttu-id="55c47-141">Se specifichi il parametro *RestorableDropped* , specifica questo parametro per recuperare un database abbandonato ripristinabile in base alla data e all'ora di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="55c47-141">If you specify the *RestorableDropped* parameter, specify this parameter to retrieve a restorable dropped database based on the deletion date and time.</span></span>

<span data-ttu-id="55c47-142">Il parametro *DatabaseDeletionDate* deve includere millisecondi per corrispondere all'ora del database desiderato.</span><span class="sxs-lookup"><span data-stu-id="55c47-142">The *DatabaseDeletionDate* parameter must include milliseconds to match the time of the desired database.</span></span>
<span data-ttu-id="55c47-143">Se si specifica un valore senza millisecondi, il database non viene trovato.</span><span class="sxs-lookup"><span data-stu-id="55c47-143">Specifying a value without milliseconds results in the database not being found.</span></span>

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

### <span data-ttu-id="55c47-144">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="55c47-144">-DatabaseName</span></span>
<span data-ttu-id="55c47-145">Specifica il nome del database recuperato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55c47-145">Specifies the name of the database that this cmdlet retrieves.</span></span>

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

### <span data-ttu-id="55c47-146">-Profile</span><span class="sxs-lookup"><span data-stu-id="55c47-146">-Profile</span></span>
<span data-ttu-id="55c47-147">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55c47-147">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="55c47-148">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="55c47-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="55c47-149">-RestorableDropped</span><span class="sxs-lookup"><span data-stu-id="55c47-149">-RestorableDropped</span></span>
<span data-ttu-id="55c47-150">Indica che questo cmdlet restituisce gli oggetti *RestorableDroppedDatabase* anziché gli oggetti di *database* .</span><span class="sxs-lookup"><span data-stu-id="55c47-150">Indicates that this cmdlet returns *RestorableDroppedDatabase* objects instead of *Database* objects.</span></span>
<span data-ttu-id="55c47-151">Puoi usare il parametro *DatabaseDeletionDate* per selezionare un database rilasciabile ripristinato specifico.</span><span class="sxs-lookup"><span data-stu-id="55c47-151">You can use the *DatabaseDeletionDate* parameter to select a specific restorable dropped database.</span></span>

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

### <span data-ttu-id="55c47-152">-RestorableDroppedDatabase</span><span class="sxs-lookup"><span data-stu-id="55c47-152">-RestorableDroppedDatabase</span></span>
<span data-ttu-id="55c47-153">Specifica un oggetto che rappresenta il database rilasciabile ripristinato recuperato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55c47-153">Specifies an object that represents the restorable dropped database that this cmdlet retrieves.</span></span>

```yaml
Type: RestorableDroppedDatabase
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55c47-154">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="55c47-154">-ServerName</span></span>
<span data-ttu-id="55c47-155">Specifica il nome del server che contiene il database recuperato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55c47-155">Specifies the name of the server that contains the database that this cmdlet retrieves.</span></span>
<span data-ttu-id="55c47-156">Il cmdlet usa l'abbonamento Azure corrente per accedere al server.</span><span class="sxs-lookup"><span data-stu-id="55c47-156">The cmdlet uses the current Azure subscription to access the server.</span></span>

```yaml
Type: String
Parameter Sets: ByServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55c47-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55c47-157">CommonParameters</span></span>
<span data-ttu-id="55c47-158">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55c47-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55c47-159">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55c47-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55c47-160">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="55c47-160">INPUTS</span></span>

### <span data-ttu-id="55c47-161">Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. database</span><span class="sxs-lookup"><span data-stu-id="55c47-161">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

### <span data-ttu-id="55c47-162">Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. RestorableDroppedDatabase</span><span class="sxs-lookup"><span data-stu-id="55c47-162">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase</span></span>

## <span data-ttu-id="55c47-163">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="55c47-163">OUTPUTS</span></span>

### <span data-ttu-id="55c47-164">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database\></span><span class="sxs-lookup"><span data-stu-id="55c47-164">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database\></span></span>
<span data-ttu-id="55c47-165">Questo cmdlet restituisce un oggetto *database* se non specifichi il parametro *RestorableDropped* .</span><span class="sxs-lookup"><span data-stu-id="55c47-165">This cmdlet returns a *Database* object if you do not specify the *RestorableDropped* parameter.</span></span>

### <span data-ttu-id="55c47-166">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase\></span><span class="sxs-lookup"><span data-stu-id="55c47-166">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase\></span></span>
<span data-ttu-id="55c47-167">Questo cmdlet restituisce un oggetto *RestorableDroppedDatabase* se specifichi il parametro *RestorableDropped* .</span><span class="sxs-lookup"><span data-stu-id="55c47-167">This cmdlet returns a *RestorableDroppedDatabase* object if you specify the *RestorableDropped* parameter.</span></span>

## <span data-ttu-id="55c47-168">Note</span><span class="sxs-lookup"><span data-stu-id="55c47-168">NOTES</span></span>

## <span data-ttu-id="55c47-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="55c47-169">RELATED LINKS</span></span>

[<span data-ttu-id="55c47-170">Database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="55c47-170">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="55c47-171">Operazioni per i database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="55c47-171">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="55c47-172">New-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="55c47-172">New-AzureSqlDatabase</span></span>](./New-AzureSqlDatabase.md)

[<span data-ttu-id="55c47-173">New-AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="55c47-173">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)

[<span data-ttu-id="55c47-174">Remove-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="55c47-174">Remove-AzureSqlDatabase</span></span>](./Remove-AzureSqlDatabase.md)

[<span data-ttu-id="55c47-175">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="55c47-175">Set-AzureSqlDatabase</span></span>](./Set-AzureSqlDatabase.md)


