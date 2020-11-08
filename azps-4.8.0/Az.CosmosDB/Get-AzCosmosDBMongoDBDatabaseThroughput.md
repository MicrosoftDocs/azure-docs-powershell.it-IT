---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabaseThroughput.md
ms.openlocfilehash: f73d39c9b09c0ef44edacfc42f439ee444eedc4d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192162"
---
# <span data-ttu-id="ae7c1-101">Get-AzCosmosDBMongoDBDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="ae7c1-101">Get-AzCosmosDBMongoDBDatabaseThroughput</span></span>

## <span data-ttu-id="ae7c1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ae7c1-102">SYNOPSIS</span></span>
<span data-ttu-id="ae7c1-103">Ottiene le proprietà della velocità effettiva CosmosDB del database MongoDB.</span><span class="sxs-lookup"><span data-stu-id="ae7c1-103">Gets the CosmosDB throughput properties of MongoDB Database.</span></span>

## <span data-ttu-id="ae7c1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ae7c1-104">SYNTAX</span></span>

### <span data-ttu-id="ae7c1-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ae7c1-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae7c1-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae7c1-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae7c1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ae7c1-107">DESCRIPTION</span></span>
<span data-ttu-id="ae7c1-108">Il cmdlet **Get-AzCosmosDBMongoDBDatabaseThroughput** ottiene le proprietà throughput del database MongoDB.</span><span class="sxs-lookup"><span data-stu-id="ae7c1-108">The **Get-AzCosmosDBMongoDBDatabaseThroughput** cmdlet gets the throughput properties of MongoDB Database.</span></span>

## <span data-ttu-id="ae7c1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ae7c1-109">EXAMPLES</span></span>

### <span data-ttu-id="ae7c1-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ae7c1-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabaseThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="ae7c1-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ae7c1-111">PARAMETERS</span></span>

### <span data-ttu-id="ae7c1-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ae7c1-112">-AccountName</span></span>
<span data-ttu-id="ae7c1-113">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="ae7c1-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ae7c1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae7c1-114">-DefaultProfile</span></span>
<span data-ttu-id="ae7c1-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ae7c1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae7c1-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae7c1-116">-InputObject</span></span>
<span data-ttu-id="ae7c1-117">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="ae7c1-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="ae7c1-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="ae7c1-118">-Name</span></span>
<span data-ttu-id="ae7c1-119">Nome database.</span><span class="sxs-lookup"><span data-stu-id="ae7c1-119">Database name.</span></span>

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

### <span data-ttu-id="ae7c1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae7c1-120">-ResourceGroupName</span></span>
<span data-ttu-id="ae7c1-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ae7c1-121">Name of resource group.</span></span>

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

### <span data-ttu-id="ae7c1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae7c1-122">CommonParameters</span></span>
<span data-ttu-id="ae7c1-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae7c1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae7c1-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae7c1-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae7c1-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ae7c1-125">INPUTS</span></span>

### <span data-ttu-id="ae7c1-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ae7c1-126">None</span></span>

## <span data-ttu-id="ae7c1-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ae7c1-127">OUTPUTS</span></span>

### <span data-ttu-id="ae7c1-128">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="ae7c1-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="ae7c1-129">Note</span><span class="sxs-lookup"><span data-stu-id="ae7c1-129">NOTES</span></span>

## <span data-ttu-id="ae7c1-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ae7c1-130">RELATED LINKS</span></span>