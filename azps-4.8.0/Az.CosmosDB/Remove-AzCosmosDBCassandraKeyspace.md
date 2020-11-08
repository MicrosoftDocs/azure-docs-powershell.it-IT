---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 7f6cae6a3187bf4393ea4fb592123c1833a18ebb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033197"
---
# <span data-ttu-id="38259-101">Remove-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="38259-101">Remove-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="38259-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="38259-102">SYNOPSIS</span></span>
<span data-ttu-id="38259-103">Elimina uno spazio di CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="38259-103">Deletes a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="38259-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="38259-104">SYNTAX</span></span>

### <span data-ttu-id="38259-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="38259-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBCassandraKeyspace -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38259-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="38259-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBCassandraKeyspace -InputObject <PSCassandraKeyspaceGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38259-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="38259-107">DESCRIPTION</span></span>
<span data-ttu-id="38259-108">Il cmdlet **Remove-AzCosmosDBCassandraKeyspace** Elimina uno spazio delle CosmosDB Cassandra esistente.</span><span class="sxs-lookup"><span data-stu-id="38259-108">The **Remove-AzCosmosDBCassandraKeyspace** cmdlet deletes an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="38259-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="38259-109">EXAMPLES</span></span>

### <span data-ttu-id="38259-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="38259-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {keyspaceName}
```

<span data-ttu-id="38259-111">Il cmdlet restituisce un oggetto di tipo bool (quando viene passato-PassThru), che è true se l'eliminazione ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="38259-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true if the delete was successful.</span></span>

## <span data-ttu-id="38259-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="38259-112">PARAMETERS</span></span>

### <span data-ttu-id="38259-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="38259-113">-AccountName</span></span>
<span data-ttu-id="38259-114">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="38259-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="38259-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="38259-115">-Confirm</span></span>
<span data-ttu-id="38259-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38259-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38259-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38259-117">-DefaultProfile</span></span>
<span data-ttu-id="38259-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="38259-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38259-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38259-119">-InputObject</span></span>
<span data-ttu-id="38259-120">Oggetto portaspazio Cassandra.</span><span class="sxs-lookup"><span data-stu-id="38259-120">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="38259-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="38259-121">-Name</span></span>
<span data-ttu-id="38259-122">Nome della barra spaziatrice Cassandra.</span><span class="sxs-lookup"><span data-stu-id="38259-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="38259-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="38259-123">-PassThru</span></span>
<span data-ttu-id="38259-124">Da impostare su true se l'utente vuole ricevere un output.</span><span class="sxs-lookup"><span data-stu-id="38259-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="38259-125">L'output è true se l'operazione è stata eseguita correttamente e se non viene generato un errore.</span><span class="sxs-lookup"><span data-stu-id="38259-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="38259-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38259-126">-ResourceGroupName</span></span>
<span data-ttu-id="38259-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="38259-127">Name of resource group.</span></span>

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

### <span data-ttu-id="38259-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38259-128">-WhatIf</span></span>
<span data-ttu-id="38259-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38259-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38259-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38259-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38259-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38259-131">CommonParameters</span></span>
<span data-ttu-id="38259-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38259-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38259-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38259-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38259-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="38259-134">INPUTS</span></span>

### <span data-ttu-id="38259-135">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="38259-135">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="38259-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="38259-136">OUTPUTS</span></span>

### <span data-ttu-id="38259-137">System. void</span><span class="sxs-lookup"><span data-stu-id="38259-137">System.Void</span></span>

### <span data-ttu-id="38259-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="38259-138">System.Boolean</span></span>

## <span data-ttu-id="38259-139">Note</span><span class="sxs-lookup"><span data-stu-id="38259-139">NOTES</span></span>

## <span data-ttu-id="38259-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="38259-140">RELATED LINKS</span></span>
