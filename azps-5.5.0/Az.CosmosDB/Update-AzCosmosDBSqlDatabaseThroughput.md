---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqldatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabaseThroughput.md
ms.openlocfilehash: 324350329b166ab3a41f7e2bd8b59af1b9efdcb7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181230"
---
# <span data-ttu-id="8471b-101">Update-AzCosmosDBSqlDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="8471b-101">Update-AzCosmosDBSqlDatabaseThroughput</span></span>

## <span data-ttu-id="8471b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8471b-102">SYNOPSIS</span></span>
<span data-ttu-id="8471b-103">Aggiorna il valore di velocità effettiva di un database Sql database databasedb.</span><span class="sxs-lookup"><span data-stu-id="8471b-103">Updates the throughput value of a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="8471b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8471b-104">SYNTAX</span></span>

### <span data-ttu-id="8471b-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8471b-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlDatabaseThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8471b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8471b-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabaseThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8471b-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8471b-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabaseThroughput [-Name <String>] -InputObject <PSSqlDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8471b-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8471b-108">DESCRIPTION</span></span>
<span data-ttu-id="8471b-109">Aggiorna il valore di velocità effettiva di un database Sql database databasedb.</span><span class="sxs-lookup"><span data-stu-id="8471b-109">Updates the throughput value of a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="8471b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8471b-110">EXAMPLES</span></span>

### <span data-ttu-id="8471b-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8471b-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlDatabseThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myDatabaseName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/sqlDatabases/{myDatabaseName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="8471b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8471b-112">PARAMETERS</span></span>

### <span data-ttu-id="8471b-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8471b-113">-AccountName</span></span>
<span data-ttu-id="8471b-114">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="8471b-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="8471b-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="8471b-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="8471b-116">Valore massimo di velocità effettiva se è abilitata la scalabilità automatica.</span><span class="sxs-lookup"><span data-stu-id="8471b-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="8471b-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8471b-117">-Confirm</span></span>
<span data-ttu-id="8471b-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8471b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8471b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8471b-119">-DefaultProfile</span></span>
<span data-ttu-id="8471b-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8471b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8471b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8471b-121">-InputObject</span></span>
<span data-ttu-id="8471b-122">Oggetto AccountDb Disa</span><span class="sxs-lookup"><span data-stu-id="8471b-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="8471b-123">-Name</span><span class="sxs-lookup"><span data-stu-id="8471b-123">-Name</span></span>
<span data-ttu-id="8471b-124">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="8471b-124">Database name.</span></span>

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

### <span data-ttu-id="8471b-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8471b-125">-ParentObject</span></span>
<span data-ttu-id="8471b-126">Oggetto AccountDb Disa</span><span class="sxs-lookup"><span data-stu-id="8471b-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="8471b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8471b-127">-ResourceGroupName</span></span>
<span data-ttu-id="8471b-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8471b-128">Name of resource group.</span></span>

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

### <span data-ttu-id="8471b-129">-Velocità effettiva</span><span class="sxs-lookup"><span data-stu-id="8471b-129">-Throughput</span></span>
<span data-ttu-id="8471b-130">Velocità effettiva di SQL database (RU/S).</span><span class="sxs-lookup"><span data-stu-id="8471b-130">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="8471b-131">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="8471b-131">Default value is 400.</span></span>

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

### <span data-ttu-id="8471b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8471b-132">-WhatIf</span></span>
<span data-ttu-id="8471b-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8471b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8471b-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8471b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8471b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8471b-135">CommonParameters</span></span>
<span data-ttu-id="8471b-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8471b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8471b-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8471b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8471b-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="8471b-138">INPUTS</span></span>

### <span data-ttu-id="8471b-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="8471b-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="8471b-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8471b-140">OUTPUTS</span></span>

### <span data-ttu-id="8471b-141">Microsoft.Azure.Commands.EnterpriseDb.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="8471b-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="8471b-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="8471b-142">NOTES</span></span>

## <span data-ttu-id="8471b-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8471b-143">RELATED LINKS</span></span>
