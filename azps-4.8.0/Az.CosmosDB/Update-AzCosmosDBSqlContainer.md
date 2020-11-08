---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 85f220c7745f28a2786e9a26edc86baa129c3c3c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94193032"
---
# <span data-ttu-id="e38a5-101">Update-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="e38a5-101">Update-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="e38a5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e38a5-102">SYNOPSIS</span></span>
<span data-ttu-id="e38a5-103">Aggiorna il contenitore SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="e38a5-103">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="e38a5-104">Esegue un'operazione di patch lato client leggendo il contenitore esistente.</span><span class="sxs-lookup"><span data-stu-id="e38a5-104">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="e38a5-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e38a5-105">SYNTAX</span></span>

### <span data-ttu-id="e38a5-106">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e38a5-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e38a5-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e38a5-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainer [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] -ParentObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e38a5-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e38a5-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainer [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e38a5-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e38a5-109">DESCRIPTION</span></span>
<span data-ttu-id="e38a5-110">Aggiorna il contenitore SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="e38a5-110">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="e38a5-111">Esegue un'operazione di patch lato client leggendo il contenitore esistente.</span><span class="sxs-lookup"><span data-stu-id="e38a5-111">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="e38a5-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e38a5-112">EXAMPLES</span></span>

### <span data-ttu-id="e38a5-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e38a5-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 800

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="e38a5-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e38a5-114">PARAMETERS</span></span>

### <span data-ttu-id="e38a5-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e38a5-115">-AccountName</span></span>
<span data-ttu-id="e38a5-116">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="e38a5-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e38a5-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="e38a5-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="e38a5-118">Valore massimo della velocità effettiva se autoscale è abilitato.</span><span class="sxs-lookup"><span data-stu-id="e38a5-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="e38a5-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e38a5-119">-Confirm</span></span>
<span data-ttu-id="e38a5-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e38a5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e38a5-121">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="e38a5-121">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="e38a5-122">Oggetto ConflictResolutionPolicy di tipo PSSqlConflictResolutionPolicy, se specificato, viene impostato come ConflictResolutionPolicy del contenitore.</span><span class="sxs-lookup"><span data-stu-id="e38a5-122">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="e38a5-123">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="e38a5-123">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="e38a5-124">Possono avere i valori: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="e38a5-124">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="e38a5-125">Se specificato insieme al parametro ConflictResolutionPolicy, viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="e38a5-125">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="e38a5-126">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="e38a5-126">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="e38a5-127">Da fornire quando il tipo è LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="e38a5-127">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="e38a5-128">Se specificato insieme al parametro ConflictResolutionPolicy, viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="e38a5-128">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="e38a5-129">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="e38a5-129">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="e38a5-130">Da fornire quando il tipo è personalizzato.</span><span class="sxs-lookup"><span data-stu-id="e38a5-130">To be provided when the type is custom.</span></span>
<span data-ttu-id="e38a5-131">Se specificato insieme al parametro ConflictResolutionPolicy, viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="e38a5-131">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="e38a5-132">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e38a5-132">-DatabaseName</span></span>
<span data-ttu-id="e38a5-133">Nome database.</span><span class="sxs-lookup"><span data-stu-id="e38a5-133">Database name.</span></span>

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

### <span data-ttu-id="e38a5-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e38a5-134">-DefaultProfile</span></span>
<span data-ttu-id="e38a5-135">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e38a5-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e38a5-136">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="e38a5-136">-IndexingPolicy</span></span>
<span data-ttu-id="e38a5-137">Oggetto Criteri di indicizzazione di tipo Microsoft. Azure. Commands. CosmosDB. PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="e38a5-137">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="e38a5-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e38a5-138">-InputObject</span></span>
<span data-ttu-id="e38a5-139">Oggetto contenitore SQL.</span><span class="sxs-lookup"><span data-stu-id="e38a5-139">Sql Container object.</span></span>

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

### <span data-ttu-id="e38a5-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="e38a5-140">-Name</span></span>
<span data-ttu-id="e38a5-141">Nome contenitore.</span><span class="sxs-lookup"><span data-stu-id="e38a5-141">Container name.</span></span>

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

### <span data-ttu-id="e38a5-142">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e38a5-142">-ParentObject</span></span>
<span data-ttu-id="e38a5-143">Oggetto database SQL.</span><span class="sxs-lookup"><span data-stu-id="e38a5-143">Sql Database object.</span></span>

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

### <span data-ttu-id="e38a5-144">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="e38a5-144">-PartitionKeyKind</span></span>
<span data-ttu-id="e38a5-145">Il tipo di algoritmo usato per il partizionamento.</span><span class="sxs-lookup"><span data-stu-id="e38a5-145">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="e38a5-146">I valori possibili includono: "hash", "range"</span><span class="sxs-lookup"><span data-stu-id="e38a5-146">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="e38a5-147">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="e38a5-147">-PartitionKeyPath</span></span>
<span data-ttu-id="e38a5-148">Percorso della chiave di partizione, ad esempio, "/Address/ZipCode".</span><span class="sxs-lookup"><span data-stu-id="e38a5-148">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="e38a5-149">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="e38a5-149">-PartitionKeyVersion</span></span>
<span data-ttu-id="e38a5-150">La versione della definizione della chiave di partizione</span><span class="sxs-lookup"><span data-stu-id="e38a5-150">The version of the partition key definition</span></span>

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

### <span data-ttu-id="e38a5-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e38a5-151">-ResourceGroupName</span></span>
<span data-ttu-id="e38a5-152">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e38a5-152">Name of resource group.</span></span>

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

### <span data-ttu-id="e38a5-153">-Throughput</span><span class="sxs-lookup"><span data-stu-id="e38a5-153">-Throughput</span></span>
<span data-ttu-id="e38a5-154">La velocità effettiva del contenitore SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="e38a5-154">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="e38a5-155">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="e38a5-155">Default value is 400.</span></span>

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

### <span data-ttu-id="e38a5-156">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="e38a5-156">-TtlInSeconds</span></span>
<span data-ttu-id="e38a5-157">TTL predefinito in secondi.</span><span class="sxs-lookup"><span data-stu-id="e38a5-157">Default Ttl in seconds.</span></span>
<span data-ttu-id="e38a5-158">Se il valore è mancante o è impostato su-1, gli elementi non scadono.</span><span class="sxs-lookup"><span data-stu-id="e38a5-158">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="e38a5-159">Se il valore è impostato su n, gli elementi scadranno n secondi dopo l'ultima modifica dell'ora.</span><span class="sxs-lookup"><span data-stu-id="e38a5-159">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="e38a5-160">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="e38a5-160">-UniqueKeyPolicy</span></span>
<span data-ttu-id="e38a5-161">Oggetto UniqueKeyPolicy di tipo Microsoft. Azure. Commands. CosmosDB. PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="e38a5-161">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="e38a5-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e38a5-162">-WhatIf</span></span>
<span data-ttu-id="e38a5-163">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e38a5-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e38a5-164">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e38a5-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e38a5-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e38a5-165">CommonParameters</span></span>
<span data-ttu-id="e38a5-166">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e38a5-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e38a5-167">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e38a5-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e38a5-168">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e38a5-168">INPUTS</span></span>

### <span data-ttu-id="e38a5-169">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="e38a5-169">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="e38a5-170">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="e38a5-170">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="e38a5-171">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="e38a5-171">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="e38a5-172">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="e38a5-172">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="e38a5-173">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="e38a5-173">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="e38a5-174">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e38a5-174">OUTPUTS</span></span>

### <span data-ttu-id="e38a5-175">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="e38a5-175">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="e38a5-176">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="e38a5-176">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="e38a5-177">Note</span><span class="sxs-lookup"><span data-stu-id="e38a5-177">NOTES</span></span>

## <span data-ttu-id="e38a5-178">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e38a5-178">RELATED LINKS</span></span>
