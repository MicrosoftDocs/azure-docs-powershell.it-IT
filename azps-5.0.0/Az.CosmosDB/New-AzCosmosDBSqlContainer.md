---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
ms.openlocfilehash: afdd1296b01a6798d9253b7b21d15ba66f924c34
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299268"
---
# <span data-ttu-id="160b3-101">New-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="160b3-101">New-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="160b3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="160b3-102">SYNOPSIS</span></span>
<span data-ttu-id="160b3-103">Crea un nuovo contenitore SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="160b3-103">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="160b3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="160b3-104">SYNTAX</span></span>

### <span data-ttu-id="160b3-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="160b3-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="160b3-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="160b3-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlContainer -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 -ParentObject <PSSqlDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="160b3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="160b3-107">DESCRIPTION</span></span>
<span data-ttu-id="160b3-108">Crea un nuovo contenitore SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="160b3-108">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="160b3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="160b3-109">EXAMPLES</span></span>

### <span data-ttu-id="160b3-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="160b3-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlContainer -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a/b/c -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName/contain
           ers/myContainerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="160b3-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="160b3-111">PARAMETERS</span></span>

### <span data-ttu-id="160b3-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="160b3-112">-AccountName</span></span>
<span data-ttu-id="160b3-113">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="160b3-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="160b3-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="160b3-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="160b3-115">Valore massimo della velocità effettiva se autoscale è abilitato.</span><span class="sxs-lookup"><span data-stu-id="160b3-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="160b3-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="160b3-116">-Confirm</span></span>
<span data-ttu-id="160b3-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="160b3-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="160b3-118">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="160b3-118">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="160b3-119">Oggetto ConflictResolutionPolicy di tipo PSSqlConflictResolutionPolicy, se specificato, viene impostato come ConflictResolutionPolicy del contenitore.</span><span class="sxs-lookup"><span data-stu-id="160b3-119">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="160b3-120">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="160b3-120">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="160b3-121">Possono avere i valori: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="160b3-121">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="160b3-122">Se specificato insieme al parametro ConflictResolutionPolicy, viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="160b3-122">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="160b3-123">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="160b3-123">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="160b3-124">Da fornire quando il tipo è LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="160b3-124">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="160b3-125">Se specificato insieme al parametro ConflictResolutionPolicy, viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="160b3-125">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="160b3-126">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="160b3-126">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="160b3-127">Da fornire quando il tipo è personalizzato.</span><span class="sxs-lookup"><span data-stu-id="160b3-127">To be provided when the type is custom.</span></span>
<span data-ttu-id="160b3-128">Se specificato insieme al parametro ConflictResolutionPolicy, viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="160b3-128">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="160b3-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="160b3-129">-DatabaseName</span></span>
<span data-ttu-id="160b3-130">Nome database.</span><span class="sxs-lookup"><span data-stu-id="160b3-130">Database name.</span></span>

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

### <span data-ttu-id="160b3-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="160b3-131">-DefaultProfile</span></span>
<span data-ttu-id="160b3-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="160b3-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="160b3-133">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="160b3-133">-IndexingPolicy</span></span>
<span data-ttu-id="160b3-134">Oggetto Criteri di indicizzazione di tipo Microsoft. Azure. Commands. CosmosDB. PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="160b3-134">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="160b3-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="160b3-135">-Name</span></span>
<span data-ttu-id="160b3-136">Nome contenitore.</span><span class="sxs-lookup"><span data-stu-id="160b3-136">Container name.</span></span>

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

### <span data-ttu-id="160b3-137">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="160b3-137">-ParentObject</span></span>
<span data-ttu-id="160b3-138">Oggetto database SQL.</span><span class="sxs-lookup"><span data-stu-id="160b3-138">Sql Database object.</span></span>

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

### <span data-ttu-id="160b3-139">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="160b3-139">-PartitionKeyKind</span></span>
<span data-ttu-id="160b3-140">Il tipo di algoritmo usato per il partizionamento.</span><span class="sxs-lookup"><span data-stu-id="160b3-140">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="160b3-141">I valori possibili includono: "hash", "range"</span><span class="sxs-lookup"><span data-stu-id="160b3-141">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="160b3-142">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="160b3-142">-PartitionKeyPath</span></span>
<span data-ttu-id="160b3-143">Percorso della chiave di partizione, ad esempio, "/Address/ZipCode".</span><span class="sxs-lookup"><span data-stu-id="160b3-143">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="160b3-144">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="160b3-144">-PartitionKeyVersion</span></span>
<span data-ttu-id="160b3-145">La versione della definizione della chiave di partizione</span><span class="sxs-lookup"><span data-stu-id="160b3-145">The version of the partition key definition</span></span>

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

### <span data-ttu-id="160b3-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="160b3-146">-ResourceGroupName</span></span>
<span data-ttu-id="160b3-147">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="160b3-147">Name of resource group.</span></span>

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

### <span data-ttu-id="160b3-148">-Throughput</span><span class="sxs-lookup"><span data-stu-id="160b3-148">-Throughput</span></span>
<span data-ttu-id="160b3-149">La velocità effettiva del contenitore SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="160b3-149">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="160b3-150">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="160b3-150">Default value is 400.</span></span>

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

### <span data-ttu-id="160b3-151">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="160b3-151">-TtlInSeconds</span></span>
<span data-ttu-id="160b3-152">TTL predefinito in secondi.</span><span class="sxs-lookup"><span data-stu-id="160b3-152">Default Ttl in seconds.</span></span>
<span data-ttu-id="160b3-153">Se il valore è mancante o è impostato su-1, gli elementi non scadono.</span><span class="sxs-lookup"><span data-stu-id="160b3-153">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="160b3-154">Se il valore è impostato su n, gli elementi scadranno n secondi dopo l'ultima modifica dell'ora.</span><span class="sxs-lookup"><span data-stu-id="160b3-154">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="160b3-155">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="160b3-155">-UniqueKeyPolicy</span></span>
<span data-ttu-id="160b3-156">Oggetto UniqueKeyPolicy di tipo Microsoft. Azure. Commands. CosmosDB. PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="160b3-156">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="160b3-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="160b3-157">-WhatIf</span></span>
<span data-ttu-id="160b3-158">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="160b3-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="160b3-159">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="160b3-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="160b3-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="160b3-160">CommonParameters</span></span>
<span data-ttu-id="160b3-161">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="160b3-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="160b3-162">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="160b3-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="160b3-163">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="160b3-163">INPUTS</span></span>

### <span data-ttu-id="160b3-164">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="160b3-164">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="160b3-165">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="160b3-165">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="160b3-166">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="160b3-166">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="160b3-167">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="160b3-167">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="160b3-168">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="160b3-168">OUTPUTS</span></span>

### <span data-ttu-id="160b3-169">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="160b3-169">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="160b3-170">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="160b3-170">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="160b3-171">Note</span><span class="sxs-lookup"><span data-stu-id="160b3-171">NOTES</span></span>

## <span data-ttu-id="160b3-172">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="160b3-172">RELATED LINKS</span></span>
