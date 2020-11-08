---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 1919b3075b24e96edce93c8d3611f3864d3f9391
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190525"
---
# <span data-ttu-id="20c74-101">Get-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="20c74-101">Get-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="20c74-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="20c74-102">SYNOPSIS</span></span>
<span data-ttu-id="20c74-103">Ottiene la raccolta MongoDB CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="20c74-103">Gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="20c74-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="20c74-104">SYNTAX</span></span>

### <span data-ttu-id="20c74-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="20c74-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBCollection -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="20c74-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="20c74-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBCollection [-Name <String>] -ParentObject <PSMongoDBDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20c74-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20c74-107">DESCRIPTION</span></span>
<span data-ttu-id="20c74-108">Il cmdlet **Get-AzCosmosDBMongoDBCollection** ottiene la raccolta MongoDB CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="20c74-108">The **Get-AzCosmosDBMongoDBCollection** cmdlet gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="20c74-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="20c74-109">EXAMPLES</span></span>

### <span data-ttu-id="20c74-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="20c74-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -Database {dbName} -Name {collectionName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

<span data-ttu-id="20c74-111">Oggetto Resource contiene MongoIndexes, _rid, _ts, _etag proprietà.</span><span class="sxs-lookup"><span data-stu-id="20c74-111">Resource Object contains MongoIndexes, _rid, _ts, _etag properties.</span></span>

### <span data-ttu-id="20c74-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="20c74-112">Example 2</span></span>
```powershell
PS C:\> (Get-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -Database {dbName} -Name {collectionName}).Resource.ShardKey 

Key           Value
----          ----- 
<ShardKey>    <Value>
```

<span data-ttu-id="20c74-113">Questo esempio ottiene il ShardKey della raccolta recuperata</span><span class="sxs-lookup"><span data-stu-id="20c74-113">This example gets the ShardKey of the retrieved collection</span></span>

## <span data-ttu-id="20c74-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="20c74-114">PARAMETERS</span></span>

### <span data-ttu-id="20c74-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="20c74-115">-AccountName</span></span>
<span data-ttu-id="20c74-116">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="20c74-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="20c74-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="20c74-117">-DatabaseName</span></span>
<span data-ttu-id="20c74-118">Nome database.</span><span class="sxs-lookup"><span data-stu-id="20c74-118">Database name.</span></span>

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

### <span data-ttu-id="20c74-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20c74-119">-DefaultProfile</span></span>
<span data-ttu-id="20c74-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="20c74-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20c74-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="20c74-121">-Name</span></span>
<span data-ttu-id="20c74-122">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="20c74-122">Collection name.</span></span>

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

### <span data-ttu-id="20c74-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="20c74-123">-ParentObject</span></span>
<span data-ttu-id="20c74-124">Oggetto di database Mongo.</span><span class="sxs-lookup"><span data-stu-id="20c74-124">Mongo Database object.</span></span>

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

### <span data-ttu-id="20c74-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20c74-125">-ResourceGroupName</span></span>
<span data-ttu-id="20c74-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="20c74-126">Name of resource group.</span></span>

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

### <span data-ttu-id="20c74-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20c74-127">CommonParameters</span></span>
<span data-ttu-id="20c74-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20c74-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20c74-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20c74-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20c74-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="20c74-130">INPUTS</span></span>

### <span data-ttu-id="20c74-131">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="20c74-131">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="20c74-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="20c74-132">OUTPUTS</span></span>

### <span data-ttu-id="20c74-133">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="20c74-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="20c74-134">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="20c74-134">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="20c74-135">Note</span><span class="sxs-lookup"><span data-stu-id="20c74-135">NOTES</span></span>

## <span data-ttu-id="20c74-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="20c74-136">RELATED LINKS</span></span>
