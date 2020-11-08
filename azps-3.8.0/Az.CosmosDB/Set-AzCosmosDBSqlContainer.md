---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 83c26ff0a05a88540563b7e3867c2e1d6ac12be0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022383"
---
# <span data-ttu-id="f16ba-101">Set-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="f16ba-101">Set-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="f16ba-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f16ba-102">SYNOPSIS</span></span>
<span data-ttu-id="f16ba-103">Crea un nuovo o aggiorna un contenitore SQL CosmosDB esistente.</span><span class="sxs-lookup"><span data-stu-id="f16ba-103">Creates a new or updates an existing CosmosDB Sql Container.</span></span>

## <span data-ttu-id="f16ba-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f16ba-104">SYNTAX</span></span>

### <span data-ttu-id="f16ba-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f16ba-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f16ba-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f16ba-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBSqlContainer -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] -InputObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f16ba-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f16ba-107">DESCRIPTION</span></span>
<span data-ttu-id="f16ba-108">Il cmdlet **set-AzCosmosDBSqlContainer** crea un nuovo o aggiorna un contenitore SQL esistente di CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="f16ba-108">The **Set-AzCosmosDBSqlContainer** cmdlet creates a new or updates an existing CosmosDB Sql Container.</span></span>

## <span data-ttu-id="f16ba-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f16ba-109">EXAMPLES</span></span>

### <span data-ttu-id="f16ba-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f16ba-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBSqlContainer -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -Name {containerName} -PartitionKeyKind Hash -PartitionKeyPath {samplePath}

Name                     : {containerName}
Id                       : {containerId}
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="f16ba-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f16ba-111">PARAMETERS</span></span>

### <span data-ttu-id="f16ba-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f16ba-112">-AccountName</span></span>
<span data-ttu-id="f16ba-113">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="f16ba-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f16ba-114">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f16ba-114">-Confirm</span></span>
<span data-ttu-id="f16ba-115">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f16ba-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f16ba-116">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="f16ba-116">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="f16ba-117">Oggetto ConflictResolutionPolicy di tipo PSSqlConflictResolutionPolicy, se specificato, viene impostato come ConflictResolutionPolicy del contenitore.</span><span class="sxs-lookup"><span data-stu-id="f16ba-117">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="f16ba-118">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="f16ba-118">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="f16ba-119">Possono avere i valori: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="f16ba-119">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="f16ba-120">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="f16ba-120">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="f16ba-121">Da fornire quando il tipo è LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="f16ba-121">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="f16ba-122">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="f16ba-122">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="f16ba-123">Da fornire quando il tipo è personalizzato.</span><span class="sxs-lookup"><span data-stu-id="f16ba-123">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="f16ba-124">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f16ba-124">-DatabaseName</span></span>
<span data-ttu-id="f16ba-125">Nome database.</span><span class="sxs-lookup"><span data-stu-id="f16ba-125">Database name.</span></span>

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

### <span data-ttu-id="f16ba-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f16ba-126">-DefaultProfile</span></span>
<span data-ttu-id="f16ba-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f16ba-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f16ba-128">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="f16ba-128">-IndexingPolicy</span></span>
<span data-ttu-id="f16ba-129">Oggetto Criteri di indicizzazione di tipo Microsoft. Azure. Commands. CosmosDB. PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="f16ba-129">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="f16ba-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f16ba-130">-InputObject</span></span>
<span data-ttu-id="f16ba-131">Oggetto database SQL.</span><span class="sxs-lookup"><span data-stu-id="f16ba-131">Sql Database object.</span></span>

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

### <span data-ttu-id="f16ba-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="f16ba-132">-Name</span></span>
<span data-ttu-id="f16ba-133">Nome contenitore.</span><span class="sxs-lookup"><span data-stu-id="f16ba-133">Container name.</span></span>

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

### <span data-ttu-id="f16ba-134">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="f16ba-134">-PartitionKeyKind</span></span>
<span data-ttu-id="f16ba-135">Il tipo di algoritmo usato per il partizionamento.</span><span class="sxs-lookup"><span data-stu-id="f16ba-135">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="f16ba-136">I valori possibili includono: "hash", "range"</span><span class="sxs-lookup"><span data-stu-id="f16ba-136">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="f16ba-137">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="f16ba-137">-PartitionKeyPath</span></span>
<span data-ttu-id="f16ba-138">Percorso della chiave di partizione, ad esempio, "/Address/ZipCode".</span><span class="sxs-lookup"><span data-stu-id="f16ba-138">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="f16ba-139">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="f16ba-139">-PartitionKeyVersion</span></span>
<span data-ttu-id="f16ba-140">La versione della definizione della chiave di partizione</span><span class="sxs-lookup"><span data-stu-id="f16ba-140">The version of the partition key definition</span></span>

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

### <span data-ttu-id="f16ba-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f16ba-141">-ResourceGroupName</span></span>
<span data-ttu-id="f16ba-142">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f16ba-142">Name of resource group.</span></span>

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

### <span data-ttu-id="f16ba-143">-Throughput</span><span class="sxs-lookup"><span data-stu-id="f16ba-143">-Throughput</span></span>
<span data-ttu-id="f16ba-144">La velocità effettiva del contenitore SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="f16ba-144">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="f16ba-145">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="f16ba-145">Default value is 400.</span></span>

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

### <span data-ttu-id="f16ba-146">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="f16ba-146">-TtlInSeconds</span></span>
<span data-ttu-id="f16ba-147">TTL predefinito in secondi.</span><span class="sxs-lookup"><span data-stu-id="f16ba-147">Default Ttl in seconds.</span></span>
<span data-ttu-id="f16ba-148">Se il valore è mancante o è impostato su-1, gli elementi non scadono.</span><span class="sxs-lookup"><span data-stu-id="f16ba-148">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="f16ba-149">Se il valore è impostato su n, gli elementi scadranno n secondi dopo l'ultima modifica dell'ora.</span><span class="sxs-lookup"><span data-stu-id="f16ba-149">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="f16ba-150">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="f16ba-150">-UniqueKeyPolicy</span></span>
<span data-ttu-id="f16ba-151">Oggetto UniqueKeyPolicy di tipo Microsoft. Azure. Commands. CosmosDB. PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="f16ba-151">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="f16ba-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f16ba-152">-WhatIf</span></span>
<span data-ttu-id="f16ba-153">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f16ba-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f16ba-154">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f16ba-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f16ba-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f16ba-155">CommonParameters</span></span>
<span data-ttu-id="f16ba-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f16ba-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f16ba-157">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f16ba-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f16ba-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f16ba-158">INPUTS</span></span>

### <span data-ttu-id="f16ba-159">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f16ba-159">None</span></span>

## <span data-ttu-id="f16ba-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f16ba-160">OUTPUTS</span></span>

### <span data-ttu-id="f16ba-161">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="f16ba-161">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="f16ba-162">Note</span><span class="sxs-lookup"><span data-stu-id="f16ba-162">NOTES</span></span>

## <span data-ttu-id="f16ba-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f16ba-163">RELATED LINKS</span></span>
