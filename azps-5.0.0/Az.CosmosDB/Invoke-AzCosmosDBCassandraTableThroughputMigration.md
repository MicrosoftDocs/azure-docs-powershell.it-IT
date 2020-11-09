---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbcassandratablethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraTableThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraTableThroughputMigration.md
ms.openlocfilehash: b6199720d9ac59c608482632518b47829a7c0b9d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299448"
---
# <span data-ttu-id="848e0-101">Invoke-AzCosmosDBCassandraTableThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="848e0-101">Invoke-AzCosmosDBCassandraTableThroughputMigration</span></span>

## <span data-ttu-id="848e0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="848e0-102">SYNOPSIS</span></span>
<span data-ttu-id="848e0-103">Usare questo comando per eseguire la migrazione della velocità di scalabilità manuale alla velocità effettiva e viceversa.</span><span class="sxs-lookup"><span data-stu-id="848e0-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="848e0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="848e0-104">SYNTAX</span></span>

### <span data-ttu-id="848e0-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="848e0-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration -KeyspaceName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="848e0-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="848e0-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration [-Name <String>]
 -ParentObject <PSCassandraKeyspaceGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="848e0-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="848e0-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration [-Name <String>] -InputObject <PSCassandraTableGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="848e0-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="848e0-108">DESCRIPTION</span></span>
<span data-ttu-id="848e0-109">ThroughpyteType parametro definisce la velocità effettiva a cui si vuole eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="848e0-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="848e0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="848e0-110">EXAMPLES</span></span>

### <span data-ttu-id="848e0-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="848e0-111">Example 1</span></span>
```powershell
PS C:\>$NewTable =  New-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -Name myTableName -Throughput  700 -KeyspaceName myKeyspaceName
      $AutoscaleThroughput = Invoke-AzCosmosDBCassandraTableThroughputMigration -InputObject $NewTable -ThroughputType Autoscale
```


## <span data-ttu-id="848e0-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="848e0-112">PARAMETERS</span></span>

### <span data-ttu-id="848e0-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="848e0-113">-AccountName</span></span>
<span data-ttu-id="848e0-114">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="848e0-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="848e0-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="848e0-115">-Confirm</span></span>
<span data-ttu-id="848e0-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="848e0-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="848e0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="848e0-117">-DefaultProfile</span></span>
<span data-ttu-id="848e0-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="848e0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="848e0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="848e0-119">-InputObject</span></span>
<span data-ttu-id="848e0-120">Oggetto tabella Cassandra.</span><span class="sxs-lookup"><span data-stu-id="848e0-120">Cassandra Table object.</span></span>

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

### <span data-ttu-id="848e0-121">-Barra spaziatrice</span><span class="sxs-lookup"><span data-stu-id="848e0-121">-KeyspaceName</span></span>
<span data-ttu-id="848e0-122">Nome della barra spaziatrice Cassandra.</span><span class="sxs-lookup"><span data-stu-id="848e0-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="848e0-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="848e0-123">-Name</span></span>
<span data-ttu-id="848e0-124">Nome tabella Cassandra.</span><span class="sxs-lookup"><span data-stu-id="848e0-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="848e0-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="848e0-125">-ParentObject</span></span>
<span data-ttu-id="848e0-126">Oggetto portaspazio Cassandra.</span><span class="sxs-lookup"><span data-stu-id="848e0-126">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="848e0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="848e0-127">-ResourceGroupName</span></span>
<span data-ttu-id="848e0-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="848e0-128">Name of resource group.</span></span>

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

### <span data-ttu-id="848e0-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="848e0-129">-ThroughputType</span></span>
<span data-ttu-id="848e0-130">Tipo di throughput a cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="848e0-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="848e0-131">I valori possibili sono: scala, manuale.</span><span class="sxs-lookup"><span data-stu-id="848e0-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="848e0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="848e0-132">-WhatIf</span></span>
<span data-ttu-id="848e0-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="848e0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="848e0-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="848e0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="848e0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="848e0-135">CommonParameters</span></span>
<span data-ttu-id="848e0-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="848e0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="848e0-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="848e0-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="848e0-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="848e0-138">INPUTS</span></span>

### <span data-ttu-id="848e0-139">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="848e0-139">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="848e0-140">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="848e0-140">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="848e0-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="848e0-141">OUTPUTS</span></span>

### <span data-ttu-id="848e0-142">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="848e0-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="848e0-143">Note</span><span class="sxs-lookup"><span data-stu-id="848e0-143">NOTES</span></span>

## <span data-ttu-id="848e0-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="848e0-144">RELATED LINKS</span></span>
