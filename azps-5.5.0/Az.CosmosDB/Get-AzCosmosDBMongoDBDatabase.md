---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: 98de834cebd158cc61247881305f40f84760ae2e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181391"
---
# <span data-ttu-id="2bde0-101">Get-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="2bde0-101">Get-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="2bde0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2bde0-102">SYNOPSIS</span></span>
<span data-ttu-id="2bde0-103">Recupera il database Database DatabaseDbDb database DatabaseDbDb</span><span class="sxs-lookup"><span data-stu-id="2bde0-103">Gets the CosmosDB MongoDB Database</span></span>

## <span data-ttu-id="2bde0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2bde0-104">SYNTAX</span></span>

### <span data-ttu-id="2bde0-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2bde0-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2bde0-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2bde0-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2bde0-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2bde0-107">DESCRIPTION</span></span>
<span data-ttu-id="2bde0-108">Il **cmdlet Get-AzCosmosDBMongoDBDatabase** ottiene il databaseDb diDbDb.</span><span class="sxs-lookup"><span data-stu-id="2bde0-108">The **Get-AzCosmosDBMongoDBDatabase** cmdlet gets the CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="2bde0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2bde0-109">EXAMPLES</span></span>

### <span data-ttu-id="2bde0-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2bde0-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

<span data-ttu-id="2bde0-111">L'oggetto risorsa _rid proprietà _ts, _etag risorse.</span><span class="sxs-lookup"><span data-stu-id="2bde0-111">Resource Object contains _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="2bde0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2bde0-112">PARAMETERS</span></span>

### <span data-ttu-id="2bde0-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2bde0-113">-AccountName</span></span>
<span data-ttu-id="2bde0-114">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="2bde0-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2bde0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bde0-115">-DefaultProfile</span></span>
<span data-ttu-id="2bde0-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2bde0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2bde0-117">-Name</span><span class="sxs-lookup"><span data-stu-id="2bde0-117">-Name</span></span>
<span data-ttu-id="2bde0-118">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="2bde0-118">Database name.</span></span>

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

### <span data-ttu-id="2bde0-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="2bde0-119">-ParentObject</span></span>
<span data-ttu-id="2bde0-120">Oggetto AccountDb Disa</span><span class="sxs-lookup"><span data-stu-id="2bde0-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="2bde0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bde0-121">-ResourceGroupName</span></span>
<span data-ttu-id="2bde0-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2bde0-122">Name of resource group.</span></span>

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

### <span data-ttu-id="2bde0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bde0-123">CommonParameters</span></span>
<span data-ttu-id="2bde0-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bde0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bde0-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2bde0-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bde0-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="2bde0-126">INPUTS</span></span>

### <span data-ttu-id="2bde0-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="2bde0-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="2bde0-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2bde0-128">OUTPUTS</span></span>

### <span data-ttu-id="2bde0-129">Microsoft.Azure.Commands.EnterpriseDb.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="2bde0-129">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="2bde0-130">Microsoft.Azure.Commands.EnterpriseDb.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="2bde0-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="2bde0-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="2bde0-131">NOTES</span></span>

## <span data-ttu-id="2bde0-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2bde0-132">RELATED LINKS</span></span>
