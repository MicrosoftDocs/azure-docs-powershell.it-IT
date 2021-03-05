---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbgremlindatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabaseThroughput.md
ms.openlocfilehash: 4dbfea5106b46bd8d0f1efc1926841dd964b0299
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983645"
---
# <span data-ttu-id="a6431-101">Get-AzCosmosDBGremlinDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="a6431-101">Get-AzCosmosDBGremlinDatabaseThroughput</span></span>

## <span data-ttu-id="a6431-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6431-102">SYNOPSIS</span></span>
<span data-ttu-id="a6431-103">Ottiene la velocità effettiva di un database DiametiDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="a6431-103">Gets the throughput of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="a6431-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a6431-104">SYNTAX</span></span>

### <span data-ttu-id="a6431-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a6431-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6431-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6431-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6431-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a6431-107">DESCRIPTION</span></span>
<span data-ttu-id="a6431-108">Il cmdlet **Get-AzCosmosDBGremlinDatabaseThroughput** ottiene la velocità effettiva di un database Di maisDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="a6431-108">The **Get-AzCosmosDBGremlinDatabaseThroughput** cmdlet gets the throughput of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="a6431-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a6431-109">EXAMPLES</span></span>

### <span data-ttu-id="a6431-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a6431-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinDatabaseThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}
Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="a6431-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6431-111">PARAMETERS</span></span>

### <span data-ttu-id="a6431-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a6431-112">-AccountName</span></span>
<span data-ttu-id="a6431-113">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="a6431-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a6431-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6431-114">-DefaultProfile</span></span>
<span data-ttu-id="a6431-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a6431-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6431-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6431-116">-InputObject</span></span>
<span data-ttu-id="a6431-117">Oggetto Account Aziendale</span><span class="sxs-lookup"><span data-stu-id="a6431-117">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6431-118">-Name</span><span class="sxs-lookup"><span data-stu-id="a6431-118">-Name</span></span>
<span data-ttu-id="a6431-119">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="a6431-119">Database name.</span></span>

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

### <span data-ttu-id="a6431-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6431-120">-ResourceGroupName</span></span>
<span data-ttu-id="a6431-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a6431-121">Name of resource group.</span></span>

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

### <span data-ttu-id="a6431-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6431-122">CommonParameters</span></span>
<span data-ttu-id="a6431-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6431-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6431-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a6431-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6431-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="a6431-125">INPUTS</span></span>

### <span data-ttu-id="a6431-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a6431-126">None</span></span>

## <span data-ttu-id="a6431-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a6431-127">OUTPUTS</span></span>

### <span data-ttu-id="a6431-128">Microsoft.Azure.Commands.EnterpriseDb.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="a6431-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="a6431-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="a6431-129">NOTES</span></span>

## <span data-ttu-id="a6431-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a6431-130">RELATED LINKS</span></span>
