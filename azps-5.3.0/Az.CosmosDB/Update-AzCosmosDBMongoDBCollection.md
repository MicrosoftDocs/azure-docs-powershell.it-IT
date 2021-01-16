---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 9440e3541e5022ffbbe328ac81859d2ababa6209
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98487816"
---
# <span data-ttu-id="f3949-101">Update-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="f3949-101">Update-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="f3949-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f3949-102">SYNOPSIS</span></span>
<span data-ttu-id="f3949-103">Aggiorna la raccolta CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="f3949-103">Updates the CosmosDB MongoDB Collection.</span></span> <span data-ttu-id="f3949-104">Esegue un'operazione di patch lato client leggendo la raccolta esistente.</span><span class="sxs-lookup"><span data-stu-id="f3949-104">Performs a client side patch operation by reading the existing Collection.</span></span>

## <span data-ttu-id="f3949-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f3949-105">SYNTAX</span></span>

### <span data-ttu-id="f3949-106">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f3949-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-Shard <String>]
 [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3949-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3949-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollection [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f3949-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3949-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollection [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -InputObject <PSMongoDBCollectionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f3949-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3949-109">DESCRIPTION</span></span>
<span data-ttu-id="f3949-110">Aggiorna la raccolta CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="f3949-110">Updates the CosmosDB MongoDB Collection.</span></span> <span data-ttu-id="f3949-111">Esegue un'operazione di patch lato client leggendo la raccolta esistente.</span><span class="sxs-lookup"><span data-stu-id="f3949-111">Performs a client side patch operation by reading the existing Collection.</span></span>

## <span data-ttu-id="f3949-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f3949-112">EXAMPLES</span></span>

### <span data-ttu-id="f3949-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f3949-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -DatabaseName myDatabaseName -Name myCollectionName -Index $index1,$index2

Name     : collection1
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName/collect
           ions/myCollectionName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

## <span data-ttu-id="f3949-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f3949-114">PARAMETERS</span></span>

### <span data-ttu-id="f3949-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f3949-115">-AccountName</span></span>
<span data-ttu-id="f3949-116">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="f3949-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f3949-117">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="f3949-117">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="f3949-118">TTL per lo spazio di archiviazione analitico.</span><span class="sxs-lookup"><span data-stu-id="f3949-118">TTL for Analytical Storage.</span></span>

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

### <span data-ttu-id="f3949-119">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="f3949-119">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="f3949-120">Valore massimo della velocità effettiva se autoscale è abilitato.</span><span class="sxs-lookup"><span data-stu-id="f3949-120">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="f3949-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f3949-121">-Confirm</span></span>
<span data-ttu-id="f3949-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3949-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3949-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f3949-123">-DatabaseName</span></span>
<span data-ttu-id="f3949-124">Nome database.</span><span class="sxs-lookup"><span data-stu-id="f3949-124">Database name.</span></span>

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

### <span data-ttu-id="f3949-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3949-125">-DefaultProfile</span></span>
<span data-ttu-id="f3949-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f3949-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3949-127">-Index</span><span class="sxs-lookup"><span data-stu-id="f3949-127">-Index</span></span>
<span data-ttu-id="f3949-128">Matrice di oggetti PSMongoIndex.</span><span class="sxs-lookup"><span data-stu-id="f3949-128">Array of PSMongoIndex objects.</span></span>

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

### <span data-ttu-id="f3949-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3949-129">-InputObject</span></span>
<span data-ttu-id="f3949-130">Oggetto contenitore SQL.</span><span class="sxs-lookup"><span data-stu-id="f3949-130">Sql Container object.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3949-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="f3949-131">-Name</span></span>
<span data-ttu-id="f3949-132">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="f3949-132">Collection name.</span></span>

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

### <span data-ttu-id="f3949-133">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f3949-133">-ParentObject</span></span>
<span data-ttu-id="f3949-134">Oggetto di database Mongo.</span><span class="sxs-lookup"><span data-stu-id="f3949-134">Mongo Database object.</span></span>

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

### <span data-ttu-id="f3949-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3949-135">-ResourceGroupName</span></span>
<span data-ttu-id="f3949-136">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f3949-136">Name of resource group.</span></span>

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

### <span data-ttu-id="f3949-137">-Shard</span><span class="sxs-lookup"><span data-stu-id="f3949-137">-Shard</span></span>
<span data-ttu-id="f3949-138">Percorso chiave di frammentazione.</span><span class="sxs-lookup"><span data-stu-id="f3949-138">Sharding key path.</span></span>

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

### <span data-ttu-id="f3949-139">-Throughput</span><span class="sxs-lookup"><span data-stu-id="f3949-139">-Throughput</span></span>
<span data-ttu-id="f3949-140">La velocità effettiva del contenitore SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="f3949-140">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="f3949-141">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="f3949-141">Default value is 400.</span></span>

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

### <span data-ttu-id="f3949-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3949-142">-WhatIf</span></span>
<span data-ttu-id="f3949-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f3949-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3949-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f3949-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3949-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3949-145">CommonParameters</span></span>
<span data-ttu-id="f3949-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3949-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3949-147">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f3949-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3949-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f3949-148">INPUTS</span></span>

### <span data-ttu-id="f3949-149">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="f3949-149">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="f3949-150">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="f3949-150">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="f3949-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f3949-151">OUTPUTS</span></span>

### <span data-ttu-id="f3949-152">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="f3949-152">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="f3949-153">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="f3949-153">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="f3949-154">Note</span><span class="sxs-lookup"><span data-stu-id="f3949-154">NOTES</span></span>

## <span data-ttu-id="f3949-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f3949-155">RELATED LINKS</span></span>
