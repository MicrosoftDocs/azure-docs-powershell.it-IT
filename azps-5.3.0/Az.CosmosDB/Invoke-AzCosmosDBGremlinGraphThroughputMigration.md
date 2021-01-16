---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbgremlingraphthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinGraphThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinGraphThroughputMigration.md
ms.openlocfilehash: 16a477febeb5c0272f3e8cc36f577b0659f4826f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98487951"
---
# <span data-ttu-id="735af-101">Invoke-AzCosmosDBGremlinGraphThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="735af-101">Invoke-AzCosmosDBGremlinGraphThroughputMigration</span></span>

## <span data-ttu-id="735af-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="735af-102">SYNOPSIS</span></span>
<span data-ttu-id="735af-103">Usare questo comando per eseguire la migrazione della velocità di scalabilità manuale alla velocità effettiva e viceversa.</span><span class="sxs-lookup"><span data-stu-id="735af-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="735af-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="735af-104">SYNTAX</span></span>

### <span data-ttu-id="735af-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="735af-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="735af-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="735af-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="735af-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="735af-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="735af-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="735af-108">DESCRIPTION</span></span>
<span data-ttu-id="735af-109">ThroughpyteType parametro definisce la velocità effettiva a cui si vuole eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="735af-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="735af-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="735af-110">EXAMPLES</span></span>

### <span data-ttu-id="735af-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="735af-111">Example 1</span></span>
```powershell
PS C:\>  $NewGraph =  New-AzCosmosDBGremlinGraph -AccountName myAccountName -ResourceGroupName myRgName -Name myGraphName -Throughput 700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBGremlinGraphThroughputMigration -InputObject $NewGraph -ThroughputType Autoscale
```


## <span data-ttu-id="735af-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="735af-112">PARAMETERS</span></span>

### <span data-ttu-id="735af-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="735af-113">-AccountName</span></span>
<span data-ttu-id="735af-114">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="735af-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="735af-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="735af-115">-Confirm</span></span>
<span data-ttu-id="735af-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="735af-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="735af-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="735af-117">-DatabaseName</span></span>
<span data-ttu-id="735af-118">Nome database.</span><span class="sxs-lookup"><span data-stu-id="735af-118">Database name.</span></span>

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

### <span data-ttu-id="735af-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="735af-119">-DefaultProfile</span></span>
<span data-ttu-id="735af-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="735af-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="735af-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="735af-121">-InputObject</span></span>
<span data-ttu-id="735af-122">Oggetto grafico Gremlin.</span><span class="sxs-lookup"><span data-stu-id="735af-122">Gremlin Graph object.</span></span>

```yaml
Type: PSGremlinGraphGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="735af-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="735af-123">-Name</span></span>
<span data-ttu-id="735af-124">Nome del grafico Gremlin.</span><span class="sxs-lookup"><span data-stu-id="735af-124">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="735af-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="735af-125">-ParentObject</span></span>
<span data-ttu-id="735af-126">Oggetto database Gremlin.</span><span class="sxs-lookup"><span data-stu-id="735af-126">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="735af-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="735af-127">-ResourceGroupName</span></span>
<span data-ttu-id="735af-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="735af-128">Name of resource group.</span></span>

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

### <span data-ttu-id="735af-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="735af-129">-ThroughputType</span></span>
<span data-ttu-id="735af-130">Tipo di throughput a cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="735af-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="735af-131">I valori possibili sono: scala, manuale.</span><span class="sxs-lookup"><span data-stu-id="735af-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="735af-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="735af-132">-WhatIf</span></span>
<span data-ttu-id="735af-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="735af-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="735af-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="735af-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="735af-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="735af-135">CommonParameters</span></span>
<span data-ttu-id="735af-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="735af-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="735af-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="735af-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="735af-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="735af-138">INPUTS</span></span>

### <span data-ttu-id="735af-139">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="735af-139">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="735af-140">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="735af-140">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="735af-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="735af-141">OUTPUTS</span></span>

### <span data-ttu-id="735af-142">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="735af-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="735af-143">Note</span><span class="sxs-lookup"><span data-stu-id="735af-143">NOTES</span></span>

## <span data-ttu-id="735af-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="735af-144">RELATED LINKS</span></span>
