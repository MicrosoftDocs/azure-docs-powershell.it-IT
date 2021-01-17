---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 7e176ebe2185f2a8c049155e04197b333fabd83c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350512"
---
# <span data-ttu-id="2b268-101">Remove-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="2b268-101">Remove-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="2b268-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2b268-102">SYNOPSIS</span></span>
<span data-ttu-id="2b268-103">Elimina una tabella di CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="2b268-103">Deletes a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="2b268-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2b268-104">SYNTAX</span></span>

### <span data-ttu-id="2b268-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2b268-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2b268-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b268-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBCassandraTable -InputObject <PSCassandraTableGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b268-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b268-107">DESCRIPTION</span></span>
<span data-ttu-id="2b268-108">**Remove-AzCosmosDBCassandraTable** Elimina una tabella CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="2b268-108">The **Remove-AzCosmosDBCassandraTable** delete a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="2b268-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2b268-109">EXAMPLES</span></span>

### <span data-ttu-id="2b268-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2b268-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroup} -AccountName {account} -KeyspaceName {keyspace} -Name {tableName}
```

<span data-ttu-id="2b268-111">Il cmdlet restituisce un oggetto di tipo bool (quando viene passato-PassThru), che è true, se l'eliminazione è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="2b268-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="2b268-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2b268-112">PARAMETERS</span></span>

### <span data-ttu-id="2b268-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2b268-113">-AccountName</span></span>
<span data-ttu-id="2b268-114">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="2b268-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2b268-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2b268-115">-Confirm</span></span>
<span data-ttu-id="2b268-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b268-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b268-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b268-117">-DefaultProfile</span></span>
<span data-ttu-id="2b268-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2b268-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b268-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b268-119">-InputObject</span></span>
<span data-ttu-id="2b268-120">Oggetto tabella Cassandra.</span><span class="sxs-lookup"><span data-stu-id="2b268-120">Cassandra Table object.</span></span>

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

### <span data-ttu-id="2b268-121">-Barra spaziatrice</span><span class="sxs-lookup"><span data-stu-id="2b268-121">-KeyspaceName</span></span>
<span data-ttu-id="2b268-122">Nome della barra spaziatrice Cassandra.</span><span class="sxs-lookup"><span data-stu-id="2b268-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="2b268-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="2b268-123">-Name</span></span>
<span data-ttu-id="2b268-124">Nome tabella Cassandra.</span><span class="sxs-lookup"><span data-stu-id="2b268-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="2b268-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2b268-125">-PassThru</span></span>
<span data-ttu-id="2b268-126">Da impostare su true se l'utente vuole ricevere un output.</span><span class="sxs-lookup"><span data-stu-id="2b268-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="2b268-127">L'output è true se l'operazione è stata eseguita correttamente e se non viene generato un errore.</span><span class="sxs-lookup"><span data-stu-id="2b268-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="2b268-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b268-128">-ResourceGroupName</span></span>
<span data-ttu-id="2b268-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2b268-129">Name of resource group.</span></span>

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

### <span data-ttu-id="2b268-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b268-130">-WhatIf</span></span>
<span data-ttu-id="2b268-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2b268-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b268-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2b268-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b268-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b268-133">CommonParameters</span></span>
<span data-ttu-id="2b268-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b268-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b268-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2b268-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b268-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2b268-136">INPUTS</span></span>

### <span data-ttu-id="2b268-137">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="2b268-137">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="2b268-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2b268-138">OUTPUTS</span></span>

### <span data-ttu-id="2b268-139">System. void</span><span class="sxs-lookup"><span data-stu-id="2b268-139">System.Void</span></span>

### <span data-ttu-id="2b268-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2b268-140">System.Boolean</span></span>

## <span data-ttu-id="2b268-141">Note</span><span class="sxs-lookup"><span data-stu-id="2b268-141">NOTES</span></span>

## <span data-ttu-id="2b268-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2b268-142">RELATED LINKS</span></span>
