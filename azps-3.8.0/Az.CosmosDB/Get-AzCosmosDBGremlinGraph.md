---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 2da3a5729673abde6ad54ea66f1b5fbd9f089db9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022080"
---
# <span data-ttu-id="00a58-101">Get-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="00a58-101">Get-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="00a58-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="00a58-102">SYNOPSIS</span></span>
<span data-ttu-id="00a58-103">Ottiene il grafico Gremlin CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="00a58-103">Gets the CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="00a58-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="00a58-104">SYNTAX</span></span>

### <span data-ttu-id="00a58-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="00a58-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraph -ResourceGroupName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="00a58-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="00a58-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraph [-Name <String>] -InputObject <PSGremlinDatabaseGetResults> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00a58-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="00a58-107">DESCRIPTION</span></span>
<span data-ttu-id="00a58-108">Il cmdlet **Get-AzCosmosDBGremlinGraph** ottiene le proprietà del grafico Gremlin di CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="00a58-108">The **Get-AzCosmosDBGremlinGraph** cmdlet gets the CosmosDB Gremlin Graph properties.</span></span>

## <span data-ttu-id="00a58-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="00a58-109">EXAMPLES</span></span>

### <span data-ttu-id="00a58-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="00a58-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

<span data-ttu-id="00a58-111">Oggetto Resource contiene IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="00a58-111">Resource Object contains IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span></span>

## <span data-ttu-id="00a58-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="00a58-112">PARAMETERS</span></span>

### <span data-ttu-id="00a58-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="00a58-113">-AccountName</span></span>
<span data-ttu-id="00a58-114">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="00a58-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="00a58-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="00a58-115">-DatabaseName</span></span>
<span data-ttu-id="00a58-116">Nome database.</span><span class="sxs-lookup"><span data-stu-id="00a58-116">Database name.</span></span>

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

### <span data-ttu-id="00a58-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00a58-117">-DefaultProfile</span></span>
<span data-ttu-id="00a58-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="00a58-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00a58-119">-Dettagli</span><span class="sxs-lookup"><span data-stu-id="00a58-119">-Detailed</span></span>
<span data-ttu-id="00a58-120">Se specificato, il cmdlet restituisce il grafico Gremlin con il valore di throughput corrispondente.</span><span class="sxs-lookup"><span data-stu-id="00a58-120">If provided then, the cmdlet returns the Gremlin Graph with the corresponding throughput value.</span></span>

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

### <span data-ttu-id="00a58-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00a58-121">-InputObject</span></span>
<span data-ttu-id="00a58-122">Oggetto database Gremlin.</span><span class="sxs-lookup"><span data-stu-id="00a58-122">Gremlin Database object.</span></span>

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

### <span data-ttu-id="00a58-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="00a58-123">-Name</span></span>
<span data-ttu-id="00a58-124">Nome del grafico Gremlin.</span><span class="sxs-lookup"><span data-stu-id="00a58-124">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="00a58-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00a58-125">-ResourceGroupName</span></span>
<span data-ttu-id="00a58-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="00a58-126">Name of resource group.</span></span>

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

### <span data-ttu-id="00a58-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00a58-127">CommonParameters</span></span>
<span data-ttu-id="00a58-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00a58-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00a58-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="00a58-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00a58-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="00a58-130">INPUTS</span></span>

### <span data-ttu-id="00a58-131">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="00a58-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="00a58-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="00a58-132">OUTPUTS</span></span>

### <span data-ttu-id="00a58-133">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="00a58-133">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="00a58-134">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="00a58-134">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="00a58-135">Note</span><span class="sxs-lookup"><span data-stu-id="00a58-135">NOTES</span></span>

## <span data-ttu-id="00a58-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="00a58-136">RELATED LINKS</span></span>
