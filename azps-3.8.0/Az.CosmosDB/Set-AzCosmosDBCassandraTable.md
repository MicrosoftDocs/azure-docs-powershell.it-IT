---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBCassandraTable.md
ms.openlocfilehash: e79353d5265a2d58b72e49ee1978ea92599bed39
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022397"
---
# <span data-ttu-id="6232c-101">Set-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="6232c-101">Set-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="6232c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6232c-102">SYNOPSIS</span></span>
<span data-ttu-id="6232c-103">Imposta la tabella CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="6232c-103">Sets the CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="6232c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6232c-104">SYNTAX</span></span>

### <span data-ttu-id="6232c-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6232c-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-Throughput <Int32>] [-TtlInSeconds <Int32>] -Schema <PSCassandraSchema>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6232c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6232c-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBCassandraTable -Name <String> [-Throughput <Int32>] [-TtlInSeconds <Int32>]
 -Schema <PSCassandraSchema> -InputObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6232c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6232c-107">DESCRIPTION</span></span>
<span data-ttu-id="6232c-108">Il cmdlet **set-AzCosmosDBCassandraTable** imposta lo spazio per la CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="6232c-108">The **Set-AzCosmosDBCassandraTable** cmdlet sets the CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="6232c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6232c-109">EXAMPLES</span></span>

### <span data-ttu-id="6232c-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6232c-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBCassandraTable -ResourceGroupName {rgName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {tableName}
Name        Id    Resource
----        --    -------
{name}     {id}   Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetPropertiesResource
```

<span data-ttu-id="6232c-111">Oggetto Resource contiene i valori delle proprietà _rid, _ts, _etag, DefaultTtl e schema.</span><span class="sxs-lookup"><span data-stu-id="6232c-111">Resource object contains the values of the _rid, _ts, _etag, DefaultTtl and Schema properties.</span></span>

## <span data-ttu-id="6232c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6232c-112">PARAMETERS</span></span>

### <span data-ttu-id="6232c-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6232c-113">-AccountName</span></span>
<span data-ttu-id="6232c-114">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="6232c-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="6232c-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6232c-115">-Confirm</span></span>
<span data-ttu-id="6232c-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6232c-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6232c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6232c-117">-DefaultProfile</span></span>
<span data-ttu-id="6232c-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6232c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6232c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6232c-119">-InputObject</span></span>
<span data-ttu-id="6232c-120">Oggetto portaspazio Cassandra.</span><span class="sxs-lookup"><span data-stu-id="6232c-120">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="6232c-121">-Barra spaziatrice</span><span class="sxs-lookup"><span data-stu-id="6232c-121">-KeyspaceName</span></span>
<span data-ttu-id="6232c-122">Nome della barra spaziatrice Cassandra.</span><span class="sxs-lookup"><span data-stu-id="6232c-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="6232c-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="6232c-123">-Name</span></span>
<span data-ttu-id="6232c-124">Nome tabella Cassandra.</span><span class="sxs-lookup"><span data-stu-id="6232c-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="6232c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6232c-125">-ResourceGroupName</span></span>
<span data-ttu-id="6232c-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6232c-126">Name of resource group.</span></span>

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

### <span data-ttu-id="6232c-127">-Schema</span><span class="sxs-lookup"><span data-stu-id="6232c-127">-Schema</span></span>
<span data-ttu-id="6232c-128">Oggetto PSCassandraSchema.</span><span class="sxs-lookup"><span data-stu-id="6232c-128">PSCassandraSchema object.</span></span>
<span data-ttu-id="6232c-129">USA New-AzCosmosDBCassandraSchema per creare questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="6232c-129">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

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

### <span data-ttu-id="6232c-130">-Throughput</span><span class="sxs-lookup"><span data-stu-id="6232c-130">-Throughput</span></span>
<span data-ttu-id="6232c-131">La velocità effettiva di Cassandra della barra spaziatrice (RU/s).</span><span class="sxs-lookup"><span data-stu-id="6232c-131">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="6232c-132">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="6232c-132">Default value is 400.</span></span>

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

### <span data-ttu-id="6232c-133">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="6232c-133">-TtlInSeconds</span></span>
<span data-ttu-id="6232c-134">TTL predefinito in secondi.</span><span class="sxs-lookup"><span data-stu-id="6232c-134">Default Ttl in seconds.</span></span>
<span data-ttu-id="6232c-135">Se il valore è mancante o è impostato su-1, gli elementi non scadono.</span><span class="sxs-lookup"><span data-stu-id="6232c-135">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="6232c-136">Se il valore è impostato su n, gli elementi scadranno n secondi dopo l'ultima modifica dell'ora.</span><span class="sxs-lookup"><span data-stu-id="6232c-136">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="6232c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6232c-137">-WhatIf</span></span>
<span data-ttu-id="6232c-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6232c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6232c-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6232c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6232c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6232c-140">CommonParameters</span></span>
<span data-ttu-id="6232c-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6232c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6232c-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6232c-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6232c-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6232c-143">INPUTS</span></span>

### <span data-ttu-id="6232c-144">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="6232c-144">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="6232c-145">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="6232c-145">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="6232c-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6232c-146">OUTPUTS</span></span>

### <span data-ttu-id="6232c-147">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="6232c-147">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="6232c-148">Note</span><span class="sxs-lookup"><span data-stu-id="6232c-148">NOTES</span></span>

## <span data-ttu-id="6232c-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6232c-149">RELATED LINKS</span></span>
