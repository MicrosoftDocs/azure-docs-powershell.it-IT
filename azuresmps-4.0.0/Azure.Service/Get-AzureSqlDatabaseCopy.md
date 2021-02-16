---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5AEF7D44-624D-4794-86FF-156E6729BB56
online version: ''
schema: 2.0.0
ms.openlocfilehash: 95e276bf6af11698a4b3b82077175ec2ede2d7dc
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402423"
---
# <span data-ttu-id="56899-101">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="56899-101">Get-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="56899-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56899-102">SYNOPSIS</span></span>
<span data-ttu-id="56899-103">Controlla lo stato delle relazioni di copia.</span><span class="sxs-lookup"><span data-stu-id="56899-103">Checks the status of copy relationships.</span></span>

## <span data-ttu-id="56899-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="56899-104">SYNTAX</span></span>

### <span data-ttu-id="56899-105">ByServerNameOnly (Default)</span><span class="sxs-lookup"><span data-stu-id="56899-105">ByServerNameOnly (Default)</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> [-DatabaseName <String>] [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="56899-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="56899-106">ByInputObject</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="56899-107">PerDatabase</span><span class="sxs-lookup"><span data-stu-id="56899-107">ByDatabase</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="56899-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="56899-108">DESCRIPTION</span></span>
<span data-ttu-id="56899-109">Il **cmdlet Get-AzureSqlDatabaseCopy** controlla lo stato di una o più relazioni di copia attive.</span><span class="sxs-lookup"><span data-stu-id="56899-109">The **Get-AzureSqlDatabaseCopy** cmdlet checks the status of one or more active copy relationships.</span></span>
<span data-ttu-id="56899-110">Eseguire questo cmdlet dopo aver eseguito il cmdlet Start-AzureSqlDatabaseCopy o Stop-AzureSqlDatabaseCopy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56899-110">Run this cmdlet after you run the Start-AzureSqlDatabaseCopy or Stop-AzureSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="56899-111">È possibile verificare una relazione di copia specifica, tutte le relazioni di copia o un elenco filtrato di relazioni di copia, ad esempio tutte le copie in uno specifico server di destinazione.</span><span class="sxs-lookup"><span data-stu-id="56899-111">You can check a specific copy relationship, all copy relationships, or a filtered list of copy relationships, such as all copies on a specific target server.</span></span>
<span data-ttu-id="56899-112">È possibile eseguire questo cmdlet nel server che ospita il database di origine o di destinazione.</span><span class="sxs-lookup"><span data-stu-id="56899-112">You can run this cmdlet on the server that hosts the source or target database.</span></span>

<span data-ttu-id="56899-113">Questo cmdlet è sincrono.</span><span class="sxs-lookup"><span data-stu-id="56899-113">This cmdlet is synchronous.</span></span>
<span data-ttu-id="56899-114">Il cmdlet blocca la console di Azure PowerShell finché non restituisce un oggetto di stato.</span><span class="sxs-lookup"><span data-stu-id="56899-114">The cmdlet blocks the Azure PowerShell console until it returns a status object.</span></span>

<span data-ttu-id="56899-115">I *parametri PartnerServer* e *PartnerDatabase* sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="56899-115">The *PartnerServer* and *PartnerDatabase* parameters are optional.</span></span>
<span data-ttu-id="56899-116">Se nessuno dei due parametri viene specificato, questo cmdlet restituisce una tabella dei risultati.</span><span class="sxs-lookup"><span data-stu-id="56899-116">If you do not specify either parameter, this cmdlet returns a table of results.</span></span>
<span data-ttu-id="56899-117">Per visualizzare lo stato solo per un database specifico, specificare entrambi i parametri.</span><span class="sxs-lookup"><span data-stu-id="56899-117">To see the status for only a particular database, specify both parameters.</span></span>

## <span data-ttu-id="56899-118">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="56899-118">EXAMPLES</span></span>

### <span data-ttu-id="56899-119">Esempio 1: Ottenere lo stato di copia di un database</span><span class="sxs-lookup"><span data-stu-id="56899-119">Example 1: Get the copy status of a database</span></span>
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

<span data-ttu-id="56899-120">Questo comando ottiene lo stato del database denominato Ordini nel server denominato lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="56899-120">This command gets the status of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="56899-121">Il *parametro PartnerServer* limita questo comando al server bk0b8kf658.</span><span class="sxs-lookup"><span data-stu-id="56899-121">The *PartnerServer* parameter restricts this command to the bk0b8kf658 server.</span></span>

### <span data-ttu-id="56899-122">Esempio 2: Ottenere lo stato di tutte le copie in un serverGet lo stato di tutte le copie in un server</span><span class="sxs-lookup"><span data-stu-id="56899-122">Example 2: Get the status of all copies on a serverGet the status of all copies on a server</span></span>
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="56899-123">Questo comando ottiene lo stato di tutte le copie attive nel server denominato lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="56899-123">This command gets the status of all active copies on the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="56899-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56899-124">PARAMETERS</span></span>

### <span data-ttu-id="56899-125">-Database</span><span class="sxs-lookup"><span data-stu-id="56899-125">-Database</span></span>
<span data-ttu-id="56899-126">Specifica un oggetto che rappresenta l'origine SQL database di Azure.</span><span class="sxs-lookup"><span data-stu-id="56899-126">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="56899-127">Questo cmdlet ottiene lo stato di copia del database specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="56899-127">This cmdlet gets the copy status of the database that this parameter specifies.</span></span>

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

### <span data-ttu-id="56899-128">-DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="56899-128">-DatabaseCopy</span></span>
<span data-ttu-id="56899-129">Specifica un oggetto che rappresenta un database.</span><span class="sxs-lookup"><span data-stu-id="56899-129">Specifies an object that represents a database.</span></span>
<span data-ttu-id="56899-130">Questo cmdlet ottiene lo stato di copia del database specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="56899-130">This cmdlet gets the copy status of the database that this parameter specifies.</span></span>
<span data-ttu-id="56899-131">Questo parametro accetta l'input della pipeline.</span><span class="sxs-lookup"><span data-stu-id="56899-131">This parameter accepts pipeline input.</span></span>

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

### <span data-ttu-id="56899-132">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="56899-132">-DatabaseName</span></span>
<span data-ttu-id="56899-133">Specifica il nome del database di origine.</span><span class="sxs-lookup"><span data-stu-id="56899-133">Specifies the name of the source database.</span></span>
<span data-ttu-id="56899-134">Questo cmdlet ottiene lo stato della copia del database specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="56899-134">This cmdlet gets that copy status of the database that this parameter specifies.</span></span>

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

### <span data-ttu-id="56899-135">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="56899-135">-PartnerDatabase</span></span>
<span data-ttu-id="56899-136">Specifica il nome del database secondario.</span><span class="sxs-lookup"><span data-stu-id="56899-136">Specifies name of the secondary database.</span></span>
<span data-ttu-id="56899-137">Se il database non viene trovato nella visualizzazione sys.dm_database_copies gestione dinamica, questo cmdlet restituisce un oggetto di stato vuoto.</span><span class="sxs-lookup"><span data-stu-id="56899-137">If this database is not found in the sys.dm_database_copies dynamic management view, this cmdlet returns an empty status object.</span></span>

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

### <span data-ttu-id="56899-138">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="56899-138">-PartnerServer</span></span>
<span data-ttu-id="56899-139">Specifica il nome del server che ospita il database di destinazione.</span><span class="sxs-lookup"><span data-stu-id="56899-139">Specifies the name of the server that hosts the target database.</span></span>
<span data-ttu-id="56899-140">Se il server non viene trovato nella visualizzazione sys.dm_database_copies gestione dinamica, questo cmdlet restituisce un oggetto di stato vuoto.</span><span class="sxs-lookup"><span data-stu-id="56899-140">If this server is not found in the sys.dm_database_copies dynamic management view, this cmdlet returns an empty status object.</span></span>

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

### <span data-ttu-id="56899-141">-Profile</span><span class="sxs-lookup"><span data-stu-id="56899-141">-Profile</span></span>
<span data-ttu-id="56899-142">Specifica il profilo di Azure da cui viene letto questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56899-142">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="56899-143">Se non si specifica un profilo, questo cmdlet legge dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="56899-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="56899-144">-ServerName</span><span class="sxs-lookup"><span data-stu-id="56899-144">-ServerName</span></span>
<span data-ttu-id="56899-145">Specifica il nome del server in cui si trova la copia del database.</span><span class="sxs-lookup"><span data-stu-id="56899-145">Specifies the name of the server on which the database copy resides.</span></span>

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

### <span data-ttu-id="56899-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56899-146">CommonParameters</span></span>
<span data-ttu-id="56899-147">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56899-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56899-148">Per altre informazioni, vedere about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56899-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56899-149">INPUT</span><span class="sxs-lookup"><span data-stu-id="56899-149">INPUTS</span></span>

### <span data-ttu-id="56899-150">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="56899-150">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

### <span data-ttu-id="56899-151">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span><span class="sxs-lookup"><span data-stu-id="56899-151">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="56899-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="56899-152">OUTPUTS</span></span>

### <span data-ttu-id="56899-153">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="56899-153">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

## <span data-ttu-id="56899-154">NOTE</span><span class="sxs-lookup"><span data-stu-id="56899-154">NOTES</span></span>
* <span data-ttu-id="56899-155">Autenticazione: questo cmdlet richiede l'autenticazione basata su certificato.</span><span class="sxs-lookup"><span data-stu-id="56899-155">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="56899-156">Per un esempio su come usare l'autenticazione basata su certificato per impostare l'abbonamento corrente, vedere il cmdlet New-AzureSqlDatabaseServerContext certificato.</span><span class="sxs-lookup"><span data-stu-id="56899-156">For an example of how to use certificate-based authentication to set the current subscription, see the New-AzureSqlDatabaseServerContext cmdlet.</span></span>

## <span data-ttu-id="56899-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="56899-157">RELATED LINKS</span></span>

[<span data-ttu-id="56899-158">Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="56899-158">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="56899-159">Operazioni per i database SQL Azure</span><span class="sxs-lookup"><span data-stu-id="56899-159">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)



[<span data-ttu-id="56899-160">Start-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="56899-160">Start-AzureSqlDatabaseCopy</span></span>](./Start-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="56899-161">Stop-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="56899-161">Stop-AzureSqlDatabaseCopy</span></span>](./Stop-AzureSqlDatabaseCopy.md)


