---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 69d3fa5be2b5650a3d4093c63a20d43e098062b6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350479"
---
# <span data-ttu-id="40638-101">Remove-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="40638-101">Remove-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="40638-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="40638-102">SYNOPSIS</span></span>
<span data-ttu-id="40638-103">Elimina una raccolta di CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="40638-103">Deletes a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="40638-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="40638-104">SYNTAX</span></span>

### <span data-ttu-id="40638-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="40638-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="40638-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="40638-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBCollection -InputObject <PSMongoDBCollectionGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40638-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="40638-107">DESCRIPTION</span></span>
<span data-ttu-id="40638-108">Il cmdlet **Remove-AzCosmosDBMongoDBCollection** Elimina una raccolta di CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="40638-108">The **Remove-AzCosmosDBMongoDBCollection** cmdlet deletes a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="40638-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="40638-109">EXAMPLES</span></span>

### <span data-ttu-id="40638-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="40638-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {collectionName}
```

<span data-ttu-id="40638-111">Il cmdlet restituisce un oggetto di tipo bool (quando viene passato-PassThru), che è true, se l'eliminazione è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="40638-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="40638-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="40638-112">PARAMETERS</span></span>

### <span data-ttu-id="40638-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="40638-113">-AccountName</span></span>
<span data-ttu-id="40638-114">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="40638-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="40638-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="40638-115">-Confirm</span></span>
<span data-ttu-id="40638-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40638-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40638-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="40638-117">-DatabaseName</span></span>
<span data-ttu-id="40638-118">Nome database.</span><span class="sxs-lookup"><span data-stu-id="40638-118">Database name.</span></span>

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

### <span data-ttu-id="40638-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40638-119">-DefaultProfile</span></span>
<span data-ttu-id="40638-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="40638-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40638-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40638-121">-InputObject</span></span>
<span data-ttu-id="40638-122">Oggetto contenitore SQL.</span><span class="sxs-lookup"><span data-stu-id="40638-122">Sql Container object.</span></span>

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

### <span data-ttu-id="40638-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="40638-123">-Name</span></span>
<span data-ttu-id="40638-124">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="40638-124">Collection name.</span></span>

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

### <span data-ttu-id="40638-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40638-125">-PassThru</span></span>
<span data-ttu-id="40638-126">Da impostare su true se l'utente vuole ricevere un output.</span><span class="sxs-lookup"><span data-stu-id="40638-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="40638-127">L'output è true se l'operazione è stata eseguita correttamente e se non viene generato un errore.</span><span class="sxs-lookup"><span data-stu-id="40638-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="40638-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40638-128">-ResourceGroupName</span></span>
<span data-ttu-id="40638-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="40638-129">Name of resource group.</span></span>

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

### <span data-ttu-id="40638-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40638-130">-WhatIf</span></span>
<span data-ttu-id="40638-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="40638-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40638-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="40638-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40638-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40638-133">CommonParameters</span></span>
<span data-ttu-id="40638-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40638-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40638-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40638-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40638-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="40638-136">INPUTS</span></span>

### <span data-ttu-id="40638-137">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="40638-137">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="40638-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="40638-138">OUTPUTS</span></span>

### <span data-ttu-id="40638-139">System. void</span><span class="sxs-lookup"><span data-stu-id="40638-139">System.Void</span></span>

### <span data-ttu-id="40638-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="40638-140">System.Boolean</span></span>

## <span data-ttu-id="40638-141">Note</span><span class="sxs-lookup"><span data-stu-id="40638-141">NOTES</span></span>

## <span data-ttu-id="40638-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="40638-142">RELATED LINKS</span></span>
