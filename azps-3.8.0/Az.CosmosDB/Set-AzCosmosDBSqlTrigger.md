---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: a67b2a665f763c32876177414a347270f557c914
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018508"
---
# <span data-ttu-id="40aed-101">Set-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="40aed-101">Set-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="40aed-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="40aed-102">SYNOPSIS</span></span>
<span data-ttu-id="40aed-103">Crea un nuovo o aggiorna un trigger SQL CosmosDB esistente.</span><span class="sxs-lookup"><span data-stu-id="40aed-103">Creates a new or updates an existing CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="40aed-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="40aed-104">SYNTAX</span></span>

### <span data-ttu-id="40aed-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="40aed-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40aed-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="40aed-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBSqlTrigger -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 -InputObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="40aed-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="40aed-107">DESCRIPTION</span></span>
<span data-ttu-id="40aed-108">Il cmdlet **set-AzCosmosDBSqlTrigger** crea un nuovo o aggiorna un trigger SQL CosmosDB esistente.</span><span class="sxs-lookup"><span data-stu-id="40aed-108">The **Set-AzCosmosDBSqlTrigger** cmdlet creates a new or updates an existing CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="40aed-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="40aed-109">EXAMPLES</span></span>

### <span data-ttu-id="40aed-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="40aed-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBSqlTrigger -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {triggerName} -ContainerName {containerName} -Body {sampleBody}

Name                   : {triggerName}
Id                     : {triggerId}
SqlTriggerGetResultsId :
Body                   :
TriggerType            :
TriggerOperation       :
_rid                   :
_ts                    :
_etag                  :
```

## <span data-ttu-id="40aed-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="40aed-111">PARAMETERS</span></span>

### <span data-ttu-id="40aed-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="40aed-112">-AccountName</span></span>
<span data-ttu-id="40aed-113">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="40aed-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="40aed-114">-Body</span><span class="sxs-lookup"><span data-stu-id="40aed-114">-Body</span></span>
<span data-ttu-id="40aed-115">Il corpo del trigger.</span><span class="sxs-lookup"><span data-stu-id="40aed-115">The body of the Trigger.</span></span>

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

### <span data-ttu-id="40aed-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="40aed-116">-Confirm</span></span>
<span data-ttu-id="40aed-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40aed-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40aed-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="40aed-118">-ContainerName</span></span>
<span data-ttu-id="40aed-119">Nome contenitore.</span><span class="sxs-lookup"><span data-stu-id="40aed-119">Container name.</span></span>

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

### <span data-ttu-id="40aed-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="40aed-120">-DatabaseName</span></span>
<span data-ttu-id="40aed-121">Nome database.</span><span class="sxs-lookup"><span data-stu-id="40aed-121">Database name.</span></span>

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

### <span data-ttu-id="40aed-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40aed-122">-DefaultProfile</span></span>
<span data-ttu-id="40aed-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="40aed-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40aed-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40aed-124">-InputObject</span></span>
<span data-ttu-id="40aed-125">Oggetto contenitore SQL.</span><span class="sxs-lookup"><span data-stu-id="40aed-125">Sql Container object.</span></span>

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

### <span data-ttu-id="40aed-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="40aed-126">-Name</span></span>
<span data-ttu-id="40aed-127">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="40aed-127">Trigger name.</span></span>

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

### <span data-ttu-id="40aed-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40aed-128">-ResourceGroupName</span></span>
<span data-ttu-id="40aed-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="40aed-129">Name of resource group.</span></span>

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

### <span data-ttu-id="40aed-130">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="40aed-130">-TriggerOperation</span></span>
<span data-ttu-id="40aed-131">Operazione a cui è associato il trigger.</span><span class="sxs-lookup"><span data-stu-id="40aed-131">The operation the trigger is associated with.</span></span>
<span data-ttu-id="40aed-132">I valori possibili includono: "tutti", "Crea", "Aggiorna", "Elimina", "Sostituisci"</span><span class="sxs-lookup"><span data-stu-id="40aed-132">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="40aed-133">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="40aed-133">-TriggerType</span></span>
<span data-ttu-id="40aed-134">Tipo di trigger.</span><span class="sxs-lookup"><span data-stu-id="40aed-134">Type of the Trigger.</span></span>
<span data-ttu-id="40aed-135">I valori possibili includono:' pre ',' post '</span><span class="sxs-lookup"><span data-stu-id="40aed-135">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="40aed-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40aed-136">-WhatIf</span></span>
<span data-ttu-id="40aed-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="40aed-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="40aed-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="40aed-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40aed-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40aed-139">CommonParameters</span></span>
<span data-ttu-id="40aed-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40aed-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40aed-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40aed-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40aed-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="40aed-142">INPUTS</span></span>

### <span data-ttu-id="40aed-143">Nessuno</span><span class="sxs-lookup"><span data-stu-id="40aed-143">None</span></span>

## <span data-ttu-id="40aed-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="40aed-144">OUTPUTS</span></span>

### <span data-ttu-id="40aed-145">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="40aed-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="40aed-146">Note</span><span class="sxs-lookup"><span data-stu-id="40aed-146">NOTES</span></span>

## <span data-ttu-id="40aed-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="40aed-147">RELATED LINKS</span></span>
