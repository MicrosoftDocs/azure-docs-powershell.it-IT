---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqldatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabaseThroughput.md
ms.openlocfilehash: 324350329b166ab3a41f7e2bd8b59af1b9efdcb7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372956"
---
# <span data-ttu-id="06f32-101">Update-AzCosmosDBSqlDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="06f32-101">Update-AzCosmosDBSqlDatabaseThroughput</span></span>

## <span data-ttu-id="06f32-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="06f32-102">SYNOPSIS</span></span>
<span data-ttu-id="06f32-103">Aggiorna il valore della velocità effettiva di un database SQL di CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="06f32-103">Updates the throughput value of a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="06f32-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="06f32-104">SYNTAX</span></span>

### <span data-ttu-id="06f32-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="06f32-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlDatabaseThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06f32-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="06f32-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabaseThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06f32-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="06f32-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabaseThroughput [-Name <String>] -InputObject <PSSqlDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06f32-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06f32-108">DESCRIPTION</span></span>
<span data-ttu-id="06f32-109">Aggiorna il valore della velocità effettiva di un database SQL di CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="06f32-109">Updates the throughput value of a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="06f32-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="06f32-110">EXAMPLES</span></span>

### <span data-ttu-id="06f32-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="06f32-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlDatabseThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myDatabaseName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/sqlDatabases/{myDatabaseName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="06f32-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="06f32-112">PARAMETERS</span></span>

### <span data-ttu-id="06f32-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="06f32-113">-AccountName</span></span>
<span data-ttu-id="06f32-114">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="06f32-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="06f32-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="06f32-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="06f32-116">Valore massimo della velocità effettiva se autoscale è abilitato.</span><span class="sxs-lookup"><span data-stu-id="06f32-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="06f32-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="06f32-117">-Confirm</span></span>
<span data-ttu-id="06f32-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06f32-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06f32-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06f32-119">-DefaultProfile</span></span>
<span data-ttu-id="06f32-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="06f32-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06f32-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06f32-121">-InputObject</span></span>
<span data-ttu-id="06f32-122">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="06f32-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="06f32-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="06f32-123">-Name</span></span>
<span data-ttu-id="06f32-124">Nome database.</span><span class="sxs-lookup"><span data-stu-id="06f32-124">Database name.</span></span>

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

### <span data-ttu-id="06f32-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="06f32-125">-ParentObject</span></span>
<span data-ttu-id="06f32-126">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="06f32-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="06f32-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06f32-127">-ResourceGroupName</span></span>
<span data-ttu-id="06f32-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="06f32-128">Name of resource group.</span></span>

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

### <span data-ttu-id="06f32-129">-Throughput</span><span class="sxs-lookup"><span data-stu-id="06f32-129">-Throughput</span></span>
<span data-ttu-id="06f32-130">La velocità effettiva del database SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="06f32-130">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="06f32-131">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="06f32-131">Default value is 400.</span></span>

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

### <span data-ttu-id="06f32-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06f32-132">-WhatIf</span></span>
<span data-ttu-id="06f32-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="06f32-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06f32-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="06f32-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06f32-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06f32-135">CommonParameters</span></span>
<span data-ttu-id="06f32-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06f32-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06f32-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06f32-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06f32-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="06f32-138">INPUTS</span></span>

### <span data-ttu-id="06f32-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="06f32-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="06f32-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="06f32-140">OUTPUTS</span></span>

### <span data-ttu-id="06f32-141">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="06f32-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="06f32-142">Note</span><span class="sxs-lookup"><span data-stu-id="06f32-142">NOTES</span></span>

## <span data-ttu-id="06f32-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="06f32-143">RELATED LINKS</span></span>
