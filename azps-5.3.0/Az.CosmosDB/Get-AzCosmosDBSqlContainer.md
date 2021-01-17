---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 0090e63086614e64c8e1c6dfc46ede52ce18ec42
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98487972"
---
# <span data-ttu-id="ba874-101">Get-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="ba874-101">Get-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="ba874-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ba874-102">SYNOPSIS</span></span>
<span data-ttu-id="ba874-103">Ottiene il contenitore SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="ba874-103">Gets the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="ba874-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ba874-104">SYNTAX</span></span>

### <span data-ttu-id="ba874-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ba874-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainer -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="ba874-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba874-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainer [-Name <String>] -ParentObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba874-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ba874-107">DESCRIPTION</span></span>
<span data-ttu-id="ba874-108">Il cmdlet **Get-AzCosmosDBSqlContainer** Ottiene l'elenco di tutti i contenitori SQL CosmosDB esistenti per un ResourceGroupName specifico, AccountName e DatabaseName e ottiene un singolo contenitore SQL CosmosDB per una determinata ResourceGroupName, AccountName, DatabaseName e ContainerName.</span><span class="sxs-lookup"><span data-stu-id="ba874-108">The **Get-AzCosmosDBSqlContainer** cmdlet gets the list of all existing CosmosDB Sql Containers for a given ResourceGroupName, AccountName and DatabaseName and gets a single CosmosDB Sql Container for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="ba874-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ba874-109">EXAMPLES</span></span>

### <span data-ttu-id="ba874-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ba874-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlContainer -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName}

Name                     : {containerName1}
Id                       : Id
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="ba874-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ba874-111">PARAMETERS</span></span>

### <span data-ttu-id="ba874-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ba874-112">-AccountName</span></span>
<span data-ttu-id="ba874-113">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="ba874-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ba874-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ba874-114">-DatabaseName</span></span>
<span data-ttu-id="ba874-115">Nome database.</span><span class="sxs-lookup"><span data-stu-id="ba874-115">Database name.</span></span>

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

### <span data-ttu-id="ba874-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba874-116">-DefaultProfile</span></span>
<span data-ttu-id="ba874-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ba874-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba874-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="ba874-118">-Name</span></span>
<span data-ttu-id="ba874-119">Nome contenitore.</span><span class="sxs-lookup"><span data-stu-id="ba874-119">Container name.</span></span>

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

### <span data-ttu-id="ba874-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ba874-120">-ParentObject</span></span>
<span data-ttu-id="ba874-121">Oggetto database SQL.</span><span class="sxs-lookup"><span data-stu-id="ba874-121">Sql Database object.</span></span>

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

### <span data-ttu-id="ba874-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba874-122">-ResourceGroupName</span></span>
<span data-ttu-id="ba874-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ba874-123">Name of resource group.</span></span>

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

### <span data-ttu-id="ba874-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba874-124">CommonParameters</span></span>
<span data-ttu-id="ba874-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba874-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba874-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ba874-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba874-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ba874-127">INPUTS</span></span>

### <span data-ttu-id="ba874-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ba874-128">None</span></span>

## <span data-ttu-id="ba874-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ba874-129">OUTPUTS</span></span>

### <span data-ttu-id="ba874-130">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="ba874-130">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="ba874-131">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="ba874-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="ba874-132">Note</span><span class="sxs-lookup"><span data-stu-id="ba874-132">NOTES</span></span>

## <span data-ttu-id="ba874-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ba874-133">RELATED LINKS</span></span>
