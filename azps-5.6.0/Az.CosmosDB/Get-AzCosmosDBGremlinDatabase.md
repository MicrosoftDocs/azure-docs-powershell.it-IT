---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 7268eff2163e408975b1711dcac4fbf8454f0b76
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004366"
---
# <span data-ttu-id="a7d39-101">Get-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="a7d39-101">Get-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="a7d39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7d39-102">SYNOPSIS</span></span>
<span data-ttu-id="a7d39-103">Ottiene il database DellesDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="a7d39-103">Gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="a7d39-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a7d39-104">SYNTAX</span></span>

### <span data-ttu-id="a7d39-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a7d39-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7d39-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7d39-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7d39-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a7d39-107">DESCRIPTION</span></span>
<span data-ttu-id="a7d39-108">Il cmdlet **Get-AzCosmosDBGremlinDatabase** ottiene il databaseDbDb Gremlin Database.</span><span class="sxs-lookup"><span data-stu-id="a7d39-108">The **Get-AzCosmosDBGremlinDatabase** cmdlet gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="a7d39-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a7d39-109">EXAMPLES</span></span>

### <span data-ttu-id="a7d39-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a7d39-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

<span data-ttu-id="a7d39-111">L'oggetto risorsa _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="a7d39-111">Resource Object contains _rid, _ts, _etag.</span></span>

## <span data-ttu-id="a7d39-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7d39-112">PARAMETERS</span></span>

### <span data-ttu-id="a7d39-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a7d39-113">-AccountName</span></span>
<span data-ttu-id="a7d39-114">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="a7d39-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a7d39-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7d39-115">-DefaultProfile</span></span>
<span data-ttu-id="a7d39-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a7d39-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7d39-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a7d39-117">-Name</span></span>
<span data-ttu-id="a7d39-118">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="a7d39-118">Database name.</span></span>

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

### <span data-ttu-id="a7d39-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a7d39-119">-ParentObject</span></span>
<span data-ttu-id="a7d39-120">Oggetto Account Aziendale</span><span class="sxs-lookup"><span data-stu-id="a7d39-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="a7d39-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7d39-121">-ResourceGroupName</span></span>
<span data-ttu-id="a7d39-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a7d39-122">Name of resource group.</span></span>

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

### <span data-ttu-id="a7d39-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7d39-123">CommonParameters</span></span>
<span data-ttu-id="a7d39-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7d39-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7d39-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a7d39-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7d39-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="a7d39-126">INPUTS</span></span>

### <span data-ttu-id="a7d39-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="a7d39-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="a7d39-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a7d39-128">OUTPUTS</span></span>

### <span data-ttu-id="a7d39-129">Microsoft.Azure.Commands.GenesDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="a7d39-129">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="a7d39-130">Microsoft.Azure.Commands.EnterpriseDb.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="a7d39-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="a7d39-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="a7d39-131">NOTES</span></span>

## <span data-ttu-id="a7d39-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a7d39-132">RELATED LINKS</span></span>
