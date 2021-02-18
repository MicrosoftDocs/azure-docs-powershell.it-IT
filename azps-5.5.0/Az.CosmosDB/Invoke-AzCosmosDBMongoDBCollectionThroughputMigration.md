---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbmongodbcollectionthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBCollectionThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBCollectionThroughputMigration.md
ms.openlocfilehash: 79dcea6f66d01e9bfa2dd53b990a8f38ec5b0f2a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204642"
---
# <span data-ttu-id="0da0d-101">Invoke-AzCosmosDBMongoDBCollectionThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="0da0d-101">Invoke-AzCosmosDBMongoDBCollectionThroughputMigration</span></span>

## <span data-ttu-id="0da0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0da0d-102">SYNOPSIS</span></span>
<span data-ttu-id="0da0d-103">Consente di eseguire la migrazione della velocità effettiva della scala automatica alla velocità effettiva manuale e viceversa.</span><span class="sxs-lookup"><span data-stu-id="0da0d-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="0da0d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0da0d-104">SYNTAX</span></span>

### <span data-ttu-id="0da0d-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0da0d-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0da0d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0da0d-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration [-Name <String>]
 -ParentObject <PSMongoDBDatabaseGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0da0d-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0da0d-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration [-Name <String>]
 -InputObject <PSMongoDBCollectionGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0da0d-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0da0d-108">DESCRIPTION</span></span>
<span data-ttu-id="0da0d-109">ThroughpyteType paramter definisce la velocità effettiva a cui si vuole eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="0da0d-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="0da0d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0da0d-110">EXAMPLES</span></span>

### <span data-ttu-id="0da0d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0da0d-111">Example 1</span></span>
```powershell
PS C:\> $NewCollection =  New-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -Name myCollectionName -Throughput  700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBMongoDBCollectionThroughputMigration -InputObject $NewCollection -ThroughputType Autoscale
```

## <span data-ttu-id="0da0d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0da0d-112">PARAMETERS</span></span>

### <span data-ttu-id="0da0d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0da0d-113">-AccountName</span></span>
<span data-ttu-id="0da0d-114">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="0da0d-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0da0d-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0da0d-115">-Confirm</span></span>
<span data-ttu-id="0da0d-116">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0da0d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0da0d-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0da0d-117">-DatabaseName</span></span>
<span data-ttu-id="0da0d-118">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="0da0d-118">Database name.</span></span>

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

### <span data-ttu-id="0da0d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0da0d-119">-DefaultProfile</span></span>
<span data-ttu-id="0da0d-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0da0d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0da0d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0da0d-121">-InputObject</span></span>
<span data-ttu-id="0da0d-122">Oggetto Raccolta mongo.</span><span class="sxs-lookup"><span data-stu-id="0da0d-122">Mongo Collection object.</span></span>

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

### <span data-ttu-id="0da0d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="0da0d-123">-Name</span></span>
<span data-ttu-id="0da0d-124">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="0da0d-124">Collection name.</span></span>

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

### <span data-ttu-id="0da0d-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0da0d-125">-ParentObject</span></span>
<span data-ttu-id="0da0d-126">Oggetto database mongo.</span><span class="sxs-lookup"><span data-stu-id="0da0d-126">Mongo Database object.</span></span>

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

### <span data-ttu-id="0da0d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0da0d-127">-ResourceGroupName</span></span>
<span data-ttu-id="0da0d-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0da0d-128">Name of resource group.</span></span>

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

### <span data-ttu-id="0da0d-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="0da0d-129">-ThroughputType</span></span>
<span data-ttu-id="0da0d-130">Tipo di velocità effettiva di cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="0da0d-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="0da0d-131">I valori possibili sono: Scala automatica, Manuale.</span><span class="sxs-lookup"><span data-stu-id="0da0d-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="0da0d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0da0d-132">-WhatIf</span></span>
<span data-ttu-id="0da0d-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0da0d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0da0d-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0da0d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0da0d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0da0d-135">CommonParameters</span></span>
<span data-ttu-id="0da0d-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0da0d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0da0d-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0da0d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0da0d-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="0da0d-138">INPUTS</span></span>

### <span data-ttu-id="0da0d-139">Microsoft.Azure.Commands.EnterpriseDb.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="0da0d-139">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="0da0d-140">Microsoft.Azure.Commands.EnterpriseDb.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="0da0d-140">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="0da0d-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0da0d-141">OUTPUTS</span></span>

### <span data-ttu-id="0da0d-142">Microsoft.Azure.Commands.EnterpriseDb.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="0da0d-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="0da0d-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="0da0d-143">NOTES</span></span>

## <span data-ttu-id="0da0d-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0da0d-144">RELATED LINKS</span></span>
