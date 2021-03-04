---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
ms.openlocfilehash: 5bf35b43db1f1d961f24c1aa2c75c9f17c333345
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958861"
---
# <span data-ttu-id="82d6f-101">Get-AzCosmosDBSqlDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="82d6f-101">Get-AzCosmosDBSqlDatabaseThroughput</span></span>

## <span data-ttu-id="82d6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82d6f-102">SYNOPSIS</span></span>
<span data-ttu-id="82d6f-103">Recupera le impostazioni di velocità effettiva corrispondenti a un database Sql diDbDb.</span><span class="sxs-lookup"><span data-stu-id="82d6f-103">Gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="82d6f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="82d6f-104">SYNTAX</span></span>

### <span data-ttu-id="82d6f-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="82d6f-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82d6f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="82d6f-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82d6f-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="82d6f-107">DESCRIPTION</span></span>
<span data-ttu-id="82d6f-108">Il cmdlet **Get-AzCosmosDBSqlDatabaseThroughput** ottiene le impostazioni di velocità effettiva corrispondenti a un database Sql diSqlsDB.</span><span class="sxs-lookup"><span data-stu-id="82d6f-108">The **Get-AzCosmosDBSqlDatabaseThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="82d6f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="82d6f-109">EXAMPLES</span></span>

### <span data-ttu-id="82d6f-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="82d6f-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabaseThroughput -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                : {throughputResourceName}
Id                  : {throughputId}
Throughput          : 0
MinimumThroughput   :
OfferReplacePending :
```

## <span data-ttu-id="82d6f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82d6f-111">PARAMETERS</span></span>

### <span data-ttu-id="82d6f-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="82d6f-112">-AccountName</span></span>
<span data-ttu-id="82d6f-113">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="82d6f-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="82d6f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82d6f-114">-DefaultProfile</span></span>
<span data-ttu-id="82d6f-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="82d6f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82d6f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="82d6f-116">-InputObject</span></span>
<span data-ttu-id="82d6f-117">Oggetto Account Aziendale</span><span class="sxs-lookup"><span data-stu-id="82d6f-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="82d6f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="82d6f-118">-Name</span></span>
<span data-ttu-id="82d6f-119">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="82d6f-119">Database name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82d6f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82d6f-120">-ResourceGroupName</span></span>
<span data-ttu-id="82d6f-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="82d6f-121">Name of resource group.</span></span>

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

### <span data-ttu-id="82d6f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82d6f-122">CommonParameters</span></span>
<span data-ttu-id="82d6f-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82d6f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82d6f-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="82d6f-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82d6f-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="82d6f-125">INPUTS</span></span>

### <span data-ttu-id="82d6f-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="82d6f-126">None</span></span>

## <span data-ttu-id="82d6f-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="82d6f-127">OUTPUTS</span></span>

### <span data-ttu-id="82d6f-128">Microsoft.Azure.Commands.EnterpriseDb.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="82d6f-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="82d6f-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="82d6f-129">NOTES</span></span>

## <span data-ttu-id="82d6f-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="82d6f-130">RELATED LINKS</span></span>
