---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 8998e9e2462e64dab3d2a96c739c93449e2e360c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181319"
---
# <span data-ttu-id="f5e59-101">New-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="f5e59-101">New-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="f5e59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5e59-102">SYNOPSIS</span></span>
<span data-ttu-id="f5e59-103">Crea una nuova istanza di CassasDB Cassandra Keyspace.</span><span class="sxs-lookup"><span data-stu-id="f5e59-103">Creates a new CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="f5e59-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f5e59-104">SYNTAX</span></span>

### <span data-ttu-id="f5e59-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f5e59-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5e59-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5e59-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBCassandraKeyspace -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f5e59-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f5e59-107">DESCRIPTION</span></span>
<span data-ttu-id="f5e59-108">Crea una nuova istanza di CassasDB Cassandra Keyspace.</span><span class="sxs-lookup"><span data-stu-id="f5e59-108">Creates a new CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="f5e59-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f5e59-109">EXAMPLES</span></span>

### <span data-ttu-id="f5e59-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f5e59-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput 600

Name     : myKeyspace
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetPropertiesResource
```

## <span data-ttu-id="f5e59-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5e59-111">PARAMETERS</span></span>

### <span data-ttu-id="f5e59-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f5e59-112">-AccountName</span></span>
<span data-ttu-id="f5e59-113">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="f5e59-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f5e59-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="f5e59-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="f5e59-115">Valore massimo di velocità effettiva se è abilitata la scalabilità automatica.</span><span class="sxs-lookup"><span data-stu-id="f5e59-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="f5e59-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f5e59-116">-Confirm</span></span>
<span data-ttu-id="f5e59-117">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5e59-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5e59-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5e59-118">-DefaultProfile</span></span>
<span data-ttu-id="f5e59-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f5e59-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5e59-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f5e59-120">-Name</span></span>
<span data-ttu-id="f5e59-121">Nome spazio tasti Cassandra.</span><span class="sxs-lookup"><span data-stu-id="f5e59-121">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="f5e59-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f5e59-122">-ParentObject</span></span>
<span data-ttu-id="f5e59-123">Oggetto AccountDb Disa</span><span class="sxs-lookup"><span data-stu-id="f5e59-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="f5e59-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5e59-124">-ResourceGroupName</span></span>
<span data-ttu-id="f5e59-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f5e59-125">Name of resource group.</span></span>

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

### <span data-ttu-id="f5e59-126">-Velocità effettiva</span><span class="sxs-lookup"><span data-stu-id="f5e59-126">-Throughput</span></span>
<span data-ttu-id="f5e59-127">Velocità effettiva di Cassandra Keyspace (RU/s).</span><span class="sxs-lookup"><span data-stu-id="f5e59-127">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="f5e59-128">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="f5e59-128">Default value is 400.</span></span>

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

### <span data-ttu-id="f5e59-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5e59-129">-WhatIf</span></span>
<span data-ttu-id="f5e59-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f5e59-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5e59-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f5e59-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5e59-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5e59-132">CommonParameters</span></span>
<span data-ttu-id="f5e59-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5e59-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5e59-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f5e59-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5e59-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="f5e59-135">INPUTS</span></span>

### <span data-ttu-id="f5e59-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="f5e59-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="f5e59-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f5e59-137">OUTPUTS</span></span>

### <span data-ttu-id="f5e59-138">Microsoft.Azure.Commands.EnterpriseDb.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="f5e59-138">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="f5e59-139">Microsoft.Azure.Commands.ExceptionsDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="f5e59-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="f5e59-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="f5e59-140">NOTES</span></span>

## <span data-ttu-id="f5e59-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f5e59-141">RELATED LINKS</span></span>
