---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
ms.openlocfilehash: d78ca6ef2e342982dc6f5e53e8fff4de606dd5ab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857122"
---
# <span data-ttu-id="0bee1-101">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="0bee1-101">Set-AzSqlElasticPool</span></span>

## <span data-ttu-id="0bee1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0bee1-102">SYNOPSIS</span></span>
<span data-ttu-id="0bee1-103">Modifica le proprietà di un pool di database elastici in Azure SQL database.</span><span class="sxs-lookup"><span data-stu-id="0bee1-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

## <span data-ttu-id="0bee1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0bee1-104">SYNTAX</span></span>

### <span data-ttu-id="0bee1-105">DtuBasedPool (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0bee1-105">DtuBasedPool (Default)</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0bee1-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="0bee1-106">VcoreBasedPool</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-StorageMB <Int32>] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0bee1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0bee1-107">DESCRIPTION</span></span>
<span data-ttu-id="0bee1-108">Il cmdlet **set-AzSqlElasticPool** imposta le proprietà per un pool elastico in Azure SQL database.</span><span class="sxs-lookup"><span data-stu-id="0bee1-108">The **Set-AzSqlElasticPool** cmdlet sets properties for an elastic pool in Azure SQL Database.</span></span> <span data-ttu-id="0bee1-109">Questo cmdlet può modificare il eDTUs per pool ( *DTU* ), la dimensione massima dello spazio di archiviazione per pool ( *StorageMB* ), il eDTUs massimo per database ( *DatabaseDtuMax* ) e il minimo eDTUs per database ( *DatabaseDtuMin* ).</span><span class="sxs-lookup"><span data-stu-id="0bee1-109">This cmdlet can modify the eDTUs per pool ( *Dtu* ), storage max size per pool ( *StorageMB* ), maximum eDTUs per database ( *DatabaseDtuMax* ), and minimum eDTUs per database ( *DatabaseDtuMin* ).</span></span>
<span data-ttu-id="0bee1-110">Diversi parametri ( *-DTU,-DatabaseDtuMin e-DatabaseDtuMax* ) richiedono che il valore impostato sia dall'elenco di valori validi per il parametro.</span><span class="sxs-lookup"><span data-stu-id="0bee1-110">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="0bee1-111">Ad esempio,-DatabaseDtuMax per un pool di eDTU standard di 100 può essere impostato solo su 10, 20, 50 o 100.</span><span class="sxs-lookup"><span data-stu-id="0bee1-111">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="0bee1-112">Per informazioni dettagliate sui valori validi, vedere la tabella per il pool di dimensioni specifiche in [pool elastici](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="0bee1-112">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="0bee1-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0bee1-113">EXAMPLES</span></span>

### <span data-ttu-id="0bee1-114">Esempio 1: modificare le proprietà per un pool elastico</span><span class="sxs-lookup"><span data-stu-id="0bee1-114">Example 1: Modify properties for an elastic pool</span></span>
```
PS C:\>Set-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Dtu 1000 -DatabaseDtuMax 100 -DatabaseDtuMin 20
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/Server01/elasticPools/ElasticPool01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
ElasticPoolName   : ElasticPool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 200
DatabaseDtuMax    : 100
DatabaseDtuMin    : 20
StorageMB         : 204800
Tags              :
```

<span data-ttu-id="0bee1-115">Questo comando modifica le proprietà di un pool elastico denominato elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="0bee1-115">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="0bee1-116">Il comando imposta il numero di DTU per il pool elastico su 1000 e imposta la DTU minima e massima.</span><span class="sxs-lookup"><span data-stu-id="0bee1-116">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="0bee1-117">Esempio 2: modificare le dimensioni massime dello spazio di archiviazione di un pool elastico</span><span class="sxs-lookup"><span data-stu-id="0bee1-117">Example 2: Modify the storage max size of an elastic pool</span></span>
```
PS C:\>Set-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -StorageMB 2097152
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/Server01/elasticPools/ElasticPool01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
ElasticPoolName   : ElasticPool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Premium
Dtu               : 200
DatabaseDtuMax    : 100
DatabaseDtuMin    : 20
StorageMB         : 2097152
Tags              :
```

<span data-ttu-id="0bee1-118">Questo comando modifica le proprietà di un pool elastico denominato elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="0bee1-118">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="0bee1-119">Il comando imposta lo spazio di archiviazione max per un pool elastico su 2 TB.</span><span class="sxs-lookup"><span data-stu-id="0bee1-119">The command sets the max storage for an elastic pool to 2 TB.</span></span>

## <span data-ttu-id="0bee1-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0bee1-120">PARAMETERS</span></span>

### <span data-ttu-id="0bee1-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0bee1-121">-AsJob</span></span>
<span data-ttu-id="0bee1-122">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="0bee1-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0bee1-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="0bee1-123">-ComputeGeneration</span></span>
<span data-ttu-id="0bee1-124">Generazione di Compute da assegnare.</span><span class="sxs-lookup"><span data-stu-id="0bee1-124">The compute generation to assign.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedPool
Aliases: Family

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bee1-125">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="0bee1-125">-DatabaseDtuMax</span></span>
<span data-ttu-id="0bee1-126">Specifica il numero massimo di DTU che può essere utilizzato da qualsiasi singolo database nel pool.</span><span class="sxs-lookup"><span data-stu-id="0bee1-126">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span>
<span data-ttu-id="0bee1-127">Per informazioni dettagliate sui valori validi, vedere la tabella per il pool di dimensioni specifiche in [pool elastici](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="0bee1-127">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="0bee1-128">I valori predefiniti per le diverse edizioni sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="0bee1-128">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="0bee1-129">Base.</span><span class="sxs-lookup"><span data-stu-id="0bee1-129">Basic.</span></span>  <span data-ttu-id="0bee1-130">5 DTU</span><span class="sxs-lookup"><span data-stu-id="0bee1-130">5 DTUs</span></span>
- <span data-ttu-id="0bee1-131">Standard.</span><span class="sxs-lookup"><span data-stu-id="0bee1-131">Standard.</span></span> <span data-ttu-id="0bee1-132">100 DTU</span><span class="sxs-lookup"><span data-stu-id="0bee1-132">100 DTUs</span></span>
- <span data-ttu-id="0bee1-133">Premium.</span><span class="sxs-lookup"><span data-stu-id="0bee1-133">Premium.</span></span> <span data-ttu-id="0bee1-134">125 DTU</span><span class="sxs-lookup"><span data-stu-id="0bee1-134">125 DTUs</span></span>

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

### <span data-ttu-id="0bee1-135">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="0bee1-135">-DatabaseDtuMin</span></span>
<span data-ttu-id="0bee1-136">Specifica il numero minimo di DTU che il pool elastico garantisce a tutti i database nel pool.</span><span class="sxs-lookup"><span data-stu-id="0bee1-136">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="0bee1-137">Per informazioni dettagliate sui valori validi, vedere la tabella per il pool di dimensioni specifiche in [pool elastici](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="0bee1-137">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="0bee1-138">Il valore predefinito è zero (0).</span><span class="sxs-lookup"><span data-stu-id="0bee1-138">The default value is zero (0).</span></span>

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

### <span data-ttu-id="0bee1-139">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="0bee1-139">-DatabaseVCoreMax</span></span>
<span data-ttu-id="0bee1-140">Il numero massimo di VCore qualsiasi database di sqlazure può essere utilizzato nel pool.</span><span class="sxs-lookup"><span data-stu-id="0bee1-140">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="0bee1-141">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="0bee1-141">-DatabaseVCoreMin</span></span>
<span data-ttu-id="0bee1-142">Il numero minimo di VCore qualsiasi database di sqlazure può essere utilizzato nel pool.</span><span class="sxs-lookup"><span data-stu-id="0bee1-142">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="0bee1-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bee1-143">-DefaultProfile</span></span>
<span data-ttu-id="0bee1-144">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0bee1-144">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0bee1-145">-DTU</span><span class="sxs-lookup"><span data-stu-id="0bee1-145">-Dtu</span></span>
<span data-ttu-id="0bee1-146">Specifica il numero totale di DTU condivisi per il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="0bee1-146">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="0bee1-147">Per informazioni dettagliate sui valori validi, vedere la tabella per il pool di dimensioni specifiche in [pool elastici](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="0bee1-147">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="0bee1-148">I valori predefiniti per le diverse edizioni sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="0bee1-148">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="0bee1-149">Base.</span><span class="sxs-lookup"><span data-stu-id="0bee1-149">Basic.</span></span> <span data-ttu-id="0bee1-150">100 DTU</span><span class="sxs-lookup"><span data-stu-id="0bee1-150">100 DTUs</span></span>
- <span data-ttu-id="0bee1-151">Standard.</span><span class="sxs-lookup"><span data-stu-id="0bee1-151">Standard.</span></span> <span data-ttu-id="0bee1-152">100 DTU</span><span class="sxs-lookup"><span data-stu-id="0bee1-152">100 DTUs</span></span>
- <span data-ttu-id="0bee1-153">Premium.</span><span class="sxs-lookup"><span data-stu-id="0bee1-153">Premium.</span></span> <span data-ttu-id="0bee1-154">125 DTU</span><span class="sxs-lookup"><span data-stu-id="0bee1-154">125 DTUs</span></span>

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

### <span data-ttu-id="0bee1-155">-Edition</span><span class="sxs-lookup"><span data-stu-id="0bee1-155">-Edition</span></span>
<span data-ttu-id="0bee1-156">Specifica l'edizione del database SQL di Azure per il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="0bee1-156">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="0bee1-157">Non è possibile modificare l'edizione.</span><span class="sxs-lookup"><span data-stu-id="0bee1-157">You cannot change the edition.</span></span> <span data-ttu-id="0bee1-158">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="0bee1-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0bee1-159">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0bee1-159">None</span></span>
- <span data-ttu-id="0bee1-160">Base</span><span class="sxs-lookup"><span data-stu-id="0bee1-160">Basic</span></span>
- <span data-ttu-id="0bee1-161">Standard</span><span class="sxs-lookup"><span data-stu-id="0bee1-161">Standard</span></span>
- <span data-ttu-id="0bee1-162">Premium</span><span class="sxs-lookup"><span data-stu-id="0bee1-162">Premium</span></span>
- <span data-ttu-id="0bee1-163">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="0bee1-163">DataWarehouse</span></span>
- <span data-ttu-id="0bee1-164">Gratuito</span><span class="sxs-lookup"><span data-stu-id="0bee1-164">Free</span></span>
- <span data-ttu-id="0bee1-165">Tratto</span><span class="sxs-lookup"><span data-stu-id="0bee1-165">Stretch</span></span>
- <span data-ttu-id="0bee1-166">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="0bee1-166">GeneralPurpose</span></span>
- <span data-ttu-id="0bee1-167">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="0bee1-167">BusinessCritical</span></span>

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

### <span data-ttu-id="0bee1-168">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="0bee1-168">-ElasticPoolName</span></span>
<span data-ttu-id="0bee1-169">Specifica il nome del pool elastico.</span><span class="sxs-lookup"><span data-stu-id="0bee1-169">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="0bee1-170">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="0bee1-170">-LicenseType</span></span>
<span data-ttu-id="0bee1-171">Tipo di licenza per il database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="0bee1-171">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="0bee1-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bee1-172">-ResourceGroupName</span></span>
<span data-ttu-id="0bee1-173">Specifica il nome del gruppo di risorse a cui è assegnato il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="0bee1-173">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="0bee1-174">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="0bee1-174">-ServerName</span></span>
<span data-ttu-id="0bee1-175">Specifica il nome del server che ospita il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="0bee1-175">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="0bee1-176">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="0bee1-176">-StorageMB</span></span>
<span data-ttu-id="0bee1-177">Specifica il limite di archiviazione, in megabyte, per il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="0bee1-177">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="0bee1-178">Per altre informazioni, vedere il cmdlet New-AzSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="0bee1-178">For more information, see the New-AzSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="0bee1-179">-Tag</span><span class="sxs-lookup"><span data-stu-id="0bee1-179">-Tags</span></span>
<span data-ttu-id="0bee1-180">Specifica un dizionario di coppie chiave-valore che questo cmdlet associa al pool elastico in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="0bee1-180">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="0bee1-181">Per esempio: `@{key0="value0";"key 1"=$null;key2="value2"}`</span><span class="sxs-lookup"><span data-stu-id="0bee1-181">For example: `@{key0="value0";"key 1"=$null;key2="value2"}`</span></span>

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

### <span data-ttu-id="0bee1-182">-VCore</span><span class="sxs-lookup"><span data-stu-id="0bee1-182">-VCore</span></span>
<span data-ttu-id="0bee1-183">Numero totale condiviso di Vcore per il pool elastico di SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="0bee1-183">The total shared number of Vcore for the Sql Azure Elastic Pool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bee1-184">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="0bee1-184">-ZoneRedundant</span></span>
<span data-ttu-id="0bee1-185">Ridondanza della zona da associare al pool di Azure SQL Elastic</span><span class="sxs-lookup"><span data-stu-id="0bee1-185">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="0bee1-186">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0bee1-186">-Confirm</span></span>
<span data-ttu-id="0bee1-187">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0bee1-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bee1-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bee1-188">-WhatIf</span></span>
<span data-ttu-id="0bee1-189">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0bee1-189">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0bee1-190">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0bee1-190">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bee1-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bee1-191">CommonParameters</span></span>
<span data-ttu-id="0bee1-192">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bee1-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bee1-193">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0bee1-193">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bee1-194">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0bee1-194">INPUTS</span></span>

### <span data-ttu-id="0bee1-195">System. String</span><span class="sxs-lookup"><span data-stu-id="0bee1-195">System.String</span></span>

## <span data-ttu-id="0bee1-196">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0bee1-196">OUTPUTS</span></span>

### <span data-ttu-id="0bee1-197">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="0bee1-197">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="0bee1-198">Note</span><span class="sxs-lookup"><span data-stu-id="0bee1-198">NOTES</span></span>

## <span data-ttu-id="0bee1-199">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0bee1-199">RELATED LINKS</span></span>

[<span data-ttu-id="0bee1-200">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="0bee1-200">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="0bee1-201">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="0bee1-201">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="0bee1-202">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="0bee1-202">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="0bee1-203">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="0bee1-203">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="0bee1-204">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="0bee1-204">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
