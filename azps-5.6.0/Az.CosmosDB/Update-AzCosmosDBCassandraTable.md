---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 3f41c44c6abffaf5147ffba17fe3ec84561315b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977422"
---
# <span data-ttu-id="a5b44-101">Update-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="a5b44-101">Update-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="a5b44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5b44-102">SYNOPSIS</span></span>
<span data-ttu-id="a5b44-103">Aggiorna la tabella CassandraDb.</span><span class="sxs-lookup"><span data-stu-id="a5b44-103">Updates the CosmosDB Cassandra Table.</span></span> <span data-ttu-id="a5b44-104">Esegue un'operazione di patch sul lato client leggendo la tabella esistente.</span><span class="sxs-lookup"><span data-stu-id="a5b44-104">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="a5b44-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a5b44-105">SYNTAX</span></span>

### <span data-ttu-id="a5b44-106">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a5b44-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5b44-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5b44-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>]
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5b44-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5b44-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>]
 -InputObject <PSCassandraTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5b44-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a5b44-109">DESCRIPTION</span></span>
<span data-ttu-id="a5b44-110">Aggiorna la tabella CassandraDb.</span><span class="sxs-lookup"><span data-stu-id="a5b44-110">Updates the CosmosDB Cassandra Table.</span></span> <span data-ttu-id="a5b44-111">Esegue un'operazione di patch sul lato client leggendo la tabella esistente.</span><span class="sxs-lookup"><span data-stu-id="a5b44-111">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="a5b44-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a5b44-112">EXAMPLES</span></span>

### <span data-ttu-id="a5b44-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a5b44-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -KeyspaceName myKeyspaceName -Name myTableName -Schema updatedSchema
        Name     : myTable
        Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName/t
                ables/myTableName
        Location :
        Tags     :
        Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetPropertiesResource
```

<span data-ttu-id="a5b44-114">{{ Aggiungi la descrizione di esempio qui }}</span><span class="sxs-lookup"><span data-stu-id="a5b44-114">{{ Add example description here }}</span></span>

## <span data-ttu-id="a5b44-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5b44-115">PARAMETERS</span></span>

### <span data-ttu-id="a5b44-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a5b44-116">-AccountName</span></span>
<span data-ttu-id="a5b44-117">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="a5b44-117">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a5b44-118">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="a5b44-118">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="a5b44-119">TTL di archiviazione analitica.</span><span class="sxs-lookup"><span data-stu-id="a5b44-119">Analytical Storage TTL.</span></span>

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

### <span data-ttu-id="a5b44-120">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="a5b44-120">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="a5b44-121">Valore massimo di velocità effettiva se è abilitata la scalabilità automatica.</span><span class="sxs-lookup"><span data-stu-id="a5b44-121">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="a5b44-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5b44-122">-Confirm</span></span>
<span data-ttu-id="a5b44-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5b44-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5b44-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5b44-124">-DefaultProfile</span></span>
<span data-ttu-id="a5b44-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a5b44-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5b44-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5b44-126">-InputObject</span></span>
<span data-ttu-id="a5b44-127">Oggetto Table di Cassandra.</span><span class="sxs-lookup"><span data-stu-id="a5b44-127">Cassandra Table object.</span></span>

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

### <span data-ttu-id="a5b44-128">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="a5b44-128">-KeyspaceName</span></span>
<span data-ttu-id="a5b44-129">Nome spazio tasti Cassandra.</span><span class="sxs-lookup"><span data-stu-id="a5b44-129">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="a5b44-130">-Name</span><span class="sxs-lookup"><span data-stu-id="a5b44-130">-Name</span></span>
<span data-ttu-id="a5b44-131">Nome tabella Cassandra.</span><span class="sxs-lookup"><span data-stu-id="a5b44-131">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="a5b44-132">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a5b44-132">-ParentObject</span></span>
<span data-ttu-id="a5b44-133">Oggetto Cassandra Keyspace.</span><span class="sxs-lookup"><span data-stu-id="a5b44-133">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="a5b44-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5b44-134">-ResourceGroupName</span></span>
<span data-ttu-id="a5b44-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a5b44-135">Name of resource group.</span></span>

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

### <span data-ttu-id="a5b44-136">-Schema</span><span class="sxs-lookup"><span data-stu-id="a5b44-136">-Schema</span></span>
<span data-ttu-id="a5b44-137">Oggetto PSCassandraSchema.</span><span class="sxs-lookup"><span data-stu-id="a5b44-137">PSCassandraSchema object.</span></span>
<span data-ttu-id="a5b44-138">Usare New-AzCosmosDBCassandraSchema per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a5b44-138">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

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

### <span data-ttu-id="a5b44-139">-Velocità effettiva</span><span class="sxs-lookup"><span data-stu-id="a5b44-139">-Throughput</span></span>
<span data-ttu-id="a5b44-140">Velocità effettiva di Cassandra Keyspace (RU/s).</span><span class="sxs-lookup"><span data-stu-id="a5b44-140">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="a5b44-141">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="a5b44-141">Default value is 400.</span></span>

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

### <span data-ttu-id="a5b44-142">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="a5b44-142">-TtlInSeconds</span></span>
<span data-ttu-id="a5b44-143">Ttl predefinito in secondi.</span><span class="sxs-lookup"><span data-stu-id="a5b44-143">Default Ttl in seconds.</span></span>
<span data-ttu-id="a5b44-144">Se il valore manca o è impostato su - 1, gli elementi non scadono.</span><span class="sxs-lookup"><span data-stu-id="a5b44-144">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="a5b44-145">Se il valore è impostato su n, gli elementi scadranno n secondi dopo l'ora dell'ultima modifica.</span><span class="sxs-lookup"><span data-stu-id="a5b44-145">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="a5b44-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5b44-146">-WhatIf</span></span>
<span data-ttu-id="a5b44-147">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a5b44-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5b44-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a5b44-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5b44-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5b44-149">CommonParameters</span></span>
<span data-ttu-id="a5b44-150">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5b44-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5b44-151">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a5b44-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5b44-152">INPUT</span><span class="sxs-lookup"><span data-stu-id="a5b44-152">INPUTS</span></span>

### <span data-ttu-id="a5b44-153">Microsoft.Azure.Commands.ColumnsDB.Models.PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="a5b44-153">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="a5b44-154">Microsoft.Azure.Commands.CommonsDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="a5b44-154">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="a5b44-155">Microsoft.Azure.Commands.EnterpriseDb.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="a5b44-155">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="a5b44-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a5b44-156">OUTPUTS</span></span>

### <span data-ttu-id="a5b44-157">Microsoft.Azure.Commands.EnterpriseDb.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="a5b44-157">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="a5b44-158">Microsoft.Azure.Commands.ExceptionsDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="a5b44-158">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="a5b44-159">NOTE</span><span class="sxs-lookup"><span data-stu-id="a5b44-159">NOTES</span></span>

## <span data-ttu-id="a5b44-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a5b44-160">RELATED LINKS</span></span>
