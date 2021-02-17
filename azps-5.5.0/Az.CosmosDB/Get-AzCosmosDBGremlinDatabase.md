---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: ba1f6b1ca309226433120ea6a68ec330cabd034c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199039"
---
# <span data-ttu-id="1ae86-101">Get-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="1ae86-101">Get-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="1ae86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ae86-102">SYNOPSIS</span></span>
<span data-ttu-id="1ae86-103">Ottiene il database DellesDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="1ae86-103">Gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="1ae86-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1ae86-104">SYNTAX</span></span>

### <span data-ttu-id="1ae86-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1ae86-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ae86-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ae86-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ae86-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1ae86-107">DESCRIPTION</span></span>
<span data-ttu-id="1ae86-108">Il **cmdlet Get-AzCosmosDBGremlinDatabase** ottiene il databaseDbDb Gremlin Database.</span><span class="sxs-lookup"><span data-stu-id="1ae86-108">The **Get-AzCosmosDBGremlinDatabase** cmdlet gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="1ae86-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1ae86-109">EXAMPLES</span></span>

### <span data-ttu-id="1ae86-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1ae86-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

<span data-ttu-id="1ae86-111">L'oggetto risorsa _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="1ae86-111">Resource Object contains _rid, _ts, _etag.</span></span>

## <span data-ttu-id="1ae86-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ae86-112">PARAMETERS</span></span>

### <span data-ttu-id="1ae86-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1ae86-113">-AccountName</span></span>
<span data-ttu-id="1ae86-114">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="1ae86-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1ae86-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ae86-115">-DefaultProfile</span></span>
<span data-ttu-id="1ae86-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1ae86-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ae86-117">-Name</span><span class="sxs-lookup"><span data-stu-id="1ae86-117">-Name</span></span>
<span data-ttu-id="1ae86-118">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="1ae86-118">Database name.</span></span>

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

### <span data-ttu-id="1ae86-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="1ae86-119">-ParentObject</span></span>
<span data-ttu-id="1ae86-120">Oggetto AccountDb Disa</span><span class="sxs-lookup"><span data-stu-id="1ae86-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="1ae86-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ae86-121">-ResourceGroupName</span></span>
<span data-ttu-id="1ae86-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1ae86-122">Name of resource group.</span></span>

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

### <span data-ttu-id="1ae86-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ae86-123">CommonParameters</span></span>
<span data-ttu-id="1ae86-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ae86-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ae86-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1ae86-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ae86-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="1ae86-126">INPUTS</span></span>

### <span data-ttu-id="1ae86-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="1ae86-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="1ae86-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1ae86-128">OUTPUTS</span></span>

### <span data-ttu-id="1ae86-129">Microsoft.Azure.Commands.EnterpriseDb.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="1ae86-129">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="1ae86-130">Microsoft.Azure.Commands.EnterpriseDb.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="1ae86-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="1ae86-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="1ae86-131">NOTES</span></span>

## <span data-ttu-id="1ae86-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1ae86-132">RELATED LINKS</span></span>
