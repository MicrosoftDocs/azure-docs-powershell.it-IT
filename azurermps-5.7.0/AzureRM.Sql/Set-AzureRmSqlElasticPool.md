---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
ms.openlocfilehash: 563cddc1723f0706eb5cdde691e9ab960e871989
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517856"
---
# <span data-ttu-id="115bb-101">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="115bb-101">Set-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="115bb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="115bb-102">SYNOPSIS</span></span>
<span data-ttu-id="115bb-103">Modifica le proprietà di un pool di database elastici in Azure SQL database.</span><span class="sxs-lookup"><span data-stu-id="115bb-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="115bb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="115bb-104">SYNTAX</span></span>

```
Set-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Edition <DatabaseEdition>] [-Dtu <Int32>]
 [-StorageMB <Int32>] [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="115bb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="115bb-105">DESCRIPTION</span></span>
<span data-ttu-id="115bb-106">Il cmdlet **set-AzureRmSqlElasticPool** imposta le proprietà per un pool elastico in Azure SQL database.</span><span class="sxs-lookup"><span data-stu-id="115bb-106">The **Set-AzureRmSqlElasticPool** cmdlet sets properties for an elastic pool in Azure SQL Database.</span></span> <span data-ttu-id="115bb-107">Questo cmdlet può modificare il eDTUs per pool ( *DTU* ), la dimensione massima dello spazio di archiviazione per pool ( *StorageMB* ), il eDTUs massimo per database ( *DatabaseDtuMax* ) e il minimo eDTUs per database ( *DatqabaseDtuMin* ).</span><span class="sxs-lookup"><span data-stu-id="115bb-107">This cmdlet can modify the eDTUs per pool ( *Dtu* ), storage max size per pool ( *StorageMB* ), maximum eDTUs per database ( *DatabaseDtuMax* ), and minimum eDTUs per database ( *DatqabaseDtuMin* ).</span></span>

<span data-ttu-id="115bb-108">Diversi parametri ( *-DTU,-DatabaseDtuMin e-DatabaseDtuMax* ) richiedono che il valore impostato sia dall'elenco di valori validi per il parametro.</span><span class="sxs-lookup"><span data-stu-id="115bb-108">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="115bb-109">Ad esempio,-DatabaseDtuMax per un pool di eDTU standard di 100 può essere impostato solo su 10, 20, 50 o 100.</span><span class="sxs-lookup"><span data-stu-id="115bb-109">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="115bb-110">Per informazioni dettagliate sui valori validi, vedere la tabella per il pool di dimensioni specifiche in [pool elastici](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="115bb-110">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="115bb-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="115bb-111">EXAMPLES</span></span>

### <span data-ttu-id="115bb-112">Esempio 1: modificare le proprietà per un pool elastico</span><span class="sxs-lookup"><span data-stu-id="115bb-112">Example 1: Modify properties for an elastic pool</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Dtu 1000 -DatabaseDtuMax 100 -DatabaseDtuMin 20
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

<span data-ttu-id="115bb-113">Questo comando modifica le proprietà di un pool elastico denominato elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="115bb-113">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="115bb-114">Il comando imposta il numero di DTU per il pool elastico su 1000 e imposta la DTU minima e massima.</span><span class="sxs-lookup"><span data-stu-id="115bb-114">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="115bb-115">Esempio 2: modificare le dimensioni massime dello spazio di archiviazione di un pool elastico</span><span class="sxs-lookup"><span data-stu-id="115bb-115">Example 2: Modify the storage max size of an elastic pool</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -StorageMB 2097152
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

<span data-ttu-id="115bb-116">Questo comando modifica le proprietà di un pool elastico denominato elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="115bb-116">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="115bb-117">Il comando imposta lo spazio di archiviazione max per un pool elastico su 2 TB.</span><span class="sxs-lookup"><span data-stu-id="115bb-117">The command sets the max storage for an elastic pool to 2 TB.</span></span>

## <span data-ttu-id="115bb-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="115bb-118">PARAMETERS</span></span>

### <span data-ttu-id="115bb-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="115bb-119">-AsJob</span></span>
<span data-ttu-id="115bb-120">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="115bb-120">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="115bb-121">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="115bb-121">-DatabaseDtuMax</span></span>
<span data-ttu-id="115bb-122">Specifica il numero massimo di DTU che può essere utilizzato da qualsiasi singolo database nel pool.</span><span class="sxs-lookup"><span data-stu-id="115bb-122">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span> 

<span data-ttu-id="115bb-123">Per informazioni dettagliate sui valori validi, vedere la tabella per il pool di dimensioni specifiche in [pool elastici](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="115bb-123">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

<span data-ttu-id="115bb-124">I valori predefiniti per le diverse edizioni sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="115bb-124">The default values for different editions are as follows:</span></span>

- <span data-ttu-id="115bb-125">Base.</span><span class="sxs-lookup"><span data-stu-id="115bb-125">Basic.</span></span>  <span data-ttu-id="115bb-126">5 DTU</span><span class="sxs-lookup"><span data-stu-id="115bb-126">5 DTUs</span></span>
- <span data-ttu-id="115bb-127">Standard.</span><span class="sxs-lookup"><span data-stu-id="115bb-127">Standard.</span></span> <span data-ttu-id="115bb-128">100 DTU</span><span class="sxs-lookup"><span data-stu-id="115bb-128">100 DTUs</span></span>
- <span data-ttu-id="115bb-129">Premium.</span><span class="sxs-lookup"><span data-stu-id="115bb-129">Premium.</span></span> <span data-ttu-id="115bb-130">125 DTU</span><span class="sxs-lookup"><span data-stu-id="115bb-130">125 DTUs</span></span>


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

### <span data-ttu-id="115bb-131">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="115bb-131">-DatabaseDtuMin</span></span>
<span data-ttu-id="115bb-132">Specifica il numero minimo di DTU che il pool elastico garantisce a tutti i database nel pool.</span><span class="sxs-lookup"><span data-stu-id="115bb-132">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>

<span data-ttu-id="115bb-133">Per informazioni dettagliate sui valori validi, vedere la tabella per il pool di dimensioni specifiche in [pool elastici](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="115bb-133">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

<span data-ttu-id="115bb-134">Il valore predefinito è zero (0).</span><span class="sxs-lookup"><span data-stu-id="115bb-134">The default value is zero (0).</span></span>

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

### <span data-ttu-id="115bb-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="115bb-135">-DefaultProfile</span></span>
<span data-ttu-id="115bb-136">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="115bb-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="115bb-137">-DTU</span><span class="sxs-lookup"><span data-stu-id="115bb-137">-Dtu</span></span>
<span data-ttu-id="115bb-138">Specifica il numero totale di DTU condivisi per il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="115bb-138">Specifies the total number of shared DTUs for the elastic pool.</span></span> 

<span data-ttu-id="115bb-139">Per informazioni dettagliate sui valori validi, vedere la tabella per il pool di dimensioni specifiche in [pool elastici](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="115bb-139">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

<span data-ttu-id="115bb-140">I valori predefiniti per le diverse edizioni sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="115bb-140">The default values for different editions are as follows:</span></span>

- <span data-ttu-id="115bb-141">Base.</span><span class="sxs-lookup"><span data-stu-id="115bb-141">Basic.</span></span> <span data-ttu-id="115bb-142">100 DTU</span><span class="sxs-lookup"><span data-stu-id="115bb-142">100 DTUs</span></span>
- <span data-ttu-id="115bb-143">Standard.</span><span class="sxs-lookup"><span data-stu-id="115bb-143">Standard.</span></span> <span data-ttu-id="115bb-144">100 DTU</span><span class="sxs-lookup"><span data-stu-id="115bb-144">100 DTUs</span></span>
- <span data-ttu-id="115bb-145">Premium.</span><span class="sxs-lookup"><span data-stu-id="115bb-145">Premium.</span></span> <span data-ttu-id="115bb-146">125 DTU</span><span class="sxs-lookup"><span data-stu-id="115bb-146">125 DTUs</span></span>

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

### <span data-ttu-id="115bb-147">-Edition</span><span class="sxs-lookup"><span data-stu-id="115bb-147">-Edition</span></span>
<span data-ttu-id="115bb-148">Specifica l'edizione del database SQL di Azure per il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="115bb-148">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="115bb-149">Non è possibile modificare l'edizione.</span><span class="sxs-lookup"><span data-stu-id="115bb-149">You cannot change the edition.</span></span> <span data-ttu-id="115bb-150">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="115bb-150">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="115bb-151">Nessuno</span><span class="sxs-lookup"><span data-stu-id="115bb-151">None</span></span>
- <span data-ttu-id="115bb-152">Base</span><span class="sxs-lookup"><span data-stu-id="115bb-152">Basic</span></span>
- <span data-ttu-id="115bb-153">Standard</span><span class="sxs-lookup"><span data-stu-id="115bb-153">Standard</span></span>
- <span data-ttu-id="115bb-154">Premium</span><span class="sxs-lookup"><span data-stu-id="115bb-154">Premium</span></span>
- <span data-ttu-id="115bb-155">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="115bb-155">DataWarehouse</span></span>

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

### <span data-ttu-id="115bb-156">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="115bb-156">-ElasticPoolName</span></span>
<span data-ttu-id="115bb-157">Specifica il nome del pool elastico.</span><span class="sxs-lookup"><span data-stu-id="115bb-157">Specifies the name of the elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="115bb-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="115bb-158">-ResourceGroupName</span></span>
<span data-ttu-id="115bb-159">Specifica il nome del gruppo di risorse a cui è assegnato il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="115bb-159">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="115bb-160">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="115bb-160">-ServerName</span></span>
<span data-ttu-id="115bb-161">Specifica il nome del server che ospita il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="115bb-161">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="115bb-162">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="115bb-162">-StorageMB</span></span>
<span data-ttu-id="115bb-163">Specifica il limite di archiviazione, in megabyte, per il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="115bb-163">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="115bb-164">Per altre informazioni, vedere il cmdlet New-AzureRmSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="115bb-164">For more information, see the New-AzureRmSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="115bb-165">-Tag</span><span class="sxs-lookup"><span data-stu-id="115bb-165">-Tags</span></span>
<span data-ttu-id="115bb-166">Specifica un dizionario di coppie chiave-valore che questo cmdlet associa al pool elastico in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="115bb-166">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="115bb-167">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="115bb-167">For example:</span></span>

`@{key0="value0";"key 1"=$null;key2="value2"}`

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

### <span data-ttu-id="115bb-168">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="115bb-168">-ZoneRedundant</span></span>
<span data-ttu-id="115bb-169">Ridondanza della zona da associare al pool di Azure SQL Elastic</span><span class="sxs-lookup"><span data-stu-id="115bb-169">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="115bb-170">-Confermare</span><span class="sxs-lookup"><span data-stu-id="115bb-170">-Confirm</span></span>
<span data-ttu-id="115bb-171">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="115bb-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="115bb-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="115bb-172">-WhatIf</span></span>
<span data-ttu-id="115bb-173">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="115bb-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="115bb-174">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="115bb-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="115bb-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="115bb-175">CommonParameters</span></span>
<span data-ttu-id="115bb-176">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="115bb-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="115bb-177">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="115bb-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="115bb-178">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="115bb-178">INPUTS</span></span>

### <span data-ttu-id="115bb-179">Nessuno</span><span class="sxs-lookup"><span data-stu-id="115bb-179">None</span></span>
<span data-ttu-id="115bb-180">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="115bb-180">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="115bb-181">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="115bb-181">OUTPUTS</span></span>

### <span data-ttu-id="115bb-182">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="115bb-182">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="115bb-183">Note</span><span class="sxs-lookup"><span data-stu-id="115bb-183">NOTES</span></span>

## <span data-ttu-id="115bb-184">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="115bb-184">RELATED LINKS</span></span>

[<span data-ttu-id="115bb-185">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="115bb-185">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="115bb-186">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="115bb-186">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="115bb-187">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="115bb-187">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="115bb-188">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="115bb-188">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="115bb-189">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="115bb-189">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
