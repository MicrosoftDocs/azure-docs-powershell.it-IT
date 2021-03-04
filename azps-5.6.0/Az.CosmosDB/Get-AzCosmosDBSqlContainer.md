---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 5c7c26faa6171babd60f9d5fb406d3b3c08ef81b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952781"
---
# <span data-ttu-id="aadc8-101">Get-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="aadc8-101">Get-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="aadc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aadc8-102">SYNOPSIS</span></span>
<span data-ttu-id="aadc8-103">Ottiene il contenitore sql database database.</span><span class="sxs-lookup"><span data-stu-id="aadc8-103">Gets the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="aadc8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aadc8-104">SYNTAX</span></span>

### <span data-ttu-id="aadc8-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="aadc8-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainer -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="aadc8-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aadc8-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainer [-Name <String>] -ParentObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aadc8-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="aadc8-107">DESCRIPTION</span></span>
<span data-ttu-id="aadc8-108">Il cmdlet **Get-AzCosmosDBSqlContainer** ottiene l'elenco di tutti i contenitori Sql esistenti di ClustersDB per un determinato ResourceGroupName, AccountName e DatabaseName e ottiene un singolo contenitore Sql Per un determinato ResourceGroupName, AccountName, DatabaseName e ContainerName.</span><span class="sxs-lookup"><span data-stu-id="aadc8-108">The **Get-AzCosmosDBSqlContainer** cmdlet gets the list of all existing CosmosDB Sql Containers for a given ResourceGroupName, AccountName and DatabaseName and gets a single CosmosDB Sql Container for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="aadc8-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aadc8-109">EXAMPLES</span></span>

### <span data-ttu-id="aadc8-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="aadc8-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlContainer -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName}

Name                     : {containerName1}
Id                       : Id
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="aadc8-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aadc8-111">PARAMETERS</span></span>

### <span data-ttu-id="aadc8-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="aadc8-112">-AccountName</span></span>
<span data-ttu-id="aadc8-113">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="aadc8-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="aadc8-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="aadc8-114">-DatabaseName</span></span>
<span data-ttu-id="aadc8-115">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="aadc8-115">Database name.</span></span>

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

### <span data-ttu-id="aadc8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aadc8-116">-DefaultProfile</span></span>
<span data-ttu-id="aadc8-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aadc8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aadc8-118">-Name</span><span class="sxs-lookup"><span data-stu-id="aadc8-118">-Name</span></span>
<span data-ttu-id="aadc8-119">Nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="aadc8-119">Container name.</span></span>

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

### <span data-ttu-id="aadc8-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="aadc8-120">-ParentObject</span></span>
<span data-ttu-id="aadc8-121">Oggetto database Sql.</span><span class="sxs-lookup"><span data-stu-id="aadc8-121">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aadc8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aadc8-122">-ResourceGroupName</span></span>
<span data-ttu-id="aadc8-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="aadc8-123">Name of resource group.</span></span>

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

### <span data-ttu-id="aadc8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aadc8-124">CommonParameters</span></span>
<span data-ttu-id="aadc8-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aadc8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aadc8-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="aadc8-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aadc8-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="aadc8-127">INPUTS</span></span>

### <span data-ttu-id="aadc8-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="aadc8-128">None</span></span>

## <span data-ttu-id="aadc8-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aadc8-129">OUTPUTS</span></span>

### <span data-ttu-id="aadc8-130">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="aadc8-130">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="aadc8-131">Microsoft.Azure.Commands.EnterpriseDb.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="aadc8-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="aadc8-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="aadc8-132">NOTES</span></span>

## <span data-ttu-id="aadc8-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aadc8-133">RELATED LINKS</span></span>
