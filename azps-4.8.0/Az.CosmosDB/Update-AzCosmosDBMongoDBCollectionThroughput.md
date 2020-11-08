---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollectionthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
ms.openlocfilehash: 23a88660bd599b0d317b89a1a7c1dbb1e2d51854
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94193033"
---
# <span data-ttu-id="336cb-101">Update-AzCosmosDBMongoDBCollectionThroughput</span><span class="sxs-lookup"><span data-stu-id="336cb-101">Update-AzCosmosDBMongoDBCollectionThroughput</span></span>

## <span data-ttu-id="336cb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="336cb-102">SYNOPSIS</span></span>
<span data-ttu-id="336cb-103">Aggiorna il valore di velocità effettiva di una raccolta di CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="336cb-103">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="336cb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="336cb-104">SYNTAX</span></span>

### <span data-ttu-id="336cb-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="336cb-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="336cb-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="336cb-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -ParentObject <PSMongoDBDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="336cb-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="336cb-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -InputObject <PSMongoDBCollectionGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="336cb-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="336cb-108">DESCRIPTION</span></span>
<span data-ttu-id="336cb-109">Aggiorna il valore di velocità effettiva di una raccolta di CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="336cb-109">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="336cb-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="336cb-110">EXAMPLES</span></span>

### <span data-ttu-id="336cb-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="336cb-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollectionThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myCollectionName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/mongodbDatabase/{mydatabaseName}/collections/{myCollectionName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

<span data-ttu-id="336cb-112">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="336cb-112">{{ Add example description here }}</span></span>

## <span data-ttu-id="336cb-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="336cb-113">PARAMETERS</span></span>

### <span data-ttu-id="336cb-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="336cb-114">-AccountName</span></span>
<span data-ttu-id="336cb-115">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="336cb-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="336cb-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="336cb-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="336cb-117">Valore massimo della velocità effettiva se autoscale è abilitato.</span><span class="sxs-lookup"><span data-stu-id="336cb-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="336cb-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="336cb-118">-Confirm</span></span>
<span data-ttu-id="336cb-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="336cb-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="336cb-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="336cb-120">-DatabaseName</span></span>
<span data-ttu-id="336cb-121">Nome database.</span><span class="sxs-lookup"><span data-stu-id="336cb-121">Database name.</span></span>

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

### <span data-ttu-id="336cb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="336cb-122">-DefaultProfile</span></span>
<span data-ttu-id="336cb-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="336cb-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="336cb-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="336cb-124">-InputObject</span></span>
<span data-ttu-id="336cb-125">Oggetto di database Mongo.</span><span class="sxs-lookup"><span data-stu-id="336cb-125">Mongo Database object.</span></span>

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

### <span data-ttu-id="336cb-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="336cb-126">-Name</span></span>
<span data-ttu-id="336cb-127">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="336cb-127">Collection name.</span></span>

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

### <span data-ttu-id="336cb-128">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="336cb-128">-ParentObject</span></span>
<span data-ttu-id="336cb-129">Oggetto di database Mongo.</span><span class="sxs-lookup"><span data-stu-id="336cb-129">Mongo Database object.</span></span>

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

### <span data-ttu-id="336cb-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="336cb-130">-ResourceGroupName</span></span>
<span data-ttu-id="336cb-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="336cb-131">Name of resource group.</span></span>

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

### <span data-ttu-id="336cb-132">-Throughput</span><span class="sxs-lookup"><span data-stu-id="336cb-132">-Throughput</span></span>
<span data-ttu-id="336cb-133">La velocità effettiva del contenitore SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="336cb-133">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="336cb-134">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="336cb-134">Default value is 400.</span></span>

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

### <span data-ttu-id="336cb-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="336cb-135">-WhatIf</span></span>
<span data-ttu-id="336cb-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="336cb-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="336cb-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="336cb-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="336cb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="336cb-138">CommonParameters</span></span>
<span data-ttu-id="336cb-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="336cb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="336cb-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="336cb-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="336cb-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="336cb-141">INPUTS</span></span>

### <span data-ttu-id="336cb-142">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="336cb-142">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="336cb-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="336cb-143">OUTPUTS</span></span>

### <span data-ttu-id="336cb-144">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="336cb-144">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="336cb-145">Note</span><span class="sxs-lookup"><span data-stu-id="336cb-145">NOTES</span></span>

## <span data-ttu-id="336cb-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="336cb-146">RELATED LINKS</span></span>