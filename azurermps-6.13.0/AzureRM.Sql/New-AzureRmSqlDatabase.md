---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
ms.openlocfilehash: 7eaa753b973b887cbbddc132b998d05f3e374e3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687567"
---
# <span data-ttu-id="2919c-101">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2919c-101">New-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="2919c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2919c-102">SYNOPSIS</span></span>
<span data-ttu-id="2919c-103">Crea un database o un database elastico.</span><span class="sxs-lookup"><span data-stu-id="2919c-103">Creates a database or an elastic database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2919c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2919c-104">SYNTAX</span></span>

### <span data-ttu-id="2919c-105">DtuBasedDatabase (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2919c-105">DtuBasedDatabase (Default)</span></span>
```
New-AzureRmSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <String>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2919c-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="2919c-106">VcoreBasedDatabase</span></span>
```
New-AzureRmSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] -Edition <String> [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>]
 [-SampleName <String>] [-ZoneRedundant] [-AsJob] -VCore <Int32> -ComputeGeneration <String>
 [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2919c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2919c-107">DESCRIPTION</span></span>
<span data-ttu-id="2919c-108">Il cmdlet **New-AzureRmSqlDatabase** crea un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="2919c-108">The **New-AzureRmSqlDatabase** cmdlet creates an Azure SQL database.</span></span>
<span data-ttu-id="2919c-109">Puoi anche creare un database elastico impostando il parametro *ElasticPoolName* su un pool elastico esistente.</span><span class="sxs-lookup"><span data-stu-id="2919c-109">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="2919c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2919c-110">EXAMPLES</span></span>

### <span data-ttu-id="2919c-111">Esempio 1: creare un database in un server specificato</span><span class="sxs-lookup"><span data-stu-id="2919c-111">Example 1: Create a database on a specified server</span></span>
```
PS C:\>New-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
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
CurrentServiceObjectiveId     : f1173c43-91bd-4aaa-973c-54e79e15235b
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : f1173c43-91bd-4aaa-973c-54e79e15235b
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
LicenseType                   :
Tags                          :
```

<span data-ttu-id="2919c-112">Questo comando crea un database denominato Database01 nel server Server01.</span><span class="sxs-lookup"><span data-stu-id="2919c-112">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="2919c-113">Esempio 2: creare un database elastico in un server specificato</span><span class="sxs-lookup"><span data-stu-id="2919c-113">Example 2: Create an elastic database on a specified server</span></span>
```
PS C:\>New-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -ElasticPoolName "ElasticPool01"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database02
Location                      : Central US
DatabaseId                    : 7bd9d561-42a7-484e-bf05-62ddef8015ab
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 8/26/2015 10:04:29 PM
CurrentServiceObjectiveId     : d1737d22-a8ea-4de7-9bd0-33395d2a7419
CurrentServiceObjectiveName   : ElasticPool
RequestedServiceObjectiveId   : d1737d22-a8ea-4de7-9bd0-33395d2a7419
RequestedServiceObjectiveName :
ElasticPoolName               : ElasticPool01
EarliestRestoreDate           :
LicenseType                   :
Tags                          :
```

<span data-ttu-id="2919c-114">Questo comando crea un database denominato Database02 nel pool elastico denominato ElasticPool01 nel server Server01.</span><span class="sxs-lookup"><span data-stu-id="2919c-114">This command creates a database named Database02 in the elastic pool named ElasticPool01 on server Server01.</span></span>

### <span data-ttu-id="2919c-115">Esempio 3: creare un database di Vcore in un server specificato</span><span class="sxs-lookup"><span data-stu-id="2919c-115">Example 3: Create an Vcore database on a specified server</span></span>
```
PS C:\>New-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database03" -Edition "GeneralPurpose" -Vcore 2 -ComputeGeneration "Gen4"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database03
Location                      : Central US
DatabaseId                    : 34d9d561-42a7-484e-bf05-62ddef8000ab
Edition                       : GeneralPurpose
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 8/26/2015 10:04:29 PM
CurrentServiceObjectiveName   : GP_Gen4_2
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
LicenseType                   : LicenseIncluded
Tags                          :
```

<span data-ttu-id="2919c-116">Questo comando crea un database di Vcore denominato Database03 nel server Server01.</span><span class="sxs-lookup"><span data-stu-id="2919c-116">This command creates a Vcore database named Database03 on server Server01.</span></span>

## <span data-ttu-id="2919c-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2919c-117">PARAMETERS</span></span>

### <span data-ttu-id="2919c-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2919c-118">-AsJob</span></span>
<span data-ttu-id="2919c-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="2919c-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2919c-120">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="2919c-120">-CatalogCollation</span></span>
<span data-ttu-id="2919c-121">Specifica il nome delle regole di confronto del catalogo di database SQL.</span><span class="sxs-lookup"><span data-stu-id="2919c-121">Specifies the name of the SQL database catalog collation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2919c-122">-CollationName</span><span class="sxs-lookup"><span data-stu-id="2919c-122">-CollationName</span></span>
<span data-ttu-id="2919c-123">Specifica il nome delle regole di confronto del database SQL.</span><span class="sxs-lookup"><span data-stu-id="2919c-123">Specifies the name of the SQL database collation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2919c-124">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="2919c-124">-ComputeGeneration</span></span>
<span data-ttu-id="2919c-125">Generazione di Compute da assegnare.</span><span class="sxs-lookup"><span data-stu-id="2919c-125">The compute generation to assign.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases: Family

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2919c-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2919c-126">-DatabaseName</span></span>
<span data-ttu-id="2919c-127">Specifica il nome del database.</span><span class="sxs-lookup"><span data-stu-id="2919c-127">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2919c-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2919c-128">-DefaultProfile</span></span>
<span data-ttu-id="2919c-129">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2919c-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2919c-130">-Edition</span><span class="sxs-lookup"><span data-stu-id="2919c-130">-Edition</span></span>
<span data-ttu-id="2919c-131">Specifica l'edizione da assegnare al database.</span><span class="sxs-lookup"><span data-stu-id="2919c-131">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="2919c-132">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="2919c-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2919c-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2919c-133">None</span></span>
- <span data-ttu-id="2919c-134">Base</span><span class="sxs-lookup"><span data-stu-id="2919c-134">Basic</span></span>
- <span data-ttu-id="2919c-135">Standard</span><span class="sxs-lookup"><span data-stu-id="2919c-135">Standard</span></span>
- <span data-ttu-id="2919c-136">Premium</span><span class="sxs-lookup"><span data-stu-id="2919c-136">Premium</span></span>
- <span data-ttu-id="2919c-137">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="2919c-137">DataWarehouse</span></span>
- <span data-ttu-id="2919c-138">Gratuito</span><span class="sxs-lookup"><span data-stu-id="2919c-138">Free</span></span>
- <span data-ttu-id="2919c-139">Tratto</span><span class="sxs-lookup"><span data-stu-id="2919c-139">Stretch</span></span>
- <span data-ttu-id="2919c-140">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="2919c-140">GeneralPurpose</span></span>
- <span data-ttu-id="2919c-141">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="2919c-141">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2919c-142">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="2919c-142">-ElasticPoolName</span></span>
<span data-ttu-id="2919c-143">Specifica il nome del pool elastico in cui inserire il database.</span><span class="sxs-lookup"><span data-stu-id="2919c-143">Specifies the name of the elastic pool in which to put the database.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2919c-144">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="2919c-144">-LicenseType</span></span>
<span data-ttu-id="2919c-145">Tipo di licenza per il database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="2919c-145">The license type for the Azure Sql database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2919c-146">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="2919c-146">-MaxSizeBytes</span></span>
<span data-ttu-id="2919c-147">Specifica la dimensione massima del database in byte.</span><span class="sxs-lookup"><span data-stu-id="2919c-147">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2919c-148">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="2919c-148">-ReadScale</span></span>
<span data-ttu-id="2919c-149">Opzione Leggi scala per assegnare al database SQL di Azure. (Abilitato/disabilitato)</span><span class="sxs-lookup"><span data-stu-id="2919c-149">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseReadScale
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2919c-150">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="2919c-150">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="2919c-151">Specifica il nome dell'obiettivo del servizio da assegnare al database.</span><span class="sxs-lookup"><span data-stu-id="2919c-151">Specifies the name of the service objective to assign to the database.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2919c-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2919c-152">-ResourceGroupName</span></span>
<span data-ttu-id="2919c-153">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="2919c-153">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="2919c-154">-Samplename</span><span class="sxs-lookup"><span data-stu-id="2919c-154">-SampleName</span></span>
<span data-ttu-id="2919c-155">Nome dello schema di esempio da applicare quando si crea questo database.</span><span class="sxs-lookup"><span data-stu-id="2919c-155">The name of the sample schema to apply when creating this database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AdventureWorksLT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2919c-156">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="2919c-156">-ServerName</span></span>
<span data-ttu-id="2919c-157">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="2919c-157">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="2919c-158">-Tag</span><span class="sxs-lookup"><span data-stu-id="2919c-158">-Tags</span></span>
<span data-ttu-id="2919c-159">Specifica un dizionario di coppie chiave-valore in forma di tabella hash che questo cmdlet associa al nuovo database.</span><span class="sxs-lookup"><span data-stu-id="2919c-159">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="2919c-160">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="2919c-160">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2919c-161">-VCore</span><span class="sxs-lookup"><span data-stu-id="2919c-161">-VCore</span></span>
<span data-ttu-id="2919c-162">Numero Vcore per il database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="2919c-162">The Vcore number for the Azure Sql database</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2919c-163">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="2919c-163">-ZoneRedundant</span></span>
<span data-ttu-id="2919c-164">Ridondanza della zona da associare al database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="2919c-164">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="2919c-165">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2919c-165">-Confirm</span></span>
<span data-ttu-id="2919c-166">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2919c-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2919c-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2919c-167">-WhatIf</span></span>
<span data-ttu-id="2919c-168">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2919c-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2919c-169">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2919c-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2919c-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2919c-170">CommonParameters</span></span>
<span data-ttu-id="2919c-171">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2919c-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2919c-172">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2919c-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2919c-173">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2919c-173">INPUTS</span></span>

### <span data-ttu-id="2919c-174">System. String</span><span class="sxs-lookup"><span data-stu-id="2919c-174">System.String</span></span>

## <span data-ttu-id="2919c-175">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2919c-175">OUTPUTS</span></span>

### <span data-ttu-id="2919c-176">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="2919c-176">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="2919c-177">Note</span><span class="sxs-lookup"><span data-stu-id="2919c-177">NOTES</span></span>

## <span data-ttu-id="2919c-178">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2919c-178">RELATED LINKS</span></span>

[<span data-ttu-id="2919c-179">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2919c-179">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="2919c-180">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2919c-180">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="2919c-181">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="2919c-181">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="2919c-182">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2919c-182">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="2919c-183">Curriculum vitae-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2919c-183">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="2919c-184">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2919c-184">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="2919c-185">Suspend-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2919c-185">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="2919c-186">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="2919c-186">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

