---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabase.md
ms.openlocfilehash: 283b12ca63f92086369f273b1f04d5e3f0cd1716
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510827"
---
# <span data-ttu-id="f2353-101">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f2353-101">Set-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="f2353-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f2353-102">SYNOPSIS</span></span>
<span data-ttu-id="f2353-103">Imposta le proprietà per un database o sposta un database esistente in un pool elastico.</span><span class="sxs-lookup"><span data-stu-id="f2353-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2353-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f2353-104">SYNTAX</span></span>

### <span data-ttu-id="f2353-105">Update (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f2353-105">Update (Default)</span></span>
```
Set-AzureRmSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f2353-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="f2353-106">VcoreBasedDatabase</span></span>
```
Set-AzureRmSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2353-107">Rinominare</span><span class="sxs-lookup"><span data-stu-id="f2353-107">Rename</span></span>
```
Set-AzureRmSqlDatabase [-DatabaseName] <String> -NewName <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f2353-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f2353-108">DESCRIPTION</span></span>
<span data-ttu-id="f2353-109">Il cmdlet **set-AzureRmSqlDatabase** imposta le proprietà per un database in Azure SQL database.</span><span class="sxs-lookup"><span data-stu-id="f2353-109">The **Set-AzureRmSqlDatabase** cmdlet sets properties for a database in Azure SQL Database.</span></span> <span data-ttu-id="f2353-110">Questo cmdlet può modificare il livello di servizio ( *edizione* ), le prestazioni ( *RequestedServiceObjectiveName* ) e le dimensioni massime di archiviazione ( *MaxSizeBytes* ) per il database.</span><span class="sxs-lookup"><span data-stu-id="f2353-110">This cmdlet can modify the service tier ( *Edition* ), performance level ( *RequestedServiceObjectiveName* ), and storage max size ( *MaxSizeBytes* ) for the database.</span></span>  <span data-ttu-id="f2353-111">Inoltre, puoi specificare il parametro *ElasticPoolName* per trasferire un database in un pool elastico.</span><span class="sxs-lookup"><span data-stu-id="f2353-111">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span> <span data-ttu-id="f2353-112">Se un database è già in un pool elastico, è possibile usare il parametro *RequestedServiceObjectiveName* per trasferire il database da un pool elastico e in un livello di prestazioni per i singoli database.</span><span class="sxs-lookup"><span data-stu-id="f2353-112">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to move the database out of an elastic pool and into a performance level for single databases.</span></span>

## <span data-ttu-id="f2353-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f2353-113">EXAMPLES</span></span>

### <span data-ttu-id="f2353-114">Esempio 1: aggiornare un database in un database S2 standard</span><span class="sxs-lookup"><span data-stu-id="f2353-114">Example 1: Update a database to a Standard S2 database</span></span>
```
PS C:\>Set-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -Edition "Standard" -RequestedServiceObjectiveName "S2"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : 455330e1-00cd-488b-b5fa-177c226f28b7
CurrentServiceObjectiveName   : S2
RequestedServiceObjectiveId   : 455330e1-00cd-488b-b5fa-177c226f28b7
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="f2353-115">Questo comando aggiorna un database denominato Database01 in un database S2 standard in un server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="f2353-115">This command updates a database named Database01 to a Standard S2 database on a server named Server01.</span></span>

### <span data-ttu-id="f2353-116">Esempio 2: aggiungere un database a un pool elastico</span><span class="sxs-lookup"><span data-stu-id="f2353-116">Example 2: Add a database to an elastic pool</span></span>
```
PS C:\>Set-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : d1737d22-a8ea-4de7-9bd0-33395d2a7419
CurrentServiceObjectiveName   : ElasticPool
RequestedServiceObjectiveId   : d1737d22-a8ea-4de7-9bd0-33395d2a7419
RequestedServiceObjectiveName :
ElasticPoolName               : elasticpool01
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="f2353-117">Questo comando aggiunge un database denominato Database01 al pool elastico denominato ElasticPool01 ospitato nel server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="f2353-117">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

### <span data-ttu-id="f2353-118">Esempio 3: modificare le dimensioni massime di archiviazione di un database</span><span class="sxs-lookup"><span data-stu-id="f2353-118">Example 3: Modify the storage max size of a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -MaxSizeBytes 1099511627776
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 1099511627776
Status                        : Online
CreationDate                  : 8/24/2017 9:00:37 AM
CurrentServiceObjectiveId     : 789681b8-ca10-4eb0-bdf2-e0b050601b40
CurrentServiceObjectiveName   : S3
RequestedServiceObjectiveId   : 789681b8-ca10-4eb0-bdf2-e0b050601b40
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="f2353-119">Questo comando aggiorna un database denominato Database01 per impostare la dimensione massima su 1 TB.</span><span class="sxs-lookup"><span data-stu-id="f2353-119">This command updates a database named Database01 to set its max size to 1 TB.</span></span>

## <span data-ttu-id="f2353-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f2353-120">PARAMETERS</span></span>

### <span data-ttu-id="f2353-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f2353-121">-AsJob</span></span>
<span data-ttu-id="f2353-122">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f2353-122">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2353-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="f2353-123">-ComputeGeneration</span></span>
<span data-ttu-id="f2353-124">Generazione di Compute da assegnare.</span><span class="sxs-lookup"><span data-stu-id="f2353-124">The compute generation to assign.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases: Family

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2353-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f2353-125">-DatabaseName</span></span>
<span data-ttu-id="f2353-126">Specifica il nome del database.</span><span class="sxs-lookup"><span data-stu-id="f2353-126">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2353-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2353-127">-DefaultProfile</span></span>
<span data-ttu-id="f2353-128">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f2353-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2353-129">-Edition</span><span class="sxs-lookup"><span data-stu-id="f2353-129">-Edition</span></span>
<span data-ttu-id="f2353-130">Specifica l'edizione per il database.</span><span class="sxs-lookup"><span data-stu-id="f2353-130">Specifies the edition for the database.</span></span>
<span data-ttu-id="f2353-131">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f2353-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f2353-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f2353-132">None</span></span>
- <span data-ttu-id="f2353-133">Base</span><span class="sxs-lookup"><span data-stu-id="f2353-133">Basic</span></span>
- <span data-ttu-id="f2353-134">Standard</span><span class="sxs-lookup"><span data-stu-id="f2353-134">Standard</span></span>
- <span data-ttu-id="f2353-135">Premium</span><span class="sxs-lookup"><span data-stu-id="f2353-135">Premium</span></span>
- <span data-ttu-id="f2353-136">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="f2353-136">DataWarehouse</span></span>
- <span data-ttu-id="f2353-137">Gratuito</span><span class="sxs-lookup"><span data-stu-id="f2353-137">Free</span></span>
- <span data-ttu-id="f2353-138">Tratto</span><span class="sxs-lookup"><span data-stu-id="f2353-138">Stretch</span></span>
- <span data-ttu-id="f2353-139">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="f2353-139">GeneralPurpose</span></span>
- <span data-ttu-id="f2353-140">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="f2353-140">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2353-141">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="f2353-141">-ElasticPoolName</span></span>
<span data-ttu-id="f2353-142">Specifica il nome del pool elastico in cui trasferire il database.</span><span class="sxs-lookup"><span data-stu-id="f2353-142">Specifies name of the elastic pool in which to move the database.</span></span>

```yaml
Type: System.String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2353-143">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="f2353-143">-LicenseType</span></span>
<span data-ttu-id="f2353-144">Tipo di licenza per il database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="f2353-144">The license type for the Azure Sql database.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2353-145">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="f2353-145">-MaxSizeBytes</span></span>
<span data-ttu-id="f2353-146">Dimensione massima del database SQL di Azure in byte.</span><span class="sxs-lookup"><span data-stu-id="f2353-146">The maximum size of the Azure SQL Database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2353-147">-NewName</span><span class="sxs-lookup"><span data-stu-id="f2353-147">-NewName</span></span>
<span data-ttu-id="f2353-148">Nuovo nome a cui rinominare il database.</span><span class="sxs-lookup"><span data-stu-id="f2353-148">The new name to rename the database to.</span></span>

```yaml
Type: System.String
Parameter Sets: Rename
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2353-149">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="f2353-149">-ReadScale</span></span>
<span data-ttu-id="f2353-150">Opzione Leggi scala per assegnare al database SQL di Azure. (Abilitato/disabilitato)</span><span class="sxs-lookup"><span data-stu-id="f2353-150">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseReadScale
Parameter Sets: Update, VcoreBasedDatabase
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2353-151">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="f2353-151">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="f2353-152">Specifica il nome dell'obiettivo del servizio da assegnare al database.</span><span class="sxs-lookup"><span data-stu-id="f2353-152">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="f2353-153">Per informazioni sugli obiettivi del servizio, vedere [livelli di servizio database SQL di Azure e livello di prestazioni](https://msdn.microsoft.com/en-us/library/azure/dn741336.aspx) nella raccolta di Microsoft Developer Network.</span><span class="sxs-lookup"><span data-stu-id="f2353-153">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://msdn.microsoft.com/en-us/library/azure/dn741336.aspx) in the Microsoft Developer Network Library.</span></span>

```yaml
Type: System.String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2353-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2353-154">-ResourceGroupName</span></span>
<span data-ttu-id="f2353-155">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="f2353-155">Specifies the name of resource group to which the server is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2353-156">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="f2353-156">-ServerName</span></span>
<span data-ttu-id="f2353-157">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="f2353-157">Specifies the name of the server that hosts the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2353-158">-Tag</span><span class="sxs-lookup"><span data-stu-id="f2353-158">-Tags</span></span>
<span data-ttu-id="f2353-159">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="f2353-159">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f2353-160">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="f2353-160">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Update, VcoreBasedDatabase
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2353-161">-VCore</span><span class="sxs-lookup"><span data-stu-id="f2353-161">-VCore</span></span>
<span data-ttu-id="f2353-162">Numero Vcore per il database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="f2353-162">The Vcore number for the Azure Sql database</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2353-163">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="f2353-163">-ZoneRedundant</span></span>
<span data-ttu-id="f2353-164">Ridondanza della zona da associare al database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="f2353-164">The zone redundancy to associate with the Azure Sql Database</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2353-165">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f2353-165">-Confirm</span></span>
<span data-ttu-id="f2353-166">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2353-166">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2353-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2353-167">-WhatIf</span></span>
<span data-ttu-id="f2353-168">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f2353-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2353-169">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f2353-169">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2353-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2353-170">CommonParameters</span></span>
<span data-ttu-id="f2353-171">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2353-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2353-172">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2353-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2353-173">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f2353-173">INPUTS</span></span>

### <span data-ttu-id="f2353-174">System. String</span><span class="sxs-lookup"><span data-stu-id="f2353-174">System.String</span></span>

## <span data-ttu-id="f2353-175">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f2353-175">OUTPUTS</span></span>

### <span data-ttu-id="f2353-176">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="f2353-176">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="f2353-177">Note</span><span class="sxs-lookup"><span data-stu-id="f2353-177">NOTES</span></span>

## <span data-ttu-id="f2353-178">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f2353-178">RELATED LINKS</span></span>

[<span data-ttu-id="f2353-179">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f2353-179">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="f2353-180">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f2353-180">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="f2353-181">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f2353-181">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="f2353-182">Curriculum vitae-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f2353-182">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="f2353-183">Suspend-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f2353-183">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="f2353-184">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="f2353-184">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
