---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbdatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabaseThroughput.md
ms.openlocfilehash: 1948bc5b5488c951861509c9b3c9ee7815eddec9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031827"
---
# <span data-ttu-id="e3b63-101">Update-AzCosmosDBMongoDBDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="e3b63-101">Update-AzCosmosDBMongoDBDatabaseThroughput</span></span>

## <span data-ttu-id="e3b63-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e3b63-102">SYNOPSIS</span></span>
<span data-ttu-id="e3b63-103">Aggiorna il valore della velocità effettiva di un database MongoDB CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="e3b63-103">Updates the throughput value of a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="e3b63-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3b63-104">SYNTAX</span></span>

### <span data-ttu-id="e3b63-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e3b63-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBDatabaseThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3b63-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3b63-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabaseThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3b63-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3b63-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabaseThroughput [-Name <String>] -InputObject <PSMongoDBDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3b63-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3b63-108">DESCRIPTION</span></span>
<span data-ttu-id="e3b63-109">Aggiorna il valore della velocità effettiva di un database MongoDB CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="e3b63-109">Updates the throughput value of a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="e3b63-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3b63-110">EXAMPLES</span></span>

### <span data-ttu-id="e3b63-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e3b63-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myDatabaseName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/mongodbDatabases/{myDatabaseName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="e3b63-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e3b63-112">PARAMETERS</span></span>

### <span data-ttu-id="e3b63-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e3b63-113">-AccountName</span></span>
<span data-ttu-id="e3b63-114">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="e3b63-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e3b63-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="e3b63-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="e3b63-116">Valore massimo della velocità effettiva se autoscale è abilitato.</span><span class="sxs-lookup"><span data-stu-id="e3b63-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="e3b63-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e3b63-117">-Confirm</span></span>
<span data-ttu-id="e3b63-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3b63-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3b63-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3b63-119">-DefaultProfile</span></span>
<span data-ttu-id="e3b63-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e3b63-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3b63-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3b63-121">-InputObject</span></span>
<span data-ttu-id="e3b63-122">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="e3b63-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="e3b63-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="e3b63-123">-Name</span></span>
<span data-ttu-id="e3b63-124">Nome database.</span><span class="sxs-lookup"><span data-stu-id="e3b63-124">Database name.</span></span>

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

### <span data-ttu-id="e3b63-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e3b63-125">-ParentObject</span></span>
<span data-ttu-id="e3b63-126">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="e3b63-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="e3b63-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3b63-127">-ResourceGroupName</span></span>
<span data-ttu-id="e3b63-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e3b63-128">Name of resource group.</span></span>

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

### <span data-ttu-id="e3b63-129">-Throughput</span><span class="sxs-lookup"><span data-stu-id="e3b63-129">-Throughput</span></span>
<span data-ttu-id="e3b63-130">La velocità effettiva del database Mongo (RU/s).</span><span class="sxs-lookup"><span data-stu-id="e3b63-130">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="e3b63-131">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="e3b63-131">Default value is 400.</span></span>

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

### <span data-ttu-id="e3b63-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3b63-132">-WhatIf</span></span>
<span data-ttu-id="e3b63-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3b63-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3b63-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3b63-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3b63-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3b63-135">CommonParameters</span></span>
<span data-ttu-id="e3b63-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3b63-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3b63-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3b63-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3b63-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e3b63-138">INPUTS</span></span>

### <span data-ttu-id="e3b63-139">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e3b63-139">None</span></span>

## <span data-ttu-id="e3b63-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3b63-140">OUTPUTS</span></span>

### <span data-ttu-id="e3b63-141">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="e3b63-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="e3b63-142">Note</span><span class="sxs-lookup"><span data-stu-id="e3b63-142">NOTES</span></span>

## <span data-ttu-id="e3b63-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3b63-143">RELATED LINKS</span></span>
