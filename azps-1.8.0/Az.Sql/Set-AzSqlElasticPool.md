---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
ms.openlocfilehash: 3f90358bcf7109690940b8627a02b6b602353fb2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676736"
---
# <span data-ttu-id="144ce-101">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="144ce-101">Set-AzSqlElasticPool</span></span>

## <span data-ttu-id="144ce-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="144ce-102">SYNOPSIS</span></span>
<span data-ttu-id="144ce-103">Modifica le proprietà di un pool di database elastici in Azure SQL database.</span><span class="sxs-lookup"><span data-stu-id="144ce-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

## <span data-ttu-id="144ce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="144ce-104">SYNTAX</span></span>

### <span data-ttu-id="144ce-105">DtuBasedPool (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="144ce-105">DtuBasedPool (Default)</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="144ce-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="144ce-106">VcoreBasedPool</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-StorageMB <Int32>] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="144ce-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="144ce-107">DESCRIPTION</span></span>
<span data-ttu-id="144ce-108">Il cmdlet **set-AzSqlElasticPool** imposta le proprietà per un pool elastico in Azure SQL database.</span><span class="sxs-lookup"><span data-stu-id="144ce-108">The **Set-AzSqlElasticPool** cmdlet sets properties for an elastic pool in Azure SQL Database.</span></span> <span data-ttu-id="144ce-109">Questo cmdlet può modificare il eDTUs per pool ( *DTU* ), la dimensione massima dello spazio di archiviazione per pool ( *StorageMB* ), il eDTUs massimo per database ( *DatabaseDtuMax* ) e il minimo eDTUs per database ( *DatqabaseDtuMin* ).</span><span class="sxs-lookup"><span data-stu-id="144ce-109">This cmdlet can modify the eDTUs per pool ( *Dtu* ), storage max size per pool ( *StorageMB* ), maximum eDTUs per database ( *DatabaseDtuMax* ), and minimum eDTUs per database ( *DatqabaseDtuMin* ).</span></span>
<span data-ttu-id="144ce-110">Diversi parametri ( *-DTU,-DatabaseDtuMin e-DatabaseDtuMax* ) richiedono che il valore impostato sia dall'elenco di valori validi per il parametro.</span><span class="sxs-lookup"><span data-stu-id="144ce-110">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="144ce-111">Ad esempio,-DatabaseDtuMax per un pool di eDTU standard di 100 può essere impostato solo su 10, 20, 50 o 100.</span><span class="sxs-lookup"><span data-stu-id="144ce-111">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="144ce-112">Per informazioni dettagliate sui valori validi, vedere la tabella per il pool di dimensioni specifiche in [pool elastici](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="144ce-112">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="144ce-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="144ce-113">EXAMPLES</span></span>

### <span data-ttu-id="144ce-114">Esempio 1: modificare le proprietà per un pool elastico</span><span class="sxs-lookup"><span data-stu-id="144ce-114">Example 1: Modify properties for an elastic pool</span></span>
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

<span data-ttu-id="144ce-115">Questo comando modifica le proprietà di un pool elastico denominato elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="144ce-115">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="144ce-116">Il comando imposta il numero di DTU per il pool elastico su 1000 e imposta la DTU minima e massima.</span><span class="sxs-lookup"><span data-stu-id="144ce-116">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="144ce-117">Esempio 2: modificare le dimensioni massime dello spazio di archiviazione di un pool elastico</span><span class="sxs-lookup"><span data-stu-id="144ce-117">Example 2: Modify the storage max size of an elastic pool</span></span>
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

<span data-ttu-id="144ce-118">Questo comando modifica le proprietà di un pool elastico denominato elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="144ce-118">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="144ce-119">Il comando imposta lo spazio di archiviazione max per un pool elastico su 2 TB.</span><span class="sxs-lookup"><span data-stu-id="144ce-119">The command sets the max storage for an elastic pool to 2 TB.</span></span>

## <span data-ttu-id="144ce-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="144ce-120">PARAMETERS</span></span>

### <span data-ttu-id="144ce-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="144ce-121">-AsJob</span></span>
<span data-ttu-id="144ce-122">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="144ce-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="144ce-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="144ce-123">-ComputeGeneration</span></span>
<span data-ttu-id="144ce-124">Generazione di Compute da assegnare.</span><span class="sxs-lookup"><span data-stu-id="144ce-124">The compute generation to assign.</span></span>

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

### <span data-ttu-id="144ce-125">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="144ce-125">-DatabaseDtuMax</span></span>
<span data-ttu-id="144ce-126">Specifica il numero massimo di DTU che può essere utilizzato da qualsiasi singolo database nel pool.</span><span class="sxs-lookup"><span data-stu-id="144ce-126">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span>
<span data-ttu-id="144ce-127">Per informazioni dettagliate sui valori validi, vedere la tabella per il pool di dimensioni specifiche in [pool elastici](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="144ce-127">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="144ce-128">I valori predefiniti per le diverse edizioni sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="144ce-128">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="144ce-129">Base.</span><span class="sxs-lookup"><span data-stu-id="144ce-129">Basic.</span></span>  <span data-ttu-id="144ce-130">5 DTU</span><span class="sxs-lookup"><span data-stu-id="144ce-130">5 DTUs</span></span>
- <span data-ttu-id="144ce-131">Standard.</span><span class="sxs-lookup"><span data-stu-id="144ce-131">Standard.</span></span> <span data-ttu-id="144ce-132">100 DTU</span><span class="sxs-lookup"><span data-stu-id="144ce-132">100 DTUs</span></span>
- <span data-ttu-id="144ce-133">Premium.</span><span class="sxs-lookup"><span data-stu-id="144ce-133">Premium.</span></span> <span data-ttu-id="144ce-134">125 DTU</span><span class="sxs-lookup"><span data-stu-id="144ce-134">125 DTUs</span></span>

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

### <span data-ttu-id="144ce-135">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="144ce-135">-DatabaseDtuMin</span></span>
<span data-ttu-id="144ce-136">Specifica il numero minimo di DTU che il pool elastico garantisce a tutti i database nel pool.</span><span class="sxs-lookup"><span data-stu-id="144ce-136">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="144ce-137">Per informazioni dettagliate sui valori validi, vedere la tabella per il pool di dimensioni specifiche in [pool elastici](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="144ce-137">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="144ce-138">Il valore predefinito è zero (0).</span><span class="sxs-lookup"><span data-stu-id="144ce-138">The default value is zero (0).</span></span>

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

### <span data-ttu-id="144ce-139">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="144ce-139">-DatabaseVCoreMax</span></span>
<span data-ttu-id="144ce-140">Il numero di Maxmium VCore qualsiasi database di sqlazure può essere utilizzato nel pool.</span><span class="sxs-lookup"><span data-stu-id="144ce-140">The maxmium VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="144ce-141">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="144ce-141">-DatabaseVCoreMin</span></span>
<span data-ttu-id="144ce-142">Il numero minimo di VCore qualsiasi database di sqlazure può essere utilizzato nel pool.</span><span class="sxs-lookup"><span data-stu-id="144ce-142">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="144ce-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="144ce-143">-DefaultProfile</span></span>
<span data-ttu-id="144ce-144">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="144ce-144">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="144ce-145">-DTU</span><span class="sxs-lookup"><span data-stu-id="144ce-145">-Dtu</span></span>
<span data-ttu-id="144ce-146">Specifica il numero totale di DTU condivisi per il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="144ce-146">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="144ce-147">Per informazioni dettagliate sui valori validi, vedere la tabella per il pool di dimensioni specifiche in [pool elastici](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="144ce-147">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="144ce-148">I valori predefiniti per le diverse edizioni sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="144ce-148">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="144ce-149">Base.</span><span class="sxs-lookup"><span data-stu-id="144ce-149">Basic.</span></span> <span data-ttu-id="144ce-150">100 DTU</span><span class="sxs-lookup"><span data-stu-id="144ce-150">100 DTUs</span></span>
- <span data-ttu-id="144ce-151">Standard.</span><span class="sxs-lookup"><span data-stu-id="144ce-151">Standard.</span></span> <span data-ttu-id="144ce-152">100 DTU</span><span class="sxs-lookup"><span data-stu-id="144ce-152">100 DTUs</span></span>
- <span data-ttu-id="144ce-153">Premium.</span><span class="sxs-lookup"><span data-stu-id="144ce-153">Premium.</span></span> <span data-ttu-id="144ce-154">125 DTU</span><span class="sxs-lookup"><span data-stu-id="144ce-154">125 DTUs</span></span>

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

### <span data-ttu-id="144ce-155">-Edition</span><span class="sxs-lookup"><span data-stu-id="144ce-155">-Edition</span></span>
<span data-ttu-id="144ce-156">Specifica l'edizione del database SQL di Azure per il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="144ce-156">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="144ce-157">Non è possibile modificare l'edizione.</span><span class="sxs-lookup"><span data-stu-id="144ce-157">You cannot change the edition.</span></span> <span data-ttu-id="144ce-158">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="144ce-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="144ce-159">Nessuno</span><span class="sxs-lookup"><span data-stu-id="144ce-159">None</span></span>
- <span data-ttu-id="144ce-160">Base</span><span class="sxs-lookup"><span data-stu-id="144ce-160">Basic</span></span>
- <span data-ttu-id="144ce-161">Standard</span><span class="sxs-lookup"><span data-stu-id="144ce-161">Standard</span></span>
- <span data-ttu-id="144ce-162">Premium</span><span class="sxs-lookup"><span data-stu-id="144ce-162">Premium</span></span>
- <span data-ttu-id="144ce-163">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="144ce-163">DataWarehouse</span></span>
- <span data-ttu-id="144ce-164">Gratuito</span><span class="sxs-lookup"><span data-stu-id="144ce-164">Free</span></span>
- <span data-ttu-id="144ce-165">Tratto</span><span class="sxs-lookup"><span data-stu-id="144ce-165">Stretch</span></span>
- <span data-ttu-id="144ce-166">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="144ce-166">GeneralPurpose</span></span>
- <span data-ttu-id="144ce-167">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="144ce-167">BusinessCritical</span></span>

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

### <span data-ttu-id="144ce-168">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="144ce-168">-ElasticPoolName</span></span>
<span data-ttu-id="144ce-169">Specifica il nome del pool elastico.</span><span class="sxs-lookup"><span data-stu-id="144ce-169">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="144ce-170">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="144ce-170">-LicenseType</span></span>
<span data-ttu-id="144ce-171">Tipo di licenza per il database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="144ce-171">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="144ce-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="144ce-172">-ResourceGroupName</span></span>
<span data-ttu-id="144ce-173">Specifica il nome del gruppo di risorse a cui è assegnato il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="144ce-173">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="144ce-174">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="144ce-174">-ServerName</span></span>
<span data-ttu-id="144ce-175">Specifica il nome del server che ospita il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="144ce-175">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="144ce-176">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="144ce-176">-StorageMB</span></span>
<span data-ttu-id="144ce-177">Specifica il limite di archiviazione, in megabyte, per il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="144ce-177">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="144ce-178">Per altre informazioni, vedere il cmdlet New-AzSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="144ce-178">For more information, see the New-AzSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="144ce-179">-Tag</span><span class="sxs-lookup"><span data-stu-id="144ce-179">-Tags</span></span>
<span data-ttu-id="144ce-180">Specifica un dizionario di coppie chiave-valore che questo cmdlet associa al pool elastico in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="144ce-180">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="144ce-181">Per esempio: `@{key0="value0";"key 1"=$null;key2="value2"}`</span><span class="sxs-lookup"><span data-stu-id="144ce-181">For example: `@{key0="value0";"key 1"=$null;key2="value2"}`</span></span>

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

### <span data-ttu-id="144ce-182">-VCore</span><span class="sxs-lookup"><span data-stu-id="144ce-182">-VCore</span></span>
<span data-ttu-id="144ce-183">Numero totale condiviso di Vcore per il pool elastico di SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="144ce-183">The total shared number of Vcore for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="144ce-184">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="144ce-184">-ZoneRedundant</span></span>
<span data-ttu-id="144ce-185">Ridondanza della zona da associare al pool di Azure SQL Elastic</span><span class="sxs-lookup"><span data-stu-id="144ce-185">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="144ce-186">-Confermare</span><span class="sxs-lookup"><span data-stu-id="144ce-186">-Confirm</span></span>
<span data-ttu-id="144ce-187">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="144ce-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="144ce-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="144ce-188">-WhatIf</span></span>
<span data-ttu-id="144ce-189">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="144ce-189">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="144ce-190">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="144ce-190">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="144ce-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="144ce-191">CommonParameters</span></span>
<span data-ttu-id="144ce-192">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="144ce-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="144ce-193">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="144ce-193">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="144ce-194">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="144ce-194">INPUTS</span></span>

### <span data-ttu-id="144ce-195">System. String</span><span class="sxs-lookup"><span data-stu-id="144ce-195">System.String</span></span>

## <span data-ttu-id="144ce-196">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="144ce-196">OUTPUTS</span></span>

### <span data-ttu-id="144ce-197">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="144ce-197">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="144ce-198">Note</span><span class="sxs-lookup"><span data-stu-id="144ce-198">NOTES</span></span>

## <span data-ttu-id="144ce-199">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="144ce-199">RELATED LINKS</span></span>

[<span data-ttu-id="144ce-200">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="144ce-200">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="144ce-201">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="144ce-201">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="144ce-202">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="144ce-202">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="144ce-203">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="144ce-203">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="144ce-204">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="144ce-204">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
