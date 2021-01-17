---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 741d63bfe54c03eb101d74519251b67c5e1664b1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346288"
---
# <span data-ttu-id="4755a-101">New-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="4755a-101">New-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="4755a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4755a-102">SYNOPSIS</span></span>
<span data-ttu-id="4755a-103">Crea una nuova raccolta MongoDB CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="4755a-103">Creates a new CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="4755a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4755a-104">SYNTAX</span></span>

### <span data-ttu-id="4755a-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4755a-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-Shard <String>]
 [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4755a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4755a-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBMongoDBCollection -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4755a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4755a-107">DESCRIPTION</span></span>
<span data-ttu-id="4755a-108">Crea una nuova raccolta MongoDB CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="4755a-108">Creates a new CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="4755a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4755a-109">EXAMPLES</span></span>

### <span data-ttu-id="4755a-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4755a-110">Example 1</span></span>
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

## <span data-ttu-id="4755a-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4755a-111">PARAMETERS</span></span>

### <span data-ttu-id="4755a-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4755a-112">-AccountName</span></span>
<span data-ttu-id="4755a-113">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="4755a-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="4755a-114">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="4755a-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="4755a-115">TTL per lo spazio di archiviazione analitico.</span><span class="sxs-lookup"><span data-stu-id="4755a-115">TTL for Analytical Storage.</span></span>

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

### <span data-ttu-id="4755a-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="4755a-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="4755a-117">Valore massimo della velocità effettiva se autoscale è abilitato.</span><span class="sxs-lookup"><span data-stu-id="4755a-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="4755a-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4755a-118">-Confirm</span></span>
<span data-ttu-id="4755a-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4755a-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4755a-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4755a-120">-DatabaseName</span></span>
<span data-ttu-id="4755a-121">Nome database.</span><span class="sxs-lookup"><span data-stu-id="4755a-121">Database name.</span></span>

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

### <span data-ttu-id="4755a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4755a-122">-DefaultProfile</span></span>
<span data-ttu-id="4755a-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4755a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4755a-124">-Index</span><span class="sxs-lookup"><span data-stu-id="4755a-124">-Index</span></span>
<span data-ttu-id="4755a-125">Matrice di oggetti PSMongoIndex.</span><span class="sxs-lookup"><span data-stu-id="4755a-125">Array of PSMongoIndex objects.</span></span>

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

### <span data-ttu-id="4755a-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="4755a-126">-Name</span></span>
<span data-ttu-id="4755a-127">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="4755a-127">Collection name.</span></span>

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

### <span data-ttu-id="4755a-128">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4755a-128">-ParentObject</span></span>
<span data-ttu-id="4755a-129">Oggetto di database Mongo.</span><span class="sxs-lookup"><span data-stu-id="4755a-129">Mongo Database object.</span></span>

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

### <span data-ttu-id="4755a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4755a-130">-ResourceGroupName</span></span>
<span data-ttu-id="4755a-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4755a-131">Name of resource group.</span></span>

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

### <span data-ttu-id="4755a-132">-Shard</span><span class="sxs-lookup"><span data-stu-id="4755a-132">-Shard</span></span>
<span data-ttu-id="4755a-133">Percorso chiave di frammentazione.</span><span class="sxs-lookup"><span data-stu-id="4755a-133">Sharding key path.</span></span>

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

### <span data-ttu-id="4755a-134">-Throughput</span><span class="sxs-lookup"><span data-stu-id="4755a-134">-Throughput</span></span>
<span data-ttu-id="4755a-135">La velocità effettiva del contenitore SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="4755a-135">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="4755a-136">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="4755a-136">Default value is 400.</span></span>

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

### <span data-ttu-id="4755a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4755a-137">-WhatIf</span></span>
<span data-ttu-id="4755a-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4755a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4755a-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4755a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4755a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4755a-140">CommonParameters</span></span>
<span data-ttu-id="4755a-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4755a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4755a-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4755a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4755a-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4755a-143">INPUTS</span></span>

### <span data-ttu-id="4755a-144">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="4755a-144">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="4755a-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4755a-145">OUTPUTS</span></span>

### <span data-ttu-id="4755a-146">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="4755a-146">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="4755a-147">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="4755a-147">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="4755a-148">Note</span><span class="sxs-lookup"><span data-stu-id="4755a-148">NOTES</span></span>

## <span data-ttu-id="4755a-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4755a-149">RELATED LINKS</span></span>
