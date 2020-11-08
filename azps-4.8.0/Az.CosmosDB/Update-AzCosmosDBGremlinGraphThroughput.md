---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: 633ea5263930db74cec3b926c655e54dec10a162
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94193034"
---
# <span data-ttu-id="b673e-101">Update-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="b673e-101">Update-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="b673e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b673e-102">SYNOPSIS</span></span>
<span data-ttu-id="b673e-103">Aggiorna il valore di throughput di un grafico di CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="b673e-103">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="b673e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b673e-104">SYNTAX</span></span>

### <span data-ttu-id="b673e-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b673e-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput -DatabaseName <String> [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b673e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b673e-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b673e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b673e-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b673e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b673e-108">DESCRIPTION</span></span>
<span data-ttu-id="b673e-109">Aggiorna il valore di throughput di un grafico di CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="b673e-109">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="b673e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b673e-110">EXAMPLES</span></span>

### <span data-ttu-id="b673e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b673e-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraphThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myGraphName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabase/{mydatabaseName}/graphs/{myGraphName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="b673e-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b673e-112">PARAMETERS</span></span>

### <span data-ttu-id="b673e-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b673e-113">-AccountName</span></span>
<span data-ttu-id="b673e-114">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="b673e-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b673e-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="b673e-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="b673e-116">Valore massimo della velocità effettiva se autoscale è abilitato.</span><span class="sxs-lookup"><span data-stu-id="b673e-116">Maximum Throughput value if autoscale is enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b673e-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b673e-117">-Confirm</span></span>
<span data-ttu-id="b673e-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b673e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b673e-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b673e-119">-DatabaseName</span></span>
<span data-ttu-id="b673e-120">Nome database.</span><span class="sxs-lookup"><span data-stu-id="b673e-120">Database name.</span></span>

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

### <span data-ttu-id="b673e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b673e-121">-DefaultProfile</span></span>
<span data-ttu-id="b673e-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b673e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b673e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b673e-123">-InputObject</span></span>
<span data-ttu-id="b673e-124">Oggetto database Gremlin.</span><span class="sxs-lookup"><span data-stu-id="b673e-124">Gremlin Database object.</span></span>

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

### <span data-ttu-id="b673e-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="b673e-125">-Name</span></span>
<span data-ttu-id="b673e-126">Nome del grafico Gremlin.</span><span class="sxs-lookup"><span data-stu-id="b673e-126">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="b673e-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b673e-127">-ParentObject</span></span>
<span data-ttu-id="b673e-128">Oggetto database Gremlin.</span><span class="sxs-lookup"><span data-stu-id="b673e-128">Gremlin Database object.</span></span>

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

### <span data-ttu-id="b673e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b673e-129">-ResourceGroupName</span></span>
<span data-ttu-id="b673e-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b673e-130">Name of resource group.</span></span>

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

### <span data-ttu-id="b673e-131">-Throughput</span><span class="sxs-lookup"><span data-stu-id="b673e-131">-Throughput</span></span>
<span data-ttu-id="b673e-132">La velocità effettiva del grafico Gremlin (RU/s).</span><span class="sxs-lookup"><span data-stu-id="b673e-132">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="b673e-133">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="b673e-133">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b673e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b673e-134">-WhatIf</span></span>
<span data-ttu-id="b673e-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b673e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b673e-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b673e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b673e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b673e-137">CommonParameters</span></span>
<span data-ttu-id="b673e-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b673e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b673e-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b673e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b673e-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b673e-140">INPUTS</span></span>

### <span data-ttu-id="b673e-141">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="b673e-141">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="b673e-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b673e-142">OUTPUTS</span></span>

### <span data-ttu-id="b673e-143">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="b673e-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="b673e-144">Note</span><span class="sxs-lookup"><span data-stu-id="b673e-144">NOTES</span></span>

## <span data-ttu-id="b673e-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b673e-145">RELATED LINKS</span></span>
