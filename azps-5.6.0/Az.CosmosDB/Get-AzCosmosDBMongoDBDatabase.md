---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: 0dfcffe55eb3214f4be9d6ccfb34231d1c9ea50c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994473"
---
# <span data-ttu-id="79482-101">Get-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="79482-101">Get-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="79482-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79482-102">SYNOPSIS</span></span>
<span data-ttu-id="79482-103">Recupera il database Database DatabaseDbDb database DatabaseDbDb</span><span class="sxs-lookup"><span data-stu-id="79482-103">Gets the CosmosDB MongoDB Database</span></span>

## <span data-ttu-id="79482-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="79482-104">SYNTAX</span></span>

### <span data-ttu-id="79482-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="79482-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79482-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="79482-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79482-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="79482-107">DESCRIPTION</span></span>
<span data-ttu-id="79482-108">Il **cmdlet Get-AzCosmosDBMongoDBDatabase** ottiene il databaseDb diDbDb.</span><span class="sxs-lookup"><span data-stu-id="79482-108">The **Get-AzCosmosDBMongoDBDatabase** cmdlet gets the CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="79482-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="79482-109">EXAMPLES</span></span>

### <span data-ttu-id="79482-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="79482-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

<span data-ttu-id="79482-111">L'oggetto risorsa _rid proprietà _ts, _etag risorse.</span><span class="sxs-lookup"><span data-stu-id="79482-111">Resource Object contains _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="79482-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79482-112">PARAMETERS</span></span>

### <span data-ttu-id="79482-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="79482-113">-AccountName</span></span>
<span data-ttu-id="79482-114">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="79482-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="79482-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79482-115">-DefaultProfile</span></span>
<span data-ttu-id="79482-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="79482-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79482-117">-Name</span><span class="sxs-lookup"><span data-stu-id="79482-117">-Name</span></span>
<span data-ttu-id="79482-118">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="79482-118">Database name.</span></span>

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

### <span data-ttu-id="79482-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="79482-119">-ParentObject</span></span>
<span data-ttu-id="79482-120">Oggetto Account Aziendale</span><span class="sxs-lookup"><span data-stu-id="79482-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="79482-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79482-121">-ResourceGroupName</span></span>
<span data-ttu-id="79482-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="79482-122">Name of resource group.</span></span>

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

### <span data-ttu-id="79482-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79482-123">CommonParameters</span></span>
<span data-ttu-id="79482-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79482-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79482-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="79482-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79482-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="79482-126">INPUTS</span></span>

### <span data-ttu-id="79482-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="79482-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="79482-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="79482-128">OUTPUTS</span></span>

### <span data-ttu-id="79482-129">Microsoft.Azure.Commands.EnterpriseDb.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="79482-129">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="79482-130">Microsoft.Azure.Commands.EnterpriseDb.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="79482-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="79482-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="79482-131">NOTES</span></span>

## <span data-ttu-id="79482-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="79482-132">RELATED LINKS</span></span>
