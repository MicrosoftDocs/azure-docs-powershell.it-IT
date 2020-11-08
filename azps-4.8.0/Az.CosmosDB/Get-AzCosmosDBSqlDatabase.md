---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 87c0436ce4aa62de7a1145d501e71783433b09eb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192156"
---
# <span data-ttu-id="6eb30-101">Get-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6eb30-101">Get-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="6eb30-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6eb30-102">SYNOPSIS</span></span>
<span data-ttu-id="6eb30-103">Ottiene il database SQL di CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="6eb30-103">Gets the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="6eb30-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6eb30-104">SYNTAX</span></span>

### <span data-ttu-id="6eb30-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6eb30-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6eb30-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6eb30-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6eb30-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6eb30-107">DESCRIPTION</span></span>
<span data-ttu-id="6eb30-108">Il cmdlet **Get-AzCosmosDBSqlDatabase** Ottiene l'elenco di tutti i database SQL CosmosDB esistenti per un ResourceGroupName specifico, AccountName e ottiene un singolo database SQL di CosmosDB per una determinata ResourceGroupName, AccountName, DatabaseName e ContainerName.</span><span class="sxs-lookup"><span data-stu-id="6eb30-108">The **Get-AzCosmosDBSqlDatabase** cmdlet gets the list of all existing CosmosDB Sql Databases for a given ResourceGroupName, AccountName and gets a single CosmosDB Sql Database for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="6eb30-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6eb30-109">EXAMPLES</span></span>

### <span data-ttu-id="6eb30-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6eb30-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabase -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                    : {databaseName}
Id                      : {databaseId}
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="6eb30-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6eb30-111">PARAMETERS</span></span>

### <span data-ttu-id="6eb30-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6eb30-112">-AccountName</span></span>
<span data-ttu-id="6eb30-113">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="6eb30-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="6eb30-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eb30-114">-DefaultProfile</span></span>
<span data-ttu-id="6eb30-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6eb30-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6eb30-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="6eb30-116">-Name</span></span>
<span data-ttu-id="6eb30-117">Nome database.</span><span class="sxs-lookup"><span data-stu-id="6eb30-117">Database name.</span></span>

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

### <span data-ttu-id="6eb30-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6eb30-118">-ParentObject</span></span>
<span data-ttu-id="6eb30-119">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="6eb30-119">CosmosDB Account object</span></span>

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

### <span data-ttu-id="6eb30-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6eb30-120">-ResourceGroupName</span></span>
<span data-ttu-id="6eb30-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6eb30-121">Name of resource group.</span></span>

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

### <span data-ttu-id="6eb30-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eb30-122">CommonParameters</span></span>
<span data-ttu-id="6eb30-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6eb30-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eb30-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6eb30-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eb30-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6eb30-125">INPUTS</span></span>

### <span data-ttu-id="6eb30-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6eb30-126">None</span></span>

## <span data-ttu-id="6eb30-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6eb30-127">OUTPUTS</span></span>

### <span data-ttu-id="6eb30-128">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="6eb30-128">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="6eb30-129">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="6eb30-129">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="6eb30-130">Note</span><span class="sxs-lookup"><span data-stu-id="6eb30-130">NOTES</span></span>

## <span data-ttu-id="6eb30-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6eb30-131">RELATED LINKS</span></span>
