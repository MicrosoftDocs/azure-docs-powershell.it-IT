---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbcassandratablethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraTableThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraTableThroughputMigration.md
ms.openlocfilehash: 4e17e8fc2ee3b9fa82881387fa4422616b25551c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196871"
---
# <span data-ttu-id="60208-101">Invoke-AzCosmosDBCassandraTableThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="60208-101">Invoke-AzCosmosDBCassandraTableThroughputMigration</span></span>

## <span data-ttu-id="60208-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60208-102">SYNOPSIS</span></span>
<span data-ttu-id="60208-103">Consente di eseguire la migrazione della velocità effettiva della scala automatica alla velocità effettiva manuale e viceversa.</span><span class="sxs-lookup"><span data-stu-id="60208-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="60208-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="60208-104">SYNTAX</span></span>

### <span data-ttu-id="60208-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="60208-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration -KeyspaceName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60208-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="60208-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration [-Name <String>]
 -ParentObject <PSCassandraKeyspaceGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60208-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="60208-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration [-Name <String>] -InputObject <PSCassandraTableGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60208-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="60208-108">DESCRIPTION</span></span>
<span data-ttu-id="60208-109">ThroughpyteType paramter definisce la velocità effettiva a cui si vuole eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="60208-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="60208-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="60208-110">EXAMPLES</span></span>

### <span data-ttu-id="60208-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="60208-111">Example 1</span></span>
```powershell
PS C:\>$NewTable =  New-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -Name myTableName -Throughput  700 -KeyspaceName myKeyspaceName
      $AutoscaleThroughput = Invoke-AzCosmosDBCassandraTableThroughputMigration -InputObject $NewTable -ThroughputType Autoscale
```

## <span data-ttu-id="60208-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60208-112">PARAMETERS</span></span>

### <span data-ttu-id="60208-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="60208-113">-AccountName</span></span>
<span data-ttu-id="60208-114">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="60208-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="60208-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="60208-115">-Confirm</span></span>
<span data-ttu-id="60208-116">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60208-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60208-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60208-117">-DefaultProfile</span></span>
<span data-ttu-id="60208-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="60208-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60208-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60208-119">-InputObject</span></span>
<span data-ttu-id="60208-120">Oggetto Table di Cassandra.</span><span class="sxs-lookup"><span data-stu-id="60208-120">Cassandra Table object.</span></span>

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

### <span data-ttu-id="60208-121">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="60208-121">-KeyspaceName</span></span>
<span data-ttu-id="60208-122">Nome spazio tasti Cassandra.</span><span class="sxs-lookup"><span data-stu-id="60208-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="60208-123">-Name</span><span class="sxs-lookup"><span data-stu-id="60208-123">-Name</span></span>
<span data-ttu-id="60208-124">Nome tabella Cassandra.</span><span class="sxs-lookup"><span data-stu-id="60208-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="60208-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="60208-125">-ParentObject</span></span>
<span data-ttu-id="60208-126">Oggetto Cassandra Keyspace.</span><span class="sxs-lookup"><span data-stu-id="60208-126">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="60208-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60208-127">-ResourceGroupName</span></span>
<span data-ttu-id="60208-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="60208-128">Name of resource group.</span></span>

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

### <span data-ttu-id="60208-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="60208-129">-ThroughputType</span></span>
<span data-ttu-id="60208-130">Tipo di velocità effettiva di cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="60208-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="60208-131">I valori possibili sono: Scala automatica, Manuale.</span><span class="sxs-lookup"><span data-stu-id="60208-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="60208-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60208-132">-WhatIf</span></span>
<span data-ttu-id="60208-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60208-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60208-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60208-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60208-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60208-135">CommonParameters</span></span>
<span data-ttu-id="60208-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60208-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60208-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="60208-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60208-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="60208-138">INPUTS</span></span>

### <span data-ttu-id="60208-139">Microsoft.Azure.Commands.EnterpriseDb.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="60208-139">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="60208-140">Microsoft.Azure.Commands.EnterpriseDb.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="60208-140">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="60208-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="60208-141">OUTPUTS</span></span>

### <span data-ttu-id="60208-142">Microsoft.Azure.Commands.EnterpriseDb.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="60208-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="60208-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="60208-143">NOTES</span></span>

## <span data-ttu-id="60208-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="60208-144">RELATED LINKS</span></span>
