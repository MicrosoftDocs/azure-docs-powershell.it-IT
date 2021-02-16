---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: ed97687a03a40df8bbc965a21d7beb268cb67432
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198910"
---
# <span data-ttu-id="262a1-101">Update-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="262a1-101">Update-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="262a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="262a1-102">SYNOPSIS</span></span>
<span data-ttu-id="262a1-103">Aggiorna il database Database Database DatabaseDbDbdb diDbDb.</span><span class="sxs-lookup"><span data-stu-id="262a1-103">Updates the CosmosDB MongoDB Database.</span></span> <span data-ttu-id="262a1-104">Esegue un'operazione di patch sul lato client leggendo il database esistente.</span><span class="sxs-lookup"><span data-stu-id="262a1-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="262a1-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="262a1-105">SYNTAX</span></span>

### <span data-ttu-id="262a1-106">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="262a1-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="262a1-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="262a1-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="262a1-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="262a1-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="262a1-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="262a1-109">DESCRIPTION</span></span>
<span data-ttu-id="262a1-110">Aggiorna il database Database Database DatabaseDbDbdb diDbDb.</span><span class="sxs-lookup"><span data-stu-id="262a1-110">Updates the CosmosDB MongoDB Database.</span></span> <span data-ttu-id="262a1-111">Esegue un'operazione di patch sul lato client leggendo il database esistente.</span><span class="sxs-lookup"><span data-stu-id="262a1-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="262a1-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="262a1-112">EXAMPLES</span></span>

### <span data-ttu-id="262a1-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="262a1-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 600

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="262a1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="262a1-114">PARAMETERS</span></span>

### <span data-ttu-id="262a1-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="262a1-115">-AccountName</span></span>
<span data-ttu-id="262a1-116">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="262a1-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="262a1-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="262a1-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="262a1-118">Valore massimo di velocità effettiva se è abilitata la scalabilità automatica.</span><span class="sxs-lookup"><span data-stu-id="262a1-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="262a1-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="262a1-119">-Confirm</span></span>
<span data-ttu-id="262a1-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="262a1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="262a1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="262a1-121">-DefaultProfile</span></span>
<span data-ttu-id="262a1-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="262a1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="262a1-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="262a1-123">-InputObject</span></span>
<span data-ttu-id="262a1-124">Oggetto database mongo.</span><span class="sxs-lookup"><span data-stu-id="262a1-124">Mongo Database object.</span></span>

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

### <span data-ttu-id="262a1-125">-Name</span><span class="sxs-lookup"><span data-stu-id="262a1-125">-Name</span></span>
<span data-ttu-id="262a1-126">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="262a1-126">Database name.</span></span>

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

### <span data-ttu-id="262a1-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="262a1-127">-ParentObject</span></span>
<span data-ttu-id="262a1-128">Oggetto AccountDb Disa</span><span class="sxs-lookup"><span data-stu-id="262a1-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="262a1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="262a1-129">-ResourceGroupName</span></span>
<span data-ttu-id="262a1-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="262a1-130">Name of resource group.</span></span>

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

### <span data-ttu-id="262a1-131">-Velocità effettiva</span><span class="sxs-lookup"><span data-stu-id="262a1-131">-Throughput</span></span>
<span data-ttu-id="262a1-132">Velocità effettiva del database mongo (RU).</span><span class="sxs-lookup"><span data-stu-id="262a1-132">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="262a1-133">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="262a1-133">Default value is 400.</span></span>

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

### <span data-ttu-id="262a1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="262a1-134">-WhatIf</span></span>
<span data-ttu-id="262a1-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="262a1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="262a1-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="262a1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="262a1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="262a1-137">CommonParameters</span></span>
<span data-ttu-id="262a1-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="262a1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="262a1-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="262a1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="262a1-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="262a1-140">INPUTS</span></span>

### <span data-ttu-id="262a1-141">Nessuno</span><span class="sxs-lookup"><span data-stu-id="262a1-141">None</span></span>

## <span data-ttu-id="262a1-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="262a1-142">OUTPUTS</span></span>

### <span data-ttu-id="262a1-143">Microsoft.Azure.Commands.EnterpriseDb.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="262a1-143">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="262a1-144">Microsoft.Azure.Commands.ExceptionsDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="262a1-144">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="262a1-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="262a1-145">NOTES</span></span>

## <span data-ttu-id="262a1-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="262a1-146">RELATED LINKS</span></span>
