---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
ms.openlocfilehash: 17e6c492828f877ebf53c634a7670e8d60c9ccba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995033"
---
# <span data-ttu-id="3bd11-101">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3bd11-101">Set-AzSqlDatabase</span></span>

## <span data-ttu-id="3bd11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3bd11-102">SYNOPSIS</span></span>
<span data-ttu-id="3bd11-103">Imposta le proprietà per un database o sposta un database esistente in un pool flessibile.</span><span class="sxs-lookup"><span data-stu-id="3bd11-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

## <span data-ttu-id="3bd11-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3bd11-104">SYNTAX</span></span>

### <span data-ttu-id="3bd11-105">Aggiorna (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3bd11-105">Update (Default)</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>]
 [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-MaintenanceConfigurationId <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bd11-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="3bd11-106">VcoreBasedDatabase</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>]
 [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-MaintenanceConfigurationId <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bd11-107">Rinomina</span><span class="sxs-lookup"><span data-stu-id="3bd11-107">Rename</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> -NewName <String> [-AsJob] [-BackupStorageRedundancy <String>]
 [-SecondaryType <String>] [-MaintenanceConfigurationId <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3bd11-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3bd11-108">DESCRIPTION</span></span>
<span data-ttu-id="3bd11-109">Il cmdlet **Set-AzSqlDatabase** imposta le proprietà per un database in Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="3bd11-109">The **Set-AzSqlDatabase** cmdlet sets properties for a database in Azure SQL Database.</span></span> <span data-ttu-id="3bd11-110">Questo cmdlet può modificare il livello di servizio (*Edition*), il livello di prestazioni (*RequestedServiceObjectiveName*) e le dimensioni massime di archiviazione (*MaxSizeBytes*) per il database.</span><span class="sxs-lookup"><span data-stu-id="3bd11-110">This cmdlet can modify the service tier (*Edition*), performance level (*RequestedServiceObjectiveName*), and storage max size (*MaxSizeBytes*) for the database.</span></span>  <span data-ttu-id="3bd11-111">Inoltre, è possibile specificare il parametro *ElasticPoolName* per spostare un database in un pool flessibile.</span><span class="sxs-lookup"><span data-stu-id="3bd11-111">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span> <span data-ttu-id="3bd11-112">Se un database è già in un pool flessibile, è possibile usare il parametro *RequestedServiceObjectiveName* per spostare il database da un pool flessibile e in un livello di prestazioni per singoli database.</span><span class="sxs-lookup"><span data-stu-id="3bd11-112">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to move the database out of an elastic pool and into a performance level for single databases.</span></span>

## <span data-ttu-id="3bd11-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3bd11-113">EXAMPLES</span></span>

### <span data-ttu-id="3bd11-114">Esempio 1: Aggiornare un database a un database S0 standard</span><span class="sxs-lookup"><span data-stu-id="3bd11-114">Example 1: Update a database to a Standard S0 database</span></span>
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

<span data-ttu-id="3bd11-115">Questo comando aggiorna un database denominato Database01 a un database Standard S0 in un server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="3bd11-115">This command updates a database named Database01 to a Standard S0 database on a server named Server01.</span></span>

### <span data-ttu-id="3bd11-116">Esempio 2: Aggiungere un database a un pool elastico</span><span class="sxs-lookup"><span data-stu-id="3bd11-116">Example 2: Add a database to an elastic pool</span></span>
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

<span data-ttu-id="3bd11-117">Questo comando aggiunge un database denominato Database01 al pool elastico denominato ElasticPool01 ospitato nel server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="3bd11-117">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

### <span data-ttu-id="3bd11-118">Esempio 3: Modificare le dimensioni massime di archiviazione di un database</span><span class="sxs-lookup"><span data-stu-id="3bd11-118">Example 3: Modify the storage max size of a database</span></span>
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

<span data-ttu-id="3bd11-119">Questo comando aggiorna un database denominato Database01 per impostare le dimensioni massime su 1 TB.</span><span class="sxs-lookup"><span data-stu-id="3bd11-119">This command updates a database named Database01 to set its max size to 1 TB.</span></span>

### <span data-ttu-id="3bd11-120">Esempio 4: Aggiornare un database generico esistente a un livello di servizio di Hyperscale</span><span class="sxs-lookup"><span data-stu-id="3bd11-120">Example 4: Update a existing General Purpose database to Hyperscale service tier</span></span>
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

<span data-ttu-id="3bd11-121">Questo comando aggiorna un database denominato Database01 da Scopo generale a Livello di servizio di Hyperscale.</span><span class="sxs-lookup"><span data-stu-id="3bd11-121">This command updates a database named Database01 from General Purpose to Hyperscale service tier.</span></span>

## <span data-ttu-id="3bd11-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3bd11-122">PARAMETERS</span></span>

### <span data-ttu-id="3bd11-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3bd11-123">-AsJob</span></span>
<span data-ttu-id="3bd11-124">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="3bd11-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3bd11-125">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="3bd11-125">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="3bd11-126">Ritardo di pausa automatico in minuti per il database (solo senza server), -1 per rifiutare esplicitamente</span><span class="sxs-lookup"><span data-stu-id="3bd11-126">The auto pause delay in minutes for database (serverless only), -1 to opt out</span></span>

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

### <span data-ttu-id="3bd11-127">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="3bd11-127">-BackupStorageRedundancy</span></span>
<span data-ttu-id="3bd11-128">Ridondanza di archiviazione di backup usata per archiviare i backup per SQL database.</span><span class="sxs-lookup"><span data-stu-id="3bd11-128">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="3bd11-129">Le opzioni disponibili sono: Locale, Area e Geo.</span><span class="sxs-lookup"><span data-stu-id="3bd11-129">Options are: Local, Zone and Geo.</span></span>

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

### <span data-ttu-id="3bd11-130">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="3bd11-130">-ComputeGeneration</span></span>
<span data-ttu-id="3bd11-131">Generazione di elaborazione da assegnare.</span><span class="sxs-lookup"><span data-stu-id="3bd11-131">The compute generation to assign.</span></span>

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

### <span data-ttu-id="3bd11-132">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="3bd11-132">-ComputeModel</span></span>
<span data-ttu-id="3bd11-133">Modello calcolato del database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="3bd11-133">Computed model of Azure Sql database.</span></span> <span data-ttu-id="3bd11-134">Senza server o in provisioning</span><span class="sxs-lookup"><span data-stu-id="3bd11-134">Serverless or Provisioned</span></span>

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

### <span data-ttu-id="3bd11-135">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3bd11-135">-DatabaseName</span></span>
<span data-ttu-id="3bd11-136">Specifica il nome del database.</span><span class="sxs-lookup"><span data-stu-id="3bd11-136">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="3bd11-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bd11-137">-DefaultProfile</span></span>
<span data-ttu-id="3bd11-138">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3bd11-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3bd11-139">-Edition</span><span class="sxs-lookup"><span data-stu-id="3bd11-139">-Edition</span></span>
<span data-ttu-id="3bd11-140">Specifica l'edizione per il database.</span><span class="sxs-lookup"><span data-stu-id="3bd11-140">Specifies the edition for the database.</span></span>
<span data-ttu-id="3bd11-141">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="3bd11-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3bd11-142">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3bd11-142">None</span></span>
- <span data-ttu-id="3bd11-143">Di base</span><span class="sxs-lookup"><span data-stu-id="3bd11-143">Basic</span></span>
- <span data-ttu-id="3bd11-144">Standard</span><span class="sxs-lookup"><span data-stu-id="3bd11-144">Standard</span></span>
- <span data-ttu-id="3bd11-145">Premium</span><span class="sxs-lookup"><span data-stu-id="3bd11-145">Premium</span></span>
- <span data-ttu-id="3bd11-146">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="3bd11-146">DataWarehouse</span></span>
- <span data-ttu-id="3bd11-147">Gratis</span><span class="sxs-lookup"><span data-stu-id="3bd11-147">Free</span></span>
- <span data-ttu-id="3bd11-148">Estendamento</span><span class="sxs-lookup"><span data-stu-id="3bd11-148">Stretch</span></span>
- <span data-ttu-id="3bd11-149">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="3bd11-149">GeneralPurpose</span></span>
- <span data-ttu-id="3bd11-150">Iperscale</span><span class="sxs-lookup"><span data-stu-id="3bd11-150">Hyperscale</span></span>
- <span data-ttu-id="3bd11-151">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="3bd11-151">BusinessCritical</span></span>

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

### <span data-ttu-id="3bd11-152">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="3bd11-152">-ElasticPoolName</span></span>
<span data-ttu-id="3bd11-153">Specifica il nome del pool flessibile in cui spostare il database.</span><span class="sxs-lookup"><span data-stu-id="3bd11-153">Specifies name of the elastic pool in which to move the database.</span></span>

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

### <span data-ttu-id="3bd11-154">-HighAvailabilityReplicaCount</span><span class="sxs-lookup"><span data-stu-id="3bd11-154">-HighAvailabilityReplicaCount</span></span>
<span data-ttu-id="3bd11-155">Numero di replica secondarie di sola lettura associate al database.</span><span class="sxs-lookup"><span data-stu-id="3bd11-155">The number of readonly secondary replicas associated with the database.</span></span>  <span data-ttu-id="3bd11-156">Solo per l'edizione Hyperscale.</span><span class="sxs-lookup"><span data-stu-id="3bd11-156">For Hyperscale edition only.</span></span>

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

### <span data-ttu-id="3bd11-157">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="3bd11-157">-LicenseType</span></span>
<span data-ttu-id="3bd11-158">Il tipo di licenza per il database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="3bd11-158">The license type for the Azure Sql database.</span></span> <span data-ttu-id="3bd11-159">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="3bd11-159">Possible values are:</span></span>
- <span data-ttu-id="3bd11-160">BasePrice - Viene applicato un prezzo scontato per Azure Hybrid Benefit (AHB) per i proprietari di licenze SQL Server licenze di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="3bd11-160">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="3bd11-161">Il prezzo del database verrà scontato per i proprietari SQL Server licenze esistenti.</span><span class="sxs-lookup"><span data-stu-id="3bd11-161">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="3bd11-162">LicenseIncluded - Il prezzo di sconto AHB (Azure Hybrid Benefit) per i proprietari SQL Server licenze non viene applicato.</span><span class="sxs-lookup"><span data-stu-id="3bd11-162">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="3bd11-163">Il prezzo del database includerà un costo SQL Server licenze.</span><span class="sxs-lookup"><span data-stu-id="3bd11-163">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="3bd11-164">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="3bd11-164">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="3bd11-165">ID di configurazione manutenzione per il SQL database.</span><span class="sxs-lookup"><span data-stu-id="3bd11-165">The Maintenance configuration id for the SQL Database.</span></span>

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

### <span data-ttu-id="3bd11-166">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="3bd11-166">-MaxSizeBytes</span></span>
<span data-ttu-id="3bd11-167">Dimensioni massime del database di SQL Azure in byte.</span><span class="sxs-lookup"><span data-stu-id="3bd11-167">The maximum size of the Azure SQL Database in bytes.</span></span>

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

### <span data-ttu-id="3bd11-168">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="3bd11-168">-MinimumCapacity</span></span>
<span data-ttu-id="3bd11-169">La capacità minima assegnata al database sarà sempre allocata, se non sospesa.</span><span class="sxs-lookup"><span data-stu-id="3bd11-169">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="3bd11-170">Solo per i database SQL di Azure senza server.</span><span class="sxs-lookup"><span data-stu-id="3bd11-170">For serverless Azure Sql databases only.</span></span>

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

### <span data-ttu-id="3bd11-171">-NewName</span><span class="sxs-lookup"><span data-stu-id="3bd11-171">-NewName</span></span>
<span data-ttu-id="3bd11-172">Il nuovo nome in cui rinominare il database.</span><span class="sxs-lookup"><span data-stu-id="3bd11-172">The new name to rename the database to.</span></span>

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

### <span data-ttu-id="3bd11-173">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="3bd11-173">-ReadScale</span></span>
<span data-ttu-id="3bd11-174">Se abilitate, le connessioni per cui lo scopo dell'applicazione è impostato su readonly nella stringa di connessione potrebbero essere instradati a una replica secondaria di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="3bd11-174">If enabled, connections that have application intent set to readonly in their connection string may be routed to a readonly secondary replica.</span></span> <span data-ttu-id="3bd11-175">Questa proprietà è impostata solo per i database Premium e Business Critical.</span><span class="sxs-lookup"><span data-stu-id="3bd11-175">This property is only settable for Premium and Business Critical databases.</span></span>

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

### <span data-ttu-id="3bd11-176">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="3bd11-176">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="3bd11-177">Specifica il nome dell'obiettivo del servizio da assegnare al database.</span><span class="sxs-lookup"><span data-stu-id="3bd11-177">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="3bd11-178">Per informazioni sugli obiettivi del servizio, vedere [Azure SQL livelli](https://docs.microsoft.com/azure/sql-database/sql-database-dtu-resource-limits-single-databases) di servizio del database e livelli di prestazioni nella Libreria di rete per sviluppatori Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3bd11-178">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://docs.microsoft.com/azure/sql-database/sql-database-dtu-resource-limits-single-databases) in the Microsoft Developer Network Library.</span></span>

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

### <span data-ttu-id="3bd11-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bd11-179">-ResourceGroupName</span></span>
<span data-ttu-id="3bd11-180">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="3bd11-180">Specifies the name of resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="3bd11-181">-SecondaryType</span><span class="sxs-lookup"><span data-stu-id="3bd11-181">-SecondaryType</span></span>
<span data-ttu-id="3bd11-182">Tipo secondario del database, se secondario.</span><span class="sxs-lookup"><span data-stu-id="3bd11-182">The secondary type of the database if it is a secondary.</span></span>  <span data-ttu-id="3bd11-183">I valori validi sono Geo e Denominato.</span><span class="sxs-lookup"><span data-stu-id="3bd11-183">Valid values are Geo and Named.</span></span>

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

### <span data-ttu-id="3bd11-184">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3bd11-184">-ServerName</span></span>
<span data-ttu-id="3bd11-185">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="3bd11-185">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="3bd11-186">-Tag</span><span class="sxs-lookup"><span data-stu-id="3bd11-186">-Tags</span></span>
<span data-ttu-id="3bd11-187">Coppie chiave-valore sotto forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="3bd11-187">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3bd11-188">Ad esempio: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="3bd11-188">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3bd11-189">-VCore</span><span class="sxs-lookup"><span data-stu-id="3bd11-189">-VCore</span></span>
<span data-ttu-id="3bd11-190">Numero Vcore per il database Sql di Azure</span><span class="sxs-lookup"><span data-stu-id="3bd11-190">The Vcore number for the Azure Sql database</span></span>

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

### <span data-ttu-id="3bd11-191">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="3bd11-191">-ZoneRedundant</span></span>
<span data-ttu-id="3bd11-192">La ridondanza dell'area da associare al database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="3bd11-192">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="3bd11-193">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3bd11-193">-Confirm</span></span>
<span data-ttu-id="3bd11-194">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bd11-194">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bd11-195">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bd11-195">-WhatIf</span></span>
<span data-ttu-id="3bd11-196">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3bd11-196">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bd11-197">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3bd11-197">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bd11-198">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bd11-198">CommonParameters</span></span>
<span data-ttu-id="3bd11-199">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bd11-199">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bd11-200">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3bd11-200">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bd11-201">INPUT</span><span class="sxs-lookup"><span data-stu-id="3bd11-201">INPUTS</span></span>

### <span data-ttu-id="3bd11-202">System.String</span><span class="sxs-lookup"><span data-stu-id="3bd11-202">System.String</span></span>

## <span data-ttu-id="3bd11-203">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3bd11-203">OUTPUTS</span></span>

### <span data-ttu-id="3bd11-204">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="3bd11-204">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="3bd11-205">NOTE</span><span class="sxs-lookup"><span data-stu-id="3bd11-205">NOTES</span></span>

## <span data-ttu-id="3bd11-206">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3bd11-206">RELATED LINKS</span></span>

[<span data-ttu-id="3bd11-207">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3bd11-207">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="3bd11-208">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3bd11-208">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="3bd11-209">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3bd11-209">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="3bd11-210">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3bd11-210">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="3bd11-211">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3bd11-211">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="3bd11-212">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="3bd11-212">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
