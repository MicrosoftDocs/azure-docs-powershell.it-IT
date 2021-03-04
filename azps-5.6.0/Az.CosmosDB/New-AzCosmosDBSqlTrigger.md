---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: a6808f6c2640a90006560b16dbfd452167e0d6fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971342"
---
# <span data-ttu-id="4de22-101">New-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="4de22-101">New-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="4de22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4de22-102">SYNOPSIS</span></span>
<span data-ttu-id="4de22-103">Crea un nuovo trigger sql Perdb.</span><span class="sxs-lookup"><span data-stu-id="4de22-103">Creates a new CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="4de22-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4de22-104">SYNTAX</span></span>

### <span data-ttu-id="4de22-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4de22-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4de22-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4de22-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlTrigger -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4de22-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4de22-107">DESCRIPTION</span></span>
<span data-ttu-id="4de22-108">Crea un nuovo trigger sql Perdb.</span><span class="sxs-lookup"><span data-stu-id="4de22-108">Creates a new CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="4de22-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4de22-109">EXAMPLES</span></span>

### <span data-ttu-id="4de22-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4de22-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlTrigger -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myTriggerName -Body myTriggerBody -TriggerOperation All -TriggerType Pre

Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/triggers/myTriggerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="4de22-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4de22-111">PARAMETERS</span></span>

### <span data-ttu-id="4de22-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4de22-112">-AccountName</span></span>
<span data-ttu-id="4de22-113">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="4de22-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="4de22-114">-Body</span><span class="sxs-lookup"><span data-stu-id="4de22-114">-Body</span></span>
<span data-ttu-id="4de22-115">Corpo del trigger.</span><span class="sxs-lookup"><span data-stu-id="4de22-115">The body of the Trigger.</span></span>

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

### <span data-ttu-id="4de22-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4de22-116">-Confirm</span></span>
<span data-ttu-id="4de22-117">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4de22-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4de22-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="4de22-118">-ContainerName</span></span>
<span data-ttu-id="4de22-119">Nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="4de22-119">Container name.</span></span>

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

### <span data-ttu-id="4de22-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4de22-120">-DatabaseName</span></span>
<span data-ttu-id="4de22-121">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="4de22-121">Database name.</span></span>

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

### <span data-ttu-id="4de22-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4de22-122">-DefaultProfile</span></span>
<span data-ttu-id="4de22-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4de22-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4de22-124">-Name</span><span class="sxs-lookup"><span data-stu-id="4de22-124">-Name</span></span>
<span data-ttu-id="4de22-125">Nome trigger.</span><span class="sxs-lookup"><span data-stu-id="4de22-125">Trigger name.</span></span>

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

### <span data-ttu-id="4de22-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4de22-126">-ParentObject</span></span>
<span data-ttu-id="4de22-127">Oggetto Contenitore Sql.</span><span class="sxs-lookup"><span data-stu-id="4de22-127">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4de22-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4de22-128">-ResourceGroupName</span></span>
<span data-ttu-id="4de22-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4de22-129">Name of resource group.</span></span>

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

### <span data-ttu-id="4de22-130">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="4de22-130">-TriggerOperation</span></span>
<span data-ttu-id="4de22-131">Operazione a cui è associato il trigger.</span><span class="sxs-lookup"><span data-stu-id="4de22-131">The operation the trigger is associated with.</span></span>
<span data-ttu-id="4de22-132">I valori possibili includono: 'All', 'Create', 'Update', 'Delete', 'Replace'</span><span class="sxs-lookup"><span data-stu-id="4de22-132">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="4de22-133">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="4de22-133">-TriggerType</span></span>
<span data-ttu-id="4de22-134">Tipo del trigger.</span><span class="sxs-lookup"><span data-stu-id="4de22-134">Type of the Trigger.</span></span>
<span data-ttu-id="4de22-135">I valori possibili includono: "Pre", "Pubblica"</span><span class="sxs-lookup"><span data-stu-id="4de22-135">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="4de22-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4de22-136">-WhatIf</span></span>
<span data-ttu-id="4de22-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4de22-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4de22-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4de22-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4de22-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4de22-139">CommonParameters</span></span>
<span data-ttu-id="4de22-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4de22-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4de22-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4de22-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4de22-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="4de22-142">INPUTS</span></span>

### <span data-ttu-id="4de22-143">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="4de22-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="4de22-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4de22-144">OUTPUTS</span></span>

### <span data-ttu-id="4de22-145">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="4de22-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

### <span data-ttu-id="4de22-146">Microsoft.Azure.Commands.CpsDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="4de22-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="4de22-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="4de22-147">NOTES</span></span>

## <span data-ttu-id="4de22-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4de22-148">RELATED LINKS</span></span>
