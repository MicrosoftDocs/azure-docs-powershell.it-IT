---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainerthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
ms.openlocfilehash: 3ceb7ccbb789c21fc0fdb51244260e6a54b3e900
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998869"
---
# <span data-ttu-id="029af-101">Get-AzCosmosDBSqlContainerThroughput</span><span class="sxs-lookup"><span data-stu-id="029af-101">Get-AzCosmosDBSqlContainerThroughput</span></span>

## <span data-ttu-id="029af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="029af-102">SYNOPSIS</span></span>
<span data-ttu-id="029af-103">Ottiene le impostazioni di velocità effettiva corrispondenti a un contenitore SQL diDb.</span><span class="sxs-lookup"><span data-stu-id="029af-103">Gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span>

## <span data-ttu-id="029af-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="029af-104">SYNTAX</span></span>

### <span data-ttu-id="029af-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="029af-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainerThroughput -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="029af-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="029af-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainerThroughput [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="029af-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="029af-107">DESCRIPTION</span></span>
<span data-ttu-id="029af-108">Il cmdlet **Get-AzCosmosDBSqlContainerThroughput** ottiene le impostazioni di velocità effettiva corrispondenti a un contenitore Sql diSqlsDB.</span><span class="sxs-lookup"><span data-stu-id="029af-108">The **Get-AzCosmosDBSqlContainerThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span> 

## <span data-ttu-id="029af-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="029af-109">EXAMPLES</span></span>

### <span data-ttu-id="029af-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="029af-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlContainerThroughput  -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {containerName}

Throughput          : {throughputValue}
MinimumThroughput   :
OfferReplacePending :
Id                  : 
Name                : {Name}
Type                : Microsoft.DocumentDB/databaseAccounts/sqlDatabases/containers/throughputSettings
Location            :
Tags                :
```

## <span data-ttu-id="029af-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="029af-111">PARAMETERS</span></span>

### <span data-ttu-id="029af-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="029af-112">-AccountName</span></span>
<span data-ttu-id="029af-113">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="029af-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="029af-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="029af-114">-DatabaseName</span></span>
<span data-ttu-id="029af-115">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="029af-115">Database name.</span></span>

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

### <span data-ttu-id="029af-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="029af-116">-DefaultProfile</span></span>
<span data-ttu-id="029af-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="029af-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="029af-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="029af-118">-InputObject</span></span>
<span data-ttu-id="029af-119">Oggetto Contenitore Sql.</span><span class="sxs-lookup"><span data-stu-id="029af-119">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="029af-120">-Name</span><span class="sxs-lookup"><span data-stu-id="029af-120">-Name</span></span>
<span data-ttu-id="029af-121">Nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="029af-121">Container name.</span></span>

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

### <span data-ttu-id="029af-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="029af-122">-ResourceGroupName</span></span>
<span data-ttu-id="029af-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="029af-123">Name of resource group.</span></span>

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

### <span data-ttu-id="029af-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="029af-124">CommonParameters</span></span>
<span data-ttu-id="029af-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="029af-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="029af-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="029af-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="029af-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="029af-127">INPUTS</span></span>

### <span data-ttu-id="029af-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="029af-128">None</span></span>

## <span data-ttu-id="029af-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="029af-129">OUTPUTS</span></span>

### <span data-ttu-id="029af-130">Microsoft.Azure.Commands.EnterpriseDb.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="029af-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="029af-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="029af-131">NOTES</span></span>

## <span data-ttu-id="029af-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="029af-132">RELATED LINKS</span></span>
