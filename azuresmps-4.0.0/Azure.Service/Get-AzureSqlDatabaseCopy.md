---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5AEF7D44-624D-4794-86FF-156E6729BB56
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8752766572975ef97094a3915446086c903a7fd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029757"
---
# <span data-ttu-id="e8fa3-101">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="e8fa3-101">Get-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="e8fa3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e8fa3-102">SYNOPSIS</span></span>
<span data-ttu-id="e8fa3-103">Controlla lo stato delle relazioni di copia.</span><span class="sxs-lookup"><span data-stu-id="e8fa3-103">Checks the status of copy relationships.</span></span>

## <span data-ttu-id="e8fa3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e8fa3-104">SYNTAX</span></span>

### <span data-ttu-id="e8fa3-105">ByServerNameOnly (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e8fa3-105">ByServerNameOnly (Default)</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> [-DatabaseName <String>] [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e8fa3-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e8fa3-106">ByInputObject</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="e8fa3-107">ByDatabase</span><span class="sxs-lookup"><span data-stu-id="e8fa3-107">ByDatabase</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e8fa3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e8fa3-108">DESCRIPTION</span></span>
<span data-ttu-id="e8fa3-109">Il cmdlet **Get-AzureSqlDatabaseCopy** controlla lo stato di una o più relazioni di copia attive.</span><span class="sxs-lookup"><span data-stu-id="e8fa3-109">The **Get-AzureSqlDatabaseCopy** cmdlet checks the status of one or more active copy relationships.</span></span>
<span data-ttu-id="e8fa3-110">Eseguire questo cmdlet dopo aver eseguito il cmdlet Start-AzureSqlDatabaseCopy o Stop-AzureSqlDatabaseCopy.</span><span class="sxs-lookup"><span data-stu-id="e8fa3-110">Run this cmdlet after you run the Start-AzureSqlDatabaseCopy or Stop-AzureSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="e8fa3-111">È possibile controllare una relazione di copia specifica, tutte le relazioni di copia o un elenco filtrato delle relazioni di copia, ad esempio tutte le copie in uno specifico server di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e8fa3-111">You can check a specific copy relationship, all copy relationships, or a filtered list of copy relationships, such as all copies on a specific target server.</span></span>
<span data-ttu-id="e8fa3-112">Puoi eseguire questo cmdlet nel server che ospita il database di origine o di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e8fa3-112">You can run this cmdlet on the server that hosts the source or target database.</span></span>

<span data-ttu-id="e8fa3-113">Questo cmdlet è sincrono.</span><span class="sxs-lookup"><span data-stu-id="e8fa3-113">This cmdlet is synchronous.</span></span>
<span data-ttu-id="e8fa3-114">Il cmdlet blocca la console di Azure PowerShell fino a quando non restituisce un oggetto stato.</span><span class="sxs-lookup"><span data-stu-id="e8fa3-114">The cmdlet blocks the Azure PowerShell console until it returns a status object.</span></span>

<span data-ttu-id="e8fa3-115">I parametri *PartnerServer* e *PartnerDatabase* sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="e8fa3-115">The *PartnerServer* and *PartnerDatabase* parameters are optional.</span></span>
<span data-ttu-id="e8fa3-116">Se non specifichi un parametro, questo cmdlet restituisce una tabella di risultati.</span><span class="sxs-lookup"><span data-stu-id="e8fa3-116">If you do not specify either parameter, this cmdlet returns a table of results.</span></span>
<span data-ttu-id="e8fa3-117">Per visualizzare lo stato di un solo database specifico, specificare entrambi i parametri.</span><span class="sxs-lookup"><span data-stu-id="e8fa3-117">To see the status for only a particular database, specify both parameters.</span></span>

## <span data-ttu-id="e8fa3-118">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e8fa3-118">EXAMPLES</span></span>

### <span data-ttu-id="e8fa3-119">Esempio 1: ottenere lo stato di copia di un database</span><span class="sxs-lookup"><span data-stu-id="e8fa3-119">Example 1: Get the copy status of a database</span></span>
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

<span data-ttu-id="e8fa3-120">Questo comando ottiene lo stato del database denominato Orders nel server denominato lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="e8fa3-120">This command gets the status of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="e8fa3-121">Il parametro *PartnerServer* limita questo comando al server bk0b8kf658.</span><span class="sxs-lookup"><span data-stu-id="e8fa3-121">The *PartnerServer* parameter restricts this command to the bk0b8kf658 server.</span></span>

### <span data-ttu-id="e8fa3-122">Esempio 2: ottenere lo stato di tutte le copie in un serverGet lo stato di tutte le copie in un server</span><span class="sxs-lookup"><span data-stu-id="e8fa3-122">Example 2: Get the status of all copies on a serverGet the status of all copies on a server</span></span>
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="e8fa3-123">Questo comando consente di ottenere lo stato di tutte le copie attive nel server denominato lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="e8fa3-123">This command gets the status of all active copies on the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="e8fa3-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e8fa3-124">PARAMETERS</span></span>

### <span data-ttu-id="e8fa3-125">-Database</span><span class="sxs-lookup"><span data-stu-id="e8fa3-125">-Database</span></span>
<span data-ttu-id="e8fa3-126">Specifica un oggetto che rappresenta il database SQL di Azure di origine.</span><span class="sxs-lookup"><span data-stu-id="e8fa3-126">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="e8fa3-127">Questo cmdlet ottiene lo stato di copia del database specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="e8fa3-127">This cmdlet gets the copy status of the database that this parameter specifies.</span></span>

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

### <span data-ttu-id="e8fa3-128">-DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="e8fa3-128">-DatabaseCopy</span></span>
<span data-ttu-id="e8fa3-129">Specifica un oggetto che rappresenta un database.</span><span class="sxs-lookup"><span data-stu-id="e8fa3-129">Specifies an object that represents a database.</span></span>
<span data-ttu-id="e8fa3-130">Questo cmdlet ottiene lo stato di copia del database specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="e8fa3-130">This cmdlet gets the copy status of the database that this parameter specifies.</span></span>
<span data-ttu-id="e8fa3-131">Questo parametro accetta l'input della pipeline.</span><span class="sxs-lookup"><span data-stu-id="e8fa3-131">This parameter accepts pipeline input.</span></span>

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

### <span data-ttu-id="e8fa3-132">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e8fa3-132">-DatabaseName</span></span>
<span data-ttu-id="e8fa3-133">Specifica il nome del database di origine.</span><span class="sxs-lookup"><span data-stu-id="e8fa3-133">Specifies the name of the source database.</span></span>
<span data-ttu-id="e8fa3-134">Questo cmdlet ottiene lo stato di copia del database specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="e8fa3-134">This cmdlet gets that copy status of the database that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameOnly
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8fa3-135">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="e8fa3-135">-PartnerDatabase</span></span>
<span data-ttu-id="e8fa3-136">Specifica il nome del database secondario.</span><span class="sxs-lookup"><span data-stu-id="e8fa3-136">Specifies name of the secondary database.</span></span>
<span data-ttu-id="e8fa3-137">Se il database non viene trovato nella sys.dm_database_copies visualizzazione a gestione dinamica, questo cmdlet restituisce un oggetto stato vuoto.</span><span class="sxs-lookup"><span data-stu-id="e8fa3-137">If this database is not found in the sys.dm_database_copies dynamic management view, this cmdlet returns an empty status object.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameOnly, ByDatabase
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8fa3-138">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="e8fa3-138">-PartnerServer</span></span>
<span data-ttu-id="e8fa3-139">Specifica il nome del server che ospita il database di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e8fa3-139">Specifies the name of the server that hosts the target database.</span></span>
<span data-ttu-id="e8fa3-140">Se il server non viene trovato nella sys.dm_database_copies visualizzazione a gestione dinamica, questo cmdlet restituisce un oggetto stato vuoto.</span><span class="sxs-lookup"><span data-stu-id="e8fa3-140">If this server is not found in the sys.dm_database_copies dynamic management view, this cmdlet returns an empty status object.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameOnly, ByDatabase
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8fa3-141">-Profile</span><span class="sxs-lookup"><span data-stu-id="e8fa3-141">-Profile</span></span>
<span data-ttu-id="e8fa3-142">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8fa3-142">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e8fa3-143">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="e8fa3-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e8fa3-144">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="e8fa3-144">-ServerName</span></span>
<span data-ttu-id="e8fa3-145">Specifica il nome del server in cui risiede la copia del database.</span><span class="sxs-lookup"><span data-stu-id="e8fa3-145">Specifies the name of the server on which the database copy resides.</span></span>

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

### <span data-ttu-id="e8fa3-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8fa3-146">CommonParameters</span></span>
<span data-ttu-id="e8fa3-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8fa3-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8fa3-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8fa3-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8fa3-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e8fa3-149">INPUTS</span></span>

### <span data-ttu-id="e8fa3-150">Microsoft. WindowsAzure. Commands. SqlDatabase. Model. DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="e8fa3-150">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

### <span data-ttu-id="e8fa3-151">Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. database</span><span class="sxs-lookup"><span data-stu-id="e8fa3-151">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="e8fa3-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e8fa3-152">OUTPUTS</span></span>

### <span data-ttu-id="e8fa3-153">Microsoft. WindowsAzure. Commands. SqlDatabase. Model. DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="e8fa3-153">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

## <span data-ttu-id="e8fa3-154">Note</span><span class="sxs-lookup"><span data-stu-id="e8fa3-154">NOTES</span></span>
* <span data-ttu-id="e8fa3-155">Autenticazione: questo cmdlet richiede l'autenticazione basata su certificati.</span><span class="sxs-lookup"><span data-stu-id="e8fa3-155">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="e8fa3-156">Per un esempio di come usare l'autenticazione basata su certificati per impostare la sottoscrizione corrente, vedere il cmdlet New-AzureSqlDatabaseServerContext.</span><span class="sxs-lookup"><span data-stu-id="e8fa3-156">For an example of how to use certificate-based authentication to set the current subscription, see the New-AzureSqlDatabaseServerContext cmdlet.</span></span>

## <span data-ttu-id="e8fa3-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e8fa3-157">RELATED LINKS</span></span>

[<span data-ttu-id="e8fa3-158">Database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="e8fa3-158">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="e8fa3-159">Operazioni per i database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="e8fa3-159">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="e8fa3-160">Cmdlet di database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="e8fa3-160">Azure SQL Database Cmdlets</span></span>](./Azure.SQLDatabase.md)

[<span data-ttu-id="e8fa3-161">Start-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="e8fa3-161">Start-AzureSqlDatabaseCopy</span></span>](./Start-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="e8fa3-162">Stop-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="e8fa3-162">Stop-AzureSqlDatabaseCopy</span></span>](./Stop-AzureSqlDatabaseCopy.md)


