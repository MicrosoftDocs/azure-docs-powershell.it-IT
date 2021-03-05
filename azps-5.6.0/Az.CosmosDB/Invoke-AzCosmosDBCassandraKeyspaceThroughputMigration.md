---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/invoke-azcosmosdbcassandrakeyspacethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration.md
ms.openlocfilehash: d14df15f40eedab68af3d0cd6bfa0672b6283652
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977469"
---
# <span data-ttu-id="d4ee8-101">Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="d4ee8-101">Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration</span></span>

## <span data-ttu-id="d4ee8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4ee8-102">SYNOPSIS</span></span>
<span data-ttu-id="d4ee8-103">Consente di eseguire la migrazione della velocità effettiva della scala automatica alla velocità effettiva manuale e viceversa.</span><span class="sxs-lookup"><span data-stu-id="d4ee8-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="d4ee8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d4ee8-104">SYNTAX</span></span>

### <span data-ttu-id="d4ee8-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d4ee8-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d4ee8-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4ee8-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4ee8-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4ee8-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>]
 -InputObject <PSCassandraKeyspaceGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4ee8-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d4ee8-108">DESCRIPTION</span></span>
<span data-ttu-id="d4ee8-109">ThroughpyteType paramter definisce la velocità effettiva a cui si vuole eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="d4ee8-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="d4ee8-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d4ee8-110">EXAMPLES</span></span>

### <span data-ttu-id="d4ee8-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d4ee8-111">Example 1</span></span>
```powershell
PS C:\> $NewKeyspace =  New-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput  700
$AutoscaleThroughput = Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration -InputObject $NewKeyspace -ThroughputType Autoscale
```

## <span data-ttu-id="d4ee8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4ee8-112">PARAMETERS</span></span>

### <span data-ttu-id="d4ee8-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d4ee8-113">-AccountName</span></span>
<span data-ttu-id="d4ee8-114">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="d4ee8-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d4ee8-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4ee8-115">-Confirm</span></span>
<span data-ttu-id="d4ee8-116">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4ee8-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4ee8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4ee8-117">-DefaultProfile</span></span>
<span data-ttu-id="d4ee8-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d4ee8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4ee8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4ee8-119">-InputObject</span></span>
<span data-ttu-id="d4ee8-120">Oggetto Cassandra Keyspace.</span><span class="sxs-lookup"><span data-stu-id="d4ee8-120">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="d4ee8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d4ee8-121">-Name</span></span>
<span data-ttu-id="d4ee8-122">Nome spazio tasti Cassandra.</span><span class="sxs-lookup"><span data-stu-id="d4ee8-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="d4ee8-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d4ee8-123">-ParentObject</span></span>
<span data-ttu-id="d4ee8-124">Oggetto Account Aziendale</span><span class="sxs-lookup"><span data-stu-id="d4ee8-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="d4ee8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4ee8-125">-ResourceGroupName</span></span>
<span data-ttu-id="d4ee8-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d4ee8-126">Name of resource group.</span></span>

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

### <span data-ttu-id="d4ee8-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="d4ee8-127">-ThroughputType</span></span>
<span data-ttu-id="d4ee8-128">Tipo di velocità effettiva di cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="d4ee8-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="d4ee8-129">I valori possibili sono: Scala automatica, Manuale.</span><span class="sxs-lookup"><span data-stu-id="d4ee8-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="d4ee8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4ee8-130">-WhatIf</span></span>
<span data-ttu-id="d4ee8-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d4ee8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4ee8-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d4ee8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4ee8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4ee8-133">CommonParameters</span></span>
<span data-ttu-id="d4ee8-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4ee8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4ee8-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d4ee8-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4ee8-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="d4ee8-136">INPUTS</span></span>

### <span data-ttu-id="d4ee8-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="d4ee8-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="d4ee8-138">Microsoft.Azure.Commands.CommonsDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="d4ee8-138">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="d4ee8-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d4ee8-139">OUTPUTS</span></span>

### <span data-ttu-id="d4ee8-140">Microsoft.Azure.Commands.EnterpriseDb.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="d4ee8-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="d4ee8-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="d4ee8-141">NOTES</span></span>

## <span data-ttu-id="d4ee8-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d4ee8-142">RELATED LINKS</span></span>
