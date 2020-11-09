---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 7e176ebe2185f2a8c049155e04197b333fabd83c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299172"
---
# <span data-ttu-id="475ce-101">Remove-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="475ce-101">Remove-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="475ce-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="475ce-102">SYNOPSIS</span></span>
<span data-ttu-id="475ce-103">Elimina una tabella di CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="475ce-103">Deletes a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="475ce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="475ce-104">SYNTAX</span></span>

### <span data-ttu-id="475ce-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="475ce-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="475ce-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="475ce-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBCassandraTable -InputObject <PSCassandraTableGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="475ce-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="475ce-107">DESCRIPTION</span></span>
<span data-ttu-id="475ce-108">**Remove-AzCosmosDBCassandraTable** Elimina una tabella CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="475ce-108">The **Remove-AzCosmosDBCassandraTable** delete a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="475ce-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="475ce-109">EXAMPLES</span></span>

### <span data-ttu-id="475ce-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="475ce-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroup} -AccountName {account} -KeyspaceName {keyspace} -Name {tableName}
```

<span data-ttu-id="475ce-111">Il cmdlet restituisce un oggetto di tipo bool (quando viene passato-PassThru), che è true, se l'eliminazione è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="475ce-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="475ce-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="475ce-112">PARAMETERS</span></span>

### <span data-ttu-id="475ce-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="475ce-113">-AccountName</span></span>
<span data-ttu-id="475ce-114">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="475ce-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="475ce-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="475ce-115">-Confirm</span></span>
<span data-ttu-id="475ce-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="475ce-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="475ce-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="475ce-117">-DefaultProfile</span></span>
<span data-ttu-id="475ce-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="475ce-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="475ce-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="475ce-119">-InputObject</span></span>
<span data-ttu-id="475ce-120">Oggetto tabella Cassandra.</span><span class="sxs-lookup"><span data-stu-id="475ce-120">Cassandra Table object.</span></span>

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

### <span data-ttu-id="475ce-121">-Barra spaziatrice</span><span class="sxs-lookup"><span data-stu-id="475ce-121">-KeyspaceName</span></span>
<span data-ttu-id="475ce-122">Nome della barra spaziatrice Cassandra.</span><span class="sxs-lookup"><span data-stu-id="475ce-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="475ce-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="475ce-123">-Name</span></span>
<span data-ttu-id="475ce-124">Nome tabella Cassandra.</span><span class="sxs-lookup"><span data-stu-id="475ce-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="475ce-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="475ce-125">-PassThru</span></span>
<span data-ttu-id="475ce-126">Da impostare su true se l'utente vuole ricevere un output.</span><span class="sxs-lookup"><span data-stu-id="475ce-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="475ce-127">L'output è true se l'operazione è stata eseguita correttamente e se non viene generato un errore.</span><span class="sxs-lookup"><span data-stu-id="475ce-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="475ce-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="475ce-128">-ResourceGroupName</span></span>
<span data-ttu-id="475ce-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="475ce-129">Name of resource group.</span></span>

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

### <span data-ttu-id="475ce-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="475ce-130">-WhatIf</span></span>
<span data-ttu-id="475ce-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="475ce-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="475ce-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="475ce-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="475ce-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="475ce-133">CommonParameters</span></span>
<span data-ttu-id="475ce-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="475ce-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="475ce-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="475ce-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="475ce-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="475ce-136">INPUTS</span></span>

### <span data-ttu-id="475ce-137">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="475ce-137">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="475ce-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="475ce-138">OUTPUTS</span></span>

### <span data-ttu-id="475ce-139">System. void</span><span class="sxs-lookup"><span data-stu-id="475ce-139">System.Void</span></span>

### <span data-ttu-id="475ce-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="475ce-140">System.Boolean</span></span>

## <span data-ttu-id="475ce-141">Note</span><span class="sxs-lookup"><span data-stu-id="475ce-141">NOTES</span></span>

## <span data-ttu-id="475ce-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="475ce-142">RELATED LINKS</span></span>
