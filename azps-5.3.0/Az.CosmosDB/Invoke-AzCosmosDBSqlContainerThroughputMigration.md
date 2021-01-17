---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbsqlcontainerthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlContainerThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlContainerThroughputMigration.md
ms.openlocfilehash: 61b564e8b92193b873e815b4a65f7c009dabf0f6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477484"
---
# <span data-ttu-id="ae868-101">Invoke-AzCosmosDBSqlContainerThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="ae868-101">Invoke-AzCosmosDBSqlContainerThroughputMigration</span></span>

## <span data-ttu-id="ae868-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ae868-102">SYNOPSIS</span></span>
<span data-ttu-id="ae868-103">Usare questo comando per eseguire la migrazione della velocità di scalabilità manuale alla velocità effettiva e viceversa.</span><span class="sxs-lookup"><span data-stu-id="ae868-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="ae868-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ae868-104">SYNTAX</span></span>

### <span data-ttu-id="ae868-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ae868-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae868-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae868-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration [-Name <String>] -ParentObject <PSSqlDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae868-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae868-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration [-Name <String>] -InputObject <PSSqlContainerGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae868-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ae868-108">DESCRIPTION</span></span>
<span data-ttu-id="ae868-109">ThroughpyteType parametro definisce la velocità effettiva a cui si vuole eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="ae868-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="ae868-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ae868-110">EXAMPLES</span></span>

### <span data-ttu-id="ae868-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ae868-111">Example 1</span></span>
```powershell
PS C:\>$NewSqlContainer =  New-AzCosmosDBSqlContainer -AccountName myAccountName -ResourceGroupName myRgName -Name myContainerName  -Throughput  700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBSqlContainerThroughputMigration -InputObject $NewSqlContainer -ThroughputType Autoscale
```


## <span data-ttu-id="ae868-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ae868-112">PARAMETERS</span></span>

### <span data-ttu-id="ae868-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ae868-113">-AccountName</span></span>
<span data-ttu-id="ae868-114">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="ae868-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ae868-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ae868-115">-Confirm</span></span>
<span data-ttu-id="ae868-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae868-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae868-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ae868-117">-DatabaseName</span></span>
<span data-ttu-id="ae868-118">Nome database.</span><span class="sxs-lookup"><span data-stu-id="ae868-118">Database name.</span></span>

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

### <span data-ttu-id="ae868-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae868-119">-DefaultProfile</span></span>
<span data-ttu-id="ae868-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ae868-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae868-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae868-121">-InputObject</span></span>
<span data-ttu-id="ae868-122">Oggetto contenitore SQL.</span><span class="sxs-lookup"><span data-stu-id="ae868-122">Sql Container object.</span></span>

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

### <span data-ttu-id="ae868-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="ae868-123">-Name</span></span>
<span data-ttu-id="ae868-124">Nome contenitore.</span><span class="sxs-lookup"><span data-stu-id="ae868-124">Container name.</span></span>

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

### <span data-ttu-id="ae868-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ae868-125">-ParentObject</span></span>
<span data-ttu-id="ae868-126">Oggetto database SQL.</span><span class="sxs-lookup"><span data-stu-id="ae868-126">Sql Database object.</span></span>

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

### <span data-ttu-id="ae868-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae868-127">-ResourceGroupName</span></span>
<span data-ttu-id="ae868-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ae868-128">Name of resource group.</span></span>

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

### <span data-ttu-id="ae868-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="ae868-129">-ThroughputType</span></span>
<span data-ttu-id="ae868-130">Tipo di throughput a cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="ae868-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="ae868-131">I valori possibili sono: scala, manuale.</span><span class="sxs-lookup"><span data-stu-id="ae868-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="ae868-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae868-132">-WhatIf</span></span>
<span data-ttu-id="ae868-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae868-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae868-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae868-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae868-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae868-135">CommonParameters</span></span>
<span data-ttu-id="ae868-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae868-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae868-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae868-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae868-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ae868-138">INPUTS</span></span>

### <span data-ttu-id="ae868-139">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="ae868-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="ae868-140">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="ae868-140">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="ae868-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ae868-141">OUTPUTS</span></span>

### <span data-ttu-id="ae868-142">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="ae868-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="ae868-143">Note</span><span class="sxs-lookup"><span data-stu-id="ae868-143">NOTES</span></span>

## <span data-ttu-id="ae868-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ae868-144">RELATED LINKS</span></span>
