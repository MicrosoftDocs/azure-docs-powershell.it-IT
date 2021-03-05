---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/invoke-azcosmosdbsqldatabasethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlDatabaseThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlDatabaseThroughputMigration.md
ms.openlocfilehash: 3a457002fc683c6082a0fad705666a177be93482
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004350"
---
# <span data-ttu-id="0f197-101">Invoke-AzCosmosDBSqlDatabaseThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="0f197-101">Invoke-AzCosmosDBSqlDatabaseThroughputMigration</span></span>

## <span data-ttu-id="0f197-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f197-102">SYNOPSIS</span></span>
<span data-ttu-id="0f197-103">Consente di eseguire la migrazione della velocità effettiva della scala automatica alla velocità effettiva manuale e viceversa.</span><span class="sxs-lookup"><span data-stu-id="0f197-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="0f197-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0f197-104">SYNTAX</span></span>

### <span data-ttu-id="0f197-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0f197-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBSqlDatabaseThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0f197-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f197-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlDatabaseThroughputMigration [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f197-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f197-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlDatabaseThroughputMigration [-Name <String>] -InputObject <PSSqlDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f197-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0f197-108">DESCRIPTION</span></span>
<span data-ttu-id="0f197-109">ThroughpyteType paramter definisce la velocità effettiva a cui si vuole eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="0f197-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="0f197-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0f197-110">EXAMPLES</span></span>

### <span data-ttu-id="0f197-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0f197-111">Example 1</span></span>
```powershell
PS C:\> $NewSqlDatabase =  New-AzCosmosDBSqlDatabase -AccountName myAccountName -ResourceGroupName myRgName -Name myDbName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBSqlDatabaseThroughputMigration -InputObject $NewSqlDatabase -ThroughputType Autoscale
```

## <span data-ttu-id="0f197-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f197-112">PARAMETERS</span></span>

### <span data-ttu-id="0f197-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0f197-113">-AccountName</span></span>
<span data-ttu-id="0f197-114">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="0f197-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0f197-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0f197-115">-Confirm</span></span>
<span data-ttu-id="0f197-116">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f197-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f197-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f197-117">-DefaultProfile</span></span>
<span data-ttu-id="0f197-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0f197-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f197-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f197-119">-InputObject</span></span>
<span data-ttu-id="0f197-120">Oggetto database Sql.</span><span class="sxs-lookup"><span data-stu-id="0f197-120">Sql Database object.</span></span>

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

### <span data-ttu-id="0f197-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0f197-121">-Name</span></span>
<span data-ttu-id="0f197-122">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="0f197-122">Database name.</span></span>

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

### <span data-ttu-id="0f197-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0f197-123">-ParentObject</span></span>
<span data-ttu-id="0f197-124">Oggetto AccountDb Disa</span><span class="sxs-lookup"><span data-stu-id="0f197-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="0f197-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f197-125">-ResourceGroupName</span></span>
<span data-ttu-id="0f197-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0f197-126">Name of resource group.</span></span>

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

### <span data-ttu-id="0f197-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="0f197-127">-ThroughputType</span></span>
<span data-ttu-id="0f197-128">Tipo di velocità effettiva di cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="0f197-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="0f197-129">I valori possibili sono: Scala automatica, Manuale.</span><span class="sxs-lookup"><span data-stu-id="0f197-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="0f197-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f197-130">-WhatIf</span></span>
<span data-ttu-id="0f197-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0f197-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f197-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0f197-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f197-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f197-133">CommonParameters</span></span>
<span data-ttu-id="0f197-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f197-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f197-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0f197-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f197-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="0f197-136">INPUTS</span></span>

### <span data-ttu-id="0f197-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="0f197-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="0f197-138">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="0f197-138">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="0f197-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0f197-139">OUTPUTS</span></span>

### <span data-ttu-id="0f197-140">Microsoft.Azure.Commands.EnterpriseDb.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="0f197-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="0f197-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="0f197-141">NOTES</span></span>

## <span data-ttu-id="0f197-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0f197-142">RELATED LINKS</span></span>
