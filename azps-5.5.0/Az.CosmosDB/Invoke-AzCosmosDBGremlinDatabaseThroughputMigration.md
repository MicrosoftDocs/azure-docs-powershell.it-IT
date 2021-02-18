---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbgremlindatabasethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinDatabaseThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinDatabaseThroughputMigration.md
ms.openlocfilehash: 3369415e3c5169695b04ccc8677c3bf0d2f99cd8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181326"
---
# <span data-ttu-id="3dc6e-101">Invoke-AzCosmosDBGremlinDatabaseThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="3dc6e-101">Invoke-AzCosmosDBGremlinDatabaseThroughputMigration</span></span>

## <span data-ttu-id="3dc6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3dc6e-102">SYNOPSIS</span></span>
<span data-ttu-id="3dc6e-103">Consente di eseguire la migrazione della velocità effettiva della scala automatica alla velocità effettiva manuale e viceversa.</span><span class="sxs-lookup"><span data-stu-id="3dc6e-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="3dc6e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3dc6e-104">SYNTAX</span></span>

### <span data-ttu-id="3dc6e-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3dc6e-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBGremlinDatabaseThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3dc6e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3dc6e-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinDatabaseThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3dc6e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3dc6e-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinDatabaseThroughputMigration [-Name <String>] -InputObject <PSGremlinDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3dc6e-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3dc6e-108">DESCRIPTION</span></span>
<span data-ttu-id="3dc6e-109">ThroughpyteType paramter definisce la velocità effettiva a cui si vuole eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="3dc6e-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="3dc6e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3dc6e-110">EXAMPLES</span></span>

### <span data-ttu-id="3dc6e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3dc6e-111">Example 1</span></span>
```powershell
PS C:\> $NewDb =  New-AzCosmosDBGremlinDatabase -AccountName myAccountName -ResourceGroupName myRgName -Name myDbName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBGremlinDatabaseThroughputMigration -InputObject $NewDb -ThroughputType Autoscale
```

## <span data-ttu-id="3dc6e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3dc6e-112">PARAMETERS</span></span>

### <span data-ttu-id="3dc6e-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3dc6e-113">-AccountName</span></span>
<span data-ttu-id="3dc6e-114">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="3dc6e-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="3dc6e-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3dc6e-115">-Confirm</span></span>
<span data-ttu-id="3dc6e-116">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3dc6e-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dc6e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dc6e-117">-DefaultProfile</span></span>
<span data-ttu-id="3dc6e-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3dc6e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3dc6e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3dc6e-119">-InputObject</span></span>
<span data-ttu-id="3dc6e-120">Oggetto di database Gremlin.</span><span class="sxs-lookup"><span data-stu-id="3dc6e-120">Gremlin Database object.</span></span>

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

### <span data-ttu-id="3dc6e-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3dc6e-121">-Name</span></span>
<span data-ttu-id="3dc6e-122">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="3dc6e-122">Database name.</span></span>

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

### <span data-ttu-id="3dc6e-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="3dc6e-123">-ParentObject</span></span>
<span data-ttu-id="3dc6e-124">Oggetto AccountDb Disa</span><span class="sxs-lookup"><span data-stu-id="3dc6e-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="3dc6e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dc6e-125">-ResourceGroupName</span></span>
<span data-ttu-id="3dc6e-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3dc6e-126">Name of resource group.</span></span>

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

### <span data-ttu-id="3dc6e-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="3dc6e-127">-ThroughputType</span></span>
<span data-ttu-id="3dc6e-128">Tipo di velocità effettiva di cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="3dc6e-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="3dc6e-129">I valori possibili sono: Scala automatica, Manuale.</span><span class="sxs-lookup"><span data-stu-id="3dc6e-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="3dc6e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dc6e-130">-WhatIf</span></span>
<span data-ttu-id="3dc6e-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3dc6e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3dc6e-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3dc6e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3dc6e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dc6e-133">CommonParameters</span></span>
<span data-ttu-id="3dc6e-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dc6e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dc6e-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3dc6e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dc6e-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="3dc6e-136">INPUTS</span></span>

### <span data-ttu-id="3dc6e-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="3dc6e-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="3dc6e-138">Microsoft.Azure.Commands.EnterpriseDb.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="3dc6e-138">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="3dc6e-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3dc6e-139">OUTPUTS</span></span>

### <span data-ttu-id="3dc6e-140">Microsoft.Azure.Commands.EnterpriseDb.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="3dc6e-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="3dc6e-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="3dc6e-141">NOTES</span></span>

## <span data-ttu-id="3dc6e-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3dc6e-142">RELATED LINKS</span></span>
