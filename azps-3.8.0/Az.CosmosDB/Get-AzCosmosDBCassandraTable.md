---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
ms.openlocfilehash: ca78194e0e47b07d2d0d061829bf4db38d85632a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022085"
---
# <span data-ttu-id="493cf-101">Get-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="493cf-101">Get-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="493cf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="493cf-102">SYNOPSIS</span></span>
<span data-ttu-id="493cf-103">Ottiene una tabella di CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="493cf-103">Gets a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="493cf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="493cf-104">SYNTAX</span></span>

### <span data-ttu-id="493cf-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="493cf-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTable -AccountName <String> -KeyspaceName <String> -ResourceGroupName <String>
 [-Name <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="493cf-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="493cf-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTable [-Name <String>] -InputObject <PSCassandraKeyspaceGetResults> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="493cf-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="493cf-107">DESCRIPTION</span></span>
<span data-ttu-id="493cf-108">Il cmdlet **Get-AzCosmosDBCassandraTable** crea un nuovo o aggiorna uno spazio dei CosmosDB Cassandra esistente.</span><span class="sxs-lookup"><span data-stu-id="493cf-108">The **Get-AzCosmosDBCassandraTable** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="493cf-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="493cf-109">EXAMPLES</span></span>

### <span data-ttu-id="493cf-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="493cf-110">Example 1</span></span>
```powershell
PS C:\> $table = Get-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="493cf-111">{{Get-AzCosmosDBCassandraTable ottiene le proprietà di un CassandraKeyspace esistente.</span><span class="sxs-lookup"><span data-stu-id="493cf-111">{{ Get-AzCosmosDBCassandraTable gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="493cf-112">È possibile espandere la risorsa per ottenere DefaultTtl, schema, _etag, _ts, _rid proprietà.}}</span><span class="sxs-lookup"><span data-stu-id="493cf-112">You can expand the Resource to get the DefaultTtl, Schema, _etag, _ts, _rid properties.}}</span></span>

## <span data-ttu-id="493cf-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="493cf-113">PARAMETERS</span></span>

### <span data-ttu-id="493cf-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="493cf-114">-AccountName</span></span>
<span data-ttu-id="493cf-115">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="493cf-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="493cf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="493cf-116">-DefaultProfile</span></span>
<span data-ttu-id="493cf-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="493cf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="493cf-118">-Dettagli</span><span class="sxs-lookup"><span data-stu-id="493cf-118">-Detailed</span></span>
<span data-ttu-id="493cf-119">Se specificato, il cmdlet restituisce la tabella Cassandra con il valore di throughput corrispondente.</span><span class="sxs-lookup"><span data-stu-id="493cf-119">If provided then, the cmdlet returns the Cassandra Table with the corresponding throughput value.</span></span>

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

### <span data-ttu-id="493cf-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="493cf-120">-InputObject</span></span>
<span data-ttu-id="493cf-121">Oggetto portaspazio Cassandra.</span><span class="sxs-lookup"><span data-stu-id="493cf-121">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="493cf-122">-Barra spaziatrice</span><span class="sxs-lookup"><span data-stu-id="493cf-122">-KeyspaceName</span></span>
<span data-ttu-id="493cf-123">Nome della barra spaziatrice Cassandra.</span><span class="sxs-lookup"><span data-stu-id="493cf-123">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="493cf-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="493cf-124">-Name</span></span>
<span data-ttu-id="493cf-125">Nome tabella Cassandra.</span><span class="sxs-lookup"><span data-stu-id="493cf-125">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="493cf-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="493cf-126">-ResourceGroupName</span></span>
<span data-ttu-id="493cf-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="493cf-127">Name of resource group.</span></span>

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

### <span data-ttu-id="493cf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="493cf-128">CommonParameters</span></span>
<span data-ttu-id="493cf-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="493cf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="493cf-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="493cf-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="493cf-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="493cf-131">INPUTS</span></span>

### <span data-ttu-id="493cf-132">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="493cf-132">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="493cf-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="493cf-133">OUTPUTS</span></span>

### <span data-ttu-id="493cf-134">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="493cf-134">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="493cf-135">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="493cf-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="493cf-136">Note</span><span class="sxs-lookup"><span data-stu-id="493cf-136">NOTES</span></span>

## <span data-ttu-id="493cf-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="493cf-137">RELATED LINKS</span></span>
