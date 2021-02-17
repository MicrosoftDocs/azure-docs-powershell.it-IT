---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: cff6f0bd099e8379e47f4100bd4b20a3b6eb36b6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177222"
---
# <span data-ttu-id="7db45-101">Update-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="7db45-101">Update-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="7db45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7db45-102">SYNOPSIS</span></span>
<span data-ttu-id="7db45-103">Aggiorna lo spazio dei dati del database Cassandra Keyspace.</span><span class="sxs-lookup"><span data-stu-id="7db45-103">Updates the CosmosDB Cassandra Keyspace.</span></span> <span data-ttu-id="7db45-104">Esegue un'operazione di patch sul lato client leggendo il tasto Keyspace esistente.</span><span class="sxs-lookup"><span data-stu-id="7db45-104">Performs a client side patch operation by reading the existing Keyspace.</span></span>

## <span data-ttu-id="7db45-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7db45-105">SYNTAX</span></span>

### <span data-ttu-id="7db45-106">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7db45-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7db45-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7db45-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspace [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7db45-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7db45-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspace [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7db45-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7db45-109">DESCRIPTION</span></span>
<span data-ttu-id="7db45-110">Aggiorna lo spazio dei dati del database Cassandra Keyspace.</span><span class="sxs-lookup"><span data-stu-id="7db45-110">Updates the CosmosDB Cassandra Keyspace.</span></span> <span data-ttu-id="7db45-111">Esegue un'operazione di patch sul lato client leggendo il tasto Keyspace esistente.</span><span class="sxs-lookup"><span data-stu-id="7db45-111">Performs a client side patch operation by reading the existing Keyspace.</span></span>

## <span data-ttu-id="7db45-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7db45-112">EXAMPLES</span></span>

### <span data-ttu-id="7db45-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7db45-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput 600

Name     : myKeyspace
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetPropertiesResource
```

## <span data-ttu-id="7db45-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7db45-114">PARAMETERS</span></span>

### <span data-ttu-id="7db45-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7db45-115">-AccountName</span></span>
<span data-ttu-id="7db45-116">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="7db45-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7db45-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="7db45-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="7db45-118">Valore massimo di velocità effettiva se è abilitata la scalabilità automatica.</span><span class="sxs-lookup"><span data-stu-id="7db45-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="7db45-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7db45-119">-Confirm</span></span>
<span data-ttu-id="7db45-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7db45-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7db45-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7db45-121">-DefaultProfile</span></span>
<span data-ttu-id="7db45-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7db45-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7db45-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7db45-123">-InputObject</span></span>
<span data-ttu-id="7db45-124">Oggetto Cassandra Keyspace.</span><span class="sxs-lookup"><span data-stu-id="7db45-124">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="7db45-125">-Name</span><span class="sxs-lookup"><span data-stu-id="7db45-125">-Name</span></span>
<span data-ttu-id="7db45-126">Nome spazio tasti Cassandra.</span><span class="sxs-lookup"><span data-stu-id="7db45-126">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="7db45-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7db45-127">-ParentObject</span></span>
<span data-ttu-id="7db45-128">Oggetto AccountDb Disa</span><span class="sxs-lookup"><span data-stu-id="7db45-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="7db45-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7db45-129">-ResourceGroupName</span></span>
<span data-ttu-id="7db45-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7db45-130">Name of resource group.</span></span>

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

### <span data-ttu-id="7db45-131">-Velocità effettiva</span><span class="sxs-lookup"><span data-stu-id="7db45-131">-Throughput</span></span>
<span data-ttu-id="7db45-132">Velocità effettiva di Cassandra Keyspace (RU/s).</span><span class="sxs-lookup"><span data-stu-id="7db45-132">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="7db45-133">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="7db45-133">Default value is 400.</span></span>

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

### <span data-ttu-id="7db45-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7db45-134">-WhatIf</span></span>
<span data-ttu-id="7db45-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7db45-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7db45-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7db45-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7db45-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7db45-137">CommonParameters</span></span>
<span data-ttu-id="7db45-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7db45-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7db45-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7db45-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7db45-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="7db45-140">INPUTS</span></span>

### <span data-ttu-id="7db45-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="7db45-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="7db45-142">Microsoft.Azure.Commands.EnterpriseDb.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="7db45-142">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="7db45-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7db45-143">OUTPUTS</span></span>

### <span data-ttu-id="7db45-144">Microsoft.Azure.Commands.EnterpriseDb.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="7db45-144">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="7db45-145">Microsoft.Azure.Commands.ExceptionsDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="7db45-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="7db45-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="7db45-146">NOTES</span></span>

## <span data-ttu-id="7db45-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7db45-147">RELATED LINKS</span></span>
