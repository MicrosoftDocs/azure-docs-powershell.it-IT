---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 3864693c5fd6da8c96557aac6f1626329f4e906f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954766"
---
# <span data-ttu-id="80911-101">New-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="80911-101">New-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="80911-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80911-102">SYNOPSIS</span></span>
<span data-ttu-id="80911-103">Crea una nuova raccoltaDbDb MongoDB.</span><span class="sxs-lookup"><span data-stu-id="80911-103">Creates a new CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="80911-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="80911-104">SYNTAX</span></span>

### <span data-ttu-id="80911-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="80911-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-Shard <String>]
 [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80911-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="80911-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBMongoDBCollection -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="80911-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="80911-107">DESCRIPTION</span></span>
<span data-ttu-id="80911-108">Crea una nuova raccoltaDbDb MongoDB.</span><span class="sxs-lookup"><span data-stu-id="80911-108">Creates a new CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="80911-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="80911-109">EXAMPLES</span></span>

### <span data-ttu-id="80911-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="80911-110">Example 1</span></span>
```powershell
PS C:\> 
        $ttlInSeconds = 604800
        $index1 = New-AzCosmosDBMongoDBIndex -Key @("partitionkey1", "partitionkey2") -Unique 1
>>      $index2 = New-AzCosmosDBMongoDBIndex -Key @("_ts") -TtlInSeconds $ttlInSeconds

New-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -DatabaseName myDatabaseName -Name myCollectionName -Index $index1,$index2 -Shard myShardKey

Name     : collection1
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName/collect
           ions/myCollectionName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

## <span data-ttu-id="80911-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80911-111">PARAMETERS</span></span>

### <span data-ttu-id="80911-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="80911-112">-AccountName</span></span>
<span data-ttu-id="80911-113">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="80911-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="80911-114">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="80911-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="80911-115">TTL per l'archiviazione analitica.</span><span class="sxs-lookup"><span data-stu-id="80911-115">TTL for Analytical Storage.</span></span>

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

### <span data-ttu-id="80911-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="80911-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="80911-117">Valore massimo di velocità effettiva se è abilitata la scalabilità automatica.</span><span class="sxs-lookup"><span data-stu-id="80911-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="80911-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="80911-118">-Confirm</span></span>
<span data-ttu-id="80911-119">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80911-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80911-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="80911-120">-DatabaseName</span></span>
<span data-ttu-id="80911-121">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="80911-121">Database name.</span></span>

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

### <span data-ttu-id="80911-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80911-122">-DefaultProfile</span></span>
<span data-ttu-id="80911-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="80911-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80911-124">-Index</span><span class="sxs-lookup"><span data-stu-id="80911-124">-Index</span></span>
<span data-ttu-id="80911-125">Matrice di oggetti PSMongoIndex.</span><span class="sxs-lookup"><span data-stu-id="80911-125">Array of PSMongoIndex objects.</span></span>

```yaml
Type: PSMongoIndex[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80911-126">-Name</span><span class="sxs-lookup"><span data-stu-id="80911-126">-Name</span></span>
<span data-ttu-id="80911-127">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="80911-127">Collection name.</span></span>

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

### <span data-ttu-id="80911-128">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="80911-128">-ParentObject</span></span>
<span data-ttu-id="80911-129">Oggetto database mongo.</span><span class="sxs-lookup"><span data-stu-id="80911-129">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80911-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80911-130">-ResourceGroupName</span></span>
<span data-ttu-id="80911-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="80911-131">Name of resource group.</span></span>

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

### <span data-ttu-id="80911-132">-Shard</span><span class="sxs-lookup"><span data-stu-id="80911-132">-Shard</span></span>
<span data-ttu-id="80911-133">Percorso della chiave di partizionamento.</span><span class="sxs-lookup"><span data-stu-id="80911-133">Sharding key path.</span></span>

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

### <span data-ttu-id="80911-134">-Velocità effettiva</span><span class="sxs-lookup"><span data-stu-id="80911-134">-Throughput</span></span>
<span data-ttu-id="80911-135">Velocità effettiva del contenitore SQL (RU/S).</span><span class="sxs-lookup"><span data-stu-id="80911-135">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="80911-136">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="80911-136">Default value is 400.</span></span>

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

### <span data-ttu-id="80911-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80911-137">-WhatIf</span></span>
<span data-ttu-id="80911-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="80911-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80911-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="80911-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80911-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80911-140">CommonParameters</span></span>
<span data-ttu-id="80911-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80911-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80911-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="80911-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80911-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="80911-143">INPUTS</span></span>

### <span data-ttu-id="80911-144">Microsoft.Azure.Commands.EnterpriseDb.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="80911-144">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="80911-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="80911-145">OUTPUTS</span></span>

### <span data-ttu-id="80911-146">Microsoft.Azure.Commands.EnterpriseDb.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="80911-146">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="80911-147">Microsoft.Azure.Commands.CpsDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="80911-147">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="80911-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="80911-148">NOTES</span></span>

## <span data-ttu-id="80911-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="80911-149">RELATED LINKS</span></span>
