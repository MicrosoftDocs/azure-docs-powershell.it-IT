---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbsqlcontainerthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlContainerThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlContainerThroughputMigration.md
ms.openlocfilehash: ac15f6ba4d8db1e4f3ab35c34b33b78fdefa05a3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177318"
---
# <span data-ttu-id="01d4c-101">Invoke-AzCosmosDBSqlContainerThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="01d4c-101">Invoke-AzCosmosDBSqlContainerThroughputMigration</span></span>

## <span data-ttu-id="01d4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01d4c-102">SYNOPSIS</span></span>
<span data-ttu-id="01d4c-103">Consente di eseguire la migrazione della velocità effettiva della scala automatica alla velocità effettiva manuale e viceversa.</span><span class="sxs-lookup"><span data-stu-id="01d4c-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="01d4c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="01d4c-104">SYNTAX</span></span>

### <span data-ttu-id="01d4c-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="01d4c-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01d4c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="01d4c-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration [-Name <String>] -ParentObject <PSSqlDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01d4c-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="01d4c-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration [-Name <String>] -InputObject <PSSqlContainerGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01d4c-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="01d4c-108">DESCRIPTION</span></span>
<span data-ttu-id="01d4c-109">ThroughpyteType paramter definisce la velocità effettiva a cui si vuole eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="01d4c-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="01d4c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="01d4c-110">EXAMPLES</span></span>

### <span data-ttu-id="01d4c-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="01d4c-111">Example 1</span></span>
```powershell
PS C:\>$NewSqlContainer =  New-AzCosmosDBSqlContainer -AccountName myAccountName -ResourceGroupName myRgName -Name myContainerName  -Throughput  700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBSqlContainerThroughputMigration -InputObject $NewSqlContainer -ThroughputType Autoscale
```

## <span data-ttu-id="01d4c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01d4c-112">PARAMETERS</span></span>

### <span data-ttu-id="01d4c-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="01d4c-113">-AccountName</span></span>
<span data-ttu-id="01d4c-114">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="01d4c-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="01d4c-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01d4c-115">-Confirm</span></span>
<span data-ttu-id="01d4c-116">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01d4c-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01d4c-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="01d4c-117">-DatabaseName</span></span>
<span data-ttu-id="01d4c-118">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="01d4c-118">Database name.</span></span>

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

### <span data-ttu-id="01d4c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01d4c-119">-DefaultProfile</span></span>
<span data-ttu-id="01d4c-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="01d4c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01d4c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01d4c-121">-InputObject</span></span>
<span data-ttu-id="01d4c-122">Oggetto Contenitore Sql.</span><span class="sxs-lookup"><span data-stu-id="01d4c-122">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01d4c-123">-Name</span><span class="sxs-lookup"><span data-stu-id="01d4c-123">-Name</span></span>
<span data-ttu-id="01d4c-124">Nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="01d4c-124">Container name.</span></span>

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

### <span data-ttu-id="01d4c-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="01d4c-125">-ParentObject</span></span>
<span data-ttu-id="01d4c-126">Oggetto Database Sql.</span><span class="sxs-lookup"><span data-stu-id="01d4c-126">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01d4c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01d4c-127">-ResourceGroupName</span></span>
<span data-ttu-id="01d4c-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="01d4c-128">Name of resource group.</span></span>

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

### <span data-ttu-id="01d4c-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="01d4c-129">-ThroughputType</span></span>
<span data-ttu-id="01d4c-130">Tipo di velocità effettiva di cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="01d4c-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="01d4c-131">I valori possibili sono: Scala automatica, Manuale.</span><span class="sxs-lookup"><span data-stu-id="01d4c-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="01d4c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01d4c-132">-WhatIf</span></span>
<span data-ttu-id="01d4c-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="01d4c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01d4c-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="01d4c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01d4c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01d4c-135">CommonParameters</span></span>
<span data-ttu-id="01d4c-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01d4c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01d4c-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="01d4c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01d4c-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="01d4c-138">INPUTS</span></span>

### <span data-ttu-id="01d4c-139">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="01d4c-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="01d4c-140">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="01d4c-140">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="01d4c-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="01d4c-141">OUTPUTS</span></span>

### <span data-ttu-id="01d4c-142">Microsoft.Azure.Commands.EnterpriseDb.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="01d4c-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="01d4c-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="01d4c-143">NOTES</span></span>

## <span data-ttu-id="01d4c-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="01d4c-144">RELATED LINKS</span></span>
