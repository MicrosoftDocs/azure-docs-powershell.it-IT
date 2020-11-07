---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
ms.openlocfilehash: ff474116854838c40a4862cf93f4d017ccdf4527
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676866"
---
# <span data-ttu-id="c6e25-101">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c6e25-101">New-AzSqlDatabase</span></span>

## <span data-ttu-id="c6e25-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c6e25-102">SYNOPSIS</span></span>
<span data-ttu-id="c6e25-103">Crea un database o un database elastico.</span><span class="sxs-lookup"><span data-stu-id="c6e25-103">Creates a database or an elastic database.</span></span>

## <span data-ttu-id="c6e25-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c6e25-104">SYNTAX</span></span>

### <span data-ttu-id="c6e25-105">DtuBasedDatabase (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c6e25-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <String>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6e25-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="c6e25-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] -Edition <String> [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>]
 [-SampleName <String>] [-ZoneRedundant] [-AsJob] -VCore <Int32> -ComputeGeneration <String>
 [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6e25-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c6e25-107">DESCRIPTION</span></span>
<span data-ttu-id="c6e25-108">Il cmdlet **New-AzSqlDatabase** crea un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="c6e25-108">The **New-AzSqlDatabase** cmdlet creates an Azure SQL database.</span></span>
<span data-ttu-id="c6e25-109">Puoi anche creare un database elastico impostando il parametro *ElasticPoolName* su un pool elastico esistente.</span><span class="sxs-lookup"><span data-stu-id="c6e25-109">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="c6e25-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c6e25-110">EXAMPLES</span></span>

### <span data-ttu-id="c6e25-111">Esempio 1: creare un database in un server specificato</span><span class="sxs-lookup"><span data-stu-id="c6e25-111">Example 1: Create a database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
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

<span data-ttu-id="c6e25-112">Questo comando crea un database denominato Database01 nel server Server01.</span><span class="sxs-lookup"><span data-stu-id="c6e25-112">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="c6e25-113">Esempio 2: creare un database elastico in un server specificato</span><span class="sxs-lookup"><span data-stu-id="c6e25-113">Example 2: Create an elastic database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -ElasticPoolName "ElasticPool01"
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

<span data-ttu-id="c6e25-114">Questo comando crea un database denominato Database02 nel pool elastico denominato ElasticPool01 nel server Server01.</span><span class="sxs-lookup"><span data-stu-id="c6e25-114">This command creates a database named Database02 in the elastic pool named ElasticPool01 on server Server01.</span></span>

### <span data-ttu-id="c6e25-115">Esempio 3: creare un database di Vcore in un server specificato</span><span class="sxs-lookup"><span data-stu-id="c6e25-115">Example 3: Create an Vcore database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database03" -Edition "GeneralPurpose" -Vcore 2 -ComputeGeneration "Gen4"
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

<span data-ttu-id="c6e25-116">Questo comando crea un database di Vcore denominato Database03 nel server Server01.</span><span class="sxs-lookup"><span data-stu-id="c6e25-116">This command creates a Vcore database named Database03 on server Server01.</span></span>

## <span data-ttu-id="c6e25-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c6e25-117">PARAMETERS</span></span>

### <span data-ttu-id="c6e25-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c6e25-118">-AsJob</span></span>
<span data-ttu-id="c6e25-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c6e25-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c6e25-120">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="c6e25-120">-CatalogCollation</span></span>
<span data-ttu-id="c6e25-121">Specifica il nome delle regole di confronto del catalogo di database SQL.</span><span class="sxs-lookup"><span data-stu-id="c6e25-121">Specifies the name of the SQL database catalog collation.</span></span>

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

### <span data-ttu-id="c6e25-122">-CollationName</span><span class="sxs-lookup"><span data-stu-id="c6e25-122">-CollationName</span></span>
<span data-ttu-id="c6e25-123">Specifica il nome delle regole di confronto del database SQL.</span><span class="sxs-lookup"><span data-stu-id="c6e25-123">Specifies the name of the SQL database collation.</span></span>

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

### <span data-ttu-id="c6e25-124">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="c6e25-124">-ComputeGeneration</span></span>
<span data-ttu-id="c6e25-125">Generazione di Compute da assegnare.</span><span class="sxs-lookup"><span data-stu-id="c6e25-125">The compute generation to assign.</span></span>

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

### <span data-ttu-id="c6e25-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c6e25-126">-DatabaseName</span></span>
<span data-ttu-id="c6e25-127">Specifica il nome del database.</span><span class="sxs-lookup"><span data-stu-id="c6e25-127">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="c6e25-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6e25-128">-DefaultProfile</span></span>
<span data-ttu-id="c6e25-129">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c6e25-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6e25-130">-Edition</span><span class="sxs-lookup"><span data-stu-id="c6e25-130">-Edition</span></span>
<span data-ttu-id="c6e25-131">Specifica l'edizione da assegnare al database.</span><span class="sxs-lookup"><span data-stu-id="c6e25-131">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="c6e25-132">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c6e25-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c6e25-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c6e25-133">None</span></span>
- <span data-ttu-id="c6e25-134">Base</span><span class="sxs-lookup"><span data-stu-id="c6e25-134">Basic</span></span>
- <span data-ttu-id="c6e25-135">Standard</span><span class="sxs-lookup"><span data-stu-id="c6e25-135">Standard</span></span>
- <span data-ttu-id="c6e25-136">Premium</span><span class="sxs-lookup"><span data-stu-id="c6e25-136">Premium</span></span>
- <span data-ttu-id="c6e25-137">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="c6e25-137">DataWarehouse</span></span>
- <span data-ttu-id="c6e25-138">Gratuito</span><span class="sxs-lookup"><span data-stu-id="c6e25-138">Free</span></span>
- <span data-ttu-id="c6e25-139">Tratto</span><span class="sxs-lookup"><span data-stu-id="c6e25-139">Stretch</span></span>
- <span data-ttu-id="c6e25-140">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="c6e25-140">GeneralPurpose</span></span>
- <span data-ttu-id="c6e25-141">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="c6e25-141">BusinessCritical</span></span>

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

### <span data-ttu-id="c6e25-142">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="c6e25-142">-ElasticPoolName</span></span>
<span data-ttu-id="c6e25-143">Specifica il nome del pool elastico in cui inserire il database.</span><span class="sxs-lookup"><span data-stu-id="c6e25-143">Specifies the name of the elastic pool in which to put the database.</span></span>

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

### <span data-ttu-id="c6e25-144">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="c6e25-144">-LicenseType</span></span>
<span data-ttu-id="c6e25-145">Tipo di licenza per il database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="c6e25-145">The license type for the Azure Sql database.</span></span> <span data-ttu-id="c6e25-146">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="c6e25-146">Possible values are:</span></span>
- <span data-ttu-id="c6e25-147">BasePrice-Azure Hybrid benefit (AHB) i prezzi scontati per i proprietari di licenze di SQL Server esistenti vengono applicati.</span><span class="sxs-lookup"><span data-stu-id="c6e25-147">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="c6e25-148">Il prezzo del database verrà scontato per i proprietari di licenze di SQL Server esistenti.</span><span class="sxs-lookup"><span data-stu-id="c6e25-148">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="c6e25-149">LicenseIncluded-Azure Hybrid benefit (AHB) i prezzi di sconto per i proprietari di licenze di SQL Server esistenti non vengono applicati.</span><span class="sxs-lookup"><span data-stu-id="c6e25-149">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="c6e25-150">Prezzo database includerà un nuovo costo per la licenza di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c6e25-150">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="c6e25-151">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="c6e25-151">-MaxSizeBytes</span></span>
<span data-ttu-id="c6e25-152">Specifica la dimensione massima del database in byte.</span><span class="sxs-lookup"><span data-stu-id="c6e25-152">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="c6e25-153">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="c6e25-153">-ReadScale</span></span>
<span data-ttu-id="c6e25-154">Opzione Leggi scala per assegnare al database SQL di Azure. (Abilitato/disabilitato)</span><span class="sxs-lookup"><span data-stu-id="c6e25-154">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

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

### <span data-ttu-id="c6e25-155">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="c6e25-155">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="c6e25-156">Specifica il nome dell'obiettivo del servizio da assegnare al database.</span><span class="sxs-lookup"><span data-stu-id="c6e25-156">Specifies the name of the service objective to assign to the database.</span></span>

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

### <span data-ttu-id="c6e25-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6e25-157">-ResourceGroupName</span></span>
<span data-ttu-id="c6e25-158">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="c6e25-158">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="c6e25-159">-Samplename</span><span class="sxs-lookup"><span data-stu-id="c6e25-159">-SampleName</span></span>
<span data-ttu-id="c6e25-160">Nome dello schema di esempio da applicare quando si crea questo database.</span><span class="sxs-lookup"><span data-stu-id="c6e25-160">The name of the sample schema to apply when creating this database.</span></span>

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

### <span data-ttu-id="c6e25-161">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="c6e25-161">-ServerName</span></span>
<span data-ttu-id="c6e25-162">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="c6e25-162">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="c6e25-163">-Tag</span><span class="sxs-lookup"><span data-stu-id="c6e25-163">-Tags</span></span>
<span data-ttu-id="c6e25-164">Specifica un dizionario di coppie chiave-valore in forma di tabella hash che questo cmdlet associa al nuovo database.</span><span class="sxs-lookup"><span data-stu-id="c6e25-164">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="c6e25-165">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="c6e25-165">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c6e25-166">-VCore</span><span class="sxs-lookup"><span data-stu-id="c6e25-166">-VCore</span></span>
<span data-ttu-id="c6e25-167">Numero Vcore per il database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="c6e25-167">The Vcore number for the Azure Sql database</span></span>

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

### <span data-ttu-id="c6e25-168">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="c6e25-168">-ZoneRedundant</span></span>
<span data-ttu-id="c6e25-169">Ridondanza della zona da associare al database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="c6e25-169">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="c6e25-170">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c6e25-170">-Confirm</span></span>
<span data-ttu-id="c6e25-171">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6e25-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6e25-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6e25-172">-WhatIf</span></span>
<span data-ttu-id="c6e25-173">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c6e25-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6e25-174">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c6e25-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6e25-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6e25-175">CommonParameters</span></span>
<span data-ttu-id="c6e25-176">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6e25-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6e25-177">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c6e25-177">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6e25-178">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c6e25-178">INPUTS</span></span>

### <span data-ttu-id="c6e25-179">System. String</span><span class="sxs-lookup"><span data-stu-id="c6e25-179">System.String</span></span>

## <span data-ttu-id="c6e25-180">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c6e25-180">OUTPUTS</span></span>

### <span data-ttu-id="c6e25-181">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="c6e25-181">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="c6e25-182">Note</span><span class="sxs-lookup"><span data-stu-id="c6e25-182">NOTES</span></span>

## <span data-ttu-id="c6e25-183">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c6e25-183">RELATED LINKS</span></span>

[<span data-ttu-id="c6e25-184">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c6e25-184">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="c6e25-185">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c6e25-185">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="c6e25-186">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="c6e25-186">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="c6e25-187">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c6e25-187">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="c6e25-188">Curriculum vitae-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c6e25-188">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="c6e25-189">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c6e25-189">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="c6e25-190">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c6e25-190">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="c6e25-191">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="c6e25-191">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
