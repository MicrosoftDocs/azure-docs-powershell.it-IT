---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
ms.openlocfilehash: a420a7edf1d5fb7133087c5ecb9fcf605cbdddf9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176758"
---
# <span data-ttu-id="47449-101">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="47449-101">Set-AzSqlElasticPool</span></span>

## <span data-ttu-id="47449-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47449-102">SYNOPSIS</span></span>
<span data-ttu-id="47449-103">Modifica le proprietà di un pool di database flessibile in Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="47449-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

## <span data-ttu-id="47449-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="47449-104">SYNTAX</span></span>

### <span data-ttu-id="47449-105">DtuBasedPool (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="47449-105">DtuBasedPool (Default)</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-MaintenanceConfigurationId <String>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="47449-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="47449-106">VcoreBasedPool</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-StorageMB <Int32>] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-MaintenanceConfigurationId <String>] [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47449-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="47449-107">DESCRIPTION</span></span>
<span data-ttu-id="47449-108">Il cmdlet **Set-AzSqlElasticPool** imposta le proprietà per un pool elastico in Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="47449-108">The **Set-AzSqlElasticPool** cmdlet sets properties for an elastic pool in Azure SQL Database.</span></span> <span data-ttu-id="47449-109">Questo cmdlet può modificare gli eDTUs per pool (*Dtu*), le dimensioni massime di archiviazione per pool (*StorageMB*), gli eDTUs massimi per database (*DatabaseDtuMax*) e gli eDTUs minimi per database (*DatabaseDtuMin*).</span><span class="sxs-lookup"><span data-stu-id="47449-109">This cmdlet can modify the eDTUs per pool (*Dtu*), storage max size per pool (*StorageMB*), maximum eDTUs per database (*DatabaseDtuMax*), and minimum eDTUs per database (*DatabaseDtuMin*).</span></span>
<span data-ttu-id="47449-110">Diversi parametri (*-Dtu, -DatabaseDtuMin e -DatabaseDtuMax*) richiedono che il valore impostato sia in un elenco di valori validi per il parametro.</span><span class="sxs-lookup"><span data-stu-id="47449-110">Several parameters (*-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax*) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="47449-111">Ad esempio, -DatabaseDtuMax per un pool eDTU Standard 100 può essere impostato solo su 10, 20, 50 o 100.</span><span class="sxs-lookup"><span data-stu-id="47449-111">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="47449-112">Per informazioni dettagliate sui valori validi, vedere la tabella per il pool di dimensioni specifico in [pool di elastici.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="47449-112">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="47449-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="47449-113">EXAMPLES</span></span>

### <span data-ttu-id="47449-114">Esempio 1: Modificare le proprietà per un pool flessibile</span><span class="sxs-lookup"><span data-stu-id="47449-114">Example 1: Modify properties for an elastic pool</span></span>
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

<span data-ttu-id="47449-115">Questo comando modifica le proprietà per un pool elastico denominato elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="47449-115">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="47449-116">Il comando imposta il numero di DKU per il pool elastico su 1000 e imposta le DKU minimo e massimo.</span><span class="sxs-lookup"><span data-stu-id="47449-116">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="47449-117">Esempio 2: Modificare le dimensioni massime di archiviazione di un pool elastico</span><span class="sxs-lookup"><span data-stu-id="47449-117">Example 2: Modify the storage max size of an elastic pool</span></span>
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

<span data-ttu-id="47449-118">Questo comando modifica le proprietà per un pool elastico denominato elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="47449-118">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="47449-119">Il comando imposta lo spazio di archiviazione massimo per un pool elastico su 2 TB.</span><span class="sxs-lookup"><span data-stu-id="47449-119">The command sets the max storage for an elastic pool to 2 TB.</span></span>

### <span data-ttu-id="47449-120">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="47449-120">Example 3</span></span>

<span data-ttu-id="47449-121">Modifica le proprietà di un pool di database flessibile in Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="47449-121">Modifies properties of an elastic database pool in Azure SQL Database.</span></span> <span data-ttu-id="47449-122">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="47449-122">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticPool -Dtu 1000 -Edition 'GeneralPurpose' -ElasticPoolName 'ElasticPool01' -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01'
```

## <span data-ttu-id="47449-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47449-123">PARAMETERS</span></span>

### <span data-ttu-id="47449-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47449-124">-AsJob</span></span>
<span data-ttu-id="47449-125">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="47449-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="47449-126">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="47449-126">-ComputeGeneration</span></span>
<span data-ttu-id="47449-127">Generazione di elaborazione da assegnare.</span><span class="sxs-lookup"><span data-stu-id="47449-127">The compute generation to assign.</span></span>

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

### <span data-ttu-id="47449-128">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="47449-128">-DatabaseDtuMax</span></span>
<span data-ttu-id="47449-129">Specifica il numero massimo di DKU che può essere utilizzato da un singolo database nel pool.</span><span class="sxs-lookup"><span data-stu-id="47449-129">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span>
<span data-ttu-id="47449-130">Per informazioni dettagliate sui valori validi, vedere la tabella per il pool di dimensioni specifico in [pool di elastici.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="47449-130">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="47449-131">I valori predefiniti per le diverse edizioni sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="47449-131">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="47449-132">Di base.</span><span class="sxs-lookup"><span data-stu-id="47449-132">Basic.</span></span>  <span data-ttu-id="47449-133">5 DKU</span><span class="sxs-lookup"><span data-stu-id="47449-133">5 DTUs</span></span>
- <span data-ttu-id="47449-134">Standard.</span><span class="sxs-lookup"><span data-stu-id="47449-134">Standard.</span></span> <span data-ttu-id="47449-135">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="47449-135">100 DTUs</span></span>
- <span data-ttu-id="47449-136">Premium.</span><span class="sxs-lookup"><span data-stu-id="47449-136">Premium.</span></span> <span data-ttu-id="47449-137">125 DKU</span><span class="sxs-lookup"><span data-stu-id="47449-137">125 DTUs</span></span>

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

### <span data-ttu-id="47449-138">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="47449-138">-DatabaseDtuMin</span></span>
<span data-ttu-id="47449-139">Specifica il numero minimo di DKU garantiti dal pool flessibile a tutti i database del pool.</span><span class="sxs-lookup"><span data-stu-id="47449-139">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="47449-140">Per informazioni dettagliate sui valori validi, vedere la tabella per il pool di dimensioni specifico in [pool di elastici.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="47449-140">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="47449-141">Il valore predefinito è zero (0).</span><span class="sxs-lookup"><span data-stu-id="47449-141">The default value is zero (0).</span></span>

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

### <span data-ttu-id="47449-142">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="47449-142">-DatabaseVCoreMax</span></span>
<span data-ttu-id="47449-143">Numero VCore massimo che qualsiasi database SqlAzure può usare nel pool.</span><span class="sxs-lookup"><span data-stu-id="47449-143">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="47449-144">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="47449-144">-DatabaseVCoreMin</span></span>
<span data-ttu-id="47449-145">Valore VCore minimo che qualsiasi database SqlAzure può usare nel pool.</span><span class="sxs-lookup"><span data-stu-id="47449-145">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="47449-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47449-146">-DefaultProfile</span></span>
<span data-ttu-id="47449-147">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="47449-147">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="47449-148">-Dtu</span><span class="sxs-lookup"><span data-stu-id="47449-148">-Dtu</span></span>
<span data-ttu-id="47449-149">Specifica il numero totale di DKU condivise per il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="47449-149">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="47449-150">Per informazioni dettagliate sui valori validi, vedere la tabella per il pool di dimensioni specifico in [pool di elastici.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="47449-150">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="47449-151">I valori predefiniti per le diverse edizioni sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="47449-151">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="47449-152">Di base.</span><span class="sxs-lookup"><span data-stu-id="47449-152">Basic.</span></span> <span data-ttu-id="47449-153">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="47449-153">100 DTUs</span></span>
- <span data-ttu-id="47449-154">Standard.</span><span class="sxs-lookup"><span data-stu-id="47449-154">Standard.</span></span> <span data-ttu-id="47449-155">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="47449-155">100 DTUs</span></span>
- <span data-ttu-id="47449-156">Premium.</span><span class="sxs-lookup"><span data-stu-id="47449-156">Premium.</span></span> <span data-ttu-id="47449-157">125 DKU</span><span class="sxs-lookup"><span data-stu-id="47449-157">125 DTUs</span></span>

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

### <span data-ttu-id="47449-158">-Edition</span><span class="sxs-lookup"><span data-stu-id="47449-158">-Edition</span></span>
<span data-ttu-id="47449-159">Specifica l'edizione del database SQL Azure per il pool flessibile.</span><span class="sxs-lookup"><span data-stu-id="47449-159">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="47449-160">Non è possibile modificare l'edizione.</span><span class="sxs-lookup"><span data-stu-id="47449-160">You cannot change the edition.</span></span> <span data-ttu-id="47449-161">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="47449-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="47449-162">Nessuno</span><span class="sxs-lookup"><span data-stu-id="47449-162">None</span></span>
- <span data-ttu-id="47449-163">Di base</span><span class="sxs-lookup"><span data-stu-id="47449-163">Basic</span></span>
- <span data-ttu-id="47449-164">Standard</span><span class="sxs-lookup"><span data-stu-id="47449-164">Standard</span></span>
- <span data-ttu-id="47449-165">Premium</span><span class="sxs-lookup"><span data-stu-id="47449-165">Premium</span></span>
- <span data-ttu-id="47449-166">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="47449-166">DataWarehouse</span></span>
- <span data-ttu-id="47449-167">Gratis</span><span class="sxs-lookup"><span data-stu-id="47449-167">Free</span></span>
- <span data-ttu-id="47449-168">Estendamento</span><span class="sxs-lookup"><span data-stu-id="47449-168">Stretch</span></span>
- <span data-ttu-id="47449-169">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="47449-169">GeneralPurpose</span></span>
- <span data-ttu-id="47449-170">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="47449-170">BusinessCritical</span></span>

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

### <span data-ttu-id="47449-171">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="47449-171">-ElasticPoolName</span></span>
<span data-ttu-id="47449-172">Specifica il nome del pool elastico.</span><span class="sxs-lookup"><span data-stu-id="47449-172">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="47449-173">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="47449-173">-LicenseType</span></span>
<span data-ttu-id="47449-174">Il tipo di licenza per il database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="47449-174">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="47449-175">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="47449-175">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="47449-176">ID configurazione manutenzione per il pool SQL elastico.</span><span class="sxs-lookup"><span data-stu-id="47449-176">The Maintenance configuration id for the SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="47449-177">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47449-177">-ResourceGroupName</span></span>
<span data-ttu-id="47449-178">Specifica il nome del gruppo di risorse a cui è assegnato il pool flessibile.</span><span class="sxs-lookup"><span data-stu-id="47449-178">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="47449-179">-ServerName</span><span class="sxs-lookup"><span data-stu-id="47449-179">-ServerName</span></span>
<span data-ttu-id="47449-180">Specifica il nome del server che ospita il pool flessibile.</span><span class="sxs-lookup"><span data-stu-id="47449-180">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="47449-181">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="47449-181">-StorageMB</span></span>
<span data-ttu-id="47449-182">Specifica il limite di archiviazione, in megabyte, per il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="47449-182">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="47449-183">Per altre informazioni, vedere il cmdlet New-AzSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="47449-183">For more information, see the New-AzSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="47449-184">-Tag</span><span class="sxs-lookup"><span data-stu-id="47449-184">-Tags</span></span>
<span data-ttu-id="47449-185">Specifica un dizionario di coppie chiave-valore che questo cmdlet associa al pool elastico sotto forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="47449-185">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="47449-186">Per esempio: `@{key0="value0";"key 1"=$null;key2="value2"}`</span><span class="sxs-lookup"><span data-stu-id="47449-186">For example: `@{key0="value0";"key 1"=$null;key2="value2"}`</span></span>

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

### <span data-ttu-id="47449-187">-VCore</span><span class="sxs-lookup"><span data-stu-id="47449-187">-VCore</span></span>
<span data-ttu-id="47449-188">Il numero condiviso totale di Vcore per il pool di sql azure elastico.</span><span class="sxs-lookup"><span data-stu-id="47449-188">The total shared number of Vcore for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="47449-189">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="47449-189">-ZoneRedundant</span></span>
<span data-ttu-id="47449-190">La ridondanza dell'area da associare al pool sql elastico di Azure</span><span class="sxs-lookup"><span data-stu-id="47449-190">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="47449-191">-Confirm</span><span class="sxs-lookup"><span data-stu-id="47449-191">-Confirm</span></span>
<span data-ttu-id="47449-192">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47449-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47449-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47449-193">-WhatIf</span></span>
<span data-ttu-id="47449-194">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="47449-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47449-195">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="47449-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47449-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47449-196">CommonParameters</span></span>
<span data-ttu-id="47449-197">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47449-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47449-198">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="47449-198">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47449-199">INPUT</span><span class="sxs-lookup"><span data-stu-id="47449-199">INPUTS</span></span>

### <span data-ttu-id="47449-200">System.String</span><span class="sxs-lookup"><span data-stu-id="47449-200">System.String</span></span>

## <span data-ttu-id="47449-201">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="47449-201">OUTPUTS</span></span>

### <span data-ttu-id="47449-202">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="47449-202">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="47449-203">NOTE</span><span class="sxs-lookup"><span data-stu-id="47449-203">NOTES</span></span>

## <span data-ttu-id="47449-204">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="47449-204">RELATED LINKS</span></span>

[<span data-ttu-id="47449-205">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="47449-205">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="47449-206">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="47449-206">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="47449-207">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="47449-207">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="47449-208">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="47449-208">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="47449-209">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="47449-209">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
