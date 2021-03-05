---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/remove-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: 7e7ffd7c06217b4e2d12aaf75684c85f8ab12e9a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983261"
---
# <span data-ttu-id="e4584-101">Remove-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="e4584-101">Remove-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="e4584-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4584-102">SYNOPSIS</span></span>
<span data-ttu-id="e4584-103">Elimina la funzione Sql UserDefinedFunction di DatabaseDb.</span><span class="sxs-lookup"><span data-stu-id="e4584-103">Deletes the CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="e4584-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e4584-104">SYNTAX</span></span>

### <span data-ttu-id="e4584-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4584-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> -ContainerName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4584-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4584-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlUserDefinedFunction -InputObject <PSSqlUserDefinedFunctionGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4584-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e4584-107">DESCRIPTION</span></span>
<span data-ttu-id="e4584-108">Il cmdlet **Remove-AzCosmosDBSqlUserDefinedFunction** elimina il cmdletDb Sql UserDefinedFunction corrispondente ai valori ResourceGroupName, AccountName e DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="e4584-108">The **Remove-AzCosmosDBSqlUserDefinedFunction** cmdlet deletes the CosmosDB Sql UserDefinedFunction corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="e4584-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e4584-109">EXAMPLES</span></span>

### <span data-ttu-id="e4584-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e4584-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {userDefinedFunctionName}
```

## <span data-ttu-id="e4584-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4584-111">PARAMETERS</span></span>

### <span data-ttu-id="e4584-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e4584-112">-AccountName</span></span>
<span data-ttu-id="e4584-113">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="e4584-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e4584-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e4584-114">-Confirm</span></span>
<span data-ttu-id="e4584-115">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4584-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4584-116">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="e4584-116">-ContainerName</span></span>
<span data-ttu-id="e4584-117">Nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="e4584-117">Container name.</span></span>

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

### <span data-ttu-id="e4584-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e4584-118">-DatabaseName</span></span>
<span data-ttu-id="e4584-119">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="e4584-119">Database name.</span></span>

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

### <span data-ttu-id="e4584-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4584-120">-DefaultProfile</span></span>
<span data-ttu-id="e4584-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e4584-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4584-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4584-122">-InputObject</span></span>
<span data-ttu-id="e4584-123">Oggetto Funzione definita dall'utente SQL</span><span class="sxs-lookup"><span data-stu-id="e4584-123">Sql User Defined Function Object</span></span>

```yaml
Type: PSSqlUserDefinedFunctionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4584-124">-Name</span><span class="sxs-lookup"><span data-stu-id="e4584-124">-Name</span></span>
<span data-ttu-id="e4584-125">Nome funzione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="e4584-125">User Defined Function Name.</span></span>

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

### <span data-ttu-id="e4584-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4584-126">-PassThru</span></span>
<span data-ttu-id="e4584-127">Per essere impostato su true se l'utente vuole ricevere un output.</span><span class="sxs-lookup"><span data-stu-id="e4584-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="e4584-128">L'output è true se l'operazione è riuscita e in caso contrario viene generato un errore.</span><span class="sxs-lookup"><span data-stu-id="e4584-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="e4584-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4584-129">-ResourceGroupName</span></span>
<span data-ttu-id="e4584-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e4584-130">Name of resource group.</span></span>

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

### <span data-ttu-id="e4584-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4584-131">-WhatIf</span></span>
<span data-ttu-id="e4584-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e4584-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4584-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e4584-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4584-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4584-134">CommonParameters</span></span>
<span data-ttu-id="e4584-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4584-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4584-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e4584-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4584-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="e4584-137">INPUTS</span></span>

### <span data-ttu-id="e4584-138">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e4584-138">None</span></span>

## <span data-ttu-id="e4584-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e4584-139">OUTPUTS</span></span>

### <span data-ttu-id="e4584-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="e4584-140">System.Void</span></span>

### <span data-ttu-id="e4584-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e4584-141">System.Boolean</span></span>

## <span data-ttu-id="e4584-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="e4584-142">NOTES</span></span>

## <span data-ttu-id="e4584-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e4584-143">RELATED LINKS</span></span>
