---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 52a889ea454b5752be25ecd216f9a20e4b830b52
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022083"
---
# <span data-ttu-id="e98a3-101">Get-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="e98a3-101">Get-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="e98a3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e98a3-102">SYNOPSIS</span></span>
<span data-ttu-id="e98a3-103">Ottiene il database di CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="e98a3-103">Gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="e98a3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e98a3-104">SYNTAX</span></span>

### <span data-ttu-id="e98a3-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e98a3-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e98a3-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e98a3-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinDatabase [-Name <String>] -InputObject <PSDatabaseAccount> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e98a3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e98a3-107">DESCRIPTION</span></span>
<span data-ttu-id="e98a3-108">Il cmdlet **Get-AzCosmosDBGremlinDatabase** ottiene il database Gremlin di CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="e98a3-108">The **Get-AzCosmosDBGremlinDatabase** cmdlet gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="e98a3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e98a3-109">EXAMPLES</span></span>

### <span data-ttu-id="e98a3-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e98a3-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

<span data-ttu-id="e98a3-111">Oggetto Resource contiene _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="e98a3-111">Resource Object contains _rid, _ts, _etag.</span></span>

## <span data-ttu-id="e98a3-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e98a3-112">PARAMETERS</span></span>

### <span data-ttu-id="e98a3-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e98a3-113">-AccountName</span></span>
<span data-ttu-id="e98a3-114">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="e98a3-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e98a3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e98a3-115">-DefaultProfile</span></span>
<span data-ttu-id="e98a3-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e98a3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e98a3-117">-Dettagli</span><span class="sxs-lookup"><span data-stu-id="e98a3-117">-Detailed</span></span>
<span data-ttu-id="e98a3-118">Se specificato, il cmdlet restituisce il database con il valore di throughput corrispondente.</span><span class="sxs-lookup"><span data-stu-id="e98a3-118">If provided then, the cmdlet returns the Database with the corresponding throughput value.</span></span>

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

### <span data-ttu-id="e98a3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e98a3-119">-InputObject</span></span>
<span data-ttu-id="e98a3-120">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="e98a3-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="e98a3-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="e98a3-121">-Name</span></span>
<span data-ttu-id="e98a3-122">Nome database.</span><span class="sxs-lookup"><span data-stu-id="e98a3-122">Database name.</span></span>

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

### <span data-ttu-id="e98a3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e98a3-123">-ResourceGroupName</span></span>
<span data-ttu-id="e98a3-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e98a3-124">Name of resource group.</span></span>

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

### <span data-ttu-id="e98a3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e98a3-125">CommonParameters</span></span>
<span data-ttu-id="e98a3-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e98a3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e98a3-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e98a3-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e98a3-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e98a3-128">INPUTS</span></span>

### <span data-ttu-id="e98a3-129">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="e98a3-129">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="e98a3-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e98a3-130">OUTPUTS</span></span>

### <span data-ttu-id="e98a3-131">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="e98a3-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="e98a3-132">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="e98a3-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="e98a3-133">Note</span><span class="sxs-lookup"><span data-stu-id="e98a3-133">NOTES</span></span>

## <span data-ttu-id="e98a3-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e98a3-134">RELATED LINKS</span></span>
