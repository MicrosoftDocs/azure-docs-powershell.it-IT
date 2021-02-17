---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 7b773bd51a928c21761900cf1f6f8c34e73c2d0e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177246"
---
# <span data-ttu-id="ec54e-101">New-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="ec54e-101">New-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="ec54e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec54e-102">SYNOPSIS</span></span>
<span data-ttu-id="ec54e-103">Crea un nuovo contenitore sql per database database.</span><span class="sxs-lookup"><span data-stu-id="ec54e-103">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="ec54e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ec54e-104">SYNTAX</span></span>

### <span data-ttu-id="ec54e-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ec54e-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-AnalyticalStorageTtl <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ec54e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec54e-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlContainer -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-AnalyticalStorageTtl <Int32>] -ParentObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec54e-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ec54e-107">DESCRIPTION</span></span>
<span data-ttu-id="ec54e-108">Crea un nuovo contenitore sql per database database.</span><span class="sxs-lookup"><span data-stu-id="ec54e-108">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="ec54e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ec54e-109">EXAMPLES</span></span>

### <span data-ttu-id="ec54e-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ec54e-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlContainer -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a/b/c -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName/contain
           ers/myContainerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="ec54e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec54e-111">PARAMETERS</span></span>

### <span data-ttu-id="ec54e-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ec54e-112">-AccountName</span></span>
<span data-ttu-id="ec54e-113">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="ec54e-113">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec54e-114">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="ec54e-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="ec54e-115">TTL per l'archiviazione analitica (in secondi).</span><span class="sxs-lookup"><span data-stu-id="ec54e-115">TTL for Analytical Storage (in Seconds).</span></span>

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

### <span data-ttu-id="ec54e-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="ec54e-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="ec54e-117">Valore massimo di velocità effettiva se è abilitata la scalabilità automatica.</span><span class="sxs-lookup"><span data-stu-id="ec54e-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="ec54e-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ec54e-118">-Confirm</span></span>
<span data-ttu-id="ec54e-119">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec54e-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec54e-120">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="ec54e-120">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="ec54e-121">Oggetto ConflictResolutionPolicy di tipo PSSqlConflictResolutionPolicy, quando specificato è impostato come ConflictResolutionPolicy del contenitore.</span><span class="sxs-lookup"><span data-stu-id="ec54e-121">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

```yaml
Type: PSSqlConflictResolutionPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec54e-122">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="ec54e-122">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="ec54e-123">Possono contenere i valori: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="ec54e-123">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="ec54e-124">Se fornito insieme al parametro ConflictResolutionPolicy, viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="ec54e-124">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec54e-125">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="ec54e-125">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="ec54e-126">Da immettere quando il tipo è LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="ec54e-126">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="ec54e-127">Se fornito insieme al parametro ConflictResolutionPolicy, viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="ec54e-127">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec54e-128">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="ec54e-128">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="ec54e-129">Da immettere quando il tipo è personalizzato.</span><span class="sxs-lookup"><span data-stu-id="ec54e-129">To be provided when the type is custom.</span></span>
<span data-ttu-id="ec54e-130">Se fornito insieme al parametro ConflictResolutionPolicy, viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="ec54e-130">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec54e-131">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ec54e-131">-DatabaseName</span></span>
<span data-ttu-id="ec54e-132">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="ec54e-132">Database name.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec54e-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec54e-133">-DefaultProfile</span></span>
<span data-ttu-id="ec54e-134">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ec54e-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec54e-135">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="ec54e-135">-IndexingPolicy</span></span>
<span data-ttu-id="ec54e-136">Oggetto criterio di indicizzazione di tipo Microsoft.Azure.Commands.SqlsDB.PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="ec54e-136">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

```yaml
Type: PSSqlIndexingPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec54e-137">-Name</span><span class="sxs-lookup"><span data-stu-id="ec54e-137">-Name</span></span>
<span data-ttu-id="ec54e-138">Nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="ec54e-138">Container name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec54e-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ec54e-139">-ParentObject</span></span>
<span data-ttu-id="ec54e-140">Oggetto Database Sql.</span><span class="sxs-lookup"><span data-stu-id="ec54e-140">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec54e-141">-PartitionKey Rieti</span><span class="sxs-lookup"><span data-stu-id="ec54e-141">-PartitionKeyKind</span></span>
<span data-ttu-id="ec54e-142">Il tipo di algoritmo usato per il partizionamento.</span><span class="sxs-lookup"><span data-stu-id="ec54e-142">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="ec54e-143">I valori possibili includono: 'Hash', 'Range'</span><span class="sxs-lookup"><span data-stu-id="ec54e-143">Possible values include: 'Hash', 'Range'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec54e-144">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="ec54e-144">-PartitionKeyPath</span></span>
<span data-ttu-id="ec54e-145">Percorso chiave di partizione, ad esempio '/address/zipcode'.</span><span class="sxs-lookup"><span data-stu-id="ec54e-145">Partition Key Path, e.g., '/address/zipcode'.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec54e-146">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="ec54e-146">-PartitionKeyVersion</span></span>
<span data-ttu-id="ec54e-147">Versione della definizione della chiave di partizione</span><span class="sxs-lookup"><span data-stu-id="ec54e-147">The version of the partition key definition</span></span>

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

### <span data-ttu-id="ec54e-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec54e-148">-ResourceGroupName</span></span>
<span data-ttu-id="ec54e-149">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ec54e-149">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec54e-150">-Velocità effettiva</span><span class="sxs-lookup"><span data-stu-id="ec54e-150">-Throughput</span></span>
<span data-ttu-id="ec54e-151">Velocità effettiva del contenitore SQL (RU/S).</span><span class="sxs-lookup"><span data-stu-id="ec54e-151">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="ec54e-152">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="ec54e-152">Default value is 400.</span></span>

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

### <span data-ttu-id="ec54e-153">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="ec54e-153">-TtlInSeconds</span></span>
<span data-ttu-id="ec54e-154">Ttl predefinito in secondi.</span><span class="sxs-lookup"><span data-stu-id="ec54e-154">Default Ttl in seconds.</span></span>
<span data-ttu-id="ec54e-155">Se il valore manca o è impostato su -1, gli elementi non scadono.</span><span class="sxs-lookup"><span data-stu-id="ec54e-155">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="ec54e-156">Se il valore è impostato su n, gli elementi scadranno n secondi dopo l'ora dell'ultima modifica.</span><span class="sxs-lookup"><span data-stu-id="ec54e-156">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="ec54e-157">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="ec54e-157">-UniqueKeyPolicy</span></span>
<span data-ttu-id="ec54e-158">Oggetto UniqueKeyPolicy di tipo Microsoft.Azure.Commands.SqlsDB.PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="ec54e-158">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

```yaml
Type: PSSqlUniqueKeyPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec54e-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec54e-159">-WhatIf</span></span>
<span data-ttu-id="ec54e-160">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ec54e-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec54e-161">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ec54e-161">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec54e-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec54e-162">CommonParameters</span></span>
<span data-ttu-id="ec54e-163">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec54e-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec54e-164">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ec54e-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec54e-165">INPUT</span><span class="sxs-lookup"><span data-stu-id="ec54e-165">INPUTS</span></span>

### <span data-ttu-id="ec54e-166">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="ec54e-166">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="ec54e-167">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="ec54e-167">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="ec54e-168">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="ec54e-168">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="ec54e-169">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="ec54e-169">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="ec54e-170">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ec54e-170">OUTPUTS</span></span>

### <span data-ttu-id="ec54e-171">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="ec54e-171">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="ec54e-172">Microsoft.Azure.Commands.ExceptionsDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="ec54e-172">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="ec54e-173">NOTE</span><span class="sxs-lookup"><span data-stu-id="ec54e-173">NOTES</span></span>

## <span data-ttu-id="ec54e-174">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ec54e-174">RELATED LINKS</span></span>
