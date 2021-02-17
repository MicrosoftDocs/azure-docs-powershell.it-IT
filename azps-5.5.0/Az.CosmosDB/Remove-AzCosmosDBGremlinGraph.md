---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 560fcaa33e635eefd4ba94c5c7cbd05cba1cc304
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209842"
---
# <span data-ttu-id="42aac-101">Remove-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="42aac-101">Remove-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="42aac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42aac-102">SYNOPSIS</span></span>
<span data-ttu-id="42aac-103">Elimina un diagramma di Gremlin di Undb.</span><span class="sxs-lookup"><span data-stu-id="42aac-103">Deletes a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="42aac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="42aac-104">SYNTAX</span></span>

### <span data-ttu-id="42aac-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="42aac-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="42aac-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="42aac-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBGremlinGraph -InputObject <PSGremlinGraphGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42aac-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="42aac-107">DESCRIPTION</span></span>
<span data-ttu-id="42aac-108">Il cmdlet **Remove-AzCosmosDBGremlinGraph** elimina un grafoFosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="42aac-108">The **Remove-AzCosmosDBGremlinGraph** cmdlet deletes a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="42aac-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="42aac-109">EXAMPLES</span></span>

### <span data-ttu-id="42aac-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="42aac-110">Example 1</span></span>
```powershell
Remove-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}
```

<span data-ttu-id="42aac-111">Il cmdlet restituisce un oggetto di tipo bool(when -PassThru is passed), che è true, se l'eliminazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="42aac-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="42aac-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="42aac-112">PARAMETERS</span></span>

### <span data-ttu-id="42aac-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="42aac-113">-AccountName</span></span>
<span data-ttu-id="42aac-114">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="42aac-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="42aac-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="42aac-115">-Confirm</span></span>
<span data-ttu-id="42aac-116">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42aac-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42aac-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="42aac-117">-DatabaseName</span></span>
<span data-ttu-id="42aac-118">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="42aac-118">Database name.</span></span>

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

### <span data-ttu-id="42aac-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42aac-119">-DefaultProfile</span></span>
<span data-ttu-id="42aac-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="42aac-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42aac-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42aac-121">-InputObject</span></span>
<span data-ttu-id="42aac-122">Oggetto Gremlin Graph.</span><span class="sxs-lookup"><span data-stu-id="42aac-122">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="42aac-123">-Name</span><span class="sxs-lookup"><span data-stu-id="42aac-123">-Name</span></span>
<span data-ttu-id="42aac-124">Nome del grafo Gremlin.</span><span class="sxs-lookup"><span data-stu-id="42aac-124">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="42aac-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="42aac-125">-PassThru</span></span>
<span data-ttu-id="42aac-126">Per essere impostato su true se l'utente vuole ricevere un output.</span><span class="sxs-lookup"><span data-stu-id="42aac-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="42aac-127">L'output è true se l'operazione è riuscita e in caso contrario viene generato un errore.</span><span class="sxs-lookup"><span data-stu-id="42aac-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="42aac-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42aac-128">-ResourceGroupName</span></span>
<span data-ttu-id="42aac-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="42aac-129">Name of resource group.</span></span>

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

### <span data-ttu-id="42aac-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42aac-130">-WhatIf</span></span>
<span data-ttu-id="42aac-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="42aac-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42aac-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="42aac-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42aac-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42aac-133">CommonParameters</span></span>
<span data-ttu-id="42aac-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42aac-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42aac-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="42aac-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42aac-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="42aac-136">INPUTS</span></span>

### <span data-ttu-id="42aac-137">Microsoft.Azure.Commands.EnterpriseDb.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="42aac-137">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="42aac-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="42aac-138">OUTPUTS</span></span>

### <span data-ttu-id="42aac-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="42aac-139">System.Void</span></span>

### <span data-ttu-id="42aac-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="42aac-140">System.Boolean</span></span>

## <span data-ttu-id="42aac-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="42aac-141">NOTES</span></span>

## <span data-ttu-id="42aac-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="42aac-142">RELATED LINKS</span></span>
