---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 8994cab45a10f874d0c544f231e20c27a01039f4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299568"
---
# <span data-ttu-id="12e3c-101">Get-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="12e3c-101">Get-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="12e3c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="12e3c-102">SYNOPSIS</span></span>
<span data-ttu-id="12e3c-103">Ottiene una tabella di CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="12e3c-103">Gets a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="12e3c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="12e3c-104">SYNTAX</span></span>

### <span data-ttu-id="12e3c-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="12e3c-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTable -AccountName <String> -KeyspaceName <String> -ResourceGroupName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12e3c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="12e3c-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTable [-Name <String>] -ParentObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12e3c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12e3c-107">DESCRIPTION</span></span>
<span data-ttu-id="12e3c-108">Il cmdlet **Get-AzCosmosDBCassandraTable** crea un nuovo o aggiorna uno spazio dei CosmosDB Cassandra esistente.</span><span class="sxs-lookup"><span data-stu-id="12e3c-108">The **Get-AzCosmosDBCassandraTable** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="12e3c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="12e3c-109">EXAMPLES</span></span>

### <span data-ttu-id="12e3c-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="12e3c-110">Example 1</span></span>
```powershell
PS C:\> $table = Get-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="12e3c-111">{{Get-AzCosmosDBCassandraTable ottiene le proprietà di un CassandraKeyspace esistente.</span><span class="sxs-lookup"><span data-stu-id="12e3c-111">{{ Get-AzCosmosDBCassandraTable gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="12e3c-112">È possibile espandere la risorsa per ottenere DefaultTtl, schema, _etag, _ts, _rid proprietà.}}</span><span class="sxs-lookup"><span data-stu-id="12e3c-112">You can expand the Resource to get the DefaultTtl, Schema, _etag, _ts, _rid properties.}}</span></span>

## <span data-ttu-id="12e3c-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="12e3c-113">PARAMETERS</span></span>

### <span data-ttu-id="12e3c-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="12e3c-114">-AccountName</span></span>
<span data-ttu-id="12e3c-115">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="12e3c-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="12e3c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12e3c-116">-DefaultProfile</span></span>
<span data-ttu-id="12e3c-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="12e3c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12e3c-118">-Barra spaziatrice</span><span class="sxs-lookup"><span data-stu-id="12e3c-118">-KeyspaceName</span></span>
<span data-ttu-id="12e3c-119">Nome della barra spaziatrice Cassandra.</span><span class="sxs-lookup"><span data-stu-id="12e3c-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="12e3c-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="12e3c-120">-Name</span></span>
<span data-ttu-id="12e3c-121">Nome tabella Cassandra.</span><span class="sxs-lookup"><span data-stu-id="12e3c-121">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="12e3c-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="12e3c-122">-ParentObject</span></span>
<span data-ttu-id="12e3c-123">Oggetto portaspazio Cassandra.</span><span class="sxs-lookup"><span data-stu-id="12e3c-123">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="12e3c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12e3c-124">-ResourceGroupName</span></span>
<span data-ttu-id="12e3c-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="12e3c-125">Name of resource group.</span></span>

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

### <span data-ttu-id="12e3c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12e3c-126">CommonParameters</span></span>
<span data-ttu-id="12e3c-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12e3c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12e3c-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12e3c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12e3c-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="12e3c-129">INPUTS</span></span>

### <span data-ttu-id="12e3c-130">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="12e3c-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="12e3c-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="12e3c-131">OUTPUTS</span></span>

### <span data-ttu-id="12e3c-132">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="12e3c-132">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="12e3c-133">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="12e3c-133">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="12e3c-134">Note</span><span class="sxs-lookup"><span data-stu-id="12e3c-134">NOTES</span></span>

## <span data-ttu-id="12e3c-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="12e3c-135">RELATED LINKS</span></span>
