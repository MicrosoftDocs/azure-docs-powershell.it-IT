---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: ee1527beb11db3027a416277ed04a444dda90af0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020141"
---
# <span data-ttu-id="c1095-101">Update-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="c1095-101">Update-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="c1095-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c1095-102">SYNOPSIS</span></span>
<span data-ttu-id="c1095-103">Aggiorna il valore di throughput di un grafico di CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="c1095-103">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="c1095-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c1095-104">SYNTAX</span></span>

### <span data-ttu-id="c1095-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c1095-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> [-Name <String>] -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1095-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1095-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c1095-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1095-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSGremlinGraphGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c1095-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c1095-108">EXAMPLES</span></span>

### <span data-ttu-id="c1095-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c1095-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraphThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myGraphName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabase/{mydatabaseName}/graphs/{myGraphName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="c1095-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c1095-110">PARAMETERS</span></span>

### <span data-ttu-id="c1095-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c1095-111">-AccountName</span></span>
<span data-ttu-id="c1095-112">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="c1095-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c1095-113">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c1095-113">-Confirm</span></span>
<span data-ttu-id="c1095-114">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1095-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1095-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c1095-115">-DatabaseName</span></span>
<span data-ttu-id="c1095-116">Nome database.</span><span class="sxs-lookup"><span data-stu-id="c1095-116">Database name.</span></span>

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

### <span data-ttu-id="c1095-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1095-117">-DefaultProfile</span></span>
<span data-ttu-id="c1095-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c1095-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1095-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c1095-119">-InputObject</span></span>
<span data-ttu-id="c1095-120">Oggetto database Gremlin.</span><span class="sxs-lookup"><span data-stu-id="c1095-120">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinGraphGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1095-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="c1095-121">-Name</span></span>
<span data-ttu-id="c1095-122">Nome del grafico Gremlin.</span><span class="sxs-lookup"><span data-stu-id="c1095-122">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="c1095-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c1095-123">-ParentObject</span></span>
<span data-ttu-id="c1095-124">Oggetto database Gremlin.</span><span class="sxs-lookup"><span data-stu-id="c1095-124">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1095-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1095-125">-ResourceGroupName</span></span>
<span data-ttu-id="c1095-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c1095-126">Name of resource group.</span></span>

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

### <span data-ttu-id="c1095-127">-Throughput</span><span class="sxs-lookup"><span data-stu-id="c1095-127">-Throughput</span></span>
<span data-ttu-id="c1095-128">La velocità effettiva del grafico Gremlin (RU/s).</span><span class="sxs-lookup"><span data-stu-id="c1095-128">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="c1095-129">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="c1095-129">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1095-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1095-130">-WhatIf</span></span>
<span data-ttu-id="c1095-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c1095-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1095-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c1095-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1095-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1095-133">CommonParameters</span></span>
<span data-ttu-id="c1095-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1095-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1095-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1095-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1095-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c1095-136">INPUTS</span></span>

### <span data-ttu-id="c1095-137">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="c1095-137">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="c1095-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c1095-138">OUTPUTS</span></span>

### <span data-ttu-id="c1095-139">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="c1095-139">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="c1095-140">Note</span><span class="sxs-lookup"><span data-stu-id="c1095-140">NOTES</span></span>

## <span data-ttu-id="c1095-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c1095-141">RELATED LINKS</span></span>
