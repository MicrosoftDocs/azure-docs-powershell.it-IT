---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: b69640eb2af37ce0ef48ca3841c3cadcc0c3a57b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94193035"
---
# <span data-ttu-id="cd960-101">Update-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="cd960-101">Update-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="cd960-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cd960-102">SYNOPSIS</span></span>
<span data-ttu-id="cd960-103">Aggiorna il grafico Gremlin di CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="cd960-103">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="cd960-104">Esegue un'operazione di patch lato client leggendo il grafico esistente.</span><span class="sxs-lookup"><span data-stu-id="cd960-104">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="cd960-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cd960-105">SYNTAX</span></span>

### <span data-ttu-id="cd960-106">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cd960-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd960-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd960-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd960-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd960-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -InputObject <PSGremlinGraphGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd960-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd960-109">DESCRIPTION</span></span>
<span data-ttu-id="cd960-110">Aggiorna il grafico Gremlin di CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="cd960-110">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="cd960-111">Esegue un'operazione di patch lato client leggendo il grafico esistente.</span><span class="sxs-lookup"><span data-stu-id="cd960-111">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="cd960-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cd960-112">EXAMPLES</span></span>

### <span data-ttu-id="cd960-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cd960-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraph -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -Throughput updatedThroughputValue

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName/graphs/myGraphName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

## <span data-ttu-id="cd960-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cd960-114">PARAMETERS</span></span>

### <span data-ttu-id="cd960-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cd960-115">-AccountName</span></span>
<span data-ttu-id="cd960-116">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="cd960-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="cd960-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="cd960-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="cd960-118">Valore massimo della velocità effettiva se autoscale è abilitato.</span><span class="sxs-lookup"><span data-stu-id="cd960-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="cd960-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cd960-119">-Confirm</span></span>
<span data-ttu-id="cd960-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd960-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd960-121">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="cd960-121">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="cd960-122">Oggetto ConflictResolutionPolicy di tipo PSConflictResolutionPolicy, se specificato, viene impostato come ConflictResolutionPolicy del contenitore.</span><span class="sxs-lookup"><span data-stu-id="cd960-122">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="cd960-123">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="cd960-123">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="cd960-124">Possono avere i valori: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="cd960-124">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="cd960-125">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="cd960-125">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="cd960-126">Da fornire quando il tipo è LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="cd960-126">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="cd960-127">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="cd960-127">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="cd960-128">Da fornire quando il tipo è personalizzato.</span><span class="sxs-lookup"><span data-stu-id="cd960-128">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="cd960-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cd960-129">-DatabaseName</span></span>
<span data-ttu-id="cd960-130">Nome database.</span><span class="sxs-lookup"><span data-stu-id="cd960-130">Database name.</span></span>

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

### <span data-ttu-id="cd960-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd960-131">-DefaultProfile</span></span>
<span data-ttu-id="cd960-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cd960-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd960-133">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="cd960-133">-IndexingPolicy</span></span>
<span data-ttu-id="cd960-134">Oggetto Criteri di indicizzazione di tipo Microsoft. Azure. Commands. CosmosDB. PSIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="cd960-134">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span></span>

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

### <span data-ttu-id="cd960-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd960-135">-InputObject</span></span>
<span data-ttu-id="cd960-136">Oggetto grafico Gremlin.</span><span class="sxs-lookup"><span data-stu-id="cd960-136">Gremlin Graph object.</span></span>

```yaml
Type: PSGremlinGraphGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd960-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="cd960-137">-Name</span></span>
<span data-ttu-id="cd960-138">Nome del grafico Gremlin.</span><span class="sxs-lookup"><span data-stu-id="cd960-138">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="cd960-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="cd960-139">-ParentObject</span></span>
<span data-ttu-id="cd960-140">Oggetto database Gremlin.</span><span class="sxs-lookup"><span data-stu-id="cd960-140">Gremlin Database object.</span></span>

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

### <span data-ttu-id="cd960-141">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="cd960-141">-PartitionKeyKind</span></span>
<span data-ttu-id="cd960-142">Il tipo di algoritmo usato per il partizionamento.</span><span class="sxs-lookup"><span data-stu-id="cd960-142">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="cd960-143">I valori possibili includono: "hash", "range"</span><span class="sxs-lookup"><span data-stu-id="cd960-143">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="cd960-144">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="cd960-144">-PartitionKeyPath</span></span>
<span data-ttu-id="cd960-145">Percorso della chiave di partizione, ad esempio, "/Address/ZipCode".</span><span class="sxs-lookup"><span data-stu-id="cd960-145">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="cd960-146">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="cd960-146">-PartitionKeyVersion</span></span>
<span data-ttu-id="cd960-147">La versione della definizione della chiave di partizione</span><span class="sxs-lookup"><span data-stu-id="cd960-147">The version of the partition key definition</span></span>

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

### <span data-ttu-id="cd960-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd960-148">-ResourceGroupName</span></span>
<span data-ttu-id="cd960-149">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cd960-149">Name of resource group.</span></span>

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

### <span data-ttu-id="cd960-150">-Throughput</span><span class="sxs-lookup"><span data-stu-id="cd960-150">-Throughput</span></span>
<span data-ttu-id="cd960-151">La velocità effettiva del grafico Gremlin (RU/s).</span><span class="sxs-lookup"><span data-stu-id="cd960-151">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="cd960-152">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="cd960-152">Default value is 400.</span></span>

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

### <span data-ttu-id="cd960-153">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="cd960-153">-TtlInSeconds</span></span>
<span data-ttu-id="cd960-154">TTL predefinito in secondi.</span><span class="sxs-lookup"><span data-stu-id="cd960-154">Default Ttl in seconds.</span></span>
<span data-ttu-id="cd960-155">Se il valore è mancante o è impostato su-1, gli elementi non scadono.</span><span class="sxs-lookup"><span data-stu-id="cd960-155">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="cd960-156">Se il valore è impostato su n, gli elementi scadranno n secondi dopo l'ultima modifica dell'ora.</span><span class="sxs-lookup"><span data-stu-id="cd960-156">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="cd960-157">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="cd960-157">-UniqueKeyPolicy</span></span>
<span data-ttu-id="cd960-158">Oggetto UniqueKeyPolicy di tipo Microsoft. Azure. Commands. CosmosDB. PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="cd960-158">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="cd960-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd960-159">-WhatIf</span></span>
<span data-ttu-id="cd960-160">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd960-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd960-161">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd960-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd960-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd960-162">CommonParameters</span></span>
<span data-ttu-id="cd960-163">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd960-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd960-164">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd960-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd960-165">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cd960-165">INPUTS</span></span>

### <span data-ttu-id="cd960-166">Microsoft. Azure. Commands. CosmosDB. Models. PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="cd960-166">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="cd960-167">Microsoft. Azure. Commands. CosmosDB. Models. PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="cd960-167">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="cd960-168">Microsoft. Azure. Commands. CosmosDB. Models. PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="cd960-168">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

### <span data-ttu-id="cd960-169">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="cd960-169">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="cd960-170">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="cd960-170">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="cd960-171">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cd960-171">OUTPUTS</span></span>

### <span data-ttu-id="cd960-172">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="cd960-172">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="cd960-173">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="cd960-173">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="cd960-174">Note</span><span class="sxs-lookup"><span data-stu-id="cd960-174">NOTES</span></span>

## <span data-ttu-id="cd960-175">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cd960-175">RELATED LINKS</span></span>
