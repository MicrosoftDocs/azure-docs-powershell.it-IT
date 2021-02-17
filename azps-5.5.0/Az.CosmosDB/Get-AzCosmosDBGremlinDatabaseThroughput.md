---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlindatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabaseThroughput.md
ms.openlocfilehash: 8905f4e4ffc4268b74ce57bfaf1bcb14565f70fd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199038"
---
# <span data-ttu-id="ac906-101">Get-AzCosmosDBGremlinDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="ac906-101">Get-AzCosmosDBGremlinDatabaseThroughput</span></span>

## <span data-ttu-id="ac906-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac906-102">SYNOPSIS</span></span>
<span data-ttu-id="ac906-103">Ottiene la velocità effettiva di un database DiametiDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="ac906-103">Gets the throughput of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="ac906-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ac906-104">SYNTAX</span></span>

### <span data-ttu-id="ac906-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ac906-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac906-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac906-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac906-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ac906-107">DESCRIPTION</span></span>
<span data-ttu-id="ac906-108">Il cmdlet **Get-AzCosmosDBGremlinDatabaseThroughput** ottiene la velocità effettiva di un database Di maiodiDb Gremlin.</span><span class="sxs-lookup"><span data-stu-id="ac906-108">The **Get-AzCosmosDBGremlinDatabaseThroughput** cmdlet gets the throughput of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="ac906-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ac906-109">EXAMPLES</span></span>

### <span data-ttu-id="ac906-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ac906-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinDatabaseThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}
Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="ac906-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac906-111">PARAMETERS</span></span>

### <span data-ttu-id="ac906-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ac906-112">-AccountName</span></span>
<span data-ttu-id="ac906-113">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="ac906-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ac906-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac906-114">-DefaultProfile</span></span>
<span data-ttu-id="ac906-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ac906-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac906-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac906-116">-InputObject</span></span>
<span data-ttu-id="ac906-117">Oggetto AccountDb Disa</span><span class="sxs-lookup"><span data-stu-id="ac906-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="ac906-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ac906-118">-Name</span></span>
<span data-ttu-id="ac906-119">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="ac906-119">Database name.</span></span>

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

### <span data-ttu-id="ac906-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac906-120">-ResourceGroupName</span></span>
<span data-ttu-id="ac906-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ac906-121">Name of resource group.</span></span>

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

### <span data-ttu-id="ac906-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac906-122">CommonParameters</span></span>
<span data-ttu-id="ac906-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac906-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac906-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ac906-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac906-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="ac906-125">INPUTS</span></span>

### <span data-ttu-id="ac906-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ac906-126">None</span></span>

## <span data-ttu-id="ac906-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ac906-127">OUTPUTS</span></span>

### <span data-ttu-id="ac906-128">Microsoft.Azure.Commands.EnterpriseDb.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="ac906-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="ac906-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="ac906-129">NOTES</span></span>

## <span data-ttu-id="ac906-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ac906-130">RELATED LINKS</span></span>
