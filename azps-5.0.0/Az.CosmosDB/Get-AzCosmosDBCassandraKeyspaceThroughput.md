---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspacethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
ms.openlocfilehash: d6d00892a8650964fbe7560ffa8e5fe279fb103b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299563"
---
# <span data-ttu-id="5d38c-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span><span class="sxs-lookup"><span data-stu-id="5d38c-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span></span>

## <span data-ttu-id="5d38c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5d38c-102">SYNOPSIS</span></span>
<span data-ttu-id="5d38c-103">Ottiene il valore della velocità effettiva dello spazio della spaziatura Cassandra.</span><span class="sxs-lookup"><span data-stu-id="5d38c-103">Gets the throughput value of the Cassandra Keyspace.</span></span>

## <span data-ttu-id="5d38c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5d38c-104">SYNTAX</span></span>

### <span data-ttu-id="5d38c-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5d38c-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d38c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d38c-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d38c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5d38c-107">DESCRIPTION</span></span>
<span data-ttu-id="5d38c-108">Il cmdlet **Get-AzCosmosDBCassandraKeyspaceThroughput** Ottiene l'oggetto throughput corrispondente a uno spazio di base specifico.</span><span class="sxs-lookup"><span data-stu-id="5d38c-108">The **Get-AzCosmosDBCassandraKeyspaceThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="5d38c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5d38c-109">EXAMPLES</span></span>

### <span data-ttu-id="5d38c-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5d38c-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}
```

## <span data-ttu-id="5d38c-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5d38c-111">PARAMETERS</span></span>

### <span data-ttu-id="5d38c-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5d38c-112">-AccountName</span></span>
<span data-ttu-id="5d38c-113">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="5d38c-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5d38c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d38c-114">-DefaultProfile</span></span>
<span data-ttu-id="5d38c-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5d38c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d38c-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d38c-116">-InputObject</span></span>
<span data-ttu-id="5d38c-117">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="5d38c-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="5d38c-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="5d38c-118">-Name</span></span>
<span data-ttu-id="5d38c-119">Nome della barra spaziatrice Cassandra.</span><span class="sxs-lookup"><span data-stu-id="5d38c-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="5d38c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d38c-120">-ResourceGroupName</span></span>
<span data-ttu-id="5d38c-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5d38c-121">Name of resource group.</span></span>

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

### <span data-ttu-id="5d38c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d38c-122">CommonParameters</span></span>
<span data-ttu-id="5d38c-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d38c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d38c-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5d38c-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d38c-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5d38c-125">INPUTS</span></span>

### <span data-ttu-id="5d38c-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="5d38c-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="5d38c-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5d38c-127">OUTPUTS</span></span>

### <span data-ttu-id="5d38c-128">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="5d38c-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="5d38c-129">Note</span><span class="sxs-lookup"><span data-stu-id="5d38c-129">NOTES</span></span>

## <span data-ttu-id="5d38c-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5d38c-130">RELATED LINKS</span></span>
