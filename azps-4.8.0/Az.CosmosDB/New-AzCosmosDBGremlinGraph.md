---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: ab81c97048c64a08ab29877becfd44b690312a27
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190828"
---
# <span data-ttu-id="90ee6-101">New-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="90ee6-101">New-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="90ee6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="90ee6-102">SYNOPSIS</span></span>
<span data-ttu-id="90ee6-103">Crea un nuovo grafico di CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="90ee6-103">Creates a new CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="90ee6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="90ee6-104">SYNTAX</span></span>

### <span data-ttu-id="90ee6-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="90ee6-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String>
 -PartitionKeyPath <String[]> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90ee6-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="90ee6-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBGremlinGraph -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSConflictResolutionPolicy>]
 -ParentObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="90ee6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="90ee6-107">DESCRIPTION</span></span>
<span data-ttu-id="90ee6-108">Crea un nuovo grafico di CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="90ee6-108">Creates a new CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="90ee6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="90ee6-109">EXAMPLES</span></span>

### <span data-ttu-id="90ee6-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="90ee6-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinGraph -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName/graphs/myGraphName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

## <span data-ttu-id="90ee6-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="90ee6-111">PARAMETERS</span></span>

### <span data-ttu-id="90ee6-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="90ee6-112">-AccountName</span></span>
<span data-ttu-id="90ee6-113">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="90ee6-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="90ee6-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="90ee6-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="90ee6-115">Valore massimo della velocità effettiva se autoscale è abilitato.</span><span class="sxs-lookup"><span data-stu-id="90ee6-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="90ee6-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="90ee6-116">-Confirm</span></span>
<span data-ttu-id="90ee6-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90ee6-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90ee6-118">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="90ee6-118">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="90ee6-119">Oggetto ConflictResolutionPolicy di tipo PSConflictResolutionPolicy, se specificato, viene impostato come ConflictResolutionPolicy del contenitore.</span><span class="sxs-lookup"><span data-stu-id="90ee6-119">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="90ee6-120">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="90ee6-120">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="90ee6-121">Possono avere i valori: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="90ee6-121">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="90ee6-122">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="90ee6-122">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="90ee6-123">Da fornire quando il tipo è LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="90ee6-123">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="90ee6-124">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="90ee6-124">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="90ee6-125">Da fornire quando il tipo è personalizzato.</span><span class="sxs-lookup"><span data-stu-id="90ee6-125">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="90ee6-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="90ee6-126">-DatabaseName</span></span>
<span data-ttu-id="90ee6-127">Nome database.</span><span class="sxs-lookup"><span data-stu-id="90ee6-127">Database name.</span></span>

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

### <span data-ttu-id="90ee6-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90ee6-128">-DefaultProfile</span></span>
<span data-ttu-id="90ee6-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="90ee6-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90ee6-130">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="90ee6-130">-IndexingPolicy</span></span>
<span data-ttu-id="90ee6-131">Oggetto Criteri di indicizzazione di tipo Microsoft. Azure. Commands. CosmosDB. PSIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="90ee6-131">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span></span>

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

### <span data-ttu-id="90ee6-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="90ee6-132">-Name</span></span>
<span data-ttu-id="90ee6-133">Nome del grafico Gremlin.</span><span class="sxs-lookup"><span data-stu-id="90ee6-133">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="90ee6-134">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="90ee6-134">-ParentObject</span></span>
<span data-ttu-id="90ee6-135">Oggetto database Gremlin.</span><span class="sxs-lookup"><span data-stu-id="90ee6-135">Gremlin Database object.</span></span>

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

### <span data-ttu-id="90ee6-136">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="90ee6-136">-PartitionKeyKind</span></span>
<span data-ttu-id="90ee6-137">Il tipo di algoritmo usato per il partizionamento.</span><span class="sxs-lookup"><span data-stu-id="90ee6-137">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="90ee6-138">I valori possibili includono: "hash", "range"</span><span class="sxs-lookup"><span data-stu-id="90ee6-138">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="90ee6-139">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="90ee6-139">-PartitionKeyPath</span></span>
<span data-ttu-id="90ee6-140">Percorso della chiave di partizione, ad esempio, "/Address/ZipCode".</span><span class="sxs-lookup"><span data-stu-id="90ee6-140">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="90ee6-141">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="90ee6-141">-PartitionKeyVersion</span></span>
<span data-ttu-id="90ee6-142">La versione della definizione della chiave di partizione</span><span class="sxs-lookup"><span data-stu-id="90ee6-142">The version of the partition key definition</span></span>

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

### <span data-ttu-id="90ee6-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90ee6-143">-ResourceGroupName</span></span>
<span data-ttu-id="90ee6-144">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="90ee6-144">Name of resource group.</span></span>

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

### <span data-ttu-id="90ee6-145">-Throughput</span><span class="sxs-lookup"><span data-stu-id="90ee6-145">-Throughput</span></span>
<span data-ttu-id="90ee6-146">La velocità effettiva del grafico Gremlin (RU/s).</span><span class="sxs-lookup"><span data-stu-id="90ee6-146">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="90ee6-147">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="90ee6-147">Default value is 400.</span></span>

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

### <span data-ttu-id="90ee6-148">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="90ee6-148">-TtlInSeconds</span></span>
<span data-ttu-id="90ee6-149">TTL predefinito in secondi.</span><span class="sxs-lookup"><span data-stu-id="90ee6-149">Default Ttl in seconds.</span></span>
<span data-ttu-id="90ee6-150">Se il valore è mancante o è impostato su-1, gli elementi non scadono.</span><span class="sxs-lookup"><span data-stu-id="90ee6-150">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="90ee6-151">Se il valore è impostato su n, gli elementi scadranno n secondi dopo l'ultima modifica dell'ora.</span><span class="sxs-lookup"><span data-stu-id="90ee6-151">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="90ee6-152">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="90ee6-152">-UniqueKeyPolicy</span></span>
<span data-ttu-id="90ee6-153">Oggetto UniqueKeyPolicy di tipo Microsoft. Azure. Commands. CosmosDB. PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="90ee6-153">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="90ee6-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90ee6-154">-WhatIf</span></span>
<span data-ttu-id="90ee6-155">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="90ee6-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90ee6-156">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="90ee6-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90ee6-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90ee6-157">CommonParameters</span></span>
<span data-ttu-id="90ee6-158">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90ee6-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90ee6-159">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90ee6-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90ee6-160">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="90ee6-160">INPUTS</span></span>

### <span data-ttu-id="90ee6-161">Microsoft. Azure. Commands. CosmosDB. Models. PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="90ee6-161">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="90ee6-162">Microsoft. Azure. Commands. CosmosDB. Models. PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="90ee6-162">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="90ee6-163">Microsoft. Azure. Commands. CosmosDB. Models. PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="90ee6-163">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

### <span data-ttu-id="90ee6-164">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="90ee6-164">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="90ee6-165">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="90ee6-165">OUTPUTS</span></span>

### <span data-ttu-id="90ee6-166">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="90ee6-166">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="90ee6-167">System. Exception</span><span class="sxs-lookup"><span data-stu-id="90ee6-167">System.Exception</span></span>

## <span data-ttu-id="90ee6-168">Note</span><span class="sxs-lookup"><span data-stu-id="90ee6-168">NOTES</span></span>

## <span data-ttu-id="90ee6-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="90ee6-169">RELATED LINKS</span></span>