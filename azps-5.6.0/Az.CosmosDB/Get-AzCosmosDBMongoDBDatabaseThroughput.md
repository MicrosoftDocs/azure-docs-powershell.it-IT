---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabaseThroughput.md
ms.openlocfilehash: d473d87971b0fcc1b8457a7d2e362c334d480ec4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980846"
---
# <span data-ttu-id="0b781-101">Get-AzCosmosDBMongoDBDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="0b781-101">Get-AzCosmosDBMongoDBDatabaseThroughput</span></span>

## <span data-ttu-id="0b781-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b781-102">SYNOPSIS</span></span>
<span data-ttu-id="0b781-103">Ottiene le proprietà di velocità effettivadb del database MongoDB.</span><span class="sxs-lookup"><span data-stu-id="0b781-103">Gets the CosmosDB throughput properties of MongoDB Database.</span></span>

## <span data-ttu-id="0b781-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0b781-104">SYNTAX</span></span>

### <span data-ttu-id="0b781-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0b781-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b781-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b781-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b781-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0b781-107">DESCRIPTION</span></span>
<span data-ttu-id="0b781-108">Il cmdlet **Get-AzCosmosDBMongoDBDatabaseThroughput** ottiene le proprietà di velocità effettiva del database MongoDB.</span><span class="sxs-lookup"><span data-stu-id="0b781-108">The **Get-AzCosmosDBMongoDBDatabaseThroughput** cmdlet gets the throughput properties of MongoDB Database.</span></span>

## <span data-ttu-id="0b781-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0b781-109">EXAMPLES</span></span>

### <span data-ttu-id="0b781-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0b781-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabaseThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="0b781-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b781-111">PARAMETERS</span></span>

### <span data-ttu-id="0b781-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0b781-112">-AccountName</span></span>
<span data-ttu-id="0b781-113">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="0b781-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0b781-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b781-114">-DefaultProfile</span></span>
<span data-ttu-id="0b781-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0b781-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b781-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b781-116">-InputObject</span></span>
<span data-ttu-id="0b781-117">Oggetto AccountDb Disa</span><span class="sxs-lookup"><span data-stu-id="0b781-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="0b781-118">-Name</span><span class="sxs-lookup"><span data-stu-id="0b781-118">-Name</span></span>
<span data-ttu-id="0b781-119">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="0b781-119">Database name.</span></span>

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

### <span data-ttu-id="0b781-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b781-120">-ResourceGroupName</span></span>
<span data-ttu-id="0b781-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0b781-121">Name of resource group.</span></span>

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

### <span data-ttu-id="0b781-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b781-122">CommonParameters</span></span>
<span data-ttu-id="0b781-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b781-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b781-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0b781-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b781-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="0b781-125">INPUTS</span></span>

### <span data-ttu-id="0b781-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0b781-126">None</span></span>

## <span data-ttu-id="0b781-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0b781-127">OUTPUTS</span></span>

### <span data-ttu-id="0b781-128">Microsoft.Azure.Commands.EnterpriseDb.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="0b781-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="0b781-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="0b781-129">NOTES</span></span>

## <span data-ttu-id="0b781-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0b781-130">RELATED LINKS</span></span>
