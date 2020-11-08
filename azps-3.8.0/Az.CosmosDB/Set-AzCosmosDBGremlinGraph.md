---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: a8ccb3757786ca76fff15b1bf68d8dc7b477ebcc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022396"
---
# <span data-ttu-id="51625-101">Set-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="51625-101">Set-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="51625-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="51625-102">SYNOPSIS</span></span>
<span data-ttu-id="51625-103">Imposta il grafico CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="51625-103">Sets the CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="51625-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="51625-104">SYNTAX</span></span>

### <span data-ttu-id="51625-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="51625-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String>
 -PartitionKeyPath <String[]> [-Throughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51625-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="51625-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBGremlinGraph -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -InputObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51625-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="51625-107">DESCRIPTION</span></span>
<span data-ttu-id="51625-108">Il cmdlet **set-AzCosmosDBGremlinGraph** imposta un grafico Gremlin di CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="51625-108">The **Set-AzCosmosDBGremlinGraph** cmdlet sets a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="51625-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="51625-109">EXAMPLES</span></span>

### <span data-ttu-id="51625-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="51625-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName} -PartitionKeyPath {path}

Name        Id    Resource
----        --    -------
{name}     {id}   Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

<span data-ttu-id="51625-111">Oggetto Resource contiene IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="51625-111">Resource Object contains IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span></span>

## <span data-ttu-id="51625-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="51625-112">PARAMETERS</span></span>

### <span data-ttu-id="51625-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="51625-113">-AccountName</span></span>
<span data-ttu-id="51625-114">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="51625-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="51625-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="51625-115">-Confirm</span></span>
<span data-ttu-id="51625-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51625-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51625-117">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="51625-117">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="51625-118">Oggetto ConflictResolutionPolicy di tipo PSConflictResolutionPolicy, se specificato, viene impostato come ConflictResolutionPolicy del contenitore.</span><span class="sxs-lookup"><span data-stu-id="51625-118">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

```yaml
Type: PSConflictResolutionPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51625-119">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="51625-119">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="51625-120">Possono avere i valori: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="51625-120">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="51625-121">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="51625-121">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="51625-122">Da fornire quando il tipo è LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="51625-122">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="51625-123">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="51625-123">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="51625-124">Da fornire quando il tipo è personalizzato.</span><span class="sxs-lookup"><span data-stu-id="51625-124">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="51625-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="51625-125">-DatabaseName</span></span>
<span data-ttu-id="51625-126">Nome database.</span><span class="sxs-lookup"><span data-stu-id="51625-126">Database name.</span></span>

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

### <span data-ttu-id="51625-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51625-127">-DefaultProfile</span></span>
<span data-ttu-id="51625-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="51625-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51625-129">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="51625-129">-IndexingPolicy</span></span>
<span data-ttu-id="51625-130">Oggetto Criteri di indicizzazione di tipo Microsoft. Azure. Commands. CosmosDB. PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="51625-130">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

```yaml
Type: PSIndexingPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51625-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51625-131">-InputObject</span></span>
<span data-ttu-id="51625-132">Oggetto database Gremlin.</span><span class="sxs-lookup"><span data-stu-id="51625-132">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51625-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="51625-133">-Name</span></span>
<span data-ttu-id="51625-134">Nome del grafico Gremlin.</span><span class="sxs-lookup"><span data-stu-id="51625-134">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="51625-135">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="51625-135">-PartitionKeyKind</span></span>
<span data-ttu-id="51625-136">Il tipo di algoritmo usato per il partizionamento.</span><span class="sxs-lookup"><span data-stu-id="51625-136">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="51625-137">I valori possibili includono: "hash", "range"</span><span class="sxs-lookup"><span data-stu-id="51625-137">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="51625-138">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="51625-138">-PartitionKeyPath</span></span>
<span data-ttu-id="51625-139">Percorso della chiave di partizione, ad esempio, "/Address/ZipCode".</span><span class="sxs-lookup"><span data-stu-id="51625-139">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="51625-140">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="51625-140">-PartitionKeyVersion</span></span>
<span data-ttu-id="51625-141">La versione della definizione della chiave di partizione</span><span class="sxs-lookup"><span data-stu-id="51625-141">The version of the partition key definition</span></span>

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

### <span data-ttu-id="51625-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51625-142">-ResourceGroupName</span></span>
<span data-ttu-id="51625-143">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="51625-143">Name of resource group.</span></span>

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

### <span data-ttu-id="51625-144">-Throughput</span><span class="sxs-lookup"><span data-stu-id="51625-144">-Throughput</span></span>
<span data-ttu-id="51625-145">La velocità effettiva del grafico Gremlin (RU/s).</span><span class="sxs-lookup"><span data-stu-id="51625-145">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="51625-146">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="51625-146">Default value is 400.</span></span>

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

### <span data-ttu-id="51625-147">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="51625-147">-TtlInSeconds</span></span>
<span data-ttu-id="51625-148">TTL predefinito in secondi.</span><span class="sxs-lookup"><span data-stu-id="51625-148">Default Ttl in seconds.</span></span>
<span data-ttu-id="51625-149">Se il valore è mancante o è impostato su-1, gli elementi non scadono.</span><span class="sxs-lookup"><span data-stu-id="51625-149">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="51625-150">Se il valore è impostato su n, gli elementi scadranno n secondi dopo l'ultima modifica dell'ora.</span><span class="sxs-lookup"><span data-stu-id="51625-150">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="51625-151">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="51625-151">-UniqueKeyPolicy</span></span>
<span data-ttu-id="51625-152">Oggetto UniqueKeyPolicy di tipo Microsoft. Azure. Commands. CosmosDB. PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="51625-152">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

```yaml
Type: PSUniqueKeyPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51625-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51625-153">-WhatIf</span></span>
<span data-ttu-id="51625-154">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="51625-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51625-155">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="51625-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51625-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51625-156">CommonParameters</span></span>
<span data-ttu-id="51625-157">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51625-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51625-158">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51625-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51625-159">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="51625-159">INPUTS</span></span>

### <span data-ttu-id="51625-160">Microsoft. Azure. Commands. CosmosDB. Models. PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="51625-160">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="51625-161">Microsoft. Azure. Commands. CosmosDB. Models. PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="51625-161">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="51625-162">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="51625-162">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="51625-163">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="51625-163">OUTPUTS</span></span>

### <span data-ttu-id="51625-164">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="51625-164">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="51625-165">Note</span><span class="sxs-lookup"><span data-stu-id="51625-165">NOTES</span></span>

## <span data-ttu-id="51625-166">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="51625-166">RELATED LINKS</span></span>
