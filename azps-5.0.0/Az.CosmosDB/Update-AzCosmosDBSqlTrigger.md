---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 6fcb529b2e2ad87a2bc83421e3c5b59ae22655f6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298981"
---
# <span data-ttu-id="2e2b4-101">Update-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="2e2b4-101">Update-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="2e2b4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2e2b4-102">SYNOPSIS</span></span>
<span data-ttu-id="2e2b4-103">Aggiorna il trigger SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="2e2b4-103">Updates the CosmosDB Sql Trigger.</span></span> <span data-ttu-id="2e2b4-104">Esegue un'operazione di patch lato client leggendo il trigger esistente.</span><span class="sxs-lookup"><span data-stu-id="2e2b4-104">Performs a client side patch operation by reading the existing Trigger.</span></span>

## <span data-ttu-id="2e2b4-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2e2b4-105">SYNTAX</span></span>

### <span data-ttu-id="2e2b4-106">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2e2b4-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-Body <String>] [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e2b4-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e2b4-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlTrigger [-Name <String>] [-Body <String>] [-TriggerOperation <String>]
 [-TriggerType <String>] -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e2b4-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e2b4-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlTrigger [-Name <String>] [-Body <String>] [-TriggerOperation <String>]
 [-TriggerType <String>] -InputObject <PSSqlTriggerGetResults> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e2b4-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2e2b4-109">DESCRIPTION</span></span>
<span data-ttu-id="2e2b4-110">Aggiorna il trigger SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="2e2b4-110">Updates the CosmosDB Sql Trigger.</span></span> <span data-ttu-id="2e2b4-111">Esegue un'operazione di patch lato client leggendo il trigger esistente.</span><span class="sxs-lookup"><span data-stu-id="2e2b4-111">Performs a client side patch operation by reading the existing Trigger.</span></span>

## <span data-ttu-id="2e2b4-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2e2b4-112">EXAMPLES</span></span>

### <span data-ttu-id="2e2b4-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2e2b4-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlTrigger -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myTriggerName -Body myTriggerBody -TriggerOperation All -TriggerType Pre

Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/triggers/myTriggerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="2e2b4-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2e2b4-114">PARAMETERS</span></span>

### <span data-ttu-id="2e2b4-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2e2b4-115">-AccountName</span></span>
<span data-ttu-id="2e2b4-116">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="2e2b4-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2e2b4-117">-Body</span><span class="sxs-lookup"><span data-stu-id="2e2b4-117">-Body</span></span>
<span data-ttu-id="2e2b4-118">Il corpo del trigger.</span><span class="sxs-lookup"><span data-stu-id="2e2b4-118">The body of the Trigger.</span></span>

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

### <span data-ttu-id="2e2b4-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2e2b4-119">-Confirm</span></span>
<span data-ttu-id="2e2b4-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e2b4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e2b4-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="2e2b4-121">-ContainerName</span></span>
<span data-ttu-id="2e2b4-122">Nome contenitore.</span><span class="sxs-lookup"><span data-stu-id="2e2b4-122">Container name.</span></span>

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

### <span data-ttu-id="2e2b4-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2e2b4-123">-DatabaseName</span></span>
<span data-ttu-id="2e2b4-124">Nome database.</span><span class="sxs-lookup"><span data-stu-id="2e2b4-124">Database name.</span></span>

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

### <span data-ttu-id="2e2b4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e2b4-125">-DefaultProfile</span></span>
<span data-ttu-id="2e2b4-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2e2b4-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e2b4-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e2b4-127">-InputObject</span></span>
<span data-ttu-id="2e2b4-128">Oggetto trigger SQL</span><span class="sxs-lookup"><span data-stu-id="2e2b4-128">Sql trigger Object</span></span>

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

### <span data-ttu-id="2e2b4-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="2e2b4-129">-Name</span></span>
<span data-ttu-id="2e2b4-130">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="2e2b4-130">Trigger name.</span></span>

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

### <span data-ttu-id="2e2b4-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="2e2b4-131">-ParentObject</span></span>
<span data-ttu-id="2e2b4-132">Oggetto contenitore SQL.</span><span class="sxs-lookup"><span data-stu-id="2e2b4-132">Sql Container object.</span></span>

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

### <span data-ttu-id="2e2b4-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e2b4-133">-ResourceGroupName</span></span>
<span data-ttu-id="2e2b4-134">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2e2b4-134">Name of resource group.</span></span>

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

### <span data-ttu-id="2e2b4-135">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="2e2b4-135">-TriggerOperation</span></span>
<span data-ttu-id="2e2b4-136">Operazione a cui è associato il trigger.</span><span class="sxs-lookup"><span data-stu-id="2e2b4-136">The operation the trigger is associated with.</span></span>
<span data-ttu-id="2e2b4-137">I valori possibili includono: "tutti", "Crea", "Aggiorna", "Elimina", "Sostituisci"</span><span class="sxs-lookup"><span data-stu-id="2e2b4-137">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="2e2b4-138">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="2e2b4-138">-TriggerType</span></span>
<span data-ttu-id="2e2b4-139">Tipo di trigger.</span><span class="sxs-lookup"><span data-stu-id="2e2b4-139">Type of the Trigger.</span></span>
<span data-ttu-id="2e2b4-140">I valori possibili includono:' pre ',' post '</span><span class="sxs-lookup"><span data-stu-id="2e2b4-140">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="2e2b4-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e2b4-141">-WhatIf</span></span>
<span data-ttu-id="2e2b4-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2e2b4-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e2b4-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2e2b4-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e2b4-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e2b4-144">CommonParameters</span></span>
<span data-ttu-id="2e2b4-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e2b4-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e2b4-146">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e2b4-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e2b4-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2e2b4-147">INPUTS</span></span>

### <span data-ttu-id="2e2b4-148">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="2e2b4-148">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="2e2b4-149">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="2e2b4-149">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="2e2b4-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2e2b4-150">OUTPUTS</span></span>

### <span data-ttu-id="2e2b4-151">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="2e2b4-151">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

### <span data-ttu-id="2e2b4-152">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="2e2b4-152">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="2e2b4-153">Note</span><span class="sxs-lookup"><span data-stu-id="2e2b4-153">NOTES</span></span>

## <span data-ttu-id="2e2b4-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2e2b4-154">RELATED LINKS</span></span>
