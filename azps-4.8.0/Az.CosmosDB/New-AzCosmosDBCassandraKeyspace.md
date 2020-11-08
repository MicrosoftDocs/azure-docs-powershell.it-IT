---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 8998e9e2462e64dab3d2a96c739c93449e2e360c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033215"
---
# <span data-ttu-id="39d40-101">New-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="39d40-101">New-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="39d40-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="39d40-102">SYNOPSIS</span></span>
<span data-ttu-id="39d40-103">Crea un nuovo spazio di CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="39d40-103">Creates a new CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="39d40-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="39d40-104">SYNTAX</span></span>

### <span data-ttu-id="39d40-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="39d40-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39d40-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="39d40-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBCassandraKeyspace -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="39d40-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="39d40-107">DESCRIPTION</span></span>
<span data-ttu-id="39d40-108">Crea un nuovo spazio di CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="39d40-108">Creates a new CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="39d40-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="39d40-109">EXAMPLES</span></span>

### <span data-ttu-id="39d40-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="39d40-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput 600

Name     : myKeyspace
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetPropertiesResource
```

## <span data-ttu-id="39d40-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="39d40-111">PARAMETERS</span></span>

### <span data-ttu-id="39d40-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="39d40-112">-AccountName</span></span>
<span data-ttu-id="39d40-113">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="39d40-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="39d40-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="39d40-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="39d40-115">Valore massimo della velocità effettiva se autoscale è abilitato.</span><span class="sxs-lookup"><span data-stu-id="39d40-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="39d40-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="39d40-116">-Confirm</span></span>
<span data-ttu-id="39d40-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39d40-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39d40-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39d40-118">-DefaultProfile</span></span>
<span data-ttu-id="39d40-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="39d40-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39d40-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="39d40-120">-Name</span></span>
<span data-ttu-id="39d40-121">Nome della barra spaziatrice Cassandra.</span><span class="sxs-lookup"><span data-stu-id="39d40-121">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="39d40-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="39d40-122">-ParentObject</span></span>
<span data-ttu-id="39d40-123">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="39d40-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="39d40-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39d40-124">-ResourceGroupName</span></span>
<span data-ttu-id="39d40-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="39d40-125">Name of resource group.</span></span>

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

### <span data-ttu-id="39d40-126">-Throughput</span><span class="sxs-lookup"><span data-stu-id="39d40-126">-Throughput</span></span>
<span data-ttu-id="39d40-127">La velocità effettiva di Cassandra della barra spaziatrice (RU/s).</span><span class="sxs-lookup"><span data-stu-id="39d40-127">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="39d40-128">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="39d40-128">Default value is 400.</span></span>

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

### <span data-ttu-id="39d40-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39d40-129">-WhatIf</span></span>
<span data-ttu-id="39d40-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="39d40-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39d40-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="39d40-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39d40-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39d40-132">CommonParameters</span></span>
<span data-ttu-id="39d40-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39d40-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39d40-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="39d40-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39d40-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="39d40-135">INPUTS</span></span>

### <span data-ttu-id="39d40-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="39d40-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="39d40-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="39d40-137">OUTPUTS</span></span>

### <span data-ttu-id="39d40-138">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="39d40-138">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="39d40-139">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="39d40-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="39d40-140">Note</span><span class="sxs-lookup"><span data-stu-id="39d40-140">NOTES</span></span>

## <span data-ttu-id="39d40-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="39d40-141">RELATED LINKS</span></span>
