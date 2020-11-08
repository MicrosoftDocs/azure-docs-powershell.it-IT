---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbcassandrakeyspacethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration.md
ms.openlocfilehash: a5e636f37b032411069b3e6c9a85226eb751705e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192157"
---
# <span data-ttu-id="81c79-101">Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="81c79-101">Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration</span></span>

## <span data-ttu-id="81c79-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="81c79-102">SYNOPSIS</span></span>
<span data-ttu-id="81c79-103">Usare questo comando per eseguire la migrazione della velocità di scalabilità manuale alla velocità effettiva e viceversa.</span><span class="sxs-lookup"><span data-stu-id="81c79-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="81c79-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="81c79-104">SYNTAX</span></span>

### <span data-ttu-id="81c79-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="81c79-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="81c79-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="81c79-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81c79-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="81c79-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>]
 -InputObject <PSCassandraKeyspaceGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81c79-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="81c79-108">DESCRIPTION</span></span>
<span data-ttu-id="81c79-109">ThroughpyteType parametro definisce la velocità effettiva a cui si vuole eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="81c79-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="81c79-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="81c79-110">EXAMPLES</span></span>

### <span data-ttu-id="81c79-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="81c79-111">Example 1</span></span>
```powershell
PS C:\> $NewKeyspace =  New-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput  700
$AutoscaleThroughput = Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration -InputObject $NewKeyspace -ThroughputType Autoscale
```

## <span data-ttu-id="81c79-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="81c79-112">PARAMETERS</span></span>

### <span data-ttu-id="81c79-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="81c79-113">-AccountName</span></span>
<span data-ttu-id="81c79-114">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="81c79-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="81c79-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="81c79-115">-Confirm</span></span>
<span data-ttu-id="81c79-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81c79-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81c79-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81c79-117">-DefaultProfile</span></span>
<span data-ttu-id="81c79-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="81c79-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81c79-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81c79-119">-InputObject</span></span>
<span data-ttu-id="81c79-120">Oggetto portaspazio Cassandra.</span><span class="sxs-lookup"><span data-stu-id="81c79-120">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="81c79-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="81c79-121">-Name</span></span>
<span data-ttu-id="81c79-122">Nome della barra spaziatrice Cassandra.</span><span class="sxs-lookup"><span data-stu-id="81c79-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="81c79-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="81c79-123">-ParentObject</span></span>
<span data-ttu-id="81c79-124">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="81c79-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="81c79-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81c79-125">-ResourceGroupName</span></span>
<span data-ttu-id="81c79-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="81c79-126">Name of resource group.</span></span>

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

### <span data-ttu-id="81c79-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="81c79-127">-ThroughputType</span></span>
<span data-ttu-id="81c79-128">Tipo di throughput a cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="81c79-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="81c79-129">I valori possibili sono: scala, manuale.</span><span class="sxs-lookup"><span data-stu-id="81c79-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="81c79-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81c79-130">-WhatIf</span></span>
<span data-ttu-id="81c79-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="81c79-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81c79-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="81c79-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81c79-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81c79-133">CommonParameters</span></span>
<span data-ttu-id="81c79-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81c79-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81c79-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81c79-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81c79-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="81c79-136">INPUTS</span></span>

### <span data-ttu-id="81c79-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="81c79-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="81c79-138">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="81c79-138">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="81c79-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="81c79-139">OUTPUTS</span></span>

### <span data-ttu-id="81c79-140">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="81c79-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="81c79-141">Note</span><span class="sxs-lookup"><span data-stu-id="81c79-141">NOTES</span></span>

## <span data-ttu-id="81c79-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="81c79-142">RELATED LINKS</span></span>