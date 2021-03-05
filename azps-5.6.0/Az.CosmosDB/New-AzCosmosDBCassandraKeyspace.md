---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 9e06e6eaaea72b0fab9b3333291b29bdc09469d7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966701"
---
# <span data-ttu-id="d1765-101">New-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="d1765-101">New-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="d1765-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1765-102">SYNOPSIS</span></span>
<span data-ttu-id="d1765-103">Crea una nuova istanza di CassasDB Cassandra Keyspace.</span><span class="sxs-lookup"><span data-stu-id="d1765-103">Creates a new CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="d1765-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d1765-104">SYNTAX</span></span>

### <span data-ttu-id="d1765-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d1765-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1765-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1765-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBCassandraKeyspace -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d1765-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d1765-107">DESCRIPTION</span></span>
<span data-ttu-id="d1765-108">Crea una nuova istanza di CassasDB Cassandra Keyspace.</span><span class="sxs-lookup"><span data-stu-id="d1765-108">Creates a new CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="d1765-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d1765-109">EXAMPLES</span></span>

### <span data-ttu-id="d1765-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d1765-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput 600

Name     : myKeyspace
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetPropertiesResource
```

## <span data-ttu-id="d1765-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1765-111">PARAMETERS</span></span>

### <span data-ttu-id="d1765-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d1765-112">-AccountName</span></span>
<span data-ttu-id="d1765-113">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="d1765-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d1765-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="d1765-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="d1765-115">Valore massimo di velocità effettiva se è abilitata la scalabilità automatica.</span><span class="sxs-lookup"><span data-stu-id="d1765-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="d1765-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d1765-116">-Confirm</span></span>
<span data-ttu-id="d1765-117">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1765-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1765-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1765-118">-DefaultProfile</span></span>
<span data-ttu-id="d1765-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d1765-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1765-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d1765-120">-Name</span></span>
<span data-ttu-id="d1765-121">Nome spazio tasti Cassandra.</span><span class="sxs-lookup"><span data-stu-id="d1765-121">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="d1765-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d1765-122">-ParentObject</span></span>
<span data-ttu-id="d1765-123">Oggetto Account Aziendale</span><span class="sxs-lookup"><span data-stu-id="d1765-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="d1765-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1765-124">-ResourceGroupName</span></span>
<span data-ttu-id="d1765-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d1765-125">Name of resource group.</span></span>

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

### <span data-ttu-id="d1765-126">-Velocità effettiva</span><span class="sxs-lookup"><span data-stu-id="d1765-126">-Throughput</span></span>
<span data-ttu-id="d1765-127">Velocità effettiva di Cassandra Keyspace (RU/s).</span><span class="sxs-lookup"><span data-stu-id="d1765-127">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="d1765-128">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="d1765-128">Default value is 400.</span></span>

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

### <span data-ttu-id="d1765-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1765-129">-WhatIf</span></span>
<span data-ttu-id="d1765-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d1765-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1765-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d1765-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1765-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1765-132">CommonParameters</span></span>
<span data-ttu-id="d1765-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1765-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1765-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d1765-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1765-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="d1765-135">INPUTS</span></span>

### <span data-ttu-id="d1765-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="d1765-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="d1765-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d1765-137">OUTPUTS</span></span>

### <span data-ttu-id="d1765-138">Microsoft.Azure.Commands.CommonsDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="d1765-138">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="d1765-139">Microsoft.Azure.Commands.CpsDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="d1765-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="d1765-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="d1765-140">NOTES</span></span>

## <span data-ttu-id="d1765-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d1765-141">RELATED LINKS</span></span>
