---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandrakeyspacethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspaceThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspaceThroughput.md
ms.openlocfilehash: 43dcbd97047ef72104a3b000f760b49aa3dfaab6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192569"
---
# <span data-ttu-id="d3d00-101">Update-AzCosmosDBCassandraKeyspaceThroughput</span><span class="sxs-lookup"><span data-stu-id="d3d00-101">Update-AzCosmosDBCassandraKeyspaceThroughput</span></span>

## <span data-ttu-id="d3d00-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d3d00-102">SYNOPSIS</span></span>
<span data-ttu-id="d3d00-103">Aggiorna il valore di throughput di un CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="d3d00-103">Updates the throughput value of a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="d3d00-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3d00-104">SYNTAX</span></span>

### <span data-ttu-id="d3d00-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d3d00-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3d00-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3d00-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3d00-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3d00-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -InputObject <PSCassandraKeyspaceGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3d00-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3d00-108">DESCRIPTION</span></span>
<span data-ttu-id="d3d00-109">Aggiorna il valore di throughput di un CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="d3d00-109">Updates the throughput value of a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="d3d00-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3d00-110">EXAMPLES</span></span>

### <span data-ttu-id="d3d00-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d3d00-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraKeyspaceThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myKeyspaceName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="d3d00-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d3d00-112">PARAMETERS</span></span>

### <span data-ttu-id="d3d00-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d3d00-113">-AccountName</span></span>
<span data-ttu-id="d3d00-114">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="d3d00-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d3d00-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="d3d00-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="d3d00-116">Valore massimo della velocità effettiva se autoscale è abilitato.</span><span class="sxs-lookup"><span data-stu-id="d3d00-116">Maximum Throughput value if autoscale is enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3d00-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d3d00-117">-Confirm</span></span>
<span data-ttu-id="d3d00-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3d00-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3d00-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3d00-119">-DefaultProfile</span></span>
<span data-ttu-id="d3d00-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d3d00-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3d00-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3d00-121">-InputObject</span></span>
<span data-ttu-id="d3d00-122">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="d3d00-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="d3d00-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="d3d00-123">-Name</span></span>
<span data-ttu-id="d3d00-124">Nome della barra spaziatrice Cassandra.</span><span class="sxs-lookup"><span data-stu-id="d3d00-124">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="d3d00-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d3d00-125">-ParentObject</span></span>
<span data-ttu-id="d3d00-126">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="d3d00-126">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3d00-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3d00-127">-ResourceGroupName</span></span>
<span data-ttu-id="d3d00-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d3d00-128">Name of resource group.</span></span>

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

### <span data-ttu-id="d3d00-129">-Throughput</span><span class="sxs-lookup"><span data-stu-id="d3d00-129">-Throughput</span></span>
<span data-ttu-id="d3d00-130">La velocità effettiva di Cassandra della barra spaziatrice (RU/s).</span><span class="sxs-lookup"><span data-stu-id="d3d00-130">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="d3d00-131">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="d3d00-131">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3d00-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3d00-132">-WhatIf</span></span>
<span data-ttu-id="d3d00-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3d00-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3d00-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3d00-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3d00-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3d00-135">CommonParameters</span></span>
<span data-ttu-id="d3d00-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3d00-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3d00-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3d00-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3d00-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d3d00-138">INPUTS</span></span>

### <span data-ttu-id="d3d00-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="d3d00-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="d3d00-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3d00-140">OUTPUTS</span></span>

### <span data-ttu-id="d3d00-141">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="d3d00-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="d3d00-142">Note</span><span class="sxs-lookup"><span data-stu-id="d3d00-142">NOTES</span></span>

## <span data-ttu-id="d3d00-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3d00-143">RELATED LINKS</span></span>
