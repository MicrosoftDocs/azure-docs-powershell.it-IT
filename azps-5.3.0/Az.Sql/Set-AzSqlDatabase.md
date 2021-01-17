---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
ms.openlocfilehash: 6d737abb6c58ea8c74085f8390d7a6acbdf54dc8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376456"
---
# <span data-ttu-id="8aae6-101">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8aae6-101">Set-AzSqlDatabase</span></span>

## <span data-ttu-id="8aae6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8aae6-102">SYNOPSIS</span></span>
<span data-ttu-id="8aae6-103">Imposta le proprietà per un database o sposta un database esistente in un pool elastico.</span><span class="sxs-lookup"><span data-stu-id="8aae6-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

## <span data-ttu-id="8aae6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8aae6-104">SYNTAX</span></span>

### <span data-ttu-id="8aae6-105">Update (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8aae6-105">Update (Default)</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>]
 [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8aae6-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="8aae6-106">VcoreBasedDatabase</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>]
 [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8aae6-107">Rinominare</span><span class="sxs-lookup"><span data-stu-id="8aae6-107">Rename</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> -NewName <String> [-AsJob] [-BackupStorageRedundancy <String>]
 [-SecondaryType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8aae6-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8aae6-108">DESCRIPTION</span></span>
<span data-ttu-id="8aae6-109">Il cmdlet **set-AzSqlDatabase** imposta le proprietà per un database in Azure SQL database.</span><span class="sxs-lookup"><span data-stu-id="8aae6-109">The **Set-AzSqlDatabase** cmdlet sets properties for a database in Azure SQL Database.</span></span> <span data-ttu-id="8aae6-110">Questo cmdlet può modificare il livello di servizio (*edizione*), le prestazioni (*RequestedServiceObjectiveName*) e le dimensioni massime di archiviazione (*MaxSizeBytes*) per il database.</span><span class="sxs-lookup"><span data-stu-id="8aae6-110">This cmdlet can modify the service tier (*Edition*), performance level (*RequestedServiceObjectiveName*), and storage max size (*MaxSizeBytes*) for the database.</span></span>  <span data-ttu-id="8aae6-111">Inoltre, puoi specificare il parametro *ElasticPoolName* per trasferire un database in un pool elastico.</span><span class="sxs-lookup"><span data-stu-id="8aae6-111">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span> <span data-ttu-id="8aae6-112">Se un database è già in un pool elastico, è possibile usare il parametro *RequestedServiceObjectiveName* per trasferire il database da un pool elastico e in un livello di prestazioni per i singoli database.</span><span class="sxs-lookup"><span data-stu-id="8aae6-112">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to move the database out of an elastic pool and into a performance level for single databases.</span></span>

## <span data-ttu-id="8aae6-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8aae6-113">EXAMPLES</span></span>

### <span data-ttu-id="8aae6-114">Esempio 1: aggiornare un database in un database S0 standard</span><span class="sxs-lookup"><span data-stu-id="8aae6-114">Example 1: Update a database to a Standard S0 database</span></span>
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

<span data-ttu-id="8aae6-115">Questo comando aggiorna un database denominato Database01 in un database S0 standard in un server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="8aae6-115">This command updates a database named Database01 to a Standard S0 database on a server named Server01.</span></span>

### <span data-ttu-id="8aae6-116">Esempio 2: aggiungere un database a un pool elastico</span><span class="sxs-lookup"><span data-stu-id="8aae6-116">Example 2: Add a database to an elastic pool</span></span>
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

<span data-ttu-id="8aae6-117">Questo comando aggiunge un database denominato Database01 al pool elastico denominato ElasticPool01 ospitato nel server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="8aae6-117">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

### <span data-ttu-id="8aae6-118">Esempio 3: modificare le dimensioni massime di archiviazione di un database</span><span class="sxs-lookup"><span data-stu-id="8aae6-118">Example 3: Modify the storage max size of a database</span></span>
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

<span data-ttu-id="8aae6-119">Questo comando aggiorna un database denominato Database01 per impostare la dimensione massima su 1 TB.</span><span class="sxs-lookup"><span data-stu-id="8aae6-119">This command updates a database named Database01 to set its max size to 1 TB.</span></span>

### <span data-ttu-id="8aae6-120">Esempio 4: aggiornare un database di uso generale esistente a livello di servizio iperscalare</span><span class="sxs-lookup"><span data-stu-id="8aae6-120">Example 4: Update a existing General Purpose database to Hyperscale service tier</span></span>
```
PS C:\>Set-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -Edition "Hyperscale" -RequestedServiceObjectiveName "HS_Gen5_2"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : 56246136-839f-4171-80af-4c28142463b1
Edition                       : Hyperscale
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : -1
Status                        : Online
CreationDate                  : 12/6/2020 5:34:16 PM
CurrentServiceObjectiveId     : 00000000-0000-0000-0000-000000000000
CurrentServiceObjectiveName   : HS_Gen5_2
RequestedServiceObjectiveName : HS_Gen5_2
RequestedServiceObjectiveId   :
ElasticPoolName               :
EarliestRestoreDate           : 12/6/2020 5:34:16 PM
Tags                          : {}
ResourceId                    : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/servers/Server01/databases/Database01
CreateMode                    :
ReadScale                     : Enabled
ZoneRedundant                 :
Capacity                      : 2
Family                        : Gen5
SkuName                       : HS_Gen5
LicenseType                   : LicenseIncluded
AutoPauseDelayInMinutes       :
MinimumCapacity               :
ReadReplicaCount              : 1
BackupStorageRedundancy       : Geo
```

<span data-ttu-id="8aae6-121">Questo comando aggiorna un database denominato Database01 da General purpose a livello di servizio iperscala.</span><span class="sxs-lookup"><span data-stu-id="8aae6-121">This command updates a database named Database01 from General Purpose to Hyperscale service tier.</span></span>

## <span data-ttu-id="8aae6-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8aae6-122">PARAMETERS</span></span>

### <span data-ttu-id="8aae6-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8aae6-123">-AsJob</span></span>
<span data-ttu-id="8aae6-124">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="8aae6-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8aae6-125">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="8aae6-125">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="8aae6-126">Ritardo di pausa automatica in minuti per il database (solo server),-1 per rifiutare la disattivazione</span><span class="sxs-lookup"><span data-stu-id="8aae6-126">The auto pause delay in minutes for database (serverless only), -1 to opt out</span></span>

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

### <span data-ttu-id="8aae6-127">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="8aae6-127">-BackupStorageRedundancy</span></span>
<span data-ttu-id="8aae6-128">Ridondanza dello spazio di archiviazione di backup utilizzata per archiviare i backup per il database SQL.</span><span class="sxs-lookup"><span data-stu-id="8aae6-128">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="8aae6-129">Le opzioni disponibili sono: locale, zona e geo.</span><span class="sxs-lookup"><span data-stu-id="8aae6-129">Options are: Local, Zone and Geo.</span></span>

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

### <span data-ttu-id="8aae6-130">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="8aae6-130">-ComputeGeneration</span></span>
<span data-ttu-id="8aae6-131">Generazione di Compute da assegnare.</span><span class="sxs-lookup"><span data-stu-id="8aae6-131">The compute generation to assign.</span></span>

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

### <span data-ttu-id="8aae6-132">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="8aae6-132">-ComputeModel</span></span>
<span data-ttu-id="8aae6-133">Modello calcolato di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="8aae6-133">Computed model of Azure Sql database.</span></span> <span data-ttu-id="8aae6-134">Server o provisioning</span><span class="sxs-lookup"><span data-stu-id="8aae6-134">Serverless or Provisioned</span></span>

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

### <span data-ttu-id="8aae6-135">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8aae6-135">-DatabaseName</span></span>
<span data-ttu-id="8aae6-136">Specifica il nome del database.</span><span class="sxs-lookup"><span data-stu-id="8aae6-136">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="8aae6-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8aae6-137">-DefaultProfile</span></span>
<span data-ttu-id="8aae6-138">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8aae6-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8aae6-139">-Edition</span><span class="sxs-lookup"><span data-stu-id="8aae6-139">-Edition</span></span>
<span data-ttu-id="8aae6-140">Specifica l'edizione per il database.</span><span class="sxs-lookup"><span data-stu-id="8aae6-140">Specifies the edition for the database.</span></span>
<span data-ttu-id="8aae6-141">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="8aae6-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8aae6-142">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8aae6-142">None</span></span>
- <span data-ttu-id="8aae6-143">Base</span><span class="sxs-lookup"><span data-stu-id="8aae6-143">Basic</span></span>
- <span data-ttu-id="8aae6-144">Standard</span><span class="sxs-lookup"><span data-stu-id="8aae6-144">Standard</span></span>
- <span data-ttu-id="8aae6-145">Premium</span><span class="sxs-lookup"><span data-stu-id="8aae6-145">Premium</span></span>
- <span data-ttu-id="8aae6-146">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="8aae6-146">DataWarehouse</span></span>
- <span data-ttu-id="8aae6-147">Gratuito</span><span class="sxs-lookup"><span data-stu-id="8aae6-147">Free</span></span>
- <span data-ttu-id="8aae6-148">Tratto</span><span class="sxs-lookup"><span data-stu-id="8aae6-148">Stretch</span></span>
- <span data-ttu-id="8aae6-149">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="8aae6-149">GeneralPurpose</span></span>
- <span data-ttu-id="8aae6-150">Superscalari</span><span class="sxs-lookup"><span data-stu-id="8aae6-150">Hyperscale</span></span>
- <span data-ttu-id="8aae6-151">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="8aae6-151">BusinessCritical</span></span>

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

### <span data-ttu-id="8aae6-152">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="8aae6-152">-ElasticPoolName</span></span>
<span data-ttu-id="8aae6-153">Specifica il nome del pool elastico in cui trasferire il database.</span><span class="sxs-lookup"><span data-stu-id="8aae6-153">Specifies name of the elastic pool in which to move the database.</span></span>

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

### <span data-ttu-id="8aae6-154">-HighAvailabilityReplicaCount</span><span class="sxs-lookup"><span data-stu-id="8aae6-154">-HighAvailabilityReplicaCount</span></span>
<span data-ttu-id="8aae6-155">Numero di repliche secondarie ReadOnly associate al database.</span><span class="sxs-lookup"><span data-stu-id="8aae6-155">The number of readonly secondary replicas associated with the database.</span></span>  <span data-ttu-id="8aae6-156">Solo per l'edizione di iperscala.</span><span class="sxs-lookup"><span data-stu-id="8aae6-156">For Hyperscale edition only.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Update, VcoreBasedDatabase
Aliases: ReadReplicaCount

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8aae6-157">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="8aae6-157">-LicenseType</span></span>
<span data-ttu-id="8aae6-158">Tipo di licenza per il database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="8aae6-158">The license type for the Azure Sql database.</span></span> <span data-ttu-id="8aae6-159">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="8aae6-159">Possible values are:</span></span>
- <span data-ttu-id="8aae6-160">BasePrice-Azure Hybrid benefit (AHB) i prezzi scontati per i proprietari di licenze di SQL Server esistenti vengono applicati.</span><span class="sxs-lookup"><span data-stu-id="8aae6-160">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="8aae6-161">Il prezzo del database verrà scontato per i proprietari di licenze di SQL Server esistenti.</span><span class="sxs-lookup"><span data-stu-id="8aae6-161">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="8aae6-162">LicenseIncluded-Azure Hybrid benefit (AHB) i prezzi di sconto per i proprietari di licenze di SQL Server esistenti non vengono applicati.</span><span class="sxs-lookup"><span data-stu-id="8aae6-162">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="8aae6-163">Prezzo database includerà un nuovo costo per la licenza di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8aae6-163">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="8aae6-164">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="8aae6-164">-MaxSizeBytes</span></span>
<span data-ttu-id="8aae6-165">Dimensione massima del database SQL di Azure in byte.</span><span class="sxs-lookup"><span data-stu-id="8aae6-165">The maximum size of the Azure SQL Database in bytes.</span></span>

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

### <span data-ttu-id="8aae6-166">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="8aae6-166">-MinimumCapacity</span></span>
<span data-ttu-id="8aae6-167">La capacità minima che il database avrà sempre allocato, se non in pausa.</span><span class="sxs-lookup"><span data-stu-id="8aae6-167">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="8aae6-168">Solo per i database SQL di Azure server.</span><span class="sxs-lookup"><span data-stu-id="8aae6-168">For serverless Azure Sql databases only.</span></span>

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

### <span data-ttu-id="8aae6-169">-NewName</span><span class="sxs-lookup"><span data-stu-id="8aae6-169">-NewName</span></span>
<span data-ttu-id="8aae6-170">Nuovo nome a cui rinominare il database.</span><span class="sxs-lookup"><span data-stu-id="8aae6-170">The new name to rename the database to.</span></span>

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

### <span data-ttu-id="8aae6-171">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="8aae6-171">-ReadScale</span></span>
<span data-ttu-id="8aae6-172">Se abilitata, le connessioni che hanno lo scopo dell'applicazione impostato su ReadOnly nella stringa di connessione possono essere instradate a una replica secondaria ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="8aae6-172">If enabled, connections that have application intent set to readonly in their connection string may be routed to a readonly secondary replica.</span></span> <span data-ttu-id="8aae6-173">Questa proprietà è impostabile solo per i database Premium e business critical.</span><span class="sxs-lookup"><span data-stu-id="8aae6-173">This property is only settable for Premium and Business Critical databases.</span></span>

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

### <span data-ttu-id="8aae6-174">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="8aae6-174">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="8aae6-175">Specifica il nome dell'obiettivo del servizio da assegnare al database.</span><span class="sxs-lookup"><span data-stu-id="8aae6-175">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="8aae6-176">Per informazioni sugli obiettivi del servizio, vedere [livelli di servizio database SQL di Azure e livello di prestazioni](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) nella raccolta di Microsoft Developer Network.</span><span class="sxs-lookup"><span data-stu-id="8aae6-176">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) in the Microsoft Developer Network Library.</span></span>

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

### <span data-ttu-id="8aae6-177">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8aae6-177">-ResourceGroupName</span></span>
<span data-ttu-id="8aae6-178">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="8aae6-178">Specifies the name of resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="8aae6-179">-SecondaryType</span><span class="sxs-lookup"><span data-stu-id="8aae6-179">-SecondaryType</span></span>
<span data-ttu-id="8aae6-180">Il tipo secondario del database se è secondario.</span><span class="sxs-lookup"><span data-stu-id="8aae6-180">The secondary type of the database if it is a secondary.</span></span>  <span data-ttu-id="8aae6-181">I valori validi sono geo e denominati.</span><span class="sxs-lookup"><span data-stu-id="8aae6-181">Valid values are Geo and Named.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Named, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8aae6-182">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="8aae6-182">-ServerName</span></span>
<span data-ttu-id="8aae6-183">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="8aae6-183">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="8aae6-184">-Tag</span><span class="sxs-lookup"><span data-stu-id="8aae6-184">-Tags</span></span>
<span data-ttu-id="8aae6-185">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="8aae6-185">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8aae6-186">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="8aae6-186">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="8aae6-187">-VCore</span><span class="sxs-lookup"><span data-stu-id="8aae6-187">-VCore</span></span>
<span data-ttu-id="8aae6-188">Numero Vcore per il database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="8aae6-188">The Vcore number for the Azure Sql database</span></span>

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

### <span data-ttu-id="8aae6-189">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="8aae6-189">-ZoneRedundant</span></span>
<span data-ttu-id="8aae6-190">Ridondanza della zona da associare al database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="8aae6-190">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="8aae6-191">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8aae6-191">-Confirm</span></span>
<span data-ttu-id="8aae6-192">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8aae6-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8aae6-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8aae6-193">-WhatIf</span></span>
<span data-ttu-id="8aae6-194">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8aae6-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8aae6-195">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8aae6-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8aae6-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8aae6-196">CommonParameters</span></span>
<span data-ttu-id="8aae6-197">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8aae6-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8aae6-198">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8aae6-198">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8aae6-199">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8aae6-199">INPUTS</span></span>

### <span data-ttu-id="8aae6-200">System. String</span><span class="sxs-lookup"><span data-stu-id="8aae6-200">System.String</span></span>

## <span data-ttu-id="8aae6-201">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8aae6-201">OUTPUTS</span></span>

### <span data-ttu-id="8aae6-202">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="8aae6-202">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="8aae6-203">Note</span><span class="sxs-lookup"><span data-stu-id="8aae6-203">NOTES</span></span>

## <span data-ttu-id="8aae6-204">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8aae6-204">RELATED LINKS</span></span>

[<span data-ttu-id="8aae6-205">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8aae6-205">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="8aae6-206">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8aae6-206">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="8aae6-207">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8aae6-207">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="8aae6-208">Curriculum vitae-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8aae6-208">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="8aae6-209">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8aae6-209">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="8aae6-210">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="8aae6-210">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
