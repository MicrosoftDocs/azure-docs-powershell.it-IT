---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 6fad5017dbd7dd258e44e69638a919e53597ec9d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344656"
---
# <span data-ttu-id="28c28-101">Update-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="28c28-101">Update-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="28c28-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="28c28-102">SYNOPSIS</span></span>
<span data-ttu-id="28c28-103">Aggiorna la tabella CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="28c28-103">Updates the CosmosDB Cassandra Table.</span></span> <span data-ttu-id="28c28-104">Esegue un'operazione di patch lato client leggendo la tabella esistente.</span><span class="sxs-lookup"><span data-stu-id="28c28-104">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="28c28-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="28c28-105">SYNTAX</span></span>

### <span data-ttu-id="28c28-106">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="28c28-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28c28-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="28c28-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>]
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="28c28-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="28c28-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>]
 -InputObject <PSCassandraTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="28c28-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="28c28-109">DESCRIPTION</span></span>
<span data-ttu-id="28c28-110">Aggiorna la tabella CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="28c28-110">Updates the CosmosDB Cassandra Table.</span></span> <span data-ttu-id="28c28-111">Esegue un'operazione di patch lato client leggendo la tabella esistente.</span><span class="sxs-lookup"><span data-stu-id="28c28-111">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="28c28-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="28c28-112">EXAMPLES</span></span>

### <span data-ttu-id="28c28-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="28c28-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -KeyspaceName myKeyspaceName -Name myTableName -Schema updatedSchema
        Name     : myTable
        Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName/t
                ables/myTableName
        Location :
        Tags     :
        Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetPropertiesResource
```

<span data-ttu-id="28c28-114">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="28c28-114">{{ Add example description here }}</span></span>

## <span data-ttu-id="28c28-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="28c28-115">PARAMETERS</span></span>

### <span data-ttu-id="28c28-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="28c28-116">-AccountName</span></span>
<span data-ttu-id="28c28-117">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="28c28-117">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="28c28-118">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="28c28-118">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="28c28-119">Archiviazione analitica TTL.</span><span class="sxs-lookup"><span data-stu-id="28c28-119">Analytical Storage TTL.</span></span>

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

### <span data-ttu-id="28c28-120">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="28c28-120">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="28c28-121">Valore massimo della velocità effettiva se autoscale è abilitato.</span><span class="sxs-lookup"><span data-stu-id="28c28-121">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="28c28-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="28c28-122">-Confirm</span></span>
<span data-ttu-id="28c28-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28c28-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28c28-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28c28-124">-DefaultProfile</span></span>
<span data-ttu-id="28c28-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="28c28-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28c28-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28c28-126">-InputObject</span></span>
<span data-ttu-id="28c28-127">Oggetto tabella Cassandra.</span><span class="sxs-lookup"><span data-stu-id="28c28-127">Cassandra Table object.</span></span>

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

### <span data-ttu-id="28c28-128">-Barra spaziatrice</span><span class="sxs-lookup"><span data-stu-id="28c28-128">-KeyspaceName</span></span>
<span data-ttu-id="28c28-129">Nome della barra spaziatrice Cassandra.</span><span class="sxs-lookup"><span data-stu-id="28c28-129">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="28c28-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="28c28-130">-Name</span></span>
<span data-ttu-id="28c28-131">Nome tabella Cassandra.</span><span class="sxs-lookup"><span data-stu-id="28c28-131">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="28c28-132">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="28c28-132">-ParentObject</span></span>
<span data-ttu-id="28c28-133">Oggetto portaspazio Cassandra.</span><span class="sxs-lookup"><span data-stu-id="28c28-133">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="28c28-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28c28-134">-ResourceGroupName</span></span>
<span data-ttu-id="28c28-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="28c28-135">Name of resource group.</span></span>

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

### <span data-ttu-id="28c28-136">-Schema</span><span class="sxs-lookup"><span data-stu-id="28c28-136">-Schema</span></span>
<span data-ttu-id="28c28-137">Oggetto PSCassandraSchema.</span><span class="sxs-lookup"><span data-stu-id="28c28-137">PSCassandraSchema object.</span></span>
<span data-ttu-id="28c28-138">USA New-AzCosmosDBCassandraSchema per creare questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="28c28-138">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

```yaml
Type: PSCassandraSchema
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28c28-139">-Throughput</span><span class="sxs-lookup"><span data-stu-id="28c28-139">-Throughput</span></span>
<span data-ttu-id="28c28-140">La velocità effettiva di Cassandra della barra spaziatrice (RU/s).</span><span class="sxs-lookup"><span data-stu-id="28c28-140">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="28c28-141">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="28c28-141">Default value is 400.</span></span>

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

### <span data-ttu-id="28c28-142">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="28c28-142">-TtlInSeconds</span></span>
<span data-ttu-id="28c28-143">TTL predefinito in secondi.</span><span class="sxs-lookup"><span data-stu-id="28c28-143">Default Ttl in seconds.</span></span>
<span data-ttu-id="28c28-144">Se il valore è mancante o è impostato su-1, gli elementi non scadono.</span><span class="sxs-lookup"><span data-stu-id="28c28-144">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="28c28-145">Se il valore è impostato su n, gli elementi scadranno n secondi dopo l'ultima modifica dell'ora.</span><span class="sxs-lookup"><span data-stu-id="28c28-145">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="28c28-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28c28-146">-WhatIf</span></span>
<span data-ttu-id="28c28-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="28c28-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28c28-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="28c28-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28c28-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28c28-149">CommonParameters</span></span>
<span data-ttu-id="28c28-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28c28-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28c28-151">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28c28-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28c28-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="28c28-152">INPUTS</span></span>

### <span data-ttu-id="28c28-153">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="28c28-153">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="28c28-154">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="28c28-154">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="28c28-155">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="28c28-155">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="28c28-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="28c28-156">OUTPUTS</span></span>

### <span data-ttu-id="28c28-157">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="28c28-157">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="28c28-158">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="28c28-158">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="28c28-159">Note</span><span class="sxs-lookup"><span data-stu-id="28c28-159">NOTES</span></span>

## <span data-ttu-id="28c28-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="28c28-160">RELATED LINKS</span></span>
