---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F63769D6-9A31-4A67-972A-1E0428853C86
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88f61718e363a630b70519590025a6da80364aeb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023381"
---
# <span data-ttu-id="8a988-101">Start-AzureSqlDatabaseRecovery</span><span class="sxs-lookup"><span data-stu-id="8a988-101">Start-AzureSqlDatabaseRecovery</span></span>

## <span data-ttu-id="8a988-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8a988-102">SYNOPSIS</span></span>
<span data-ttu-id="8a988-103">Avvia una richiesta di ripristino per un database.</span><span class="sxs-lookup"><span data-stu-id="8a988-103">Initiates a restore request for a database.</span></span>

## <span data-ttu-id="8a988-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8a988-104">SYNTAX</span></span>

### <span data-ttu-id="8a988-105">BySourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="8a988-105">BySourceDatabaseName</span></span>
```
Start-AzureSqlDatabaseRecovery -SourceServerName <String> -SourceDatabaseName <String>
 [-TargetServerName <String>] [-TargetDatabaseName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="8a988-106">BySourceDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="8a988-106">BySourceDatabaseObject</span></span>
```
Start-AzureSqlDatabaseRecovery -SourceDatabase <RecoverableDatabase> [-TargetServerName <String>]
 [-TargetDatabaseName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8a988-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8a988-107">DESCRIPTION</span></span>
<span data-ttu-id="8a988-108">Il cmdlet **Start-AzureSqlDatabaseRecovery** avvia una richiesta di ripristino per un database Live o Dropped.</span><span class="sxs-lookup"><span data-stu-id="8a988-108">The **Start-AzureSqlDatabaseRecovery** cmdlet initiates a restore request for a live or dropped database.</span></span>
<span data-ttu-id="8a988-109">Questo cmdlet supporta il ripristino di base che usa l'ultimo backup disponibile noto per il database.</span><span class="sxs-lookup"><span data-stu-id="8a988-109">This cmdlet supports basic recovery that uses the last known available backup for the database.</span></span>
<span data-ttu-id="8a988-110">L'operazione di ripristino crea un nuovo database.</span><span class="sxs-lookup"><span data-stu-id="8a988-110">The recovery operation creates a new database.</span></span>
<span data-ttu-id="8a988-111">Se si recupera un database Live nello stesso server, è necessario specificare un nome diverso per il nuovo database.</span><span class="sxs-lookup"><span data-stu-id="8a988-111">If you recover a live database on the same server, you must specify a different name for the new database.</span></span>

<span data-ttu-id="8a988-112">Per eseguire un ripristino puntuale per un database, USA invece il cmdlet **Start-AzureSqlDatabaseRestore** .</span><span class="sxs-lookup"><span data-stu-id="8a988-112">To do a point in time restore for a database, use the **Start-AzureSqlDatabaseRestore** cmdlet instead.</span></span>

## <span data-ttu-id="8a988-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8a988-113">EXAMPLES</span></span>

### <span data-ttu-id="8a988-114">Esempio 1: recuperare un database specificato come oggetto</span><span class="sxs-lookup"><span data-stu-id="8a988-114">Example 1: Recover a database specified as an object</span></span>
```
PS C:\> $Database = Get-AzureSqlRecoverableDatabase -ServerName "Server01" -DatabaseName "Database17" 
PS C:\> $Operation = Start-AzureSqlDatabaseRecovery -SourceDatabase $Database -TargetDatabaseName "DatabaseRestored"
```

<span data-ttu-id="8a988-115">Il primo comando ottiene un oggetto database usando il cmdlet **Get-AzureSqlRecoverableDatabase** .</span><span class="sxs-lookup"><span data-stu-id="8a988-115">The first command gets a database object by using the **Get-AzureSqlRecoverableDatabase** cmdlet.</span></span>
<span data-ttu-id="8a988-116">Il comando Archivia l'oggetto nella variabile $Database.</span><span class="sxs-lookup"><span data-stu-id="8a988-116">The command stores that object in the $Database variable.</span></span>

<span data-ttu-id="8a988-117">Il secondo comando Ripristina il database archiviato in $Database.</span><span class="sxs-lookup"><span data-stu-id="8a988-117">The second command recovers the database stored in $Database.</span></span>

### <span data-ttu-id="8a988-118">Esempio 2: recuperare un database specificato per nome</span><span class="sxs-lookup"><span data-stu-id="8a988-118">Example 2: Recover a database specified by name</span></span>
```
PS C:\> $Operation = Start-AzureSqlDatabaseRecovery -SourceServerName "Server01" -SourceDatabaseName "Database17" -TargetDatabaseName "DatabaseRestored"
```

<span data-ttu-id="8a988-119">Questo comando ripristina un database usando il nome del database.</span><span class="sxs-lookup"><span data-stu-id="8a988-119">This command recovers a database using the database name.</span></span>

## <span data-ttu-id="8a988-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8a988-120">PARAMETERS</span></span>

### <span data-ttu-id="8a988-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="8a988-121">-Profile</span></span>
<span data-ttu-id="8a988-122">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a988-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8a988-123">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="8a988-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8a988-124">-SourceDatabase</span><span class="sxs-lookup"><span data-stu-id="8a988-124">-SourceDatabase</span></span>
<span data-ttu-id="8a988-125">Specifica l'oggetto di database che rappresenta il database che questo cmdlet viene ripristinato.</span><span class="sxs-lookup"><span data-stu-id="8a988-125">Specifies the database object that represents the database that this cmdlet recovers.</span></span>

```yaml
Type: RecoverableDatabase
Parameter Sets: BySourceDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a988-126">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="8a988-126">-SourceDatabaseName</span></span>
<span data-ttu-id="8a988-127">Specifica il nome del database che questo cmdlet viene ripristinato.</span><span class="sxs-lookup"><span data-stu-id="8a988-127">Specifies the name of the database that this cmdlet recovers.</span></span>

```yaml
Type: String
Parameter Sets: BySourceDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a988-128">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="8a988-128">-SourceServerName</span></span>
<span data-ttu-id="8a988-129">Specifica il nome del server in cui il database di origine è in esecuzione o in cui è stato eseguito il database di origine prima dell'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="8a988-129">Specifies the name of the server on which the source database is live and running, or on which the source database ran before it was deleted.</span></span>

```yaml
Type: String
Parameter Sets: BySourceDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a988-130">-NomeDatabaseDestinazione</span><span class="sxs-lookup"><span data-stu-id="8a988-130">-TargetDatabaseName</span></span>
<span data-ttu-id="8a988-131">Specifica il nome del database recuperato.</span><span class="sxs-lookup"><span data-stu-id="8a988-131">Specifies the name of the recovered database.</span></span>
<span data-ttu-id="8a988-132">Se il database di origine è ancora attivo, per recuperarlo nello stesso server è necessario specificare un nome diverso dal nome del database di origine.</span><span class="sxs-lookup"><span data-stu-id="8a988-132">If the source database is still live, in order to recover it to the same server, you must specify a name that differs from the source database name.</span></span>

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

### <span data-ttu-id="8a988-133">-TargetServerName</span><span class="sxs-lookup"><span data-stu-id="8a988-133">-TargetServerName</span></span>
<span data-ttu-id="8a988-134">Specifica il nome del server a cui ripristinare un database.</span><span class="sxs-lookup"><span data-stu-id="8a988-134">Specifies the name of the server to which to restore a database.</span></span>
<span data-ttu-id="8a988-135">È possibile ripristinare un database nello stesso server o in un server diverso.</span><span class="sxs-lookup"><span data-stu-id="8a988-135">You can restore a database to the same server or to a different server.</span></span>

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

### <span data-ttu-id="8a988-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a988-136">CommonParameters</span></span>
<span data-ttu-id="8a988-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a988-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a988-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a988-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a988-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8a988-139">INPUTS</span></span>

### <span data-ttu-id="8a988-140">Microsoft. WindowsAzure. Management. SQL. Models. RecoverableDatabase</span><span class="sxs-lookup"><span data-stu-id="8a988-140">Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase</span></span>

## <span data-ttu-id="8a988-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8a988-141">OUTPUTS</span></span>

### <span data-ttu-id="8a988-142">Microsoft. WindowsAzure. Management. SQL. Models. RecoverDatabaseOperation</span><span class="sxs-lookup"><span data-stu-id="8a988-142">Microsoft.WindowsAzure.Management.Sql.Models.RecoverDatabaseOperation</span></span>

## <span data-ttu-id="8a988-143">Note</span><span class="sxs-lookup"><span data-stu-id="8a988-143">NOTES</span></span>
* <span data-ttu-id="8a988-144">Per eseguire questo cmdlet, è necessario usare l'autenticazione basata su certificati.</span><span class="sxs-lookup"><span data-stu-id="8a988-144">You must use certificate-based authentication to run this cmdlet.</span></span> <span data-ttu-id="8a988-145">Eseguire i comandi seguenti nel computer in cui si esegue questo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="8a988-145">Run the following commands on the computer where you run this cmdlet:</span></span> 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## <span data-ttu-id="8a988-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8a988-146">RELATED LINKS</span></span>

[<span data-ttu-id="8a988-147">Database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="8a988-147">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="8a988-148">Creare una richiesta di ripristino di database</span><span class="sxs-lookup"><span data-stu-id="8a988-148">Create Database Recovery Request</span></span>](https://msdn.microsoft.com/en-us/library/dn800986.aspx)

[<span data-ttu-id="8a988-149">Geo-replica in Azure SQL database</span><span class="sxs-lookup"><span data-stu-id="8a988-149">Geo-Replication in Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/)

[<span data-ttu-id="8a988-150">Operazioni per i database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="8a988-150">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="8a988-151">Get-AzureSqlRecoverableDatabase</span><span class="sxs-lookup"><span data-stu-id="8a988-151">Get-AzureSqlRecoverableDatabase</span></span>](./Get-AzureSqlRecoverableDatabase.md)

[<span data-ttu-id="8a988-152">Start-AzureSqlDatabaseRestore</span><span class="sxs-lookup"><span data-stu-id="8a988-152">Start-AzureSqlDatabaseRestore</span></span>](./Start-AzureSqlDatabaseRestore.md)


