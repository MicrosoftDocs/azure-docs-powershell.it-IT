---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 623ed0391ba36722cce26a42f1dd3d820cbd49f8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022078"
---
# <span data-ttu-id="33466-101">Get-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="33466-101">Get-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="33466-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="33466-102">SYNOPSIS</span></span>
<span data-ttu-id="33466-103">Ottiene la raccolta MongoDB CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="33466-103">Gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="33466-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="33466-104">SYNTAX</span></span>

### <span data-ttu-id="33466-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="33466-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBCollection -ResourceGroupName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="33466-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="33466-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBCollection [-Name <String>] -InputObject <PSMongoDBDatabaseGetResults> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33466-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="33466-107">DESCRIPTION</span></span>
<span data-ttu-id="33466-108">Il cmdlet **Get-AzCosmosDBMongoDBCollection** ottiene la raccolta MongoDB CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="33466-108">The **Get-AzCosmosDBMongoDBCollection** cmdlet gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="33466-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="33466-109">EXAMPLES</span></span>

### <span data-ttu-id="33466-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="33466-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName}  -Database {dbName} -Name {collectionName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

<span data-ttu-id="33466-111">Oggetto Resource contiene MongoIndexes, _rid, _ts, _etag proprietà.</span><span class="sxs-lookup"><span data-stu-id="33466-111">Resource Object contains MongoIndexes, _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="33466-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="33466-112">PARAMETERS</span></span>

### <span data-ttu-id="33466-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="33466-113">-AccountName</span></span>
<span data-ttu-id="33466-114">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="33466-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="33466-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="33466-115">-DatabaseName</span></span>
<span data-ttu-id="33466-116">Nome database.</span><span class="sxs-lookup"><span data-stu-id="33466-116">Database name.</span></span>

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

### <span data-ttu-id="33466-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33466-117">-DefaultProfile</span></span>
<span data-ttu-id="33466-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="33466-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33466-119">-Dettagli</span><span class="sxs-lookup"><span data-stu-id="33466-119">-Detailed</span></span>
<span data-ttu-id="33466-120">Se specificato, il cmdlet restituisce la raccolta con il valore di throughput corrispondente.</span><span class="sxs-lookup"><span data-stu-id="33466-120">If provided then, the cmdlet returns the collection with the corresponding throughput value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33466-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33466-121">-InputObject</span></span>
<span data-ttu-id="33466-122">Oggetto di database Mongo.</span><span class="sxs-lookup"><span data-stu-id="33466-122">Mongo Database object.</span></span>

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

### <span data-ttu-id="33466-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="33466-123">-Name</span></span>
<span data-ttu-id="33466-124">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="33466-124">Collection name.</span></span>

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

### <span data-ttu-id="33466-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33466-125">-ResourceGroupName</span></span>
<span data-ttu-id="33466-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="33466-126">Name of resource group.</span></span>

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

### <span data-ttu-id="33466-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33466-127">CommonParameters</span></span>
<span data-ttu-id="33466-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33466-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33466-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="33466-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33466-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="33466-130">INPUTS</span></span>

### <span data-ttu-id="33466-131">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="33466-131">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="33466-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="33466-132">OUTPUTS</span></span>

### <span data-ttu-id="33466-133">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="33466-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="33466-134">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="33466-134">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="33466-135">Note</span><span class="sxs-lookup"><span data-stu-id="33466-135">NOTES</span></span>

## <span data-ttu-id="33466-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="33466-136">RELATED LINKS</span></span>
