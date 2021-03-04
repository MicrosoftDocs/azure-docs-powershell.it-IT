---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/remove-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraTable.md
ms.openlocfilehash: d860e9f5992cb1bd8df9a3f7f14e51565412284b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975902"
---
# <span data-ttu-id="63762-101">Remove-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="63762-101">Remove-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="63762-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63762-102">SYNOPSIS</span></span>
<span data-ttu-id="63762-103">Elimina una tabella CassandraDb.</span><span class="sxs-lookup"><span data-stu-id="63762-103">Deletes a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="63762-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="63762-104">SYNTAX</span></span>

### <span data-ttu-id="63762-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="63762-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="63762-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="63762-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBCassandraTable -InputObject <PSCassandraTableGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63762-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="63762-107">DESCRIPTION</span></span>
<span data-ttu-id="63762-108">La **tabella Remove-AzCosmosDBCassandraTable** elimina una tabellaDb Cassandra.</span><span class="sxs-lookup"><span data-stu-id="63762-108">The **Remove-AzCosmosDBCassandraTable** delete a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="63762-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="63762-109">EXAMPLES</span></span>

### <span data-ttu-id="63762-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="63762-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroup} -AccountName {account} -KeyspaceName {keyspace} -Name {tableName}
```

<span data-ttu-id="63762-111">Il cmdlet restituisce un oggetto di tipo bool(when -PassThru is passed), che è true se l'eliminazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="63762-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="63762-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="63762-112">PARAMETERS</span></span>

### <span data-ttu-id="63762-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="63762-113">-AccountName</span></span>
<span data-ttu-id="63762-114">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="63762-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="63762-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="63762-115">-Confirm</span></span>
<span data-ttu-id="63762-116">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63762-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63762-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63762-117">-DefaultProfile</span></span>
<span data-ttu-id="63762-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="63762-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63762-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63762-119">-InputObject</span></span>
<span data-ttu-id="63762-120">Oggetto Table di Cassandra.</span><span class="sxs-lookup"><span data-stu-id="63762-120">Cassandra Table object.</span></span>

```yaml
Type: PSCassandraTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63762-121">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="63762-121">-KeyspaceName</span></span>
<span data-ttu-id="63762-122">Nome spazio tasti Cassandra.</span><span class="sxs-lookup"><span data-stu-id="63762-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="63762-123">-Name</span><span class="sxs-lookup"><span data-stu-id="63762-123">-Name</span></span>
<span data-ttu-id="63762-124">Nome tabella Cassandra.</span><span class="sxs-lookup"><span data-stu-id="63762-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="63762-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="63762-125">-PassThru</span></span>
<span data-ttu-id="63762-126">Per essere impostato su true se l'utente vuole ricevere un output.</span><span class="sxs-lookup"><span data-stu-id="63762-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="63762-127">L'output è true se l'operazione è riuscita e in caso contrario viene generato un errore.</span><span class="sxs-lookup"><span data-stu-id="63762-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="63762-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63762-128">-ResourceGroupName</span></span>
<span data-ttu-id="63762-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="63762-129">Name of resource group.</span></span>

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

### <span data-ttu-id="63762-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63762-130">-WhatIf</span></span>
<span data-ttu-id="63762-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="63762-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63762-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="63762-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63762-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63762-133">CommonParameters</span></span>
<span data-ttu-id="63762-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63762-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63762-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="63762-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63762-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="63762-136">INPUTS</span></span>

### <span data-ttu-id="63762-137">Microsoft.Azure.Commands.EnterpriseDb.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="63762-137">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="63762-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="63762-138">OUTPUTS</span></span>

### <span data-ttu-id="63762-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="63762-139">System.Void</span></span>

### <span data-ttu-id="63762-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="63762-140">System.Boolean</span></span>

## <span data-ttu-id="63762-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="63762-141">NOTES</span></span>

## <span data-ttu-id="63762-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="63762-142">RELATED LINKS</span></span>
