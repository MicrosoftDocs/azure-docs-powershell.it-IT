---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 535d6aa9f2ea6538e6b00f1334ce1114fad89f81
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299347"
---
# <span data-ttu-id="60cae-101">New-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="60cae-101">New-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="60cae-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="60cae-102">SYNOPSIS</span></span>
<span data-ttu-id="60cae-103">Crea un nuovo database di CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="60cae-103">Creates a new CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="60cae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="60cae-104">SYNTAX</span></span>

### <span data-ttu-id="60cae-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="60cae-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60cae-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="60cae-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBGremlinDatabase -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="60cae-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60cae-107">DESCRIPTION</span></span>
<span data-ttu-id="60cae-108">Crea un nuovo database di CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="60cae-108">Creates a new CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="60cae-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="60cae-109">EXAMPLES</span></span>

### <span data-ttu-id="60cae-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="60cae-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

## <span data-ttu-id="60cae-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="60cae-111">PARAMETERS</span></span>

### <span data-ttu-id="60cae-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="60cae-112">-AccountName</span></span>
<span data-ttu-id="60cae-113">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="60cae-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="60cae-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="60cae-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="60cae-115">Valore massimo della velocità effettiva se autoscale è abilitato.</span><span class="sxs-lookup"><span data-stu-id="60cae-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="60cae-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="60cae-116">-Confirm</span></span>
<span data-ttu-id="60cae-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60cae-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60cae-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60cae-118">-DefaultProfile</span></span>
<span data-ttu-id="60cae-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="60cae-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60cae-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="60cae-120">-Name</span></span>
<span data-ttu-id="60cae-121">Nome database.</span><span class="sxs-lookup"><span data-stu-id="60cae-121">Database name.</span></span>

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

### <span data-ttu-id="60cae-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="60cae-122">-ParentObject</span></span>
<span data-ttu-id="60cae-123">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="60cae-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="60cae-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60cae-124">-ResourceGroupName</span></span>
<span data-ttu-id="60cae-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="60cae-125">Name of resource group.</span></span>

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

### <span data-ttu-id="60cae-126">-Throughput</span><span class="sxs-lookup"><span data-stu-id="60cae-126">-Throughput</span></span>
<span data-ttu-id="60cae-127">La velocità effettiva del database Gremlin (RU/s).</span><span class="sxs-lookup"><span data-stu-id="60cae-127">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="60cae-128">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="60cae-128">Default value is 400.</span></span>

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

### <span data-ttu-id="60cae-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60cae-129">-WhatIf</span></span>
<span data-ttu-id="60cae-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60cae-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60cae-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60cae-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60cae-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60cae-132">CommonParameters</span></span>
<span data-ttu-id="60cae-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60cae-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60cae-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60cae-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60cae-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="60cae-135">INPUTS</span></span>

### <span data-ttu-id="60cae-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="60cae-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="60cae-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="60cae-137">OUTPUTS</span></span>

### <span data-ttu-id="60cae-138">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="60cae-138">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="60cae-139">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="60cae-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="60cae-140">Note</span><span class="sxs-lookup"><span data-stu-id="60cae-140">NOTES</span></span>

## <span data-ttu-id="60cae-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="60cae-141">RELATED LINKS</span></span>
