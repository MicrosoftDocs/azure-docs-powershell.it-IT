---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 535d6aa9f2ea6538e6b00f1334ce1114fad89f81
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348991"
---
# <span data-ttu-id="f44ad-101">New-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="f44ad-101">New-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="f44ad-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f44ad-102">SYNOPSIS</span></span>
<span data-ttu-id="f44ad-103">Crea un nuovo database di CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="f44ad-103">Creates a new CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="f44ad-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f44ad-104">SYNTAX</span></span>

### <span data-ttu-id="f44ad-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f44ad-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f44ad-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f44ad-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBGremlinDatabase -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f44ad-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f44ad-107">DESCRIPTION</span></span>
<span data-ttu-id="f44ad-108">Crea un nuovo database di CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="f44ad-108">Creates a new CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="f44ad-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f44ad-109">EXAMPLES</span></span>

### <span data-ttu-id="f44ad-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f44ad-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

## <span data-ttu-id="f44ad-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f44ad-111">PARAMETERS</span></span>

### <span data-ttu-id="f44ad-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f44ad-112">-AccountName</span></span>
<span data-ttu-id="f44ad-113">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="f44ad-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f44ad-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="f44ad-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="f44ad-115">Valore massimo della velocità effettiva se autoscale è abilitato.</span><span class="sxs-lookup"><span data-stu-id="f44ad-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="f44ad-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f44ad-116">-Confirm</span></span>
<span data-ttu-id="f44ad-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f44ad-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f44ad-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f44ad-118">-DefaultProfile</span></span>
<span data-ttu-id="f44ad-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f44ad-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f44ad-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="f44ad-120">-Name</span></span>
<span data-ttu-id="f44ad-121">Nome database.</span><span class="sxs-lookup"><span data-stu-id="f44ad-121">Database name.</span></span>

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

### <span data-ttu-id="f44ad-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f44ad-122">-ParentObject</span></span>
<span data-ttu-id="f44ad-123">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="f44ad-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="f44ad-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f44ad-124">-ResourceGroupName</span></span>
<span data-ttu-id="f44ad-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f44ad-125">Name of resource group.</span></span>

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

### <span data-ttu-id="f44ad-126">-Throughput</span><span class="sxs-lookup"><span data-stu-id="f44ad-126">-Throughput</span></span>
<span data-ttu-id="f44ad-127">La velocità effettiva del database Gremlin (RU/s).</span><span class="sxs-lookup"><span data-stu-id="f44ad-127">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="f44ad-128">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="f44ad-128">Default value is 400.</span></span>

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

### <span data-ttu-id="f44ad-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f44ad-129">-WhatIf</span></span>
<span data-ttu-id="f44ad-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f44ad-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f44ad-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f44ad-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f44ad-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f44ad-132">CommonParameters</span></span>
<span data-ttu-id="f44ad-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f44ad-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f44ad-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f44ad-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f44ad-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f44ad-135">INPUTS</span></span>

### <span data-ttu-id="f44ad-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="f44ad-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="f44ad-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f44ad-137">OUTPUTS</span></span>

### <span data-ttu-id="f44ad-138">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="f44ad-138">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="f44ad-139">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="f44ad-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="f44ad-140">Note</span><span class="sxs-lookup"><span data-stu-id="f44ad-140">NOTES</span></span>

## <span data-ttu-id="f44ad-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f44ad-141">RELATED LINKS</span></span>
