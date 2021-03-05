---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: f5357e23b8a4e4ec5c613dc7a6b1b0f53e5bac3b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983614"
---
# <span data-ttu-id="c97a7-101">Get-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="c97a7-101">Get-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="c97a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c97a7-102">SYNOPSIS</span></span>
<span data-ttu-id="c97a7-103">Ottiene la velocità effettiva di un grafico di Gremlin diDb.</span><span class="sxs-lookup"><span data-stu-id="c97a7-103">Gets the throughput of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="c97a7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c97a7-104">SYNTAX</span></span>

### <span data-ttu-id="c97a7-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c97a7-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraphThroughput -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c97a7-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c97a7-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraphThroughput [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c97a7-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c97a7-107">DESCRIPTION</span></span>
<span data-ttu-id="c97a7-108">Il cmdlet **Get-AzCosmosDBGremlinGraphThroughput** ottiene la velocità effettiva di un diagramma di gremlin di Questo tipo.</span><span class="sxs-lookup"><span data-stu-id="c97a7-108">The **Get-AzCosmosDBGremlinGraphThroughput** cmdlet gets the throughput of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="c97a7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c97a7-109">EXAMPLES</span></span>

### <span data-ttu-id="c97a7-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c97a7-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraphThroughput -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="c97a7-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c97a7-111">PARAMETERS</span></span>

### <span data-ttu-id="c97a7-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c97a7-112">-AccountName</span></span>
<span data-ttu-id="c97a7-113">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="c97a7-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c97a7-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c97a7-114">-Confirm</span></span>
<span data-ttu-id="c97a7-115">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c97a7-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c97a7-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c97a7-116">-DatabaseName</span></span>
<span data-ttu-id="c97a7-117">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="c97a7-117">Database name.</span></span>

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

### <span data-ttu-id="c97a7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c97a7-118">-DefaultProfile</span></span>
<span data-ttu-id="c97a7-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c97a7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c97a7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c97a7-120">-InputObject</span></span>
<span data-ttu-id="c97a7-121">Oggetto Grafico Di Gremlin.</span><span class="sxs-lookup"><span data-stu-id="c97a7-121">Gremlin Graph object.</span></span>

```yaml
Type: PSGremlinGraphGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c97a7-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c97a7-122">-Name</span></span>
<span data-ttu-id="c97a7-123">Nome del grafo Gremlin.</span><span class="sxs-lookup"><span data-stu-id="c97a7-123">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="c97a7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c97a7-124">-ResourceGroupName</span></span>
<span data-ttu-id="c97a7-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c97a7-125">Name of resource group.</span></span>

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

### <span data-ttu-id="c97a7-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c97a7-126">-WhatIf</span></span>
<span data-ttu-id="c97a7-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c97a7-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c97a7-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c97a7-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c97a7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c97a7-129">CommonParameters</span></span>
<span data-ttu-id="c97a7-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c97a7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c97a7-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c97a7-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c97a7-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="c97a7-132">INPUTS</span></span>

### <span data-ttu-id="c97a7-133">Microsoft.Azure.Commands.GenesDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="c97a7-133">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="c97a7-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c97a7-134">OUTPUTS</span></span>

### <span data-ttu-id="c97a7-135">Microsoft.Azure.Commands.EnterpriseDb.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="c97a7-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="c97a7-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="c97a7-136">NOTES</span></span>

## <span data-ttu-id="c97a7-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c97a7-137">RELATED LINKS</span></span>
