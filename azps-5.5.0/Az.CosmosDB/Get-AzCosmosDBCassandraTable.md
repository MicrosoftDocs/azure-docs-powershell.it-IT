---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 8994cab45a10f874d0c544f231e20c27a01039f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199047"
---
# <span data-ttu-id="4e038-101">Get-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="4e038-101">Get-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="4e038-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e038-102">SYNOPSIS</span></span>
<span data-ttu-id="4e038-103">Ottiene una tabella della Cassa seguente: Cassandra.</span><span class="sxs-lookup"><span data-stu-id="4e038-103">Gets a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="4e038-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4e038-104">SYNTAX</span></span>

### <span data-ttu-id="4e038-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4e038-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTable -AccountName <String> -KeyspaceName <String> -ResourceGroupName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e038-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e038-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTable [-Name <String>] -ParentObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e038-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4e038-107">DESCRIPTION</span></span>
<span data-ttu-id="4e038-108">Il cmdlet **Get-AzCosmosDBCassandraTable** crea un nuovo elemento o aggiorna un elemento Esistente CassasDB Cassandra Keyspace.</span><span class="sxs-lookup"><span data-stu-id="4e038-108">The **Get-AzCosmosDBCassandraTable** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="4e038-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4e038-109">EXAMPLES</span></span>

### <span data-ttu-id="4e038-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4e038-110">Example 1</span></span>
```powershell
PS C:\> $table = Get-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="4e038-111">{{ Get-AzCosmosDBCassandraTable ottiene le proprietà di una CassandraKeyspace esistente.</span><span class="sxs-lookup"><span data-stu-id="4e038-111">{{ Get-AzCosmosDBCassandraTable gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="4e038-112">È possibile espandere la risorsa per ottenere le proprietà DefaultTtl, Schema, _etag, _ts _rid.}}</span><span class="sxs-lookup"><span data-stu-id="4e038-112">You can expand the Resource to get the DefaultTtl, Schema, _etag, _ts, _rid properties.}}</span></span>

## <span data-ttu-id="4e038-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e038-113">PARAMETERS</span></span>

### <span data-ttu-id="4e038-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4e038-114">-AccountName</span></span>
<span data-ttu-id="4e038-115">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="4e038-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="4e038-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e038-116">-DefaultProfile</span></span>
<span data-ttu-id="4e038-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4e038-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e038-118">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="4e038-118">-KeyspaceName</span></span>
<span data-ttu-id="4e038-119">Nome spazio tasti Cassandra.</span><span class="sxs-lookup"><span data-stu-id="4e038-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="4e038-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4e038-120">-Name</span></span>
<span data-ttu-id="4e038-121">Nome tabella Cassandra.</span><span class="sxs-lookup"><span data-stu-id="4e038-121">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="4e038-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4e038-122">-ParentObject</span></span>
<span data-ttu-id="4e038-123">Oggetto Cassandra Keyspace.</span><span class="sxs-lookup"><span data-stu-id="4e038-123">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e038-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e038-124">-ResourceGroupName</span></span>
<span data-ttu-id="4e038-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4e038-125">Name of resource group.</span></span>

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

### <span data-ttu-id="4e038-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e038-126">CommonParameters</span></span>
<span data-ttu-id="4e038-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e038-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e038-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4e038-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e038-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="4e038-129">INPUTS</span></span>

### <span data-ttu-id="4e038-130">Microsoft.Azure.Commands.EnterpriseDb.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="4e038-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="4e038-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4e038-131">OUTPUTS</span></span>

### <span data-ttu-id="4e038-132">Microsoft.Azure.Commands.EnterpriseDb.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="4e038-132">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="4e038-133">Microsoft.Azure.Commands.EnterpriseDb.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="4e038-133">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="4e038-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="4e038-134">NOTES</span></span>

## <span data-ttu-id="4e038-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4e038-135">RELATED LINKS</span></span>
