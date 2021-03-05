---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: dbffec52b5c1b30f6b00febbc2e6c952beda669e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977293"
---
# <span data-ttu-id="de4a0-101">Update-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="de4a0-101">Update-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="de4a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de4a0-102">SYNOPSIS</span></span>
<span data-ttu-id="de4a0-103">Aggiorna il database Database Database DatabaseDbDbdb diDbDb.</span><span class="sxs-lookup"><span data-stu-id="de4a0-103">Updates the CosmosDB MongoDB Database.</span></span> <span data-ttu-id="de4a0-104">Esegue un'operazione di patch sul lato client leggendo il database esistente.</span><span class="sxs-lookup"><span data-stu-id="de4a0-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="de4a0-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="de4a0-105">SYNTAX</span></span>

### <span data-ttu-id="de4a0-106">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="de4a0-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de4a0-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="de4a0-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="de4a0-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="de4a0-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="de4a0-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="de4a0-109">DESCRIPTION</span></span>
<span data-ttu-id="de4a0-110">Aggiorna il database Database Database DatabaseDbDbdb diDbDb.</span><span class="sxs-lookup"><span data-stu-id="de4a0-110">Updates the CosmosDB MongoDB Database.</span></span> <span data-ttu-id="de4a0-111">Esegue un'operazione di patch sul lato client leggendo il database esistente.</span><span class="sxs-lookup"><span data-stu-id="de4a0-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="de4a0-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="de4a0-112">EXAMPLES</span></span>

### <span data-ttu-id="de4a0-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="de4a0-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 600

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="de4a0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de4a0-114">PARAMETERS</span></span>

### <span data-ttu-id="de4a0-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="de4a0-115">-AccountName</span></span>
<span data-ttu-id="de4a0-116">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="de4a0-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="de4a0-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="de4a0-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="de4a0-118">Valore massimo di velocità effettiva se è abilitata la scalabilità automatica.</span><span class="sxs-lookup"><span data-stu-id="de4a0-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="de4a0-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="de4a0-119">-Confirm</span></span>
<span data-ttu-id="de4a0-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de4a0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de4a0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de4a0-121">-DefaultProfile</span></span>
<span data-ttu-id="de4a0-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="de4a0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de4a0-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="de4a0-123">-InputObject</span></span>
<span data-ttu-id="de4a0-124">Oggetto database mongo.</span><span class="sxs-lookup"><span data-stu-id="de4a0-124">Mongo Database object.</span></span>

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

### <span data-ttu-id="de4a0-125">-Name</span><span class="sxs-lookup"><span data-stu-id="de4a0-125">-Name</span></span>
<span data-ttu-id="de4a0-126">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="de4a0-126">Database name.</span></span>

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

### <span data-ttu-id="de4a0-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="de4a0-127">-ParentObject</span></span>
<span data-ttu-id="de4a0-128">Oggetto Account Aziendale</span><span class="sxs-lookup"><span data-stu-id="de4a0-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="de4a0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de4a0-129">-ResourceGroupName</span></span>
<span data-ttu-id="de4a0-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="de4a0-130">Name of resource group.</span></span>

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

### <span data-ttu-id="de4a0-131">-Velocità effettiva</span><span class="sxs-lookup"><span data-stu-id="de4a0-131">-Throughput</span></span>
<span data-ttu-id="de4a0-132">Velocità effettiva del database mongo (RU).</span><span class="sxs-lookup"><span data-stu-id="de4a0-132">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="de4a0-133">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="de4a0-133">Default value is 400.</span></span>

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

### <span data-ttu-id="de4a0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de4a0-134">-WhatIf</span></span>
<span data-ttu-id="de4a0-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="de4a0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de4a0-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="de4a0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de4a0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de4a0-137">CommonParameters</span></span>
<span data-ttu-id="de4a0-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de4a0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de4a0-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="de4a0-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de4a0-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="de4a0-140">INPUTS</span></span>

### <span data-ttu-id="de4a0-141">Nessuno</span><span class="sxs-lookup"><span data-stu-id="de4a0-141">None</span></span>

## <span data-ttu-id="de4a0-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="de4a0-142">OUTPUTS</span></span>

### <span data-ttu-id="de4a0-143">Microsoft.Azure.Commands.EnterpriseDb.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="de4a0-143">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="de4a0-144">Microsoft.Azure.Commands.ExceptionsDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="de4a0-144">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="de4a0-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="de4a0-145">NOTES</span></span>

## <span data-ttu-id="de4a0-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="de4a0-146">RELATED LINKS</span></span>
