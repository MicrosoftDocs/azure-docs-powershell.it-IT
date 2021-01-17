---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabaseThroughput.md
ms.openlocfilehash: f73d39c9b09c0ef44edacfc42f439ee444eedc4d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322235"
---
# <span data-ttu-id="c6016-101">Get-AzCosmosDBMongoDBDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="c6016-101">Get-AzCosmosDBMongoDBDatabaseThroughput</span></span>

## <span data-ttu-id="c6016-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c6016-102">SYNOPSIS</span></span>
<span data-ttu-id="c6016-103">Ottiene le proprietà della velocità effettiva CosmosDB del database MongoDB.</span><span class="sxs-lookup"><span data-stu-id="c6016-103">Gets the CosmosDB throughput properties of MongoDB Database.</span></span>

## <span data-ttu-id="c6016-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c6016-104">SYNTAX</span></span>

### <span data-ttu-id="c6016-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c6016-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6016-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6016-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6016-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c6016-107">DESCRIPTION</span></span>
<span data-ttu-id="c6016-108">Il cmdlet **Get-AzCosmosDBMongoDBDatabaseThroughput** ottiene le proprietà throughput del database MongoDB.</span><span class="sxs-lookup"><span data-stu-id="c6016-108">The **Get-AzCosmosDBMongoDBDatabaseThroughput** cmdlet gets the throughput properties of MongoDB Database.</span></span>

## <span data-ttu-id="c6016-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c6016-109">EXAMPLES</span></span>

### <span data-ttu-id="c6016-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c6016-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabaseThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="c6016-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c6016-111">PARAMETERS</span></span>

### <span data-ttu-id="c6016-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c6016-112">-AccountName</span></span>
<span data-ttu-id="c6016-113">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="c6016-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c6016-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6016-114">-DefaultProfile</span></span>
<span data-ttu-id="c6016-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c6016-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6016-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6016-116">-InputObject</span></span>
<span data-ttu-id="c6016-117">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="c6016-117">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6016-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="c6016-118">-Name</span></span>
<span data-ttu-id="c6016-119">Nome database.</span><span class="sxs-lookup"><span data-stu-id="c6016-119">Database name.</span></span>

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

### <span data-ttu-id="c6016-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6016-120">-ResourceGroupName</span></span>
<span data-ttu-id="c6016-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c6016-121">Name of resource group.</span></span>

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

### <span data-ttu-id="c6016-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6016-122">CommonParameters</span></span>
<span data-ttu-id="c6016-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6016-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6016-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c6016-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6016-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c6016-125">INPUTS</span></span>

### <span data-ttu-id="c6016-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c6016-126">None</span></span>

## <span data-ttu-id="c6016-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c6016-127">OUTPUTS</span></span>

### <span data-ttu-id="c6016-128">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="c6016-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="c6016-129">Note</span><span class="sxs-lookup"><span data-stu-id="c6016-129">NOTES</span></span>

## <span data-ttu-id="c6016-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c6016-130">RELATED LINKS</span></span>
