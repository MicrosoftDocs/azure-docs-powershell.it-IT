---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/remove-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 849f716787c01c5810af74c37e97bbdb0bd2ef13
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954750"
---
# <span data-ttu-id="1446b-101">Remove-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="1446b-101">Remove-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="1446b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1446b-102">SYNOPSIS</span></span>
<span data-ttu-id="1446b-103">Elimina un oggetto Db Cassandra Keyspace.</span><span class="sxs-lookup"><span data-stu-id="1446b-103">Deletes a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="1446b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1446b-104">SYNTAX</span></span>

### <span data-ttu-id="1446b-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1446b-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBCassandraKeyspace -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1446b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1446b-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBCassandraKeyspace -InputObject <PSCassandraKeyspaceGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1446b-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1446b-107">DESCRIPTION</span></span>
<span data-ttu-id="1446b-108">Il cmdlet **Remove-AzCosmosDBCassandraKeyspace** elimina un keyspace Esistente di CassasDB Cassandra Keyspace.</span><span class="sxs-lookup"><span data-stu-id="1446b-108">The **Remove-AzCosmosDBCassandraKeyspace** cmdlet deletes an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="1446b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1446b-109">EXAMPLES</span></span>

### <span data-ttu-id="1446b-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1446b-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {keyspaceName}
```

<span data-ttu-id="1446b-111">Il cmdlet restituisce un oggetto di tipo bool(when -PassThru is passed), che è true se l'eliminazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="1446b-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true if the delete was successful.</span></span>

## <span data-ttu-id="1446b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1446b-112">PARAMETERS</span></span>

### <span data-ttu-id="1446b-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1446b-113">-AccountName</span></span>
<span data-ttu-id="1446b-114">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="1446b-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1446b-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1446b-115">-Confirm</span></span>
<span data-ttu-id="1446b-116">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1446b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1446b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1446b-117">-DefaultProfile</span></span>
<span data-ttu-id="1446b-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1446b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1446b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1446b-119">-InputObject</span></span>
<span data-ttu-id="1446b-120">Oggetto Cassandra Keyspace.</span><span class="sxs-lookup"><span data-stu-id="1446b-120">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="1446b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="1446b-121">-Name</span></span>
<span data-ttu-id="1446b-122">Nome spazio tasti Cassandra.</span><span class="sxs-lookup"><span data-stu-id="1446b-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="1446b-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1446b-123">-PassThru</span></span>
<span data-ttu-id="1446b-124">Per essere impostato su true se l'utente vuole ricevere un output.</span><span class="sxs-lookup"><span data-stu-id="1446b-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="1446b-125">L'output è true se l'operazione è riuscita e in caso contrario viene generato un errore.</span><span class="sxs-lookup"><span data-stu-id="1446b-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="1446b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1446b-126">-ResourceGroupName</span></span>
<span data-ttu-id="1446b-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1446b-127">Name of resource group.</span></span>

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

### <span data-ttu-id="1446b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1446b-128">-WhatIf</span></span>
<span data-ttu-id="1446b-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1446b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1446b-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1446b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1446b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1446b-131">CommonParameters</span></span>
<span data-ttu-id="1446b-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1446b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1446b-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1446b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1446b-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="1446b-134">INPUTS</span></span>

### <span data-ttu-id="1446b-135">Microsoft.Azure.Commands.CommonsDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="1446b-135">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="1446b-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1446b-136">OUTPUTS</span></span>

### <span data-ttu-id="1446b-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="1446b-137">System.Void</span></span>

### <span data-ttu-id="1446b-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1446b-138">System.Boolean</span></span>

## <span data-ttu-id="1446b-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="1446b-139">NOTES</span></span>

## <span data-ttu-id="1446b-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1446b-140">RELATED LINKS</span></span>
