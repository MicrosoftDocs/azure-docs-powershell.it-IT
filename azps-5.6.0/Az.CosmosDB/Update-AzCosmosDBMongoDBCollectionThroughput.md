---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollectionthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
ms.openlocfilehash: 66ca19099d4562da3add57411a16be1a0573ea02
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977294"
---
# <span data-ttu-id="fee51-101">Update-AzCosmosDBMongoDBCollectionThroughput</span><span class="sxs-lookup"><span data-stu-id="fee51-101">Update-AzCosmosDBMongoDBCollectionThroughput</span></span>

## <span data-ttu-id="fee51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fee51-102">SYNOPSIS</span></span>
<span data-ttu-id="fee51-103">Aggiorna il valore di velocità effettiva di una raccolta Dibdbdb di UnisDB.</span><span class="sxs-lookup"><span data-stu-id="fee51-103">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="fee51-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fee51-104">SYNTAX</span></span>

### <span data-ttu-id="fee51-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fee51-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fee51-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fee51-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -ParentObject <PSMongoDBDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fee51-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fee51-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -InputObject <PSMongoDBCollectionGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fee51-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fee51-108">DESCRIPTION</span></span>
<span data-ttu-id="fee51-109">Aggiorna il valore di velocità effettiva di una raccolta Diedb MongoDB.</span><span class="sxs-lookup"><span data-stu-id="fee51-109">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="fee51-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fee51-110">EXAMPLES</span></span>

### <span data-ttu-id="fee51-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fee51-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollectionThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myCollectionName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/mongodbDatabase/{mydatabaseName}/collections/{myCollectionName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

<span data-ttu-id="fee51-112">{{ Aggiungi la descrizione di esempio qui }}</span><span class="sxs-lookup"><span data-stu-id="fee51-112">{{ Add example description here }}</span></span>

## <span data-ttu-id="fee51-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fee51-113">PARAMETERS</span></span>

### <span data-ttu-id="fee51-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fee51-114">-AccountName</span></span>
<span data-ttu-id="fee51-115">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="fee51-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="fee51-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="fee51-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="fee51-117">Valore massimo di velocità effettiva se è abilitata la scalabilità automatica.</span><span class="sxs-lookup"><span data-stu-id="fee51-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="fee51-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fee51-118">-Confirm</span></span>
<span data-ttu-id="fee51-119">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fee51-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fee51-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fee51-120">-DatabaseName</span></span>
<span data-ttu-id="fee51-121">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="fee51-121">Database name.</span></span>

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

### <span data-ttu-id="fee51-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fee51-122">-DefaultProfile</span></span>
<span data-ttu-id="fee51-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fee51-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fee51-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fee51-124">-InputObject</span></span>
<span data-ttu-id="fee51-125">Oggetto database mongo.</span><span class="sxs-lookup"><span data-stu-id="fee51-125">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fee51-126">-Name</span><span class="sxs-lookup"><span data-stu-id="fee51-126">-Name</span></span>
<span data-ttu-id="fee51-127">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="fee51-127">Collection name.</span></span>

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

### <span data-ttu-id="fee51-128">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="fee51-128">-ParentObject</span></span>
<span data-ttu-id="fee51-129">Oggetto database mongo.</span><span class="sxs-lookup"><span data-stu-id="fee51-129">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fee51-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fee51-130">-ResourceGroupName</span></span>
<span data-ttu-id="fee51-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fee51-131">Name of resource group.</span></span>

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

### <span data-ttu-id="fee51-132">-Velocità effettiva</span><span class="sxs-lookup"><span data-stu-id="fee51-132">-Throughput</span></span>
<span data-ttu-id="fee51-133">Velocità effettiva del contenitore SQL (RU/S).</span><span class="sxs-lookup"><span data-stu-id="fee51-133">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="fee51-134">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="fee51-134">Default value is 400.</span></span>

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

### <span data-ttu-id="fee51-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fee51-135">-WhatIf</span></span>
<span data-ttu-id="fee51-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fee51-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fee51-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fee51-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fee51-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fee51-138">CommonParameters</span></span>
<span data-ttu-id="fee51-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fee51-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fee51-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fee51-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fee51-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="fee51-141">INPUTS</span></span>

### <span data-ttu-id="fee51-142">Microsoft.Azure.Commands.EnterpriseDb.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="fee51-142">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="fee51-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fee51-143">OUTPUTS</span></span>

### <span data-ttu-id="fee51-144">Microsoft.Azure.Commands.EnterpriseDb.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="fee51-144">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="fee51-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="fee51-145">NOTES</span></span>

## <span data-ttu-id="fee51-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fee51-146">RELATED LINKS</span></span>
