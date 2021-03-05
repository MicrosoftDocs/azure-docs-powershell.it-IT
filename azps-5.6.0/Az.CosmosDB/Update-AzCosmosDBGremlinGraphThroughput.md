---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: c5d7bc79185639c4ec79ab14d7ed2f6201dcedb6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977325"
---
# <span data-ttu-id="dc0c0-101">Update-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="dc0c0-101">Update-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="dc0c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc0c0-102">SYNOPSIS</span></span>
<span data-ttu-id="dc0c0-103">Aggiorna il valore di velocità effettiva di un grafico di Gremlindb.</span><span class="sxs-lookup"><span data-stu-id="dc0c0-103">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="dc0c0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dc0c0-104">SYNTAX</span></span>

### <span data-ttu-id="dc0c0-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dc0c0-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput -DatabaseName <String> [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc0c0-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc0c0-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc0c0-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc0c0-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc0c0-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="dc0c0-108">DESCRIPTION</span></span>
<span data-ttu-id="dc0c0-109">Aggiorna il valore di velocità effettiva di un grafico di Gremlindb.</span><span class="sxs-lookup"><span data-stu-id="dc0c0-109">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="dc0c0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dc0c0-110">EXAMPLES</span></span>

### <span data-ttu-id="dc0c0-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="dc0c0-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraphThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myGraphName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabase/{mydatabaseName}/graphs/{myGraphName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="dc0c0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc0c0-112">PARAMETERS</span></span>

### <span data-ttu-id="dc0c0-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="dc0c0-113">-AccountName</span></span>
<span data-ttu-id="dc0c0-114">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="dc0c0-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="dc0c0-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="dc0c0-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="dc0c0-116">Valore massimo di velocità effettiva se è abilitata la scalabilità automatica.</span><span class="sxs-lookup"><span data-stu-id="dc0c0-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="dc0c0-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc0c0-117">-Confirm</span></span>
<span data-ttu-id="dc0c0-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc0c0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc0c0-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dc0c0-119">-DatabaseName</span></span>
<span data-ttu-id="dc0c0-120">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="dc0c0-120">Database name.</span></span>

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

### <span data-ttu-id="dc0c0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc0c0-121">-DefaultProfile</span></span>
<span data-ttu-id="dc0c0-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dc0c0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc0c0-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc0c0-123">-InputObject</span></span>
<span data-ttu-id="dc0c0-124">Oggetto di database Gremlin.</span><span class="sxs-lookup"><span data-stu-id="dc0c0-124">Gremlin Database object.</span></span>

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

### <span data-ttu-id="dc0c0-125">-Name</span><span class="sxs-lookup"><span data-stu-id="dc0c0-125">-Name</span></span>
<span data-ttu-id="dc0c0-126">Nome del grafo Gremlin.</span><span class="sxs-lookup"><span data-stu-id="dc0c0-126">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="dc0c0-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="dc0c0-127">-ParentObject</span></span>
<span data-ttu-id="dc0c0-128">Oggetto di database Gremlin.</span><span class="sxs-lookup"><span data-stu-id="dc0c0-128">Gremlin Database object.</span></span>

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

### <span data-ttu-id="dc0c0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc0c0-129">-ResourceGroupName</span></span>
<span data-ttu-id="dc0c0-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dc0c0-130">Name of resource group.</span></span>

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

### <span data-ttu-id="dc0c0-131">-Velocità effettiva</span><span class="sxs-lookup"><span data-stu-id="dc0c0-131">-Throughput</span></span>
<span data-ttu-id="dc0c0-132">Velocità effettiva di Gremlin Graph (RU/s).</span><span class="sxs-lookup"><span data-stu-id="dc0c0-132">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="dc0c0-133">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="dc0c0-133">Default value is 400.</span></span>

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

### <span data-ttu-id="dc0c0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc0c0-134">-WhatIf</span></span>
<span data-ttu-id="dc0c0-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dc0c0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc0c0-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dc0c0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc0c0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc0c0-137">CommonParameters</span></span>
<span data-ttu-id="dc0c0-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc0c0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc0c0-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dc0c0-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc0c0-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="dc0c0-140">INPUTS</span></span>

### <span data-ttu-id="dc0c0-141">Microsoft.Azure.Commands.GenesDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="dc0c0-141">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="dc0c0-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dc0c0-142">OUTPUTS</span></span>

### <span data-ttu-id="dc0c0-143">Microsoft.Azure.Commands.EnterpriseDb.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="dc0c0-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="dc0c0-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="dc0c0-144">NOTES</span></span>

## <span data-ttu-id="dc0c0-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dc0c0-145">RELATED LINKS</span></span>
