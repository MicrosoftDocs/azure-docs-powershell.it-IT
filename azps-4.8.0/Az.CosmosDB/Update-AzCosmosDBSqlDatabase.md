---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 1c52d1f163f5f5d23f6f282a7f00a071a38761de
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190810"
---
# <span data-ttu-id="7e123-101">Update-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7e123-101">Update-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="7e123-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7e123-102">SYNOPSIS</span></span>
<span data-ttu-id="7e123-103">Aggiorna il database SQL di CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="7e123-103">Updates the CosmosDB Sql Database.</span></span> <span data-ttu-id="7e123-104">Esegue un'operazione di patch lato client leggendo il database esistente.</span><span class="sxs-lookup"><span data-stu-id="7e123-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="7e123-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7e123-105">SYNTAX</span></span>

### <span data-ttu-id="7e123-106">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7e123-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e123-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e123-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7e123-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e123-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSSqlDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7e123-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e123-109">DESCRIPTION</span></span>
<span data-ttu-id="7e123-110">Aggiorna il database SQL di CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="7e123-110">Updates the CosmosDB Sql Database.</span></span> <span data-ttu-id="7e123-111">Esegue un'operazione di patch lato client leggendo il database esistente.</span><span class="sxs-lookup"><span data-stu-id="7e123-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="7e123-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7e123-112">EXAMPLES</span></span>

### <span data-ttu-id="7e123-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7e123-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 900

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="7e123-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7e123-114">PARAMETERS</span></span>

### <span data-ttu-id="7e123-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7e123-115">-AccountName</span></span>
<span data-ttu-id="7e123-116">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="7e123-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7e123-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="7e123-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="7e123-118">Valore massimo della velocità effettiva se autoscale è abilitato.</span><span class="sxs-lookup"><span data-stu-id="7e123-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="7e123-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7e123-119">-Confirm</span></span>
<span data-ttu-id="7e123-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e123-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e123-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e123-121">-DefaultProfile</span></span>
<span data-ttu-id="7e123-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7e123-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e123-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e123-123">-InputObject</span></span>
<span data-ttu-id="7e123-124">Oggetto database SQL.</span><span class="sxs-lookup"><span data-stu-id="7e123-124">Sql Database object.</span></span>

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

### <span data-ttu-id="7e123-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="7e123-125">-Name</span></span>
<span data-ttu-id="7e123-126">Nome database.</span><span class="sxs-lookup"><span data-stu-id="7e123-126">Database name.</span></span>

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

### <span data-ttu-id="7e123-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7e123-127">-ParentObject</span></span>
<span data-ttu-id="7e123-128">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="7e123-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="7e123-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e123-129">-ResourceGroupName</span></span>
<span data-ttu-id="7e123-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7e123-130">Name of resource group.</span></span>

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

### <span data-ttu-id="7e123-131">-Throughput</span><span class="sxs-lookup"><span data-stu-id="7e123-131">-Throughput</span></span>
<span data-ttu-id="7e123-132">La velocità effettiva del database SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="7e123-132">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="7e123-133">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="7e123-133">Default value is 400.</span></span>

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

### <span data-ttu-id="7e123-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e123-134">-WhatIf</span></span>
<span data-ttu-id="7e123-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7e123-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e123-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7e123-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e123-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e123-137">CommonParameters</span></span>
<span data-ttu-id="7e123-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e123-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e123-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e123-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e123-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7e123-140">INPUTS</span></span>

### <span data-ttu-id="7e123-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="7e123-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="7e123-142">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="7e123-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="7e123-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7e123-143">OUTPUTS</span></span>

### <span data-ttu-id="7e123-144">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="7e123-144">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="7e123-145">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="7e123-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="7e123-146">Note</span><span class="sxs-lookup"><span data-stu-id="7e123-146">NOTES</span></span>

## <span data-ttu-id="7e123-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7e123-147">RELATED LINKS</span></span>
