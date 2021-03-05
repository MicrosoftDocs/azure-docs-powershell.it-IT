---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbgremlindatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabaseThroughput.md
ms.openlocfilehash: 21dd30bd60e9b26fc306ed99b31cd3c52d9fdf8f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977342"
---
# <span data-ttu-id="732f2-101">Update-AzCosmosDBGremlinDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="732f2-101">Update-AzCosmosDBGremlinDatabaseThroughput</span></span>

## <span data-ttu-id="732f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="732f2-102">SYNOPSIS</span></span>
<span data-ttu-id="732f2-103">Aggiorna il valore di velocità effettiva di un database DiametiDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="732f2-103">Updates the throughput value of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="732f2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="732f2-104">SYNTAX</span></span>

### <span data-ttu-id="732f2-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="732f2-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="732f2-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="732f2-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="732f2-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="732f2-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -InputObject <PSGremlinDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="732f2-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="732f2-108">DESCRIPTION</span></span>
<span data-ttu-id="732f2-109">Aggiorna il valore di velocità effettiva di un database DiametiDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="732f2-109">Updates the throughput value of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="732f2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="732f2-110">EXAMPLES</span></span>

### <span data-ttu-id="732f2-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="732f2-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinDatabaseThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myDatabaseName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabases/{myDatabaseName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="732f2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="732f2-112">PARAMETERS</span></span>

### <span data-ttu-id="732f2-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="732f2-113">-AccountName</span></span>
<span data-ttu-id="732f2-114">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="732f2-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="732f2-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="732f2-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="732f2-116">Valore massimo di velocità effettiva se è abilitata la scalabilità automatica.</span><span class="sxs-lookup"><span data-stu-id="732f2-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="732f2-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="732f2-117">-Confirm</span></span>
<span data-ttu-id="732f2-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="732f2-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="732f2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="732f2-119">-DefaultProfile</span></span>
<span data-ttu-id="732f2-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="732f2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="732f2-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="732f2-121">-InputObject</span></span>
<span data-ttu-id="732f2-122">Oggetto AccountDb Disa</span><span class="sxs-lookup"><span data-stu-id="732f2-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="732f2-123">-Name</span><span class="sxs-lookup"><span data-stu-id="732f2-123">-Name</span></span>
<span data-ttu-id="732f2-124">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="732f2-124">Database name.</span></span>

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

### <span data-ttu-id="732f2-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="732f2-125">-ParentObject</span></span>
<span data-ttu-id="732f2-126">Oggetto AccountDb Disa</span><span class="sxs-lookup"><span data-stu-id="732f2-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="732f2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="732f2-127">-ResourceGroupName</span></span>
<span data-ttu-id="732f2-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="732f2-128">Name of resource group.</span></span>

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

### <span data-ttu-id="732f2-129">-Velocità effettiva</span><span class="sxs-lookup"><span data-stu-id="732f2-129">-Throughput</span></span>
<span data-ttu-id="732f2-130">Velocità effettiva del database di Gremlin (RU/s).</span><span class="sxs-lookup"><span data-stu-id="732f2-130">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="732f2-131">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="732f2-131">Default value is 400.</span></span>

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

### <span data-ttu-id="732f2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="732f2-132">-WhatIf</span></span>
<span data-ttu-id="732f2-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="732f2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="732f2-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="732f2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="732f2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="732f2-135">CommonParameters</span></span>
<span data-ttu-id="732f2-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="732f2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="732f2-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="732f2-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="732f2-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="732f2-138">INPUTS</span></span>

### <span data-ttu-id="732f2-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="732f2-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="732f2-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="732f2-140">OUTPUTS</span></span>

### <span data-ttu-id="732f2-141">Microsoft.Azure.Commands.EnterpriseDb.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="732f2-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="732f2-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="732f2-142">NOTES</span></span>

## <span data-ttu-id="732f2-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="732f2-143">RELATED LINKS</span></span>
