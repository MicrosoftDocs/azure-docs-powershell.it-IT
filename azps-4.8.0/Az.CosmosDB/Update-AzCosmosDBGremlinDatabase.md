---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: c52d76889de743a624ce60241a9495ef09ce2c4c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190512"
---
# <span data-ttu-id="4d147-101">Update-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="4d147-101">Update-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="4d147-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4d147-102">SYNOPSIS</span></span>
<span data-ttu-id="4d147-103">Aggiorna il database di CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="4d147-103">Updates the CosmosDB Gremlin Database.</span></span> <span data-ttu-id="4d147-104">Esegue un'operazione di patch lato client leggendo il database esistente.</span><span class="sxs-lookup"><span data-stu-id="4d147-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="4d147-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4d147-105">SYNTAX</span></span>

### <span data-ttu-id="4d147-106">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4d147-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d147-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d147-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4d147-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d147-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4d147-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4d147-109">DESCRIPTION</span></span>
<span data-ttu-id="4d147-110">Aggiorna il database di CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="4d147-110">Updates the CosmosDB Gremlin Database.</span></span> <span data-ttu-id="4d147-111">Esegue un'operazione di patch lato client leggendo il database esistente.</span><span class="sxs-lookup"><span data-stu-id="4d147-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="4d147-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4d147-112">EXAMPLES</span></span>

### <span data-ttu-id="4d147-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4d147-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -throughput updatedThroughputValueAsInteger

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

## <span data-ttu-id="4d147-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4d147-114">PARAMETERS</span></span>

### <span data-ttu-id="4d147-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4d147-115">-AccountName</span></span>
<span data-ttu-id="4d147-116">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="4d147-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="4d147-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="4d147-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="4d147-118">Valore massimo della velocità effettiva se autoscale è abilitato.</span><span class="sxs-lookup"><span data-stu-id="4d147-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="4d147-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4d147-119">-Confirm</span></span>
<span data-ttu-id="4d147-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d147-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d147-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d147-121">-DefaultProfile</span></span>
<span data-ttu-id="4d147-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4d147-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d147-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d147-123">-InputObject</span></span>
<span data-ttu-id="4d147-124">Oggetto database Gremlin.</span><span class="sxs-lookup"><span data-stu-id="4d147-124">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d147-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="4d147-125">-Name</span></span>
<span data-ttu-id="4d147-126">Nome database.</span><span class="sxs-lookup"><span data-stu-id="4d147-126">Database name.</span></span>

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

### <span data-ttu-id="4d147-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4d147-127">-ParentObject</span></span>
<span data-ttu-id="4d147-128">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="4d147-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="4d147-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d147-129">-ResourceGroupName</span></span>
<span data-ttu-id="4d147-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4d147-130">Name of resource group.</span></span>

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

### <span data-ttu-id="4d147-131">-Throughput</span><span class="sxs-lookup"><span data-stu-id="4d147-131">-Throughput</span></span>
<span data-ttu-id="4d147-132">La velocità effettiva del database Gremlin (RU/s).</span><span class="sxs-lookup"><span data-stu-id="4d147-132">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="4d147-133">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="4d147-133">Default value is 400.</span></span>

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

### <span data-ttu-id="4d147-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d147-134">-WhatIf</span></span>
<span data-ttu-id="4d147-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4d147-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d147-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4d147-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d147-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d147-137">CommonParameters</span></span>
<span data-ttu-id="4d147-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d147-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d147-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4d147-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d147-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4d147-140">INPUTS</span></span>

### <span data-ttu-id="4d147-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="4d147-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="4d147-142">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="4d147-142">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="4d147-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4d147-143">OUTPUTS</span></span>

### <span data-ttu-id="4d147-144">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="4d147-144">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="4d147-145">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="4d147-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="4d147-146">Note</span><span class="sxs-lookup"><span data-stu-id="4d147-146">NOTES</span></span>

## <span data-ttu-id="4d147-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4d147-147">RELATED LINKS</span></span>
