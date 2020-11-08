---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: 37da28136e8c0a794e263cff4c2b9f9c0d6ce69f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022400"
---
# <span data-ttu-id="dac92-101">Remove-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="dac92-101">Remove-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="dac92-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dac92-102">SYNOPSIS</span></span>
<span data-ttu-id="dac92-103">Elimina il CosmosDB SQL.</span><span class="sxs-lookup"><span data-stu-id="dac92-103">Deletes the CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="dac92-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dac92-104">SYNTAX</span></span>

### <span data-ttu-id="dac92-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="dac92-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> -ContainerName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dac92-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dac92-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlUserDefinedFunction -InputObject <PSSqlUserDefinedFunctionGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dac92-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dac92-107">DESCRIPTION</span></span>
<span data-ttu-id="dac92-108">Il cmdlet **Remove-AzCosmosDBSqlUserDefinedFunction** Elimina il CosmosDB SQL che corrisponde alla ResourceGroupName specificata, AccountName e DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="dac92-108">The **Remove-AzCosmosDBSqlUserDefinedFunction** cmdlet deletes the CosmosDB Sql UserDefinedFunction corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="dac92-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dac92-109">EXAMPLES</span></span>

### <span data-ttu-id="dac92-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="dac92-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {userDefinedFunctionName}
```

## <span data-ttu-id="dac92-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dac92-111">PARAMETERS</span></span>

### <span data-ttu-id="dac92-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="dac92-112">-AccountName</span></span>
<span data-ttu-id="dac92-113">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="dac92-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="dac92-114">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dac92-114">-Confirm</span></span>
<span data-ttu-id="dac92-115">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dac92-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dac92-116">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="dac92-116">-ContainerName</span></span>
<span data-ttu-id="dac92-117">Nome contenitore.</span><span class="sxs-lookup"><span data-stu-id="dac92-117">Container name.</span></span>

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

### <span data-ttu-id="dac92-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dac92-118">-DatabaseName</span></span>
<span data-ttu-id="dac92-119">Nome database.</span><span class="sxs-lookup"><span data-stu-id="dac92-119">Database name.</span></span>

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

### <span data-ttu-id="dac92-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dac92-120">-DefaultProfile</span></span>
<span data-ttu-id="dac92-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dac92-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dac92-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dac92-122">-InputObject</span></span>
<span data-ttu-id="dac92-123">Oggetto funzione definito dall'utente SQL</span><span class="sxs-lookup"><span data-stu-id="dac92-123">Sql User Defined Function Object</span></span>

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

### <span data-ttu-id="dac92-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="dac92-124">-Name</span></span>
<span data-ttu-id="dac92-125">Nome della funzione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="dac92-125">User Defined Function Name.</span></span>

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

### <span data-ttu-id="dac92-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dac92-126">-PassThru</span></span>
<span data-ttu-id="dac92-127">Da impostare su true se l'utente vuole ricevere un output.</span><span class="sxs-lookup"><span data-stu-id="dac92-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="dac92-128">L'output è true se l'operazione è stata eseguita correttamente e se non viene generato un errore.</span><span class="sxs-lookup"><span data-stu-id="dac92-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="dac92-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dac92-129">-ResourceGroupName</span></span>
<span data-ttu-id="dac92-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dac92-130">Name of resource group.</span></span>

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

### <span data-ttu-id="dac92-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dac92-131">-WhatIf</span></span>
<span data-ttu-id="dac92-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dac92-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dac92-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dac92-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dac92-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dac92-134">CommonParameters</span></span>
<span data-ttu-id="dac92-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dac92-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dac92-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dac92-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dac92-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dac92-137">INPUTS</span></span>

### <span data-ttu-id="dac92-138">Nessuno</span><span class="sxs-lookup"><span data-stu-id="dac92-138">None</span></span>

## <span data-ttu-id="dac92-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dac92-139">OUTPUTS</span></span>

### <span data-ttu-id="dac92-140">System. void</span><span class="sxs-lookup"><span data-stu-id="dac92-140">System.Void</span></span>

### <span data-ttu-id="dac92-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dac92-141">System.Boolean</span></span>

## <span data-ttu-id="dac92-142">Note</span><span class="sxs-lookup"><span data-stu-id="dac92-142">NOTES</span></span>

## <span data-ttu-id="dac92-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dac92-143">RELATED LINKS</span></span>
