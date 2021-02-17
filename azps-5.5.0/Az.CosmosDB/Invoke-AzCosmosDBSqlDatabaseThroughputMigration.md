---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbsqldatabasethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlDatabaseThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlDatabaseThroughputMigration.md
ms.openlocfilehash: 15ee57c32d8eeeca996994900113360adac1c407
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177310"
---
# <span data-ttu-id="76060-101">Invoke-AzCosmosDBSqlDatabaseThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="76060-101">Invoke-AzCosmosDBSqlDatabaseThroughputMigration</span></span>

## <span data-ttu-id="76060-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76060-102">SYNOPSIS</span></span>
<span data-ttu-id="76060-103">Consente di eseguire la migrazione della velocità effettiva della scala automatica alla velocità effettiva manuale e viceversa.</span><span class="sxs-lookup"><span data-stu-id="76060-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="76060-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="76060-104">SYNTAX</span></span>

### <span data-ttu-id="76060-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="76060-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBSqlDatabaseThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="76060-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="76060-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlDatabaseThroughputMigration [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76060-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="76060-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlDatabaseThroughputMigration [-Name <String>] -InputObject <PSSqlDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76060-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="76060-108">DESCRIPTION</span></span>
<span data-ttu-id="76060-109">ThroughpyteType paramter definisce la velocità effettiva a cui si vuole eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="76060-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="76060-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="76060-110">EXAMPLES</span></span>

### <span data-ttu-id="76060-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="76060-111">Example 1</span></span>
```powershell
PS C:\> $NewSqlDatabase =  New-AzCosmosDBSqlDatabase -AccountName myAccountName -ResourceGroupName myRgName -Name myDbName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBSqlDatabaseThroughputMigration -InputObject $NewSqlDatabase -ThroughputType Autoscale
```

## <span data-ttu-id="76060-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76060-112">PARAMETERS</span></span>

### <span data-ttu-id="76060-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="76060-113">-AccountName</span></span>
<span data-ttu-id="76060-114">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="76060-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="76060-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76060-115">-Confirm</span></span>
<span data-ttu-id="76060-116">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76060-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76060-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76060-117">-DefaultProfile</span></span>
<span data-ttu-id="76060-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="76060-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76060-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76060-119">-InputObject</span></span>
<span data-ttu-id="76060-120">Oggetto Database Sql.</span><span class="sxs-lookup"><span data-stu-id="76060-120">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76060-121">-Name</span><span class="sxs-lookup"><span data-stu-id="76060-121">-Name</span></span>
<span data-ttu-id="76060-122">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="76060-122">Database name.</span></span>

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

### <span data-ttu-id="76060-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="76060-123">-ParentObject</span></span>
<span data-ttu-id="76060-124">Oggetto AccountDb Disa</span><span class="sxs-lookup"><span data-stu-id="76060-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="76060-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76060-125">-ResourceGroupName</span></span>
<span data-ttu-id="76060-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="76060-126">Name of resource group.</span></span>

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

### <span data-ttu-id="76060-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="76060-127">-ThroughputType</span></span>
<span data-ttu-id="76060-128">Tipo di velocità effettiva di cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="76060-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="76060-129">I valori possibili sono: Scala automatica, Manuale.</span><span class="sxs-lookup"><span data-stu-id="76060-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="76060-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76060-130">-WhatIf</span></span>
<span data-ttu-id="76060-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="76060-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76060-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="76060-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76060-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76060-133">CommonParameters</span></span>
<span data-ttu-id="76060-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76060-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76060-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="76060-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76060-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="76060-136">INPUTS</span></span>

### <span data-ttu-id="76060-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="76060-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="76060-138">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="76060-138">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="76060-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="76060-139">OUTPUTS</span></span>

### <span data-ttu-id="76060-140">Microsoft.Azure.Commands.EnterpriseDb.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="76060-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="76060-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="76060-141">NOTES</span></span>

## <span data-ttu-id="76060-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="76060-142">RELATED LINKS</span></span>
