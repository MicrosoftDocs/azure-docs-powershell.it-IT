---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
ms.openlocfilehash: 8fbc0d1e1ac32906c081c5a9714c8420e0f1292e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676850"
---
# <span data-ttu-id="7a640-101">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="7a640-101">New-AzSqlElasticPool</span></span>

## <span data-ttu-id="7a640-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7a640-102">SYNOPSIS</span></span>
<span data-ttu-id="7a640-103">Crea un pool di database elastici per un database SQL.</span><span class="sxs-lookup"><span data-stu-id="7a640-103">Creates an elastic database pool for a SQL Database.</span></span>

## <span data-ttu-id="7a640-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7a640-104">SYNTAX</span></span>

### <span data-ttu-id="7a640-105">DtuBasedPool (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7a640-105">DtuBasedPool (Default)</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a640-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="7a640-106">VcoreBasedPool</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> -Edition <String> [-StorageMB <Int32>] -VCore <Int32>
 -ComputeGeneration <String> [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a640-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a640-107">DESCRIPTION</span></span>
<span data-ttu-id="7a640-108">Il cmdlet **New-AzSqlElasticPool** crea un pool di database elastici per un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="7a640-108">The **New-AzSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>
<span data-ttu-id="7a640-109">Diversi parametri ( *-DTU,-DatabaseDtuMin e-DatabaseDtuMax* ) richiedono che il valore impostato sia dall'elenco di valori validi per il parametro.</span><span class="sxs-lookup"><span data-stu-id="7a640-109">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="7a640-110">Ad esempio,-DatabaseDtuMax per un pool di eDTU standard di 100 può essere impostato solo su 10, 20, 50 o 100.</span><span class="sxs-lookup"><span data-stu-id="7a640-110">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="7a640-111">Per informazioni dettagliate sui valori validi, vedere la tabella per il pool di dimensioni specifiche in [pool elastici](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="7a640-111">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="7a640-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7a640-112">EXAMPLES</span></span>

### <span data-ttu-id="7a640-113">Esempio 1: creare un pool elastico</span><span class="sxs-lookup"><span data-stu-id="7a640-113">Example 1: Create an elastic pool</span></span>
```
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

<span data-ttu-id="7a640-114">Questo comando crea un pool elastico nel livello di servizio standard denominato ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="7a640-114">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="7a640-115">Il server denominato Server01, assegnato a un gruppo di risorse di Azure denominato ResourceGroup01, ospita il pool di elastici in.</span><span class="sxs-lookup"><span data-stu-id="7a640-115">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="7a640-116">Il comando specifica i valori della proprietà DTU per il pool e i database nel pool.</span><span class="sxs-lookup"><span data-stu-id="7a640-116">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

## <span data-ttu-id="7a640-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7a640-117">PARAMETERS</span></span>

### <span data-ttu-id="7a640-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a640-118">-AsJob</span></span>
<span data-ttu-id="7a640-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7a640-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7a640-120">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="7a640-120">-ComputeGeneration</span></span>
<span data-ttu-id="7a640-121">Generazione di Compute da assegnare.</span><span class="sxs-lookup"><span data-stu-id="7a640-121">The compute generation to assign.</span></span>

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

### <span data-ttu-id="7a640-122">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="7a640-122">-DatabaseDtuMax</span></span>
<span data-ttu-id="7a640-123">Specifica il numero massimo di unità di throughput del database (DTU) che ogni singolo database nel pool può utilizzare.</span><span class="sxs-lookup"><span data-stu-id="7a640-123">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="7a640-124">I valori predefiniti per le diverse edizioni sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="7a640-124">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="7a640-125">Base.</span><span class="sxs-lookup"><span data-stu-id="7a640-125">Basic.</span></span> <span data-ttu-id="7a640-126">5 DTU</span><span class="sxs-lookup"><span data-stu-id="7a640-126">5 DTUs</span></span>
- <span data-ttu-id="7a640-127">Standard.</span><span class="sxs-lookup"><span data-stu-id="7a640-127">Standard.</span></span> <span data-ttu-id="7a640-128">100 DTU</span><span class="sxs-lookup"><span data-stu-id="7a640-128">100 DTUs</span></span>
- <span data-ttu-id="7a640-129">Premium.</span><span class="sxs-lookup"><span data-stu-id="7a640-129">Premium.</span></span> <span data-ttu-id="7a640-130">125 DTU per informazioni dettagliate sui valori validi, vedere la tabella per il pool di dimensioni specifiche in [pool elastici](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="7a640-130">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span>

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

### <span data-ttu-id="7a640-131">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="7a640-131">-DatabaseDtuMin</span></span>
<span data-ttu-id="7a640-132">Specifica il numero minimo di DTU che il pool elastico garantisce a tutti i database nel pool.</span><span class="sxs-lookup"><span data-stu-id="7a640-132">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="7a640-133">Il valore predefinito è zero (0).</span><span class="sxs-lookup"><span data-stu-id="7a640-133">The default value is zero (0).</span></span>
<span data-ttu-id="7a640-134">Per informazioni dettagliate sui valori validi, vedere la tabella per il pool di dimensioni specifiche in [pool elastici](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="7a640-134">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="7a640-135">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="7a640-135">-DatabaseVCoreMax</span></span>
<span data-ttu-id="7a640-136">Il numero di Maxmium VCore qualsiasi database di sqlazure può essere utilizzato nel pool.</span><span class="sxs-lookup"><span data-stu-id="7a640-136">The maxmium VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="7a640-137">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="7a640-137">-DatabaseVCoreMin</span></span>
<span data-ttu-id="7a640-138">Il numero minimo di VCore qualsiasi database di sqlazure può essere utilizzato nel pool.</span><span class="sxs-lookup"><span data-stu-id="7a640-138">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="7a640-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a640-139">-DefaultProfile</span></span>
<span data-ttu-id="7a640-140">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7a640-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a640-141">-DTU</span><span class="sxs-lookup"><span data-stu-id="7a640-141">-Dtu</span></span>
<span data-ttu-id="7a640-142">Specifica il numero totale di DTU condivisi per il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="7a640-142">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="7a640-143">I valori predefiniti per le diverse edizioni sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="7a640-143">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="7a640-144">Base.</span><span class="sxs-lookup"><span data-stu-id="7a640-144">Basic.</span></span>
<span data-ttu-id="7a640-145">100 DTU</span><span class="sxs-lookup"><span data-stu-id="7a640-145">100 DTUs</span></span>
- <span data-ttu-id="7a640-146">Standard.</span><span class="sxs-lookup"><span data-stu-id="7a640-146">Standard.</span></span>
<span data-ttu-id="7a640-147">100 DTU</span><span class="sxs-lookup"><span data-stu-id="7a640-147">100 DTUs</span></span>
- <span data-ttu-id="7a640-148">Premium.</span><span class="sxs-lookup"><span data-stu-id="7a640-148">Premium.</span></span>
<span data-ttu-id="7a640-149">125 DTU per informazioni dettagliate sui valori validi, vedere la tabella per il pool di dimensioni specifiche in [pool elastici](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="7a640-149">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="7a640-150">-Edition</span><span class="sxs-lookup"><span data-stu-id="7a640-150">-Edition</span></span>
<span data-ttu-id="7a640-151">Specifica l'edizione del database SQL di Azure usato per il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="7a640-151">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="7a640-152">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="7a640-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7a640-153">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7a640-153">None</span></span>
- <span data-ttu-id="7a640-154">Base</span><span class="sxs-lookup"><span data-stu-id="7a640-154">Basic</span></span>
- <span data-ttu-id="7a640-155">Standard</span><span class="sxs-lookup"><span data-stu-id="7a640-155">Standard</span></span>
- <span data-ttu-id="7a640-156">Premium</span><span class="sxs-lookup"><span data-stu-id="7a640-156">Premium</span></span>
- <span data-ttu-id="7a640-157">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="7a640-157">DataWarehouse</span></span>
- <span data-ttu-id="7a640-158">Gratuito</span><span class="sxs-lookup"><span data-stu-id="7a640-158">Free</span></span>
- <span data-ttu-id="7a640-159">Tratto</span><span class="sxs-lookup"><span data-stu-id="7a640-159">Stretch</span></span>
- <span data-ttu-id="7a640-160">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="7a640-160">GeneralPurpose</span></span>
- <span data-ttu-id="7a640-161">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="7a640-161">BusinessCritical</span></span>

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

### <span data-ttu-id="7a640-162">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="7a640-162">-ElasticPoolName</span></span>
<span data-ttu-id="7a640-163">Specifica il nome del pool elastico creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a640-163">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="7a640-164">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="7a640-164">-LicenseType</span></span>
<span data-ttu-id="7a640-165">Tipo di licenza per il database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="7a640-165">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="7a640-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a640-166">-ResourceGroupName</span></span>
<span data-ttu-id="7a640-167">Specifica il nome del gruppo di risorse a cui questo cmdlet assegna il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="7a640-167">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="7a640-168">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="7a640-168">-ServerName</span></span>
<span data-ttu-id="7a640-169">Specifica il nome del server che ospita il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="7a640-169">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="7a640-170">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="7a640-170">-StorageMB</span></span>
<span data-ttu-id="7a640-171">Specifica il limite di archiviazione, in megabyte, per il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="7a640-171">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="7a640-172">Se non specifichi questo parametro, questo cmdlet calcola un valore che dipende dal valore del parametro *DTU* .</span><span class="sxs-lookup"><span data-stu-id="7a640-172">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>
<span data-ttu-id="7a640-173">Vedere [limiti di eDTU e archiviazione](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) per i valori possibili.</span><span class="sxs-lookup"><span data-stu-id="7a640-173">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

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

### <span data-ttu-id="7a640-174">-Tag</span><span class="sxs-lookup"><span data-stu-id="7a640-174">-Tags</span></span>
<span data-ttu-id="7a640-175">Specifica un dizionario di coppie chiave-valore in forma di tabella hash associata al pool elastico da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a640-175">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="7a640-176">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="7a640-176">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7a640-177">-VCore</span><span class="sxs-lookup"><span data-stu-id="7a640-177">-VCore</span></span>
<span data-ttu-id="7a640-178">Numero totale condiviso di Vcores per il pool elastico di SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="7a640-178">The total shared number of Vcores for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="7a640-179">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="7a640-179">-ZoneRedundant</span></span>
<span data-ttu-id="7a640-180">Ridondanza della zona da associare al pool di Azure SQL Elastic</span><span class="sxs-lookup"><span data-stu-id="7a640-180">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="7a640-181">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7a640-181">-Confirm</span></span>
<span data-ttu-id="7a640-182">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a640-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a640-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a640-183">-WhatIf</span></span>
<span data-ttu-id="7a640-184">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7a640-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a640-185">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7a640-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a640-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a640-186">CommonParameters</span></span>
<span data-ttu-id="7a640-187">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a640-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a640-188">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a640-188">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a640-189">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7a640-189">INPUTS</span></span>

### <span data-ttu-id="7a640-190">System. String</span><span class="sxs-lookup"><span data-stu-id="7a640-190">System.String</span></span>

## <span data-ttu-id="7a640-191">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7a640-191">OUTPUTS</span></span>

### <span data-ttu-id="7a640-192">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="7a640-192">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="7a640-193">Note</span><span class="sxs-lookup"><span data-stu-id="7a640-193">NOTES</span></span>

## <span data-ttu-id="7a640-194">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7a640-194">RELATED LINKS</span></span>

[<span data-ttu-id="7a640-195">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="7a640-195">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="7a640-196">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="7a640-196">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="7a640-197">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="7a640-197">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="7a640-198">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="7a640-198">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="7a640-199">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="7a640-199">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="7a640-200">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="7a640-200">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
