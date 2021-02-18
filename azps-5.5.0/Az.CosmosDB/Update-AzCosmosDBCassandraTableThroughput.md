---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: f686a9923b8281029984a0fc84fcd5d51866256d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181295"
---
# <span data-ttu-id="aee45-101">Update-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="aee45-101">Update-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="aee45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aee45-102">SYNOPSIS</span></span>
<span data-ttu-id="aee45-103">Aggiorna il valore di velocità effettiva di una tabella CassandraDB.</span><span class="sxs-lookup"><span data-stu-id="aee45-103">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="aee45-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aee45-104">SYNTAX</span></span>

### <span data-ttu-id="aee45-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="aee45-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTableThroughput -KeyspaceName <String> [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aee45-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aee45-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -ParentObject <PSCassandraKeyspaceGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aee45-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aee45-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -InputObject <PSCassandraTableGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aee45-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="aee45-108">DESCRIPTION</span></span>
<span data-ttu-id="aee45-109">Aggiorna il valore di velocità effettiva di una tabella CassandraDB.</span><span class="sxs-lookup"><span data-stu-id="aee45-109">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="aee45-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aee45-110">EXAMPLES</span></span>

### <span data-ttu-id="aee45-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="aee45-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -KeyspaceName {myKeyspacename} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/tables/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="aee45-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aee45-112">PARAMETERS</span></span>

### <span data-ttu-id="aee45-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="aee45-113">-AccountName</span></span>
<span data-ttu-id="aee45-114">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="aee45-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="aee45-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="aee45-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="aee45-116">Valore massimo di velocità effettiva se è abilitata la scalabilità automatica.</span><span class="sxs-lookup"><span data-stu-id="aee45-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="aee45-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aee45-117">-Confirm</span></span>
<span data-ttu-id="aee45-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aee45-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aee45-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aee45-119">-DefaultProfile</span></span>
<span data-ttu-id="aee45-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aee45-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aee45-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aee45-121">-InputObject</span></span>
<span data-ttu-id="aee45-122">Oggetto Cassandra Keyspace.</span><span class="sxs-lookup"><span data-stu-id="aee45-122">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="aee45-123">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="aee45-123">-KeyspaceName</span></span>
<span data-ttu-id="aee45-124">Nome spazio tasti Cassandra.</span><span class="sxs-lookup"><span data-stu-id="aee45-124">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="aee45-125">-Name</span><span class="sxs-lookup"><span data-stu-id="aee45-125">-Name</span></span>
<span data-ttu-id="aee45-126">Nome tabella Cassandra.</span><span class="sxs-lookup"><span data-stu-id="aee45-126">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="aee45-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="aee45-127">-ParentObject</span></span>
<span data-ttu-id="aee45-128">Oggetto Cassandra Keyspace.</span><span class="sxs-lookup"><span data-stu-id="aee45-128">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="aee45-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aee45-129">-ResourceGroupName</span></span>
<span data-ttu-id="aee45-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="aee45-130">Name of resource group.</span></span>

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

### <span data-ttu-id="aee45-131">-Velocità effettiva</span><span class="sxs-lookup"><span data-stu-id="aee45-131">-Throughput</span></span>
<span data-ttu-id="aee45-132">Velocità effettiva di Cassandra Keyspace (RU/s).</span><span class="sxs-lookup"><span data-stu-id="aee45-132">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="aee45-133">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="aee45-133">Default value is 400.</span></span>

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

### <span data-ttu-id="aee45-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aee45-134">-WhatIf</span></span>
<span data-ttu-id="aee45-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aee45-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aee45-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aee45-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aee45-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aee45-137">CommonParameters</span></span>
<span data-ttu-id="aee45-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aee45-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aee45-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="aee45-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aee45-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="aee45-140">INPUTS</span></span>

### <span data-ttu-id="aee45-141">Microsoft.Azure.Commands.EnterpriseDb.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="aee45-141">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="aee45-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aee45-142">OUTPUTS</span></span>

### <span data-ttu-id="aee45-143">Microsoft.Azure.Commands.EnterpriseDb.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="aee45-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="aee45-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="aee45-144">NOTES</span></span>

## <span data-ttu-id="aee45-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aee45-145">RELATED LINKS</span></span>
