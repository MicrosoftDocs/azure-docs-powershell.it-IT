---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbmongodbdatabasethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration.md
ms.openlocfilehash: 1ba30d016b2ff8b143987961d08d68eacca16890
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98487944"
---
# <span data-ttu-id="c03bb-101">Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="c03bb-101">Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration</span></span>

## <span data-ttu-id="c03bb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c03bb-102">SYNOPSIS</span></span>
<span data-ttu-id="c03bb-103">Usare questo comando per eseguire la migrazione della velocità di scalabilità manuale alla velocità effettiva e viceversa.</span><span class="sxs-lookup"><span data-stu-id="c03bb-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="c03bb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c03bb-104">SYNTAX</span></span>

### <span data-ttu-id="c03bb-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c03bb-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c03bb-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c03bb-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c03bb-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c03bb-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>] -InputObject <PSMongoDBDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c03bb-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c03bb-108">DESCRIPTION</span></span>
<span data-ttu-id="c03bb-109">ThroughpyteType parametro definisce la velocità effettiva a cui si vuole eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="c03bb-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="c03bb-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c03bb-110">EXAMPLES</span></span>

### <span data-ttu-id="c03bb-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c03bb-111">Example 1</span></span>
```powershell
PS C:\>$NewMongodbDatabase =  New-AzCosmosDBMongoDBDatabase -AccountName myAccountName -ResourceGroupName myRgName -Name myDbName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration -InputObject $NewMongodbDatabase -ThroughputType Autoscale
```


## <span data-ttu-id="c03bb-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c03bb-112">PARAMETERS</span></span>

### <span data-ttu-id="c03bb-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c03bb-113">-AccountName</span></span>
<span data-ttu-id="c03bb-114">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="c03bb-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c03bb-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c03bb-115">-Confirm</span></span>
<span data-ttu-id="c03bb-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c03bb-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c03bb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c03bb-117">-DefaultProfile</span></span>
<span data-ttu-id="c03bb-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c03bb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c03bb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c03bb-119">-InputObject</span></span>
<span data-ttu-id="c03bb-120">Oggetto di database Mongo.</span><span class="sxs-lookup"><span data-stu-id="c03bb-120">Mongo Database object.</span></span>

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

### <span data-ttu-id="c03bb-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="c03bb-121">-Name</span></span>
<span data-ttu-id="c03bb-122">Nome database.</span><span class="sxs-lookup"><span data-stu-id="c03bb-122">Database name.</span></span>

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

### <span data-ttu-id="c03bb-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c03bb-123">-ParentObject</span></span>
<span data-ttu-id="c03bb-124">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="c03bb-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="c03bb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c03bb-125">-ResourceGroupName</span></span>
<span data-ttu-id="c03bb-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c03bb-126">Name of resource group.</span></span>

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

### <span data-ttu-id="c03bb-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="c03bb-127">-ThroughputType</span></span>
<span data-ttu-id="c03bb-128">Tipo di throughput a cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="c03bb-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="c03bb-129">I valori possibili sono: scala, manuale.</span><span class="sxs-lookup"><span data-stu-id="c03bb-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="c03bb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c03bb-130">-WhatIf</span></span>
<span data-ttu-id="c03bb-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c03bb-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c03bb-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c03bb-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c03bb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c03bb-133">CommonParameters</span></span>
<span data-ttu-id="c03bb-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c03bb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c03bb-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c03bb-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c03bb-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c03bb-136">INPUTS</span></span>

### <span data-ttu-id="c03bb-137">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="c03bb-137">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="c03bb-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c03bb-138">OUTPUTS</span></span>

### <span data-ttu-id="c03bb-139">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="c03bb-139">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="c03bb-140">Note</span><span class="sxs-lookup"><span data-stu-id="c03bb-140">NOTES</span></span>

## <span data-ttu-id="c03bb-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c03bb-141">RELATED LINKS</span></span>
