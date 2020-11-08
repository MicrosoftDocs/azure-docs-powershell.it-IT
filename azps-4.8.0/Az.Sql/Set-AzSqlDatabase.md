---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
ms.openlocfilehash: f236c00f50d9ec74a98def114d08ab851e5a89f7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191846"
---
# <span data-ttu-id="58854-101">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="58854-101">Set-AzSqlDatabase</span></span>

## <span data-ttu-id="58854-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="58854-102">SYNOPSIS</span></span>
<span data-ttu-id="58854-103">Imposta le proprietà per un database o sposta un database esistente in un pool elastico.</span><span class="sxs-lookup"><span data-stu-id="58854-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

## <span data-ttu-id="58854-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="58854-104">SYNTAX</span></span>

### <span data-ttu-id="58854-105">Update (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="58854-105">Update (Default)</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-ReadReplicaCount <Int32>]
 [-BackupStorageRedundancy <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58854-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="58854-106">VcoreBasedDatabase</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-ReadReplicaCount <Int32>]
 [-BackupStorageRedundancy <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58854-107">Rinominare</span><span class="sxs-lookup"><span data-stu-id="58854-107">Rename</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> -NewName <String> [-AsJob] [-BackupStorageRedundancy <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58854-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58854-108">DESCRIPTION</span></span>
<span data-ttu-id="58854-109">Il cmdlet **set-AzSqlDatabase** imposta le proprietà per un database in Azure SQL database.</span><span class="sxs-lookup"><span data-stu-id="58854-109">The **Set-AzSqlDatabase** cmdlet sets properties for a database in Azure SQL Database.</span></span> <span data-ttu-id="58854-110">Questo cmdlet può modificare il livello di servizio ( *edizione* ), le prestazioni ( *RequestedServiceObjectiveName* ) e le dimensioni massime di archiviazione ( *MaxSizeBytes* ) per il database.</span><span class="sxs-lookup"><span data-stu-id="58854-110">This cmdlet can modify the service tier ( *Edition* ), performance level ( *RequestedServiceObjectiveName* ), and storage max size ( *MaxSizeBytes* ) for the database.</span></span>  <span data-ttu-id="58854-111">Inoltre, puoi specificare il parametro *ElasticPoolName* per trasferire un database in un pool elastico.</span><span class="sxs-lookup"><span data-stu-id="58854-111">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span> <span data-ttu-id="58854-112">Se un database è già in un pool elastico, è possibile usare il parametro *RequestedServiceObjectiveName* per trasferire il database da un pool elastico e in un livello di prestazioni per i singoli database.</span><span class="sxs-lookup"><span data-stu-id="58854-112">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to move the database out of an elastic pool and into a performance level for single databases.</span></span>

## <span data-ttu-id="58854-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="58854-113">EXAMPLES</span></span>

### <span data-ttu-id="58854-114">Esempio 1: aggiornare un database in un database S0 standard</span><span class="sxs-lookup"><span data-stu-id="58854-114">Example 1: Update a database to a Standard S0 database</span></span>
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

<span data-ttu-id="58854-115">Questo comando aggiorna un database denominato Database01 in un database S0 standard in un server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="58854-115">This command updates a database named Database01 to a Standard S0 database on a server named Server01.</span></span>

### <span data-ttu-id="58854-116">Esempio 2: aggiungere un database a un pool elastico</span><span class="sxs-lookup"><span data-stu-id="58854-116">Example 2: Add a database to an elastic pool</span></span>
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

<span data-ttu-id="58854-117">Questo comando aggiunge un database denominato Database01 al pool elastico denominato ElasticPool01 ospitato nel server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="58854-117">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

### <span data-ttu-id="58854-118">Esempio 3: modificare le dimensioni massime di archiviazione di un database</span><span class="sxs-lookup"><span data-stu-id="58854-118">Example 3: Modify the storage max size of a database</span></span>
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

<span data-ttu-id="58854-119">Questo comando aggiorna un database denominato Database01 per impostare la dimensione massima su 1 TB.</span><span class="sxs-lookup"><span data-stu-id="58854-119">This command updates a database named Database01 to set its max size to 1 TB.</span></span>

## <span data-ttu-id="58854-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="58854-120">PARAMETERS</span></span>

### <span data-ttu-id="58854-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="58854-121">-AsJob</span></span>
<span data-ttu-id="58854-122">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="58854-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="58854-123">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="58854-123">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="58854-124">Ritardo di pausa automatica in minuti per il database (solo server),-1 per rifiutare la disattivazione</span><span class="sxs-lookup"><span data-stu-id="58854-124">The auto pause delay in minutes for database (serverless only), -1 to opt out</span></span>

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

### <span data-ttu-id="58854-125">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="58854-125">-BackupStorageRedundancy</span></span>
<span data-ttu-id="58854-126">Ridondanza dello spazio di archiviazione di backup utilizzata per archiviare i backup per il database SQL.</span><span class="sxs-lookup"><span data-stu-id="58854-126">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="58854-127">Le opzioni disponibili sono: locale, zona e geo.</span><span class="sxs-lookup"><span data-stu-id="58854-127">Options are: Local, Zone and Geo.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Zone, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58854-128">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="58854-128">-ComputeGeneration</span></span>
<span data-ttu-id="58854-129">Generazione di Compute da assegnare.</span><span class="sxs-lookup"><span data-stu-id="58854-129">The compute generation to assign.</span></span>

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

### <span data-ttu-id="58854-130">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="58854-130">-ComputeModel</span></span>
<span data-ttu-id="58854-131">Modello calcolato di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="58854-131">Computed model of Azure Sql database.</span></span> <span data-ttu-id="58854-132">Server o provisioning</span><span class="sxs-lookup"><span data-stu-id="58854-132">Serverless or Provisioned</span></span>

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

### <span data-ttu-id="58854-133">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="58854-133">-DatabaseName</span></span>
<span data-ttu-id="58854-134">Specifica il nome del database.</span><span class="sxs-lookup"><span data-stu-id="58854-134">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="58854-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58854-135">-DefaultProfile</span></span>
<span data-ttu-id="58854-136">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="58854-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="58854-137">-Edition</span><span class="sxs-lookup"><span data-stu-id="58854-137">-Edition</span></span>
<span data-ttu-id="58854-138">Specifica l'edizione per il database.</span><span class="sxs-lookup"><span data-stu-id="58854-138">Specifies the edition for the database.</span></span>
<span data-ttu-id="58854-139">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="58854-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="58854-140">Nessuno</span><span class="sxs-lookup"><span data-stu-id="58854-140">None</span></span>
- <span data-ttu-id="58854-141">Base</span><span class="sxs-lookup"><span data-stu-id="58854-141">Basic</span></span>
- <span data-ttu-id="58854-142">Standard</span><span class="sxs-lookup"><span data-stu-id="58854-142">Standard</span></span>
- <span data-ttu-id="58854-143">Premium</span><span class="sxs-lookup"><span data-stu-id="58854-143">Premium</span></span>
- <span data-ttu-id="58854-144">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="58854-144">DataWarehouse</span></span>
- <span data-ttu-id="58854-145">Gratuito</span><span class="sxs-lookup"><span data-stu-id="58854-145">Free</span></span>
- <span data-ttu-id="58854-146">Tratto</span><span class="sxs-lookup"><span data-stu-id="58854-146">Stretch</span></span>
- <span data-ttu-id="58854-147">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="58854-147">GeneralPurpose</span></span>
- <span data-ttu-id="58854-148">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="58854-148">BusinessCritical</span></span>

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

### <span data-ttu-id="58854-149">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="58854-149">-ElasticPoolName</span></span>
<span data-ttu-id="58854-150">Specifica il nome del pool elastico in cui trasferire il database.</span><span class="sxs-lookup"><span data-stu-id="58854-150">Specifies name of the elastic pool in which to move the database.</span></span>

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

### <span data-ttu-id="58854-151">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="58854-151">-LicenseType</span></span>
<span data-ttu-id="58854-152">Tipo di licenza per il database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="58854-152">The license type for the Azure Sql database.</span></span> <span data-ttu-id="58854-153">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="58854-153">Possible values are:</span></span>
- <span data-ttu-id="58854-154">BasePrice-Azure Hybrid benefit (AHB) i prezzi scontati per i proprietari di licenze di SQL Server esistenti vengono applicati.</span><span class="sxs-lookup"><span data-stu-id="58854-154">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="58854-155">Il prezzo del database verrà scontato per i proprietari di licenze di SQL Server esistenti.</span><span class="sxs-lookup"><span data-stu-id="58854-155">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="58854-156">LicenseIncluded-Azure Hybrid benefit (AHB) i prezzi di sconto per i proprietari di licenze di SQL Server esistenti non vengono applicati.</span><span class="sxs-lookup"><span data-stu-id="58854-156">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="58854-157">Prezzo database includerà un nuovo costo per la licenza di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="58854-157">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="58854-158">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="58854-158">-MaxSizeBytes</span></span>
<span data-ttu-id="58854-159">Dimensione massima del database SQL di Azure in byte.</span><span class="sxs-lookup"><span data-stu-id="58854-159">The maximum size of the Azure SQL Database in bytes.</span></span>

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

### <span data-ttu-id="58854-160">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="58854-160">-MinimumCapacity</span></span>
<span data-ttu-id="58854-161">La capacità minima che il database avrà sempre allocato, se non in pausa.</span><span class="sxs-lookup"><span data-stu-id="58854-161">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="58854-162">Solo per i database SQL di Azure server.</span><span class="sxs-lookup"><span data-stu-id="58854-162">For serverless Azure Sql databases only.</span></span>

```yaml
Type: System.Double
Parameter Sets: Update, VcoreBasedDatabase
Aliases: MinVCore, MinCapacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58854-163">-NewName</span><span class="sxs-lookup"><span data-stu-id="58854-163">-NewName</span></span>
<span data-ttu-id="58854-164">Nuovo nome a cui rinominare il database.</span><span class="sxs-lookup"><span data-stu-id="58854-164">The new name to rename the database to.</span></span>

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

### <span data-ttu-id="58854-165">-ReadReplicaCount</span><span class="sxs-lookup"><span data-stu-id="58854-165">-ReadReplicaCount</span></span>
<span data-ttu-id="58854-166">Numero di repliche secondarie ReadOnly associate al database.</span><span class="sxs-lookup"><span data-stu-id="58854-166">The number of readonly secondary replicas associated with the database.</span></span>  <span data-ttu-id="58854-167">Solo per l'edizione di iperscala.</span><span class="sxs-lookup"><span data-stu-id="58854-167">For Hyperscale edition only.</span></span>

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

### <span data-ttu-id="58854-168">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="58854-168">-ReadScale</span></span>
<span data-ttu-id="58854-169">Se abilitata, le connessioni che hanno lo scopo dell'applicazione impostato su ReadOnly nella stringa di connessione possono essere instradate a una replica secondaria ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="58854-169">If enabled, connections that have application intent set to readonly in their connection string may be routed to a readonly secondary replica.</span></span> <span data-ttu-id="58854-170">Questa proprietà è impostabile solo per i database Premium e business critical.</span><span class="sxs-lookup"><span data-stu-id="58854-170">This property is only settable for Premium and Business Critical databases.</span></span>

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

### <span data-ttu-id="58854-171">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="58854-171">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="58854-172">Specifica il nome dell'obiettivo del servizio da assegnare al database.</span><span class="sxs-lookup"><span data-stu-id="58854-172">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="58854-173">Per informazioni sugli obiettivi del servizio, vedere [livelli di servizio database SQL di Azure e livello di prestazioni](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) nella raccolta di Microsoft Developer Network.</span><span class="sxs-lookup"><span data-stu-id="58854-173">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) in the Microsoft Developer Network Library.</span></span>

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

### <span data-ttu-id="58854-174">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58854-174">-ResourceGroupName</span></span>
<span data-ttu-id="58854-175">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="58854-175">Specifies the name of resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="58854-176">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="58854-176">-ServerName</span></span>
<span data-ttu-id="58854-177">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="58854-177">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="58854-178">-Tag</span><span class="sxs-lookup"><span data-stu-id="58854-178">-Tags</span></span>
<span data-ttu-id="58854-179">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="58854-179">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="58854-180">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="58854-180">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="58854-181">-VCore</span><span class="sxs-lookup"><span data-stu-id="58854-181">-VCore</span></span>
<span data-ttu-id="58854-182">Numero Vcore per il database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="58854-182">The Vcore number for the Azure Sql database</span></span>

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

### <span data-ttu-id="58854-183">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="58854-183">-ZoneRedundant</span></span>
<span data-ttu-id="58854-184">Ridondanza della zona da associare al database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="58854-184">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="58854-185">-Confermare</span><span class="sxs-lookup"><span data-stu-id="58854-185">-Confirm</span></span>
<span data-ttu-id="58854-186">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58854-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58854-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58854-187">-WhatIf</span></span>
<span data-ttu-id="58854-188">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="58854-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58854-189">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="58854-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58854-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58854-190">CommonParameters</span></span>
<span data-ttu-id="58854-191">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58854-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58854-192">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="58854-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58854-193">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="58854-193">INPUTS</span></span>

### <span data-ttu-id="58854-194">System. String</span><span class="sxs-lookup"><span data-stu-id="58854-194">System.String</span></span>

## <span data-ttu-id="58854-195">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="58854-195">OUTPUTS</span></span>

### <span data-ttu-id="58854-196">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="58854-196">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="58854-197">Note</span><span class="sxs-lookup"><span data-stu-id="58854-197">NOTES</span></span>

## <span data-ttu-id="58854-198">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="58854-198">RELATED LINKS</span></span>

[<span data-ttu-id="58854-199">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="58854-199">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="58854-200">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="58854-200">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="58854-201">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="58854-201">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="58854-202">Curriculum vitae-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="58854-202">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="58854-203">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="58854-203">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="58854-204">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="58854-204">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
