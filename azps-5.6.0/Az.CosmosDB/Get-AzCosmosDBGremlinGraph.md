---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 4818f0bb179274181c998c4ad07ca013ade0a2b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983629"
---
# <span data-ttu-id="c07c4-101">Get-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="c07c4-101">Get-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="c07c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c07c4-102">SYNOPSIS</span></span>
<span data-ttu-id="c07c4-103">Recupera il diagramma di Gremlin della AMMORT.</span><span class="sxs-lookup"><span data-stu-id="c07c4-103">Gets the CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="c07c4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c07c4-104">SYNTAX</span></span>

### <span data-ttu-id="c07c4-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c07c4-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraph -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="c07c4-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c07c4-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraph [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c07c4-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c07c4-107">DESCRIPTION</span></span>
<span data-ttu-id="c07c4-108">Il cmdlet **Get-AzCosmosDBGremlinGraph** ottiene le proprietà DieresDB Gremlin Graph.</span><span class="sxs-lookup"><span data-stu-id="c07c4-108">The **Get-AzCosmosDBGremlinGraph** cmdlet gets the CosmosDB Gremlin Graph properties.</span></span>

## <span data-ttu-id="c07c4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c07c4-109">EXAMPLES</span></span>

### <span data-ttu-id="c07c4-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c07c4-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

<span data-ttu-id="c07c4-111">L'oggetto risorsa contiene IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="c07c4-111">Resource Object contains IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span></span>

## <span data-ttu-id="c07c4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c07c4-112">PARAMETERS</span></span>

### <span data-ttu-id="c07c4-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c07c4-113">-AccountName</span></span>
<span data-ttu-id="c07c4-114">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="c07c4-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c07c4-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c07c4-115">-DatabaseName</span></span>
<span data-ttu-id="c07c4-116">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="c07c4-116">Database name.</span></span>

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

### <span data-ttu-id="c07c4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c07c4-117">-DefaultProfile</span></span>
<span data-ttu-id="c07c4-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c07c4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c07c4-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c07c4-119">-Name</span></span>
<span data-ttu-id="c07c4-120">Nome del grafo Gremlin.</span><span class="sxs-lookup"><span data-stu-id="c07c4-120">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="c07c4-121">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c07c4-121">-ParentObject</span></span>
<span data-ttu-id="c07c4-122">Oggetto di database Gremlin.</span><span class="sxs-lookup"><span data-stu-id="c07c4-122">Gremlin Database object.</span></span>

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

### <span data-ttu-id="c07c4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c07c4-123">-ResourceGroupName</span></span>
<span data-ttu-id="c07c4-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c07c4-124">Name of resource group.</span></span>

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

### <span data-ttu-id="c07c4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c07c4-125">CommonParameters</span></span>
<span data-ttu-id="c07c4-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c07c4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c07c4-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c07c4-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c07c4-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="c07c4-128">INPUTS</span></span>

### <span data-ttu-id="c07c4-129">Microsoft.Azure.Commands.GenesDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="c07c4-129">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="c07c4-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c07c4-130">OUTPUTS</span></span>

### <span data-ttu-id="c07c4-131">Microsoft.Azure.Commands.GenesDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="c07c4-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="c07c4-132">Microsoft.Azure.Commands.EnterpriseDb.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="c07c4-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="c07c4-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="c07c4-133">NOTES</span></span>

## <span data-ttu-id="c07c4-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c07c4-134">RELATED LINKS</span></span>
