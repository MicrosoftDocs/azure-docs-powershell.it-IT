---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: 989035c1478228eb8895a2f99779129c605b2f36
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977421"
---
# <span data-ttu-id="79674-101">Update-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="79674-101">Update-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="79674-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79674-102">SYNOPSIS</span></span>
<span data-ttu-id="79674-103">Aggiorna il valore di velocità effettiva di una tabella CassandraDB.</span><span class="sxs-lookup"><span data-stu-id="79674-103">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="79674-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="79674-104">SYNTAX</span></span>

### <span data-ttu-id="79674-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="79674-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTableThroughput -KeyspaceName <String> [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79674-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="79674-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -ParentObject <PSCassandraKeyspaceGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79674-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="79674-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -InputObject <PSCassandraTableGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79674-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="79674-108">DESCRIPTION</span></span>
<span data-ttu-id="79674-109">Aggiorna il valore di velocità effettiva di una tabella CassandraDB.</span><span class="sxs-lookup"><span data-stu-id="79674-109">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="79674-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="79674-110">EXAMPLES</span></span>

### <span data-ttu-id="79674-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="79674-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -KeyspaceName {myKeyspacename} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/tables/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="79674-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79674-112">PARAMETERS</span></span>

### <span data-ttu-id="79674-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="79674-113">-AccountName</span></span>
<span data-ttu-id="79674-114">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="79674-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="79674-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="79674-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="79674-116">Valore massimo di velocità effettiva se è abilitata la scalabilità automatica.</span><span class="sxs-lookup"><span data-stu-id="79674-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="79674-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79674-117">-Confirm</span></span>
<span data-ttu-id="79674-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79674-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79674-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79674-119">-DefaultProfile</span></span>
<span data-ttu-id="79674-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="79674-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79674-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="79674-121">-InputObject</span></span>
<span data-ttu-id="79674-122">Oggetto Cassandra Keyspace.</span><span class="sxs-lookup"><span data-stu-id="79674-122">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="79674-123">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="79674-123">-KeyspaceName</span></span>
<span data-ttu-id="79674-124">Nome spazio tasti Cassandra.</span><span class="sxs-lookup"><span data-stu-id="79674-124">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="79674-125">-Name</span><span class="sxs-lookup"><span data-stu-id="79674-125">-Name</span></span>
<span data-ttu-id="79674-126">Nome tabella Cassandra.</span><span class="sxs-lookup"><span data-stu-id="79674-126">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="79674-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="79674-127">-ParentObject</span></span>
<span data-ttu-id="79674-128">Oggetto Cassandra Keyspace.</span><span class="sxs-lookup"><span data-stu-id="79674-128">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="79674-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79674-129">-ResourceGroupName</span></span>
<span data-ttu-id="79674-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="79674-130">Name of resource group.</span></span>

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

### <span data-ttu-id="79674-131">-Velocità effettiva</span><span class="sxs-lookup"><span data-stu-id="79674-131">-Throughput</span></span>
<span data-ttu-id="79674-132">Velocità effettiva di Cassandra Keyspace (RU/s).</span><span class="sxs-lookup"><span data-stu-id="79674-132">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="79674-133">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="79674-133">Default value is 400.</span></span>

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

### <span data-ttu-id="79674-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79674-134">-WhatIf</span></span>
<span data-ttu-id="79674-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="79674-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79674-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="79674-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79674-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79674-137">CommonParameters</span></span>
<span data-ttu-id="79674-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79674-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79674-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="79674-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79674-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="79674-140">INPUTS</span></span>

### <span data-ttu-id="79674-141">Microsoft.Azure.Commands.CommonsDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="79674-141">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="79674-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="79674-142">OUTPUTS</span></span>

### <span data-ttu-id="79674-143">Microsoft.Azure.Commands.EnterpriseDb.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="79674-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="79674-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="79674-144">NOTES</span></span>

## <span data-ttu-id="79674-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="79674-145">RELATED LINKS</span></span>
