---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
ms.openlocfilehash: 3d93b0d82a2769acce620ce97141be68c003c281
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517896"
---
# <span data-ttu-id="576ce-101">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="576ce-101">New-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="576ce-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="576ce-102">SYNOPSIS</span></span>
<span data-ttu-id="576ce-103">Crea un pool di database elastici per un database SQL.</span><span class="sxs-lookup"><span data-stu-id="576ce-103">Creates an elastic database pool for a SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="576ce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="576ce-104">SYNTAX</span></span>

```
New-AzureRmSqlElasticPool -ElasticPoolName <String> [-Edition <DatabaseEdition>] [-Dtu <Int32>]
 [-StorageMB <Int32>] [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="576ce-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="576ce-105">DESCRIPTION</span></span>
<span data-ttu-id="576ce-106">Il cmdlet **New-AzureRmSqlElasticPool** crea un pool di database elastici per un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="576ce-106">The **New-AzureRmSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>

<span data-ttu-id="576ce-107">Diversi parametri ( *-DTU,-DatabaseDtuMin e-DatabaseDtuMax* ) richiedono che il valore impostato sia dall'elenco di valori validi per il parametro.</span><span class="sxs-lookup"><span data-stu-id="576ce-107">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="576ce-108">Ad esempio,-DatabaseDtuMax per un pool di eDTU standard di 100 può essere impostato solo su 10, 20, 50 o 100.</span><span class="sxs-lookup"><span data-stu-id="576ce-108">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="576ce-109">Per informazioni dettagliate sui valori validi, vedere la tabella per il pool di dimensioni specifiche in [pool elastici](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="576ce-109">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

## <span data-ttu-id="576ce-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="576ce-110">EXAMPLES</span></span>

### <span data-ttu-id="576ce-111">Esempio 1: creare un pool elastico</span><span class="sxs-lookup"><span data-stu-id="576ce-111">Example 1: Create an elastic pool</span></span>
```
PS C:\>New-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Edition "Standard" -Dtu 400 -DatabaseDtuMin 10 -DatabaseDtuMax 100
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

<span data-ttu-id="576ce-112">Questo comando crea un pool elastico nel livello di servizio standard denominato ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="576ce-112">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="576ce-113">Il server denominato Server01, assegnato a un gruppo di risorse di Azure denominato ResourceGroup01, ospita il pool di elastici in.</span><span class="sxs-lookup"><span data-stu-id="576ce-113">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="576ce-114">Il comando specifica i valori della proprietà DTU per il pool e i database nel pool.</span><span class="sxs-lookup"><span data-stu-id="576ce-114">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

## <span data-ttu-id="576ce-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="576ce-115">PARAMETERS</span></span>

### <span data-ttu-id="576ce-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="576ce-116">-AsJob</span></span>
<span data-ttu-id="576ce-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="576ce-117">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="576ce-118">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="576ce-118">-DatabaseDtuMax</span></span>
<span data-ttu-id="576ce-119">Specifica il numero massimo di unità di throughput del database (DTU) che ogni singolo database nel pool può utilizzare.</span><span class="sxs-lookup"><span data-stu-id="576ce-119">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="576ce-120">I valori predefiniti per le diverse edizioni sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="576ce-120">The default values for the different editions are as follows:</span></span>

- <span data-ttu-id="576ce-121">Base.</span><span class="sxs-lookup"><span data-stu-id="576ce-121">Basic.</span></span> <span data-ttu-id="576ce-122">5 DTU</span><span class="sxs-lookup"><span data-stu-id="576ce-122">5 DTUs</span></span>
- <span data-ttu-id="576ce-123">Standard.</span><span class="sxs-lookup"><span data-stu-id="576ce-123">Standard.</span></span> <span data-ttu-id="576ce-124">100 DTU</span><span class="sxs-lookup"><span data-stu-id="576ce-124">100 DTUs</span></span>
- <span data-ttu-id="576ce-125">Premium.</span><span class="sxs-lookup"><span data-stu-id="576ce-125">Premium.</span></span> <span data-ttu-id="576ce-126">125 DTU</span><span class="sxs-lookup"><span data-stu-id="576ce-126">125 DTUs</span></span>

<span data-ttu-id="576ce-127">Per informazioni dettagliate sui valori validi, vedere la tabella per il pool di dimensioni specifiche in [pool elastici](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="576ce-127">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span> 


```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="576ce-128">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="576ce-128">-DatabaseDtuMin</span></span>
<span data-ttu-id="576ce-129">Specifica il numero minimo di DTU che il pool elastico garantisce a tutti i database nel pool.</span><span class="sxs-lookup"><span data-stu-id="576ce-129">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="576ce-130">Il valore predefinito è zero (0).</span><span class="sxs-lookup"><span data-stu-id="576ce-130">The default value is zero (0).</span></span>

<span data-ttu-id="576ce-131">Per informazioni dettagliate sui valori validi, vedere la tabella per il pool di dimensioni specifiche in [pool elastici](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="576ce-131">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="576ce-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="576ce-132">-DefaultProfile</span></span>
<span data-ttu-id="576ce-133">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="576ce-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="576ce-134">-DTU</span><span class="sxs-lookup"><span data-stu-id="576ce-134">-Dtu</span></span>
<span data-ttu-id="576ce-135">Specifica il numero totale di DTU condivisi per il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="576ce-135">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="576ce-136">I valori predefiniti per le diverse edizioni sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="576ce-136">The default values for the different editions are as follows:</span></span>

- <span data-ttu-id="576ce-137">Base.</span><span class="sxs-lookup"><span data-stu-id="576ce-137">Basic.</span></span>
<span data-ttu-id="576ce-138">100 DTU</span><span class="sxs-lookup"><span data-stu-id="576ce-138">100 DTUs</span></span>
- <span data-ttu-id="576ce-139">Standard.</span><span class="sxs-lookup"><span data-stu-id="576ce-139">Standard.</span></span>
<span data-ttu-id="576ce-140">100 DTU</span><span class="sxs-lookup"><span data-stu-id="576ce-140">100 DTUs</span></span>
- <span data-ttu-id="576ce-141">Premium.</span><span class="sxs-lookup"><span data-stu-id="576ce-141">Premium.</span></span>
<span data-ttu-id="576ce-142">125 DTU</span><span class="sxs-lookup"><span data-stu-id="576ce-142">125 DTUs</span></span>

<span data-ttu-id="576ce-143">Per informazioni dettagliate sui valori validi, vedere la tabella per il pool di dimensioni specifiche in [pool elastici](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="576ce-143">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="576ce-144">-Edition</span><span class="sxs-lookup"><span data-stu-id="576ce-144">-Edition</span></span>
<span data-ttu-id="576ce-145">Specifica l'edizione del database SQL di Azure usato per il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="576ce-145">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="576ce-146">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="576ce-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="576ce-147">Premium</span><span class="sxs-lookup"><span data-stu-id="576ce-147">Premium</span></span>
- <span data-ttu-id="576ce-148">Base</span><span class="sxs-lookup"><span data-stu-id="576ce-148">Basic</span></span>
- <span data-ttu-id="576ce-149">Standard</span><span class="sxs-lookup"><span data-stu-id="576ce-149">Standard</span></span>
- <span data-ttu-id="576ce-150">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="576ce-150">DataWarehouse</span></span>
- <span data-ttu-id="576ce-151">Tratto</span><span class="sxs-lookup"><span data-stu-id="576ce-151">Stretch</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="576ce-152">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="576ce-152">-ElasticPoolName</span></span>
<span data-ttu-id="576ce-153">Specifica il nome del pool elastico creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="576ce-153">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="576ce-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="576ce-154">-ResourceGroupName</span></span>
<span data-ttu-id="576ce-155">Specifica il nome del gruppo di risorse a cui questo cmdlet assegna il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="576ce-155">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="576ce-156">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="576ce-156">-ServerName</span></span>
<span data-ttu-id="576ce-157">Specifica il nome del server che ospita il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="576ce-157">Specifies the name of the server that hosts the elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="576ce-158">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="576ce-158">-StorageMB</span></span>
<span data-ttu-id="576ce-159">Specifica il limite di archiviazione, in megabyte, per il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="576ce-159">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="576ce-160">Se non specifichi questo parametro, questo cmdlet calcola un valore che dipende dal valore del parametro *DTU* .</span><span class="sxs-lookup"><span data-stu-id="576ce-160">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>

<span data-ttu-id="576ce-161">Vedere [limiti di eDTU e archiviazione](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) per i valori possibili.</span><span class="sxs-lookup"><span data-stu-id="576ce-161">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="576ce-162">-Tag</span><span class="sxs-lookup"><span data-stu-id="576ce-162">-Tags</span></span>
<span data-ttu-id="576ce-163">Specifica un dizionario di coppie chiave-valore in forma di tabella hash associata al pool elastico da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="576ce-163">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="576ce-164">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="576ce-164">For example:</span></span>

<span data-ttu-id="576ce-165">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="576ce-165">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="576ce-166">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="576ce-166">-ZoneRedundant</span></span>
<span data-ttu-id="576ce-167">Ridondanza della zona da associare al pool di Azure SQL Elastic</span><span class="sxs-lookup"><span data-stu-id="576ce-167">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="576ce-168">-Confermare</span><span class="sxs-lookup"><span data-stu-id="576ce-168">-Confirm</span></span>
<span data-ttu-id="576ce-169">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="576ce-169">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="576ce-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="576ce-170">-WhatIf</span></span>
<span data-ttu-id="576ce-171">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="576ce-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="576ce-172">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="576ce-172">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="576ce-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="576ce-173">CommonParameters</span></span>
<span data-ttu-id="576ce-174">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="576ce-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="576ce-175">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="576ce-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="576ce-176">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="576ce-176">INPUTS</span></span>

### <span data-ttu-id="576ce-177">Nessuno</span><span class="sxs-lookup"><span data-stu-id="576ce-177">None</span></span>
<span data-ttu-id="576ce-178">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="576ce-178">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="576ce-179">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="576ce-179">OUTPUTS</span></span>

### <span data-ttu-id="576ce-180">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="576ce-180">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="576ce-181">Note</span><span class="sxs-lookup"><span data-stu-id="576ce-181">NOTES</span></span>

## <span data-ttu-id="576ce-182">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="576ce-182">RELATED LINKS</span></span>

[<span data-ttu-id="576ce-183">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="576ce-183">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="576ce-184">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="576ce-184">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="576ce-185">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="576ce-185">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="576ce-186">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="576ce-186">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="576ce-187">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="576ce-187">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

[<span data-ttu-id="576ce-188">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="576ce-188">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
