---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: da512c08120c65f68c39c5072a3e770886ec5031
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177239"
---
# <span data-ttu-id="fac44-101">New-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="fac44-101">New-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="fac44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fac44-102">SYNOPSIS</span></span>
<span data-ttu-id="fac44-103">Crea un nuovo trigger sql Perdb.</span><span class="sxs-lookup"><span data-stu-id="fac44-103">Creates a new CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="fac44-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fac44-104">SYNTAX</span></span>

### <span data-ttu-id="fac44-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fac44-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fac44-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fac44-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlTrigger -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fac44-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fac44-107">DESCRIPTION</span></span>
<span data-ttu-id="fac44-108">Crea un nuovo trigger sql Perdb.</span><span class="sxs-lookup"><span data-stu-id="fac44-108">Creates a new CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="fac44-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fac44-109">EXAMPLES</span></span>

### <span data-ttu-id="fac44-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fac44-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlTrigger -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myTriggerName -Body myTriggerBody -TriggerOperation All -TriggerType Pre

Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/triggers/myTriggerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="fac44-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fac44-111">PARAMETERS</span></span>

### <span data-ttu-id="fac44-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fac44-112">-AccountName</span></span>
<span data-ttu-id="fac44-113">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="fac44-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="fac44-114">-Body</span><span class="sxs-lookup"><span data-stu-id="fac44-114">-Body</span></span>
<span data-ttu-id="fac44-115">Corpo del trigger.</span><span class="sxs-lookup"><span data-stu-id="fac44-115">The body of the Trigger.</span></span>

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

### <span data-ttu-id="fac44-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fac44-116">-Confirm</span></span>
<span data-ttu-id="fac44-117">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fac44-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fac44-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="fac44-118">-ContainerName</span></span>
<span data-ttu-id="fac44-119">Nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="fac44-119">Container name.</span></span>

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

### <span data-ttu-id="fac44-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fac44-120">-DatabaseName</span></span>
<span data-ttu-id="fac44-121">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="fac44-121">Database name.</span></span>

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

### <span data-ttu-id="fac44-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fac44-122">-DefaultProfile</span></span>
<span data-ttu-id="fac44-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fac44-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fac44-124">-Name</span><span class="sxs-lookup"><span data-stu-id="fac44-124">-Name</span></span>
<span data-ttu-id="fac44-125">Nome trigger.</span><span class="sxs-lookup"><span data-stu-id="fac44-125">Trigger name.</span></span>

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

### <span data-ttu-id="fac44-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="fac44-126">-ParentObject</span></span>
<span data-ttu-id="fac44-127">Oggetto Contenitore Sql.</span><span class="sxs-lookup"><span data-stu-id="fac44-127">Sql Container object.</span></span>

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

### <span data-ttu-id="fac44-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fac44-128">-ResourceGroupName</span></span>
<span data-ttu-id="fac44-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fac44-129">Name of resource group.</span></span>

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

### <span data-ttu-id="fac44-130">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="fac44-130">-TriggerOperation</span></span>
<span data-ttu-id="fac44-131">Operazione a cui è associato il trigger.</span><span class="sxs-lookup"><span data-stu-id="fac44-131">The operation the trigger is associated with.</span></span>
<span data-ttu-id="fac44-132">I valori possibili includono: 'All', 'Create', 'Update', 'Delete', 'Replace'</span><span class="sxs-lookup"><span data-stu-id="fac44-132">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="fac44-133">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="fac44-133">-TriggerType</span></span>
<span data-ttu-id="fac44-134">Tipo del trigger.</span><span class="sxs-lookup"><span data-stu-id="fac44-134">Type of the Trigger.</span></span>
<span data-ttu-id="fac44-135">I valori possibili includono: "Pre", "Pubblica"</span><span class="sxs-lookup"><span data-stu-id="fac44-135">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="fac44-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fac44-136">-WhatIf</span></span>
<span data-ttu-id="fac44-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fac44-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fac44-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fac44-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fac44-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fac44-139">CommonParameters</span></span>
<span data-ttu-id="fac44-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fac44-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fac44-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fac44-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fac44-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="fac44-142">INPUTS</span></span>

### <span data-ttu-id="fac44-143">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="fac44-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="fac44-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fac44-144">OUTPUTS</span></span>

### <span data-ttu-id="fac44-145">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="fac44-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

### <span data-ttu-id="fac44-146">Microsoft.Azure.Commands.ExceptionsDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="fac44-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="fac44-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="fac44-147">NOTES</span></span>

## <span data-ttu-id="fac44-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fac44-148">RELATED LINKS</span></span>
