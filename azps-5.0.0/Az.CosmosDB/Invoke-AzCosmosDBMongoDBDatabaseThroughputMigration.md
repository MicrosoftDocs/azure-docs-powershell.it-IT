---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbmongodbdatabasethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration.md
ms.openlocfilehash: 1ba30d016b2ff8b143987961d08d68eacca16890
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299430"
---
# <span data-ttu-id="e90c2-101">Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="e90c2-101">Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration</span></span>

## <span data-ttu-id="e90c2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e90c2-102">SYNOPSIS</span></span>
<span data-ttu-id="e90c2-103">Usare questo comando per eseguire la migrazione della velocità di scalabilità manuale alla velocità effettiva e viceversa.</span><span class="sxs-lookup"><span data-stu-id="e90c2-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="e90c2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e90c2-104">SYNTAX</span></span>

### <span data-ttu-id="e90c2-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e90c2-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e90c2-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e90c2-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e90c2-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e90c2-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>] -InputObject <PSMongoDBDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e90c2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e90c2-108">DESCRIPTION</span></span>
<span data-ttu-id="e90c2-109">ThroughpyteType parametro definisce la velocità effettiva a cui si vuole eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="e90c2-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="e90c2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e90c2-110">EXAMPLES</span></span>

### <span data-ttu-id="e90c2-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e90c2-111">Example 1</span></span>
```powershell
PS C:\>$NewMongodbDatabase =  New-AzCosmosDBMongoDBDatabase -AccountName myAccountName -ResourceGroupName myRgName -Name myDbName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration -InputObject $NewMongodbDatabase -ThroughputType Autoscale
```


## <span data-ttu-id="e90c2-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e90c2-112">PARAMETERS</span></span>

### <span data-ttu-id="e90c2-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e90c2-113">-AccountName</span></span>
<span data-ttu-id="e90c2-114">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="e90c2-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e90c2-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e90c2-115">-Confirm</span></span>
<span data-ttu-id="e90c2-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e90c2-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e90c2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e90c2-117">-DefaultProfile</span></span>
<span data-ttu-id="e90c2-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e90c2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e90c2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e90c2-119">-InputObject</span></span>
<span data-ttu-id="e90c2-120">Oggetto di database Mongo.</span><span class="sxs-lookup"><span data-stu-id="e90c2-120">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e90c2-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="e90c2-121">-Name</span></span>
<span data-ttu-id="e90c2-122">Nome database.</span><span class="sxs-lookup"><span data-stu-id="e90c2-122">Database name.</span></span>

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

### <span data-ttu-id="e90c2-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e90c2-123">-ParentObject</span></span>
<span data-ttu-id="e90c2-124">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="e90c2-124">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e90c2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e90c2-125">-ResourceGroupName</span></span>
<span data-ttu-id="e90c2-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e90c2-126">Name of resource group.</span></span>

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

### <span data-ttu-id="e90c2-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="e90c2-127">-ThroughputType</span></span>
<span data-ttu-id="e90c2-128">Tipo di throughput a cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="e90c2-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="e90c2-129">I valori possibili sono: scala, manuale.</span><span class="sxs-lookup"><span data-stu-id="e90c2-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="e90c2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e90c2-130">-WhatIf</span></span>
<span data-ttu-id="e90c2-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e90c2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e90c2-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e90c2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e90c2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e90c2-133">CommonParameters</span></span>
<span data-ttu-id="e90c2-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e90c2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e90c2-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e90c2-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e90c2-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e90c2-136">INPUTS</span></span>

### <span data-ttu-id="e90c2-137">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="e90c2-137">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="e90c2-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e90c2-138">OUTPUTS</span></span>

### <span data-ttu-id="e90c2-139">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="e90c2-139">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="e90c2-140">Note</span><span class="sxs-lookup"><span data-stu-id="e90c2-140">NOTES</span></span>

## <span data-ttu-id="e90c2-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e90c2-141">RELATED LINKS</span></span>
