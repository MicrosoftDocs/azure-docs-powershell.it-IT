---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
ms.openlocfilehash: 8fed3f32f5ff0a9920b87438b75cb25cee7c9217
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474905"
---
# <span data-ttu-id="4c83d-101">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="4c83d-101">New-AzSqlElasticPool</span></span>

## <span data-ttu-id="4c83d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4c83d-102">SYNOPSIS</span></span>
<span data-ttu-id="4c83d-103">Crea un pool di database elastici per un database SQL.</span><span class="sxs-lookup"><span data-stu-id="4c83d-103">Creates an elastic database pool for a SQL Database.</span></span>

## <span data-ttu-id="4c83d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4c83d-104">SYNTAX</span></span>

### <span data-ttu-id="4c83d-105">DtuBasedPool (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4c83d-105">DtuBasedPool (Default)</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c83d-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="4c83d-106">VcoreBasedPool</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> -Edition <String> [-StorageMB <Int32>] -VCore <Int32>
 -ComputeGeneration <String> [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c83d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4c83d-107">DESCRIPTION</span></span>
<span data-ttu-id="4c83d-108">Il cmdlet **New-AzSqlElasticPool** crea un pool di database elastici per un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="4c83d-108">The **New-AzSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>
<span data-ttu-id="4c83d-109">Diversi parametri (*-DTU,-DatabaseDtuMin e-DatabaseDtuMax*) richiedono che il valore impostato sia dall'elenco di valori validi per il parametro.</span><span class="sxs-lookup"><span data-stu-id="4c83d-109">Several parameters (*-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax*) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="4c83d-110">Ad esempio,-DatabaseDtuMax per un pool di eDTU standard di 100 può essere impostato solo su 10, 20, 50 o 100.</span><span class="sxs-lookup"><span data-stu-id="4c83d-110">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="4c83d-111">Per informazioni dettagliate sui valori validi, vedere la tabella per il pool di dimensioni specifiche in [pool elastici](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="4c83d-111">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="4c83d-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4c83d-112">EXAMPLES</span></span>

### <span data-ttu-id="4c83d-113">Esempio 1: creare un pool elastico di DTU</span><span class="sxs-lookup"><span data-stu-id="4c83d-113">Example 1: Create a DTU elastic pool</span></span>

```powershell
PS C:\>New-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Edition "Standard" -Dtu 400 -DatabaseDtuMin 10 -DatabaseDtuMax 100
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              :
```

<span data-ttu-id="4c83d-114">Questo comando crea un pool elastico nel livello di servizio standard denominato ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="4c83d-114">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="4c83d-115">Il server denominato Server01, assegnato a un gruppo di risorse di Azure denominato ResourceGroup01, ospita il pool di elastici in.</span><span class="sxs-lookup"><span data-stu-id="4c83d-115">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="4c83d-116">Il comando specifica i valori della proprietà DTU per il pool e i database nel pool.</span><span class="sxs-lookup"><span data-stu-id="4c83d-116">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

### <span data-ttu-id="4c83d-117">Esempio 2: creare un pool elastico di vCore</span><span class="sxs-lookup"><span data-stu-id="4c83d-117">Example 2: Create a vCore elastic pool</span></span>

```powershell
PS C:\> New-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Edition "GeneralPurpose" -vCore 2 -ComputeGeneration Gen5
ResourceId          : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/servers/server01/elasticPools/ElasticPool01
ResourceGroupName   : ResourceGroup01
ServerName          : Server01
ElasticPoolName     : ElasticPool01
Location            : Central US
CreationDate        : 8/29/2019 2:16:40 AM
State               : Ready
Edition             : GeneralPurpose
SkuName             : GP_Gen5
Dtu                 : 2
DatabaseDtuMax      : 2
DatabaseDtuMin      : 0
Capacity            : 2
DatabaseCapacityMin : 0
DatabaseCapacityMax : 2
Family              : Gen5
MaxSizeBytes        : 34359738368
StorageMB           : 32768
Tags                :
```

<span data-ttu-id="4c83d-118">Questo comando crea un pool elastico nel livello di servizio GengeralPurpose denominato ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="4c83d-118">This command creates an elastic pool in the GengeralPurpose service tier named ElasticPool01.</span></span> <span data-ttu-id="4c83d-119">Il server denominato Server01, assegnato a un gruppo di risorse di Azure denominato ResourceGroup01, ospita il pool di elastici in.</span><span class="sxs-lookup"><span data-stu-id="4c83d-119">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="4c83d-120">Il comando specifica i valori della proprietà vCore per il pool e i database nel pool.</span><span class="sxs-lookup"><span data-stu-id="4c83d-120">The command specifies the vCore property values for the pool and the databases in the pool.</span></span>

### <span data-ttu-id="4c83d-121">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="4c83d-121">Example 3</span></span>

<span data-ttu-id="4c83d-122">Crea un pool di database elastici per un database SQL.</span><span class="sxs-lookup"><span data-stu-id="4c83d-122">Creates an elastic database pool for a SQL Database.</span></span> <span data-ttu-id="4c83d-123">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="4c83d-123">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlElasticPool -ComputeGeneration Gen5 -Edition 'GeneralPurpose' -ElasticPoolName 'ElasticPool01' -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -StorageMB 2097152 -VCore 2
```

## <span data-ttu-id="4c83d-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4c83d-124">PARAMETERS</span></span>

### <span data-ttu-id="4c83d-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4c83d-125">-AsJob</span></span>
<span data-ttu-id="4c83d-126">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="4c83d-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4c83d-127">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="4c83d-127">-ComputeGeneration</span></span>
<span data-ttu-id="4c83d-128">Generazione di Compute da assegnare.</span><span class="sxs-lookup"><span data-stu-id="4c83d-128">The compute generation to assign.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c83d-129">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="4c83d-129">-DatabaseDtuMax</span></span>
<span data-ttu-id="4c83d-130">Specifica il numero massimo di unità di throughput del database (DTU) che ogni singolo database nel pool può utilizzare.</span><span class="sxs-lookup"><span data-stu-id="4c83d-130">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="4c83d-131">I valori predefiniti per le diverse edizioni sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="4c83d-131">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="4c83d-132">Base.</span><span class="sxs-lookup"><span data-stu-id="4c83d-132">Basic.</span></span> <span data-ttu-id="4c83d-133">5 DTU</span><span class="sxs-lookup"><span data-stu-id="4c83d-133">5 DTUs</span></span>
- <span data-ttu-id="4c83d-134">Standard.</span><span class="sxs-lookup"><span data-stu-id="4c83d-134">Standard.</span></span> <span data-ttu-id="4c83d-135">100 DTU</span><span class="sxs-lookup"><span data-stu-id="4c83d-135">100 DTUs</span></span>
- <span data-ttu-id="4c83d-136">Premium.</span><span class="sxs-lookup"><span data-stu-id="4c83d-136">Premium.</span></span> <span data-ttu-id="4c83d-137">125 DTU per informazioni dettagliate sui valori validi, vedere la tabella per il pool di dimensioni specifiche in [pool elastici](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="4c83d-137">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span>

```yaml
Type: System.Int32
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c83d-138">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="4c83d-138">-DatabaseDtuMin</span></span>
<span data-ttu-id="4c83d-139">Specifica il numero minimo di DTU che il pool elastico garantisce a tutti i database nel pool.</span><span class="sxs-lookup"><span data-stu-id="4c83d-139">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="4c83d-140">Il valore predefinito è zero (0).</span><span class="sxs-lookup"><span data-stu-id="4c83d-140">The default value is zero (0).</span></span>
<span data-ttu-id="4c83d-141">Per informazioni dettagliate sui valori validi, vedere la tabella per il pool di dimensioni specifiche in [pool elastici](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="4c83d-141">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

```yaml
Type: System.Int32
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c83d-142">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="4c83d-142">-DatabaseVCoreMax</span></span>
<span data-ttu-id="4c83d-143">Il numero massimo di VCore qualsiasi database di sqlazure può essere utilizzato nel pool.</span><span class="sxs-lookup"><span data-stu-id="4c83d-143">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

```yaml
Type: System.Double
Parameter Sets: VcoreBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c83d-144">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="4c83d-144">-DatabaseVCoreMin</span></span>
<span data-ttu-id="4c83d-145">Il numero minimo di VCore qualsiasi database di sqlazure può essere utilizzato nel pool.</span><span class="sxs-lookup"><span data-stu-id="4c83d-145">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

```yaml
Type: System.Double
Parameter Sets: VcoreBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c83d-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c83d-146">-DefaultProfile</span></span>
<span data-ttu-id="4c83d-147">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4c83d-147">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4c83d-148">-DTU</span><span class="sxs-lookup"><span data-stu-id="4c83d-148">-Dtu</span></span>
<span data-ttu-id="4c83d-149">Specifica il numero totale di DTU condivisi per il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="4c83d-149">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="4c83d-150">I valori predefiniti per le diverse edizioni sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="4c83d-150">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="4c83d-151">Base.</span><span class="sxs-lookup"><span data-stu-id="4c83d-151">Basic.</span></span>
<span data-ttu-id="4c83d-152">100 DTU</span><span class="sxs-lookup"><span data-stu-id="4c83d-152">100 DTUs</span></span>
- <span data-ttu-id="4c83d-153">Standard.</span><span class="sxs-lookup"><span data-stu-id="4c83d-153">Standard.</span></span>
<span data-ttu-id="4c83d-154">100 DTU</span><span class="sxs-lookup"><span data-stu-id="4c83d-154">100 DTUs</span></span>
- <span data-ttu-id="4c83d-155">Premium.</span><span class="sxs-lookup"><span data-stu-id="4c83d-155">Premium.</span></span>
<span data-ttu-id="4c83d-156">125 DTU per informazioni dettagliate sui valori validi, vedere la tabella per il pool di dimensioni specifiche in [pool elastici](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="4c83d-156">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

```yaml
Type: System.Int32
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c83d-157">-Edition</span><span class="sxs-lookup"><span data-stu-id="4c83d-157">-Edition</span></span>
<span data-ttu-id="4c83d-158">Specifica l'edizione del database SQL di Azure usato per il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="4c83d-158">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="4c83d-159">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="4c83d-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4c83d-160">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4c83d-160">None</span></span>
- <span data-ttu-id="4c83d-161">Base</span><span class="sxs-lookup"><span data-stu-id="4c83d-161">Basic</span></span>
- <span data-ttu-id="4c83d-162">Standard</span><span class="sxs-lookup"><span data-stu-id="4c83d-162">Standard</span></span>
- <span data-ttu-id="4c83d-163">Premium</span><span class="sxs-lookup"><span data-stu-id="4c83d-163">Premium</span></span>
- <span data-ttu-id="4c83d-164">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="4c83d-164">DataWarehouse</span></span>
- <span data-ttu-id="4c83d-165">Gratuito</span><span class="sxs-lookup"><span data-stu-id="4c83d-165">Free</span></span>
- <span data-ttu-id="4c83d-166">Tratto</span><span class="sxs-lookup"><span data-stu-id="4c83d-166">Stretch</span></span>
- <span data-ttu-id="4c83d-167">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="4c83d-167">GeneralPurpose</span></span>
- <span data-ttu-id="4c83d-168">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="4c83d-168">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: VcoreBasedPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c83d-169">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="4c83d-169">-ElasticPoolName</span></span>
<span data-ttu-id="4c83d-170">Specifica il nome del pool elastico creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c83d-170">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c83d-171">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="4c83d-171">-LicenseType</span></span>
<span data-ttu-id="4c83d-172">Tipo di licenza per il database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="4c83d-172">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="4c83d-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c83d-173">-ResourceGroupName</span></span>
<span data-ttu-id="4c83d-174">Specifica il nome del gruppo di risorse a cui questo cmdlet assegna il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="4c83d-174">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="4c83d-175">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="4c83d-175">-ServerName</span></span>
<span data-ttu-id="4c83d-176">Specifica il nome del server che ospita il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="4c83d-176">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="4c83d-177">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="4c83d-177">-StorageMB</span></span>
<span data-ttu-id="4c83d-178">Specifica il limite di archiviazione, in megabyte, per il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="4c83d-178">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="4c83d-179">Se non specifichi questo parametro, questo cmdlet calcola un valore che dipende dal valore del parametro *DTU* .</span><span class="sxs-lookup"><span data-stu-id="4c83d-179">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>
<span data-ttu-id="4c83d-180">Vedere [limiti di eDTU e archiviazione](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) per i valori possibili.</span><span class="sxs-lookup"><span data-stu-id="4c83d-180">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

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

### <span data-ttu-id="4c83d-181">-Tag</span><span class="sxs-lookup"><span data-stu-id="4c83d-181">-Tags</span></span>
<span data-ttu-id="4c83d-182">Specifica un dizionario di coppie chiave-valore in forma di tabella hash associata al pool elastico da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c83d-182">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="4c83d-183">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="4c83d-183">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4c83d-184">-VCore</span><span class="sxs-lookup"><span data-stu-id="4c83d-184">-VCore</span></span>
<span data-ttu-id="4c83d-185">Numero totale condiviso di Vcores per il pool elastico di SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="4c83d-185">The total shared number of Vcores for the Sql Azure Elastic Pool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c83d-186">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="4c83d-186">-ZoneRedundant</span></span>
<span data-ttu-id="4c83d-187">Ridondanza della zona da associare al pool di Azure SQL Elastic</span><span class="sxs-lookup"><span data-stu-id="4c83d-187">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="4c83d-188">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4c83d-188">-Confirm</span></span>
<span data-ttu-id="4c83d-189">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c83d-189">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c83d-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c83d-190">-WhatIf</span></span>
<span data-ttu-id="4c83d-191">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4c83d-191">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c83d-192">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4c83d-192">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c83d-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c83d-193">CommonParameters</span></span>
<span data-ttu-id="4c83d-194">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c83d-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c83d-195">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4c83d-195">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c83d-196">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4c83d-196">INPUTS</span></span>

### <span data-ttu-id="4c83d-197">System. String</span><span class="sxs-lookup"><span data-stu-id="4c83d-197">System.String</span></span>

## <span data-ttu-id="4c83d-198">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4c83d-198">OUTPUTS</span></span>

### <span data-ttu-id="4c83d-199">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="4c83d-199">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="4c83d-200">Note</span><span class="sxs-lookup"><span data-stu-id="4c83d-200">NOTES</span></span>

## <span data-ttu-id="4c83d-201">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4c83d-201">RELATED LINKS</span></span>

[<span data-ttu-id="4c83d-202">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="4c83d-202">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="4c83d-203">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="4c83d-203">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="4c83d-204">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="4c83d-204">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="4c83d-205">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="4c83d-205">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="4c83d-206">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="4c83d-206">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="4c83d-207">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="4c83d-207">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
