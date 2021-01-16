---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
ms.openlocfilehash: 7c3dea3fc8f7fd6bf4870e68e242917421647661
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333724"
---
# <span data-ttu-id="241e5-101">Get-AzCosmosDBSqlDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="241e5-101">Get-AzCosmosDBSqlDatabaseThroughput</span></span>

## <span data-ttu-id="241e5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="241e5-102">SYNOPSIS</span></span>
<span data-ttu-id="241e5-103">Ottiene le impostazioni della velocità effettiva corrispondenti a un database SQL di CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="241e5-103">Gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="241e5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="241e5-104">SYNTAX</span></span>

### <span data-ttu-id="241e5-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="241e5-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="241e5-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="241e5-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="241e5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="241e5-107">DESCRIPTION</span></span>
<span data-ttu-id="241e5-108">Il cmdlet **Get-AzCosmosDBSqlDatabaseThroughput** ottiene le impostazioni della velocità effettiva corrispondenti a un database SQL di CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="241e5-108">The **Get-AzCosmosDBSqlDatabaseThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="241e5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="241e5-109">EXAMPLES</span></span>

### <span data-ttu-id="241e5-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="241e5-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabaseThroughput -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                : {throughputResourceName}
Id                  : {throughputId}
Throughput          : 0
MinimumThroughput   :
OfferReplacePending :
```

## <span data-ttu-id="241e5-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="241e5-111">PARAMETERS</span></span>

### <span data-ttu-id="241e5-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="241e5-112">-AccountName</span></span>
<span data-ttu-id="241e5-113">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="241e5-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="241e5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="241e5-114">-DefaultProfile</span></span>
<span data-ttu-id="241e5-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="241e5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="241e5-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="241e5-116">-InputObject</span></span>
<span data-ttu-id="241e5-117">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="241e5-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="241e5-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="241e5-118">-Name</span></span>
<span data-ttu-id="241e5-119">Nome database.</span><span class="sxs-lookup"><span data-stu-id="241e5-119">Database name.</span></span>

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

### <span data-ttu-id="241e5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="241e5-120">-ResourceGroupName</span></span>
<span data-ttu-id="241e5-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="241e5-121">Name of resource group.</span></span>

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

### <span data-ttu-id="241e5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="241e5-122">CommonParameters</span></span>
<span data-ttu-id="241e5-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="241e5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="241e5-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="241e5-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="241e5-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="241e5-125">INPUTS</span></span>

### <span data-ttu-id="241e5-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="241e5-126">None</span></span>

## <span data-ttu-id="241e5-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="241e5-127">OUTPUTS</span></span>

### <span data-ttu-id="241e5-128">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="241e5-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="241e5-129">Note</span><span class="sxs-lookup"><span data-stu-id="241e5-129">NOTES</span></span>

## <span data-ttu-id="241e5-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="241e5-130">RELATED LINKS</span></span>
