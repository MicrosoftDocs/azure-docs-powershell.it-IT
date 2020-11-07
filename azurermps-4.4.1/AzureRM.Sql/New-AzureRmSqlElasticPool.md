---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
ms.openlocfilehash: 454aac300aa3b34cbc435df455100d64c5d0abdd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688602"
---
# <span data-ttu-id="ceafe-101">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ceafe-101">New-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="ceafe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ceafe-102">SYNOPSIS</span></span>
<span data-ttu-id="ceafe-103">Crea un pool di database elastici per un database SQL.</span><span class="sxs-lookup"><span data-stu-id="ceafe-103">Creates an elastic database pool for a SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ceafe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ceafe-104">SYNTAX</span></span>

```
New-AzureRmSqlElasticPool -ElasticPoolName <String> [-Edition <DatabaseEdition>] [-Dtu <Int32>]
 [-StorageMB <Int32>] [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ceafe-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ceafe-105">DESCRIPTION</span></span>
<span data-ttu-id="ceafe-106">Il cmdlet **New-AzureRmSqlElasticPool** crea un pool di database elastici per un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="ceafe-106">The **New-AzureRmSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>

<span data-ttu-id="ceafe-107">Diversi parametri ( *-DTU,-DatabaseDtuMin e-DatabaseDtuMax* ) richiedono che il valore impostato sia dall'elenco di valori validi per il parametro.</span><span class="sxs-lookup"><span data-stu-id="ceafe-107">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="ceafe-108">Ad esempio,-DatabaseDtuMax per un pool di eDTU standard di 100 può essere impostato solo su 10, 20, 50 o 100.</span><span class="sxs-lookup"><span data-stu-id="ceafe-108">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="ceafe-109">Per informazioni dettagliate sui valori validi, vedere la tabella per il pool di dimensioni specifiche in [pool elastici](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="ceafe-109">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

## <span data-ttu-id="ceafe-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ceafe-110">EXAMPLES</span></span>

### <span data-ttu-id="ceafe-111">Esempio 1: creare un pool elastico</span><span class="sxs-lookup"><span data-stu-id="ceafe-111">Example 1: Create an elastic pool</span></span>
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

<span data-ttu-id="ceafe-112">Questo comando crea un pool elastico nel livello di servizio standard denominato ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="ceafe-112">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="ceafe-113">Il server denominato Server01, assegnato a un gruppo di risorse di Azure denominato ResourceGroup01, ospita il pool di elastici in.</span><span class="sxs-lookup"><span data-stu-id="ceafe-113">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="ceafe-114">Il comando specifica i valori della proprietà DTU per il pool e i database nel pool.</span><span class="sxs-lookup"><span data-stu-id="ceafe-114">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

## <span data-ttu-id="ceafe-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ceafe-115">PARAMETERS</span></span>

### <span data-ttu-id="ceafe-116">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="ceafe-116">-DatabaseDtuMax</span></span>
<span data-ttu-id="ceafe-117">Specifica il numero massimo di unità di throughput del database (DTU) che ogni singolo database nel pool può utilizzare.</span><span class="sxs-lookup"><span data-stu-id="ceafe-117">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="ceafe-118">I valori predefiniti per le diverse edizioni sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ceafe-118">The default values for the different editions are as follows:</span></span>

- <span data-ttu-id="ceafe-119">Base.</span><span class="sxs-lookup"><span data-stu-id="ceafe-119">Basic.</span></span> <span data-ttu-id="ceafe-120">5 DTU</span><span class="sxs-lookup"><span data-stu-id="ceafe-120">5 DTUs</span></span>
- <span data-ttu-id="ceafe-121">Standard.</span><span class="sxs-lookup"><span data-stu-id="ceafe-121">Standard.</span></span> <span data-ttu-id="ceafe-122">100 DTU</span><span class="sxs-lookup"><span data-stu-id="ceafe-122">100 DTUs</span></span>
- <span data-ttu-id="ceafe-123">Premium.</span><span class="sxs-lookup"><span data-stu-id="ceafe-123">Premium.</span></span> <span data-ttu-id="ceafe-124">125 DTU</span><span class="sxs-lookup"><span data-stu-id="ceafe-124">125 DTUs</span></span>

<span data-ttu-id="ceafe-125">Per informazioni dettagliate sui valori validi, vedere la tabella per il pool di dimensioni specifiche in [pool elastici](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="ceafe-125">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span> 


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

### <span data-ttu-id="ceafe-126">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="ceafe-126">-DatabaseDtuMin</span></span>
<span data-ttu-id="ceafe-127">Specifica il numero minimo di DTU che il pool elastico garantisce a tutti i database nel pool.</span><span class="sxs-lookup"><span data-stu-id="ceafe-127">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="ceafe-128">Il valore predefinito è zero (0).</span><span class="sxs-lookup"><span data-stu-id="ceafe-128">The default value is zero (0).</span></span>

<span data-ttu-id="ceafe-129">Per informazioni dettagliate sui valori validi, vedere la tabella per il pool di dimensioni specifiche in [pool elastici](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="ceafe-129">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

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

### <span data-ttu-id="ceafe-130">-DTU</span><span class="sxs-lookup"><span data-stu-id="ceafe-130">-Dtu</span></span>
<span data-ttu-id="ceafe-131">Specifica il numero totale di DTU condivisi per il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="ceafe-131">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="ceafe-132">I valori predefiniti per le diverse edizioni sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ceafe-132">The default values for the different editions are as follows:</span></span>

- <span data-ttu-id="ceafe-133">Base.</span><span class="sxs-lookup"><span data-stu-id="ceafe-133">Basic.</span></span>
<span data-ttu-id="ceafe-134">100 DTU</span><span class="sxs-lookup"><span data-stu-id="ceafe-134">100 DTUs</span></span>
- <span data-ttu-id="ceafe-135">Standard.</span><span class="sxs-lookup"><span data-stu-id="ceafe-135">Standard.</span></span>
<span data-ttu-id="ceafe-136">100 DTU</span><span class="sxs-lookup"><span data-stu-id="ceafe-136">100 DTUs</span></span>
- <span data-ttu-id="ceafe-137">Premium.</span><span class="sxs-lookup"><span data-stu-id="ceafe-137">Premium.</span></span>
<span data-ttu-id="ceafe-138">125 DTU</span><span class="sxs-lookup"><span data-stu-id="ceafe-138">125 DTUs</span></span>

<span data-ttu-id="ceafe-139">Per informazioni dettagliate sui valori validi, vedere la tabella per il pool di dimensioni specifiche in [pool elastici](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="ceafe-139">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

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

### <span data-ttu-id="ceafe-140">-Edition</span><span class="sxs-lookup"><span data-stu-id="ceafe-140">-Edition</span></span>
<span data-ttu-id="ceafe-141">Specifica l'edizione del database SQL di Azure usato per il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="ceafe-141">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="ceafe-142">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ceafe-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ceafe-143">Premium</span><span class="sxs-lookup"><span data-stu-id="ceafe-143">Premium</span></span>
- <span data-ttu-id="ceafe-144">Base</span><span class="sxs-lookup"><span data-stu-id="ceafe-144">Basic</span></span>
- <span data-ttu-id="ceafe-145">Standard</span><span class="sxs-lookup"><span data-stu-id="ceafe-145">Standard</span></span>
- <span data-ttu-id="ceafe-146">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="ceafe-146">DataWarehouse</span></span>
- <span data-ttu-id="ceafe-147">Tratto</span><span class="sxs-lookup"><span data-stu-id="ceafe-147">Stretch</span></span>
- <span data-ttu-id="ceafe-148">Gratuito</span><span class="sxs-lookup"><span data-stu-id="ceafe-148">Free</span></span>
- <span data-ttu-id="ceafe-149">Premiumr</span><span class="sxs-lookup"><span data-stu-id="ceafe-149">PremiumRS</span></span>

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

### <span data-ttu-id="ceafe-150">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="ceafe-150">-ElasticPoolName</span></span>
<span data-ttu-id="ceafe-151">Specifica il nome del pool elastico creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ceafe-151">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ceafe-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ceafe-152">-ResourceGroupName</span></span>
<span data-ttu-id="ceafe-153">Specifica il nome del gruppo di risorse a cui questo cmdlet assegna il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="ceafe-153">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="ceafe-154">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="ceafe-154">-ServerName</span></span>
<span data-ttu-id="ceafe-155">Specifica il nome del server che ospita il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="ceafe-155">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="ceafe-156">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="ceafe-156">-StorageMB</span></span>
<span data-ttu-id="ceafe-157">Specifica il limite di archiviazione, in megabyte, per il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="ceafe-157">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="ceafe-158">Se non specifichi questo parametro, questo cmdlet calcola un valore che dipende dal valore del parametro *DTU* .</span><span class="sxs-lookup"><span data-stu-id="ceafe-158">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>

<span data-ttu-id="ceafe-159">Vedere [limiti di eDTU e archiviazione](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) per i valori possibili.</span><span class="sxs-lookup"><span data-stu-id="ceafe-159">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

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

### <span data-ttu-id="ceafe-160">-Tag</span><span class="sxs-lookup"><span data-stu-id="ceafe-160">-Tags</span></span>
<span data-ttu-id="ceafe-161">Specifica un dizionario di coppie chiave-valore in forma di tabella hash associata al pool elastico da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ceafe-161">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="ceafe-162">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="ceafe-162">For example:</span></span>

<span data-ttu-id="ceafe-163">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="ceafe-163">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ceafe-164">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ceafe-164">-Confirm</span></span>
<span data-ttu-id="ceafe-165">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ceafe-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ceafe-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ceafe-166">-WhatIf</span></span>
<span data-ttu-id="ceafe-167">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ceafe-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ceafe-168">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ceafe-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ceafe-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceafe-169">-DefaultProfile</span></span>
<span data-ttu-id="ceafe-170">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ceafe-170">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ceafe-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceafe-171">CommonParameters</span></span>
<span data-ttu-id="ceafe-172">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ceafe-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceafe-173">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ceafe-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceafe-174">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ceafe-174">INPUTS</span></span>

## <span data-ttu-id="ceafe-175">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ceafe-175">OUTPUTS</span></span>

### <span data-ttu-id="ceafe-176">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="ceafe-176">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="ceafe-177">Note</span><span class="sxs-lookup"><span data-stu-id="ceafe-177">NOTES</span></span>

## <span data-ttu-id="ceafe-178">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ceafe-178">RELATED LINKS</span></span>

[<span data-ttu-id="ceafe-179">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ceafe-179">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="ceafe-180">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="ceafe-180">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="ceafe-181">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="ceafe-181">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="ceafe-182">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ceafe-182">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="ceafe-183">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ceafe-183">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

[<span data-ttu-id="ceafe-184">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="ceafe-184">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
