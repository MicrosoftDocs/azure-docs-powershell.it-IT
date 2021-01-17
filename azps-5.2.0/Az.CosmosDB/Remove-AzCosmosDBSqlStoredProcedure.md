---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: 6abad7d11da1ba73f1f34804c32bddeb779b0b1d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336355"
---
# <span data-ttu-id="94967-101">Remove-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="94967-101">Remove-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="94967-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="94967-102">SYNOPSIS</span></span>
<span data-ttu-id="94967-103">Elimina il CosmosDB SQL StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="94967-103">Deletes the CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="94967-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="94967-104">SYNTAX</span></span>

### <span data-ttu-id="94967-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="94967-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94967-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="94967-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlStoredProcedure -InputObject <PSSqlStoredProcedureGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94967-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="94967-107">DESCRIPTION</span></span>
<span data-ttu-id="94967-108">Il cmdlet **Remove-AzCosmosDBSqlStoredProcedure** Elimina il CosmosDB SQL StoredProcedure corrispondente alla ResourceGroupName specificata, AccountName e DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="94967-108">The **Remove-AzCosmosDBSqlStoredProcedure** cmdlet deletes the CosmosDB Sql StoredProcedure corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="94967-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="94967-109">EXAMPLES</span></span>

### <span data-ttu-id="94967-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="94967-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlStoredProcedure -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {storedProcedureName}
```

## <span data-ttu-id="94967-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="94967-111">PARAMETERS</span></span>

### <span data-ttu-id="94967-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="94967-112">-AccountName</span></span>
<span data-ttu-id="94967-113">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="94967-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="94967-114">-Confermare</span><span class="sxs-lookup"><span data-stu-id="94967-114">-Confirm</span></span>
<span data-ttu-id="94967-115">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94967-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94967-116">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="94967-116">-ContainerName</span></span>
<span data-ttu-id="94967-117">Nome contenitore.</span><span class="sxs-lookup"><span data-stu-id="94967-117">Container name.</span></span>

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

### <span data-ttu-id="94967-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="94967-118">-DatabaseName</span></span>
<span data-ttu-id="94967-119">Nome database.</span><span class="sxs-lookup"><span data-stu-id="94967-119">Database name.</span></span>

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

### <span data-ttu-id="94967-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94967-120">-DefaultProfile</span></span>
<span data-ttu-id="94967-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="94967-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94967-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94967-122">-InputObject</span></span>
<span data-ttu-id="94967-123">Oggetto database SQL.</span><span class="sxs-lookup"><span data-stu-id="94967-123">Sql Database object.</span></span>

```yaml
Type: PSSqlStoredProcedureGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94967-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="94967-124">-Name</span></span>
<span data-ttu-id="94967-125">Nome Prcodecure archiviato.</span><span class="sxs-lookup"><span data-stu-id="94967-125">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="94967-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="94967-126">-PassThru</span></span>
<span data-ttu-id="94967-127">Da impostare su true se l'utente vuole ricevere un output.</span><span class="sxs-lookup"><span data-stu-id="94967-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="94967-128">L'output è true se l'operazione è stata eseguita correttamente e se non viene generato un errore.</span><span class="sxs-lookup"><span data-stu-id="94967-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="94967-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94967-129">-ResourceGroupName</span></span>
<span data-ttu-id="94967-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="94967-130">Name of resource group.</span></span>

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

### <span data-ttu-id="94967-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94967-131">-WhatIf</span></span>
<span data-ttu-id="94967-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="94967-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94967-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="94967-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94967-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94967-134">CommonParameters</span></span>
<span data-ttu-id="94967-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94967-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94967-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94967-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94967-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="94967-137">INPUTS</span></span>

### <span data-ttu-id="94967-138">Nessuno</span><span class="sxs-lookup"><span data-stu-id="94967-138">None</span></span>

## <span data-ttu-id="94967-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="94967-139">OUTPUTS</span></span>

### <span data-ttu-id="94967-140">System. void</span><span class="sxs-lookup"><span data-stu-id="94967-140">System.Void</span></span>

### <span data-ttu-id="94967-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="94967-141">System.Boolean</span></span>

## <span data-ttu-id="94967-142">Note</span><span class="sxs-lookup"><span data-stu-id="94967-142">NOTES</span></span>

## <span data-ttu-id="94967-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="94967-143">RELATED LINKS</span></span>
