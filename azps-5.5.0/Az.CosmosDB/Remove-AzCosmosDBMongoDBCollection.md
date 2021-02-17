---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 69d3fa5be2b5650a3d4093c63a20d43e098062b6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177238"
---
# <span data-ttu-id="b5b7d-101">Remove-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="b5b7d-101">Remove-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="b5b7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5b7d-102">SYNOPSIS</span></span>
<span data-ttu-id="b5b7d-103">Elimina una raccolta MagaDBDb.</span><span class="sxs-lookup"><span data-stu-id="b5b7d-103">Deletes a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="b5b7d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b5b7d-104">SYNTAX</span></span>

### <span data-ttu-id="b5b7d-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b5b7d-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b5b7d-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5b7d-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBCollection -InputObject <PSMongoDBCollectionGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5b7d-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b5b7d-107">DESCRIPTION</span></span>
<span data-ttu-id="b5b7d-108">Il cmdlet **Remove-AzCosmosDBMongoDBCollection** elimina una raccolta Dibdb MongoDB.</span><span class="sxs-lookup"><span data-stu-id="b5b7d-108">The **Remove-AzCosmosDBMongoDBCollection** cmdlet deletes a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="b5b7d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b5b7d-109">EXAMPLES</span></span>

### <span data-ttu-id="b5b7d-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b5b7d-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {collectionName}
```

<span data-ttu-id="b5b7d-111">Il cmdlet restituisce un oggetto di tipo bool(when -PassThru is passed), che è true, se l'eliminazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="b5b7d-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="b5b7d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5b7d-112">PARAMETERS</span></span>

### <span data-ttu-id="b5b7d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b5b7d-113">-AccountName</span></span>
<span data-ttu-id="b5b7d-114">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="b5b7d-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b5b7d-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b5b7d-115">-Confirm</span></span>
<span data-ttu-id="b5b7d-116">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5b7d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5b7d-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b5b7d-117">-DatabaseName</span></span>
<span data-ttu-id="b5b7d-118">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="b5b7d-118">Database name.</span></span>

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

### <span data-ttu-id="b5b7d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5b7d-119">-DefaultProfile</span></span>
<span data-ttu-id="b5b7d-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b5b7d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5b7d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5b7d-121">-InputObject</span></span>
<span data-ttu-id="b5b7d-122">Oggetto Contenitore Sql.</span><span class="sxs-lookup"><span data-stu-id="b5b7d-122">Sql Container object.</span></span>

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

### <span data-ttu-id="b5b7d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="b5b7d-123">-Name</span></span>
<span data-ttu-id="b5b7d-124">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="b5b7d-124">Collection name.</span></span>

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

### <span data-ttu-id="b5b7d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b5b7d-125">-PassThru</span></span>
<span data-ttu-id="b5b7d-126">Per essere impostato su true se l'utente vuole ricevere un output.</span><span class="sxs-lookup"><span data-stu-id="b5b7d-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="b5b7d-127">L'output è true se l'operazione è riuscita e in caso contrario viene generato un errore.</span><span class="sxs-lookup"><span data-stu-id="b5b7d-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="b5b7d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5b7d-128">-ResourceGroupName</span></span>
<span data-ttu-id="b5b7d-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b5b7d-129">Name of resource group.</span></span>

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

### <span data-ttu-id="b5b7d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5b7d-130">-WhatIf</span></span>
<span data-ttu-id="b5b7d-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b5b7d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5b7d-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b5b7d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5b7d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5b7d-133">CommonParameters</span></span>
<span data-ttu-id="b5b7d-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5b7d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5b7d-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b5b7d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5b7d-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="b5b7d-136">INPUTS</span></span>

### <span data-ttu-id="b5b7d-137">Microsoft.Azure.Commands.EnterpriseDb.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="b5b7d-137">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="b5b7d-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b5b7d-138">OUTPUTS</span></span>

### <span data-ttu-id="b5b7d-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="b5b7d-139">System.Void</span></span>

### <span data-ttu-id="b5b7d-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b5b7d-140">System.Boolean</span></span>

## <span data-ttu-id="b5b7d-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="b5b7d-141">NOTES</span></span>

## <span data-ttu-id="b5b7d-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b5b7d-142">RELATED LINKS</span></span>
