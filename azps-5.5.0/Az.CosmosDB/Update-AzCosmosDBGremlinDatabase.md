---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: c52d76889de743a624ce60241a9495ef09ce2c4c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181294"
---
# <span data-ttu-id="2e70a-101">Update-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="2e70a-101">Update-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="2e70a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e70a-102">SYNOPSIS</span></span>
<span data-ttu-id="2e70a-103">Aggiorna il database DellesDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="2e70a-103">Updates the CosmosDB Gremlin Database.</span></span> <span data-ttu-id="2e70a-104">Esegue un'operazione di patch sul lato client leggendo il database esistente.</span><span class="sxs-lookup"><span data-stu-id="2e70a-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="2e70a-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2e70a-105">SYNTAX</span></span>

### <span data-ttu-id="2e70a-106">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2e70a-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e70a-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e70a-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2e70a-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e70a-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2e70a-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2e70a-109">DESCRIPTION</span></span>
<span data-ttu-id="2e70a-110">Aggiorna il database DellesDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="2e70a-110">Updates the CosmosDB Gremlin Database.</span></span> <span data-ttu-id="2e70a-111">Esegue un'operazione di patch sul lato client leggendo il database esistente.</span><span class="sxs-lookup"><span data-stu-id="2e70a-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="2e70a-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2e70a-112">EXAMPLES</span></span>

### <span data-ttu-id="2e70a-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2e70a-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -throughput updatedThroughputValueAsInteger

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

## <span data-ttu-id="2e70a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e70a-114">PARAMETERS</span></span>

### <span data-ttu-id="2e70a-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2e70a-115">-AccountName</span></span>
<span data-ttu-id="2e70a-116">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="2e70a-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2e70a-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="2e70a-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="2e70a-118">Valore massimo di velocità effettiva se è abilitata la scalabilità automatica.</span><span class="sxs-lookup"><span data-stu-id="2e70a-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="2e70a-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e70a-119">-Confirm</span></span>
<span data-ttu-id="2e70a-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e70a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e70a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e70a-121">-DefaultProfile</span></span>
<span data-ttu-id="2e70a-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2e70a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e70a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e70a-123">-InputObject</span></span>
<span data-ttu-id="2e70a-124">Oggetto di database Gremlin.</span><span class="sxs-lookup"><span data-stu-id="2e70a-124">Gremlin Database object.</span></span>

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

### <span data-ttu-id="2e70a-125">-Name</span><span class="sxs-lookup"><span data-stu-id="2e70a-125">-Name</span></span>
<span data-ttu-id="2e70a-126">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="2e70a-126">Database name.</span></span>

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

### <span data-ttu-id="2e70a-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="2e70a-127">-ParentObject</span></span>
<span data-ttu-id="2e70a-128">Oggetto AccountDb Disa</span><span class="sxs-lookup"><span data-stu-id="2e70a-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="2e70a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e70a-129">-ResourceGroupName</span></span>
<span data-ttu-id="2e70a-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2e70a-130">Name of resource group.</span></span>

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

### <span data-ttu-id="2e70a-131">-Velocità effettiva</span><span class="sxs-lookup"><span data-stu-id="2e70a-131">-Throughput</span></span>
<span data-ttu-id="2e70a-132">Velocità effettiva del database di Gremlin (RU/s).</span><span class="sxs-lookup"><span data-stu-id="2e70a-132">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="2e70a-133">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="2e70a-133">Default value is 400.</span></span>

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

### <span data-ttu-id="2e70a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e70a-134">-WhatIf</span></span>
<span data-ttu-id="2e70a-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2e70a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e70a-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2e70a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e70a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e70a-137">CommonParameters</span></span>
<span data-ttu-id="2e70a-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e70a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e70a-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2e70a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e70a-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="2e70a-140">INPUTS</span></span>

### <span data-ttu-id="2e70a-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="2e70a-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="2e70a-142">Microsoft.Azure.Commands.EnterpriseDb.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="2e70a-142">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="2e70a-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2e70a-143">OUTPUTS</span></span>

### <span data-ttu-id="2e70a-144">Microsoft.Azure.Commands.EnterpriseDb.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="2e70a-144">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="2e70a-145">Microsoft.Azure.Commands.ExceptionsDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="2e70a-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="2e70a-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="2e70a-146">NOTES</span></span>

## <span data-ttu-id="2e70a-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2e70a-147">RELATED LINKS</span></span>
