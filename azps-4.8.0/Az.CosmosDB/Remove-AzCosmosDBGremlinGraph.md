---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 560fcaa33e635eefd4ba94c5c7cbd05cba1cc304
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190816"
---
# <span data-ttu-id="1b8e7-101">Remove-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="1b8e7-101">Remove-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="1b8e7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1b8e7-102">SYNOPSIS</span></span>
<span data-ttu-id="1b8e7-103">Elimina un grafico CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="1b8e7-103">Deletes a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="1b8e7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1b8e7-104">SYNTAX</span></span>

### <span data-ttu-id="1b8e7-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1b8e7-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1b8e7-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b8e7-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBGremlinGraph -InputObject <PSGremlinGraphGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b8e7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b8e7-107">DESCRIPTION</span></span>
<span data-ttu-id="1b8e7-108">Il cmdlet **Remove-AzCosmosDBGremlinGraph** Elimina un grafico Gremlin di CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="1b8e7-108">The **Remove-AzCosmosDBGremlinGraph** cmdlet deletes a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="1b8e7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1b8e7-109">EXAMPLES</span></span>

### <span data-ttu-id="1b8e7-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1b8e7-110">Example 1</span></span>
```powershell
Remove-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}
```

<span data-ttu-id="1b8e7-111">Il cmdlet restituisce un oggetto di tipo bool (quando viene passato-PassThru), che è true, se l'eliminazione è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="1b8e7-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="1b8e7-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1b8e7-112">PARAMETERS</span></span>

### <span data-ttu-id="1b8e7-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1b8e7-113">-AccountName</span></span>
<span data-ttu-id="1b8e7-114">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="1b8e7-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1b8e7-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1b8e7-115">-Confirm</span></span>
<span data-ttu-id="1b8e7-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b8e7-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b8e7-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1b8e7-117">-DatabaseName</span></span>
<span data-ttu-id="1b8e7-118">Nome database.</span><span class="sxs-lookup"><span data-stu-id="1b8e7-118">Database name.</span></span>

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

### <span data-ttu-id="1b8e7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b8e7-119">-DefaultProfile</span></span>
<span data-ttu-id="1b8e7-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1b8e7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b8e7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1b8e7-121">-InputObject</span></span>
<span data-ttu-id="1b8e7-122">Oggetto grafico Gremlin.</span><span class="sxs-lookup"><span data-stu-id="1b8e7-122">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="1b8e7-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="1b8e7-123">-Name</span></span>
<span data-ttu-id="1b8e7-124">Nome del grafico Gremlin.</span><span class="sxs-lookup"><span data-stu-id="1b8e7-124">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="1b8e7-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1b8e7-125">-PassThru</span></span>
<span data-ttu-id="1b8e7-126">Da impostare su true se l'utente vuole ricevere un output.</span><span class="sxs-lookup"><span data-stu-id="1b8e7-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="1b8e7-127">L'output è true se l'operazione è stata eseguita correttamente e se non viene generato un errore.</span><span class="sxs-lookup"><span data-stu-id="1b8e7-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="1b8e7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b8e7-128">-ResourceGroupName</span></span>
<span data-ttu-id="1b8e7-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1b8e7-129">Name of resource group.</span></span>

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

### <span data-ttu-id="1b8e7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b8e7-130">-WhatIf</span></span>
<span data-ttu-id="1b8e7-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1b8e7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b8e7-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1b8e7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b8e7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b8e7-133">CommonParameters</span></span>
<span data-ttu-id="1b8e7-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b8e7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b8e7-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1b8e7-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b8e7-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1b8e7-136">INPUTS</span></span>

### <span data-ttu-id="1b8e7-137">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="1b8e7-137">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="1b8e7-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1b8e7-138">OUTPUTS</span></span>

### <span data-ttu-id="1b8e7-139">System. void</span><span class="sxs-lookup"><span data-stu-id="1b8e7-139">System.Void</span></span>

### <span data-ttu-id="1b8e7-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1b8e7-140">System.Boolean</span></span>

## <span data-ttu-id="1b8e7-141">Note</span><span class="sxs-lookup"><span data-stu-id="1b8e7-141">NOTES</span></span>

## <span data-ttu-id="1b8e7-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1b8e7-142">RELATED LINKS</span></span>