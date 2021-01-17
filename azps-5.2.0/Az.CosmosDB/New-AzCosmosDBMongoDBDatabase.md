---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: d4724976d5b4c702999fdd64c0811aa975c258d1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346255"
---
# <span data-ttu-id="94ff6-101">New-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="94ff6-101">New-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="94ff6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="94ff6-102">SYNOPSIS</span></span>
<span data-ttu-id="94ff6-103">Crea un nuovo database MongoDB di CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="94ff6-103">Creates a new CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="94ff6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="94ff6-104">SYNTAX</span></span>

### <span data-ttu-id="94ff6-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="94ff6-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94ff6-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="94ff6-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBMongoDBDatabase -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="94ff6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="94ff6-107">DESCRIPTION</span></span>
<span data-ttu-id="94ff6-108">Crea un nuovo database MongoDB di CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="94ff6-108">Creates a new CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="94ff6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="94ff6-109">EXAMPLES</span></span>

### <span data-ttu-id="94ff6-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="94ff6-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="94ff6-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="94ff6-111">PARAMETERS</span></span>

### <span data-ttu-id="94ff6-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="94ff6-112">-AccountName</span></span>
<span data-ttu-id="94ff6-113">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="94ff6-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="94ff6-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="94ff6-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="94ff6-115">Valore massimo della velocità effettiva se autoscale è abilitato.</span><span class="sxs-lookup"><span data-stu-id="94ff6-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="94ff6-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="94ff6-116">-Confirm</span></span>
<span data-ttu-id="94ff6-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94ff6-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94ff6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94ff6-118">-DefaultProfile</span></span>
<span data-ttu-id="94ff6-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="94ff6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94ff6-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="94ff6-120">-Name</span></span>
<span data-ttu-id="94ff6-121">Nome database.</span><span class="sxs-lookup"><span data-stu-id="94ff6-121">Database name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94ff6-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="94ff6-122">-ParentObject</span></span>
<span data-ttu-id="94ff6-123">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="94ff6-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="94ff6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94ff6-124">-ResourceGroupName</span></span>
<span data-ttu-id="94ff6-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="94ff6-125">Name of resource group.</span></span>

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

### <span data-ttu-id="94ff6-126">-Throughput</span><span class="sxs-lookup"><span data-stu-id="94ff6-126">-Throughput</span></span>
<span data-ttu-id="94ff6-127">La velocità effettiva del database Mongo (RU/s).</span><span class="sxs-lookup"><span data-stu-id="94ff6-127">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="94ff6-128">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="94ff6-128">Default value is 400.</span></span>

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

### <span data-ttu-id="94ff6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94ff6-129">-WhatIf</span></span>
<span data-ttu-id="94ff6-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="94ff6-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94ff6-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="94ff6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94ff6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94ff6-132">CommonParameters</span></span>
<span data-ttu-id="94ff6-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94ff6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94ff6-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94ff6-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94ff6-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="94ff6-135">INPUTS</span></span>

### <span data-ttu-id="94ff6-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="94ff6-136">None</span></span>

## <span data-ttu-id="94ff6-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="94ff6-137">OUTPUTS</span></span>

### <span data-ttu-id="94ff6-138">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="94ff6-138">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="94ff6-139">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="94ff6-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="94ff6-140">Note</span><span class="sxs-lookup"><span data-stu-id="94ff6-140">NOTES</span></span>

## <span data-ttu-id="94ff6-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="94ff6-141">RELATED LINKS</span></span>
