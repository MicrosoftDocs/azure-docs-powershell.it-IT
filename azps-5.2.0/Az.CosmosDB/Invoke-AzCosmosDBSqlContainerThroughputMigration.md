---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbsqlcontainerthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlContainerThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlContainerThroughputMigration.md
ms.openlocfilehash: 61b564e8b92193b873e815b4a65f7c009dabf0f6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361227"
---
# <span data-ttu-id="e2ca9-101">Invoke-AzCosmosDBSqlContainerThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="e2ca9-101">Invoke-AzCosmosDBSqlContainerThroughputMigration</span></span>

## <span data-ttu-id="e2ca9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e2ca9-102">SYNOPSIS</span></span>
<span data-ttu-id="e2ca9-103">Usare questo comando per eseguire la migrazione della velocità di scalabilità manuale alla velocità effettiva e viceversa.</span><span class="sxs-lookup"><span data-stu-id="e2ca9-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="e2ca9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e2ca9-104">SYNTAX</span></span>

### <span data-ttu-id="e2ca9-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e2ca9-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2ca9-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2ca9-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration [-Name <String>] -ParentObject <PSSqlDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2ca9-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2ca9-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration [-Name <String>] -InputObject <PSSqlContainerGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2ca9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2ca9-108">DESCRIPTION</span></span>
<span data-ttu-id="e2ca9-109">ThroughpyteType parametro definisce la velocità effettiva a cui si vuole eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="e2ca9-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="e2ca9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e2ca9-110">EXAMPLES</span></span>

### <span data-ttu-id="e2ca9-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e2ca9-111">Example 1</span></span>
```powershell
PS C:\>$NewSqlContainer =  New-AzCosmosDBSqlContainer -AccountName myAccountName -ResourceGroupName myRgName -Name myContainerName  -Throughput  700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBSqlContainerThroughputMigration -InputObject $NewSqlContainer -ThroughputType Autoscale
```


## <span data-ttu-id="e2ca9-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e2ca9-112">PARAMETERS</span></span>

### <span data-ttu-id="e2ca9-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e2ca9-113">-AccountName</span></span>
<span data-ttu-id="e2ca9-114">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="e2ca9-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e2ca9-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e2ca9-115">-Confirm</span></span>
<span data-ttu-id="e2ca9-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2ca9-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2ca9-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e2ca9-117">-DatabaseName</span></span>
<span data-ttu-id="e2ca9-118">Nome database.</span><span class="sxs-lookup"><span data-stu-id="e2ca9-118">Database name.</span></span>

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

### <span data-ttu-id="e2ca9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2ca9-119">-DefaultProfile</span></span>
<span data-ttu-id="e2ca9-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e2ca9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2ca9-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2ca9-121">-InputObject</span></span>
<span data-ttu-id="e2ca9-122">Oggetto contenitore SQL.</span><span class="sxs-lookup"><span data-stu-id="e2ca9-122">Sql Container object.</span></span>

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

### <span data-ttu-id="e2ca9-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="e2ca9-123">-Name</span></span>
<span data-ttu-id="e2ca9-124">Nome contenitore.</span><span class="sxs-lookup"><span data-stu-id="e2ca9-124">Container name.</span></span>

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

### <span data-ttu-id="e2ca9-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e2ca9-125">-ParentObject</span></span>
<span data-ttu-id="e2ca9-126">Oggetto database SQL.</span><span class="sxs-lookup"><span data-stu-id="e2ca9-126">Sql Database object.</span></span>

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

### <span data-ttu-id="e2ca9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2ca9-127">-ResourceGroupName</span></span>
<span data-ttu-id="e2ca9-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e2ca9-128">Name of resource group.</span></span>

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

### <span data-ttu-id="e2ca9-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="e2ca9-129">-ThroughputType</span></span>
<span data-ttu-id="e2ca9-130">Tipo di throughput a cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="e2ca9-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="e2ca9-131">I valori possibili sono: scala, manuale.</span><span class="sxs-lookup"><span data-stu-id="e2ca9-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="e2ca9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2ca9-132">-WhatIf</span></span>
<span data-ttu-id="e2ca9-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e2ca9-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2ca9-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e2ca9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2ca9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2ca9-135">CommonParameters</span></span>
<span data-ttu-id="e2ca9-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2ca9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2ca9-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2ca9-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2ca9-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e2ca9-138">INPUTS</span></span>

### <span data-ttu-id="e2ca9-139">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="e2ca9-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="e2ca9-140">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="e2ca9-140">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="e2ca9-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e2ca9-141">OUTPUTS</span></span>

### <span data-ttu-id="e2ca9-142">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="e2ca9-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="e2ca9-143">Note</span><span class="sxs-lookup"><span data-stu-id="e2ca9-143">NOTES</span></span>

## <span data-ttu-id="e2ca9-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e2ca9-144">RELATED LINKS</span></span>
