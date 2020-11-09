---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: 6f2490eee06ab9cded7634fec1c938d40b4feb50
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299149"
---
# <span data-ttu-id="3ea9b-101">Remove-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="3ea9b-101">Remove-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="3ea9b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3ea9b-102">SYNOPSIS</span></span>
<span data-ttu-id="3ea9b-103">Elimina un database MongoDB CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="3ea9b-103">Deletes a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="3ea9b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3ea9b-104">SYNTAX</span></span>

### <span data-ttu-id="3ea9b-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ea9b-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ea9b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ea9b-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBDatabase -InputObject <PSMongoDBDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ea9b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ea9b-107">DESCRIPTION</span></span>
<span data-ttu-id="3ea9b-108">Il cmdlet **Remove-AzCosmosDBMongoDBDatabase** Elimina un database MongoDB di CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="3ea9b-108">The **Remove-AzCosmosDBMongoDBDatabase** cmdlet deletes a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="3ea9b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3ea9b-109">EXAMPLES</span></span>

### <span data-ttu-id="3ea9b-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3ea9b-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName}
```

<span data-ttu-id="3ea9b-111">Il cmdlet restituisce un oggetto di tipo bool (quando viene passato-PassThru), che è true, se l'eliminazione è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="3ea9b-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="3ea9b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3ea9b-112">PARAMETERS</span></span>

### <span data-ttu-id="3ea9b-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3ea9b-113">-AccountName</span></span>
<span data-ttu-id="3ea9b-114">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="3ea9b-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="3ea9b-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3ea9b-115">-Confirm</span></span>
<span data-ttu-id="3ea9b-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ea9b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ea9b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ea9b-117">-DefaultProfile</span></span>
<span data-ttu-id="3ea9b-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3ea9b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ea9b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ea9b-119">-InputObject</span></span>
<span data-ttu-id="3ea9b-120">Oggetto di database Mongo.</span><span class="sxs-lookup"><span data-stu-id="3ea9b-120">Mongo Database object.</span></span>

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

### <span data-ttu-id="3ea9b-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="3ea9b-121">-Name</span></span>
<span data-ttu-id="3ea9b-122">Nome database.</span><span class="sxs-lookup"><span data-stu-id="3ea9b-122">Database name.</span></span>

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

### <span data-ttu-id="3ea9b-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3ea9b-123">-PassThru</span></span>
<span data-ttu-id="3ea9b-124">Da impostare su true se l'utente vuole ricevere un output.</span><span class="sxs-lookup"><span data-stu-id="3ea9b-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="3ea9b-125">L'output è true se l'operazione è stata eseguita correttamente e se non viene generato un errore.</span><span class="sxs-lookup"><span data-stu-id="3ea9b-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="3ea9b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ea9b-126">-ResourceGroupName</span></span>
<span data-ttu-id="3ea9b-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3ea9b-127">Name of resource group.</span></span>

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

### <span data-ttu-id="3ea9b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ea9b-128">-WhatIf</span></span>
<span data-ttu-id="3ea9b-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3ea9b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ea9b-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3ea9b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ea9b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ea9b-131">CommonParameters</span></span>
<span data-ttu-id="3ea9b-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ea9b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ea9b-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ea9b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ea9b-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3ea9b-134">INPUTS</span></span>

### <span data-ttu-id="3ea9b-135">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="3ea9b-135">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="3ea9b-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3ea9b-136">OUTPUTS</span></span>

### <span data-ttu-id="3ea9b-137">System. void</span><span class="sxs-lookup"><span data-stu-id="3ea9b-137">System.Void</span></span>

### <span data-ttu-id="3ea9b-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3ea9b-138">System.Boolean</span></span>

## <span data-ttu-id="3ea9b-139">Note</span><span class="sxs-lookup"><span data-stu-id="3ea9b-139">NOTES</span></span>

## <span data-ttu-id="3ea9b-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3ea9b-140">RELATED LINKS</span></span>
