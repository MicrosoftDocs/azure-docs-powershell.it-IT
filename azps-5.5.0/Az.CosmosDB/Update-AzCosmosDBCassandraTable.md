---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 6fad5017dbd7dd258e44e69638a919e53597ec9d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198934"
---
# <span data-ttu-id="66b82-101">Update-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="66b82-101">Update-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="66b82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66b82-102">SYNOPSIS</span></span>
<span data-ttu-id="66b82-103">Aggiorna la tabella CassandraDb.</span><span class="sxs-lookup"><span data-stu-id="66b82-103">Updates the CosmosDB Cassandra Table.</span></span> <span data-ttu-id="66b82-104">Esegue un'operazione di patch sul lato client leggendo la tabella esistente.</span><span class="sxs-lookup"><span data-stu-id="66b82-104">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="66b82-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="66b82-105">SYNTAX</span></span>

### <span data-ttu-id="66b82-106">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="66b82-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66b82-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="66b82-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>]
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="66b82-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="66b82-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>]
 -InputObject <PSCassandraTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="66b82-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="66b82-109">DESCRIPTION</span></span>
<span data-ttu-id="66b82-110">Aggiorna la tabella CassandraDb.</span><span class="sxs-lookup"><span data-stu-id="66b82-110">Updates the CosmosDB Cassandra Table.</span></span> <span data-ttu-id="66b82-111">Esegue un'operazione di patch sul lato client leggendo la tabella esistente.</span><span class="sxs-lookup"><span data-stu-id="66b82-111">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="66b82-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="66b82-112">EXAMPLES</span></span>

### <span data-ttu-id="66b82-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="66b82-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -KeyspaceName myKeyspaceName -Name myTableName -Schema updatedSchema
        Name     : myTable
        Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName/t
                ables/myTableName
        Location :
        Tags     :
        Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetPropertiesResource
```

<span data-ttu-id="66b82-114">{{ Aggiungi la descrizione di esempio qui }}</span><span class="sxs-lookup"><span data-stu-id="66b82-114">{{ Add example description here }}</span></span>

## <span data-ttu-id="66b82-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66b82-115">PARAMETERS</span></span>

### <span data-ttu-id="66b82-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="66b82-116">-AccountName</span></span>
<span data-ttu-id="66b82-117">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="66b82-117">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="66b82-118">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="66b82-118">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="66b82-119">TTL di archiviazione analitica.</span><span class="sxs-lookup"><span data-stu-id="66b82-119">Analytical Storage TTL.</span></span>

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

### <span data-ttu-id="66b82-120">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="66b82-120">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="66b82-121">Valore massimo di velocità effettiva se è abilitata la scalabilità automatica.</span><span class="sxs-lookup"><span data-stu-id="66b82-121">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="66b82-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="66b82-122">-Confirm</span></span>
<span data-ttu-id="66b82-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66b82-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66b82-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66b82-124">-DefaultProfile</span></span>
<span data-ttu-id="66b82-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="66b82-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66b82-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66b82-126">-InputObject</span></span>
<span data-ttu-id="66b82-127">Oggetto Table di Cassandra.</span><span class="sxs-lookup"><span data-stu-id="66b82-127">Cassandra Table object.</span></span>

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

### <span data-ttu-id="66b82-128">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="66b82-128">-KeyspaceName</span></span>
<span data-ttu-id="66b82-129">Nome spazio tasti Cassandra.</span><span class="sxs-lookup"><span data-stu-id="66b82-129">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="66b82-130">-Name</span><span class="sxs-lookup"><span data-stu-id="66b82-130">-Name</span></span>
<span data-ttu-id="66b82-131">Nome tabella Cassandra.</span><span class="sxs-lookup"><span data-stu-id="66b82-131">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="66b82-132">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="66b82-132">-ParentObject</span></span>
<span data-ttu-id="66b82-133">Oggetto Cassandra Keyspace.</span><span class="sxs-lookup"><span data-stu-id="66b82-133">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="66b82-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66b82-134">-ResourceGroupName</span></span>
<span data-ttu-id="66b82-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="66b82-135">Name of resource group.</span></span>

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

### <span data-ttu-id="66b82-136">-Schema</span><span class="sxs-lookup"><span data-stu-id="66b82-136">-Schema</span></span>
<span data-ttu-id="66b82-137">Oggetto PSCassandraSchema.</span><span class="sxs-lookup"><span data-stu-id="66b82-137">PSCassandraSchema object.</span></span>
<span data-ttu-id="66b82-138">Usare New-AzCosmosDBCassandraSchema per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="66b82-138">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

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

### <span data-ttu-id="66b82-139">-Velocità effettiva</span><span class="sxs-lookup"><span data-stu-id="66b82-139">-Throughput</span></span>
<span data-ttu-id="66b82-140">Velocità effettiva di Cassandra Keyspace (RU/s).</span><span class="sxs-lookup"><span data-stu-id="66b82-140">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="66b82-141">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="66b82-141">Default value is 400.</span></span>

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

### <span data-ttu-id="66b82-142">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="66b82-142">-TtlInSeconds</span></span>
<span data-ttu-id="66b82-143">Ttl predefinito in secondi.</span><span class="sxs-lookup"><span data-stu-id="66b82-143">Default Ttl in seconds.</span></span>
<span data-ttu-id="66b82-144">Se il valore manca o è impostato su -1, gli elementi non scadono.</span><span class="sxs-lookup"><span data-stu-id="66b82-144">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="66b82-145">Se il valore è impostato su n, gli elementi scadranno n secondi dopo l'ora dell'ultima modifica.</span><span class="sxs-lookup"><span data-stu-id="66b82-145">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="66b82-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66b82-146">-WhatIf</span></span>
<span data-ttu-id="66b82-147">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="66b82-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66b82-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="66b82-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66b82-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66b82-149">CommonParameters</span></span>
<span data-ttu-id="66b82-150">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66b82-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66b82-151">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="66b82-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66b82-152">INPUT</span><span class="sxs-lookup"><span data-stu-id="66b82-152">INPUTS</span></span>

### <span data-ttu-id="66b82-153">Microsoft.Azure.Commands.ColumnsDB.Models.PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="66b82-153">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="66b82-154">Microsoft.Azure.Commands.EnterpriseDb.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="66b82-154">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="66b82-155">Microsoft.Azure.Commands.EnterpriseDb.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="66b82-155">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="66b82-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="66b82-156">OUTPUTS</span></span>

### <span data-ttu-id="66b82-157">Microsoft.Azure.Commands.EnterpriseDb.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="66b82-157">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="66b82-158">Microsoft.Azure.Commands.ExceptionsDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="66b82-158">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="66b82-159">NOTE</span><span class="sxs-lookup"><span data-stu-id="66b82-159">NOTES</span></span>

## <span data-ttu-id="66b82-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="66b82-160">RELATED LINKS</span></span>
