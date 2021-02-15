---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 6fcb529b2e2ad87a2bc83421e3c5b59ae22655f6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196742"
---
# <span data-ttu-id="7c191-101">Update-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="7c191-101">Update-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="7c191-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c191-102">SYNOPSIS</span></span>
<span data-ttu-id="7c191-103">Aggiorna il trigger di sql database database.</span><span class="sxs-lookup"><span data-stu-id="7c191-103">Updates the CosmosDB Sql Trigger.</span></span> <span data-ttu-id="7c191-104">Esegue un'operazione di patch sul lato client leggendo il trigger esistente.</span><span class="sxs-lookup"><span data-stu-id="7c191-104">Performs a client side patch operation by reading the existing Trigger.</span></span>

## <span data-ttu-id="7c191-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7c191-105">SYNTAX</span></span>

### <span data-ttu-id="7c191-106">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7c191-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-Body <String>] [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c191-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c191-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlTrigger [-Name <String>] [-Body <String>] [-TriggerOperation <String>]
 [-TriggerType <String>] -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c191-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c191-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlTrigger [-Name <String>] [-Body <String>] [-TriggerOperation <String>]
 [-TriggerType <String>] -InputObject <PSSqlTriggerGetResults> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c191-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7c191-109">DESCRIPTION</span></span>
<span data-ttu-id="7c191-110">Aggiorna il trigger di sql database database.</span><span class="sxs-lookup"><span data-stu-id="7c191-110">Updates the CosmosDB Sql Trigger.</span></span> <span data-ttu-id="7c191-111">Esegue un'operazione di patch sul lato client leggendo il trigger esistente.</span><span class="sxs-lookup"><span data-stu-id="7c191-111">Performs a client side patch operation by reading the existing Trigger.</span></span>

## <span data-ttu-id="7c191-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7c191-112">EXAMPLES</span></span>

### <span data-ttu-id="7c191-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7c191-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlTrigger -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myTriggerName -Body myTriggerBody -TriggerOperation All -TriggerType Pre

Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/triggers/myTriggerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="7c191-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c191-114">PARAMETERS</span></span>

### <span data-ttu-id="7c191-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7c191-115">-AccountName</span></span>
<span data-ttu-id="7c191-116">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="7c191-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7c191-117">-Body</span><span class="sxs-lookup"><span data-stu-id="7c191-117">-Body</span></span>
<span data-ttu-id="7c191-118">Corpo del trigger.</span><span class="sxs-lookup"><span data-stu-id="7c191-118">The body of the Trigger.</span></span>

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

### <span data-ttu-id="7c191-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7c191-119">-Confirm</span></span>
<span data-ttu-id="7c191-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c191-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c191-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="7c191-121">-ContainerName</span></span>
<span data-ttu-id="7c191-122">Nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="7c191-122">Container name.</span></span>

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

### <span data-ttu-id="7c191-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7c191-123">-DatabaseName</span></span>
<span data-ttu-id="7c191-124">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="7c191-124">Database name.</span></span>

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

### <span data-ttu-id="7c191-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c191-125">-DefaultProfile</span></span>
<span data-ttu-id="7c191-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7c191-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c191-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c191-127">-InputObject</span></span>
<span data-ttu-id="7c191-128">Oggetto trigger Sql</span><span class="sxs-lookup"><span data-stu-id="7c191-128">Sql trigger Object</span></span>

```yaml
Type: PSSqlTriggerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c191-129">-Name</span><span class="sxs-lookup"><span data-stu-id="7c191-129">-Name</span></span>
<span data-ttu-id="7c191-130">Nome trigger.</span><span class="sxs-lookup"><span data-stu-id="7c191-130">Trigger name.</span></span>

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

### <span data-ttu-id="7c191-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7c191-131">-ParentObject</span></span>
<span data-ttu-id="7c191-132">Oggetto Contenitore Sql.</span><span class="sxs-lookup"><span data-stu-id="7c191-132">Sql Container object.</span></span>

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

### <span data-ttu-id="7c191-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c191-133">-ResourceGroupName</span></span>
<span data-ttu-id="7c191-134">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7c191-134">Name of resource group.</span></span>

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

### <span data-ttu-id="7c191-135">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="7c191-135">-TriggerOperation</span></span>
<span data-ttu-id="7c191-136">Operazione a cui è associato il trigger.</span><span class="sxs-lookup"><span data-stu-id="7c191-136">The operation the trigger is associated with.</span></span>
<span data-ttu-id="7c191-137">I valori possibili includono: 'All', 'Create', 'Update', 'Delete', 'Replace'</span><span class="sxs-lookup"><span data-stu-id="7c191-137">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="7c191-138">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="7c191-138">-TriggerType</span></span>
<span data-ttu-id="7c191-139">Tipo del trigger.</span><span class="sxs-lookup"><span data-stu-id="7c191-139">Type of the Trigger.</span></span>
<span data-ttu-id="7c191-140">I valori possibili includono: "Pre", "Pubblica"</span><span class="sxs-lookup"><span data-stu-id="7c191-140">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="7c191-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c191-141">-WhatIf</span></span>
<span data-ttu-id="7c191-142">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c191-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c191-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c191-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c191-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c191-144">CommonParameters</span></span>
<span data-ttu-id="7c191-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c191-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c191-146">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7c191-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c191-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="7c191-147">INPUTS</span></span>

### <span data-ttu-id="7c191-148">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="7c191-148">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="7c191-149">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="7c191-149">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="7c191-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7c191-150">OUTPUTS</span></span>

### <span data-ttu-id="7c191-151">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="7c191-151">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

### <span data-ttu-id="7c191-152">Microsoft.Azure.Commands.ExceptionsDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="7c191-152">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="7c191-153">NOTE</span><span class="sxs-lookup"><span data-stu-id="7c191-153">NOTES</span></span>

## <span data-ttu-id="7c191-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7c191-154">RELATED LINKS</span></span>
