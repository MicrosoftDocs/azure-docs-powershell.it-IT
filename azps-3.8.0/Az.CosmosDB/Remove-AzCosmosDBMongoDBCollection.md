---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 69d3fa5be2b5650a3d4093c63a20d43e098062b6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021578"
---
# <span data-ttu-id="9c18c-101">Remove-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="9c18c-101">Remove-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="9c18c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9c18c-102">SYNOPSIS</span></span>
<span data-ttu-id="9c18c-103">Elimina una raccolta di CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="9c18c-103">Deletes a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="9c18c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9c18c-104">SYNTAX</span></span>

### <span data-ttu-id="9c18c-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9c18c-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9c18c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c18c-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBCollection -InputObject <PSMongoDBCollectionGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c18c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9c18c-107">DESCRIPTION</span></span>
<span data-ttu-id="9c18c-108">Il cmdlet **Remove-AzCosmosDBMongoDBCollection** Elimina una raccolta di CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="9c18c-108">The **Remove-AzCosmosDBMongoDBCollection** cmdlet deletes a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="9c18c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9c18c-109">EXAMPLES</span></span>

### <span data-ttu-id="9c18c-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9c18c-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {collectionName}
```

<span data-ttu-id="9c18c-111">Il cmdlet restituisce un oggetto di tipo bool (quando viene passato-PassThru), che è true, se l'eliminazione è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="9c18c-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="9c18c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9c18c-112">PARAMETERS</span></span>

### <span data-ttu-id="9c18c-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9c18c-113">-AccountName</span></span>
<span data-ttu-id="9c18c-114">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="9c18c-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9c18c-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9c18c-115">-Confirm</span></span>
<span data-ttu-id="9c18c-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c18c-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c18c-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9c18c-117">-DatabaseName</span></span>
<span data-ttu-id="9c18c-118">Nome database.</span><span class="sxs-lookup"><span data-stu-id="9c18c-118">Database name.</span></span>

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

### <span data-ttu-id="9c18c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c18c-119">-DefaultProfile</span></span>
<span data-ttu-id="9c18c-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9c18c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c18c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c18c-121">-InputObject</span></span>
<span data-ttu-id="9c18c-122">Oggetto contenitore SQL.</span><span class="sxs-lookup"><span data-stu-id="9c18c-122">Sql Container object.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c18c-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="9c18c-123">-Name</span></span>
<span data-ttu-id="9c18c-124">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="9c18c-124">Collection name.</span></span>

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

### <span data-ttu-id="9c18c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c18c-125">-PassThru</span></span>
<span data-ttu-id="9c18c-126">Da impostare su true se l'utente vuole ricevere un output.</span><span class="sxs-lookup"><span data-stu-id="9c18c-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="9c18c-127">L'output è true se l'operazione è stata eseguita correttamente e se non viene generato un errore.</span><span class="sxs-lookup"><span data-stu-id="9c18c-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="9c18c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c18c-128">-ResourceGroupName</span></span>
<span data-ttu-id="9c18c-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9c18c-129">Name of resource group.</span></span>

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

### <span data-ttu-id="9c18c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c18c-130">-WhatIf</span></span>
<span data-ttu-id="9c18c-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9c18c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c18c-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9c18c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c18c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c18c-133">CommonParameters</span></span>
<span data-ttu-id="9c18c-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c18c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c18c-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c18c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c18c-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9c18c-136">INPUTS</span></span>

### <span data-ttu-id="9c18c-137">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="9c18c-137">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="9c18c-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9c18c-138">OUTPUTS</span></span>

### <span data-ttu-id="9c18c-139">System. void</span><span class="sxs-lookup"><span data-stu-id="9c18c-139">System.Void</span></span>

### <span data-ttu-id="9c18c-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9c18c-140">System.Boolean</span></span>

## <span data-ttu-id="9c18c-141">Note</span><span class="sxs-lookup"><span data-stu-id="9c18c-141">NOTES</span></span>

## <span data-ttu-id="9c18c-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9c18c-142">RELATED LINKS</span></span>
