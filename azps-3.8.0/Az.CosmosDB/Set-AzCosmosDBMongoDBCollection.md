---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 33aa465024591436d80b34b765c90badfb0f1662
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022395"
---
# <span data-ttu-id="7e699-101">Set-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="7e699-101">Set-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="7e699-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7e699-102">SYNOPSIS</span></span>
<span data-ttu-id="7e699-103">Imposta la raccolta CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="7e699-103">Sets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="7e699-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7e699-104">SYNTAX</span></span>

### <span data-ttu-id="7e699-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7e699-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-Throughput <Int32>] [-Shard <String>] [-Index <PSMongoIndex[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e699-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e699-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBMongoDBCollection -Name <String> [-Throughput <Int32>] [-Shard <String>]
 [-Index <PSMongoIndex[]>] -InputObject <PSMongoDBDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e699-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e699-107">DESCRIPTION</span></span>
<span data-ttu-id="7e699-108">Il cmdlet **set-AzCosmosDBMongoDBCollection** imposta la raccolta MongoDB CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="7e699-108">The **Set-AzCosmosDBMongoDBCollection** cmdlet sets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="7e699-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7e699-109">EXAMPLES</span></span>

### <span data-ttu-id="7e699-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7e699-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName}  -Database {dbName} -Name {collectionName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

<span data-ttu-id="7e699-111">Oggetto Resource contiene MongoIndexes, _rid, _ts, _etag proprietà.</span><span class="sxs-lookup"><span data-stu-id="7e699-111">Resource Object contains MongoIndexes, _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="7e699-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7e699-112">PARAMETERS</span></span>

### <span data-ttu-id="7e699-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7e699-113">-AccountName</span></span>
<span data-ttu-id="7e699-114">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="7e699-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7e699-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7e699-115">-Confirm</span></span>
<span data-ttu-id="7e699-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e699-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e699-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7e699-117">-DatabaseName</span></span>
<span data-ttu-id="7e699-118">Nome database.</span><span class="sxs-lookup"><span data-stu-id="7e699-118">Database name.</span></span>

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

### <span data-ttu-id="7e699-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e699-119">-DefaultProfile</span></span>
<span data-ttu-id="7e699-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7e699-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e699-121">-Index</span><span class="sxs-lookup"><span data-stu-id="7e699-121">-Index</span></span>
<span data-ttu-id="7e699-122">Matrice di oggetti PSMongoIndex.</span><span class="sxs-lookup"><span data-stu-id="7e699-122">Array of PSMongoIndex objects.</span></span>

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

### <span data-ttu-id="7e699-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e699-123">-InputObject</span></span>
<span data-ttu-id="7e699-124">Oggetto di database Mongo.</span><span class="sxs-lookup"><span data-stu-id="7e699-124">Mongo Database object.</span></span>

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

### <span data-ttu-id="7e699-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="7e699-125">-Name</span></span>
<span data-ttu-id="7e699-126">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="7e699-126">Collection name.</span></span>

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

### <span data-ttu-id="7e699-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e699-127">-ResourceGroupName</span></span>
<span data-ttu-id="7e699-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7e699-128">Name of resource group.</span></span>

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

### <span data-ttu-id="7e699-129">-Shard</span><span class="sxs-lookup"><span data-stu-id="7e699-129">-Shard</span></span>
<span data-ttu-id="7e699-130">Percorso chiave di frammentazione.</span><span class="sxs-lookup"><span data-stu-id="7e699-130">Sharding key path.</span></span>

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

### <span data-ttu-id="7e699-131">-Throughput</span><span class="sxs-lookup"><span data-stu-id="7e699-131">-Throughput</span></span>
<span data-ttu-id="7e699-132">La velocità effettiva del contenitore SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="7e699-132">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="7e699-133">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="7e699-133">Default value is 400.</span></span>

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

### <span data-ttu-id="7e699-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e699-134">-WhatIf</span></span>
<span data-ttu-id="7e699-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7e699-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e699-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7e699-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e699-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e699-137">CommonParameters</span></span>
<span data-ttu-id="7e699-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e699-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e699-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e699-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e699-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7e699-140">INPUTS</span></span>

### <span data-ttu-id="7e699-141">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="7e699-141">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="7e699-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7e699-142">OUTPUTS</span></span>

### <span data-ttu-id="7e699-143">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="7e699-143">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="7e699-144">Note</span><span class="sxs-lookup"><span data-stu-id="7e699-144">NOTES</span></span>

## <span data-ttu-id="7e699-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7e699-145">RELATED LINKS</span></span>
