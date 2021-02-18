---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: CB601E21-424D-4B09-85E5-A4B2A5068267
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7716587787515221a6e016436a6e3d030c1ab0eb
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405619"
---
# <span data-ttu-id="38881-101">Stop-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="38881-101">Stop-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="38881-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38881-102">SYNOPSIS</span></span>
<span data-ttu-id="38881-103">Termina una relazione di copia continua.</span><span class="sxs-lookup"><span data-stu-id="38881-103">Terminates a continuous copy relationship.</span></span>

## <span data-ttu-id="38881-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="38881-104">SYNTAX</span></span>

### <span data-ttu-id="38881-105">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="38881-105">ByInputObject</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-ForcedTermination] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38881-106">PerDatabase</span><span class="sxs-lookup"><span data-stu-id="38881-106">ByDatabase</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="38881-107">ByDatabaseName</span><span class="sxs-lookup"><span data-stu-id="38881-107">ByDatabaseName</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="38881-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="38881-108">DESCRIPTION</span></span>
<span data-ttu-id="38881-109">Il **cmdlet Stop-AzureSqlDatabaseCopy** termina una relazione di copia continua.</span><span class="sxs-lookup"><span data-stu-id="38881-109">The **Stop-AzureSqlDatabaseCopy** cmdlet terminates a continuous copy relationship.</span></span>
<span data-ttu-id="38881-110">Questo cmdlet interrompe lo spostamento di dati tra il database di origine e il database secondario o di destinazione e quindi modifica lo stato del database secondario in un database online autonomo.</span><span class="sxs-lookup"><span data-stu-id="38881-110">This cmdlet stops the data movement between the source database and secondary or target database, and then changes the state of the secondary database to be a stand-alone online database.</span></span>

<span data-ttu-id="38881-111">Esistono due modi per terminare una relazione continua con la copia, la risoluzione o la risoluzione pianificata e la risoluzione forzata con possibile perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="38881-111">There are two ways to end a continuous copy relationship, termination or planned termination and forced termination with possible data loss.</span></span>
<span data-ttu-id="38881-112">Nel server che ospita il database di origine è possibile eseguire questo cmdlet in modalità di terminazione forzata o di terminazione forzata.</span><span class="sxs-lookup"><span data-stu-id="38881-112">On the server that hosts the source database, you can run this cmdlet in termination or forced termination mode.</span></span>
<span data-ttu-id="38881-113">Nel server che ospita il database secondario è necessario usare la modalità di terminazione forzata.</span><span class="sxs-lookup"><span data-stu-id="38881-113">On the server that hosts the secondary database, you must use forced termination mode.</span></span>

<span data-ttu-id="38881-114">Una terminazione pianificata attende che tutte le transazioni commit nel database di origine, nel momento in cui si esegue il cmdlet, vengano replicate nel database secondario.</span><span class="sxs-lookup"><span data-stu-id="38881-114">A planned termination waits until all committed transactions on the source database, at the time that you run the cmdlet, have been replicated to the secondary database.</span></span>
<span data-ttu-id="38881-115">La terminazione forzata non attende la replica delle transazioni in sospeso e può causare la perdita di dati nel database secondario.</span><span class="sxs-lookup"><span data-stu-id="38881-115">Forced termination does not wait for replication of any outstanding committed transactions, and can cause possible data loss in the secondary database.</span></span>

<span data-ttu-id="38881-116">Mentre lo stato della replica è IN SOSPESO, solo la terminazione forzata può terminare correttamente una relazione di copia continua.</span><span class="sxs-lookup"><span data-stu-id="38881-116">While replication status is PENDING, only forced termination can successfully end a continuous copy relationship.</span></span>
<span data-ttu-id="38881-117">Se lo stato della replica è IN SOSPESO, la terminazione non forzata non è supportata.</span><span class="sxs-lookup"><span data-stu-id="38881-117">If the replication status is PENDING, termination that is not forced is not supported.</span></span>

## <span data-ttu-id="38881-118">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="38881-118">EXAMPLES</span></span>

### <span data-ttu-id="38881-119">Esempio 1: Terminare una relazione di copia continua</span><span class="sxs-lookup"><span data-stu-id="38881-119">Example 1: Terminate a continuous copy relationship</span></span>
```
PS C:\>Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

<span data-ttu-id="38881-120">Questo comando termina la relazione di copia continua del database denominato Ordini nel server denominato lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="38881-120">This command terminates the continuous copy relationship of database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="38881-121">Il server bk0b8kf658 ospita il database secondario.</span><span class="sxs-lookup"><span data-stu-id="38881-121">The server named bk0b8kf658 hosts the secondary database.</span></span>

### <span data-ttu-id="38881-122">Esempio 2: Interrompere forzatamente una relazione di copia continua</span><span class="sxs-lookup"><span data-stu-id="38881-122">Example 2: Forcibly terminate a continuous copy relationship</span></span>
```
PS C:\>$DatabaseCopy = Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders"
PS C:\> $DatabaseCopy | Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -ForcedTermination
```

<span data-ttu-id="38881-123">Il primo comando recupera la relazione di copia del database per il database denominato Ordini nel server denominato lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="38881-123">The first command gets the database copy relationship for the database named Orders on the server named lpqd0zbr8y.</span></span>

<span data-ttu-id="38881-124">Il secondo comando termina forzatamente una relazione di copia continua dal server che ospita il database secondario.</span><span class="sxs-lookup"><span data-stu-id="38881-124">The second command forcibly terminates a continuous copy relationship from the server that hosts the secondary database.</span></span>

## <span data-ttu-id="38881-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38881-125">PARAMETERS</span></span>

### <span data-ttu-id="38881-126">-Database</span><span class="sxs-lookup"><span data-stu-id="38881-126">-Database</span></span>
<span data-ttu-id="38881-127">Specifica un oggetto che rappresenta l'origine SQL database di Azure.</span><span class="sxs-lookup"><span data-stu-id="38881-127">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="38881-128">Questo cmdlet termina la relazione di copia continua del database specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="38881-128">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>

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

### <span data-ttu-id="38881-129">-DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="38881-129">-DatabaseCopy</span></span>
<span data-ttu-id="38881-130">Specifica un oggetto che rappresenta un database.</span><span class="sxs-lookup"><span data-stu-id="38881-130">Specifies an object that represents a database.</span></span>
<span data-ttu-id="38881-131">Questo cmdlet termina la relazione di copia continua del database specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="38881-131">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>
<span data-ttu-id="38881-132">Questo parametro accetta l'input della pipeline.</span><span class="sxs-lookup"><span data-stu-id="38881-132">This parameter accepts pipeline input.</span></span>

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

### <span data-ttu-id="38881-133">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="38881-133">-DatabaseName</span></span>
<span data-ttu-id="38881-134">Specifica il nome di un database.</span><span class="sxs-lookup"><span data-stu-id="38881-134">Specifies the name of a database.</span></span>
<span data-ttu-id="38881-135">Questo cmdlet termina la relazione di copia continua del database specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="38881-135">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>

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

### <span data-ttu-id="38881-136">-Force</span><span class="sxs-lookup"><span data-stu-id="38881-136">-Force</span></span>
<span data-ttu-id="38881-137">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="38881-137">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="38881-138">-ForcedTermination</span><span class="sxs-lookup"><span data-stu-id="38881-138">-ForcedTermination</span></span>
<span data-ttu-id="38881-139">Indica che questo cmdlet causa la terminazione forzata della relazione di copia continua.</span><span class="sxs-lookup"><span data-stu-id="38881-139">Indicates that this cmdlet causes forced termination of the continuous copy relationship.</span></span>
<span data-ttu-id="38881-140">La risoluzione forzata può causare la perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="38881-140">Forced termination may cause with data loss.</span></span>
<span data-ttu-id="38881-141">Per eseguire questo cmdlet in un server che ospita il database di destinazione, è necessario specificare questo parametro.</span><span class="sxs-lookup"><span data-stu-id="38881-141">To run this cmdlet on a server that hosts the target database, you must specify this parameter.</span></span>
<span data-ttu-id="38881-142">Per eseguire questo cmdlet in un server che ospita il database di origine, se il database secondario non è disponibile, è necessario specificare questo parametro.</span><span class="sxs-lookup"><span data-stu-id="38881-142">To run this cmdlet on a server that hosts the source database, if the secondary database is unavailable, you must specify this parameter.</span></span>

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

### <span data-ttu-id="38881-143">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="38881-143">-PartnerDatabase</span></span>
<span data-ttu-id="38881-144">Specifica il nome del database secondario.</span><span class="sxs-lookup"><span data-stu-id="38881-144">Specifies name of the secondary database.</span></span>
<span data-ttu-id="38881-145">Se si specifica un nome, questo deve corrispondere al nome del database di origine.</span><span class="sxs-lookup"><span data-stu-id="38881-145">If you specify a name, it must match the name of the source database.</span></span>

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

### <span data-ttu-id="38881-146">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="38881-146">-PartnerServer</span></span>
<span data-ttu-id="38881-147">Specifica il nome del server che ospita il database di destinazione.</span><span class="sxs-lookup"><span data-stu-id="38881-147">Specifies the name of the server that hosts the target database.</span></span>

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

### <span data-ttu-id="38881-148">-Profile</span><span class="sxs-lookup"><span data-stu-id="38881-148">-Profile</span></span>
<span data-ttu-id="38881-149">Specifica il profilo di Azure da cui viene letto questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38881-149">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="38881-150">Se non si specifica un profilo, questo cmdlet legge dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="38881-150">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="38881-151">-ServerName</span><span class="sxs-lookup"><span data-stu-id="38881-151">-ServerName</span></span>
<span data-ttu-id="38881-152">Specifica il nome del server in cui si trova il database di origine.</span><span class="sxs-lookup"><span data-stu-id="38881-152">Specifies the name of the server on which the source database resides.</span></span>

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

### <span data-ttu-id="38881-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38881-153">-Confirm</span></span>
<span data-ttu-id="38881-154">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38881-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38881-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38881-155">-WhatIf</span></span>
<span data-ttu-id="38881-156">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38881-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38881-157">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38881-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38881-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38881-158">CommonParameters</span></span>
<span data-ttu-id="38881-159">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38881-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38881-160">Per altre informazioni, vedere about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38881-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38881-161">INPUT</span><span class="sxs-lookup"><span data-stu-id="38881-161">INPUTS</span></span>

### <span data-ttu-id="38881-162">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="38881-162">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

### <span data-ttu-id="38881-163">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span><span class="sxs-lookup"><span data-stu-id="38881-163">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="38881-164">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="38881-164">OUTPUTS</span></span>

### <span data-ttu-id="38881-165">Nessuno</span><span class="sxs-lookup"><span data-stu-id="38881-165">None</span></span>

## <span data-ttu-id="38881-166">NOTE</span><span class="sxs-lookup"><span data-stu-id="38881-166">NOTES</span></span>
* <span data-ttu-id="38881-167">Autenticazione: questo cmdlet richiede l'autenticazione basata su certificato.</span><span class="sxs-lookup"><span data-stu-id="38881-167">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="38881-168">Per un esempio su come usare l'autenticazione basata su certificato per impostare la sottoscrizione corrente, vedere il cmdlet **New-AzureSqlDatabaseServerContext.**</span><span class="sxs-lookup"><span data-stu-id="38881-168">For an example of how to use certificate-based authentication to set the current subscription, see the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
* <span data-ttu-id="38881-169">Restrizioni: nel server che ospita il database secondario è supportata solo la terminazione forzata.</span><span class="sxs-lookup"><span data-stu-id="38881-169">Restrictions: On the server that hosts the secondary database, only forced termination is supported.</span></span>
* <span data-ttu-id="38881-170">Impatto della terminazione sul database secondario precedente: dopo la terminazione, il database secondario diventa un database indipendente.</span><span class="sxs-lookup"><span data-stu-id="38881-170">Impact of termination on the former secondary database: After termination, the secondary database becomes an independent database.</span></span> <span data-ttu-id="38881-171">Se il seeding è già stato completato nel database secondario, dopo la chiusura il database è aperto per l'accesso completo.</span><span class="sxs-lookup"><span data-stu-id="38881-171">If seeding already completed on the secondary database, after termination this database is open for full access.</span></span> <span data-ttu-id="38881-172">Se il database di origine è un database di lettura/scrittura, anche il database secondario precedente diventa un database di lettura-scrittura.</span><span class="sxs-lookup"><span data-stu-id="38881-172">If the source database is a read-write database, the former secondary database becomes a read-write database, too.</span></span>

  <span data-ttu-id="38881-173">Se il seeding è in corso, il seeding viene interrotto e il database secondario precedente non diventa mai visibile nel server che ospita il database secondario.</span><span class="sxs-lookup"><span data-stu-id="38881-173">If seeding is currently in progress, seeding is aborted, and the former secondary database never becomes visible on the server that hosts the secondary database.</span></span>

* <span data-ttu-id="38881-174">È possibile impostare il database di origine sulla modalità di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="38881-174">You can set the source database to read-only mode.</span></span> <span data-ttu-id="38881-175">Questo garantisce la sincronizzazione dei database di origine e secondari dopo la terminazione e garantisce che nessuna transazione sia commessa durante la chiusura.</span><span class="sxs-lookup"><span data-stu-id="38881-175">This guarantees that source and secondary databases are synchronized after termination, and makes sure that no transactions are committed during termination.</span></span> <span data-ttu-id="38881-176">Al termine dell'interruzione, impostare di nuovo l'origine sulla modalità di lettura-scrittura.</span><span class="sxs-lookup"><span data-stu-id="38881-176">Once the termination finishes, set the source back to read-write mode.</span></span> <span data-ttu-id="38881-177">Facoltativamente, è anche possibile impostare l'ex database secondario sulla modalità di lettura-scrittura.</span><span class="sxs-lookup"><span data-stu-id="38881-177">Optionally, you can also set the former secondary database to read-write mode.</span></span>
* <span data-ttu-id="38881-178">Monitoraggio: per verificare lo stato delle operazioni sia nell'origine che nella destinazione della relazione di copia continua, usare il cmdlet **Get-AzureSqlDatabaseOperation.**</span><span class="sxs-lookup"><span data-stu-id="38881-178">Monitoring: To verify the status of the operations at both the source and target of the continuous copy relationship, use the **Get-AzureSqlDatabaseOperation** cmdlet.</span></span>

## <span data-ttu-id="38881-179">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="38881-179">RELATED LINKS</span></span>

[<span data-ttu-id="38881-180">Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="38881-180">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="38881-181">Operazioni per i database SQL Azure</span><span class="sxs-lookup"><span data-stu-id="38881-181">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="38881-182">Interrompi copia database</span><span class="sxs-lookup"><span data-stu-id="38881-182">Stop Database Copy</span></span>](https://msdn.microsoft.com/en-us/library/dn509573.aspx)



[<span data-ttu-id="38881-183">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="38881-183">Get-AzureSqlDatabaseCopy</span></span>](./Get-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="38881-184">Start-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="38881-184">Start-AzureSqlDatabaseCopy</span></span>](./Start-AzureSqlDatabaseCopy.md)


