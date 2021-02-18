---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 60bbe085aaaa65c65ba33839db5f02ae5198e155
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181239"
---
# <span data-ttu-id="f06f2-101">Update-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="f06f2-101">Update-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="f06f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f06f2-102">SYNOPSIS</span></span>
<span data-ttu-id="f06f2-103">Aggiorna il contenitore sql database database.</span><span class="sxs-lookup"><span data-stu-id="f06f2-103">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="f06f2-104">Esegue un'operazione di patch sul lato client leggendo il contenitore esistente.</span><span class="sxs-lookup"><span data-stu-id="f06f2-104">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="f06f2-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f06f2-105">SYNTAX</span></span>

### <span data-ttu-id="f06f2-106">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f06f2-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-AnalyticalStorageTtl <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f06f2-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f06f2-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainer [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] -ParentObject <PSSqlDatabaseGetResults>
 [-AnalyticalStorageTtl <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f06f2-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f06f2-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainer [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] [-AnalyticalStorageTtl <Int32>]
 -InputObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f06f2-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f06f2-109">DESCRIPTION</span></span>
<span data-ttu-id="f06f2-110">Aggiorna il contenitore sql database database.</span><span class="sxs-lookup"><span data-stu-id="f06f2-110">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="f06f2-111">Esegue un'operazione di patch sul lato client leggendo il contenitore esistente.</span><span class="sxs-lookup"><span data-stu-id="f06f2-111">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="f06f2-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f06f2-112">EXAMPLES</span></span>

### <span data-ttu-id="f06f2-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f06f2-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 800

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="f06f2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f06f2-114">PARAMETERS</span></span>

### <span data-ttu-id="f06f2-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f06f2-115">-AccountName</span></span>
<span data-ttu-id="f06f2-116">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="f06f2-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f06f2-117">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="f06f2-117">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="f06f2-118">TTL per l'archiviazione analitica (in secondi).</span><span class="sxs-lookup"><span data-stu-id="f06f2-118">TTL for Analytical Storage (in Seconds).</span></span>

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

### <span data-ttu-id="f06f2-119">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="f06f2-119">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="f06f2-120">Valore massimo di velocità effettiva se è abilitata la scalabilità automatica.</span><span class="sxs-lookup"><span data-stu-id="f06f2-120">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="f06f2-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f06f2-121">-Confirm</span></span>
<span data-ttu-id="f06f2-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f06f2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f06f2-123">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="f06f2-123">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="f06f2-124">Oggetto ConflictResolutionPolicy di tipo PSSqlConflictResolutionPolicy, quando specificato è impostato come ConflictResolutionPolicy del contenitore.</span><span class="sxs-lookup"><span data-stu-id="f06f2-124">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="f06f2-125">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="f06f2-125">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="f06f2-126">Possono contenere i valori: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="f06f2-126">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="f06f2-127">Se fornito insieme al parametro ConflictResolutionPolicy, viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="f06f2-127">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="f06f2-128">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="f06f2-128">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="f06f2-129">Da immettere quando il tipo è LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="f06f2-129">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="f06f2-130">Se fornito insieme al parametro ConflictResolutionPolicy, viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="f06f2-130">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="f06f2-131">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="f06f2-131">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="f06f2-132">Da immettere quando il tipo è personalizzato.</span><span class="sxs-lookup"><span data-stu-id="f06f2-132">To be provided when the type is custom.</span></span>
<span data-ttu-id="f06f2-133">Se fornito insieme al parametro ConflictResolutionPolicy, viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="f06f2-133">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="f06f2-134">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f06f2-134">-DatabaseName</span></span>
<span data-ttu-id="f06f2-135">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="f06f2-135">Database name.</span></span>

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

### <span data-ttu-id="f06f2-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f06f2-136">-DefaultProfile</span></span>
<span data-ttu-id="f06f2-137">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f06f2-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f06f2-138">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="f06f2-138">-IndexingPolicy</span></span>
<span data-ttu-id="f06f2-139">Oggetto criterio di indicizzazione di tipo Microsoft.Azure.Commands.SqlsDB.PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="f06f2-139">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="f06f2-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f06f2-140">-InputObject</span></span>
<span data-ttu-id="f06f2-141">Oggetto Contenitore Sql.</span><span class="sxs-lookup"><span data-stu-id="f06f2-141">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f06f2-142">-Name</span><span class="sxs-lookup"><span data-stu-id="f06f2-142">-Name</span></span>
<span data-ttu-id="f06f2-143">Nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="f06f2-143">Container name.</span></span>

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

### <span data-ttu-id="f06f2-144">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f06f2-144">-ParentObject</span></span>
<span data-ttu-id="f06f2-145">Oggetto Database Sql.</span><span class="sxs-lookup"><span data-stu-id="f06f2-145">Sql Database object.</span></span>

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

### <span data-ttu-id="f06f2-146">-PartitionKey Rieti</span><span class="sxs-lookup"><span data-stu-id="f06f2-146">-PartitionKeyKind</span></span>
<span data-ttu-id="f06f2-147">Il tipo di algoritmo usato per il partizionamento.</span><span class="sxs-lookup"><span data-stu-id="f06f2-147">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="f06f2-148">I valori possibili includono: 'Hash', 'Range'</span><span class="sxs-lookup"><span data-stu-id="f06f2-148">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="f06f2-149">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="f06f2-149">-PartitionKeyPath</span></span>
<span data-ttu-id="f06f2-150">Percorso chiave di partizione, ad esempio '/address/zipcode'.</span><span class="sxs-lookup"><span data-stu-id="f06f2-150">Partition Key Path, e.g., '/address/zipcode'.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f06f2-151">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="f06f2-151">-PartitionKeyVersion</span></span>
<span data-ttu-id="f06f2-152">Versione della definizione della chiave di partizione</span><span class="sxs-lookup"><span data-stu-id="f06f2-152">The version of the partition key definition</span></span>

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

### <span data-ttu-id="f06f2-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f06f2-153">-ResourceGroupName</span></span>
<span data-ttu-id="f06f2-154">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f06f2-154">Name of resource group.</span></span>

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

### <span data-ttu-id="f06f2-155">-Velocità effettiva</span><span class="sxs-lookup"><span data-stu-id="f06f2-155">-Throughput</span></span>
<span data-ttu-id="f06f2-156">Velocità effettiva del contenitore SQL (RU/S).</span><span class="sxs-lookup"><span data-stu-id="f06f2-156">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="f06f2-157">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="f06f2-157">Default value is 400.</span></span>

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

### <span data-ttu-id="f06f2-158">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="f06f2-158">-TtlInSeconds</span></span>
<span data-ttu-id="f06f2-159">Ttl predefinito in secondi.</span><span class="sxs-lookup"><span data-stu-id="f06f2-159">Default Ttl in seconds.</span></span>
<span data-ttu-id="f06f2-160">Se il valore manca o è impostato su -1, gli elementi non scadono.</span><span class="sxs-lookup"><span data-stu-id="f06f2-160">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="f06f2-161">Se il valore è impostato su n, gli elementi scadranno n secondi dopo l'ora dell'ultima modifica.</span><span class="sxs-lookup"><span data-stu-id="f06f2-161">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="f06f2-162">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="f06f2-162">-UniqueKeyPolicy</span></span>
<span data-ttu-id="f06f2-163">Oggetto UniqueKeyPolicy di tipo Microsoft.Azure.Commands.SqlsDB.PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="f06f2-163">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="f06f2-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f06f2-164">-WhatIf</span></span>
<span data-ttu-id="f06f2-165">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f06f2-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f06f2-166">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f06f2-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f06f2-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f06f2-167">CommonParameters</span></span>
<span data-ttu-id="f06f2-168">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f06f2-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f06f2-169">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f06f2-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f06f2-170">INPUT</span><span class="sxs-lookup"><span data-stu-id="f06f2-170">INPUTS</span></span>

### <span data-ttu-id="f06f2-171">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="f06f2-171">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="f06f2-172">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="f06f2-172">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="f06f2-173">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="f06f2-173">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="f06f2-174">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="f06f2-174">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="f06f2-175">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="f06f2-175">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="f06f2-176">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f06f2-176">OUTPUTS</span></span>

### <span data-ttu-id="f06f2-177">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="f06f2-177">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="f06f2-178">Microsoft.Azure.Commands.ExceptionsDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="f06f2-178">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="f06f2-179">NOTE</span><span class="sxs-lookup"><span data-stu-id="f06f2-179">NOTES</span></span>

## <span data-ttu-id="f06f2-180">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f06f2-180">RELATED LINKS</span></span>
