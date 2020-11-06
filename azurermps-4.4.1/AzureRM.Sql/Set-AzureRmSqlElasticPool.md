---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
ms.openlocfilehash: 512c77862c44af68b26eb300eb9a692c115b0750
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512807"
---
# <span data-ttu-id="0066f-101">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="0066f-101">Set-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="0066f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0066f-102">SYNOPSIS</span></span>
<span data-ttu-id="0066f-103">Modifica le proprietà di un pool di database elastici in Azure SQL database.</span><span class="sxs-lookup"><span data-stu-id="0066f-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0066f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0066f-104">SYNTAX</span></span>

```
Set-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Edition <DatabaseEdition>] [-Dtu <Int32>]
 [-StorageMB <Int32>] [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0066f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0066f-105">DESCRIPTION</span></span>
<span data-ttu-id="0066f-106">Il cmdlet **set-AzureRmSqlElasticPool** modifica le proprietà di un pool di database elastici in un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="0066f-106">The **Set-AzureRmSqlElasticPool** cmdlet modifies properties for an elastic database pool in an Azure SQL Database.</span></span> <span data-ttu-id="0066f-107">Questo cmdlet può modificare le unità minime di throughput del database (DTU) per ogni database, oltre al massimo DTU per database, al numero di DTU per il pool e al limite di spazio di archiviazione per il pool.</span><span class="sxs-lookup"><span data-stu-id="0066f-107">This cmdlet can modify the minimum Database Throughput Units (DTUs) per database in addition to the maximum DTUs per database, the number of DTUs for the pool, and the storage limit for the pool.</span></span>

<span data-ttu-id="0066f-108">Diversi parametri ( *-DTU,-DatabaseDtuMin e-DatabaseDtuMax* ) richiedono che il valore impostato sia dall'elenco di valori validi per il parametro.</span><span class="sxs-lookup"><span data-stu-id="0066f-108">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="0066f-109">Ad esempio,-DatabaseDtuMax per un pool di eDTU standard di 100 può essere impostato solo su 10, 20, 50 o 100.</span><span class="sxs-lookup"><span data-stu-id="0066f-109">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="0066f-110">Per informazioni dettagliate sui valori validi, vedere la tabella per il pool di dimensioni specifiche in [pool elastici](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="0066f-110">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="0066f-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0066f-111">EXAMPLES</span></span>

### <span data-ttu-id="0066f-112">Esempio 1: modificare le proprietà per un pool elastico</span><span class="sxs-lookup"><span data-stu-id="0066f-112">Example 1: Modify properties for an elastic pool</span></span>
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

<span data-ttu-id="0066f-113">Questo comando modifica le proprietà di un pool elastico denominato elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="0066f-113">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="0066f-114">Il comando imposta il numero di DTU per il pool elastico su 1000 e imposta la DTU minima e massima.</span><span class="sxs-lookup"><span data-stu-id="0066f-114">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="0066f-115">Esempio 2: modificare lo spazio di archiviazione max di un pool elastico</span><span class="sxs-lookup"><span data-stu-id="0066f-115">Example 2: Modify the max storage of an elastic pool</span></span>
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

<span data-ttu-id="0066f-116">Questo comando modifica le proprietà di un pool elastico denominato elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="0066f-116">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="0066f-117">Il comando imposta lo spazio di archiviazione max per un pool elastico su 2 TB.</span><span class="sxs-lookup"><span data-stu-id="0066f-117">The command sets the max storage for an elastic pool to 2 TB.</span></span>

## <span data-ttu-id="0066f-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0066f-118">PARAMETERS</span></span>

### <span data-ttu-id="0066f-119">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="0066f-119">-DatabaseDtuMax</span></span>
<span data-ttu-id="0066f-120">Specifica il numero massimo di DTU che può essere utilizzato da qualsiasi singolo database nel pool.</span><span class="sxs-lookup"><span data-stu-id="0066f-120">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span> 

<span data-ttu-id="0066f-121">Per informazioni dettagliate sui valori validi, vedere la tabella per il pool di dimensioni specifiche in [pool elastici](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="0066f-121">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

<span data-ttu-id="0066f-122">I valori predefiniti per le diverse edizioni sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="0066f-122">The default values for different editions are as follows:</span></span>

- <span data-ttu-id="0066f-123">Base.</span><span class="sxs-lookup"><span data-stu-id="0066f-123">Basic.</span></span>  <span data-ttu-id="0066f-124">5 DTU</span><span class="sxs-lookup"><span data-stu-id="0066f-124">5 DTUs</span></span>
- <span data-ttu-id="0066f-125">Standard.</span><span class="sxs-lookup"><span data-stu-id="0066f-125">Standard.</span></span> <span data-ttu-id="0066f-126">100 DTU</span><span class="sxs-lookup"><span data-stu-id="0066f-126">100 DTUs</span></span>
- <span data-ttu-id="0066f-127">Premium.</span><span class="sxs-lookup"><span data-stu-id="0066f-127">Premium.</span></span> <span data-ttu-id="0066f-128">125 DTU</span><span class="sxs-lookup"><span data-stu-id="0066f-128">125 DTUs</span></span>


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

### <span data-ttu-id="0066f-129">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="0066f-129">-DatabaseDtuMin</span></span>
<span data-ttu-id="0066f-130">Specifica il numero minimo di DTU che il pool elastico garantisce a tutti i database nel pool.</span><span class="sxs-lookup"><span data-stu-id="0066f-130">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>

<span data-ttu-id="0066f-131">Per informazioni dettagliate sui valori validi, vedere la tabella per il pool di dimensioni specifiche in [pool elastici](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="0066f-131">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

<span data-ttu-id="0066f-132">Il valore predefinito è zero (0).</span><span class="sxs-lookup"><span data-stu-id="0066f-132">The default value is zero (0).</span></span>

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

### <span data-ttu-id="0066f-133">-DTU</span><span class="sxs-lookup"><span data-stu-id="0066f-133">-Dtu</span></span>
<span data-ttu-id="0066f-134">Specifica il numero totale di DTU condivisi per il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="0066f-134">Specifies the total number of shared DTUs for the elastic pool.</span></span> 

<span data-ttu-id="0066f-135">Per informazioni dettagliate sui valori validi, vedere la tabella per il pool di dimensioni specifiche in [pool elastici](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="0066f-135">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

<span data-ttu-id="0066f-136">I valori predefiniti per le diverse edizioni sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="0066f-136">The default values for different editions are as follows:</span></span>

- <span data-ttu-id="0066f-137">Base.</span><span class="sxs-lookup"><span data-stu-id="0066f-137">Basic.</span></span> <span data-ttu-id="0066f-138">100 DTU</span><span class="sxs-lookup"><span data-stu-id="0066f-138">100 DTUs</span></span>
- <span data-ttu-id="0066f-139">Standard.</span><span class="sxs-lookup"><span data-stu-id="0066f-139">Standard.</span></span> <span data-ttu-id="0066f-140">100 DTU</span><span class="sxs-lookup"><span data-stu-id="0066f-140">100 DTUs</span></span>
- <span data-ttu-id="0066f-141">Premium.</span><span class="sxs-lookup"><span data-stu-id="0066f-141">Premium.</span></span> <span data-ttu-id="0066f-142">125 DTU</span><span class="sxs-lookup"><span data-stu-id="0066f-142">125 DTUs</span></span>

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

### <span data-ttu-id="0066f-143">-Edition</span><span class="sxs-lookup"><span data-stu-id="0066f-143">-Edition</span></span>
<span data-ttu-id="0066f-144">Specifica l'edizione del database SQL di Azure per il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="0066f-144">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="0066f-145">Non è possibile modificare l'edizione.</span><span class="sxs-lookup"><span data-stu-id="0066f-145">You cannot change the edition.</span></span> <span data-ttu-id="0066f-146">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="0066f-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0066f-147">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0066f-147">None</span></span>
- <span data-ttu-id="0066f-148">Base</span><span class="sxs-lookup"><span data-stu-id="0066f-148">Basic</span></span>
- <span data-ttu-id="0066f-149">Standard</span><span class="sxs-lookup"><span data-stu-id="0066f-149">Standard</span></span>
- <span data-ttu-id="0066f-150">Premium</span><span class="sxs-lookup"><span data-stu-id="0066f-150">Premium</span></span>
- <span data-ttu-id="0066f-151">Premiumr</span><span class="sxs-lookup"><span data-stu-id="0066f-151">PremiumRS</span></span>
- <span data-ttu-id="0066f-152">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="0066f-152">DataWarehouse</span></span>
- <span data-ttu-id="0066f-153">Gratuito</span><span class="sxs-lookup"><span data-stu-id="0066f-153">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases: 
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0066f-154">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="0066f-154">-ElasticPoolName</span></span>
<span data-ttu-id="0066f-155">Specifica il nome del pool elastico.</span><span class="sxs-lookup"><span data-stu-id="0066f-155">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="0066f-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0066f-156">-ResourceGroupName</span></span>
<span data-ttu-id="0066f-157">Specifica il nome del gruppo di risorse a cui è assegnato il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="0066f-157">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="0066f-158">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="0066f-158">-ServerName</span></span>
<span data-ttu-id="0066f-159">Specifica il nome del server che ospita il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="0066f-159">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="0066f-160">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="0066f-160">-StorageMB</span></span>
<span data-ttu-id="0066f-161">Specifica il limite di archiviazione, in megabyte, per il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="0066f-161">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="0066f-162">Per altre informazioni, vedere il cmdlet New-AzureRmSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="0066f-162">For more information, see the New-AzureRmSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="0066f-163">-Tag</span><span class="sxs-lookup"><span data-stu-id="0066f-163">-Tags</span></span>
<span data-ttu-id="0066f-164">Specifica un dizionario di coppie chiave-valore che questo cmdlet associa al pool elastico in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="0066f-164">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="0066f-165">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="0066f-165">For example:</span></span>

`@{key0="value0";"key 1"=$null;key2="value2"}`

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

### <span data-ttu-id="0066f-166">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0066f-166">-Confirm</span></span>
<span data-ttu-id="0066f-167">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0066f-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0066f-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0066f-168">-WhatIf</span></span>
<span data-ttu-id="0066f-169">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0066f-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0066f-170">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0066f-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0066f-171">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0066f-171">-DefaultProfile</span></span>
<span data-ttu-id="0066f-172">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0066f-172">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0066f-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0066f-173">CommonParameters</span></span>
<span data-ttu-id="0066f-174">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0066f-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0066f-175">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0066f-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0066f-176">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0066f-176">INPUTS</span></span>

## <span data-ttu-id="0066f-177">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0066f-177">OUTPUTS</span></span>

### <span data-ttu-id="0066f-178">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="0066f-178">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="0066f-179">Note</span><span class="sxs-lookup"><span data-stu-id="0066f-179">NOTES</span></span>

## <span data-ttu-id="0066f-180">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0066f-180">RELATED LINKS</span></span>

[<span data-ttu-id="0066f-181">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="0066f-181">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="0066f-182">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="0066f-182">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="0066f-183">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="0066f-183">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="0066f-184">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="0066f-184">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="0066f-185">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="0066f-185">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
