---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 30e550ae8670547e6f87ed022053bcbef7927867
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299575"
---
# <span data-ttu-id="5fb20-101">Get-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="5fb20-101">Get-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="5fb20-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5fb20-102">SYNOPSIS</span></span>
<span data-ttu-id="5fb20-103">Ottiene uno spazio di CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="5fb20-103">Gets a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="5fb20-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5fb20-104">SYNTAX</span></span>

### <span data-ttu-id="5fb20-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5fb20-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5fb20-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5fb20-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspace [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5fb20-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5fb20-107">DESCRIPTION</span></span>
<span data-ttu-id="5fb20-108">Il cmdlet **Get-AzCosmosDBCassandraKeyspace** crea un nuovo o aggiorna uno spazio dei CosmosDB Cassandra esistente.</span><span class="sxs-lookup"><span data-stu-id="5fb20-108">The **Get-AzCosmosDBCassandraKeyspace** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="5fb20-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5fb20-109">EXAMPLES</span></span>

### <span data-ttu-id="5fb20-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5fb20-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="5fb20-111">Get-AzCosmosDBCassandraKeyspace ottiene le proprietà di un CassandraKeyspace esistente.</span><span class="sxs-lookup"><span data-stu-id="5fb20-111">Get-AzCosmosDBCassandraKeyspace gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="5fb20-112">Puoi espandere la risorsa per ottenere le proprietà _etag, _ts, _rid.</span><span class="sxs-lookup"><span data-stu-id="5fb20-112">You can expand the Resource to get the _etag, _ts, _rid properties.</span></span>

## <span data-ttu-id="5fb20-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5fb20-113">PARAMETERS</span></span>

### <span data-ttu-id="5fb20-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5fb20-114">-AccountName</span></span>
<span data-ttu-id="5fb20-115">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="5fb20-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5fb20-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fb20-116">-DefaultProfile</span></span>
<span data-ttu-id="5fb20-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5fb20-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fb20-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="5fb20-118">-Name</span></span>
<span data-ttu-id="5fb20-119">Nome della barra spaziatrice Cassandra.</span><span class="sxs-lookup"><span data-stu-id="5fb20-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="5fb20-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5fb20-120">-ParentObject</span></span>
<span data-ttu-id="5fb20-121">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="5fb20-121">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb20-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fb20-122">-ResourceGroupName</span></span>
<span data-ttu-id="5fb20-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5fb20-123">Name of resource group.</span></span>

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

### <span data-ttu-id="5fb20-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fb20-124">CommonParameters</span></span>
<span data-ttu-id="5fb20-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fb20-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fb20-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5fb20-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fb20-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5fb20-127">INPUTS</span></span>

### <span data-ttu-id="5fb20-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="5fb20-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="5fb20-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5fb20-129">OUTPUTS</span></span>

### <span data-ttu-id="5fb20-130">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="5fb20-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="5fb20-131">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="5fb20-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="5fb20-132">Note</span><span class="sxs-lookup"><span data-stu-id="5fb20-132">NOTES</span></span>

## <span data-ttu-id="5fb20-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5fb20-133">RELATED LINKS</span></span>
