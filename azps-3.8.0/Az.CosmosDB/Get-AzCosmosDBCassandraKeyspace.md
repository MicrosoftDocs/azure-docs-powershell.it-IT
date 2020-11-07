---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: cd9c9ba5f46ec83cf9b804e103ad1038662ca271
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864505"
---
# <span data-ttu-id="0a9dd-101">Get-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="0a9dd-101">Get-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="0a9dd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0a9dd-102">SYNOPSIS</span></span>
<span data-ttu-id="0a9dd-103">Ottiene uno spazio di CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="0a9dd-103">Gets a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="0a9dd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0a9dd-104">SYNTAX</span></span>

### <span data-ttu-id="0a9dd-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0a9dd-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a9dd-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a9dd-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspace [-Name <String>] -InputObject <PSDatabaseAccount> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a9dd-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0a9dd-107">DESCRIPTION</span></span>
<span data-ttu-id="0a9dd-108">Il cmdlet **Get-AzCosmosDBCassandraKeyspace** crea un nuovo o aggiorna uno spazio dei CosmosDB Cassandra esistente.</span><span class="sxs-lookup"><span data-stu-id="0a9dd-108">The **Get-AzCosmosDBCassandraKeyspace** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="0a9dd-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0a9dd-109">EXAMPLES</span></span>

### <span data-ttu-id="0a9dd-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0a9dd-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="0a9dd-111">Get-AzCosmosDBCassandraKeyspace ottiene le proprietà di un CassandraKeyspace esistente.</span><span class="sxs-lookup"><span data-stu-id="0a9dd-111">Get-AzCosmosDBCassandraKeyspace gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="0a9dd-112">Puoi espandere la risorsa per ottenere le proprietà _etag, _ts, _rid.</span><span class="sxs-lookup"><span data-stu-id="0a9dd-112">You can expand the Resource to get the _etag, _ts, _rid properties.</span></span>

## <span data-ttu-id="0a9dd-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0a9dd-113">PARAMETERS</span></span>

### <span data-ttu-id="0a9dd-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0a9dd-114">-AccountName</span></span>
<span data-ttu-id="0a9dd-115">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="0a9dd-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0a9dd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a9dd-116">-DefaultProfile</span></span>
<span data-ttu-id="0a9dd-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0a9dd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a9dd-118">-Dettagli</span><span class="sxs-lookup"><span data-stu-id="0a9dd-118">-Detailed</span></span>
<span data-ttu-id="0a9dd-119">Se specificato, il cmdlet restituisce lo spazio dei valori con il valore di throughput corrispondente.</span><span class="sxs-lookup"><span data-stu-id="0a9dd-119">If provided then, the cmdlet returns the Keyspace with the corresponding throughput value.</span></span>

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

### <span data-ttu-id="0a9dd-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a9dd-120">-InputObject</span></span>
<span data-ttu-id="0a9dd-121">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="0a9dd-121">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a9dd-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="0a9dd-122">-Name</span></span>
<span data-ttu-id="0a9dd-123">Nome della barra spaziatrice Cassandra.</span><span class="sxs-lookup"><span data-stu-id="0a9dd-123">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="0a9dd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a9dd-124">-ResourceGroupName</span></span>
<span data-ttu-id="0a9dd-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0a9dd-125">Name of resource group.</span></span>

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

### <span data-ttu-id="0a9dd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a9dd-126">CommonParameters</span></span>
<span data-ttu-id="0a9dd-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a9dd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a9dd-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0a9dd-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a9dd-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0a9dd-129">INPUTS</span></span>

### <span data-ttu-id="0a9dd-130">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="0a9dd-130">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="0a9dd-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0a9dd-131">OUTPUTS</span></span>

### <span data-ttu-id="0a9dd-132">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="0a9dd-132">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="0a9dd-133">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="0a9dd-133">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="0a9dd-134">Note</span><span class="sxs-lookup"><span data-stu-id="0a9dd-134">NOTES</span></span>

## <span data-ttu-id="0a9dd-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0a9dd-135">RELATED LINKS</span></span>
