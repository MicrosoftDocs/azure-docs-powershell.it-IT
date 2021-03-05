---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 8195179599d98fbc3fd8954361ba142706460886
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012253"
---
# <span data-ttu-id="bfa37-101">New-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bfa37-101">New-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="bfa37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfa37-102">SYNOPSIS</span></span>
<span data-ttu-id="bfa37-103">Crea un nuovo database Sql databaseDbdb.</span><span class="sxs-lookup"><span data-stu-id="bfa37-103">Creates a new CosmosDB Sql Database.</span></span>

## <span data-ttu-id="bfa37-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bfa37-104">SYNTAX</span></span>

### <span data-ttu-id="bfa37-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bfa37-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfa37-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfa37-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlDatabase -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bfa37-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bfa37-107">DESCRIPTION</span></span>
<span data-ttu-id="bfa37-108">Crea un nuovo database Sql databaseDbdb.</span><span class="sxs-lookup"><span data-stu-id="bfa37-108">Creates a new CosmosDB Sql Database.</span></span>

## <span data-ttu-id="bfa37-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bfa37-109">EXAMPLES</span></span>

### <span data-ttu-id="bfa37-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bfa37-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="bfa37-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bfa37-111">PARAMETERS</span></span>

### <span data-ttu-id="bfa37-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bfa37-112">-AccountName</span></span>
<span data-ttu-id="bfa37-113">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="bfa37-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="bfa37-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="bfa37-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="bfa37-115">Valore massimo di velocità effettiva se è abilitata la scalabilità automatica.</span><span class="sxs-lookup"><span data-stu-id="bfa37-115">Maximum Throughput value if autoscale is enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfa37-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bfa37-116">-Confirm</span></span>
<span data-ttu-id="bfa37-117">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfa37-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfa37-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfa37-118">-DefaultProfile</span></span>
<span data-ttu-id="bfa37-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bfa37-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfa37-120">-Name</span><span class="sxs-lookup"><span data-stu-id="bfa37-120">-Name</span></span>
<span data-ttu-id="bfa37-121">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="bfa37-121">Database name.</span></span>

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

### <span data-ttu-id="bfa37-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="bfa37-122">-ParentObject</span></span>
<span data-ttu-id="bfa37-123">Oggetto Account Aziendale</span><span class="sxs-lookup"><span data-stu-id="bfa37-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="bfa37-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfa37-124">-ResourceGroupName</span></span>
<span data-ttu-id="bfa37-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bfa37-125">Name of resource group.</span></span>

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

### <span data-ttu-id="bfa37-126">-Velocità effettiva</span><span class="sxs-lookup"><span data-stu-id="bfa37-126">-Throughput</span></span>
<span data-ttu-id="bfa37-127">Velocità effettiva di SQL database (RU/S).</span><span class="sxs-lookup"><span data-stu-id="bfa37-127">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="bfa37-128">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="bfa37-128">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfa37-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfa37-129">-WhatIf</span></span>
<span data-ttu-id="bfa37-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bfa37-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfa37-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bfa37-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfa37-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfa37-132">CommonParameters</span></span>
<span data-ttu-id="bfa37-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfa37-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfa37-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bfa37-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfa37-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="bfa37-135">INPUTS</span></span>

### <span data-ttu-id="bfa37-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="bfa37-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="bfa37-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bfa37-137">OUTPUTS</span></span>

### <span data-ttu-id="bfa37-138">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="bfa37-138">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="bfa37-139">Microsoft.Azure.Commands.ExceptionsDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="bfa37-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="bfa37-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="bfa37-140">NOTES</span></span>

## <span data-ttu-id="bfa37-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bfa37-141">RELATED LINKS</span></span>
