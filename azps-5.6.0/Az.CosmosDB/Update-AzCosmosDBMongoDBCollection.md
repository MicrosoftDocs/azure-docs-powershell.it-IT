---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 2458c31ba75470c5d2b5bb2b73d817eb58c5bc61
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977309"
---
# <span data-ttu-id="1ab2e-101">Update-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="1ab2e-101">Update-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="1ab2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ab2e-102">SYNOPSIS</span></span>
<span data-ttu-id="1ab2e-103">Aggiorna la raccolta MongoDBdb del DatabaseDb.</span><span class="sxs-lookup"><span data-stu-id="1ab2e-103">Updates the CosmosDB MongoDB Collection.</span></span> <span data-ttu-id="1ab2e-104">Esegue un'operazione di patch sul lato client leggendo la raccolta esistente.</span><span class="sxs-lookup"><span data-stu-id="1ab2e-104">Performs a client side patch operation by reading the existing Collection.</span></span>

## <span data-ttu-id="1ab2e-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1ab2e-105">SYNTAX</span></span>

### <span data-ttu-id="1ab2e-106">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1ab2e-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-Shard <String>]
 [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ab2e-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ab2e-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollection [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1ab2e-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ab2e-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollection [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -InputObject <PSMongoDBCollectionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1ab2e-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1ab2e-109">DESCRIPTION</span></span>
<span data-ttu-id="1ab2e-110">Aggiorna la raccolta MongoDBdb del DatabaseDb.</span><span class="sxs-lookup"><span data-stu-id="1ab2e-110">Updates the CosmosDB MongoDB Collection.</span></span> <span data-ttu-id="1ab2e-111">Esegue un'operazione di patch sul lato client leggendo la raccolta esistente.</span><span class="sxs-lookup"><span data-stu-id="1ab2e-111">Performs a client side patch operation by reading the existing Collection.</span></span>

## <span data-ttu-id="1ab2e-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1ab2e-112">EXAMPLES</span></span>

### <span data-ttu-id="1ab2e-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1ab2e-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -DatabaseName myDatabaseName -Name myCollectionName -Index $index1,$index2

Name     : collection1
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName/collect
           ions/myCollectionName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

## <span data-ttu-id="1ab2e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ab2e-114">PARAMETERS</span></span>

### <span data-ttu-id="1ab2e-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1ab2e-115">-AccountName</span></span>
<span data-ttu-id="1ab2e-116">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="1ab2e-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1ab2e-117">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="1ab2e-117">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="1ab2e-118">TTL per l'archiviazione analitica.</span><span class="sxs-lookup"><span data-stu-id="1ab2e-118">TTL for Analytical Storage.</span></span>

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

### <span data-ttu-id="1ab2e-119">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="1ab2e-119">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="1ab2e-120">Valore massimo di velocità effettiva se è abilitata la scalabilità automatica.</span><span class="sxs-lookup"><span data-stu-id="1ab2e-120">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="1ab2e-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1ab2e-121">-Confirm</span></span>
<span data-ttu-id="1ab2e-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ab2e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ab2e-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1ab2e-123">-DatabaseName</span></span>
<span data-ttu-id="1ab2e-124">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="1ab2e-124">Database name.</span></span>

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

### <span data-ttu-id="1ab2e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ab2e-125">-DefaultProfile</span></span>
<span data-ttu-id="1ab2e-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1ab2e-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ab2e-127">-Index</span><span class="sxs-lookup"><span data-stu-id="1ab2e-127">-Index</span></span>
<span data-ttu-id="1ab2e-128">Matrice di oggetti PSMongoIndex.</span><span class="sxs-lookup"><span data-stu-id="1ab2e-128">Array of PSMongoIndex objects.</span></span>

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

### <span data-ttu-id="1ab2e-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ab2e-129">-InputObject</span></span>
<span data-ttu-id="1ab2e-130">Oggetto Contenitore Sql.</span><span class="sxs-lookup"><span data-stu-id="1ab2e-130">Sql Container object.</span></span>

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

### <span data-ttu-id="1ab2e-131">-Name</span><span class="sxs-lookup"><span data-stu-id="1ab2e-131">-Name</span></span>
<span data-ttu-id="1ab2e-132">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="1ab2e-132">Collection name.</span></span>

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

### <span data-ttu-id="1ab2e-133">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="1ab2e-133">-ParentObject</span></span>
<span data-ttu-id="1ab2e-134">Oggetto database mongo.</span><span class="sxs-lookup"><span data-stu-id="1ab2e-134">Mongo Database object.</span></span>

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

### <span data-ttu-id="1ab2e-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ab2e-135">-ResourceGroupName</span></span>
<span data-ttu-id="1ab2e-136">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1ab2e-136">Name of resource group.</span></span>

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

### <span data-ttu-id="1ab2e-137">-Shard</span><span class="sxs-lookup"><span data-stu-id="1ab2e-137">-Shard</span></span>
<span data-ttu-id="1ab2e-138">Percorso della chiave di partizionamento.</span><span class="sxs-lookup"><span data-stu-id="1ab2e-138">Sharding key path.</span></span>

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

### <span data-ttu-id="1ab2e-139">-Velocità effettiva</span><span class="sxs-lookup"><span data-stu-id="1ab2e-139">-Throughput</span></span>
<span data-ttu-id="1ab2e-140">Velocità effettiva del contenitore SQL (RU/S).</span><span class="sxs-lookup"><span data-stu-id="1ab2e-140">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="1ab2e-141">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="1ab2e-141">Default value is 400.</span></span>

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

### <span data-ttu-id="1ab2e-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ab2e-142">-WhatIf</span></span>
<span data-ttu-id="1ab2e-143">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1ab2e-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ab2e-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1ab2e-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ab2e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ab2e-145">CommonParameters</span></span>
<span data-ttu-id="1ab2e-146">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ab2e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ab2e-147">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1ab2e-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ab2e-148">INPUT</span><span class="sxs-lookup"><span data-stu-id="1ab2e-148">INPUTS</span></span>

### <span data-ttu-id="1ab2e-149">Microsoft.Azure.Commands.EnterpriseDb.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="1ab2e-149">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="1ab2e-150">Microsoft.Azure.Commands.EnterpriseDb.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="1ab2e-150">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="1ab2e-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1ab2e-151">OUTPUTS</span></span>

### <span data-ttu-id="1ab2e-152">Microsoft.Azure.Commands.EnterpriseDb.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="1ab2e-152">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="1ab2e-153">Microsoft.Azure.Commands.ExceptionsDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="1ab2e-153">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="1ab2e-154">NOTE</span><span class="sxs-lookup"><span data-stu-id="1ab2e-154">NOTES</span></span>

## <span data-ttu-id="1ab2e-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1ab2e-155">RELATED LINKS</span></span>
