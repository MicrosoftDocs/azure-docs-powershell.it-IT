---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: b69640eb2af37ce0ef48ca3841c3cadcc0c3a57b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181263"
---
# <span data-ttu-id="f7fd2-101">Update-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="f7fd2-101">Update-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="f7fd2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7fd2-102">SYNOPSIS</span></span>
<span data-ttu-id="f7fd2-103">Aggiorna il diagramma di Gremlin diDb.</span><span class="sxs-lookup"><span data-stu-id="f7fd2-103">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="f7fd2-104">Esegue un'operazione di patch sul lato client leggendo il grafico esistente.</span><span class="sxs-lookup"><span data-stu-id="f7fd2-104">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="f7fd2-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f7fd2-105">SYNTAX</span></span>

### <span data-ttu-id="f7fd2-106">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f7fd2-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7fd2-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7fd2-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7fd2-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7fd2-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -InputObject <PSGremlinGraphGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7fd2-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f7fd2-109">DESCRIPTION</span></span>
<span data-ttu-id="f7fd2-110">Aggiorna il diagramma di Gremlin diDb.</span><span class="sxs-lookup"><span data-stu-id="f7fd2-110">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="f7fd2-111">Esegue un'operazione di patch sul lato client leggendo il grafico esistente.</span><span class="sxs-lookup"><span data-stu-id="f7fd2-111">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="f7fd2-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f7fd2-112">EXAMPLES</span></span>

### <span data-ttu-id="f7fd2-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f7fd2-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraph -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -Throughput updatedThroughputValue

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName/graphs/myGraphName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

## <span data-ttu-id="f7fd2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7fd2-114">PARAMETERS</span></span>

### <span data-ttu-id="f7fd2-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f7fd2-115">-AccountName</span></span>
<span data-ttu-id="f7fd2-116">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="f7fd2-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f7fd2-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="f7fd2-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="f7fd2-118">Valore massimo di velocità effettiva se è abilitata la scalabilità automatica.</span><span class="sxs-lookup"><span data-stu-id="f7fd2-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="f7fd2-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7fd2-119">-Confirm</span></span>
<span data-ttu-id="f7fd2-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7fd2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7fd2-121">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="f7fd2-121">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="f7fd2-122">Oggetto ConflictResolutionPolicy di tipo PSConflictResolutionPolicy, quando specificato è impostato come ConflictResolutionPolicy del contenitore.</span><span class="sxs-lookup"><span data-stu-id="f7fd2-122">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="f7fd2-123">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="f7fd2-123">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="f7fd2-124">Possono contenere i valori: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="f7fd2-124">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="f7fd2-125">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="f7fd2-125">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="f7fd2-126">Da immettere quando il tipo è LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="f7fd2-126">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="f7fd2-127">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="f7fd2-127">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="f7fd2-128">Da immettere quando il tipo è personalizzato.</span><span class="sxs-lookup"><span data-stu-id="f7fd2-128">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="f7fd2-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f7fd2-129">-DatabaseName</span></span>
<span data-ttu-id="f7fd2-130">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="f7fd2-130">Database name.</span></span>

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

### <span data-ttu-id="f7fd2-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7fd2-131">-DefaultProfile</span></span>
<span data-ttu-id="f7fd2-132">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f7fd2-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7fd2-133">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="f7fd2-133">-IndexingPolicy</span></span>
<span data-ttu-id="f7fd2-134">Oggetto criterio di indicizzazione di tipo Microsoft.Azure.Commands.MoltosDB.PSIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="f7fd2-134">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span></span>

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

### <span data-ttu-id="f7fd2-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7fd2-135">-InputObject</span></span>
<span data-ttu-id="f7fd2-136">Oggetto Gremlin Graph.</span><span class="sxs-lookup"><span data-stu-id="f7fd2-136">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="f7fd2-137">-Name</span><span class="sxs-lookup"><span data-stu-id="f7fd2-137">-Name</span></span>
<span data-ttu-id="f7fd2-138">Nome del grafo Gremlin.</span><span class="sxs-lookup"><span data-stu-id="f7fd2-138">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="f7fd2-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f7fd2-139">-ParentObject</span></span>
<span data-ttu-id="f7fd2-140">Oggetto di database Gremlin.</span><span class="sxs-lookup"><span data-stu-id="f7fd2-140">Gremlin Database object.</span></span>

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

### <span data-ttu-id="f7fd2-141">-PartitionKey Rieti</span><span class="sxs-lookup"><span data-stu-id="f7fd2-141">-PartitionKeyKind</span></span>
<span data-ttu-id="f7fd2-142">Il tipo di algoritmo usato per il partizionamento.</span><span class="sxs-lookup"><span data-stu-id="f7fd2-142">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="f7fd2-143">I valori possibili includono: 'Hash', 'Range'</span><span class="sxs-lookup"><span data-stu-id="f7fd2-143">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="f7fd2-144">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="f7fd2-144">-PartitionKeyPath</span></span>
<span data-ttu-id="f7fd2-145">Percorso chiave di partizione, ad esempio '/address/zipcode'.</span><span class="sxs-lookup"><span data-stu-id="f7fd2-145">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="f7fd2-146">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="f7fd2-146">-PartitionKeyVersion</span></span>
<span data-ttu-id="f7fd2-147">Versione della definizione della chiave di partizione</span><span class="sxs-lookup"><span data-stu-id="f7fd2-147">The version of the partition key definition</span></span>

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

### <span data-ttu-id="f7fd2-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7fd2-148">-ResourceGroupName</span></span>
<span data-ttu-id="f7fd2-149">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f7fd2-149">Name of resource group.</span></span>

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

### <span data-ttu-id="f7fd2-150">-Velocità effettiva</span><span class="sxs-lookup"><span data-stu-id="f7fd2-150">-Throughput</span></span>
<span data-ttu-id="f7fd2-151">Velocità effettiva di Gremlin Graph (RU/s).</span><span class="sxs-lookup"><span data-stu-id="f7fd2-151">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="f7fd2-152">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="f7fd2-152">Default value is 400.</span></span>

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

### <span data-ttu-id="f7fd2-153">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="f7fd2-153">-TtlInSeconds</span></span>
<span data-ttu-id="f7fd2-154">Ttl predefinito in secondi.</span><span class="sxs-lookup"><span data-stu-id="f7fd2-154">Default Ttl in seconds.</span></span>
<span data-ttu-id="f7fd2-155">Se il valore manca o è impostato su -1, gli elementi non scadono.</span><span class="sxs-lookup"><span data-stu-id="f7fd2-155">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="f7fd2-156">Se il valore è impostato su n, gli elementi scadranno n secondi dopo l'ora dell'ultima modifica.</span><span class="sxs-lookup"><span data-stu-id="f7fd2-156">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="f7fd2-157">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="f7fd2-157">-UniqueKeyPolicy</span></span>
<span data-ttu-id="f7fd2-158">Oggetto UniqueKeyPolicy di tipo Microsoft.Azure.Commands.ChancesDB.PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="f7fd2-158">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="f7fd2-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7fd2-159">-WhatIf</span></span>
<span data-ttu-id="f7fd2-160">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f7fd2-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7fd2-161">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f7fd2-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7fd2-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7fd2-162">CommonParameters</span></span>
<span data-ttu-id="f7fd2-163">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7fd2-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7fd2-164">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f7fd2-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7fd2-165">INPUT</span><span class="sxs-lookup"><span data-stu-id="f7fd2-165">INPUTS</span></span>

### <span data-ttu-id="f7fd2-166">Microsoft.Azure.Commands.EnterpriseDb.Models.PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="f7fd2-166">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="f7fd2-167">Microsoft.Azure.Commands.ChancesDB.Models.PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="f7fd2-167">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="f7fd2-168">Microsoft.Azure.Commands.FerenzasDB.Models.PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="f7fd2-168">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

### <span data-ttu-id="f7fd2-169">Microsoft.Azure.Commands.EnterpriseDb.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="f7fd2-169">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="f7fd2-170">Microsoft.Azure.Commands.EnterpriseDb.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="f7fd2-170">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="f7fd2-171">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f7fd2-171">OUTPUTS</span></span>

### <span data-ttu-id="f7fd2-172">Microsoft.Azure.Commands.EnterpriseDb.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="f7fd2-172">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="f7fd2-173">Microsoft.Azure.Commands.ExceptionsDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="f7fd2-173">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="f7fd2-174">NOTE</span><span class="sxs-lookup"><span data-stu-id="f7fd2-174">NOTES</span></span>

## <span data-ttu-id="f7fd2-175">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f7fd2-175">RELATED LINKS</span></span>
