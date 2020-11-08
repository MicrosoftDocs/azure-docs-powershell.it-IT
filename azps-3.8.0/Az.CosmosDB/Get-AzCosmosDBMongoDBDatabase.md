---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: f1cb4a45a68758dc1209b4e30d352def8e348e9f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022064"
---
# <span data-ttu-id="785de-101">Get-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="785de-101">Get-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="785de-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="785de-102">SYNOPSIS</span></span>
<span data-ttu-id="785de-103">Ottiene il database MongoDB di CosmosDB</span><span class="sxs-lookup"><span data-stu-id="785de-103">Gets the CosmosDB MongoDB Database</span></span>

## <span data-ttu-id="785de-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="785de-104">SYNTAX</span></span>

### <span data-ttu-id="785de-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="785de-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="785de-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="785de-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabase [-Name <String>] -InputObject <PSDatabaseAccount> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="785de-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="785de-107">DESCRIPTION</span></span>
<span data-ttu-id="785de-108">Il cmdlet **Get-AzCosmosDBMongoDBDatabase** ottiene il database MongoDB CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="785de-108">The **Get-AzCosmosDBMongoDBDatabase** cmdlet gets the CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="785de-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="785de-109">EXAMPLES</span></span>

### <span data-ttu-id="785de-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="785de-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

<span data-ttu-id="785de-111">Oggetto Resource contiene _rid, _ts, _etag proprietà.</span><span class="sxs-lookup"><span data-stu-id="785de-111">Resource Object contains _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="785de-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="785de-112">PARAMETERS</span></span>

### <span data-ttu-id="785de-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="785de-113">-AccountName</span></span>
<span data-ttu-id="785de-114">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="785de-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="785de-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="785de-115">-DefaultProfile</span></span>
<span data-ttu-id="785de-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="785de-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="785de-117">-Dettagli</span><span class="sxs-lookup"><span data-stu-id="785de-117">-Detailed</span></span>
<span data-ttu-id="785de-118">Se specificato, il cmdlet restituisce il database con il valore di throughput corrispondente.</span><span class="sxs-lookup"><span data-stu-id="785de-118">If provided then, the cmdlet returns the database with the corresponding throughput value.</span></span>

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

### <span data-ttu-id="785de-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="785de-119">-InputObject</span></span>
<span data-ttu-id="785de-120">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="785de-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="785de-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="785de-121">-Name</span></span>
<span data-ttu-id="785de-122">Nome database.</span><span class="sxs-lookup"><span data-stu-id="785de-122">Database name.</span></span>

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

### <span data-ttu-id="785de-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="785de-123">-ResourceGroupName</span></span>
<span data-ttu-id="785de-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="785de-124">Name of resource group.</span></span>

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

### <span data-ttu-id="785de-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="785de-125">CommonParameters</span></span>
<span data-ttu-id="785de-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="785de-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="785de-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="785de-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="785de-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="785de-128">INPUTS</span></span>

### <span data-ttu-id="785de-129">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="785de-129">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="785de-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="785de-130">OUTPUTS</span></span>

### <span data-ttu-id="785de-131">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="785de-131">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="785de-132">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="785de-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="785de-133">Note</span><span class="sxs-lookup"><span data-stu-id="785de-133">NOTES</span></span>

## <span data-ttu-id="785de-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="785de-134">RELATED LINKS</span></span>
