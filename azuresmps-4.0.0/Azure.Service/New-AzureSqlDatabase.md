---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F4FE79DB-B481-49BD-A33B-7C642A136890
online version: ''
schema: 2.0.0
ms.openlocfilehash: 588fcf73c258364e41117eed05c62de7eaa231e9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023931"
---
# <span data-ttu-id="56929-101">New-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="56929-101">New-AzureSqlDatabase</span></span>

## <span data-ttu-id="56929-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="56929-102">SYNOPSIS</span></span>
<span data-ttu-id="56929-103">Crea un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="56929-103">Creates an Azure SQL Database.</span></span>

## <span data-ttu-id="56929-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="56929-104">SYNTAX</span></span>

### <span data-ttu-id="56929-105">ByConnectionContext</span><span class="sxs-lookup"><span data-stu-id="56929-105">ByConnectionContext</span></span>
```
New-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String>
 [-Collation <String>] [-Edition <DatabaseEdition>] [-ServiceObjective <ServiceObjective>] [-MaxSizeGB <Int32>]
 [-MaxSizeBytes <Int64>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56929-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="56929-106">ByServerName</span></span>
```
New-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-Collation <String>]
 [-Edition <DatabaseEdition>] [-ServiceObjective <ServiceObjective>] [-MaxSizeGB <Int32>]
 [-MaxSizeBytes <Int64>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56929-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56929-107">DESCRIPTION</span></span>
<span data-ttu-id="56929-108">Il cmdlet **New-AzureSqlDatabase** crea un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="56929-108">The **New-AzureSqlDatabase** cmdlet creates an Azure SQL Database.</span></span>
<span data-ttu-id="56929-109">Puoi specificare il server usando un contesto di connessione del server di database SQL di Azure creato usando il cmdlet **New-AzureSqlDatabaseServerContext** .</span><span class="sxs-lookup"><span data-stu-id="56929-109">You can specify the server by using an Azure SQL Database server connection context that you create using the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
<span data-ttu-id="56929-110">In alternativa, se specifichi il nome del server, il cmdlet usa le informazioni correnti sull'abbonamento a Azure per autenticare la richiesta di accesso al server.</span><span class="sxs-lookup"><span data-stu-id="56929-110">Or, if you specify the server name, the cmdlet uses the current Azure subscription information to authenticate the request to access the server.</span></span>

<span data-ttu-id="56929-111">Quando si crea un nuovo database specificando un server di database SQL di Azure, il cmdlet **New-AzureSqlDatabase** crea un contesto di connessione temporaneo usando il nome del server specificato e le informazioni correnti sull'abbonamento a Azure per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="56929-111">When you create a new database by specifying an Azure SQL Database server, the **New-AzureSqlDatabase** cmdlet creates a temporary connection context using the specified server name and the current Azure subscription information to perform the operation.</span></span>

## <span data-ttu-id="56929-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="56929-112">EXAMPLES</span></span>

### <span data-ttu-id="56929-113">Esempio 1: creare un database</span><span class="sxs-lookup"><span data-stu-id="56929-113">Example 1: Create a database</span></span>
```
PS C:\> $Database01 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01" -Edition "Business" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

<span data-ttu-id="56929-114">Questo comando crea un database SQL di Azure denominato database1, per il contesto di connessione del server di database SQL di Azure $Context.</span><span class="sxs-lookup"><span data-stu-id="56929-114">This command creates an Azure SQL Database named Database1, for the Azure SQL Database server connection context $Context.</span></span>

### <span data-ttu-id="56929-115">Esempio 2: creare un database nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="56929-115">Example 2: Create a database in the current subscription</span></span>
```
PS C:\> $Database01 = New-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01" -Edition "Business" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

<span data-ttu-id="56929-116">Questo esempio crea un database denominato database1, nel server di database SQL di Azure specificato denominato lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="56929-116">This example creates a database named Database1, in the specified Azure SQL Database server named lpqd0zbr8y.</span></span>
<span data-ttu-id="56929-117">Il cmdlet usa le informazioni correnti sull'abbonamento a Azure per autenticare la richiesta di accesso al server.</span><span class="sxs-lookup"><span data-stu-id="56929-117">The cmdlet uses the current Azure subscription information to authenticate the request to access the server.</span></span>

## <span data-ttu-id="56929-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="56929-118">PARAMETERS</span></span>

### <span data-ttu-id="56929-119">-Regole di confronto</span><span class="sxs-lookup"><span data-stu-id="56929-119">-Collation</span></span>
<span data-ttu-id="56929-120">Specifica una regola di confronto per il nuovo database.</span><span class="sxs-lookup"><span data-stu-id="56929-120">Specifies a collation for the new database.</span></span>

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

### <span data-ttu-id="56929-121">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="56929-121">-ConnectionContext</span></span>
<span data-ttu-id="56929-122">Specifica il contesto di connessione di un server in cui questo cmdlet crea un database.</span><span class="sxs-lookup"><span data-stu-id="56929-122">Specifies the connection context of a server where this cmdlet creates a database.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56929-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="56929-123">-DatabaseName</span></span>
<span data-ttu-id="56929-124">Specifica il nome del nuovo database.</span><span class="sxs-lookup"><span data-stu-id="56929-124">Specifies the name of the new database.</span></span>

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

### <span data-ttu-id="56929-125">-Edition</span><span class="sxs-lookup"><span data-stu-id="56929-125">-Edition</span></span>
<span data-ttu-id="56929-126">Specifica l'edizione per il nuovo database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="56929-126">Specifies the edition for the new Azure SQL Database.</span></span>
<span data-ttu-id="56929-127">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="56929-127">Valid values are:</span></span> 

- <span data-ttu-id="56929-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="56929-128">None</span></span>
- <span data-ttu-id="56929-129">Web</span><span class="sxs-lookup"><span data-stu-id="56929-129">Web</span></span>
- <span data-ttu-id="56929-130">Business</span><span class="sxs-lookup"><span data-stu-id="56929-130">Business</span></span>
- <span data-ttu-id="56929-131">Base</span><span class="sxs-lookup"><span data-stu-id="56929-131">Basic</span></span>
- <span data-ttu-id="56929-132">Standard</span><span class="sxs-lookup"><span data-stu-id="56929-132">Standard</span></span>
-  <span data-ttu-id="56929-133">Premium</span><span class="sxs-lookup"><span data-stu-id="56929-133">Premium</span></span>

<span data-ttu-id="56929-134">Il valore predefinito è Web.</span><span class="sxs-lookup"><span data-stu-id="56929-134">The default value is Web.</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56929-135">-Force</span><span class="sxs-lookup"><span data-stu-id="56929-135">-Force</span></span>
<span data-ttu-id="56929-136">Consente di completare l'azione senza richiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="56929-136">Allows the action to complete without prompting the user for confirmation.</span></span>

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

### <span data-ttu-id="56929-137">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="56929-137">-MaxSizeBytes</span></span>
<span data-ttu-id="56929-138">Specifica la dimensione massima del database in byte.</span><span class="sxs-lookup"><span data-stu-id="56929-138">Specifies the maximum size of the database in bytes.</span></span>
<span data-ttu-id="56929-139">Puoi specificare questo parametro o il parametro *MaxSizeGB* .</span><span class="sxs-lookup"><span data-stu-id="56929-139">You can specify either this parameter or the *MaxSizeGB* parameter.</span></span>
<span data-ttu-id="56929-140">Vedere la descrizione del parametro *MaxSizeGB* per i valori accettabili in base a Edition.</span><span class="sxs-lookup"><span data-stu-id="56929-140">See the *MaxSizeGB* parameter description for acceptable values based on edition.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56929-141">-MaxSizeGB</span><span class="sxs-lookup"><span data-stu-id="56929-141">-MaxSizeGB</span></span>
<span data-ttu-id="56929-142">Specifica la dimensione massima del database in gigabyte.</span><span class="sxs-lookup"><span data-stu-id="56929-142">Specifies the maximum size of the database in gigabytes.</span></span>
<span data-ttu-id="56929-143">Puoi specificare questo parametro o il parametro *MaxSizeBytes* .</span><span class="sxs-lookup"><span data-stu-id="56929-143">You can specify either this parameter or the *MaxSizeBytes* parameter.</span></span>
<span data-ttu-id="56929-144">I valori accettabili variano in base all'edizione.</span><span class="sxs-lookup"><span data-stu-id="56929-144">The acceptable values differ based on edition.</span></span>

<span data-ttu-id="56929-145">Valori di base dell'edizione: 1 o 2</span><span class="sxs-lookup"><span data-stu-id="56929-145">Basic Edition values: 1 or 2</span></span>

<span data-ttu-id="56929-146">Valori standard dell'edizione: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200 o 250</span><span class="sxs-lookup"><span data-stu-id="56929-146">Standard Edition values: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, or 250</span></span>

<span data-ttu-id="56929-147">Valori di edizione Premium: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300, 400 o 500</span><span class="sxs-lookup"><span data-stu-id="56929-147">Premium Edition values: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300, 400, or 500</span></span>

<span data-ttu-id="56929-148">Valori di Web Edition: 1 o 5</span><span class="sxs-lookup"><span data-stu-id="56929-148">Web Edition values: 1 or 5</span></span>

<span data-ttu-id="56929-149">Valori di Business Edition: 10, 20, 30, 40, 50, 100 o 150</span><span class="sxs-lookup"><span data-stu-id="56929-149">Business Edition values: 10, 20, 30, 40, 50, 100, or 150</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56929-150">-Profile</span><span class="sxs-lookup"><span data-stu-id="56929-150">-Profile</span></span>
<span data-ttu-id="56929-151">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56929-151">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="56929-152">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="56929-152">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="56929-153">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="56929-153">-ServerName</span></span>
<span data-ttu-id="56929-154">Specifica il nome del server di database SQL di Azure che contiene il nuovo database.</span><span class="sxs-lookup"><span data-stu-id="56929-154">Specifies the name of the Azure SQL Database server to contain the new database.</span></span>

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

### <span data-ttu-id="56929-155">-ServiceObjective</span><span class="sxs-lookup"><span data-stu-id="56929-155">-ServiceObjective</span></span>
<span data-ttu-id="56929-156">Specifica un oggetto che rappresenta il nuovo obiettivo del servizio (livello di prestazioni) per il database.</span><span class="sxs-lookup"><span data-stu-id="56929-156">Specifies an object that represent the new service objective (performance level) for this database.</span></span>
<span data-ttu-id="56929-157">Questo valore rappresenta il livello di risorse assegnate a questo database.</span><span class="sxs-lookup"><span data-stu-id="56929-157">This value represents the level of resources assigned to this database.</span></span>
<span data-ttu-id="56929-158">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="56929-158">Valid values are:</span></span> 

<span data-ttu-id="56929-159">Basic: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c standard (S0): f1173c43-91bd-4AAA-973C-54e79e15235b standard (S1): 1b1ebd4d-D903-4baa-97f9-4ea675f5e928 standard (S2): 455330e1-00cd-488b-B5FA-177c226f28b7 \* standard (S3): 789681b8-CA10-4EB0-bdf2-e0b050601b40 Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0 Premium (P3): a7c4c615-CFB1-464B-b252-925be0a19446</span><span class="sxs-lookup"><span data-stu-id="56929-159">Basic: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c Standard (S0): f1173c43-91bd-4aaa-973c-54e79e15235b Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928 Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7 \*Standard (S3): 789681b8-ca10-4eb0-bdf2-e0b050601b40 Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0 Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446</span></span>

<span data-ttu-id="56929-160">\* Standard (S3) fa parte del più recente aggiornamento di database SQL V12 (Preview).</span><span class="sxs-lookup"><span data-stu-id="56929-160">\*Standard (S3) is part of the Latest SQL Database Update V12 (preview).</span></span>
<span data-ttu-id="56929-161">Per altre informazioni, vedere Novità di Azure SQL database V12 Preview https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/ .</span><span class="sxs-lookup"><span data-stu-id="56929-161">For more information, see What's New in the Azure SQL Database V12 Previewhttps://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/.</span></span>

```yaml
Type: ServiceObjective
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56929-162">-Confermare</span><span class="sxs-lookup"><span data-stu-id="56929-162">-Confirm</span></span>
<span data-ttu-id="56929-163">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56929-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56929-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56929-164">-WhatIf</span></span>
<span data-ttu-id="56929-165">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="56929-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56929-166">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="56929-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56929-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56929-167">CommonParameters</span></span>
<span data-ttu-id="56929-168">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56929-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56929-169">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56929-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56929-170">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="56929-170">INPUTS</span></span>

## <span data-ttu-id="56929-171">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="56929-171">OUTPUTS</span></span>

### <span data-ttu-id="56929-172">Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. database</span><span class="sxs-lookup"><span data-stu-id="56929-172">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="56929-173">Note</span><span class="sxs-lookup"><span data-stu-id="56929-173">NOTES</span></span>
* <span data-ttu-id="56929-174">Per eliminare un database creato da **New-AzureSqlDatabase** , usare il cmdlet Remove-AzureSqlDatabase.</span><span class="sxs-lookup"><span data-stu-id="56929-174">To delete a database that was created by **New-AzureSqlDatabase** , use the Remove-AzureSqlDatabase cmdlet.</span></span>

## <span data-ttu-id="56929-175">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="56929-175">RELATED LINKS</span></span>

[<span data-ttu-id="56929-176">Database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="56929-176">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="56929-177">Creare un database</span><span class="sxs-lookup"><span data-stu-id="56929-177">Create Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505701.aspx)

[<span data-ttu-id="56929-178">Operazioni per i database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="56929-178">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="56929-179">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="56929-179">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="56929-180">New-AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="56929-180">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)

[<span data-ttu-id="56929-181">Remove-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="56929-181">Remove-AzureSqlDatabase</span></span>](./Remove-AzureSqlDatabase.md)

[<span data-ttu-id="56929-182">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="56929-182">Set-AzureSqlDatabase</span></span>](./Set-AzureSqlDatabase.md)


