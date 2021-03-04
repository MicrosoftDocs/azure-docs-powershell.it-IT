---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
ms.openlocfilehash: c4ccb57292fd4abc2c9b6fd14c5e4492047a2e89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956590"
---
# <span data-ttu-id="1f7c6-101">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1f7c6-101">New-AzSqlDatabase</span></span>

## <span data-ttu-id="1f7c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f7c6-102">SYNOPSIS</span></span>
<span data-ttu-id="1f7c6-103">Crea un database o un database flessibile.</span><span class="sxs-lookup"><span data-stu-id="1f7c6-103">Creates a database or an elastic database.</span></span>

## <span data-ttu-id="1f7c6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1f7c6-104">SYNTAX</span></span>

### <span data-ttu-id="1f7c6-105">DtuBasedDatabase (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1f7c6-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <String>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-Force] [-LicenseType <String>] [-AutoPauseDelayInMinutes <Int32>]
 [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>] [-BackupStorageRedundancy <String>]
 [-SecondaryType <String>] [-MaintenanceConfigurationId <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f7c6-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="1f7c6-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] -Edition <String> [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>]
 [-SampleName <String>] [-ZoneRedundant] [-AsJob] [-Force] -VCore <Int32> -ComputeGeneration <String>
 [-LicenseType <String>] [-ComputeModel <String>] [-AutoPauseDelayInMinutes <Int32>]
 [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>] [-BackupStorageRedundancy <String>]
 [-SecondaryType <String>] [-MaintenanceConfigurationId <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1f7c6-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1f7c6-107">DESCRIPTION</span></span>
<span data-ttu-id="1f7c6-108">Il cmdlet **New-AzSqlDatabase** crea un database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="1f7c6-108">The **New-AzSqlDatabase** cmdlet creates an Azure SQL database.</span></span>
<span data-ttu-id="1f7c6-109">È anche possibile creare un database flessibile impostando il *parametro ElasticPoolName* su un pool elastico esistente.</span><span class="sxs-lookup"><span data-stu-id="1f7c6-109">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="1f7c6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1f7c6-110">EXAMPLES</span></span>

### <span data-ttu-id="1f7c6-111">Esempio 1: Creare un database in un server specificato</span><span class="sxs-lookup"><span data-stu-id="1f7c6-111">Example 1: Create a database on a specified server</span></span>
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

<span data-ttu-id="1f7c6-112">Questo comando crea un database denominato Database01 nel server Server01.</span><span class="sxs-lookup"><span data-stu-id="1f7c6-112">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="1f7c6-113">Esempio 2: Creare un database flessibile in un server specificato</span><span class="sxs-lookup"><span data-stu-id="1f7c6-113">Example 2: Create an elastic database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database02" -ElasticPoolName "ElasticPool01"
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

<span data-ttu-id="1f7c6-114">Questo comando crea un database denominato Database02 nel pool elastico denominato ElasticPool01 nel server Server01.</span><span class="sxs-lookup"><span data-stu-id="1f7c6-114">This command creates a database named Database02 in the elastic pool named ElasticPool01 on server Server01.</span></span>

### <span data-ttu-id="1f7c6-115">Esempio 3: Creare un database Vcore in un server specificato</span><span class="sxs-lookup"><span data-stu-id="1f7c6-115">Example 3: Create an Vcore database on a specified server</span></span>
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

<span data-ttu-id="1f7c6-116">Questo comando crea un database Vcore denominato Database03 nel server Server01.</span><span class="sxs-lookup"><span data-stu-id="1f7c6-116">This command creates a Vcore database named Database03 on server Server01.</span></span>

### <span data-ttu-id="1f7c6-117">Esempio 4: Creare un database senza server nel server specificato</span><span class="sxs-lookup"><span data-stu-id="1f7c6-117">Example 4: Create an Serverless database on the specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database04" -Edition "GeneralPurpose" -Vcore 2 -ComputeGeneration "Gen5" -ComputeModel Serverless
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database04
Location                      : Central US
DatabaseId                    : ef5a9698-012c-4def-8d94-7f6bfb7b4f04
Edition                       : GeneralPurpose
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 34359738368
Status                        : Online
CreationDate                  : 4/12/2019 11:20:29 PM
CurrentServiceObjectiveName   : GP_S_Gen5_2
RequestedServiceObjectiveName : GP_S_Gen5_2
ElasticPoolName               :
EarliestRestoreDate           : 4/12/2019 11:50:29 PM
Tags                          :
CreateMode                    :
ReadScale                     : Disabled
ZoneRedundant                 : False
Capacity                      : 2
Family                        : Gen5
SkuName                       : GP_S_Gen5
LicenseType                   : LicenseIncluded
AutoPauseDelayInMinutes       : 360
MinimumCapacity          : 0.5
```

<span data-ttu-id="1f7c6-118">Questo comando crea un database senza server denominato Database04 sul server01.</span><span class="sxs-lookup"><span data-stu-id="1f7c6-118">This command creates a Serverless database named Database04 on server Server01.</span></span>

## <span data-ttu-id="1f7c6-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f7c6-119">PARAMETERS</span></span>

### <span data-ttu-id="1f7c6-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f7c6-120">-AsJob</span></span>
<span data-ttu-id="1f7c6-121">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="1f7c6-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1f7c6-122">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="1f7c6-122">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="1f7c6-123">Ritardo di pausa automatico in minuti per il database (solo senza server), -1 per rifiutare esplicitamente</span><span class="sxs-lookup"><span data-stu-id="1f7c6-123">The auto pause delay in minutes for database(serverless only), -1 to opt out</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f7c6-124">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="1f7c6-124">-BackupStorageRedundancy</span></span>
<span data-ttu-id="1f7c6-125">Ridondanza di archiviazione di backup usata per archiviare i backup per SQL database.</span><span class="sxs-lookup"><span data-stu-id="1f7c6-125">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="1f7c6-126">Le opzioni disponibili sono: Locale, Area e Geo.</span><span class="sxs-lookup"><span data-stu-id="1f7c6-126">Options are: Local, Zone and Geo.</span></span>

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

### <span data-ttu-id="1f7c6-127">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="1f7c6-127">-CatalogCollation</span></span>
<span data-ttu-id="1f7c6-128">Specifica il nome della fascicolazione SQL del catalogo di database.</span><span class="sxs-lookup"><span data-stu-id="1f7c6-128">Specifies the name of the SQL database catalog collation.</span></span>

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

### <span data-ttu-id="1f7c6-129">-CollationName</span><span class="sxs-lookup"><span data-stu-id="1f7c6-129">-CollationName</span></span>
<span data-ttu-id="1f7c6-130">Specifica il nome della SQL regole di confronto del database.</span><span class="sxs-lookup"><span data-stu-id="1f7c6-130">Specifies the name of the SQL database collation.</span></span>

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

### <span data-ttu-id="1f7c6-131">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="1f7c6-131">-ComputeGeneration</span></span>
<span data-ttu-id="1f7c6-132">Generazione di elaborazione da assegnare.</span><span class="sxs-lookup"><span data-stu-id="1f7c6-132">The compute generation to assign.</span></span>

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

### <span data-ttu-id="1f7c6-133">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="1f7c6-133">-ComputeModel</span></span>
<span data-ttu-id="1f7c6-134">Modello di calcolo per il database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="1f7c6-134">The compute model for Azure Sql database.</span></span> <span data-ttu-id="1f7c6-135">Senza server o in provisioning</span><span class="sxs-lookup"><span data-stu-id="1f7c6-135">Serverless or Provisioned</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f7c6-136">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1f7c6-136">-DatabaseName</span></span>
<span data-ttu-id="1f7c6-137">Specifica il nome del database.</span><span class="sxs-lookup"><span data-stu-id="1f7c6-137">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="1f7c6-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f7c6-138">-DefaultProfile</span></span>
<span data-ttu-id="1f7c6-139">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1f7c6-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f7c6-140">-Edition</span><span class="sxs-lookup"><span data-stu-id="1f7c6-140">-Edition</span></span>
<span data-ttu-id="1f7c6-141">Specifica l'edizione da assegnare al database.</span><span class="sxs-lookup"><span data-stu-id="1f7c6-141">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="1f7c6-142">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="1f7c6-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1f7c6-143">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1f7c6-143">None</span></span>
- <span data-ttu-id="1f7c6-144">Di base</span><span class="sxs-lookup"><span data-stu-id="1f7c6-144">Basic</span></span>
- <span data-ttu-id="1f7c6-145">Standard</span><span class="sxs-lookup"><span data-stu-id="1f7c6-145">Standard</span></span>
- <span data-ttu-id="1f7c6-146">Premium</span><span class="sxs-lookup"><span data-stu-id="1f7c6-146">Premium</span></span>
- <span data-ttu-id="1f7c6-147">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="1f7c6-147">DataWarehouse</span></span>
- <span data-ttu-id="1f7c6-148">Gratis</span><span class="sxs-lookup"><span data-stu-id="1f7c6-148">Free</span></span>
- <span data-ttu-id="1f7c6-149">Estendamento</span><span class="sxs-lookup"><span data-stu-id="1f7c6-149">Stretch</span></span>
- <span data-ttu-id="1f7c6-150">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="1f7c6-150">GeneralPurpose</span></span>
- <span data-ttu-id="1f7c6-151">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="1f7c6-151">BusinessCritical</span></span>

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

### <span data-ttu-id="1f7c6-152">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="1f7c6-152">-ElasticPoolName</span></span>
<span data-ttu-id="1f7c6-153">Specifica il nome del pool flessibile in cui inserire il database.</span><span class="sxs-lookup"><span data-stu-id="1f7c6-153">Specifies the name of the elastic pool in which to put the database.</span></span>

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

### <span data-ttu-id="1f7c6-154">-Force</span><span class="sxs-lookup"><span data-stu-id="1f7c6-154">-Force</span></span>
<span data-ttu-id="1f7c6-155">Ignora messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="1f7c6-155">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="1f7c6-156">-HighAvailabilityReplicaCount</span><span class="sxs-lookup"><span data-stu-id="1f7c6-156">-HighAvailabilityReplicaCount</span></span>
<span data-ttu-id="1f7c6-157">Numero di replica secondarie di sola lettura associate al database a cui possono essere instradati le connessioni con lo scopo dell'applicazione di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="1f7c6-157">The number of readonly secondary replicas associated with the database to which readonly application intent connections may be routed.</span></span> <span data-ttu-id="1f7c6-158">Questa proprietà è impostata solo per i database dell'edizione Hyperscale.</span><span class="sxs-lookup"><span data-stu-id="1f7c6-158">This property is only settable for Hyperscale edition databases.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: ReadReplicaCount

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f7c6-159">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="1f7c6-159">-LicenseType</span></span>
<span data-ttu-id="1f7c6-160">Il tipo di licenza per il database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="1f7c6-160">The license type for the Azure Sql database.</span></span> <span data-ttu-id="1f7c6-161">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="1f7c6-161">Possible values are:</span></span>
- <span data-ttu-id="1f7c6-162">BasePrice - Viene applicato un prezzo scontato per Azure Hybrid Benefit (AHB) per i proprietari di licenze SQL Server licenze di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="1f7c6-162">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="1f7c6-163">Il prezzo del database verrà scontato per i proprietari SQL Server licenze esistenti.</span><span class="sxs-lookup"><span data-stu-id="1f7c6-163">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="1f7c6-164">LicenseIncluded - Il prezzo di sconto AHB (Azure Hybrid Benefit) per i proprietari SQL Server licenze non viene applicato.</span><span class="sxs-lookup"><span data-stu-id="1f7c6-164">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="1f7c6-165">Il prezzo del database includerà un costo SQL Server licenze.</span><span class="sxs-lookup"><span data-stu-id="1f7c6-165">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="1f7c6-166">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="1f7c6-166">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="1f7c6-167">ID di configurazione manutenzione per il SQL database.</span><span class="sxs-lookup"><span data-stu-id="1f7c6-167">The Maintenance configuration id for the SQL Database.</span></span>

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

### <span data-ttu-id="1f7c6-168">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="1f7c6-168">-MaxSizeBytes</span></span>
<span data-ttu-id="1f7c6-169">Specifica la dimensione massima del database in byte.</span><span class="sxs-lookup"><span data-stu-id="1f7c6-169">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="1f7c6-170">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="1f7c6-170">-MinimumCapacity</span></span>
<span data-ttu-id="1f7c6-171">La capacità minima assegnata al database sarà sempre allocata, se non sospesa.</span><span class="sxs-lookup"><span data-stu-id="1f7c6-171">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="1f7c6-172">Solo per database SQL di Azure senza server.</span><span class="sxs-lookup"><span data-stu-id="1f7c6-172">For serverless Azure Sql databases only.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases: MinVCore, MinCapacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f7c6-173">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="1f7c6-173">-ReadScale</span></span>
<span data-ttu-id="1f7c6-174">Se abilitate, le connessioni per cui lo scopo dell'applicazione è impostato su readonly nella stringa di connessione potrebbero essere instradati a una replica secondaria di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="1f7c6-174">If enabled, connections that have application intent set to readonly in their connection string may be routed to a readonly secondary replica.</span></span> <span data-ttu-id="1f7c6-175">Questa proprietà è impostata solo per i database Premium e Business Critical.</span><span class="sxs-lookup"><span data-stu-id="1f7c6-175">This property is only settable for Premium and Business Critical databases.</span></span>

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

### <span data-ttu-id="1f7c6-176">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="1f7c6-176">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="1f7c6-177">Specifica il nome dell'obiettivo del servizio da assegnare al database.</span><span class="sxs-lookup"><span data-stu-id="1f7c6-177">Specifies the name of the service objective to assign to the database.</span></span>

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

### <span data-ttu-id="1f7c6-178">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f7c6-178">-ResourceGroupName</span></span>
<span data-ttu-id="1f7c6-179">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="1f7c6-179">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="1f7c6-180">-SampleName</span><span class="sxs-lookup"><span data-stu-id="1f7c6-180">-SampleName</span></span>
<span data-ttu-id="1f7c6-181">Nome dello schema di esempio da applicare quando si crea il database.</span><span class="sxs-lookup"><span data-stu-id="1f7c6-181">The name of the sample schema to apply when creating this database.</span></span>

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

### <span data-ttu-id="1f7c6-182">-SecondaryType</span><span class="sxs-lookup"><span data-stu-id="1f7c6-182">-SecondaryType</span></span>
<span data-ttu-id="1f7c6-183">Tipo secondario del database, se secondario.</span><span class="sxs-lookup"><span data-stu-id="1f7c6-183">The secondary type of the database if it is a secondary.</span></span>  <span data-ttu-id="1f7c6-184">I valori validi sono Geo e Denominato.</span><span class="sxs-lookup"><span data-stu-id="1f7c6-184">Valid values are Geo and Named.</span></span>

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

### <span data-ttu-id="1f7c6-185">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1f7c6-185">-ServerName</span></span>
<span data-ttu-id="1f7c6-186">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="1f7c6-186">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="1f7c6-187">-Tag</span><span class="sxs-lookup"><span data-stu-id="1f7c6-187">-Tags</span></span>
<span data-ttu-id="1f7c6-188">Specifica un dizionario di coppie chiave-valore sotto forma di tabella hash che questo cmdlet associa al nuovo database.</span><span class="sxs-lookup"><span data-stu-id="1f7c6-188">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="1f7c6-189">Ad esempio: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="1f7c6-189">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1f7c6-190">-VCore</span><span class="sxs-lookup"><span data-stu-id="1f7c6-190">-VCore</span></span>
<span data-ttu-id="1f7c6-191">Numero Vcore per il database Sql di Azure</span><span class="sxs-lookup"><span data-stu-id="1f7c6-191">The Vcore number for the Azure Sql database</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity, MaxVCore, MaxCapacity

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f7c6-192">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="1f7c6-192">-ZoneRedundant</span></span>
<span data-ttu-id="1f7c6-193">La ridondanza dell'area da associare al database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="1f7c6-193">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="1f7c6-194">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f7c6-194">-Confirm</span></span>
<span data-ttu-id="1f7c6-195">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f7c6-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f7c6-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f7c6-196">-WhatIf</span></span>
<span data-ttu-id="1f7c6-197">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f7c6-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f7c6-198">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f7c6-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f7c6-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f7c6-199">CommonParameters</span></span>
<span data-ttu-id="1f7c6-200">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f7c6-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f7c6-201">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1f7c6-201">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f7c6-202">INPUT</span><span class="sxs-lookup"><span data-stu-id="1f7c6-202">INPUTS</span></span>

### <span data-ttu-id="1f7c6-203">System.String</span><span class="sxs-lookup"><span data-stu-id="1f7c6-203">System.String</span></span>

## <span data-ttu-id="1f7c6-204">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1f7c6-204">OUTPUTS</span></span>

### <span data-ttu-id="1f7c6-205">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="1f7c6-205">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="1f7c6-206">NOTE</span><span class="sxs-lookup"><span data-stu-id="1f7c6-206">NOTES</span></span>

## <span data-ttu-id="1f7c6-207">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1f7c6-207">RELATED LINKS</span></span>

[<span data-ttu-id="1f7c6-208">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1f7c6-208">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="1f7c6-209">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="1f7c6-209">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="1f7c6-210">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="1f7c6-210">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="1f7c6-211">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1f7c6-211">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="1f7c6-212">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1f7c6-212">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="1f7c6-213">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1f7c6-213">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="1f7c6-214">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1f7c6-214">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="1f7c6-215">documentazione SQL database</span><span class="sxs-lookup"><span data-stu-id="1f7c6-215">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

