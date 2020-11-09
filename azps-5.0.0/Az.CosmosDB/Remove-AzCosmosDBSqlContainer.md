---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 2d8d136385470267ee88b139cc3dc23e134b5b88
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299148"
---
# <span data-ttu-id="25056-101">Remove-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="25056-101">Remove-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="25056-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="25056-102">SYNOPSIS</span></span>
<span data-ttu-id="25056-103">Elimina il contenitore SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="25056-103">Deletes the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="25056-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="25056-104">SYNTAX</span></span>

### <span data-ttu-id="25056-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="25056-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="25056-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="25056-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlContainer -InputObject <PSSqlContainerGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25056-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="25056-107">DESCRIPTION</span></span>
<span data-ttu-id="25056-108">Il cmdlet **Remove-AzCosmosDBSqlContainer** Elimina il contenitore SQL CosmosDB corrispondente alla ResourceGroupName specificata, AccountName, DatabaseName e ContainerName.</span><span class="sxs-lookup"><span data-stu-id="25056-108">The **Remove-AzCosmosDBSqlContainer** cmdlet deletes the CosmosDB Sql Container corresponding to the given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="25056-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="25056-109">EXAMPLES</span></span>

### <span data-ttu-id="25056-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="25056-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlContainer -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -Name {containerName}
```

## <span data-ttu-id="25056-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="25056-111">PARAMETERS</span></span>

### <span data-ttu-id="25056-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="25056-112">-AccountName</span></span>
<span data-ttu-id="25056-113">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="25056-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="25056-114">-Confermare</span><span class="sxs-lookup"><span data-stu-id="25056-114">-Confirm</span></span>
<span data-ttu-id="25056-115">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25056-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25056-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="25056-116">-DatabaseName</span></span>
<span data-ttu-id="25056-117">Nome database.</span><span class="sxs-lookup"><span data-stu-id="25056-117">Database name.</span></span>

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

### <span data-ttu-id="25056-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25056-118">-DefaultProfile</span></span>
<span data-ttu-id="25056-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="25056-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25056-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25056-120">-InputObject</span></span>
<span data-ttu-id="25056-121">Oggetto contenitore SQL.</span><span class="sxs-lookup"><span data-stu-id="25056-121">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25056-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="25056-122">-Name</span></span>
<span data-ttu-id="25056-123">Nome contenitore.</span><span class="sxs-lookup"><span data-stu-id="25056-123">Container name.</span></span>

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

### <span data-ttu-id="25056-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25056-124">-PassThru</span></span>
<span data-ttu-id="25056-125">Da impostare su true se l'utente vuole ricevere un output.</span><span class="sxs-lookup"><span data-stu-id="25056-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="25056-126">L'output è true se l'operazione è stata eseguita correttamente e se non viene generato un errore.</span><span class="sxs-lookup"><span data-stu-id="25056-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="25056-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25056-127">-ResourceGroupName</span></span>
<span data-ttu-id="25056-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="25056-128">Name of resource group.</span></span>

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

### <span data-ttu-id="25056-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25056-129">-WhatIf</span></span>
<span data-ttu-id="25056-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="25056-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25056-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="25056-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25056-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25056-132">CommonParameters</span></span>
<span data-ttu-id="25056-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25056-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25056-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="25056-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25056-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="25056-135">INPUTS</span></span>

### <span data-ttu-id="25056-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="25056-136">None</span></span>

## <span data-ttu-id="25056-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="25056-137">OUTPUTS</span></span>

### <span data-ttu-id="25056-138">System. void</span><span class="sxs-lookup"><span data-stu-id="25056-138">System.Void</span></span>

### <span data-ttu-id="25056-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="25056-139">System.Boolean</span></span>

## <span data-ttu-id="25056-140">Note</span><span class="sxs-lookup"><span data-stu-id="25056-140">NOTES</span></span>

## <span data-ttu-id="25056-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="25056-141">RELATED LINKS</span></span>
