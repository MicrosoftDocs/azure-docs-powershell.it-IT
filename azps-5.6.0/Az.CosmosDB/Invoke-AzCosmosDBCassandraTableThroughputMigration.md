---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/invoke-azcosmosdbcassandratablethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraTableThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraTableThroughputMigration.md
ms.openlocfilehash: 65b1cbaebdf4118b5e22a7d1f9672273281ba55b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992835"
---
# <span data-ttu-id="34458-101">Invoke-AzCosmosDBCassandraTableThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="34458-101">Invoke-AzCosmosDBCassandraTableThroughputMigration</span></span>

## <span data-ttu-id="34458-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34458-102">SYNOPSIS</span></span>
<span data-ttu-id="34458-103">Consente di eseguire la migrazione della velocità effettiva della scala automatica alla velocità effettiva manuale e viceversa.</span><span class="sxs-lookup"><span data-stu-id="34458-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="34458-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="34458-104">SYNTAX</span></span>

### <span data-ttu-id="34458-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="34458-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration -KeyspaceName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34458-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="34458-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration [-Name <String>]
 -ParentObject <PSCassandraKeyspaceGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34458-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="34458-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration [-Name <String>] -InputObject <PSCassandraTableGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34458-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="34458-108">DESCRIPTION</span></span>
<span data-ttu-id="34458-109">ThroughpyteType paramter definisce la velocità effettiva a cui si vuole eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="34458-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="34458-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="34458-110">EXAMPLES</span></span>

### <span data-ttu-id="34458-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="34458-111">Example 1</span></span>
```powershell
PS C:\>$NewTable =  New-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -Name myTableName -Throughput  700 -KeyspaceName myKeyspaceName
      $AutoscaleThroughput = Invoke-AzCosmosDBCassandraTableThroughputMigration -InputObject $NewTable -ThroughputType Autoscale
```

## <span data-ttu-id="34458-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34458-112">PARAMETERS</span></span>

### <span data-ttu-id="34458-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="34458-113">-AccountName</span></span>
<span data-ttu-id="34458-114">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="34458-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="34458-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="34458-115">-Confirm</span></span>
<span data-ttu-id="34458-116">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34458-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34458-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34458-117">-DefaultProfile</span></span>
<span data-ttu-id="34458-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="34458-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34458-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34458-119">-InputObject</span></span>
<span data-ttu-id="34458-120">Oggetto Table di Cassandra.</span><span class="sxs-lookup"><span data-stu-id="34458-120">Cassandra Table object.</span></span>

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

### <span data-ttu-id="34458-121">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="34458-121">-KeyspaceName</span></span>
<span data-ttu-id="34458-122">Nome spazio tasti Cassandra.</span><span class="sxs-lookup"><span data-stu-id="34458-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="34458-123">-Name</span><span class="sxs-lookup"><span data-stu-id="34458-123">-Name</span></span>
<span data-ttu-id="34458-124">Nome tabella Cassandra.</span><span class="sxs-lookup"><span data-stu-id="34458-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="34458-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="34458-125">-ParentObject</span></span>
<span data-ttu-id="34458-126">Oggetto Cassandra Keyspace.</span><span class="sxs-lookup"><span data-stu-id="34458-126">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="34458-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34458-127">-ResourceGroupName</span></span>
<span data-ttu-id="34458-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="34458-128">Name of resource group.</span></span>

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

### <span data-ttu-id="34458-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="34458-129">-ThroughputType</span></span>
<span data-ttu-id="34458-130">Tipo di velocità effettiva di cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="34458-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="34458-131">I valori possibili sono: Scala automatica, Manuale.</span><span class="sxs-lookup"><span data-stu-id="34458-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="34458-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34458-132">-WhatIf</span></span>
<span data-ttu-id="34458-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="34458-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34458-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="34458-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34458-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34458-135">CommonParameters</span></span>
<span data-ttu-id="34458-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34458-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34458-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="34458-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34458-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="34458-138">INPUTS</span></span>

### <span data-ttu-id="34458-139">Microsoft.Azure.Commands.CommonsDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="34458-139">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="34458-140">Microsoft.Azure.Commands.EnterpriseDb.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="34458-140">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="34458-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="34458-141">OUTPUTS</span></span>

### <span data-ttu-id="34458-142">Microsoft.Azure.Commands.EnterpriseDb.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="34458-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="34458-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="34458-143">NOTES</span></span>

## <span data-ttu-id="34458-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="34458-144">RELATED LINKS</span></span>
