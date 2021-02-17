---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbmongodbdatabasethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration.md
ms.openlocfilehash: 7b30582e0a55e65009fa7248c61cd36f32393249
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196854"
---
# <span data-ttu-id="72cb9-101">Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="72cb9-101">Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration</span></span>

## <span data-ttu-id="72cb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72cb9-102">SYNOPSIS</span></span>
<span data-ttu-id="72cb9-103">Consente di eseguire la migrazione della velocità effettiva della scala automatica alla velocità effettiva manuale e viceversa.</span><span class="sxs-lookup"><span data-stu-id="72cb9-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="72cb9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="72cb9-104">SYNTAX</span></span>

### <span data-ttu-id="72cb9-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="72cb9-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="72cb9-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="72cb9-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72cb9-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="72cb9-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>] -InputObject <PSMongoDBDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72cb9-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="72cb9-108">DESCRIPTION</span></span>
<span data-ttu-id="72cb9-109">ThroughpyteType paramter definisce la velocità effettiva a cui si vuole eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="72cb9-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="72cb9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="72cb9-110">EXAMPLES</span></span>

### <span data-ttu-id="72cb9-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="72cb9-111">Example 1</span></span>
```powershell
PS C:\>$NewMongodbDatabase =  New-AzCosmosDBMongoDBDatabase -AccountName myAccountName -ResourceGroupName myRgName -Name myDbName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration -InputObject $NewMongodbDatabase -ThroughputType Autoscale
```

## <span data-ttu-id="72cb9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72cb9-112">PARAMETERS</span></span>

### <span data-ttu-id="72cb9-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="72cb9-113">-AccountName</span></span>
<span data-ttu-id="72cb9-114">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="72cb9-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="72cb9-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="72cb9-115">-Confirm</span></span>
<span data-ttu-id="72cb9-116">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72cb9-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72cb9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72cb9-117">-DefaultProfile</span></span>
<span data-ttu-id="72cb9-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="72cb9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72cb9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72cb9-119">-InputObject</span></span>
<span data-ttu-id="72cb9-120">Oggetto database mongo.</span><span class="sxs-lookup"><span data-stu-id="72cb9-120">Mongo Database object.</span></span>

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

### <span data-ttu-id="72cb9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="72cb9-121">-Name</span></span>
<span data-ttu-id="72cb9-122">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="72cb9-122">Database name.</span></span>

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

### <span data-ttu-id="72cb9-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="72cb9-123">-ParentObject</span></span>
<span data-ttu-id="72cb9-124">Oggetto AccountDb Disa</span><span class="sxs-lookup"><span data-stu-id="72cb9-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="72cb9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72cb9-125">-ResourceGroupName</span></span>
<span data-ttu-id="72cb9-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="72cb9-126">Name of resource group.</span></span>

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

### <span data-ttu-id="72cb9-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="72cb9-127">-ThroughputType</span></span>
<span data-ttu-id="72cb9-128">Tipo di velocità effettiva di cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="72cb9-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="72cb9-129">I valori possibili sono: Scala automatica, Manuale.</span><span class="sxs-lookup"><span data-stu-id="72cb9-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="72cb9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72cb9-130">-WhatIf</span></span>
<span data-ttu-id="72cb9-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="72cb9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72cb9-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="72cb9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72cb9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72cb9-133">CommonParameters</span></span>
<span data-ttu-id="72cb9-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72cb9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72cb9-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="72cb9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72cb9-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="72cb9-136">INPUTS</span></span>

### <span data-ttu-id="72cb9-137">Microsoft.Azure.Commands.EnterpriseDb.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="72cb9-137">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="72cb9-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="72cb9-138">OUTPUTS</span></span>

### <span data-ttu-id="72cb9-139">Microsoft.Azure.Commands.EnterpriseDb.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="72cb9-139">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="72cb9-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="72cb9-140">NOTES</span></span>

## <span data-ttu-id="72cb9-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="72cb9-141">RELATED LINKS</span></span>
