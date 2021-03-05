---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbmongodbdatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabaseThroughput.md
ms.openlocfilehash: 14fd294f0ebfcfe5f58a18ab4eeb433879f6a159
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977278"
---
# <span data-ttu-id="283e8-101">Update-AzCosmosDBMongoDBDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="283e8-101">Update-AzCosmosDBMongoDBDatabaseThroughput</span></span>

## <span data-ttu-id="283e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="283e8-102">SYNOPSIS</span></span>
<span data-ttu-id="283e8-103">Aggiorna il valore di velocità effettiva di un database MDBDb di Unirsi.</span><span class="sxs-lookup"><span data-stu-id="283e8-103">Updates the throughput value of a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="283e8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="283e8-104">SYNTAX</span></span>

### <span data-ttu-id="283e8-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="283e8-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBDatabaseThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="283e8-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="283e8-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabaseThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="283e8-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="283e8-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabaseThroughput [-Name <String>] -InputObject <PSMongoDBDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="283e8-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="283e8-108">DESCRIPTION</span></span>
<span data-ttu-id="283e8-109">Aggiorna il valore di velocità effettiva di un database MDBDb di Unirsi.</span><span class="sxs-lookup"><span data-stu-id="283e8-109">Updates the throughput value of a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="283e8-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="283e8-110">EXAMPLES</span></span>

### <span data-ttu-id="283e8-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="283e8-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myDatabaseName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/mongodbDatabases/{myDatabaseName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="283e8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="283e8-112">PARAMETERS</span></span>

### <span data-ttu-id="283e8-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="283e8-113">-AccountName</span></span>
<span data-ttu-id="283e8-114">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="283e8-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="283e8-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="283e8-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="283e8-116">Valore massimo di velocità effettiva se è abilitata la scalabilità automatica.</span><span class="sxs-lookup"><span data-stu-id="283e8-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="283e8-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="283e8-117">-Confirm</span></span>
<span data-ttu-id="283e8-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="283e8-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="283e8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="283e8-119">-DefaultProfile</span></span>
<span data-ttu-id="283e8-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="283e8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="283e8-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="283e8-121">-InputObject</span></span>
<span data-ttu-id="283e8-122">Oggetto Account Aziendale</span><span class="sxs-lookup"><span data-stu-id="283e8-122">CosmosDB Account object</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="283e8-123">-Name</span><span class="sxs-lookup"><span data-stu-id="283e8-123">-Name</span></span>
<span data-ttu-id="283e8-124">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="283e8-124">Database name.</span></span>

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

### <span data-ttu-id="283e8-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="283e8-125">-ParentObject</span></span>
<span data-ttu-id="283e8-126">Oggetto Account Aziendale</span><span class="sxs-lookup"><span data-stu-id="283e8-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="283e8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="283e8-127">-ResourceGroupName</span></span>
<span data-ttu-id="283e8-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="283e8-128">Name of resource group.</span></span>

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

### <span data-ttu-id="283e8-129">-Velocità effettiva</span><span class="sxs-lookup"><span data-stu-id="283e8-129">-Throughput</span></span>
<span data-ttu-id="283e8-130">Velocità effettiva del database mongo (RU).</span><span class="sxs-lookup"><span data-stu-id="283e8-130">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="283e8-131">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="283e8-131">Default value is 400.</span></span>

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

### <span data-ttu-id="283e8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="283e8-132">-WhatIf</span></span>
<span data-ttu-id="283e8-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="283e8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="283e8-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="283e8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="283e8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="283e8-135">CommonParameters</span></span>
<span data-ttu-id="283e8-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="283e8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="283e8-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="283e8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="283e8-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="283e8-138">INPUTS</span></span>

### <span data-ttu-id="283e8-139">Nessuno</span><span class="sxs-lookup"><span data-stu-id="283e8-139">None</span></span>

## <span data-ttu-id="283e8-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="283e8-140">OUTPUTS</span></span>

### <span data-ttu-id="283e8-141">Microsoft.Azure.Commands.EnterpriseDb.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="283e8-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="283e8-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="283e8-142">NOTES</span></span>

## <span data-ttu-id="283e8-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="283e8-143">RELATED LINKS</span></span>
