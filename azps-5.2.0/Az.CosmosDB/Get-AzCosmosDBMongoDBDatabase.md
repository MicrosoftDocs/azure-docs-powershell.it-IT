---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: 98de834cebd158cc61247881305f40f84760ae2e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322249"
---
# <span data-ttu-id="75e21-101">Get-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="75e21-101">Get-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="75e21-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="75e21-102">SYNOPSIS</span></span>
<span data-ttu-id="75e21-103">Ottiene il database MongoDB di CosmosDB</span><span class="sxs-lookup"><span data-stu-id="75e21-103">Gets the CosmosDB MongoDB Database</span></span>

## <span data-ttu-id="75e21-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="75e21-104">SYNTAX</span></span>

### <span data-ttu-id="75e21-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="75e21-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75e21-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="75e21-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75e21-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="75e21-107">DESCRIPTION</span></span>
<span data-ttu-id="75e21-108">Il cmdlet **Get-AzCosmosDBMongoDBDatabase** ottiene il database MongoDB CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="75e21-108">The **Get-AzCosmosDBMongoDBDatabase** cmdlet gets the CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="75e21-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="75e21-109">EXAMPLES</span></span>

### <span data-ttu-id="75e21-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="75e21-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

<span data-ttu-id="75e21-111">Oggetto Resource contiene _rid, _ts, _etag proprietà.</span><span class="sxs-lookup"><span data-stu-id="75e21-111">Resource Object contains _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="75e21-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="75e21-112">PARAMETERS</span></span>

### <span data-ttu-id="75e21-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="75e21-113">-AccountName</span></span>
<span data-ttu-id="75e21-114">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="75e21-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="75e21-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75e21-115">-DefaultProfile</span></span>
<span data-ttu-id="75e21-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="75e21-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75e21-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="75e21-117">-Name</span></span>
<span data-ttu-id="75e21-118">Nome database.</span><span class="sxs-lookup"><span data-stu-id="75e21-118">Database name.</span></span>

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

### <span data-ttu-id="75e21-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="75e21-119">-ParentObject</span></span>
<span data-ttu-id="75e21-120">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="75e21-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75e21-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75e21-121">-ResourceGroupName</span></span>
<span data-ttu-id="75e21-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="75e21-122">Name of resource group.</span></span>

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

### <span data-ttu-id="75e21-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75e21-123">CommonParameters</span></span>
<span data-ttu-id="75e21-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75e21-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75e21-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="75e21-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75e21-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="75e21-126">INPUTS</span></span>

### <span data-ttu-id="75e21-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="75e21-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="75e21-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="75e21-128">OUTPUTS</span></span>

### <span data-ttu-id="75e21-129">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="75e21-129">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="75e21-130">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="75e21-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="75e21-131">Note</span><span class="sxs-lookup"><span data-stu-id="75e21-131">NOTES</span></span>

## <span data-ttu-id="75e21-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="75e21-132">RELATED LINKS</span></span>
