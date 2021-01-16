---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 1b8bcbdeb797aea0faa5e9b3a0b5cb1e36b0f1b9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343912"
---
# <span data-ttu-id="0871b-101">Get-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="0871b-101">Get-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="0871b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0871b-102">SYNOPSIS</span></span>
<span data-ttu-id="0871b-103">Ottiene il grafico Gremlin CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="0871b-103">Gets the CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="0871b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0871b-104">SYNTAX</span></span>

### <span data-ttu-id="0871b-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0871b-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraph -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="0871b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0871b-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraph [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0871b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0871b-107">DESCRIPTION</span></span>
<span data-ttu-id="0871b-108">Il cmdlet **Get-AzCosmosDBGremlinGraph** ottiene le proprietà del grafico Gremlin di CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="0871b-108">The **Get-AzCosmosDBGremlinGraph** cmdlet gets the CosmosDB Gremlin Graph properties.</span></span>

## <span data-ttu-id="0871b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0871b-109">EXAMPLES</span></span>

### <span data-ttu-id="0871b-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0871b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

<span data-ttu-id="0871b-111">Oggetto Resource contiene IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="0871b-111">Resource Object contains IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span></span>

## <span data-ttu-id="0871b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0871b-112">PARAMETERS</span></span>

### <span data-ttu-id="0871b-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0871b-113">-AccountName</span></span>
<span data-ttu-id="0871b-114">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="0871b-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0871b-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0871b-115">-DatabaseName</span></span>
<span data-ttu-id="0871b-116">Nome database.</span><span class="sxs-lookup"><span data-stu-id="0871b-116">Database name.</span></span>

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

### <span data-ttu-id="0871b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0871b-117">-DefaultProfile</span></span>
<span data-ttu-id="0871b-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0871b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0871b-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="0871b-119">-Name</span></span>
<span data-ttu-id="0871b-120">Nome del grafico Gremlin.</span><span class="sxs-lookup"><span data-stu-id="0871b-120">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="0871b-121">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0871b-121">-ParentObject</span></span>
<span data-ttu-id="0871b-122">Oggetto database Gremlin.</span><span class="sxs-lookup"><span data-stu-id="0871b-122">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0871b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0871b-123">-ResourceGroupName</span></span>
<span data-ttu-id="0871b-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0871b-124">Name of resource group.</span></span>

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

### <span data-ttu-id="0871b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0871b-125">CommonParameters</span></span>
<span data-ttu-id="0871b-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0871b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0871b-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0871b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0871b-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0871b-128">INPUTS</span></span>

### <span data-ttu-id="0871b-129">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="0871b-129">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="0871b-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0871b-130">OUTPUTS</span></span>

### <span data-ttu-id="0871b-131">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="0871b-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="0871b-132">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="0871b-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="0871b-133">Note</span><span class="sxs-lookup"><span data-stu-id="0871b-133">NOTES</span></span>

## <span data-ttu-id="0871b-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0871b-134">RELATED LINKS</span></span>
