---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 30e550ae8670547e6f87ed022053bcbef7927867
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190357"
---
# <span data-ttu-id="f59f6-101">Get-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="f59f6-101">Get-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="f59f6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f59f6-102">SYNOPSIS</span></span>
<span data-ttu-id="f59f6-103">Ottiene uno spazio di CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="f59f6-103">Gets a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="f59f6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f59f6-104">SYNTAX</span></span>

### <span data-ttu-id="f59f6-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f59f6-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f59f6-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f59f6-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspace [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f59f6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f59f6-107">DESCRIPTION</span></span>
<span data-ttu-id="f59f6-108">Il cmdlet **Get-AzCosmosDBCassandraKeyspace** crea un nuovo o aggiorna uno spazio dei CosmosDB Cassandra esistente.</span><span class="sxs-lookup"><span data-stu-id="f59f6-108">The **Get-AzCosmosDBCassandraKeyspace** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="f59f6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f59f6-109">EXAMPLES</span></span>

### <span data-ttu-id="f59f6-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f59f6-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="f59f6-111">Get-AzCosmosDBCassandraKeyspace ottiene le proprietà di un CassandraKeyspace esistente.</span><span class="sxs-lookup"><span data-stu-id="f59f6-111">Get-AzCosmosDBCassandraKeyspace gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="f59f6-112">Puoi espandere la risorsa per ottenere le proprietà _etag, _ts, _rid.</span><span class="sxs-lookup"><span data-stu-id="f59f6-112">You can expand the Resource to get the _etag, _ts, _rid properties.</span></span>

## <span data-ttu-id="f59f6-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f59f6-113">PARAMETERS</span></span>

### <span data-ttu-id="f59f6-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f59f6-114">-AccountName</span></span>
<span data-ttu-id="f59f6-115">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="f59f6-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f59f6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f59f6-116">-DefaultProfile</span></span>
<span data-ttu-id="f59f6-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f59f6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f59f6-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="f59f6-118">-Name</span></span>
<span data-ttu-id="f59f6-119">Nome della barra spaziatrice Cassandra.</span><span class="sxs-lookup"><span data-stu-id="f59f6-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="f59f6-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f59f6-120">-ParentObject</span></span>
<span data-ttu-id="f59f6-121">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="f59f6-121">CosmosDB Account object</span></span>

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

### <span data-ttu-id="f59f6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f59f6-122">-ResourceGroupName</span></span>
<span data-ttu-id="f59f6-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f59f6-123">Name of resource group.</span></span>

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

### <span data-ttu-id="f59f6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f59f6-124">CommonParameters</span></span>
<span data-ttu-id="f59f6-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f59f6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f59f6-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f59f6-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f59f6-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f59f6-127">INPUTS</span></span>

### <span data-ttu-id="f59f6-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="f59f6-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="f59f6-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f59f6-129">OUTPUTS</span></span>

### <span data-ttu-id="f59f6-130">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="f59f6-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="f59f6-131">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="f59f6-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="f59f6-132">Note</span><span class="sxs-lookup"><span data-stu-id="f59f6-132">NOTES</span></span>

## <span data-ttu-id="f59f6-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f59f6-133">RELATED LINKS</span></span>
