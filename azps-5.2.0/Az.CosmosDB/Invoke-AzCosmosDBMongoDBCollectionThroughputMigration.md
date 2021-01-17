---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbmongodbcollectionthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBCollectionThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBCollectionThroughputMigration.md
ms.openlocfilehash: e2f1449536f9b4db5b743c1a1e352e427ae86821
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343471"
---
# <span data-ttu-id="34d4f-101">Invoke-AzCosmosDBMongoDBCollectionThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="34d4f-101">Invoke-AzCosmosDBMongoDBCollectionThroughputMigration</span></span>

## <span data-ttu-id="34d4f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="34d4f-102">SYNOPSIS</span></span>
<span data-ttu-id="34d4f-103">Usare questo comando per eseguire la migrazione della velocità di scalabilità manuale alla velocità effettiva e viceversa.</span><span class="sxs-lookup"><span data-stu-id="34d4f-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="34d4f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="34d4f-104">SYNTAX</span></span>

### <span data-ttu-id="34d4f-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="34d4f-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34d4f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="34d4f-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration [-Name <String>]
 -ParentObject <PSMongoDBDatabaseGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34d4f-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="34d4f-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration [-Name <String>]
 -InputObject <PSMongoDBCollectionGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34d4f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34d4f-108">DESCRIPTION</span></span>
<span data-ttu-id="34d4f-109">ThroughpyteType parametro definisce la velocità effettiva a cui si vuole eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="34d4f-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="34d4f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="34d4f-110">EXAMPLES</span></span>

### <span data-ttu-id="34d4f-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="34d4f-111">Example 1</span></span>
```powershell
PS C:\> $NewCollection =  New-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -Name myCollectionName -Throughput  700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBMongoDBCollectionThroughputMigration -InputObject $NewCollection -ThroughputType Autoscale
```


## <span data-ttu-id="34d4f-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="34d4f-112">PARAMETERS</span></span>

### <span data-ttu-id="34d4f-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="34d4f-113">-AccountName</span></span>
<span data-ttu-id="34d4f-114">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="34d4f-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="34d4f-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="34d4f-115">-Confirm</span></span>
<span data-ttu-id="34d4f-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34d4f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34d4f-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="34d4f-117">-DatabaseName</span></span>
<span data-ttu-id="34d4f-118">Nome database.</span><span class="sxs-lookup"><span data-stu-id="34d4f-118">Database name.</span></span>

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

### <span data-ttu-id="34d4f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34d4f-119">-DefaultProfile</span></span>
<span data-ttu-id="34d4f-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="34d4f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34d4f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34d4f-121">-InputObject</span></span>
<span data-ttu-id="34d4f-122">Oggetto raccolta Mongo.</span><span class="sxs-lookup"><span data-stu-id="34d4f-122">Mongo Collection object.</span></span>

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

### <span data-ttu-id="34d4f-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="34d4f-123">-Name</span></span>
<span data-ttu-id="34d4f-124">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="34d4f-124">Collection name.</span></span>

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

### <span data-ttu-id="34d4f-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="34d4f-125">-ParentObject</span></span>
<span data-ttu-id="34d4f-126">Oggetto di database Mongo.</span><span class="sxs-lookup"><span data-stu-id="34d4f-126">Mongo Database object.</span></span>

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

### <span data-ttu-id="34d4f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34d4f-127">-ResourceGroupName</span></span>
<span data-ttu-id="34d4f-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="34d4f-128">Name of resource group.</span></span>

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

### <span data-ttu-id="34d4f-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="34d4f-129">-ThroughputType</span></span>
<span data-ttu-id="34d4f-130">Tipo di throughput a cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="34d4f-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="34d4f-131">I valori possibili sono: scala, manuale.</span><span class="sxs-lookup"><span data-stu-id="34d4f-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="34d4f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34d4f-132">-WhatIf</span></span>
<span data-ttu-id="34d4f-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="34d4f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34d4f-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="34d4f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34d4f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34d4f-135">CommonParameters</span></span>
<span data-ttu-id="34d4f-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34d4f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34d4f-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="34d4f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34d4f-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="34d4f-138">INPUTS</span></span>

### <span data-ttu-id="34d4f-139">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="34d4f-139">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="34d4f-140">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="34d4f-140">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="34d4f-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="34d4f-141">OUTPUTS</span></span>

### <span data-ttu-id="34d4f-142">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="34d4f-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="34d4f-143">Note</span><span class="sxs-lookup"><span data-stu-id="34d4f-143">NOTES</span></span>

## <span data-ttu-id="34d4f-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="34d4f-144">RELATED LINKS</span></span>
