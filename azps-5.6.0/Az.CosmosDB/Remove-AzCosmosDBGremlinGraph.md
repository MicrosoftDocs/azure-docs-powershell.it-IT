---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/remove-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 4838a2de4a61d0c00371ab018d441dcd52bec699
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971309"
---
# <span data-ttu-id="1d86b-101">Remove-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="1d86b-101">Remove-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="1d86b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d86b-102">SYNOPSIS</span></span>
<span data-ttu-id="1d86b-103">Elimina un diagramma di Gremlin di Undb.</span><span class="sxs-lookup"><span data-stu-id="1d86b-103">Deletes a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="1d86b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1d86b-104">SYNTAX</span></span>

### <span data-ttu-id="1d86b-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1d86b-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1d86b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d86b-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBGremlinGraph -InputObject <PSGremlinGraphGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d86b-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1d86b-107">DESCRIPTION</span></span>
<span data-ttu-id="1d86b-108">Il cmdlet **Remove-AzCosmosDBGremlinGraph** elimina un grafoFosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="1d86b-108">The **Remove-AzCosmosDBGremlinGraph** cmdlet deletes a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="1d86b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1d86b-109">EXAMPLES</span></span>

### <span data-ttu-id="1d86b-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1d86b-110">Example 1</span></span>
```powershell
Remove-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}
```

<span data-ttu-id="1d86b-111">Il cmdlet restituisce un oggetto di tipo bool(when -PassThru is passed), che è true se l'eliminazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="1d86b-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="1d86b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d86b-112">PARAMETERS</span></span>

### <span data-ttu-id="1d86b-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1d86b-113">-AccountName</span></span>
<span data-ttu-id="1d86b-114">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="1d86b-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1d86b-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1d86b-115">-Confirm</span></span>
<span data-ttu-id="1d86b-116">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d86b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d86b-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1d86b-117">-DatabaseName</span></span>
<span data-ttu-id="1d86b-118">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="1d86b-118">Database name.</span></span>

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

### <span data-ttu-id="1d86b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d86b-119">-DefaultProfile</span></span>
<span data-ttu-id="1d86b-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1d86b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d86b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d86b-121">-InputObject</span></span>
<span data-ttu-id="1d86b-122">Oggetto Grafico Di Gremlin.</span><span class="sxs-lookup"><span data-stu-id="1d86b-122">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="1d86b-123">-Name</span><span class="sxs-lookup"><span data-stu-id="1d86b-123">-Name</span></span>
<span data-ttu-id="1d86b-124">Nome del grafo Gremlin.</span><span class="sxs-lookup"><span data-stu-id="1d86b-124">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="1d86b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1d86b-125">-PassThru</span></span>
<span data-ttu-id="1d86b-126">Per essere impostato su true se l'utente vuole ricevere un output.</span><span class="sxs-lookup"><span data-stu-id="1d86b-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="1d86b-127">L'output è true se l'operazione è riuscita e in caso contrario viene generato un errore.</span><span class="sxs-lookup"><span data-stu-id="1d86b-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d86b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d86b-128">-ResourceGroupName</span></span>
<span data-ttu-id="1d86b-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1d86b-129">Name of resource group.</span></span>

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

### <span data-ttu-id="1d86b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d86b-130">-WhatIf</span></span>
<span data-ttu-id="1d86b-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1d86b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d86b-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1d86b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d86b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d86b-133">CommonParameters</span></span>
<span data-ttu-id="1d86b-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d86b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d86b-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1d86b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d86b-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="1d86b-136">INPUTS</span></span>

### <span data-ttu-id="1d86b-137">Microsoft.Azure.Commands.GenesDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="1d86b-137">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="1d86b-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1d86b-138">OUTPUTS</span></span>

### <span data-ttu-id="1d86b-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="1d86b-139">System.Void</span></span>

### <span data-ttu-id="1d86b-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1d86b-140">System.Boolean</span></span>

## <span data-ttu-id="1d86b-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="1d86b-141">NOTES</span></span>

## <span data-ttu-id="1d86b-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1d86b-142">RELATED LINKS</span></span>
