---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspacethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
ms.openlocfilehash: 21a32bc2c3251d0069dcdb05d9eea29c52207ae8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022088"
---
# <span data-ttu-id="db46a-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span><span class="sxs-lookup"><span data-stu-id="db46a-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span></span>

## <span data-ttu-id="db46a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="db46a-102">SYNOPSIS</span></span>
<span data-ttu-id="db46a-103">Ottiene il valore della velocità effettiva dello spazio della spaziatura Cassandra.</span><span class="sxs-lookup"><span data-stu-id="db46a-103">Gets the throughput value of the Cassandra Keyspace.</span></span>

## <span data-ttu-id="db46a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db46a-104">SYNTAX</span></span>

### <span data-ttu-id="db46a-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="db46a-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db46a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db46a-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -Name <String> -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db46a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db46a-107">DESCRIPTION</span></span>
<span data-ttu-id="db46a-108">Il cmdlet **Get-AzCosmosDBCassandraKeyspaceThroughput** Ottiene l'oggetto throughput corrispondente a uno spazio di base specifico.</span><span class="sxs-lookup"><span data-stu-id="db46a-108">The **Get-AzCosmosDBCassandraKeyspaceThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="db46a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db46a-109">EXAMPLES</span></span>

### <span data-ttu-id="db46a-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="db46a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}
```

## <span data-ttu-id="db46a-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="db46a-111">PARAMETERS</span></span>

### <span data-ttu-id="db46a-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="db46a-112">-AccountName</span></span>
<span data-ttu-id="db46a-113">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="db46a-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="db46a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db46a-114">-DefaultProfile</span></span>
<span data-ttu-id="db46a-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="db46a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db46a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db46a-116">-InputObject</span></span>
<span data-ttu-id="db46a-117">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="db46a-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="db46a-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="db46a-118">-Name</span></span>
<span data-ttu-id="db46a-119">Nome della barra spaziatrice Cassandra.</span><span class="sxs-lookup"><span data-stu-id="db46a-119">Cassandra Keyspace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db46a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db46a-120">-ResourceGroupName</span></span>
<span data-ttu-id="db46a-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="db46a-121">Name of resource group.</span></span>

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

### <span data-ttu-id="db46a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db46a-122">CommonParameters</span></span>
<span data-ttu-id="db46a-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db46a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db46a-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db46a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db46a-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="db46a-125">INPUTS</span></span>

### <span data-ttu-id="db46a-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="db46a-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="db46a-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db46a-127">OUTPUTS</span></span>

### <span data-ttu-id="db46a-128">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="db46a-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="db46a-129">Note</span><span class="sxs-lookup"><span data-stu-id="db46a-129">NOTES</span></span>

## <span data-ttu-id="db46a-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db46a-130">RELATED LINKS</span></span>
