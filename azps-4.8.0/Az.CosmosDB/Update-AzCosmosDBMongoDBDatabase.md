---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: ed97687a03a40df8bbc965a21d7beb268cb67432
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190812"
---
# <span data-ttu-id="e721c-101">Update-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="e721c-101">Update-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="e721c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e721c-102">SYNOPSIS</span></span>
<span data-ttu-id="e721c-103">Aggiorna il database MongoDB di CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="e721c-103">Updates the CosmosDB MongoDB Database.</span></span> <span data-ttu-id="e721c-104">Esegue un'operazione di patch lato client leggendo il database esistente.</span><span class="sxs-lookup"><span data-stu-id="e721c-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="e721c-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e721c-105">SYNTAX</span></span>

### <span data-ttu-id="e721c-106">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e721c-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e721c-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e721c-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e721c-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e721c-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e721c-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e721c-109">DESCRIPTION</span></span>
<span data-ttu-id="e721c-110">Aggiorna il database MongoDB di CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="e721c-110">Updates the CosmosDB MongoDB Database.</span></span> <span data-ttu-id="e721c-111">Esegue un'operazione di patch lato client leggendo il database esistente.</span><span class="sxs-lookup"><span data-stu-id="e721c-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="e721c-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e721c-112">EXAMPLES</span></span>

### <span data-ttu-id="e721c-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e721c-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 600

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="e721c-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e721c-114">PARAMETERS</span></span>

### <span data-ttu-id="e721c-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e721c-115">-AccountName</span></span>
<span data-ttu-id="e721c-116">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="e721c-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e721c-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="e721c-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="e721c-118">Valore massimo della velocità effettiva se autoscale è abilitato.</span><span class="sxs-lookup"><span data-stu-id="e721c-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="e721c-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e721c-119">-Confirm</span></span>
<span data-ttu-id="e721c-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e721c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e721c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e721c-121">-DefaultProfile</span></span>
<span data-ttu-id="e721c-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e721c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e721c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e721c-123">-InputObject</span></span>
<span data-ttu-id="e721c-124">Oggetto di database Mongo.</span><span class="sxs-lookup"><span data-stu-id="e721c-124">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e721c-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="e721c-125">-Name</span></span>
<span data-ttu-id="e721c-126">Nome database.</span><span class="sxs-lookup"><span data-stu-id="e721c-126">Database name.</span></span>

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

### <span data-ttu-id="e721c-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e721c-127">-ParentObject</span></span>
<span data-ttu-id="e721c-128">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="e721c-128">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e721c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e721c-129">-ResourceGroupName</span></span>
<span data-ttu-id="e721c-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e721c-130">Name of resource group.</span></span>

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

### <span data-ttu-id="e721c-131">-Throughput</span><span class="sxs-lookup"><span data-stu-id="e721c-131">-Throughput</span></span>
<span data-ttu-id="e721c-132">La velocità effettiva del database Mongo (RU/s).</span><span class="sxs-lookup"><span data-stu-id="e721c-132">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="e721c-133">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="e721c-133">Default value is 400.</span></span>

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

### <span data-ttu-id="e721c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e721c-134">-WhatIf</span></span>
<span data-ttu-id="e721c-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e721c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e721c-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e721c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e721c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e721c-137">CommonParameters</span></span>
<span data-ttu-id="e721c-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e721c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e721c-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e721c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e721c-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e721c-140">INPUTS</span></span>

### <span data-ttu-id="e721c-141">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e721c-141">None</span></span>

## <span data-ttu-id="e721c-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e721c-142">OUTPUTS</span></span>

### <span data-ttu-id="e721c-143">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="e721c-143">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="e721c-144">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="e721c-144">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="e721c-145">Note</span><span class="sxs-lookup"><span data-stu-id="e721c-145">NOTES</span></span>

## <span data-ttu-id="e721c-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e721c-146">RELATED LINKS</span></span>
