---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 1c52d1f163f5f5d23f6f282a7f00a071a38761de
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98487803"
---
# <span data-ttu-id="d3cf4-101">Update-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d3cf4-101">Update-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="d3cf4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d3cf4-102">SYNOPSIS</span></span>
<span data-ttu-id="d3cf4-103">Aggiorna il database SQL di CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="d3cf4-103">Updates the CosmosDB Sql Database.</span></span> <span data-ttu-id="d3cf4-104">Esegue un'operazione di patch lato client leggendo il database esistente.</span><span class="sxs-lookup"><span data-stu-id="d3cf4-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="d3cf4-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3cf4-105">SYNTAX</span></span>

### <span data-ttu-id="d3cf4-106">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d3cf4-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3cf4-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3cf4-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d3cf4-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3cf4-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSSqlDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d3cf4-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3cf4-109">DESCRIPTION</span></span>
<span data-ttu-id="d3cf4-110">Aggiorna il database SQL di CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="d3cf4-110">Updates the CosmosDB Sql Database.</span></span> <span data-ttu-id="d3cf4-111">Esegue un'operazione di patch lato client leggendo il database esistente.</span><span class="sxs-lookup"><span data-stu-id="d3cf4-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="d3cf4-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3cf4-112">EXAMPLES</span></span>

### <span data-ttu-id="d3cf4-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d3cf4-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 900

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="d3cf4-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d3cf4-114">PARAMETERS</span></span>

### <span data-ttu-id="d3cf4-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d3cf4-115">-AccountName</span></span>
<span data-ttu-id="d3cf4-116">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="d3cf4-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d3cf4-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="d3cf4-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="d3cf4-118">Valore massimo della velocità effettiva se autoscale è abilitato.</span><span class="sxs-lookup"><span data-stu-id="d3cf4-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="d3cf4-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d3cf4-119">-Confirm</span></span>
<span data-ttu-id="d3cf4-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3cf4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3cf4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3cf4-121">-DefaultProfile</span></span>
<span data-ttu-id="d3cf4-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d3cf4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3cf4-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3cf4-123">-InputObject</span></span>
<span data-ttu-id="d3cf4-124">Oggetto database SQL.</span><span class="sxs-lookup"><span data-stu-id="d3cf4-124">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3cf4-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="d3cf4-125">-Name</span></span>
<span data-ttu-id="d3cf4-126">Nome database.</span><span class="sxs-lookup"><span data-stu-id="d3cf4-126">Database name.</span></span>

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

### <span data-ttu-id="d3cf4-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d3cf4-127">-ParentObject</span></span>
<span data-ttu-id="d3cf4-128">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="d3cf4-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="d3cf4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3cf4-129">-ResourceGroupName</span></span>
<span data-ttu-id="d3cf4-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d3cf4-130">Name of resource group.</span></span>

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

### <span data-ttu-id="d3cf4-131">-Throughput</span><span class="sxs-lookup"><span data-stu-id="d3cf4-131">-Throughput</span></span>
<span data-ttu-id="d3cf4-132">La velocità effettiva del database SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="d3cf4-132">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="d3cf4-133">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="d3cf4-133">Default value is 400.</span></span>

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

### <span data-ttu-id="d3cf4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3cf4-134">-WhatIf</span></span>
<span data-ttu-id="d3cf4-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3cf4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3cf4-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3cf4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3cf4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3cf4-137">CommonParameters</span></span>
<span data-ttu-id="d3cf4-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3cf4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3cf4-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3cf4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3cf4-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d3cf4-140">INPUTS</span></span>

### <span data-ttu-id="d3cf4-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="d3cf4-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="d3cf4-142">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="d3cf4-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="d3cf4-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3cf4-143">OUTPUTS</span></span>

### <span data-ttu-id="d3cf4-144">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="d3cf4-144">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="d3cf4-145">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="d3cf4-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="d3cf4-146">Note</span><span class="sxs-lookup"><span data-stu-id="d3cf4-146">NOTES</span></span>

## <span data-ttu-id="d3cf4-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3cf4-147">RELATED LINKS</span></span>
