---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
ms.openlocfilehash: 9ba9c092f021041f1a56626a79e07b369b694d5a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018520"
---
# <span data-ttu-id="84474-101">Get-AzCosmosDBSqlDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="84474-101">Get-AzCosmosDBSqlDatabaseThroughput</span></span>

## <span data-ttu-id="84474-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="84474-102">SYNOPSIS</span></span>
<span data-ttu-id="84474-103">Ottiene le impostazioni della velocità effettiva corrispondenti a un database SQL di CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="84474-103">Gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="84474-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="84474-104">SYNTAX</span></span>

### <span data-ttu-id="84474-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="84474-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84474-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="84474-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84474-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84474-107">DESCRIPTION</span></span>
<span data-ttu-id="84474-108">Il cmdlet **Get-AzCosmosDBSqlDatabaseThroughput** ottiene le impostazioni della velocità effettiva corrispondenti a un database SQL di CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="84474-108">The **Get-AzCosmosDBSqlDatabaseThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="84474-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="84474-109">EXAMPLES</span></span>

### <span data-ttu-id="84474-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="84474-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabaseThroughput -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                : {throughputResourceName}
Id                  : {throughputId}
Throughput          : 0
MinimumThroughput   :
OfferReplacePending :
```

## <span data-ttu-id="84474-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="84474-111">PARAMETERS</span></span>

### <span data-ttu-id="84474-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="84474-112">-AccountName</span></span>
<span data-ttu-id="84474-113">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="84474-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="84474-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84474-114">-DefaultProfile</span></span>
<span data-ttu-id="84474-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="84474-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84474-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84474-116">-InputObject</span></span>
<span data-ttu-id="84474-117">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="84474-117">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84474-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="84474-118">-Name</span></span>
<span data-ttu-id="84474-119">Nome database.</span><span class="sxs-lookup"><span data-stu-id="84474-119">Database name.</span></span>

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

### <span data-ttu-id="84474-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84474-120">-ResourceGroupName</span></span>
<span data-ttu-id="84474-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="84474-121">Name of resource group.</span></span>

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

### <span data-ttu-id="84474-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84474-122">CommonParameters</span></span>
<span data-ttu-id="84474-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84474-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84474-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84474-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84474-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="84474-125">INPUTS</span></span>

### <span data-ttu-id="84474-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="84474-126">None</span></span>

## <span data-ttu-id="84474-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="84474-127">OUTPUTS</span></span>

### <span data-ttu-id="84474-128">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="84474-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="84474-129">Note</span><span class="sxs-lookup"><span data-stu-id="84474-129">NOTES</span></span>

## <span data-ttu-id="84474-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="84474-130">RELATED LINKS</span></span>
