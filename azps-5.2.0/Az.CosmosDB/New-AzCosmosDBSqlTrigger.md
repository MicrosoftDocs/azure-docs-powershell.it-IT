---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: da512c08120c65f68c39c5072a3e770886ec5031
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366978"
---
# <span data-ttu-id="93c06-101">New-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="93c06-101">New-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="93c06-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="93c06-102">SYNOPSIS</span></span>
<span data-ttu-id="93c06-103">Crea un nuovo trigger SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="93c06-103">Creates a new CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="93c06-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="93c06-104">SYNTAX</span></span>

### <span data-ttu-id="93c06-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="93c06-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93c06-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="93c06-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlTrigger -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="93c06-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="93c06-107">DESCRIPTION</span></span>
<span data-ttu-id="93c06-108">Crea un nuovo trigger SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="93c06-108">Creates a new CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="93c06-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="93c06-109">EXAMPLES</span></span>

### <span data-ttu-id="93c06-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="93c06-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlTrigger -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myTriggerName -Body myTriggerBody -TriggerOperation All -TriggerType Pre

Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/triggers/myTriggerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="93c06-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="93c06-111">PARAMETERS</span></span>

### <span data-ttu-id="93c06-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="93c06-112">-AccountName</span></span>
<span data-ttu-id="93c06-113">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="93c06-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="93c06-114">-Body</span><span class="sxs-lookup"><span data-stu-id="93c06-114">-Body</span></span>
<span data-ttu-id="93c06-115">Il corpo del trigger.</span><span class="sxs-lookup"><span data-stu-id="93c06-115">The body of the Trigger.</span></span>

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

### <span data-ttu-id="93c06-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="93c06-116">-Confirm</span></span>
<span data-ttu-id="93c06-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93c06-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93c06-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="93c06-118">-ContainerName</span></span>
<span data-ttu-id="93c06-119">Nome contenitore.</span><span class="sxs-lookup"><span data-stu-id="93c06-119">Container name.</span></span>

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

### <span data-ttu-id="93c06-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="93c06-120">-DatabaseName</span></span>
<span data-ttu-id="93c06-121">Nome database.</span><span class="sxs-lookup"><span data-stu-id="93c06-121">Database name.</span></span>

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

### <span data-ttu-id="93c06-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93c06-122">-DefaultProfile</span></span>
<span data-ttu-id="93c06-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="93c06-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93c06-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="93c06-124">-Name</span></span>
<span data-ttu-id="93c06-125">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="93c06-125">Trigger name.</span></span>

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

### <span data-ttu-id="93c06-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="93c06-126">-ParentObject</span></span>
<span data-ttu-id="93c06-127">Oggetto contenitore SQL.</span><span class="sxs-lookup"><span data-stu-id="93c06-127">Sql Container object.</span></span>

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

### <span data-ttu-id="93c06-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93c06-128">-ResourceGroupName</span></span>
<span data-ttu-id="93c06-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="93c06-129">Name of resource group.</span></span>

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

### <span data-ttu-id="93c06-130">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="93c06-130">-TriggerOperation</span></span>
<span data-ttu-id="93c06-131">Operazione a cui è associato il trigger.</span><span class="sxs-lookup"><span data-stu-id="93c06-131">The operation the trigger is associated with.</span></span>
<span data-ttu-id="93c06-132">I valori possibili includono: "tutti", "Crea", "Aggiorna", "Elimina", "Sostituisci"</span><span class="sxs-lookup"><span data-stu-id="93c06-132">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="93c06-133">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="93c06-133">-TriggerType</span></span>
<span data-ttu-id="93c06-134">Tipo di trigger.</span><span class="sxs-lookup"><span data-stu-id="93c06-134">Type of the Trigger.</span></span>
<span data-ttu-id="93c06-135">I valori possibili includono:' pre ',' post '</span><span class="sxs-lookup"><span data-stu-id="93c06-135">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="93c06-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93c06-136">-WhatIf</span></span>
<span data-ttu-id="93c06-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="93c06-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93c06-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="93c06-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93c06-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93c06-139">CommonParameters</span></span>
<span data-ttu-id="93c06-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93c06-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93c06-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="93c06-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93c06-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="93c06-142">INPUTS</span></span>

### <span data-ttu-id="93c06-143">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="93c06-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="93c06-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="93c06-144">OUTPUTS</span></span>

### <span data-ttu-id="93c06-145">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="93c06-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

### <span data-ttu-id="93c06-146">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="93c06-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="93c06-147">Note</span><span class="sxs-lookup"><span data-stu-id="93c06-147">NOTES</span></span>

## <span data-ttu-id="93c06-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="93c06-148">RELATED LINKS</span></span>
