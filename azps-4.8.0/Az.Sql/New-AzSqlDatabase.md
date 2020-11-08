---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
ms.openlocfilehash: 264fecd37738a0da484c28f1ec8ce84f14efe159
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188778"
---
# <span data-ttu-id="0a753-101">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0a753-101">New-AzSqlDatabase</span></span>

## <span data-ttu-id="0a753-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0a753-102">SYNOPSIS</span></span>
<span data-ttu-id="0a753-103">Crea un database o un database elastico.</span><span class="sxs-lookup"><span data-stu-id="0a753-103">Creates a database or an elastic database.</span></span>

## <span data-ttu-id="0a753-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0a753-104">SYNTAX</span></span>

### <span data-ttu-id="0a753-105">DtuBasedDatabase (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0a753-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <String>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-Force] [-LicenseType <String>] [-AutoPauseDelayInMinutes <Int32>]
 [-MinimumCapacity <Double>] [-ReadReplicaCount <Int32>] [-BackupStorageRedundancy <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a753-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="0a753-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] -Edition <String> [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>]
 [-SampleName <String>] [-ZoneRedundant] [-AsJob] [-Force] -VCore <Int32> -ComputeGeneration <String>
 [-LicenseType <String>] [-ComputeModel <String>] [-AutoPauseDelayInMinutes <Int32>]
 [-MinimumCapacity <Double>] [-ReadReplicaCount <Int32>] [-BackupStorageRedundancy <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a753-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0a753-107">DESCRIPTION</span></span>
<span data-ttu-id="0a753-108">Il cmdlet **New-AzSqlDatabase** crea un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="0a753-108">The **New-AzSqlDatabase** cmdlet creates an Azure SQL database.</span></span>
<span data-ttu-id="0a753-109">Puoi anche creare un database elastico impostando il parametro *ElasticPoolName* su un pool elastico esistente.</span><span class="sxs-lookup"><span data-stu-id="0a753-109">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="0a753-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0a753-110">EXAMPLES</span></span>

### <span data-ttu-id="0a753-111">Esempio 1: creare un database in un server specificato</span><span class="sxs-lookup"><span data-stu-id="0a753-111">Example 1: Create a database on a specified server</span></span>
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

<span data-ttu-id="0a753-112">Questo comando crea un database denominato Database01 nel server Server01.</span><span class="sxs-lookup"><span data-stu-id="0a753-112">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="0a753-113">Esempio 2: creare un database elastico in un server specificato</span><span class="sxs-lookup"><span data-stu-id="0a753-113">Example 2: Create an elastic database on a specified server</span></span>
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

<span data-ttu-id="0a753-114">Questo comando crea un database denominato Database02 nel pool elastico denominato ElasticPool01 nel server Server01.</span><span class="sxs-lookup"><span data-stu-id="0a753-114">This command creates a database named Database02 in the elastic pool named ElasticPool01 on server Server01.</span></span>

### <span data-ttu-id="0a753-115">Esempio 3: creare un database di Vcore in un server specificato</span><span class="sxs-lookup"><span data-stu-id="0a753-115">Example 3: Create an Vcore database on a specified server</span></span>
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

<span data-ttu-id="0a753-116">Questo comando crea un database di Vcore denominato Database03 nel server Server01.</span><span class="sxs-lookup"><span data-stu-id="0a753-116">This command creates a Vcore database named Database03 on server Server01.</span></span>

### <span data-ttu-id="0a753-117">Esempio 4: creare un database non server nel server specificato</span><span class="sxs-lookup"><span data-stu-id="0a753-117">Example 4: Create an Serverless database on the specified server</span></span>
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

<span data-ttu-id="0a753-118">Questo comando crea un database server non denominato Database04 nel server Server01.</span><span class="sxs-lookup"><span data-stu-id="0a753-118">This command creates a Serverless database named Database04 on server Server01.</span></span>

## <span data-ttu-id="0a753-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0a753-119">PARAMETERS</span></span>

### <span data-ttu-id="0a753-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a753-120">-AsJob</span></span>
<span data-ttu-id="0a753-121">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="0a753-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0a753-122">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="0a753-122">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="0a753-123">Ritardo di pausa automatica in minuti per il database (solo server),-1 per rifiutare la disattivazione</span><span class="sxs-lookup"><span data-stu-id="0a753-123">The auto pause delay in minutes for database(serverless only), -1 to opt out</span></span>

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

### <span data-ttu-id="0a753-124">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="0a753-124">-BackupStorageRedundancy</span></span>
<span data-ttu-id="0a753-125">Ridondanza dello spazio di archiviazione di backup utilizzata per archiviare i backup per il database SQL.</span><span class="sxs-lookup"><span data-stu-id="0a753-125">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="0a753-126">Le opzioni disponibili sono: locale, zona e geo.</span><span class="sxs-lookup"><span data-stu-id="0a753-126">Options are: Local, Zone and Geo.</span></span>

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

### <span data-ttu-id="0a753-127">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="0a753-127">-CatalogCollation</span></span>
<span data-ttu-id="0a753-128">Specifica il nome delle regole di confronto del catalogo di database SQL.</span><span class="sxs-lookup"><span data-stu-id="0a753-128">Specifies the name of the SQL database catalog collation.</span></span>

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

### <span data-ttu-id="0a753-129">-CollationName</span><span class="sxs-lookup"><span data-stu-id="0a753-129">-CollationName</span></span>
<span data-ttu-id="0a753-130">Specifica il nome delle regole di confronto del database SQL.</span><span class="sxs-lookup"><span data-stu-id="0a753-130">Specifies the name of the SQL database collation.</span></span>

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

### <span data-ttu-id="0a753-131">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="0a753-131">-ComputeGeneration</span></span>
<span data-ttu-id="0a753-132">Generazione di Compute da assegnare.</span><span class="sxs-lookup"><span data-stu-id="0a753-132">The compute generation to assign.</span></span>

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

### <span data-ttu-id="0a753-133">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="0a753-133">-ComputeModel</span></span>
<span data-ttu-id="0a753-134">Il modello di calcolo per il database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="0a753-134">The compute model for Azure Sql database.</span></span> <span data-ttu-id="0a753-135">Server o provisioning</span><span class="sxs-lookup"><span data-stu-id="0a753-135">Serverless or Provisioned</span></span>

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

### <span data-ttu-id="0a753-136">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0a753-136">-DatabaseName</span></span>
<span data-ttu-id="0a753-137">Specifica il nome del database.</span><span class="sxs-lookup"><span data-stu-id="0a753-137">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="0a753-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a753-138">-DefaultProfile</span></span>
<span data-ttu-id="0a753-139">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0a753-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a753-140">-Edition</span><span class="sxs-lookup"><span data-stu-id="0a753-140">-Edition</span></span>
<span data-ttu-id="0a753-141">Specifica l'edizione da assegnare al database.</span><span class="sxs-lookup"><span data-stu-id="0a753-141">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="0a753-142">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="0a753-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0a753-143">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0a753-143">None</span></span>
- <span data-ttu-id="0a753-144">Base</span><span class="sxs-lookup"><span data-stu-id="0a753-144">Basic</span></span>
- <span data-ttu-id="0a753-145">Standard</span><span class="sxs-lookup"><span data-stu-id="0a753-145">Standard</span></span>
- <span data-ttu-id="0a753-146">Premium</span><span class="sxs-lookup"><span data-stu-id="0a753-146">Premium</span></span>
- <span data-ttu-id="0a753-147">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="0a753-147">DataWarehouse</span></span>
- <span data-ttu-id="0a753-148">Gratuito</span><span class="sxs-lookup"><span data-stu-id="0a753-148">Free</span></span>
- <span data-ttu-id="0a753-149">Tratto</span><span class="sxs-lookup"><span data-stu-id="0a753-149">Stretch</span></span>
- <span data-ttu-id="0a753-150">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="0a753-150">GeneralPurpose</span></span>
- <span data-ttu-id="0a753-151">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="0a753-151">BusinessCritical</span></span>

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

### <span data-ttu-id="0a753-152">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="0a753-152">-ElasticPoolName</span></span>
<span data-ttu-id="0a753-153">Specifica il nome del pool elastico in cui inserire il database.</span><span class="sxs-lookup"><span data-stu-id="0a753-153">Specifies the name of the elastic pool in which to put the database.</span></span>

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

### <span data-ttu-id="0a753-154">-Force</span><span class="sxs-lookup"><span data-stu-id="0a753-154">-Force</span></span>
<span data-ttu-id="0a753-155">Ignorare il messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="0a753-155">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="0a753-156">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="0a753-156">-LicenseType</span></span>
<span data-ttu-id="0a753-157">Tipo di licenza per il database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="0a753-157">The license type for the Azure Sql database.</span></span> <span data-ttu-id="0a753-158">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="0a753-158">Possible values are:</span></span>
- <span data-ttu-id="0a753-159">BasePrice-Azure Hybrid benefit (AHB) i prezzi scontati per i proprietari di licenze di SQL Server esistenti vengono applicati.</span><span class="sxs-lookup"><span data-stu-id="0a753-159">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="0a753-160">Il prezzo del database verrà scontato per i proprietari di licenze di SQL Server esistenti.</span><span class="sxs-lookup"><span data-stu-id="0a753-160">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="0a753-161">LicenseIncluded-Azure Hybrid benefit (AHB) i prezzi di sconto per i proprietari di licenze di SQL Server esistenti non vengono applicati.</span><span class="sxs-lookup"><span data-stu-id="0a753-161">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="0a753-162">Prezzo database includerà un nuovo costo per la licenza di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0a753-162">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="0a753-163">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="0a753-163">-MaxSizeBytes</span></span>
<span data-ttu-id="0a753-164">Specifica la dimensione massima del database in byte.</span><span class="sxs-lookup"><span data-stu-id="0a753-164">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="0a753-165">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="0a753-165">-MinimumCapacity</span></span>
<span data-ttu-id="0a753-166">La capacità minima che il database avrà sempre allocato, se non in pausa.</span><span class="sxs-lookup"><span data-stu-id="0a753-166">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="0a753-167">Solo per i database SQL di Azure server.</span><span class="sxs-lookup"><span data-stu-id="0a753-167">For serverless Azure Sql databases only.</span></span>

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

### <span data-ttu-id="0a753-168">-ReadReplicaCount</span><span class="sxs-lookup"><span data-stu-id="0a753-168">-ReadReplicaCount</span></span>
<span data-ttu-id="0a753-169">Numero di repliche secondarie ReadOnly associate al database in cui possono essere instradate le connessioni intenti all'applicazione ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="0a753-169">The number of readonly secondary replicas associated with the database to which readonly application intent connections may be routed.</span></span> <span data-ttu-id="0a753-170">Questa proprietà è impostabile solo per i database di iperscala Edition.</span><span class="sxs-lookup"><span data-stu-id="0a753-170">This property is only settable for Hyperscale edition databases.</span></span>

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

### <span data-ttu-id="0a753-171">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="0a753-171">-ReadScale</span></span>
<span data-ttu-id="0a753-172">Se abilitata, le connessioni che hanno lo scopo dell'applicazione impostato su ReadOnly nella stringa di connessione possono essere instradate a una replica secondaria ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="0a753-172">If enabled, connections that have application intent set to readonly in their connection string may be routed to a readonly secondary replica.</span></span> <span data-ttu-id="0a753-173">Questa proprietà è impostabile solo per i database Premium e business critical.</span><span class="sxs-lookup"><span data-stu-id="0a753-173">This property is only settable for Premium and Business Critical databases.</span></span>

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

### <span data-ttu-id="0a753-174">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="0a753-174">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="0a753-175">Specifica il nome dell'obiettivo del servizio da assegnare al database.</span><span class="sxs-lookup"><span data-stu-id="0a753-175">Specifies the name of the service objective to assign to the database.</span></span>

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

### <span data-ttu-id="0a753-176">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a753-176">-ResourceGroupName</span></span>
<span data-ttu-id="0a753-177">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="0a753-177">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="0a753-178">-Samplename</span><span class="sxs-lookup"><span data-stu-id="0a753-178">-SampleName</span></span>
<span data-ttu-id="0a753-179">Nome dello schema di esempio da applicare quando si crea questo database.</span><span class="sxs-lookup"><span data-stu-id="0a753-179">The name of the sample schema to apply when creating this database.</span></span>

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

### <span data-ttu-id="0a753-180">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="0a753-180">-ServerName</span></span>
<span data-ttu-id="0a753-181">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="0a753-181">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="0a753-182">-Tag</span><span class="sxs-lookup"><span data-stu-id="0a753-182">-Tags</span></span>
<span data-ttu-id="0a753-183">Specifica un dizionario di coppie chiave-valore in forma di tabella hash che questo cmdlet associa al nuovo database.</span><span class="sxs-lookup"><span data-stu-id="0a753-183">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="0a753-184">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="0a753-184">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="0a753-185">-VCore</span><span class="sxs-lookup"><span data-stu-id="0a753-185">-VCore</span></span>
<span data-ttu-id="0a753-186">Numero Vcore per il database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="0a753-186">The Vcore number for the Azure Sql database</span></span>

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

### <span data-ttu-id="0a753-187">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="0a753-187">-ZoneRedundant</span></span>
<span data-ttu-id="0a753-188">Ridondanza della zona da associare al database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="0a753-188">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="0a753-189">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0a753-189">-Confirm</span></span>
<span data-ttu-id="0a753-190">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a753-190">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a753-191">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a753-191">-WhatIf</span></span>
<span data-ttu-id="0a753-192">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0a753-192">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a753-193">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0a753-193">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a753-194">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a753-194">CommonParameters</span></span>
<span data-ttu-id="0a753-195">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a753-195">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a753-196">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0a753-196">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a753-197">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0a753-197">INPUTS</span></span>

### <span data-ttu-id="0a753-198">System. String</span><span class="sxs-lookup"><span data-stu-id="0a753-198">System.String</span></span>

## <span data-ttu-id="0a753-199">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0a753-199">OUTPUTS</span></span>

### <span data-ttu-id="0a753-200">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="0a753-200">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="0a753-201">Note</span><span class="sxs-lookup"><span data-stu-id="0a753-201">NOTES</span></span>

## <span data-ttu-id="0a753-202">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0a753-202">RELATED LINKS</span></span>

[<span data-ttu-id="0a753-203">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0a753-203">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="0a753-204">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="0a753-204">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="0a753-205">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="0a753-205">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="0a753-206">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0a753-206">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="0a753-207">Curriculum vitae-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0a753-207">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="0a753-208">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0a753-208">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="0a753-209">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0a753-209">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="0a753-210">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="0a753-210">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

