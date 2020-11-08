---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
ms.openlocfilehash: cb76e0ff789f89079772d7f718c3f16c9c01d707
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191834"
---
# <span data-ttu-id="8696a-101">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="8696a-101">Set-AzSqlElasticPool</span></span>

## <span data-ttu-id="8696a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8696a-102">SYNOPSIS</span></span>
<span data-ttu-id="8696a-103">Modifica le proprietà di un pool di database elastici in Azure SQL database.</span><span class="sxs-lookup"><span data-stu-id="8696a-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

## <span data-ttu-id="8696a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8696a-104">SYNTAX</span></span>

### <span data-ttu-id="8696a-105">DtuBasedPool (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8696a-105">DtuBasedPool (Default)</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8696a-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="8696a-106">VcoreBasedPool</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-StorageMB <Int32>] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8696a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8696a-107">DESCRIPTION</span></span>
<span data-ttu-id="8696a-108">Il cmdlet **set-AzSqlElasticPool** imposta le proprietà per un pool elastico in Azure SQL database.</span><span class="sxs-lookup"><span data-stu-id="8696a-108">The **Set-AzSqlElasticPool** cmdlet sets properties for an elastic pool in Azure SQL Database.</span></span> <span data-ttu-id="8696a-109">Questo cmdlet può modificare il eDTUs per pool ( *DTU* ), la dimensione massima dello spazio di archiviazione per pool ( *StorageMB* ), il eDTUs massimo per database ( *DatabaseDtuMax* ) e il minimo eDTUs per database ( *DatabaseDtuMin* ).</span><span class="sxs-lookup"><span data-stu-id="8696a-109">This cmdlet can modify the eDTUs per pool ( *Dtu* ), storage max size per pool ( *StorageMB* ), maximum eDTUs per database ( *DatabaseDtuMax* ), and minimum eDTUs per database ( *DatabaseDtuMin* ).</span></span>
<span data-ttu-id="8696a-110">Diversi parametri ( *-DTU,-DatabaseDtuMin e-DatabaseDtuMax* ) richiedono che il valore impostato sia dall'elenco di valori validi per il parametro.</span><span class="sxs-lookup"><span data-stu-id="8696a-110">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="8696a-111">Ad esempio,-DatabaseDtuMax per un pool di eDTU standard di 100 può essere impostato solo su 10, 20, 50 o 100.</span><span class="sxs-lookup"><span data-stu-id="8696a-111">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="8696a-112">Per informazioni dettagliate sui valori validi, vedere la tabella per il pool di dimensioni specifiche in [pool elastici](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="8696a-112">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="8696a-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8696a-113">EXAMPLES</span></span>

### <span data-ttu-id="8696a-114">Esempio 1: modificare le proprietà per un pool elastico</span><span class="sxs-lookup"><span data-stu-id="8696a-114">Example 1: Modify properties for an elastic pool</span></span>
```powershell
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

<span data-ttu-id="8696a-115">Questo comando modifica le proprietà di un pool elastico denominato elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="8696a-115">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="8696a-116">Il comando imposta il numero di DTU per il pool elastico su 1000 e imposta la DTU minima e massima.</span><span class="sxs-lookup"><span data-stu-id="8696a-116">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="8696a-117">Esempio 2: modificare le dimensioni massime dello spazio di archiviazione di un pool elastico</span><span class="sxs-lookup"><span data-stu-id="8696a-117">Example 2: Modify the storage max size of an elastic pool</span></span>
```powershell
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

<span data-ttu-id="8696a-118">Questo comando modifica le proprietà di un pool elastico denominato elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="8696a-118">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="8696a-119">Il comando imposta lo spazio di archiviazione max per un pool elastico su 2 TB.</span><span class="sxs-lookup"><span data-stu-id="8696a-119">The command sets the max storage for an elastic pool to 2 TB.</span></span>

### <span data-ttu-id="8696a-120">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="8696a-120">Example 3</span></span>

<span data-ttu-id="8696a-121">Modifica le proprietà di un pool di database elastici in Azure SQL database.</span><span class="sxs-lookup"><span data-stu-id="8696a-121">Modifies properties of an elastic database pool in Azure SQL Database.</span></span> <span data-ttu-id="8696a-122">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="8696a-122">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticPool -Dtu 1000 -Edition 'GeneralPurpose' -ElasticPoolName 'ElasticPool01' -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01'
```

## <span data-ttu-id="8696a-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8696a-123">PARAMETERS</span></span>

### <span data-ttu-id="8696a-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8696a-124">-AsJob</span></span>
<span data-ttu-id="8696a-125">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="8696a-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8696a-126">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="8696a-126">-ComputeGeneration</span></span>
<span data-ttu-id="8696a-127">Generazione di Compute da assegnare.</span><span class="sxs-lookup"><span data-stu-id="8696a-127">The compute generation to assign.</span></span>

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

### <span data-ttu-id="8696a-128">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="8696a-128">-DatabaseDtuMax</span></span>
<span data-ttu-id="8696a-129">Specifica il numero massimo di DTU che può essere utilizzato da qualsiasi singolo database nel pool.</span><span class="sxs-lookup"><span data-stu-id="8696a-129">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span>
<span data-ttu-id="8696a-130">Per informazioni dettagliate sui valori validi, vedere la tabella per il pool di dimensioni specifiche in [pool elastici](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="8696a-130">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="8696a-131">I valori predefiniti per le diverse edizioni sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="8696a-131">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="8696a-132">Base.</span><span class="sxs-lookup"><span data-stu-id="8696a-132">Basic.</span></span>  <span data-ttu-id="8696a-133">5 DTU</span><span class="sxs-lookup"><span data-stu-id="8696a-133">5 DTUs</span></span>
- <span data-ttu-id="8696a-134">Standard.</span><span class="sxs-lookup"><span data-stu-id="8696a-134">Standard.</span></span> <span data-ttu-id="8696a-135">100 DTU</span><span class="sxs-lookup"><span data-stu-id="8696a-135">100 DTUs</span></span>
- <span data-ttu-id="8696a-136">Premium.</span><span class="sxs-lookup"><span data-stu-id="8696a-136">Premium.</span></span> <span data-ttu-id="8696a-137">125 DTU</span><span class="sxs-lookup"><span data-stu-id="8696a-137">125 DTUs</span></span>

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

### <span data-ttu-id="8696a-138">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="8696a-138">-DatabaseDtuMin</span></span>
<span data-ttu-id="8696a-139">Specifica il numero minimo di DTU che il pool elastico garantisce a tutti i database nel pool.</span><span class="sxs-lookup"><span data-stu-id="8696a-139">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="8696a-140">Per informazioni dettagliate sui valori validi, vedere la tabella per il pool di dimensioni specifiche in [pool elastici](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="8696a-140">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="8696a-141">Il valore predefinito è zero (0).</span><span class="sxs-lookup"><span data-stu-id="8696a-141">The default value is zero (0).</span></span>

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

### <span data-ttu-id="8696a-142">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="8696a-142">-DatabaseVCoreMax</span></span>
<span data-ttu-id="8696a-143">Il numero massimo di VCore qualsiasi database di sqlazure può essere utilizzato nel pool.</span><span class="sxs-lookup"><span data-stu-id="8696a-143">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="8696a-144">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="8696a-144">-DatabaseVCoreMin</span></span>
<span data-ttu-id="8696a-145">Il numero minimo di VCore qualsiasi database di sqlazure può essere utilizzato nel pool.</span><span class="sxs-lookup"><span data-stu-id="8696a-145">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="8696a-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8696a-146">-DefaultProfile</span></span>
<span data-ttu-id="8696a-147">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8696a-147">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8696a-148">-DTU</span><span class="sxs-lookup"><span data-stu-id="8696a-148">-Dtu</span></span>
<span data-ttu-id="8696a-149">Specifica il numero totale di DTU condivisi per il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="8696a-149">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="8696a-150">Per informazioni dettagliate sui valori validi, vedere la tabella per il pool di dimensioni specifiche in [pool elastici](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="8696a-150">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="8696a-151">I valori predefiniti per le diverse edizioni sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="8696a-151">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="8696a-152">Base.</span><span class="sxs-lookup"><span data-stu-id="8696a-152">Basic.</span></span> <span data-ttu-id="8696a-153">100 DTU</span><span class="sxs-lookup"><span data-stu-id="8696a-153">100 DTUs</span></span>
- <span data-ttu-id="8696a-154">Standard.</span><span class="sxs-lookup"><span data-stu-id="8696a-154">Standard.</span></span> <span data-ttu-id="8696a-155">100 DTU</span><span class="sxs-lookup"><span data-stu-id="8696a-155">100 DTUs</span></span>
- <span data-ttu-id="8696a-156">Premium.</span><span class="sxs-lookup"><span data-stu-id="8696a-156">Premium.</span></span> <span data-ttu-id="8696a-157">125 DTU</span><span class="sxs-lookup"><span data-stu-id="8696a-157">125 DTUs</span></span>

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

### <span data-ttu-id="8696a-158">-Edition</span><span class="sxs-lookup"><span data-stu-id="8696a-158">-Edition</span></span>
<span data-ttu-id="8696a-159">Specifica l'edizione del database SQL di Azure per il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="8696a-159">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="8696a-160">Non è possibile modificare l'edizione.</span><span class="sxs-lookup"><span data-stu-id="8696a-160">You cannot change the edition.</span></span> <span data-ttu-id="8696a-161">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="8696a-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8696a-162">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8696a-162">None</span></span>
- <span data-ttu-id="8696a-163">Base</span><span class="sxs-lookup"><span data-stu-id="8696a-163">Basic</span></span>
- <span data-ttu-id="8696a-164">Standard</span><span class="sxs-lookup"><span data-stu-id="8696a-164">Standard</span></span>
- <span data-ttu-id="8696a-165">Premium</span><span class="sxs-lookup"><span data-stu-id="8696a-165">Premium</span></span>
- <span data-ttu-id="8696a-166">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="8696a-166">DataWarehouse</span></span>
- <span data-ttu-id="8696a-167">Gratuito</span><span class="sxs-lookup"><span data-stu-id="8696a-167">Free</span></span>
- <span data-ttu-id="8696a-168">Tratto</span><span class="sxs-lookup"><span data-stu-id="8696a-168">Stretch</span></span>
- <span data-ttu-id="8696a-169">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="8696a-169">GeneralPurpose</span></span>
- <span data-ttu-id="8696a-170">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="8696a-170">BusinessCritical</span></span>

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

### <span data-ttu-id="8696a-171">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="8696a-171">-ElasticPoolName</span></span>
<span data-ttu-id="8696a-172">Specifica il nome del pool elastico.</span><span class="sxs-lookup"><span data-stu-id="8696a-172">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="8696a-173">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="8696a-173">-LicenseType</span></span>
<span data-ttu-id="8696a-174">Tipo di licenza per il database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="8696a-174">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="8696a-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8696a-175">-ResourceGroupName</span></span>
<span data-ttu-id="8696a-176">Specifica il nome del gruppo di risorse a cui è assegnato il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="8696a-176">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="8696a-177">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="8696a-177">-ServerName</span></span>
<span data-ttu-id="8696a-178">Specifica il nome del server che ospita il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="8696a-178">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="8696a-179">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="8696a-179">-StorageMB</span></span>
<span data-ttu-id="8696a-180">Specifica il limite di archiviazione, in megabyte, per il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="8696a-180">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="8696a-181">Per altre informazioni, vedere il cmdlet New-AzSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="8696a-181">For more information, see the New-AzSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="8696a-182">-Tag</span><span class="sxs-lookup"><span data-stu-id="8696a-182">-Tags</span></span>
<span data-ttu-id="8696a-183">Specifica un dizionario di coppie chiave-valore che questo cmdlet associa al pool elastico in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="8696a-183">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="8696a-184">Per esempio: `@{key0="value0";"key 1"=$null;key2="value2"}`</span><span class="sxs-lookup"><span data-stu-id="8696a-184">For example: `@{key0="value0";"key 1"=$null;key2="value2"}`</span></span>

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

### <span data-ttu-id="8696a-185">-VCore</span><span class="sxs-lookup"><span data-stu-id="8696a-185">-VCore</span></span>
<span data-ttu-id="8696a-186">Numero totale condiviso di Vcore per il pool elastico di SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="8696a-186">The total shared number of Vcore for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="8696a-187">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="8696a-187">-ZoneRedundant</span></span>
<span data-ttu-id="8696a-188">Ridondanza della zona da associare al pool di Azure SQL Elastic</span><span class="sxs-lookup"><span data-stu-id="8696a-188">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="8696a-189">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8696a-189">-Confirm</span></span>
<span data-ttu-id="8696a-190">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8696a-190">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8696a-191">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8696a-191">-WhatIf</span></span>
<span data-ttu-id="8696a-192">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8696a-192">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8696a-193">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8696a-193">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8696a-194">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8696a-194">CommonParameters</span></span>
<span data-ttu-id="8696a-195">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8696a-195">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8696a-196">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8696a-196">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8696a-197">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8696a-197">INPUTS</span></span>

### <span data-ttu-id="8696a-198">System. String</span><span class="sxs-lookup"><span data-stu-id="8696a-198">System.String</span></span>

## <span data-ttu-id="8696a-199">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8696a-199">OUTPUTS</span></span>

### <span data-ttu-id="8696a-200">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="8696a-200">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="8696a-201">Note</span><span class="sxs-lookup"><span data-stu-id="8696a-201">NOTES</span></span>

## <span data-ttu-id="8696a-202">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8696a-202">RELATED LINKS</span></span>

[<span data-ttu-id="8696a-203">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="8696a-203">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="8696a-204">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="8696a-204">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="8696a-205">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="8696a-205">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="8696a-206">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="8696a-206">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="8696a-207">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="8696a-207">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
