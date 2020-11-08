---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 8496df5eb29d3f3a552e5b68a5e481d5cb01efd1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192570"
---
# <span data-ttu-id="813d8-101">Remove-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="813d8-101">Remove-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="813d8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="813d8-102">SYNOPSIS</span></span>
<span data-ttu-id="813d8-103">Elimina il database SQL di CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="813d8-103">Deletes the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="813d8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="813d8-104">SYNTAX</span></span>

### <span data-ttu-id="813d8-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="813d8-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="813d8-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="813d8-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlDatabase -InputObject <PSSqlDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="813d8-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="813d8-107">DESCRIPTION</span></span>
<span data-ttu-id="813d8-108">Il cmdlet **Remove-AzCosmosDBSqlDatabase** Elimina il database SQL CosmosDB corrispondente alla ResourceGroupName specificata, AccountName e DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="813d8-108">The **Remove-AzCosmosDBSqlDatabase** cmdlet deletes the CosmosDB Sql Database corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="813d8-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="813d8-109">EXAMPLES</span></span>

### <span data-ttu-id="813d8-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="813d8-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlDatabase -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {databaseName}
```

## <span data-ttu-id="813d8-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="813d8-111">PARAMETERS</span></span>

### <span data-ttu-id="813d8-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="813d8-112">-AccountName</span></span>
<span data-ttu-id="813d8-113">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="813d8-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="813d8-114">-Confermare</span><span class="sxs-lookup"><span data-stu-id="813d8-114">-Confirm</span></span>
<span data-ttu-id="813d8-115">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="813d8-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="813d8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="813d8-116">-DefaultProfile</span></span>
<span data-ttu-id="813d8-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="813d8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="813d8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="813d8-118">-InputObject</span></span>
<span data-ttu-id="813d8-119">Oggetto database SQL.</span><span class="sxs-lookup"><span data-stu-id="813d8-119">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="813d8-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="813d8-120">-Name</span></span>
<span data-ttu-id="813d8-121">Nome database.</span><span class="sxs-lookup"><span data-stu-id="813d8-121">Database name.</span></span>

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

### <span data-ttu-id="813d8-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="813d8-122">-PassThru</span></span>
<span data-ttu-id="813d8-123">Da impostare su true se l'utente vuole ricevere un output.</span><span class="sxs-lookup"><span data-stu-id="813d8-123">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="813d8-124">L'output è true se l'operazione è stata eseguita correttamente e se non viene generato un errore.</span><span class="sxs-lookup"><span data-stu-id="813d8-124">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="813d8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="813d8-125">-ResourceGroupName</span></span>
<span data-ttu-id="813d8-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="813d8-126">Name of resource group.</span></span>

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

### <span data-ttu-id="813d8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="813d8-127">-WhatIf</span></span>
<span data-ttu-id="813d8-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="813d8-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="813d8-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="813d8-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="813d8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="813d8-130">CommonParameters</span></span>
<span data-ttu-id="813d8-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="813d8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="813d8-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="813d8-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="813d8-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="813d8-133">INPUTS</span></span>

### <span data-ttu-id="813d8-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="813d8-134">None</span></span>

## <span data-ttu-id="813d8-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="813d8-135">OUTPUTS</span></span>

### <span data-ttu-id="813d8-136">System. void</span><span class="sxs-lookup"><span data-stu-id="813d8-136">System.Void</span></span>

### <span data-ttu-id="813d8-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="813d8-137">System.Boolean</span></span>

## <span data-ttu-id="813d8-138">Note</span><span class="sxs-lookup"><span data-stu-id="813d8-138">NOTES</span></span>

## <span data-ttu-id="813d8-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="813d8-139">RELATED LINKS</span></span>