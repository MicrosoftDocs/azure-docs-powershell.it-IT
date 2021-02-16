---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspacethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
ms.openlocfilehash: d6d00892a8650964fbe7560ffa8e5fe279fb103b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199063"
---
# <span data-ttu-id="186de-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span><span class="sxs-lookup"><span data-stu-id="186de-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span></span>

## <span data-ttu-id="186de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="186de-102">SYNOPSIS</span></span>
<span data-ttu-id="186de-103">Ottiene il valore di velocità effettiva di Cassandra Keyspace.</span><span class="sxs-lookup"><span data-stu-id="186de-103">Gets the throughput value of the Cassandra Keyspace.</span></span>

## <span data-ttu-id="186de-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="186de-104">SYNTAX</span></span>

### <span data-ttu-id="186de-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="186de-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="186de-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="186de-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="186de-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="186de-107">DESCRIPTION</span></span>
<span data-ttu-id="186de-108">Il cmdlet **Get-AzCosmosDBCassandraKeyspaceThroughput** ottiene l'oggetto velocità effettiva corrispondente a un determinato keyspace.</span><span class="sxs-lookup"><span data-stu-id="186de-108">The **Get-AzCosmosDBCassandraKeyspaceThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="186de-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="186de-109">EXAMPLES</span></span>

### <span data-ttu-id="186de-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="186de-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}
```

## <span data-ttu-id="186de-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="186de-111">PARAMETERS</span></span>

### <span data-ttu-id="186de-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="186de-112">-AccountName</span></span>
<span data-ttu-id="186de-113">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="186de-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="186de-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="186de-114">-DefaultProfile</span></span>
<span data-ttu-id="186de-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="186de-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="186de-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="186de-116">-InputObject</span></span>
<span data-ttu-id="186de-117">Oggetto AccountDb Disa</span><span class="sxs-lookup"><span data-stu-id="186de-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="186de-118">-Name</span><span class="sxs-lookup"><span data-stu-id="186de-118">-Name</span></span>
<span data-ttu-id="186de-119">Nome spazio tasti Cassandra.</span><span class="sxs-lookup"><span data-stu-id="186de-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="186de-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="186de-120">-ResourceGroupName</span></span>
<span data-ttu-id="186de-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="186de-121">Name of resource group.</span></span>

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

### <span data-ttu-id="186de-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="186de-122">CommonParameters</span></span>
<span data-ttu-id="186de-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="186de-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="186de-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="186de-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="186de-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="186de-125">INPUTS</span></span>

### <span data-ttu-id="186de-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="186de-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="186de-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="186de-127">OUTPUTS</span></span>

### <span data-ttu-id="186de-128">Microsoft.Azure.Commands.EnterpriseDb.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="186de-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="186de-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="186de-129">NOTES</span></span>

## <span data-ttu-id="186de-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="186de-130">RELATED LINKS</span></span>
