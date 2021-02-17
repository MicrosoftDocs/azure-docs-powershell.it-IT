---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: 6f2490eee06ab9cded7634fec1c938d40b4feb50
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209835"
---
# <span data-ttu-id="6236c-101">Remove-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="6236c-101">Remove-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="6236c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6236c-102">SYNOPSIS</span></span>
<span data-ttu-id="6236c-103">Elimina un databaseDbDbDb.</span><span class="sxs-lookup"><span data-stu-id="6236c-103">Deletes a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="6236c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6236c-104">SYNTAX</span></span>

### <span data-ttu-id="6236c-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6236c-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6236c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6236c-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBDatabase -InputObject <PSMongoDBDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6236c-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6236c-107">DESCRIPTION</span></span>
<span data-ttu-id="6236c-108">Il cmdlet **Remove-AzCosmosDBMongoDBDatabase** elimina un databaseDbDb Magodb.</span><span class="sxs-lookup"><span data-stu-id="6236c-108">The **Remove-AzCosmosDBMongoDBDatabase** cmdlet deletes a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="6236c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6236c-109">EXAMPLES</span></span>

### <span data-ttu-id="6236c-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6236c-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName}
```

<span data-ttu-id="6236c-111">Il cmdlet restituisce un oggetto di tipo bool(when -PassThru is passed), che è true se l'eliminazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="6236c-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="6236c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6236c-112">PARAMETERS</span></span>

### <span data-ttu-id="6236c-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6236c-113">-AccountName</span></span>
<span data-ttu-id="6236c-114">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="6236c-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="6236c-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6236c-115">-Confirm</span></span>
<span data-ttu-id="6236c-116">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6236c-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6236c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6236c-117">-DefaultProfile</span></span>
<span data-ttu-id="6236c-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6236c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6236c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6236c-119">-InputObject</span></span>
<span data-ttu-id="6236c-120">Oggetto database mongo.</span><span class="sxs-lookup"><span data-stu-id="6236c-120">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6236c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6236c-121">-Name</span></span>
<span data-ttu-id="6236c-122">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="6236c-122">Database name.</span></span>

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

### <span data-ttu-id="6236c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6236c-123">-PassThru</span></span>
<span data-ttu-id="6236c-124">Per essere impostato su true se l'utente vuole ricevere un output.</span><span class="sxs-lookup"><span data-stu-id="6236c-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="6236c-125">L'output è true se l'operazione è riuscita e in caso contrario viene generato un errore.</span><span class="sxs-lookup"><span data-stu-id="6236c-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="6236c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6236c-126">-ResourceGroupName</span></span>
<span data-ttu-id="6236c-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6236c-127">Name of resource group.</span></span>

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

### <span data-ttu-id="6236c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6236c-128">-WhatIf</span></span>
<span data-ttu-id="6236c-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6236c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6236c-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6236c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6236c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6236c-131">CommonParameters</span></span>
<span data-ttu-id="6236c-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6236c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6236c-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6236c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6236c-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="6236c-134">INPUTS</span></span>

### <span data-ttu-id="6236c-135">Microsoft.Azure.Commands.EnterpriseDb.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="6236c-135">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="6236c-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6236c-136">OUTPUTS</span></span>

### <span data-ttu-id="6236c-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="6236c-137">System.Void</span></span>

### <span data-ttu-id="6236c-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6236c-138">System.Boolean</span></span>

## <span data-ttu-id="6236c-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="6236c-139">NOTES</span></span>

## <span data-ttu-id="6236c-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6236c-140">RELATED LINKS</span></span>
