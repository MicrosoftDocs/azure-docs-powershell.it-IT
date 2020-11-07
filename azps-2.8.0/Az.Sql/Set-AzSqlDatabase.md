---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
ms.openlocfilehash: dd69e345e5e2bac5ebab0ec4e45c03501ccc8139
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857281"
---
# <span data-ttu-id="31e59-101">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="31e59-101">Set-AzSqlDatabase</span></span>

## <span data-ttu-id="31e59-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="31e59-102">SYNOPSIS</span></span>
<span data-ttu-id="31e59-103">Imposta le proprietà per un database o sposta un database esistente in un pool elastico.</span><span class="sxs-lookup"><span data-stu-id="31e59-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

## <span data-ttu-id="31e59-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="31e59-104">SYNTAX</span></span>

### <span data-ttu-id="31e59-105">Update (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="31e59-105">Update (Default)</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="31e59-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="31e59-106">VcoreBasedDatabase</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="31e59-107">Rinominare</span><span class="sxs-lookup"><span data-stu-id="31e59-107">Rename</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> -NewName <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="31e59-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31e59-108">DESCRIPTION</span></span>
<span data-ttu-id="31e59-109">Il cmdlet **set-AzSqlDatabase** imposta le proprietà per un database in Azure SQL database.</span><span class="sxs-lookup"><span data-stu-id="31e59-109">The **Set-AzSqlDatabase** cmdlet sets properties for a database in Azure SQL Database.</span></span> <span data-ttu-id="31e59-110">Questo cmdlet può modificare il livello di servizio ( *edizione* ), le prestazioni ( *RequestedServiceObjectiveName* ) e le dimensioni massime di archiviazione ( *MaxSizeBytes* ) per il database.</span><span class="sxs-lookup"><span data-stu-id="31e59-110">This cmdlet can modify the service tier ( *Edition* ), performance level ( *RequestedServiceObjectiveName* ), and storage max size ( *MaxSizeBytes* ) for the database.</span></span>  <span data-ttu-id="31e59-111">Inoltre, puoi specificare il parametro *ElasticPoolName* per trasferire un database in un pool elastico.</span><span class="sxs-lookup"><span data-stu-id="31e59-111">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span> <span data-ttu-id="31e59-112">Se un database è già in un pool elastico, è possibile usare il parametro *RequestedServiceObjectiveName* per trasferire il database da un pool elastico e in un livello di prestazioni per i singoli database.</span><span class="sxs-lookup"><span data-stu-id="31e59-112">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to move the database out of an elastic pool and into a performance level for single databases.</span></span>

## <span data-ttu-id="31e59-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="31e59-113">EXAMPLES</span></span>

### <span data-ttu-id="31e59-114">Esempio 1: aggiornare un database in un database S0 standard</span><span class="sxs-lookup"><span data-stu-id="31e59-114">Example 1: Update a database to a Standard S0 database</span></span>
```
PS C:\>Set-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -Edition "Standard" -RequestedServiceObjectiveName "S0"
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
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : 455330e1-00cd-488b-b5fa-177c226f28b7
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="31e59-115">Questo comando aggiorna un database denominato Database01 in un database S0 standard in un server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="31e59-115">This command updates a database named Database01 to a Standard S0 database on a server named Server01.</span></span>

### <span data-ttu-id="31e59-116">Esempio 2: aggiungere un database a un pool elastico</span><span class="sxs-lookup"><span data-stu-id="31e59-116">Example 2: Add a database to an elastic pool</span></span>
```
PS C:\>Set-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
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

<span data-ttu-id="31e59-117">Questo comando aggiunge un database denominato Database01 al pool elastico denominato ElasticPool01 ospitato nel server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="31e59-117">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

### <span data-ttu-id="31e59-118">Esempio 3: modificare le dimensioni massime di archiviazione di un database</span><span class="sxs-lookup"><span data-stu-id="31e59-118">Example 3: Modify the storage max size of a database</span></span>
```
PS C:\>Set-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -MaxSizeBytes 1099511627776
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

<span data-ttu-id="31e59-119">Questo comando aggiorna un database denominato Database01 per impostare la dimensione massima su 1 TB.</span><span class="sxs-lookup"><span data-stu-id="31e59-119">This command updates a database named Database01 to set its max size to 1 TB.</span></span>

## <span data-ttu-id="31e59-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="31e59-120">PARAMETERS</span></span>

### <span data-ttu-id="31e59-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="31e59-121">-AsJob</span></span>
<span data-ttu-id="31e59-122">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="31e59-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="31e59-123">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="31e59-123">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="31e59-124">Ritardo di pausa automatica in minuti per il database (solo server),-1 per rifiutare la disattivazione</span><span class="sxs-lookup"><span data-stu-id="31e59-124">The auto pause delay in minutes for database (serverless only), -1 to opt out</span></span>

```yaml
Type: System.Int32
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31e59-125">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="31e59-125">-ComputeGeneration</span></span>
<span data-ttu-id="31e59-126">Generazione di Compute da assegnare.</span><span class="sxs-lookup"><span data-stu-id="31e59-126">The compute generation to assign.</span></span>

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

### <span data-ttu-id="31e59-127">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="31e59-127">-ComputeModel</span></span>
<span data-ttu-id="31e59-128">Modello calcolato di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="31e59-128">Computed model of Azure Sql database.</span></span> <span data-ttu-id="31e59-129">Server o provisioning</span><span class="sxs-lookup"><span data-stu-id="31e59-129">Serverless or Provisioned</span></span>

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

### <span data-ttu-id="31e59-130">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="31e59-130">-DatabaseName</span></span>
<span data-ttu-id="31e59-131">Specifica il nome del database.</span><span class="sxs-lookup"><span data-stu-id="31e59-131">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="31e59-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31e59-132">-DefaultProfile</span></span>
<span data-ttu-id="31e59-133">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="31e59-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="31e59-134">-Edition</span><span class="sxs-lookup"><span data-stu-id="31e59-134">-Edition</span></span>
<span data-ttu-id="31e59-135">Specifica l'edizione per il database.</span><span class="sxs-lookup"><span data-stu-id="31e59-135">Specifies the edition for the database.</span></span>
<span data-ttu-id="31e59-136">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="31e59-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="31e59-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="31e59-137">None</span></span>
- <span data-ttu-id="31e59-138">Base</span><span class="sxs-lookup"><span data-stu-id="31e59-138">Basic</span></span>
- <span data-ttu-id="31e59-139">Standard</span><span class="sxs-lookup"><span data-stu-id="31e59-139">Standard</span></span>
- <span data-ttu-id="31e59-140">Premium</span><span class="sxs-lookup"><span data-stu-id="31e59-140">Premium</span></span>
- <span data-ttu-id="31e59-141">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="31e59-141">DataWarehouse</span></span>
- <span data-ttu-id="31e59-142">Gratuito</span><span class="sxs-lookup"><span data-stu-id="31e59-142">Free</span></span>
- <span data-ttu-id="31e59-143">Tratto</span><span class="sxs-lookup"><span data-stu-id="31e59-143">Stretch</span></span>
- <span data-ttu-id="31e59-144">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="31e59-144">GeneralPurpose</span></span>
- <span data-ttu-id="31e59-145">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="31e59-145">BusinessCritical</span></span>

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

### <span data-ttu-id="31e59-146">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="31e59-146">-ElasticPoolName</span></span>
<span data-ttu-id="31e59-147">Specifica il nome del pool elastico in cui trasferire il database.</span><span class="sxs-lookup"><span data-stu-id="31e59-147">Specifies name of the elastic pool in which to move the database.</span></span>

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

### <span data-ttu-id="31e59-148">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="31e59-148">-LicenseType</span></span>
<span data-ttu-id="31e59-149">Tipo di licenza per il database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="31e59-149">The license type for the Azure Sql database.</span></span> <span data-ttu-id="31e59-150">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="31e59-150">Possible values are:</span></span>
- <span data-ttu-id="31e59-151">BasePrice-Azure Hybrid benefit (AHB) i prezzi scontati per i proprietari di licenze di SQL Server esistenti vengono applicati.</span><span class="sxs-lookup"><span data-stu-id="31e59-151">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="31e59-152">Il prezzo del database verrà scontato per i proprietari di licenze di SQL Server esistenti.</span><span class="sxs-lookup"><span data-stu-id="31e59-152">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="31e59-153">LicenseIncluded-Azure Hybrid benefit (AHB) i prezzi di sconto per i proprietari di licenze di SQL Server esistenti non vengono applicati.</span><span class="sxs-lookup"><span data-stu-id="31e59-153">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="31e59-154">Prezzo database includerà un nuovo costo per la licenza di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="31e59-154">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="31e59-155">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="31e59-155">-MaxSizeBytes</span></span>
<span data-ttu-id="31e59-156">Dimensione massima del database SQL di Azure in byte.</span><span class="sxs-lookup"><span data-stu-id="31e59-156">The maximum size of the Azure SQL Database in bytes.</span></span>

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

### <span data-ttu-id="31e59-157">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="31e59-157">-MinimumCapacity</span></span>
<span data-ttu-id="31e59-158">La capacità minima che il database avrà sempre allocato, se non in pausa.</span><span class="sxs-lookup"><span data-stu-id="31e59-158">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="31e59-159">Solo per i database SQL di Azure server.</span><span class="sxs-lookup"><span data-stu-id="31e59-159">For serverless Azure Sql databases only.</span></span>

```yaml
Type: System.Double
Parameter Sets: Update, VcoreBasedDatabase
Aliases: MinVCore

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31e59-160">-NewName</span><span class="sxs-lookup"><span data-stu-id="31e59-160">-NewName</span></span>
<span data-ttu-id="31e59-161">Nuovo nome a cui rinominare il database.</span><span class="sxs-lookup"><span data-stu-id="31e59-161">The new name to rename the database to.</span></span>

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

### <span data-ttu-id="31e59-162">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="31e59-162">-ReadScale</span></span>
<span data-ttu-id="31e59-163">Opzione Leggi scala per assegnare al database SQL di Azure. (Abilitato/disabilitato)</span><span class="sxs-lookup"><span data-stu-id="31e59-163">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

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

### <span data-ttu-id="31e59-164">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="31e59-164">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="31e59-165">Specifica il nome dell'obiettivo del servizio da assegnare al database.</span><span class="sxs-lookup"><span data-stu-id="31e59-165">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="31e59-166">Per informazioni sugli obiettivi del servizio, vedere [livelli di servizio database SQL di Azure e livello di prestazioni](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) nella raccolta di Microsoft Developer Network.</span><span class="sxs-lookup"><span data-stu-id="31e59-166">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) in the Microsoft Developer Network Library.</span></span>

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

### <span data-ttu-id="31e59-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31e59-167">-ResourceGroupName</span></span>
<span data-ttu-id="31e59-168">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="31e59-168">Specifies the name of resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="31e59-169">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="31e59-169">-ServerName</span></span>
<span data-ttu-id="31e59-170">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="31e59-170">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="31e59-171">-Tag</span><span class="sxs-lookup"><span data-stu-id="31e59-171">-Tags</span></span>
<span data-ttu-id="31e59-172">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="31e59-172">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="31e59-173">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="31e59-173">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="31e59-174">-VCore</span><span class="sxs-lookup"><span data-stu-id="31e59-174">-VCore</span></span>
<span data-ttu-id="31e59-175">Numero Vcore per il database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="31e59-175">The Vcore number for the Azure Sql database</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity, MaxVCore, MaxCapacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31e59-176">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="31e59-176">-ZoneRedundant</span></span>
<span data-ttu-id="31e59-177">Ridondanza della zona da associare al database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="31e59-177">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="31e59-178">-Confermare</span><span class="sxs-lookup"><span data-stu-id="31e59-178">-Confirm</span></span>
<span data-ttu-id="31e59-179">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31e59-179">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31e59-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31e59-180">-WhatIf</span></span>
<span data-ttu-id="31e59-181">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="31e59-181">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31e59-182">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="31e59-182">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31e59-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31e59-183">CommonParameters</span></span>
<span data-ttu-id="31e59-184">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31e59-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31e59-185">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="31e59-185">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31e59-186">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="31e59-186">INPUTS</span></span>

### <span data-ttu-id="31e59-187">System. String</span><span class="sxs-lookup"><span data-stu-id="31e59-187">System.String</span></span>

## <span data-ttu-id="31e59-188">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="31e59-188">OUTPUTS</span></span>

### <span data-ttu-id="31e59-189">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="31e59-189">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="31e59-190">Note</span><span class="sxs-lookup"><span data-stu-id="31e59-190">NOTES</span></span>

## <span data-ttu-id="31e59-191">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="31e59-191">RELATED LINKS</span></span>

[<span data-ttu-id="31e59-192">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="31e59-192">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="31e59-193">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="31e59-193">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="31e59-194">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="31e59-194">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="31e59-195">Curriculum vitae-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="31e59-195">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="31e59-196">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="31e59-196">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="31e59-197">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="31e59-197">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
