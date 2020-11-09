---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: 1c29b8fd4f81f67b5eaae9de06d055e5e1a2dace
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299544"
---
# <span data-ttu-id="b38ce-101">Get-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="b38ce-101">Get-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="b38ce-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b38ce-102">SYNOPSIS</span></span>
<span data-ttu-id="b38ce-103">Ottiene la velocità effettiva di un grafico di CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="b38ce-103">Gets the throughput of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="b38ce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b38ce-104">SYNTAX</span></span>

### <span data-ttu-id="b38ce-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b38ce-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraphThroughput -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b38ce-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b38ce-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraphThroughput [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b38ce-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b38ce-107">DESCRIPTION</span></span>
<span data-ttu-id="b38ce-108">Il cmdlet **Get-AzCosmosDBGremlinGraphThroughput** ottiene la velocità effettiva di un grafico Gremlin di CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="b38ce-108">The **Get-AzCosmosDBGremlinGraphThroughput** cmdlet gets the throughput of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="b38ce-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b38ce-109">EXAMPLES</span></span>

### <span data-ttu-id="b38ce-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b38ce-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraphThroughput -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="b38ce-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b38ce-111">PARAMETERS</span></span>

### <span data-ttu-id="b38ce-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b38ce-112">-AccountName</span></span>
<span data-ttu-id="b38ce-113">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="b38ce-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b38ce-114">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b38ce-114">-Confirm</span></span>
<span data-ttu-id="b38ce-115">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b38ce-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b38ce-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b38ce-116">-DatabaseName</span></span>
<span data-ttu-id="b38ce-117">Nome database.</span><span class="sxs-lookup"><span data-stu-id="b38ce-117">Database name.</span></span>

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

### <span data-ttu-id="b38ce-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b38ce-118">-DefaultProfile</span></span>
<span data-ttu-id="b38ce-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b38ce-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b38ce-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b38ce-120">-InputObject</span></span>
<span data-ttu-id="b38ce-121">Oggetto grafico Gremlin.</span><span class="sxs-lookup"><span data-stu-id="b38ce-121">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="b38ce-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="b38ce-122">-Name</span></span>
<span data-ttu-id="b38ce-123">Nome del grafico Gremlin.</span><span class="sxs-lookup"><span data-stu-id="b38ce-123">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="b38ce-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b38ce-124">-ResourceGroupName</span></span>
<span data-ttu-id="b38ce-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b38ce-125">Name of resource group.</span></span>

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

### <span data-ttu-id="b38ce-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b38ce-126">-WhatIf</span></span>
<span data-ttu-id="b38ce-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b38ce-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b38ce-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b38ce-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b38ce-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b38ce-129">CommonParameters</span></span>
<span data-ttu-id="b38ce-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b38ce-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b38ce-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b38ce-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b38ce-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b38ce-132">INPUTS</span></span>

### <span data-ttu-id="b38ce-133">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="b38ce-133">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="b38ce-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b38ce-134">OUTPUTS</span></span>

### <span data-ttu-id="b38ce-135">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="b38ce-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="b38ce-136">Note</span><span class="sxs-lookup"><span data-stu-id="b38ce-136">NOTES</span></span>

## <span data-ttu-id="b38ce-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b38ce-137">RELATED LINKS</span></span>
