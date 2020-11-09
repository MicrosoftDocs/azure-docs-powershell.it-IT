---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 42ec4db0f9c0967e375cc30a582c35aaca65840f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299370"
---
# <span data-ttu-id="5072a-101">New-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="5072a-101">New-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="5072a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5072a-102">SYNOPSIS</span></span>
<span data-ttu-id="5072a-103">Crea una nuova tabella di CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="5072a-103">Creates a new CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="5072a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5072a-104">SYNTAX</span></span>

### <span data-ttu-id="5072a-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5072a-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-AnalyticalStorageTtl <Int32>] -Schema <PSCassandraSchema> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5072a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5072a-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBCassandraTable -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] -Schema <PSCassandraSchema>
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5072a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5072a-107">DESCRIPTION</span></span>
<span data-ttu-id="5072a-108">Crea una nuova tabella di CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="5072a-108">Creates a new CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="5072a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5072a-109">EXAMPLES</span></span>

### <span data-ttu-id="5072a-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5072a-110">Example 1</span></span>
```powershell
PS C:\>       
      $Column1 = New-AzCosmosDBCassandraColumn -Name "ColumnA" -Type "int"
      $Column2 = New-AzCosmosDBCassandraColumn -Name "ColumnB" -Type "ascii"
      $Column3 = New-AzCosmosDBCassandraColumn -Name "ColumnC" -Type "int"
      $Column4 = New-AzCosmosDBCassandraColumn -Name "ColumnD" -Type "ascii"

      $clusterkey1 = New-AzCosmosDBCassandraClusterKey -Name "ColumnB" -OrderBy "Asc"
      $clusterkey2 = New-AzCosmosDBCassandraClusterKey -Name "ColumnA" -OrderBy "Asc"

      $schema = New-AzCosmosDBCassandraSchema -Column $Column1,$Column2 -ClusterKey $clusterkey1 -PartitionKey "ColumnA"

      New-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -KeyspaceName myKeyspaceName -Name myTableName -Schema $schema
        Name     : myTable
        Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName/t
                ables/myTableName
        Location :
        Tags     :
        Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetPropertiesResource
```

## <span data-ttu-id="5072a-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5072a-111">PARAMETERS</span></span>

### <span data-ttu-id="5072a-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5072a-112">-AccountName</span></span>
<span data-ttu-id="5072a-113">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="5072a-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5072a-114">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="5072a-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="5072a-115">Archiviazione analitica TTL.</span><span class="sxs-lookup"><span data-stu-id="5072a-115">Analytical Storage TTL.</span></span>

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

### <span data-ttu-id="5072a-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="5072a-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="5072a-117">Valore massimo della velocità effettiva se autoscale è abilitato.</span><span class="sxs-lookup"><span data-stu-id="5072a-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="5072a-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5072a-118">-Confirm</span></span>
<span data-ttu-id="5072a-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5072a-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5072a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5072a-120">-DefaultProfile</span></span>
<span data-ttu-id="5072a-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5072a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5072a-122">-Barra spaziatrice</span><span class="sxs-lookup"><span data-stu-id="5072a-122">-KeyspaceName</span></span>
<span data-ttu-id="5072a-123">Nome della barra spaziatrice Cassandra.</span><span class="sxs-lookup"><span data-stu-id="5072a-123">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="5072a-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="5072a-124">-Name</span></span>
<span data-ttu-id="5072a-125">Nome tabella Cassandra.</span><span class="sxs-lookup"><span data-stu-id="5072a-125">Cassandra Table Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5072a-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5072a-126">-ParentObject</span></span>
<span data-ttu-id="5072a-127">Oggetto portaspazio Cassandra.</span><span class="sxs-lookup"><span data-stu-id="5072a-127">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="5072a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5072a-128">-ResourceGroupName</span></span>
<span data-ttu-id="5072a-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5072a-129">Name of resource group.</span></span>

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

### <span data-ttu-id="5072a-130">-Schema</span><span class="sxs-lookup"><span data-stu-id="5072a-130">-Schema</span></span>
<span data-ttu-id="5072a-131">Oggetto PSCassandraSchema.</span><span class="sxs-lookup"><span data-stu-id="5072a-131">PSCassandraSchema object.</span></span>
<span data-ttu-id="5072a-132">USA New-AzCosmosDBCassandraSchema per creare questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="5072a-132">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

```yaml
Type: PSCassandraSchema
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5072a-133">-Throughput</span><span class="sxs-lookup"><span data-stu-id="5072a-133">-Throughput</span></span>
<span data-ttu-id="5072a-134">La velocità effettiva di Cassandra della barra spaziatrice (RU/s).</span><span class="sxs-lookup"><span data-stu-id="5072a-134">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="5072a-135">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="5072a-135">Default value is 400.</span></span>

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

### <span data-ttu-id="5072a-136">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="5072a-136">-TtlInSeconds</span></span>
<span data-ttu-id="5072a-137">TTL predefinito in secondi.</span><span class="sxs-lookup"><span data-stu-id="5072a-137">Default Ttl in seconds.</span></span>
<span data-ttu-id="5072a-138">Se il valore è mancante o è impostato su-1, gli elementi non scadono.</span><span class="sxs-lookup"><span data-stu-id="5072a-138">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="5072a-139">Se il valore è impostato su n, gli elementi scadranno n secondi dopo l'ultima modifica dell'ora.</span><span class="sxs-lookup"><span data-stu-id="5072a-139">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="5072a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5072a-140">-WhatIf</span></span>
<span data-ttu-id="5072a-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5072a-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5072a-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5072a-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5072a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5072a-143">CommonParameters</span></span>
<span data-ttu-id="5072a-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5072a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5072a-145">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5072a-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5072a-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5072a-146">INPUTS</span></span>

### <span data-ttu-id="5072a-147">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="5072a-147">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="5072a-148">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="5072a-148">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="5072a-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5072a-149">OUTPUTS</span></span>

### <span data-ttu-id="5072a-150">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="5072a-150">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="5072a-151">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="5072a-151">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="5072a-152">Note</span><span class="sxs-lookup"><span data-stu-id="5072a-152">NOTES</span></span>

## <span data-ttu-id="5072a-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5072a-153">RELATED LINKS</span></span>
