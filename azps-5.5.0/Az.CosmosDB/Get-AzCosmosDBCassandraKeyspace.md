---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 30e550ae8670547e6f87ed022053bcbef7927867
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199070"
---
# <span data-ttu-id="9ce3d-101">Get-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="9ce3d-101">Get-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="9ce3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ce3d-102">SYNOPSIS</span></span>
<span data-ttu-id="9ce3d-103">Ottiene un elemento Db Cassandra Keyspace.</span><span class="sxs-lookup"><span data-stu-id="9ce3d-103">Gets a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="9ce3d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9ce3d-104">SYNTAX</span></span>

### <span data-ttu-id="9ce3d-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9ce3d-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ce3d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ce3d-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspace [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ce3d-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9ce3d-107">DESCRIPTION</span></span>
<span data-ttu-id="9ce3d-108">Il cmdlet **Get-AzCosmosDBCassandraKeyspace** crea un nuovo elemento o aggiorna un elemento Esistente CassasDB Cassandra Keyspace.</span><span class="sxs-lookup"><span data-stu-id="9ce3d-108">The **Get-AzCosmosDBCassandraKeyspace** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="9ce3d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9ce3d-109">EXAMPLES</span></span>

### <span data-ttu-id="9ce3d-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9ce3d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="9ce3d-111">Get-AzCosmosDBCassandraKeyspace ottiene le proprietà di una cassandraKeyspace esistente.</span><span class="sxs-lookup"><span data-stu-id="9ce3d-111">Get-AzCosmosDBCassandraKeyspace gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="9ce3d-112">È possibile espandere la risorsa per ottenere le _etag proprietà _ts, _rid risorsa.</span><span class="sxs-lookup"><span data-stu-id="9ce3d-112">You can expand the Resource to get the _etag, _ts, _rid properties.</span></span>

## <span data-ttu-id="9ce3d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ce3d-113">PARAMETERS</span></span>

### <span data-ttu-id="9ce3d-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9ce3d-114">-AccountName</span></span>
<span data-ttu-id="9ce3d-115">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="9ce3d-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9ce3d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ce3d-116">-DefaultProfile</span></span>
<span data-ttu-id="9ce3d-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9ce3d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ce3d-118">-Name</span><span class="sxs-lookup"><span data-stu-id="9ce3d-118">-Name</span></span>
<span data-ttu-id="9ce3d-119">Nome spazio tasti Cassandra.</span><span class="sxs-lookup"><span data-stu-id="9ce3d-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="9ce3d-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9ce3d-120">-ParentObject</span></span>
<span data-ttu-id="9ce3d-121">Oggetto AccountDb Disa</span><span class="sxs-lookup"><span data-stu-id="9ce3d-121">CosmosDB Account object</span></span>

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

### <span data-ttu-id="9ce3d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ce3d-122">-ResourceGroupName</span></span>
<span data-ttu-id="9ce3d-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9ce3d-123">Name of resource group.</span></span>

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

### <span data-ttu-id="9ce3d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ce3d-124">CommonParameters</span></span>
<span data-ttu-id="9ce3d-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ce3d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ce3d-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9ce3d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ce3d-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="9ce3d-127">INPUTS</span></span>

### <span data-ttu-id="9ce3d-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="9ce3d-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="9ce3d-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9ce3d-129">OUTPUTS</span></span>

### <span data-ttu-id="9ce3d-130">Microsoft.Azure.Commands.EnterpriseDb.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="9ce3d-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="9ce3d-131">Microsoft.Azure.Commands.EnterpriseDb.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="9ce3d-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="9ce3d-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="9ce3d-132">NOTES</span></span>

## <span data-ttu-id="9ce3d-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9ce3d-133">RELATED LINKS</span></span>
