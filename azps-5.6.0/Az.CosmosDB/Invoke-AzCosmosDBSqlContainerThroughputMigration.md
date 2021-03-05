---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/invoke-azcosmosdbsqlcontainerthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlContainerThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlContainerThroughputMigration.md
ms.openlocfilehash: c502040c2d4b11302c158cffb66bf6fd01e148ba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996854"
---
# <span data-ttu-id="39c11-101">Invoke-AzCosmosDBSqlContainerThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="39c11-101">Invoke-AzCosmosDBSqlContainerThroughputMigration</span></span>

## <span data-ttu-id="39c11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39c11-102">SYNOPSIS</span></span>
<span data-ttu-id="39c11-103">Consente di eseguire la migrazione della velocità effettiva della scala automatica alla velocità effettiva manuale e viceversa.</span><span class="sxs-lookup"><span data-stu-id="39c11-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="39c11-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="39c11-104">SYNTAX</span></span>

### <span data-ttu-id="39c11-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="39c11-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39c11-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="39c11-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration [-Name <String>] -ParentObject <PSSqlDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39c11-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="39c11-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration [-Name <String>] -InputObject <PSSqlContainerGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39c11-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="39c11-108">DESCRIPTION</span></span>
<span data-ttu-id="39c11-109">ThroughpyteType paramter definisce la velocità effettiva a cui si vuole eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="39c11-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="39c11-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="39c11-110">EXAMPLES</span></span>

### <span data-ttu-id="39c11-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="39c11-111">Example 1</span></span>
```powershell
PS C:\>$NewSqlContainer =  New-AzCosmosDBSqlContainer -AccountName myAccountName -ResourceGroupName myRgName -Name myContainerName  -Throughput  700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBSqlContainerThroughputMigration -InputObject $NewSqlContainer -ThroughputType Autoscale
```

## <span data-ttu-id="39c11-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39c11-112">PARAMETERS</span></span>

### <span data-ttu-id="39c11-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="39c11-113">-AccountName</span></span>
<span data-ttu-id="39c11-114">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="39c11-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="39c11-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39c11-115">-Confirm</span></span>
<span data-ttu-id="39c11-116">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39c11-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39c11-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="39c11-117">-DatabaseName</span></span>
<span data-ttu-id="39c11-118">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="39c11-118">Database name.</span></span>

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

### <span data-ttu-id="39c11-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39c11-119">-DefaultProfile</span></span>
<span data-ttu-id="39c11-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="39c11-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39c11-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39c11-121">-InputObject</span></span>
<span data-ttu-id="39c11-122">Oggetto Contenitore Sql.</span><span class="sxs-lookup"><span data-stu-id="39c11-122">Sql Container object.</span></span>

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

### <span data-ttu-id="39c11-123">-Name</span><span class="sxs-lookup"><span data-stu-id="39c11-123">-Name</span></span>
<span data-ttu-id="39c11-124">Nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="39c11-124">Container name.</span></span>

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

### <span data-ttu-id="39c11-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="39c11-125">-ParentObject</span></span>
<span data-ttu-id="39c11-126">Oggetto Database Sql.</span><span class="sxs-lookup"><span data-stu-id="39c11-126">Sql Database object.</span></span>

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

### <span data-ttu-id="39c11-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39c11-127">-ResourceGroupName</span></span>
<span data-ttu-id="39c11-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="39c11-128">Name of resource group.</span></span>

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

### <span data-ttu-id="39c11-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="39c11-129">-ThroughputType</span></span>
<span data-ttu-id="39c11-130">Tipo di velocità effettiva di cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="39c11-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="39c11-131">I valori possibili sono: Scala automatica, Manuale.</span><span class="sxs-lookup"><span data-stu-id="39c11-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="39c11-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39c11-132">-WhatIf</span></span>
<span data-ttu-id="39c11-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="39c11-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39c11-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="39c11-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39c11-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39c11-135">CommonParameters</span></span>
<span data-ttu-id="39c11-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39c11-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39c11-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="39c11-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39c11-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="39c11-138">INPUTS</span></span>

### <span data-ttu-id="39c11-139">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="39c11-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="39c11-140">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="39c11-140">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="39c11-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="39c11-141">OUTPUTS</span></span>

### <span data-ttu-id="39c11-142">Microsoft.Azure.Commands.EnterpriseDb.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="39c11-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="39c11-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="39c11-143">NOTES</span></span>

## <span data-ttu-id="39c11-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="39c11-144">RELATED LINKS</span></span>
