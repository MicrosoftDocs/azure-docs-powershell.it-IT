---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: ab81c97048c64a08ab29877becfd44b690312a27
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196830"
---
# <span data-ttu-id="f66c4-101">New-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="f66c4-101">New-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="f66c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f66c4-102">SYNOPSIS</span></span>
<span data-ttu-id="f66c4-103">Crea un nuovo diagramma di Gremlindb.</span><span class="sxs-lookup"><span data-stu-id="f66c4-103">Creates a new CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="f66c4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f66c4-104">SYNTAX</span></span>

### <span data-ttu-id="f66c4-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f66c4-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String>
 -PartitionKeyPath <String[]> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f66c4-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f66c4-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBGremlinGraph -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSConflictResolutionPolicy>]
 -ParentObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f66c4-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f66c4-107">DESCRIPTION</span></span>
<span data-ttu-id="f66c4-108">Crea un nuovo diagramma di Gremlindb.</span><span class="sxs-lookup"><span data-stu-id="f66c4-108">Creates a new CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="f66c4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f66c4-109">EXAMPLES</span></span>

### <span data-ttu-id="f66c4-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f66c4-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinGraph -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName/graphs/myGraphName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

## <span data-ttu-id="f66c4-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f66c4-111">PARAMETERS</span></span>

### <span data-ttu-id="f66c4-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f66c4-112">-AccountName</span></span>
<span data-ttu-id="f66c4-113">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="f66c4-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f66c4-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="f66c4-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="f66c4-115">Valore massimo di velocità effettiva se è abilitata la scalabilità automatica.</span><span class="sxs-lookup"><span data-stu-id="f66c4-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="f66c4-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f66c4-116">-Confirm</span></span>
<span data-ttu-id="f66c4-117">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f66c4-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f66c4-118">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="f66c4-118">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="f66c4-119">Oggetto ConflictResolutionPolicy di tipo PSConflictResolutionPolicy, quando specificato è impostato come ConflictResolutionPolicy del contenitore.</span><span class="sxs-lookup"><span data-stu-id="f66c4-119">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="f66c4-120">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="f66c4-120">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="f66c4-121">Possono contenere i valori: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="f66c4-121">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="f66c4-122">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="f66c4-122">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="f66c4-123">Da immettere quando il tipo è LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="f66c4-123">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="f66c4-124">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="f66c4-124">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="f66c4-125">Da immettere quando il tipo è personalizzato.</span><span class="sxs-lookup"><span data-stu-id="f66c4-125">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="f66c4-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f66c4-126">-DatabaseName</span></span>
<span data-ttu-id="f66c4-127">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="f66c4-127">Database name.</span></span>

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

### <span data-ttu-id="f66c4-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f66c4-128">-DefaultProfile</span></span>
<span data-ttu-id="f66c4-129">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f66c4-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f66c4-130">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="f66c4-130">-IndexingPolicy</span></span>
<span data-ttu-id="f66c4-131">Oggetto criterio di indicizzazione di tipo Microsoft.Azure.Commands.MoltosDB.PSIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="f66c4-131">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span></span>

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

### <span data-ttu-id="f66c4-132">-Name</span><span class="sxs-lookup"><span data-stu-id="f66c4-132">-Name</span></span>
<span data-ttu-id="f66c4-133">Nome del grafo Gremlin.</span><span class="sxs-lookup"><span data-stu-id="f66c4-133">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="f66c4-134">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f66c4-134">-ParentObject</span></span>
<span data-ttu-id="f66c4-135">Oggetto di database Gremlin.</span><span class="sxs-lookup"><span data-stu-id="f66c4-135">Gremlin Database object.</span></span>

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

### <span data-ttu-id="f66c4-136">-PartitionKey Rieti</span><span class="sxs-lookup"><span data-stu-id="f66c4-136">-PartitionKeyKind</span></span>
<span data-ttu-id="f66c4-137">Il tipo di algoritmo usato per il partizionamento.</span><span class="sxs-lookup"><span data-stu-id="f66c4-137">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="f66c4-138">I valori possibili includono: 'Hash', 'Range'</span><span class="sxs-lookup"><span data-stu-id="f66c4-138">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="f66c4-139">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="f66c4-139">-PartitionKeyPath</span></span>
<span data-ttu-id="f66c4-140">Percorso chiave di partizione, ad esempio '/address/zipcode'.</span><span class="sxs-lookup"><span data-stu-id="f66c4-140">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="f66c4-141">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="f66c4-141">-PartitionKeyVersion</span></span>
<span data-ttu-id="f66c4-142">Versione della definizione della chiave di partizione</span><span class="sxs-lookup"><span data-stu-id="f66c4-142">The version of the partition key definition</span></span>

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

### <span data-ttu-id="f66c4-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f66c4-143">-ResourceGroupName</span></span>
<span data-ttu-id="f66c4-144">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f66c4-144">Name of resource group.</span></span>

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

### <span data-ttu-id="f66c4-145">-Velocità effettiva</span><span class="sxs-lookup"><span data-stu-id="f66c4-145">-Throughput</span></span>
<span data-ttu-id="f66c4-146">Velocità effettiva di Gremlin Graph (RU/s).</span><span class="sxs-lookup"><span data-stu-id="f66c4-146">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="f66c4-147">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="f66c4-147">Default value is 400.</span></span>

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

### <span data-ttu-id="f66c4-148">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="f66c4-148">-TtlInSeconds</span></span>
<span data-ttu-id="f66c4-149">Ttl predefinito in secondi.</span><span class="sxs-lookup"><span data-stu-id="f66c4-149">Default Ttl in seconds.</span></span>
<span data-ttu-id="f66c4-150">Se il valore manca o è impostato su -1, gli elementi non scadono.</span><span class="sxs-lookup"><span data-stu-id="f66c4-150">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="f66c4-151">Se il valore è impostato su n, gli elementi scadranno n secondi dopo l'ora dell'ultima modifica.</span><span class="sxs-lookup"><span data-stu-id="f66c4-151">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="f66c4-152">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="f66c4-152">-UniqueKeyPolicy</span></span>
<span data-ttu-id="f66c4-153">Oggetto UniqueKeyPolicy di tipo Microsoft.Azure.Commands.ChancesDB.PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="f66c4-153">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="f66c4-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f66c4-154">-WhatIf</span></span>
<span data-ttu-id="f66c4-155">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f66c4-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f66c4-156">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f66c4-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f66c4-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f66c4-157">CommonParameters</span></span>
<span data-ttu-id="f66c4-158">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f66c4-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f66c4-159">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f66c4-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f66c4-160">INPUT</span><span class="sxs-lookup"><span data-stu-id="f66c4-160">INPUTS</span></span>

### <span data-ttu-id="f66c4-161">Microsoft.Azure.Commands.EnterpriseDb.Models.PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="f66c4-161">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="f66c4-162">Microsoft.Azure.Commands.ChancesDB.Models.PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="f66c4-162">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="f66c4-163">Microsoft.Azure.Commands.FerenzasDB.Models.PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="f66c4-163">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

### <span data-ttu-id="f66c4-164">Microsoft.Azure.Commands.EnterpriseDb.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="f66c4-164">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="f66c4-165">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f66c4-165">OUTPUTS</span></span>

### <span data-ttu-id="f66c4-166">Microsoft.Azure.Commands.EnterpriseDb.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="f66c4-166">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="f66c4-167">System.Exception</span><span class="sxs-lookup"><span data-stu-id="f66c4-167">System.Exception</span></span>

## <span data-ttu-id="f66c4-168">NOTE</span><span class="sxs-lookup"><span data-stu-id="f66c4-168">NOTES</span></span>

## <span data-ttu-id="f66c4-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f66c4-169">RELATED LINKS</span></span>
