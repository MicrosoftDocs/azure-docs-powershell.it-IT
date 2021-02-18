---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbcollectionthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollectionThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollectionThroughput.md
ms.openlocfilehash: 0b6b24b0e8c759ca4263d46cf9fe922cd27829e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181398"
---
# <span data-ttu-id="2b430-101">Get-AzCosmosDBMongoDBCollectionThroughput</span><span class="sxs-lookup"><span data-stu-id="2b430-101">Get-AzCosmosDBMongoDBCollectionThroughput</span></span>

## <span data-ttu-id="2b430-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b430-102">SYNOPSIS</span></span>
<span data-ttu-id="2b430-103">Ottiene le proprietà di velocità effettiva diDbDb per la raccolta di MongoDB.</span><span class="sxs-lookup"><span data-stu-id="2b430-103">Gets the CosmosDB throughput properties of MongoDB Collection.</span></span>

## <span data-ttu-id="2b430-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2b430-104">SYNTAX</span></span>

### <span data-ttu-id="2b430-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2b430-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBCollectionThroughput -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2b430-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b430-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -InputObject <PSMongoDBCollectionGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b430-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2b430-107">DESCRIPTION</span></span>
<span data-ttu-id="2b430-108">Il cmdlet **Get-AzCosmosDBMongoDBCollectionThroughput** ottiene le proprietà di velocità effettiva della raccolta di MongoDB.</span><span class="sxs-lookup"><span data-stu-id="2b430-108">The **Get-AzCosmosDBMongoDBCollectionThroughput** cmdlet gets the throughput properties of MongoDB Collection.</span></span>

## <span data-ttu-id="2b430-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2b430-109">EXAMPLES</span></span>

### <span data-ttu-id="2b430-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2b430-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBCollectionThroughput -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {databaseName} -Name {collectionName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="2b430-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2b430-111">PARAMETERS</span></span>

### <span data-ttu-id="2b430-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2b430-112">-AccountName</span></span>
<span data-ttu-id="2b430-113">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="2b430-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2b430-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2b430-114">-Confirm</span></span>
<span data-ttu-id="2b430-115">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b430-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b430-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2b430-116">-DatabaseName</span></span>
<span data-ttu-id="2b430-117">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="2b430-117">Database name.</span></span>

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

### <span data-ttu-id="2b430-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b430-118">-DefaultProfile</span></span>
<span data-ttu-id="2b430-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2b430-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b430-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b430-120">-InputObject</span></span>
<span data-ttu-id="2b430-121">Se viene specificato, il cmdlet restituisce la raccolta con il valore di velocità effettiva corrispondente.</span><span class="sxs-lookup"><span data-stu-id="2b430-121">If provided then, the cmdlet returns the collection with the corresponding throughput value.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b430-122">-Name</span><span class="sxs-lookup"><span data-stu-id="2b430-122">-Name</span></span>
<span data-ttu-id="2b430-123">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="2b430-123">Collection name.</span></span>

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

### <span data-ttu-id="2b430-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b430-124">-ResourceGroupName</span></span>
<span data-ttu-id="2b430-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2b430-125">Name of resource group.</span></span>

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

### <span data-ttu-id="2b430-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b430-126">-WhatIf</span></span>
<span data-ttu-id="2b430-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2b430-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b430-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2b430-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b430-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b430-129">CommonParameters</span></span>
<span data-ttu-id="2b430-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b430-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b430-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2b430-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b430-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="2b430-132">INPUTS</span></span>

### <span data-ttu-id="2b430-133">Microsoft.Azure.Commands.EnterpriseDb.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="2b430-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="2b430-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2b430-134">OUTPUTS</span></span>

### <span data-ttu-id="2b430-135">Microsoft.Azure.Commands.EnterpriseDb.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="2b430-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="2b430-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="2b430-136">NOTES</span></span>

## <span data-ttu-id="2b430-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2b430-137">RELATED LINKS</span></span>
