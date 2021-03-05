---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 4a9a5595345b44eaf3a3b44d9d9ba1d8895a6376
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977453"
---
# <span data-ttu-id="b33c3-101">Update-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="b33c3-101">Update-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="b33c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b33c3-102">SYNOPSIS</span></span>
<span data-ttu-id="b33c3-103">Aggiorna lo spazio dei dati del database Cassandra Keyspace.</span><span class="sxs-lookup"><span data-stu-id="b33c3-103">Updates the CosmosDB Cassandra Keyspace.</span></span> <span data-ttu-id="b33c3-104">Esegue un'operazione di patch sul lato client leggendo il tasto Keyspace esistente.</span><span class="sxs-lookup"><span data-stu-id="b33c3-104">Performs a client side patch operation by reading the existing Keyspace.</span></span>

## <span data-ttu-id="b33c3-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b33c3-105">SYNTAX</span></span>

### <span data-ttu-id="b33c3-106">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b33c3-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b33c3-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b33c3-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspace [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b33c3-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b33c3-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspace [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b33c3-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b33c3-109">DESCRIPTION</span></span>
<span data-ttu-id="b33c3-110">Aggiorna lo spazio dei dati del database Cassandra Keyspace.</span><span class="sxs-lookup"><span data-stu-id="b33c3-110">Updates the CosmosDB Cassandra Keyspace.</span></span> <span data-ttu-id="b33c3-111">Esegue un'operazione di patch sul lato client leggendo il tasto Keyspace esistente.</span><span class="sxs-lookup"><span data-stu-id="b33c3-111">Performs a client side patch operation by reading the existing Keyspace.</span></span>

## <span data-ttu-id="b33c3-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b33c3-112">EXAMPLES</span></span>

### <span data-ttu-id="b33c3-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b33c3-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput 600

Name     : myKeyspace
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetPropertiesResource
```

## <span data-ttu-id="b33c3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b33c3-114">PARAMETERS</span></span>

### <span data-ttu-id="b33c3-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b33c3-115">-AccountName</span></span>
<span data-ttu-id="b33c3-116">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="b33c3-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b33c3-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="b33c3-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="b33c3-118">Valore massimo di velocità effettiva se è abilitata la scalabilità automatica.</span><span class="sxs-lookup"><span data-stu-id="b33c3-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="b33c3-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b33c3-119">-Confirm</span></span>
<span data-ttu-id="b33c3-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b33c3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b33c3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b33c3-121">-DefaultProfile</span></span>
<span data-ttu-id="b33c3-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b33c3-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b33c3-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b33c3-123">-InputObject</span></span>
<span data-ttu-id="b33c3-124">Oggetto Cassandra Keyspace.</span><span class="sxs-lookup"><span data-stu-id="b33c3-124">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="b33c3-125">-Name</span><span class="sxs-lookup"><span data-stu-id="b33c3-125">-Name</span></span>
<span data-ttu-id="b33c3-126">Nome spazio tasti Cassandra.</span><span class="sxs-lookup"><span data-stu-id="b33c3-126">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="b33c3-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b33c3-127">-ParentObject</span></span>
<span data-ttu-id="b33c3-128">Oggetto Account Aziendale</span><span class="sxs-lookup"><span data-stu-id="b33c3-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="b33c3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b33c3-129">-ResourceGroupName</span></span>
<span data-ttu-id="b33c3-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b33c3-130">Name of resource group.</span></span>

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

### <span data-ttu-id="b33c3-131">-Velocità effettiva</span><span class="sxs-lookup"><span data-stu-id="b33c3-131">-Throughput</span></span>
<span data-ttu-id="b33c3-132">Velocità effettiva di Cassandra Keyspace (RU/s).</span><span class="sxs-lookup"><span data-stu-id="b33c3-132">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="b33c3-133">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="b33c3-133">Default value is 400.</span></span>

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

### <span data-ttu-id="b33c3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b33c3-134">-WhatIf</span></span>
<span data-ttu-id="b33c3-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b33c3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b33c3-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b33c3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b33c3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b33c3-137">CommonParameters</span></span>
<span data-ttu-id="b33c3-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b33c3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b33c3-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b33c3-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b33c3-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="b33c3-140">INPUTS</span></span>

### <span data-ttu-id="b33c3-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="b33c3-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="b33c3-142">Microsoft.Azure.Commands.CommonsDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="b33c3-142">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="b33c3-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b33c3-143">OUTPUTS</span></span>

### <span data-ttu-id="b33c3-144">Microsoft.Azure.Commands.CommonsDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="b33c3-144">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="b33c3-145">Microsoft.Azure.Commands.ExceptionsDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="b33c3-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="b33c3-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="b33c3-146">NOTES</span></span>

## <span data-ttu-id="b33c3-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b33c3-147">RELATED LINKS</span></span>
