---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 89a48ecb4b167919562428e1116d95bb1e3d6390
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022066"
---
# <span data-ttu-id="99c0e-101">Get-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="99c0e-101">Get-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="99c0e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="99c0e-102">SYNOPSIS</span></span>
<span data-ttu-id="99c0e-103">Ottiene il contenitore SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="99c0e-103">Gets the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="99c0e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="99c0e-104">SYNTAX</span></span>

### <span data-ttu-id="99c0e-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="99c0e-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainer -ResourceGroupName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="99c0e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="99c0e-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainer [-Name <String>] -InputObject <PSSqlDatabaseGetResults> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99c0e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="99c0e-107">DESCRIPTION</span></span>
<span data-ttu-id="99c0e-108">Il cmdlet **Get-AzCosmosDBSqlContainer** Ottiene l'elenco di tutti i contenitori SQL CosmosDB esistenti per un ResourceGroupName specifico, AccountName e DatabaseName e ottiene un singolo contenitore SQL CosmosDB per una determinata ResourceGroupName, AccountName, DatabaseName e ContainerName.</span><span class="sxs-lookup"><span data-stu-id="99c0e-108">The **Get-AzCosmosDBSqlContainer** cmdlet gets the list of all existing CosmosDB Sql Containers for a given ResourceGroupName, AccountName and DatabaseName and gets a single CosmosDB Sql Container for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="99c0e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="99c0e-109">EXAMPLES</span></span>

### <span data-ttu-id="99c0e-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="99c0e-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlContainer -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName}

Name                     : {containerName1}
Id                       : Id
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="99c0e-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="99c0e-111">PARAMETERS</span></span>

### <span data-ttu-id="99c0e-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="99c0e-112">-AccountName</span></span>
<span data-ttu-id="99c0e-113">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="99c0e-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="99c0e-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="99c0e-114">-DatabaseName</span></span>
<span data-ttu-id="99c0e-115">Nome database.</span><span class="sxs-lookup"><span data-stu-id="99c0e-115">Database name.</span></span>

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

### <span data-ttu-id="99c0e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99c0e-116">-DefaultProfile</span></span>
<span data-ttu-id="99c0e-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="99c0e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99c0e-118">-Dettagli</span><span class="sxs-lookup"><span data-stu-id="99c0e-118">-Detailed</span></span>
<span data-ttu-id="99c0e-119">Se specificato, il cmdlet restituisce il contenitore con il valore della velocità effettiva.</span><span class="sxs-lookup"><span data-stu-id="99c0e-119">If provided then, the cmdlet returns the container with the throughput value.</span></span>

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

### <span data-ttu-id="99c0e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99c0e-120">-InputObject</span></span>
<span data-ttu-id="99c0e-121">Oggetto database SQL.</span><span class="sxs-lookup"><span data-stu-id="99c0e-121">Sql Database object.</span></span>

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

### <span data-ttu-id="99c0e-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="99c0e-122">-Name</span></span>
<span data-ttu-id="99c0e-123">Nome contenitore.</span><span class="sxs-lookup"><span data-stu-id="99c0e-123">Container name.</span></span>

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

### <span data-ttu-id="99c0e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99c0e-124">-ResourceGroupName</span></span>
<span data-ttu-id="99c0e-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="99c0e-125">Name of resource group.</span></span>

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

### <span data-ttu-id="99c0e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99c0e-126">CommonParameters</span></span>
<span data-ttu-id="99c0e-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99c0e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99c0e-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99c0e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99c0e-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="99c0e-129">INPUTS</span></span>

### <span data-ttu-id="99c0e-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="99c0e-130">None</span></span>

## <span data-ttu-id="99c0e-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="99c0e-131">OUTPUTS</span></span>

### <span data-ttu-id="99c0e-132">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="99c0e-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="99c0e-133">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="99c0e-133">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="99c0e-134">Note</span><span class="sxs-lookup"><span data-stu-id="99c0e-134">NOTES</span></span>

## <span data-ttu-id="99c0e-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="99c0e-135">RELATED LINKS</span></span>
