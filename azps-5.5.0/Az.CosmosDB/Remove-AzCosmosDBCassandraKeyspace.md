---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 7f6cae6a3187bf4393ea4fb592123c1833a18ebb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198958"
---
# <span data-ttu-id="6eb00-101">Remove-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="6eb00-101">Remove-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="6eb00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6eb00-102">SYNOPSIS</span></span>
<span data-ttu-id="6eb00-103">Elimina un oggetto Db Cassandra Keyspace.</span><span class="sxs-lookup"><span data-stu-id="6eb00-103">Deletes a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="6eb00-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6eb00-104">SYNTAX</span></span>

### <span data-ttu-id="6eb00-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6eb00-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBCassandraKeyspace -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6eb00-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6eb00-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBCassandraKeyspace -InputObject <PSCassandraKeyspaceGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6eb00-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6eb00-107">DESCRIPTION</span></span>
<span data-ttu-id="6eb00-108">Il cmdlet **Remove-AzCosmosDBCassandraKeyspace** elimina un keyspace esistente di CassandraDB.</span><span class="sxs-lookup"><span data-stu-id="6eb00-108">The **Remove-AzCosmosDBCassandraKeyspace** cmdlet deletes an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="6eb00-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6eb00-109">EXAMPLES</span></span>

### <span data-ttu-id="6eb00-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6eb00-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {keyspaceName}
```

<span data-ttu-id="6eb00-111">Il cmdlet restituisce un oggetto di tipo bool(when -PassThru is passed), che è true se l'eliminazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="6eb00-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true if the delete was successful.</span></span>

## <span data-ttu-id="6eb00-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6eb00-112">PARAMETERS</span></span>

### <span data-ttu-id="6eb00-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6eb00-113">-AccountName</span></span>
<span data-ttu-id="6eb00-114">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="6eb00-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="6eb00-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6eb00-115">-Confirm</span></span>
<span data-ttu-id="6eb00-116">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6eb00-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6eb00-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eb00-117">-DefaultProfile</span></span>
<span data-ttu-id="6eb00-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6eb00-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6eb00-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6eb00-119">-InputObject</span></span>
<span data-ttu-id="6eb00-120">Oggetto Cassandra Keyspace.</span><span class="sxs-lookup"><span data-stu-id="6eb00-120">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6eb00-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6eb00-121">-Name</span></span>
<span data-ttu-id="6eb00-122">Nome spazio tasti Cassandra.</span><span class="sxs-lookup"><span data-stu-id="6eb00-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="6eb00-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6eb00-123">-PassThru</span></span>
<span data-ttu-id="6eb00-124">Per essere impostato su true se l'utente vuole ricevere un output.</span><span class="sxs-lookup"><span data-stu-id="6eb00-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="6eb00-125">L'output è true se l'operazione è riuscita e in caso contrario viene generato un errore.</span><span class="sxs-lookup"><span data-stu-id="6eb00-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="6eb00-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6eb00-126">-ResourceGroupName</span></span>
<span data-ttu-id="6eb00-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6eb00-127">Name of resource group.</span></span>

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

### <span data-ttu-id="6eb00-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6eb00-128">-WhatIf</span></span>
<span data-ttu-id="6eb00-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6eb00-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6eb00-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6eb00-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6eb00-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eb00-131">CommonParameters</span></span>
<span data-ttu-id="6eb00-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6eb00-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eb00-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6eb00-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eb00-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="6eb00-134">INPUTS</span></span>

### <span data-ttu-id="6eb00-135">Microsoft.Azure.Commands.EnterpriseDb.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="6eb00-135">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="6eb00-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6eb00-136">OUTPUTS</span></span>

### <span data-ttu-id="6eb00-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="6eb00-137">System.Void</span></span>

### <span data-ttu-id="6eb00-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6eb00-138">System.Boolean</span></span>

## <span data-ttu-id="6eb00-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="6eb00-139">NOTES</span></span>

## <span data-ttu-id="6eb00-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6eb00-140">RELATED LINKS</span></span>
