---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: 9c3aff7edb26863f2843ef517c7ce0f08f91296f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022381"
---
# <span data-ttu-id="362e5-101">Update-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="362e5-101">Update-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="362e5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="362e5-102">SYNOPSIS</span></span>
<span data-ttu-id="362e5-103">Aggiorna il valore della velocità effettiva di una tabella di CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="362e5-103">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="362e5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="362e5-104">SYNTAX</span></span>

### <span data-ttu-id="362e5-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="362e5-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTableThroughput -ResourceGroupName <String> -AccountName <String>
 -KeyspaceName <String> [-Name <String>] -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="362e5-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="362e5-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="362e5-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="362e5-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSCassandraTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="362e5-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="362e5-108">EXAMPLES</span></span>

### <span data-ttu-id="362e5-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="362e5-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -KeyspaceName {myKeyspacename} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/tables/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="362e5-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="362e5-110">PARAMETERS</span></span>

### <span data-ttu-id="362e5-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="362e5-111">-AccountName</span></span>
<span data-ttu-id="362e5-112">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="362e5-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="362e5-113">-Confermare</span><span class="sxs-lookup"><span data-stu-id="362e5-113">-Confirm</span></span>
<span data-ttu-id="362e5-114">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="362e5-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="362e5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="362e5-115">-DefaultProfile</span></span>
<span data-ttu-id="362e5-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="362e5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="362e5-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="362e5-117">-InputObject</span></span>
<span data-ttu-id="362e5-118">Oggetto portaspazio Cassandra.</span><span class="sxs-lookup"><span data-stu-id="362e5-118">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="362e5-119">-Barra spaziatrice</span><span class="sxs-lookup"><span data-stu-id="362e5-119">-KeyspaceName</span></span>
<span data-ttu-id="362e5-120">Nome della barra spaziatrice Cassandra.</span><span class="sxs-lookup"><span data-stu-id="362e5-120">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="362e5-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="362e5-121">-Name</span></span>
<span data-ttu-id="362e5-122">Nome tabella Cassandra.</span><span class="sxs-lookup"><span data-stu-id="362e5-122">Cassandra Table Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="362e5-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="362e5-123">-ParentObject</span></span>
<span data-ttu-id="362e5-124">Oggetto portaspazio Cassandra.</span><span class="sxs-lookup"><span data-stu-id="362e5-124">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="362e5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="362e5-125">-ResourceGroupName</span></span>
<span data-ttu-id="362e5-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="362e5-126">Name of resource group.</span></span>

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

### <span data-ttu-id="362e5-127">-Throughput</span><span class="sxs-lookup"><span data-stu-id="362e5-127">-Throughput</span></span>
<span data-ttu-id="362e5-128">La velocità effettiva di Cassandra della barra spaziatrice (RU/s).</span><span class="sxs-lookup"><span data-stu-id="362e5-128">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="362e5-129">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="362e5-129">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="362e5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="362e5-130">-WhatIf</span></span>
<span data-ttu-id="362e5-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="362e5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="362e5-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="362e5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="362e5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="362e5-133">CommonParameters</span></span>
<span data-ttu-id="362e5-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="362e5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="362e5-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="362e5-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="362e5-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="362e5-136">INPUTS</span></span>

### <span data-ttu-id="362e5-137">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="362e5-137">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="362e5-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="362e5-138">OUTPUTS</span></span>

### <span data-ttu-id="362e5-139">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="362e5-139">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="362e5-140">Note</span><span class="sxs-lookup"><span data-stu-id="362e5-140">NOTES</span></span>

## <span data-ttu-id="362e5-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="362e5-141">RELATED LINKS</span></span>
