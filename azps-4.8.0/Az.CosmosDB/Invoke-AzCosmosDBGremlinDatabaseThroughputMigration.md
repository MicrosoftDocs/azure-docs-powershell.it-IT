---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbgremlindatabasethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinDatabaseThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinDatabaseThroughputMigration.md
ms.openlocfilehash: 84039f883937354cf8c8fae3c99bfbc6f73bb574
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190526"
---
# <span data-ttu-id="5b892-101">Invoke-AzCosmosDBGremlinDatabaseThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="5b892-101">Invoke-AzCosmosDBGremlinDatabaseThroughputMigration</span></span>

## <span data-ttu-id="5b892-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5b892-102">SYNOPSIS</span></span>
<span data-ttu-id="5b892-103">Usare questo comando per eseguire la migrazione della velocità di scalabilità manuale alla velocità effettiva e viceversa.</span><span class="sxs-lookup"><span data-stu-id="5b892-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="5b892-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5b892-104">SYNTAX</span></span>

### <span data-ttu-id="5b892-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5b892-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBGremlinDatabaseThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5b892-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b892-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinDatabaseThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b892-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b892-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinDatabaseThroughputMigration [-Name <String>] -InputObject <PSGremlinDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b892-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5b892-108">DESCRIPTION</span></span>
<span data-ttu-id="5b892-109">ThroughpyteType parametro definisce la velocità effettiva a cui si vuole eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="5b892-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="5b892-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5b892-110">EXAMPLES</span></span>

### <span data-ttu-id="5b892-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5b892-111">Example 1</span></span>
```powershell
PS C:\> $NewDb =  New-AzCosmosDBGremlinDatabase -AccountName myAccountName -ResourceGroupName myRgName -Name myDbName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBGremlinDatabaseThroughputMigration -InputObject $NewDb -ThroughputType Autoscale
```


## <span data-ttu-id="5b892-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5b892-112">PARAMETERS</span></span>

### <span data-ttu-id="5b892-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5b892-113">-AccountName</span></span>
<span data-ttu-id="5b892-114">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="5b892-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5b892-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5b892-115">-Confirm</span></span>
<span data-ttu-id="5b892-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b892-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b892-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b892-117">-DefaultProfile</span></span>
<span data-ttu-id="5b892-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5b892-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b892-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b892-119">-InputObject</span></span>
<span data-ttu-id="5b892-120">Oggetto database Gremlin.</span><span class="sxs-lookup"><span data-stu-id="5b892-120">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b892-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="5b892-121">-Name</span></span>
<span data-ttu-id="5b892-122">Nome database.</span><span class="sxs-lookup"><span data-stu-id="5b892-122">Database name.</span></span>

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

### <span data-ttu-id="5b892-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5b892-123">-ParentObject</span></span>
<span data-ttu-id="5b892-124">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="5b892-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="5b892-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b892-125">-ResourceGroupName</span></span>
<span data-ttu-id="5b892-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5b892-126">Name of resource group.</span></span>

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

### <span data-ttu-id="5b892-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="5b892-127">-ThroughputType</span></span>
<span data-ttu-id="5b892-128">Tipo di throughput a cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="5b892-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="5b892-129">I valori possibili sono: scala, manuale.</span><span class="sxs-lookup"><span data-stu-id="5b892-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="5b892-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b892-130">-WhatIf</span></span>
<span data-ttu-id="5b892-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5b892-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b892-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5b892-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b892-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b892-133">CommonParameters</span></span>
<span data-ttu-id="5b892-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b892-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b892-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5b892-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b892-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5b892-136">INPUTS</span></span>

### <span data-ttu-id="5b892-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="5b892-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="5b892-138">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="5b892-138">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="5b892-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5b892-139">OUTPUTS</span></span>

### <span data-ttu-id="5b892-140">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="5b892-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="5b892-141">Note</span><span class="sxs-lookup"><span data-stu-id="5b892-141">NOTES</span></span>

## <span data-ttu-id="5b892-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5b892-142">RELATED LINKS</span></span>
