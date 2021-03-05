---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
ms.openlocfilehash: d625e28b0007a9dc99434f0257a910ea804e3644
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970206"
---
# <span data-ttu-id="a8f32-101">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a8f32-101">New-AzSqlElasticPool</span></span>

## <span data-ttu-id="a8f32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8f32-102">SYNOPSIS</span></span>
<span data-ttu-id="a8f32-103">Crea un pool di database flessibile per un SQL database.</span><span class="sxs-lookup"><span data-stu-id="a8f32-103">Creates an elastic database pool for a SQL Database.</span></span>

## <span data-ttu-id="a8f32-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a8f32-104">SYNTAX</span></span>

### <span data-ttu-id="a8f32-105">DtuBasedPool (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a8f32-105">DtuBasedPool (Default)</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-MaintenanceConfigurationId <String>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8f32-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="a8f32-106">VcoreBasedPool</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> -Edition <String> [-StorageMB <Int32>] -VCore <Int32>
 -ComputeGeneration <String> [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-MaintenanceConfigurationId <String>] [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8f32-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a8f32-107">DESCRIPTION</span></span>
<span data-ttu-id="a8f32-108">Il cmdlet **New-AzSqlElasticPool** crea un pool di database flessibile per un database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a8f32-108">The **New-AzSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>
<span data-ttu-id="a8f32-109">Diversi parametri (*-Dtu, -DatabaseDtuMin e -DatabaseDtuMax*) richiedono che il valore impostato sia in un elenco di valori validi per il parametro.</span><span class="sxs-lookup"><span data-stu-id="a8f32-109">Several parameters (*-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax*) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="a8f32-110">Ad esempio, -DatabaseDtuMax per un pool eDTU Standard 100 può essere impostato solo su 10, 20, 50 o 100.</span><span class="sxs-lookup"><span data-stu-id="a8f32-110">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="a8f32-111">Per informazioni dettagliate sui valori validi, vedere la tabella per il pool di dimensioni specifico in [pool di dimensioni elastiche.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="a8f32-111">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="a8f32-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a8f32-112">EXAMPLES</span></span>

### <span data-ttu-id="a8f32-113">Esempio 1: Creare un pool flessibile DTU</span><span class="sxs-lookup"><span data-stu-id="a8f32-113">Example 1: Create a DTU elastic pool</span></span>

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

<span data-ttu-id="a8f32-114">Questo comando crea un pool flessibile nel livello di servizio Standard denominato ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="a8f32-114">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="a8f32-115">Il server denominato server01, assegnato a un gruppo di risorse di Azure denominato ResourceGroup01, ospita il pool flessibile.</span><span class="sxs-lookup"><span data-stu-id="a8f32-115">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="a8f32-116">Il comando specifica i valori delle proprietà DTU per il pool e i database nel pool.</span><span class="sxs-lookup"><span data-stu-id="a8f32-116">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

### <span data-ttu-id="a8f32-117">Esempio 2: Creare un pool elastico vCore</span><span class="sxs-lookup"><span data-stu-id="a8f32-117">Example 2: Create a vCore elastic pool</span></span>

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

<span data-ttu-id="a8f32-118">Questo comando crea un pool flessibile nel livello di servizio GengeralPurpose denominato ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="a8f32-118">This command creates an elastic pool in the GengeralPurpose service tier named ElasticPool01.</span></span> <span data-ttu-id="a8f32-119">Il server denominato server01, assegnato a un gruppo di risorse di Azure denominato ResourceGroup01, ospita il pool flessibile.</span><span class="sxs-lookup"><span data-stu-id="a8f32-119">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="a8f32-120">Il comando specifica i valori delle proprietà vCore per il pool e i database nel pool.</span><span class="sxs-lookup"><span data-stu-id="a8f32-120">The command specifies the vCore property values for the pool and the databases in the pool.</span></span>

### <span data-ttu-id="a8f32-121">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="a8f32-121">Example 3</span></span>

<span data-ttu-id="a8f32-122">Crea un pool di database flessibile per un SQL database.</span><span class="sxs-lookup"><span data-stu-id="a8f32-122">Creates an elastic database pool for a SQL Database.</span></span> <span data-ttu-id="a8f32-123">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="a8f32-123">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlElasticPool -ComputeGeneration Gen5 -Edition 'GeneralPurpose' -ElasticPoolName 'ElasticPool01' -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -StorageMB 2097152 -VCore 2
```

## <span data-ttu-id="a8f32-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8f32-124">PARAMETERS</span></span>

### <span data-ttu-id="a8f32-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a8f32-125">-AsJob</span></span>
<span data-ttu-id="a8f32-126">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a8f32-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a8f32-127">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="a8f32-127">-ComputeGeneration</span></span>
<span data-ttu-id="a8f32-128">Generazione di elaborazione da assegnare.</span><span class="sxs-lookup"><span data-stu-id="a8f32-128">The compute generation to assign.</span></span>

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

### <span data-ttu-id="a8f32-129">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="a8f32-129">-DatabaseDtuMax</span></span>
<span data-ttu-id="a8f32-130">Specifica il numero massimo di DKU (Database Throughput Units) che qualsiasi database nel pool può utilizzare.</span><span class="sxs-lookup"><span data-stu-id="a8f32-130">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="a8f32-131">I valori predefiniti per le diverse edizioni sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a8f32-131">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="a8f32-132">Di base.</span><span class="sxs-lookup"><span data-stu-id="a8f32-132">Basic.</span></span> <span data-ttu-id="a8f32-133">5 DKU</span><span class="sxs-lookup"><span data-stu-id="a8f32-133">5 DTUs</span></span>
- <span data-ttu-id="a8f32-134">Standard.</span><span class="sxs-lookup"><span data-stu-id="a8f32-134">Standard.</span></span> <span data-ttu-id="a8f32-135">100 DKU</span><span class="sxs-lookup"><span data-stu-id="a8f32-135">100 DTUs</span></span>
- <span data-ttu-id="a8f32-136">Premium.</span><span class="sxs-lookup"><span data-stu-id="a8f32-136">Premium.</span></span> <span data-ttu-id="a8f32-137">125 DKU Per informazioni dettagliate sui valori validi, vedere la tabella per il pool di dimensioni specifico in [pool di elastici](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="a8f32-137">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span>

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

### <span data-ttu-id="a8f32-138">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="a8f32-138">-DatabaseDtuMin</span></span>
<span data-ttu-id="a8f32-139">Specifica il numero minimo di DKU garantiti dal pool flessibile a tutti i database del pool.</span><span class="sxs-lookup"><span data-stu-id="a8f32-139">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="a8f32-140">Il valore predefinito è zero (0).</span><span class="sxs-lookup"><span data-stu-id="a8f32-140">The default value is zero (0).</span></span>
<span data-ttu-id="a8f32-141">Per informazioni dettagliate sui valori validi, vedere la tabella per il pool di dimensioni specifico in [pool di dimensioni elastiche.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="a8f32-141">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="a8f32-142">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="a8f32-142">-DatabaseVCoreMax</span></span>
<span data-ttu-id="a8f32-143">Numero VCore massimo che qualsiasi database SqlAzure può usare nel pool.</span><span class="sxs-lookup"><span data-stu-id="a8f32-143">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="a8f32-144">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="a8f32-144">-DatabaseVCoreMin</span></span>
<span data-ttu-id="a8f32-145">Valore VCore minimo che qualsiasi database SqlAzure può usare nel pool.</span><span class="sxs-lookup"><span data-stu-id="a8f32-145">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="a8f32-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8f32-146">-DefaultProfile</span></span>
<span data-ttu-id="a8f32-147">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a8f32-147">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a8f32-148">-Dtu</span><span class="sxs-lookup"><span data-stu-id="a8f32-148">-Dtu</span></span>
<span data-ttu-id="a8f32-149">Specifica il numero totale di DKU condivise per il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="a8f32-149">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="a8f32-150">I valori predefiniti per le diverse edizioni sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a8f32-150">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="a8f32-151">Di base.</span><span class="sxs-lookup"><span data-stu-id="a8f32-151">Basic.</span></span>
<span data-ttu-id="a8f32-152">100 DKU</span><span class="sxs-lookup"><span data-stu-id="a8f32-152">100 DTUs</span></span>
- <span data-ttu-id="a8f32-153">Standard.</span><span class="sxs-lookup"><span data-stu-id="a8f32-153">Standard.</span></span>
<span data-ttu-id="a8f32-154">100 DKU</span><span class="sxs-lookup"><span data-stu-id="a8f32-154">100 DTUs</span></span>
- <span data-ttu-id="a8f32-155">Premium.</span><span class="sxs-lookup"><span data-stu-id="a8f32-155">Premium.</span></span>
<span data-ttu-id="a8f32-156">125 DKU Per informazioni dettagliate sui valori validi, vedere la tabella per il pool di dimensioni specifico in pool [di dimensioni elastiche.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="a8f32-156">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="a8f32-157">-Edition</span><span class="sxs-lookup"><span data-stu-id="a8f32-157">-Edition</span></span>
<span data-ttu-id="a8f32-158">Specifica l'edizione del database SQL Azure usato per il pool flessibile.</span><span class="sxs-lookup"><span data-stu-id="a8f32-158">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="a8f32-159">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="a8f32-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a8f32-160">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a8f32-160">None</span></span>
- <span data-ttu-id="a8f32-161">Di base</span><span class="sxs-lookup"><span data-stu-id="a8f32-161">Basic</span></span>
- <span data-ttu-id="a8f32-162">Standard</span><span class="sxs-lookup"><span data-stu-id="a8f32-162">Standard</span></span>
- <span data-ttu-id="a8f32-163">Premium</span><span class="sxs-lookup"><span data-stu-id="a8f32-163">Premium</span></span>
- <span data-ttu-id="a8f32-164">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="a8f32-164">DataWarehouse</span></span>
- <span data-ttu-id="a8f32-165">Gratis</span><span class="sxs-lookup"><span data-stu-id="a8f32-165">Free</span></span>
- <span data-ttu-id="a8f32-166">Estendamento</span><span class="sxs-lookup"><span data-stu-id="a8f32-166">Stretch</span></span>
- <span data-ttu-id="a8f32-167">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="a8f32-167">GeneralPurpose</span></span>
- <span data-ttu-id="a8f32-168">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="a8f32-168">BusinessCritical</span></span>

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

### <span data-ttu-id="a8f32-169">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="a8f32-169">-ElasticPoolName</span></span>
<span data-ttu-id="a8f32-170">Specifica il nome del pool flessibile creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8f32-170">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="a8f32-171">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="a8f32-171">-LicenseType</span></span>
<span data-ttu-id="a8f32-172">Il tipo di licenza per il database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="a8f32-172">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="a8f32-173">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="a8f32-173">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="a8f32-174">ID configurazione manutenzione per il pool SQL elastico.</span><span class="sxs-lookup"><span data-stu-id="a8f32-174">The Maintenance configuration id for the SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="a8f32-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8f32-175">-ResourceGroupName</span></span>
<span data-ttu-id="a8f32-176">Specifica il nome del gruppo di risorse a cui questo cmdlet assegna il pool flessibile.</span><span class="sxs-lookup"><span data-stu-id="a8f32-176">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="a8f32-177">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a8f32-177">-ServerName</span></span>
<span data-ttu-id="a8f32-178">Specifica il nome del server che ospita il pool flessibile.</span><span class="sxs-lookup"><span data-stu-id="a8f32-178">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="a8f32-179">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="a8f32-179">-StorageMB</span></span>
<span data-ttu-id="a8f32-180">Specifica il limite di archiviazione, in megabyte, per il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="a8f32-180">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="a8f32-181">Se non si specifica questo parametro, questo cmdlet calcola un valore che dipende dal valore del *parametro Dtu.*</span><span class="sxs-lookup"><span data-stu-id="a8f32-181">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>
<span data-ttu-id="a8f32-182">Vedere [i limiti di eDTU e di archiviazione](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) per i valori possibili.</span><span class="sxs-lookup"><span data-stu-id="a8f32-182">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

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

### <span data-ttu-id="a8f32-183">-Tag</span><span class="sxs-lookup"><span data-stu-id="a8f32-183">-Tags</span></span>
<span data-ttu-id="a8f32-184">Specifica un dizionario di coppie chiave-valore sotto forma di tabella hash che questo cmdlet associa al pool elastico.</span><span class="sxs-lookup"><span data-stu-id="a8f32-184">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="a8f32-185">Ad esempio: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="a8f32-185">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a8f32-186">-VCore</span><span class="sxs-lookup"><span data-stu-id="a8f32-186">-VCore</span></span>
<span data-ttu-id="a8f32-187">Il numero totale condiviso di Vcore per il pool di sql azure elastico.</span><span class="sxs-lookup"><span data-stu-id="a8f32-187">The total shared number of Vcores for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="a8f32-188">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="a8f32-188">-ZoneRedundant</span></span>
<span data-ttu-id="a8f32-189">La ridondanza dell'area da associare al pool sql elastico di Azure</span><span class="sxs-lookup"><span data-stu-id="a8f32-189">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="a8f32-190">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a8f32-190">-Confirm</span></span>
<span data-ttu-id="a8f32-191">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8f32-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8f32-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8f32-192">-WhatIf</span></span>
<span data-ttu-id="a8f32-193">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a8f32-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8f32-194">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a8f32-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8f32-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8f32-195">CommonParameters</span></span>
<span data-ttu-id="a8f32-196">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8f32-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8f32-197">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a8f32-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8f32-198">INPUT</span><span class="sxs-lookup"><span data-stu-id="a8f32-198">INPUTS</span></span>

### <span data-ttu-id="a8f32-199">System.String</span><span class="sxs-lookup"><span data-stu-id="a8f32-199">System.String</span></span>

## <span data-ttu-id="a8f32-200">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a8f32-200">OUTPUTS</span></span>

### <span data-ttu-id="a8f32-201">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="a8f32-201">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="a8f32-202">NOTE</span><span class="sxs-lookup"><span data-stu-id="a8f32-202">NOTES</span></span>

## <span data-ttu-id="a8f32-203">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a8f32-203">RELATED LINKS</span></span>

[<span data-ttu-id="a8f32-204">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a8f32-204">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="a8f32-205">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="a8f32-205">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="a8f32-206">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="a8f32-206">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="a8f32-207">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a8f32-207">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="a8f32-208">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a8f32-208">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="a8f32-209">documentazione SQL database</span><span class="sxs-lookup"><span data-stu-id="a8f32-209">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
