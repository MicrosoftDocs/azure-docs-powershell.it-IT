---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbmongodbcollectionthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBCollectionThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBCollectionThroughputMigration.md
ms.openlocfilehash: e2f1449536f9b4db5b743c1a1e352e427ae86821
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299431"
---
# <span data-ttu-id="9b63e-101">Invoke-AzCosmosDBMongoDBCollectionThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="9b63e-101">Invoke-AzCosmosDBMongoDBCollectionThroughputMigration</span></span>

## <span data-ttu-id="9b63e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9b63e-102">SYNOPSIS</span></span>
<span data-ttu-id="9b63e-103">Usare questo comando per eseguire la migrazione della velocità di scalabilità manuale alla velocità effettiva e viceversa.</span><span class="sxs-lookup"><span data-stu-id="9b63e-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="9b63e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9b63e-104">SYNTAX</span></span>

### <span data-ttu-id="9b63e-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9b63e-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b63e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b63e-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration [-Name <String>]
 -ParentObject <PSMongoDBDatabaseGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b63e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b63e-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration [-Name <String>]
 -InputObject <PSMongoDBCollectionGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b63e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9b63e-108">DESCRIPTION</span></span>
<span data-ttu-id="9b63e-109">ThroughpyteType parametro definisce la velocità effettiva a cui si vuole eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="9b63e-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="9b63e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9b63e-110">EXAMPLES</span></span>

### <span data-ttu-id="9b63e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9b63e-111">Example 1</span></span>
```powershell
PS C:\> $NewCollection =  New-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -Name myCollectionName -Throughput  700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBMongoDBCollectionThroughputMigration -InputObject $NewCollection -ThroughputType Autoscale
```


## <span data-ttu-id="9b63e-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9b63e-112">PARAMETERS</span></span>

### <span data-ttu-id="9b63e-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9b63e-113">-AccountName</span></span>
<span data-ttu-id="9b63e-114">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="9b63e-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9b63e-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9b63e-115">-Confirm</span></span>
<span data-ttu-id="9b63e-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b63e-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b63e-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9b63e-117">-DatabaseName</span></span>
<span data-ttu-id="9b63e-118">Nome database.</span><span class="sxs-lookup"><span data-stu-id="9b63e-118">Database name.</span></span>

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

### <span data-ttu-id="9b63e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b63e-119">-DefaultProfile</span></span>
<span data-ttu-id="9b63e-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9b63e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b63e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b63e-121">-InputObject</span></span>
<span data-ttu-id="9b63e-122">Oggetto raccolta Mongo.</span><span class="sxs-lookup"><span data-stu-id="9b63e-122">Mongo Collection object.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b63e-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="9b63e-123">-Name</span></span>
<span data-ttu-id="9b63e-124">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="9b63e-124">Collection name.</span></span>

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

### <span data-ttu-id="9b63e-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9b63e-125">-ParentObject</span></span>
<span data-ttu-id="9b63e-126">Oggetto di database Mongo.</span><span class="sxs-lookup"><span data-stu-id="9b63e-126">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b63e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b63e-127">-ResourceGroupName</span></span>
<span data-ttu-id="9b63e-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9b63e-128">Name of resource group.</span></span>

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

### <span data-ttu-id="9b63e-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="9b63e-129">-ThroughputType</span></span>
<span data-ttu-id="9b63e-130">Tipo di throughput a cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="9b63e-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="9b63e-131">I valori possibili sono: scala, manuale.</span><span class="sxs-lookup"><span data-stu-id="9b63e-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="9b63e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b63e-132">-WhatIf</span></span>
<span data-ttu-id="9b63e-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9b63e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b63e-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9b63e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b63e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b63e-135">CommonParameters</span></span>
<span data-ttu-id="9b63e-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b63e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b63e-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9b63e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b63e-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9b63e-138">INPUTS</span></span>

### <span data-ttu-id="9b63e-139">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="9b63e-139">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="9b63e-140">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="9b63e-140">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="9b63e-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9b63e-141">OUTPUTS</span></span>

### <span data-ttu-id="9b63e-142">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="9b63e-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="9b63e-143">Note</span><span class="sxs-lookup"><span data-stu-id="9b63e-143">NOTES</span></span>

## <span data-ttu-id="9b63e-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9b63e-144">RELATED LINKS</span></span>
