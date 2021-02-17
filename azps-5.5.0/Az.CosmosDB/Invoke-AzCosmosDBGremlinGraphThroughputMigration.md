---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbgremlingraphthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinGraphThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinGraphThroughputMigration.md
ms.openlocfilehash: 16817d4af40ddd27a8838f40618758686af26a58
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196855"
---
# <span data-ttu-id="a144b-101">Invoke-AzCosmosDBGremlinGraphThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="a144b-101">Invoke-AzCosmosDBGremlinGraphThroughputMigration</span></span>

## <span data-ttu-id="a144b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a144b-102">SYNOPSIS</span></span>
<span data-ttu-id="a144b-103">Consente di eseguire la migrazione della velocità effettiva della scala automatica alla velocità effettiva manuale e viceversa.</span><span class="sxs-lookup"><span data-stu-id="a144b-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="a144b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a144b-104">SYNTAX</span></span>

### <span data-ttu-id="a144b-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a144b-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a144b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a144b-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a144b-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a144b-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a144b-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a144b-108">DESCRIPTION</span></span>
<span data-ttu-id="a144b-109">ThroughpyteType paramter definisce la velocità effettiva a cui si vuole eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="a144b-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="a144b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a144b-110">EXAMPLES</span></span>

### <span data-ttu-id="a144b-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a144b-111">Example 1</span></span>
```powershell
PS C:\>  $NewGraph =  New-AzCosmosDBGremlinGraph -AccountName myAccountName -ResourceGroupName myRgName -Name myGraphName -Throughput 700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBGremlinGraphThroughputMigration -InputObject $NewGraph -ThroughputType Autoscale
```

## <span data-ttu-id="a144b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a144b-112">PARAMETERS</span></span>

### <span data-ttu-id="a144b-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a144b-113">-AccountName</span></span>
<span data-ttu-id="a144b-114">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="a144b-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a144b-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a144b-115">-Confirm</span></span>
<span data-ttu-id="a144b-116">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a144b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a144b-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a144b-117">-DatabaseName</span></span>
<span data-ttu-id="a144b-118">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="a144b-118">Database name.</span></span>

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

### <span data-ttu-id="a144b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a144b-119">-DefaultProfile</span></span>
<span data-ttu-id="a144b-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a144b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a144b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a144b-121">-InputObject</span></span>
<span data-ttu-id="a144b-122">Oggetto Gremlin Graph.</span><span class="sxs-lookup"><span data-stu-id="a144b-122">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="a144b-123">-Name</span><span class="sxs-lookup"><span data-stu-id="a144b-123">-Name</span></span>
<span data-ttu-id="a144b-124">Nome del grafo Gremlin.</span><span class="sxs-lookup"><span data-stu-id="a144b-124">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="a144b-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a144b-125">-ParentObject</span></span>
<span data-ttu-id="a144b-126">Oggetto di database Gremlin.</span><span class="sxs-lookup"><span data-stu-id="a144b-126">Gremlin Database object.</span></span>

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

### <span data-ttu-id="a144b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a144b-127">-ResourceGroupName</span></span>
<span data-ttu-id="a144b-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a144b-128">Name of resource group.</span></span>

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

### <span data-ttu-id="a144b-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="a144b-129">-ThroughputType</span></span>
<span data-ttu-id="a144b-130">Tipo di velocità effettiva di cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="a144b-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="a144b-131">I valori possibili sono: Scala automatica, Manuale.</span><span class="sxs-lookup"><span data-stu-id="a144b-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="a144b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a144b-132">-WhatIf</span></span>
<span data-ttu-id="a144b-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a144b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a144b-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a144b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a144b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a144b-135">CommonParameters</span></span>
<span data-ttu-id="a144b-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a144b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a144b-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a144b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a144b-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="a144b-138">INPUTS</span></span>

### <span data-ttu-id="a144b-139">Microsoft.Azure.Commands.EnterpriseDb.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="a144b-139">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="a144b-140">Microsoft.Azure.Commands.EnterpriseDb.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="a144b-140">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="a144b-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a144b-141">OUTPUTS</span></span>

### <span data-ttu-id="a144b-142">Microsoft.Azure.Commands.EnterpriseDb.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="a144b-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="a144b-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="a144b-143">NOTES</span></span>

## <span data-ttu-id="a144b-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a144b-144">RELATED LINKS</span></span>
