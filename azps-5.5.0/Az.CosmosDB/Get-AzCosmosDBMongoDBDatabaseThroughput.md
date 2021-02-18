---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabaseThroughput.md
ms.openlocfilehash: f73d39c9b09c0ef44edacfc42f439ee444eedc4d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181390"
---
# <span data-ttu-id="4afe7-101">Get-AzCosmosDBMongoDBDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="4afe7-101">Get-AzCosmosDBMongoDBDatabaseThroughput</span></span>

## <span data-ttu-id="4afe7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4afe7-102">SYNOPSIS</span></span>
<span data-ttu-id="4afe7-103">Ottiene le proprietà di velocità effettivadb del database MongoDB.</span><span class="sxs-lookup"><span data-stu-id="4afe7-103">Gets the CosmosDB throughput properties of MongoDB Database.</span></span>

## <span data-ttu-id="4afe7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4afe7-104">SYNTAX</span></span>

### <span data-ttu-id="4afe7-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4afe7-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4afe7-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4afe7-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4afe7-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4afe7-107">DESCRIPTION</span></span>
<span data-ttu-id="4afe7-108">Il cmdlet **Get-AzCosmosDBMongoDBDatabaseThroughput** ottiene le proprietà di velocità effettiva del database MongoDB.</span><span class="sxs-lookup"><span data-stu-id="4afe7-108">The **Get-AzCosmosDBMongoDBDatabaseThroughput** cmdlet gets the throughput properties of MongoDB Database.</span></span>

## <span data-ttu-id="4afe7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4afe7-109">EXAMPLES</span></span>

### <span data-ttu-id="4afe7-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4afe7-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabaseThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="4afe7-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4afe7-111">PARAMETERS</span></span>

### <span data-ttu-id="4afe7-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4afe7-112">-AccountName</span></span>
<span data-ttu-id="4afe7-113">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="4afe7-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="4afe7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4afe7-114">-DefaultProfile</span></span>
<span data-ttu-id="4afe7-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4afe7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4afe7-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4afe7-116">-InputObject</span></span>
<span data-ttu-id="4afe7-117">Oggetto AccountDb Disa</span><span class="sxs-lookup"><span data-stu-id="4afe7-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="4afe7-118">-Name</span><span class="sxs-lookup"><span data-stu-id="4afe7-118">-Name</span></span>
<span data-ttu-id="4afe7-119">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="4afe7-119">Database name.</span></span>

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

### <span data-ttu-id="4afe7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4afe7-120">-ResourceGroupName</span></span>
<span data-ttu-id="4afe7-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4afe7-121">Name of resource group.</span></span>

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

### <span data-ttu-id="4afe7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4afe7-122">CommonParameters</span></span>
<span data-ttu-id="4afe7-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4afe7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4afe7-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4afe7-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4afe7-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="4afe7-125">INPUTS</span></span>

### <span data-ttu-id="4afe7-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4afe7-126">None</span></span>

## <span data-ttu-id="4afe7-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4afe7-127">OUTPUTS</span></span>

### <span data-ttu-id="4afe7-128">Microsoft.Azure.Commands.EnterpriseDb.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="4afe7-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="4afe7-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="4afe7-129">NOTES</span></span>

## <span data-ttu-id="4afe7-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4afe7-130">RELATED LINKS</span></span>
