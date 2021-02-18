---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbcassandrakeyspacethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration.md
ms.openlocfilehash: a5e636f37b032411069b3e6c9a85226eb751705e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181342"
---
# <span data-ttu-id="7fac9-101">Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="7fac9-101">Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration</span></span>

## <span data-ttu-id="7fac9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fac9-102">SYNOPSIS</span></span>
<span data-ttu-id="7fac9-103">Consente di eseguire la migrazione della velocità effettiva della scala automatica alla velocità effettiva manuale e viceversa.</span><span class="sxs-lookup"><span data-stu-id="7fac9-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="7fac9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7fac9-104">SYNTAX</span></span>

### <span data-ttu-id="7fac9-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7fac9-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7fac9-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fac9-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fac9-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fac9-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>]
 -InputObject <PSCassandraKeyspaceGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fac9-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7fac9-108">DESCRIPTION</span></span>
<span data-ttu-id="7fac9-109">ThroughpyteType paramter definisce la velocità effettiva a cui si vuole eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="7fac9-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="7fac9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7fac9-110">EXAMPLES</span></span>

### <span data-ttu-id="7fac9-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7fac9-111">Example 1</span></span>
```powershell
PS C:\> $NewKeyspace =  New-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput  700
$AutoscaleThroughput = Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration -InputObject $NewKeyspace -ThroughputType Autoscale
```

## <span data-ttu-id="7fac9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7fac9-112">PARAMETERS</span></span>

### <span data-ttu-id="7fac9-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7fac9-113">-AccountName</span></span>
<span data-ttu-id="7fac9-114">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="7fac9-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7fac9-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7fac9-115">-Confirm</span></span>
<span data-ttu-id="7fac9-116">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7fac9-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fac9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fac9-117">-DefaultProfile</span></span>
<span data-ttu-id="7fac9-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7fac9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fac9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7fac9-119">-InputObject</span></span>
<span data-ttu-id="7fac9-120">Oggetto Cassandra Keyspace.</span><span class="sxs-lookup"><span data-stu-id="7fac9-120">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="7fac9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7fac9-121">-Name</span></span>
<span data-ttu-id="7fac9-122">Nome spazio tasti Cassandra.</span><span class="sxs-lookup"><span data-stu-id="7fac9-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="7fac9-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7fac9-123">-ParentObject</span></span>
<span data-ttu-id="7fac9-124">Oggetto AccountDb Disa</span><span class="sxs-lookup"><span data-stu-id="7fac9-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="7fac9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fac9-125">-ResourceGroupName</span></span>
<span data-ttu-id="7fac9-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7fac9-126">Name of resource group.</span></span>

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

### <span data-ttu-id="7fac9-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="7fac9-127">-ThroughputType</span></span>
<span data-ttu-id="7fac9-128">Tipo di velocità effettiva di cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="7fac9-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="7fac9-129">I valori possibili sono: Scala automatica, Manuale.</span><span class="sxs-lookup"><span data-stu-id="7fac9-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="7fac9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fac9-130">-WhatIf</span></span>
<span data-ttu-id="7fac9-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7fac9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fac9-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7fac9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fac9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fac9-133">CommonParameters</span></span>
<span data-ttu-id="7fac9-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fac9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fac9-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7fac9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fac9-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="7fac9-136">INPUTS</span></span>

### <span data-ttu-id="7fac9-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="7fac9-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="7fac9-138">Microsoft.Azure.Commands.EnterpriseDb.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="7fac9-138">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="7fac9-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7fac9-139">OUTPUTS</span></span>

### <span data-ttu-id="7fac9-140">Microsoft.Azure.Commands.EnterpriseDb.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="7fac9-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="7fac9-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="7fac9-141">NOTES</span></span>

## <span data-ttu-id="7fac9-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7fac9-142">RELATED LINKS</span></span>
