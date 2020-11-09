---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: cff6f0bd099e8379e47f4100bd4b20a3b6eb36b6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299089"
---
# <span data-ttu-id="f5c8a-101">Update-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="f5c8a-101">Update-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="f5c8a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f5c8a-102">SYNOPSIS</span></span>
<span data-ttu-id="f5c8a-103">Aggiorna lo spazio di CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="f5c8a-103">Updates the CosmosDB Cassandra Keyspace.</span></span> <span data-ttu-id="f5c8a-104">Esegue un'operazione di patch lato client leggendo lo spazio dei blocchi esistente.</span><span class="sxs-lookup"><span data-stu-id="f5c8a-104">Performs a client side patch operation by reading the existing Keyspace.</span></span>

## <span data-ttu-id="f5c8a-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f5c8a-105">SYNTAX</span></span>

### <span data-ttu-id="f5c8a-106">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f5c8a-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5c8a-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5c8a-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspace [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f5c8a-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5c8a-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspace [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f5c8a-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f5c8a-109">DESCRIPTION</span></span>
<span data-ttu-id="f5c8a-110">Aggiorna lo spazio di CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="f5c8a-110">Updates the CosmosDB Cassandra Keyspace.</span></span> <span data-ttu-id="f5c8a-111">Esegue un'operazione di patch lato client leggendo lo spazio dei blocchi esistente.</span><span class="sxs-lookup"><span data-stu-id="f5c8a-111">Performs a client side patch operation by reading the existing Keyspace.</span></span>

## <span data-ttu-id="f5c8a-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f5c8a-112">EXAMPLES</span></span>

### <span data-ttu-id="f5c8a-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f5c8a-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput 600

Name     : myKeyspace
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetPropertiesResource
```

## <span data-ttu-id="f5c8a-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f5c8a-114">PARAMETERS</span></span>

### <span data-ttu-id="f5c8a-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f5c8a-115">-AccountName</span></span>
<span data-ttu-id="f5c8a-116">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="f5c8a-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f5c8a-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="f5c8a-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="f5c8a-118">Valore massimo della velocità effettiva se autoscale è abilitato.</span><span class="sxs-lookup"><span data-stu-id="f5c8a-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="f5c8a-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f5c8a-119">-Confirm</span></span>
<span data-ttu-id="f5c8a-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5c8a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5c8a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5c8a-121">-DefaultProfile</span></span>
<span data-ttu-id="f5c8a-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f5c8a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5c8a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5c8a-123">-InputObject</span></span>
<span data-ttu-id="f5c8a-124">Oggetto portaspazio Cassandra.</span><span class="sxs-lookup"><span data-stu-id="f5c8a-124">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="f5c8a-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="f5c8a-125">-Name</span></span>
<span data-ttu-id="f5c8a-126">Nome della barra spaziatrice Cassandra.</span><span class="sxs-lookup"><span data-stu-id="f5c8a-126">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="f5c8a-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f5c8a-127">-ParentObject</span></span>
<span data-ttu-id="f5c8a-128">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="f5c8a-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="f5c8a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5c8a-129">-ResourceGroupName</span></span>
<span data-ttu-id="f5c8a-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f5c8a-130">Name of resource group.</span></span>

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

### <span data-ttu-id="f5c8a-131">-Throughput</span><span class="sxs-lookup"><span data-stu-id="f5c8a-131">-Throughput</span></span>
<span data-ttu-id="f5c8a-132">La velocità effettiva di Cassandra della barra spaziatrice (RU/s).</span><span class="sxs-lookup"><span data-stu-id="f5c8a-132">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="f5c8a-133">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="f5c8a-133">Default value is 400.</span></span>

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

### <span data-ttu-id="f5c8a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5c8a-134">-WhatIf</span></span>
<span data-ttu-id="f5c8a-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f5c8a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5c8a-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f5c8a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5c8a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5c8a-137">CommonParameters</span></span>
<span data-ttu-id="f5c8a-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5c8a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5c8a-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f5c8a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5c8a-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f5c8a-140">INPUTS</span></span>

### <span data-ttu-id="f5c8a-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="f5c8a-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="f5c8a-142">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="f5c8a-142">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="f5c8a-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f5c8a-143">OUTPUTS</span></span>

### <span data-ttu-id="f5c8a-144">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="f5c8a-144">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="f5c8a-145">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="f5c8a-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="f5c8a-146">Note</span><span class="sxs-lookup"><span data-stu-id="f5c8a-146">NOTES</span></span>

## <span data-ttu-id="f5c8a-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f5c8a-147">RELATED LINKS</span></span>
