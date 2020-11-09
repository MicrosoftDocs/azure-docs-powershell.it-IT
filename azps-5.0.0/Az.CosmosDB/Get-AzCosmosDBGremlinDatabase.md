---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: ba1f6b1ca309226433120ea6a68ec330cabd034c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299556"
---
# <span data-ttu-id="aa4b4-101">Get-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="aa4b4-101">Get-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="aa4b4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aa4b4-102">SYNOPSIS</span></span>
<span data-ttu-id="aa4b4-103">Ottiene il database di CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="aa4b4-103">Gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="aa4b4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aa4b4-104">SYNTAX</span></span>

### <span data-ttu-id="aa4b4-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="aa4b4-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa4b4-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa4b4-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa4b4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aa4b4-107">DESCRIPTION</span></span>
<span data-ttu-id="aa4b4-108">Il cmdlet **Get-AzCosmosDBGremlinDatabase** ottiene il database Gremlin di CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="aa4b4-108">The **Get-AzCosmosDBGremlinDatabase** cmdlet gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="aa4b4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aa4b4-109">EXAMPLES</span></span>

### <span data-ttu-id="aa4b4-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="aa4b4-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

<span data-ttu-id="aa4b4-111">Oggetto Resource contiene _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="aa4b4-111">Resource Object contains _rid, _ts, _etag.</span></span>

## <span data-ttu-id="aa4b4-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aa4b4-112">PARAMETERS</span></span>

### <span data-ttu-id="aa4b4-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="aa4b4-113">-AccountName</span></span>
<span data-ttu-id="aa4b4-114">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="aa4b4-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="aa4b4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa4b4-115">-DefaultProfile</span></span>
<span data-ttu-id="aa4b4-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aa4b4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa4b4-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="aa4b4-117">-Name</span></span>
<span data-ttu-id="aa4b4-118">Nome database.</span><span class="sxs-lookup"><span data-stu-id="aa4b4-118">Database name.</span></span>

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

### <span data-ttu-id="aa4b4-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="aa4b4-119">-ParentObject</span></span>
<span data-ttu-id="aa4b4-120">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="aa4b4-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="aa4b4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa4b4-121">-ResourceGroupName</span></span>
<span data-ttu-id="aa4b4-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="aa4b4-122">Name of resource group.</span></span>

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

### <span data-ttu-id="aa4b4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa4b4-123">CommonParameters</span></span>
<span data-ttu-id="aa4b4-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa4b4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa4b4-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa4b4-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa4b4-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aa4b4-126">INPUTS</span></span>

### <span data-ttu-id="aa4b4-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="aa4b4-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="aa4b4-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aa4b4-128">OUTPUTS</span></span>

### <span data-ttu-id="aa4b4-129">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="aa4b4-129">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="aa4b4-130">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="aa4b4-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="aa4b4-131">Note</span><span class="sxs-lookup"><span data-stu-id="aa4b4-131">NOTES</span></span>

## <span data-ttu-id="aa4b4-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aa4b4-132">RELATED LINKS</span></span>
