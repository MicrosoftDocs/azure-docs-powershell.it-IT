---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbcollectionthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollectionThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollectionThroughput.md
ms.openlocfilehash: 0b6b24b0e8c759ca4263d46cf9fe922cd27829e0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299527"
---
# <span data-ttu-id="e4623-101">Get-AzCosmosDBMongoDBCollectionThroughput</span><span class="sxs-lookup"><span data-stu-id="e4623-101">Get-AzCosmosDBMongoDBCollectionThroughput</span></span>

## <span data-ttu-id="e4623-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e4623-102">SYNOPSIS</span></span>
<span data-ttu-id="e4623-103">Ottiene le proprietà della velocità effettiva CosmosDB della raccolta MongoDB.</span><span class="sxs-lookup"><span data-stu-id="e4623-103">Gets the CosmosDB throughput properties of MongoDB Collection.</span></span>

## <span data-ttu-id="e4623-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e4623-104">SYNTAX</span></span>

### <span data-ttu-id="e4623-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e4623-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBCollectionThroughput -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e4623-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4623-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -InputObject <PSMongoDBCollectionGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4623-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e4623-107">DESCRIPTION</span></span>
<span data-ttu-id="e4623-108">Il cmdlet **Get-AzCosmosDBMongoDBCollectionThroughput** ottiene le proprietà throughput della raccolta MongoDB.</span><span class="sxs-lookup"><span data-stu-id="e4623-108">The **Get-AzCosmosDBMongoDBCollectionThroughput** cmdlet gets the throughput properties of MongoDB Collection.</span></span>

## <span data-ttu-id="e4623-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e4623-109">EXAMPLES</span></span>

### <span data-ttu-id="e4623-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e4623-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBCollectionThroughput -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {databaseName} -Name {collectionName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="e4623-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e4623-111">PARAMETERS</span></span>

### <span data-ttu-id="e4623-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e4623-112">-AccountName</span></span>
<span data-ttu-id="e4623-113">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="e4623-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e4623-114">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e4623-114">-Confirm</span></span>
<span data-ttu-id="e4623-115">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4623-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4623-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e4623-116">-DatabaseName</span></span>
<span data-ttu-id="e4623-117">Nome database.</span><span class="sxs-lookup"><span data-stu-id="e4623-117">Database name.</span></span>

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

### <span data-ttu-id="e4623-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4623-118">-DefaultProfile</span></span>
<span data-ttu-id="e4623-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e4623-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4623-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4623-120">-InputObject</span></span>
<span data-ttu-id="e4623-121">Se specificato, il cmdlet restituisce la raccolta con il valore di throughput corrispondente.</span><span class="sxs-lookup"><span data-stu-id="e4623-121">If provided then, the cmdlet returns the collection with the corresponding throughput value.</span></span>

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

### <span data-ttu-id="e4623-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="e4623-122">-Name</span></span>
<span data-ttu-id="e4623-123">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="e4623-123">Collection name.</span></span>

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

### <span data-ttu-id="e4623-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4623-124">-ResourceGroupName</span></span>
<span data-ttu-id="e4623-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e4623-125">Name of resource group.</span></span>

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

### <span data-ttu-id="e4623-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4623-126">-WhatIf</span></span>
<span data-ttu-id="e4623-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e4623-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4623-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e4623-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4623-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4623-129">CommonParameters</span></span>
<span data-ttu-id="e4623-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4623-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4623-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4623-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4623-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e4623-132">INPUTS</span></span>

### <span data-ttu-id="e4623-133">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="e4623-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="e4623-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e4623-134">OUTPUTS</span></span>

### <span data-ttu-id="e4623-135">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="e4623-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="e4623-136">Note</span><span class="sxs-lookup"><span data-stu-id="e4623-136">NOTES</span></span>

## <span data-ttu-id="e4623-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e4623-137">RELATED LINKS</span></span>
