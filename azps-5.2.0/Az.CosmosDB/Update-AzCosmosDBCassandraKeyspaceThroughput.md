---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandrakeyspacethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspaceThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspaceThroughput.md
ms.openlocfilehash: 43dcbd97047ef72104a3b000f760b49aa3dfaab6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344647"
---
# <span data-ttu-id="6ca47-101">Update-AzCosmosDBCassandraKeyspaceThroughput</span><span class="sxs-lookup"><span data-stu-id="6ca47-101">Update-AzCosmosDBCassandraKeyspaceThroughput</span></span>

## <span data-ttu-id="6ca47-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6ca47-102">SYNOPSIS</span></span>
<span data-ttu-id="6ca47-103">Aggiorna il valore di throughput di un CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="6ca47-103">Updates the throughput value of a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="6ca47-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6ca47-104">SYNTAX</span></span>

### <span data-ttu-id="6ca47-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6ca47-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ca47-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ca47-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ca47-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ca47-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -InputObject <PSCassandraKeyspaceGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ca47-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6ca47-108">DESCRIPTION</span></span>
<span data-ttu-id="6ca47-109">Aggiorna il valore di throughput di un CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="6ca47-109">Updates the throughput value of a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="6ca47-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6ca47-110">EXAMPLES</span></span>

### <span data-ttu-id="6ca47-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6ca47-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraKeyspaceThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myKeyspaceName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="6ca47-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6ca47-112">PARAMETERS</span></span>

### <span data-ttu-id="6ca47-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6ca47-113">-AccountName</span></span>
<span data-ttu-id="6ca47-114">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="6ca47-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="6ca47-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="6ca47-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="6ca47-116">Valore massimo della velocità effettiva se autoscale è abilitato.</span><span class="sxs-lookup"><span data-stu-id="6ca47-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="6ca47-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6ca47-117">-Confirm</span></span>
<span data-ttu-id="6ca47-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ca47-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ca47-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ca47-119">-DefaultProfile</span></span>
<span data-ttu-id="6ca47-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6ca47-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ca47-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ca47-121">-InputObject</span></span>
<span data-ttu-id="6ca47-122">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="6ca47-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="6ca47-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="6ca47-123">-Name</span></span>
<span data-ttu-id="6ca47-124">Nome della barra spaziatrice Cassandra.</span><span class="sxs-lookup"><span data-stu-id="6ca47-124">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="6ca47-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6ca47-125">-ParentObject</span></span>
<span data-ttu-id="6ca47-126">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="6ca47-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="6ca47-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ca47-127">-ResourceGroupName</span></span>
<span data-ttu-id="6ca47-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6ca47-128">Name of resource group.</span></span>

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

### <span data-ttu-id="6ca47-129">-Throughput</span><span class="sxs-lookup"><span data-stu-id="6ca47-129">-Throughput</span></span>
<span data-ttu-id="6ca47-130">La velocità effettiva di Cassandra della barra spaziatrice (RU/s).</span><span class="sxs-lookup"><span data-stu-id="6ca47-130">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="6ca47-131">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="6ca47-131">Default value is 400.</span></span>

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

### <span data-ttu-id="6ca47-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ca47-132">-WhatIf</span></span>
<span data-ttu-id="6ca47-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6ca47-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ca47-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6ca47-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ca47-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ca47-135">CommonParameters</span></span>
<span data-ttu-id="6ca47-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ca47-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ca47-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6ca47-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ca47-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6ca47-138">INPUTS</span></span>

### <span data-ttu-id="6ca47-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="6ca47-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="6ca47-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6ca47-140">OUTPUTS</span></span>

### <span data-ttu-id="6ca47-141">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="6ca47-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="6ca47-142">Note</span><span class="sxs-lookup"><span data-stu-id="6ca47-142">NOTES</span></span>

## <span data-ttu-id="6ca47-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6ca47-143">RELATED LINKS</span></span>
