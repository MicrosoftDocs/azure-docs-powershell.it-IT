---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 82F4DB8F-8DAF-40D2-8031-3EDBF5D08417
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6274d3851042c15791707807471ae1bc6a2733ab
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023823"
---
# <span data-ttu-id="c4134-101">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c4134-101">Set-AzureSqlDatabase</span></span>

## <span data-ttu-id="c4134-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c4134-102">SYNOPSIS</span></span>
<span data-ttu-id="c4134-103">Imposta le proprietà per un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="c4134-103">Sets properties for an Azure SQL Database.</span></span>

## <span data-ttu-id="c4134-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c4134-104">SYNTAX</span></span>

### <span data-ttu-id="c4134-105">ByNameWithConnectionContext</span><span class="sxs-lookup"><span data-stu-id="c4134-105">ByNameWithConnectionContext</span></span>
```
Set-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String>
 [-NewDatabaseName <String>] [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4134-106">ByObjectWithConnectionContext</span><span class="sxs-lookup"><span data-stu-id="c4134-106">ByObjectWithConnectionContext</span></span>
```
Set-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -Database <Database>
 [-NewDatabaseName <String>] [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4134-107">ByNameWithServerName</span><span class="sxs-lookup"><span data-stu-id="c4134-107">ByNameWithServerName</span></span>
```
Set-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-NewDatabaseName <String>]
 [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4134-108">ByObjectWithServerName</span><span class="sxs-lookup"><span data-stu-id="c4134-108">ByObjectWithServerName</span></span>
```
Set-AzureSqlDatabase -ServerName <String> -Database <Database> [-NewDatabaseName <String>]
 [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4134-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c4134-109">DESCRIPTION</span></span>
<span data-ttu-id="c4134-110">Il cmdlet **set-AzureSqlDatabase** imposta le proprietà per un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="c4134-110">The **Set-AzureSqlDatabase** cmdlet sets properties for an Azure SQL Database.</span></span>
<span data-ttu-id="c4134-111">Puoi specificare il database per nome o passare un oggetto database SQL di Azure tramite la pipeline.</span><span class="sxs-lookup"><span data-stu-id="c4134-111">You can specify the database by name, or pass an Azure SQL Database object through the pipeline.</span></span>
<span data-ttu-id="c4134-112">Puoi specificare il server per nome o passare un contesto di connessione al server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="c4134-112">You can specify the server by name, or pass an Azure SQL Database server connection context.</span></span>
<span data-ttu-id="c4134-113">Creare un contesto di connessione eseguendo il cmdlet **New-AzureSqlDatabaseServerContext** .</span><span class="sxs-lookup"><span data-stu-id="c4134-113">Create a connection context by running the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
<span data-ttu-id="c4134-114">Se specifichi il server per nome, il cmdlet usa le informazioni correnti sull'abbonamento a Azure per autenticare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="c4134-114">If you specify the server by name, the cmdlet uses the current Azure subscription information to authenticate the request.</span></span>

## <span data-ttu-id="c4134-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c4134-115">EXAMPLES</span></span>

### <span data-ttu-id="c4134-116">Esempio 1: modificare le dimensioni di un database tramite un contesto di connessione</span><span class="sxs-lookup"><span data-stu-id="c4134-116">Example 1: Change the size of a database by using a connection context</span></span>
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
PS C:\> Set-AzureSqlDatabase -ConnectionContext $Context -Database $Database01 -MaxSizeGB 20
```

<span data-ttu-id="c4134-117">In questo esempio vengono modificate le dimensioni del database denominato Database01 a 20 GB, nel contesto di connessione del server di database SQL di Azure $Context.</span><span class="sxs-lookup"><span data-stu-id="c4134-117">This example changes the size of the database named Database01 to 20 GB, in the Azure SQL Database server connection context $Context.</span></span>

### <span data-ttu-id="c4134-118">Esempio 2: modificare le dimensioni di un database usando un nome di server</span><span class="sxs-lookup"><span data-stu-id="c4134-118">Example 2: Change the size of a database by using a server name</span></span>
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
PS C:\> Set-AzureSqlDatabase -ServerName "lpqd0zbr8y" -Database $Database01 -MaxSizeGB 20
```

<span data-ttu-id="c4134-119">Questo esempio modifica le dimensioni del database denominato Database01 in 20 GB nel server denominato lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="c4134-119">This example changes the size of the database named Database01 to 20 GB in the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="c4134-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c4134-120">PARAMETERS</span></span>

### <span data-ttu-id="c4134-121">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="c4134-121">-ConnectionContext</span></span>
<span data-ttu-id="c4134-122">Specifica il contesto di connessione di un server.</span><span class="sxs-lookup"><span data-stu-id="c4134-122">Specifies the connection context of a server.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByNameWithConnectionContext, ByObjectWithConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4134-123">-Database</span><span class="sxs-lookup"><span data-stu-id="c4134-123">-Database</span></span>
<span data-ttu-id="c4134-124">Specifica un oggetto che rappresenta il database SQL di Azure modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4134-124">Specifies an object that represents the Azure SQL Database that this cmdlet modifies.</span></span>

```yaml
Type: Database
Parameter Sets: ByObjectWithConnectionContext, ByObjectWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4134-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c4134-125">-DatabaseName</span></span>
<span data-ttu-id="c4134-126">Specifica il nome del database modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4134-126">Specifies the name of the database that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: ByNameWithConnectionContext, ByNameWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4134-127">-Edition</span><span class="sxs-lookup"><span data-stu-id="c4134-127">-Edition</span></span>
<span data-ttu-id="c4134-128">Specifica la nuova edizione per il database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="c4134-128">Specifies the new edition for the Azure SQL Database.</span></span>
<span data-ttu-id="c4134-129">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="c4134-129">Valid values are:</span></span> 

- <span data-ttu-id="c4134-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c4134-130">None</span></span>
- <span data-ttu-id="c4134-131">Web</span><span class="sxs-lookup"><span data-stu-id="c4134-131">Web</span></span>
- <span data-ttu-id="c4134-132">Business</span><span class="sxs-lookup"><span data-stu-id="c4134-132">Business</span></span>
- <span data-ttu-id="c4134-133">Base</span><span class="sxs-lookup"><span data-stu-id="c4134-133">Basic</span></span>
- <span data-ttu-id="c4134-134">Standard</span><span class="sxs-lookup"><span data-stu-id="c4134-134">Standard</span></span>
-  <span data-ttu-id="c4134-135">Premium</span><span class="sxs-lookup"><span data-stu-id="c4134-135">Premium</span></span>

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

### <span data-ttu-id="c4134-136">-Force</span><span class="sxs-lookup"><span data-stu-id="c4134-136">-Force</span></span>
<span data-ttu-id="c4134-137">Consente di completare l'azione senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="c4134-137">Allows the action to complete without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="c4134-138">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="c4134-138">-MaxSizeBytes</span></span>
<span data-ttu-id="c4134-139">Specifica le nuove dimensioni massime per il database in byte.</span><span class="sxs-lookup"><span data-stu-id="c4134-139">Specifies the new maximum size for the database in bytes.</span></span>
<span data-ttu-id="c4134-140">Puoi specificare questo parametro o il parametro *MaxSizeGB* .</span><span class="sxs-lookup"><span data-stu-id="c4134-140">You can specify either this parameter or the *MaxSizeGB* parameter.</span></span>
<span data-ttu-id="c4134-141">Vedere il parametro *MaxSizeGB* per i valori accettabili in base a Edition.</span><span class="sxs-lookup"><span data-stu-id="c4134-141">See the *MaxSizeGB* parameter for acceptable values based on edition.</span></span>

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

### <span data-ttu-id="c4134-142">-MaxSizeGB</span><span class="sxs-lookup"><span data-stu-id="c4134-142">-MaxSizeGB</span></span>
<span data-ttu-id="c4134-143">Specifica le nuove dimensioni massime per il database in gigabyte.</span><span class="sxs-lookup"><span data-stu-id="c4134-143">Specifies the new maximum size for the database in gigabytes.</span></span>
<span data-ttu-id="c4134-144">Puoi specificare questo parametro o il parametro *MaxSizeBytes* .</span><span class="sxs-lookup"><span data-stu-id="c4134-144">You can specify either this parameter or the *MaxSizeBytes* parameter.</span></span>
<span data-ttu-id="c4134-145">I valori accettabili variano in base all'edizione.</span><span class="sxs-lookup"><span data-stu-id="c4134-145">The acceptable values differ based on edition.</span></span>

<span data-ttu-id="c4134-146">Valori di base dell'edizione: 1 o 2</span><span class="sxs-lookup"><span data-stu-id="c4134-146">Basic Edition values: 1 or 2</span></span>

<span data-ttu-id="c4134-147">Valori standard dell'edizione: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200 o 250</span><span class="sxs-lookup"><span data-stu-id="c4134-147">Standard Edition values: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, or 250</span></span>

<span data-ttu-id="c4134-148">Valori di edizione Premium: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300, 400 o 500</span><span class="sxs-lookup"><span data-stu-id="c4134-148">Premium Edition values: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300, 400, or 500</span></span>

<span data-ttu-id="c4134-149">Valori di Web Edition: 1 o 5</span><span class="sxs-lookup"><span data-stu-id="c4134-149">Web Edition values: 1 or 5</span></span>

<span data-ttu-id="c4134-150">Valori di Business Edition: 10, 20, 30, 40, 50, 100 o 150</span><span class="sxs-lookup"><span data-stu-id="c4134-150">Business Edition values: 10, 20, 30, 40, 50, 100, or 150</span></span>

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

### <span data-ttu-id="c4134-151">-NewDatabaseName</span><span class="sxs-lookup"><span data-stu-id="c4134-151">-NewDatabaseName</span></span>
<span data-ttu-id="c4134-152">Specifica il nuovo nome del database.</span><span class="sxs-lookup"><span data-stu-id="c4134-152">Specifies the new name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NewName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4134-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4134-153">-PassThru</span></span>
<span data-ttu-id="c4134-154">Restituisce il database SQL di Azure aggiornato.</span><span class="sxs-lookup"><span data-stu-id="c4134-154">Returns the updated Azure SQL Database.</span></span>

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

### <span data-ttu-id="c4134-155">-Profile</span><span class="sxs-lookup"><span data-stu-id="c4134-155">-Profile</span></span>
<span data-ttu-id="c4134-156">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4134-156">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c4134-157">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="c4134-157">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c4134-158">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="c4134-158">-ServerName</span></span>
<span data-ttu-id="c4134-159">Specifica il nome del server che contiene il database modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4134-159">Specifies the name of the server that contains the database that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: ByNameWithServerName, ByObjectWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4134-160">-ServiceObjective</span><span class="sxs-lookup"><span data-stu-id="c4134-160">-ServiceObjective</span></span>
<span data-ttu-id="c4134-161">Specifica un oggetto che rappresenta il nuovo obiettivo del servizio (livello di prestazioni) per il database.</span><span class="sxs-lookup"><span data-stu-id="c4134-161">Specifies an object representing the new service objective (performance level) for this database.</span></span>
<span data-ttu-id="c4134-162">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="c4134-162">Valid values are:</span></span> 

- <span data-ttu-id="c4134-163">Base: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c</span><span class="sxs-lookup"><span data-stu-id="c4134-163">Basic: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c</span></span>
- <span data-ttu-id="c4134-164">Standard (S0): f1173c43-91bd-4AAA-973C-54e79e15235b</span><span class="sxs-lookup"><span data-stu-id="c4134-164">Standard (S0): f1173c43-91bd-4aaa-973c-54e79e15235b</span></span>
- <span data-ttu-id="c4134-165">Standard (S1): 1b1ebd4d-D903-4baa-97f9-4ea675f5e928</span><span class="sxs-lookup"><span data-stu-id="c4134-165">Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928</span></span>
- <span data-ttu-id="c4134-166">Standard (S2): 455330e1-00cd-488b-B5FA-177c226f28b7</span><span class="sxs-lookup"><span data-stu-id="c4134-166">Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7</span></span>
- <span data-ttu-id="c4134-167">\* Standard (S3): 789681b8-CA10-4EB0-bdf2-e0b050601b40</span><span class="sxs-lookup"><span data-stu-id="c4134-167">\*Standard (S3): 789681b8-ca10-4eb0-bdf2-e0b050601b40</span></span>
- <span data-ttu-id="c4134-168">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span><span class="sxs-lookup"><span data-stu-id="c4134-168">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span></span>
- <span data-ttu-id="c4134-169">Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0</span><span class="sxs-lookup"><span data-stu-id="c4134-169">Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0</span></span>
- <span data-ttu-id="c4134-170">Premium (P3): a7c4c615-CFB1-464B-b252-925be0a19446</span><span class="sxs-lookup"><span data-stu-id="c4134-170">Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446</span></span>

<span data-ttu-id="c4134-171">\* Standard (S3) fa parte del più recente aggiornamento di database SQL V12 (Preview).</span><span class="sxs-lookup"><span data-stu-id="c4134-171">\*Standard (S3) is part of the Latest SQL Database Update V12 (preview).</span></span>
<span data-ttu-id="c4134-172">Per altre informazioni, vedere Novità di Azure SQL database V12 Preview https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/ .</span><span class="sxs-lookup"><span data-stu-id="c4134-172">For more information, see What's New in the Azure SQL Database V12 Previewhttps://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/.</span></span>

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

### <span data-ttu-id="c4134-173">-Sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="c4134-173">-Sync</span></span>
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

### <span data-ttu-id="c4134-174">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c4134-174">-Confirm</span></span>
<span data-ttu-id="c4134-175">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4134-175">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4134-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4134-176">-WhatIf</span></span>
<span data-ttu-id="c4134-177">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c4134-177">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4134-178">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c4134-178">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4134-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4134-179">CommonParameters</span></span>
<span data-ttu-id="c4134-180">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4134-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4134-181">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4134-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4134-182">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c4134-182">INPUTS</span></span>

### <span data-ttu-id="c4134-183">Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. database</span><span class="sxs-lookup"><span data-stu-id="c4134-183">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="c4134-184">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c4134-184">OUTPUTS</span></span>

### <span data-ttu-id="c4134-185">Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. database</span><span class="sxs-lookup"><span data-stu-id="c4134-185">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="c4134-186">Note</span><span class="sxs-lookup"><span data-stu-id="c4134-186">NOTES</span></span>

## <span data-ttu-id="c4134-187">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c4134-187">RELATED LINKS</span></span>

[<span data-ttu-id="c4134-188">Database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="c4134-188">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="c4134-189">Operazioni per i database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="c4134-189">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="c4134-190">Aggiornare il database</span><span class="sxs-lookup"><span data-stu-id="c4134-190">Update Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505718.aspx)

[<span data-ttu-id="c4134-191">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c4134-191">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="c4134-192">New-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c4134-192">New-AzureSqlDatabase</span></span>](./New-AzureSqlDatabase.md)

[<span data-ttu-id="c4134-193">Remove-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c4134-193">Remove-AzureSqlDatabase</span></span>](./Remove-AzureSqlDatabase.md)

[<span data-ttu-id="c4134-194">New-AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="c4134-194">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)


