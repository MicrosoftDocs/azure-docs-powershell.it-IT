---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: f686a9923b8281029984a0fc84fcd5d51866256d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192149"
---
# <span data-ttu-id="44fed-101">Update-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="44fed-101">Update-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="44fed-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="44fed-102">SYNOPSIS</span></span>
<span data-ttu-id="44fed-103">Aggiorna il valore della velocità effettiva di una tabella di CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="44fed-103">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="44fed-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="44fed-104">SYNTAX</span></span>

### <span data-ttu-id="44fed-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="44fed-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTableThroughput -KeyspaceName <String> [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44fed-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="44fed-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -ParentObject <PSCassandraKeyspaceGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44fed-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="44fed-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -InputObject <PSCassandraTableGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44fed-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="44fed-108">DESCRIPTION</span></span>
<span data-ttu-id="44fed-109">Aggiorna il valore della velocità effettiva di una tabella di CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="44fed-109">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="44fed-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="44fed-110">EXAMPLES</span></span>

### <span data-ttu-id="44fed-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="44fed-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -KeyspaceName {myKeyspacename} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/tables/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="44fed-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="44fed-112">PARAMETERS</span></span>

### <span data-ttu-id="44fed-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="44fed-113">-AccountName</span></span>
<span data-ttu-id="44fed-114">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="44fed-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="44fed-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="44fed-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="44fed-116">Valore massimo della velocità effettiva se autoscale è abilitato.</span><span class="sxs-lookup"><span data-stu-id="44fed-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="44fed-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="44fed-117">-Confirm</span></span>
<span data-ttu-id="44fed-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44fed-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44fed-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44fed-119">-DefaultProfile</span></span>
<span data-ttu-id="44fed-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="44fed-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44fed-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44fed-121">-InputObject</span></span>
<span data-ttu-id="44fed-122">Oggetto portaspazio Cassandra.</span><span class="sxs-lookup"><span data-stu-id="44fed-122">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="44fed-123">-Barra spaziatrice</span><span class="sxs-lookup"><span data-stu-id="44fed-123">-KeyspaceName</span></span>
<span data-ttu-id="44fed-124">Nome della barra spaziatrice Cassandra.</span><span class="sxs-lookup"><span data-stu-id="44fed-124">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="44fed-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="44fed-125">-Name</span></span>
<span data-ttu-id="44fed-126">Nome tabella Cassandra.</span><span class="sxs-lookup"><span data-stu-id="44fed-126">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="44fed-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="44fed-127">-ParentObject</span></span>
<span data-ttu-id="44fed-128">Oggetto portaspazio Cassandra.</span><span class="sxs-lookup"><span data-stu-id="44fed-128">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="44fed-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44fed-129">-ResourceGroupName</span></span>
<span data-ttu-id="44fed-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="44fed-130">Name of resource group.</span></span>

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

### <span data-ttu-id="44fed-131">-Throughput</span><span class="sxs-lookup"><span data-stu-id="44fed-131">-Throughput</span></span>
<span data-ttu-id="44fed-132">La velocità effettiva di Cassandra della barra spaziatrice (RU/s).</span><span class="sxs-lookup"><span data-stu-id="44fed-132">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="44fed-133">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="44fed-133">Default value is 400.</span></span>

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

### <span data-ttu-id="44fed-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44fed-134">-WhatIf</span></span>
<span data-ttu-id="44fed-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="44fed-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44fed-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="44fed-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44fed-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44fed-137">CommonParameters</span></span>
<span data-ttu-id="44fed-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44fed-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44fed-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44fed-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44fed-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="44fed-140">INPUTS</span></span>

### <span data-ttu-id="44fed-141">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="44fed-141">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="44fed-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="44fed-142">OUTPUTS</span></span>

### <span data-ttu-id="44fed-143">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="44fed-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="44fed-144">Note</span><span class="sxs-lookup"><span data-stu-id="44fed-144">NOTES</span></span>

## <span data-ttu-id="44fed-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="44fed-145">RELATED LINKS</span></span>
