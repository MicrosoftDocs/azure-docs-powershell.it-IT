---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: CB601E21-424D-4B09-85E5-A4B2A5068267
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2b7674cb5b7abc489dc6aa6d3746f499b9686312
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029865"
---
# <span data-ttu-id="445d6-101">Stop-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="445d6-101">Stop-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="445d6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="445d6-102">SYNOPSIS</span></span>
<span data-ttu-id="445d6-103">Termina una relazione di copia continua.</span><span class="sxs-lookup"><span data-stu-id="445d6-103">Terminates a continuous copy relationship.</span></span>

## <span data-ttu-id="445d6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="445d6-104">SYNTAX</span></span>

### <span data-ttu-id="445d6-105">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="445d6-105">ByInputObject</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-ForcedTermination] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="445d6-106">ByDatabase</span><span class="sxs-lookup"><span data-stu-id="445d6-106">ByDatabase</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="445d6-107">ByDatabaseName</span><span class="sxs-lookup"><span data-stu-id="445d6-107">ByDatabaseName</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="445d6-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="445d6-108">DESCRIPTION</span></span>
<span data-ttu-id="445d6-109">Il cmdlet **Stop-AzureSqlDatabaseCopy** termina una relazione di copia continua.</span><span class="sxs-lookup"><span data-stu-id="445d6-109">The **Stop-AzureSqlDatabaseCopy** cmdlet terminates a continuous copy relationship.</span></span>
<span data-ttu-id="445d6-110">Questo cmdlet interrompe lo spostamento dei dati tra il database di origine e il database secondario o di destinazione e quindi modifica lo stato del database secondario in un database online autonomo.</span><span class="sxs-lookup"><span data-stu-id="445d6-110">This cmdlet stops the data movement between the source database and secondary or target database, and then changes the state of the secondary database to be a stand-alone online database.</span></span>

<span data-ttu-id="445d6-111">Esistono due modi per terminare una relazione di copia continua, una terminazione o una terminazione pianificata e una terminazione forzata con possibili perdite di dati.</span><span class="sxs-lookup"><span data-stu-id="445d6-111">There are two ways to end a continuous copy relationship, termination or planned termination and forced termination with possible data loss.</span></span>
<span data-ttu-id="445d6-112">Nel server che ospita il database di origine è possibile eseguire questo cmdlet in modalità terminazione o terminazione forzata.</span><span class="sxs-lookup"><span data-stu-id="445d6-112">On the server that hosts the source database, you can run this cmdlet in termination or forced termination mode.</span></span>
<span data-ttu-id="445d6-113">Nel server che ospita il database secondario è necessario usare la modalità di terminazione forzata.</span><span class="sxs-lookup"><span data-stu-id="445d6-113">On the server that hosts the secondary database, you must use forced termination mode.</span></span>

<span data-ttu-id="445d6-114">Una terminazione pianificata attende che tutte le transazioni impegnate nel database di origine, al momento dell'esecuzione del cmdlet, siano state replicate nel database secondario.</span><span class="sxs-lookup"><span data-stu-id="445d6-114">A planned termination waits until all committed transactions on the source database, at the time that you run the cmdlet, have been replicated to the secondary database.</span></span>
<span data-ttu-id="445d6-115">La terminazione forzata non attende la replica delle transazioni di cui è stato eseguito il commit in sospeso e può causare possibili perdite di dati nel database secondario.</span><span class="sxs-lookup"><span data-stu-id="445d6-115">Forced termination does not wait for replication of any outstanding committed transactions, and can cause possible data loss in the secondary database.</span></span>

<span data-ttu-id="445d6-116">Mentre lo stato di replica è in sospeso, solo la terminazione forzata può terminare correttamente una relazione di copia continua.</span><span class="sxs-lookup"><span data-stu-id="445d6-116">While replication status is PENDING, only forced termination can successfully end a continuous copy relationship.</span></span>
<span data-ttu-id="445d6-117">Se lo stato di replica è in sospeso, la terminazione non forzata non è supportata.</span><span class="sxs-lookup"><span data-stu-id="445d6-117">If the replication status is PENDING, termination that is not forced is not supported.</span></span>

## <span data-ttu-id="445d6-118">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="445d6-118">EXAMPLES</span></span>

### <span data-ttu-id="445d6-119">Esempio 1: terminare una relazione di copia continua</span><span class="sxs-lookup"><span data-stu-id="445d6-119">Example 1: Terminate a continuous copy relationship</span></span>
```
PS C:\>Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

<span data-ttu-id="445d6-120">Questo comando termina la relazione di copia continua del database denominata Orders sul server denominato lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="445d6-120">This command terminates the continuous copy relationship of database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="445d6-121">Il server denominato bk0b8kf658 ospita il database secondario.</span><span class="sxs-lookup"><span data-stu-id="445d6-121">The server named bk0b8kf658 hosts the secondary database.</span></span>

### <span data-ttu-id="445d6-122">Esempio 2: terminazione forzata di una relazione di copia continua</span><span class="sxs-lookup"><span data-stu-id="445d6-122">Example 2: Forcibly terminate a continuous copy relationship</span></span>
```
PS C:\>$DatabaseCopy = Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders"
PS C:\> $DatabaseCopy | Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -ForcedTermination
```

<span data-ttu-id="445d6-123">Il primo comando ottiene la relazione di copia del database per il database denominato Orders nel server denominato lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="445d6-123">The first command gets the database copy relationship for the database named Orders on the server named lpqd0zbr8y.</span></span>

<span data-ttu-id="445d6-124">Il secondo comando termina con forza una relazione di copia continua dal server che ospita il database secondario.</span><span class="sxs-lookup"><span data-stu-id="445d6-124">The second command forcibly terminates a continuous copy relationship from the server that hosts the secondary database.</span></span>

## <span data-ttu-id="445d6-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="445d6-125">PARAMETERS</span></span>

### <span data-ttu-id="445d6-126">-Database</span><span class="sxs-lookup"><span data-stu-id="445d6-126">-Database</span></span>
<span data-ttu-id="445d6-127">Specifica un oggetto che rappresenta il database SQL di Azure di origine.</span><span class="sxs-lookup"><span data-stu-id="445d6-127">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="445d6-128">Questo cmdlet termina la relazione di copia continua del database specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="445d6-128">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>

```yaml
Type: Database
Parameter Sets: ByDatabase
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="445d6-129">-DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="445d6-129">-DatabaseCopy</span></span>
<span data-ttu-id="445d6-130">Specifica un oggetto che rappresenta un database.</span><span class="sxs-lookup"><span data-stu-id="445d6-130">Specifies an object that represents a database.</span></span>
<span data-ttu-id="445d6-131">Questo cmdlet termina la relazione di copia continua del database specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="445d6-131">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>
<span data-ttu-id="445d6-132">Questo parametro accetta l'input della pipeline.</span><span class="sxs-lookup"><span data-stu-id="445d6-132">This parameter accepts pipeline input.</span></span>

```yaml
Type: DatabaseCopy
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="445d6-133">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="445d6-133">-DatabaseName</span></span>
<span data-ttu-id="445d6-134">Specifica il nome di un database.</span><span class="sxs-lookup"><span data-stu-id="445d6-134">Specifies the name of a database.</span></span>
<span data-ttu-id="445d6-135">Questo cmdlet termina la relazione di copia continua del database specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="445d6-135">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="445d6-136">-Force</span><span class="sxs-lookup"><span data-stu-id="445d6-136">-Force</span></span>
<span data-ttu-id="445d6-137">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="445d6-137">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="445d6-138">-ForcedTermination</span><span class="sxs-lookup"><span data-stu-id="445d6-138">-ForcedTermination</span></span>
<span data-ttu-id="445d6-139">Indica che questo cmdlet causa la terminazione forzata della relazione di copia continua.</span><span class="sxs-lookup"><span data-stu-id="445d6-139">Indicates that this cmdlet causes forced termination of the continuous copy relationship.</span></span>
<span data-ttu-id="445d6-140">La terminazione forzata può causare la perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="445d6-140">Forced termination may cause with data loss.</span></span>
<span data-ttu-id="445d6-141">Per eseguire questo cmdlet in un server che ospita il database di destinazione, è necessario specificare questo parametro.</span><span class="sxs-lookup"><span data-stu-id="445d6-141">To run this cmdlet on a server that hosts the target database, you must specify this parameter.</span></span>
<span data-ttu-id="445d6-142">Per eseguire questo cmdlet in un server che ospita il database di origine, se il database secondario non è disponibile, è necessario specificare questo parametro.</span><span class="sxs-lookup"><span data-stu-id="445d6-142">To run this cmdlet on a server that hosts the source database, if the secondary database is unavailable, you must specify this parameter.</span></span>

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

### <span data-ttu-id="445d6-143">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="445d6-143">-PartnerDatabase</span></span>
<span data-ttu-id="445d6-144">Specifica il nome del database secondario.</span><span class="sxs-lookup"><span data-stu-id="445d6-144">Specifies name of the secondary database.</span></span>
<span data-ttu-id="445d6-145">Se specifichi un nome, deve corrispondere al nome del database di origine.</span><span class="sxs-lookup"><span data-stu-id="445d6-145">If you specify a name, it must match the name of the source database.</span></span>

```yaml
Type: String
Parameter Sets: ByDatabase, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="445d6-146">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="445d6-146">-PartnerServer</span></span>
<span data-ttu-id="445d6-147">Specifica il nome del server che ospita il database di destinazione.</span><span class="sxs-lookup"><span data-stu-id="445d6-147">Specifies the name of the server that hosts the target database.</span></span>

```yaml
Type: String
Parameter Sets: ByDatabase, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="445d6-148">-Profile</span><span class="sxs-lookup"><span data-stu-id="445d6-148">-Profile</span></span>
<span data-ttu-id="445d6-149">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="445d6-149">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="445d6-150">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="445d6-150">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="445d6-151">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="445d6-151">-ServerName</span></span>
<span data-ttu-id="445d6-152">Specifica il nome del server in cui risiede il database di origine.</span><span class="sxs-lookup"><span data-stu-id="445d6-152">Specifies the name of the server on which the source database resides.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="445d6-153">-Confermare</span><span class="sxs-lookup"><span data-stu-id="445d6-153">-Confirm</span></span>
<span data-ttu-id="445d6-154">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="445d6-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="445d6-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="445d6-155">-WhatIf</span></span>
<span data-ttu-id="445d6-156">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="445d6-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="445d6-157">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="445d6-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="445d6-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="445d6-158">CommonParameters</span></span>
<span data-ttu-id="445d6-159">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="445d6-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="445d6-160">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="445d6-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="445d6-161">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="445d6-161">INPUTS</span></span>

### <span data-ttu-id="445d6-162">Microsoft. WindowsAzure. Commands. SqlDatabase. Model. DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="445d6-162">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

### <span data-ttu-id="445d6-163">Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. database</span><span class="sxs-lookup"><span data-stu-id="445d6-163">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="445d6-164">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="445d6-164">OUTPUTS</span></span>

### <span data-ttu-id="445d6-165">Nessuno</span><span class="sxs-lookup"><span data-stu-id="445d6-165">None</span></span>

## <span data-ttu-id="445d6-166">Note</span><span class="sxs-lookup"><span data-stu-id="445d6-166">NOTES</span></span>
* <span data-ttu-id="445d6-167">Autenticazione: questo cmdlet richiede l'autenticazione basata su certificati.</span><span class="sxs-lookup"><span data-stu-id="445d6-167">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="445d6-168">Per un esempio di come usare l'autenticazione basata su certificati per impostare la sottoscrizione corrente, vedere il cmdlet **New-AzureSqlDatabaseServerContext** .</span><span class="sxs-lookup"><span data-stu-id="445d6-168">For an example of how to use certificate-based authentication to set the current subscription, see the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
* <span data-ttu-id="445d6-169">Restrizioni: nel server che ospita il database secondario è supportata solo la terminazione forzata.</span><span class="sxs-lookup"><span data-stu-id="445d6-169">Restrictions: On the server that hosts the secondary database, only forced termination is supported.</span></span>
* <span data-ttu-id="445d6-170">Impatto della terminazione nell'ex database secondario: dopo la terminazione, il database secondario diventa un database indipendente.</span><span class="sxs-lookup"><span data-stu-id="445d6-170">Impact of termination on the former secondary database: After termination, the secondary database becomes an independent database.</span></span> <span data-ttu-id="445d6-171">Se i seeding sono già stati completati nel database secondario, dopo la terminazione questo database è aperto per l'accesso completo.</span><span class="sxs-lookup"><span data-stu-id="445d6-171">If seeding already completed on the secondary database, after termination this database is open for full access.</span></span> <span data-ttu-id="445d6-172">Se il database di origine è un database di lettura e scrittura, anche il database secondario precedente diventa un database di lettura e scrittura.</span><span class="sxs-lookup"><span data-stu-id="445d6-172">If the source database is a read-write database, the former secondary database becomes a read-write database, too.</span></span>

  <span data-ttu-id="445d6-173">Se il seeding è attualmente in corso, il seeding viene interrotto e il database secondario precedente non diventa mai visibile nel server che ospita il database secondario.</span><span class="sxs-lookup"><span data-stu-id="445d6-173">If seeding is currently in progress, seeding is aborted, and the former secondary database never becomes visible on the server that hosts the secondary database.</span></span>

* <span data-ttu-id="445d6-174">Puoi impostare il database di origine in modalità di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="445d6-174">You can set the source database to read-only mode.</span></span> <span data-ttu-id="445d6-175">Questo garantisce che i database di origine e secondari vengano sincronizzati dopo la terminazione e che non vengano commessi transazioni durante la terminazione.</span><span class="sxs-lookup"><span data-stu-id="445d6-175">This guarantees that source and secondary databases are synchronized after termination, and makes sure that no transactions are committed during termination.</span></span> <span data-ttu-id="445d6-176">Una volta terminata la terminazione, riportare la sorgente in modalità di lettura-scrittura.</span><span class="sxs-lookup"><span data-stu-id="445d6-176">Once the termination finishes, set the source back to read-write mode.</span></span> <span data-ttu-id="445d6-177">Facoltativamente, è anche possibile impostare il database secondario precedente in modalità di lettura-scrittura.</span><span class="sxs-lookup"><span data-stu-id="445d6-177">Optionally, you can also set the former secondary database to read-write mode.</span></span>
* <span data-ttu-id="445d6-178">Monitoraggio: per verificare lo stato delle operazioni sia per l'origine che per la destinazione della relazione di copia continua, usare il cmdlet **Get-AzureSqlDatabaseOperation** .</span><span class="sxs-lookup"><span data-stu-id="445d6-178">Monitoring: To verify the status of the operations at both the source and target of the continuous copy relationship, use the **Get-AzureSqlDatabaseOperation** cmdlet.</span></span>

## <span data-ttu-id="445d6-179">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="445d6-179">RELATED LINKS</span></span>

[<span data-ttu-id="445d6-180">Database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="445d6-180">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="445d6-181">Operazioni per i database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="445d6-181">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="445d6-182">Interrompi copia database</span><span class="sxs-lookup"><span data-stu-id="445d6-182">Stop Database Copy</span></span>](https://msdn.microsoft.com/en-us/library/dn509573.aspx)

[<span data-ttu-id="445d6-183">Cmdlet di database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="445d6-183">Azure SQL Database Cmdlets</span></span>](./Azure.SQLDatabase.md)

[<span data-ttu-id="445d6-184">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="445d6-184">Get-AzureSqlDatabaseCopy</span></span>](./Get-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="445d6-185">Start-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="445d6-185">Start-AzureSqlDatabaseCopy</span></span>](./Start-AzureSqlDatabaseCopy.md)


