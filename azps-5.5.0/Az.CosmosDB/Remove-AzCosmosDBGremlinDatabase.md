---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 5c3150e2bdb81c8864116bc521b9f07f2ea43e1b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198935"
---
# <span data-ttu-id="09a49-101">Remove-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="09a49-101">Remove-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="09a49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09a49-102">SYNOPSIS</span></span>
<span data-ttu-id="09a49-103">Elimina un database Diedb Gremlin.</span><span class="sxs-lookup"><span data-stu-id="09a49-103">Deletes a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="09a49-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="09a49-104">SYNTAX</span></span>

### <span data-ttu-id="09a49-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="09a49-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBGremlinDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09a49-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="09a49-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBGremlinDatabase -InputObject <PSGremlinDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09a49-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="09a49-107">DESCRIPTION</span></span>
<span data-ttu-id="09a49-108">Il cmdlet **Remove-AzCosmosDBGremlinDatabase** elimina un databaseDb Gremlin.</span><span class="sxs-lookup"><span data-stu-id="09a49-108">The **Remove-AzCosmosDBGremlinDatabase** cmdlet deletes a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="09a49-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="09a49-109">EXAMPLES</span></span>

### <span data-ttu-id="09a49-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="09a49-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName}
```

<span data-ttu-id="09a49-111">Il cmdlet restituisce un oggetto di tipo bool(when -PassThru is passed), che è true, se l'eliminazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="09a49-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="09a49-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09a49-112">PARAMETERS</span></span>

### <span data-ttu-id="09a49-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="09a49-113">-AccountName</span></span>
<span data-ttu-id="09a49-114">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="09a49-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="09a49-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="09a49-115">-Confirm</span></span>
<span data-ttu-id="09a49-116">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09a49-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09a49-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09a49-117">-DefaultProfile</span></span>
<span data-ttu-id="09a49-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="09a49-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09a49-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09a49-119">-InputObject</span></span>
<span data-ttu-id="09a49-120">Oggetto di database Gremlin.</span><span class="sxs-lookup"><span data-stu-id="09a49-120">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09a49-121">-Name</span><span class="sxs-lookup"><span data-stu-id="09a49-121">-Name</span></span>
<span data-ttu-id="09a49-122">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="09a49-122">Database name.</span></span>

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

### <span data-ttu-id="09a49-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="09a49-123">-PassThru</span></span>
<span data-ttu-id="09a49-124">Per essere impostato su true se l'utente vuole ricevere un output.</span><span class="sxs-lookup"><span data-stu-id="09a49-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="09a49-125">L'output è true se l'operazione è riuscita e in caso contrario viene generato un errore.</span><span class="sxs-lookup"><span data-stu-id="09a49-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="09a49-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09a49-126">-ResourceGroupName</span></span>
<span data-ttu-id="09a49-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="09a49-127">Name of resource group.</span></span>

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

### <span data-ttu-id="09a49-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09a49-128">-WhatIf</span></span>
<span data-ttu-id="09a49-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="09a49-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09a49-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="09a49-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09a49-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09a49-131">CommonParameters</span></span>
<span data-ttu-id="09a49-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09a49-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09a49-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="09a49-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09a49-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="09a49-134">INPUTS</span></span>

### <span data-ttu-id="09a49-135">Microsoft.Azure.Commands.EnterpriseDb.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="09a49-135">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="09a49-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="09a49-136">OUTPUTS</span></span>

### <span data-ttu-id="09a49-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="09a49-137">System.Void</span></span>

### <span data-ttu-id="09a49-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="09a49-138">System.Boolean</span></span>

## <span data-ttu-id="09a49-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="09a49-139">NOTES</span></span>

## <span data-ttu-id="09a49-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="09a49-140">RELATED LINKS</span></span>
