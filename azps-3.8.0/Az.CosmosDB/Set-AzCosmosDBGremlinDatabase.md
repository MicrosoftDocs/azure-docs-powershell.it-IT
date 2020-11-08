---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 18c1c215daa499514cf671f0c33956757dd56611
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022394"
---
# <span data-ttu-id="7ee64-101">Set-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="7ee64-101">Set-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="7ee64-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7ee64-102">SYNOPSIS</span></span>
<span data-ttu-id="7ee64-103">Imposta il database di CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="7ee64-103">Sets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="7ee64-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7ee64-104">SYNTAX</span></span>

### <span data-ttu-id="7ee64-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7ee64-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ee64-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ee64-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBGremlinDatabase -Name <String> [-Throughput <Int32>] -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ee64-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ee64-107">DESCRIPTION</span></span>
<span data-ttu-id="7ee64-108">Il cmdlet **set-AzCosmosDBGremlinDatabase** imposta il database di CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="7ee64-108">The **Set-AzCosmosDBGremlinDatabase** cmdlet sets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="7ee64-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7ee64-109">EXAMPLES</span></span>

### <span data-ttu-id="7ee64-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7ee64-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

<span data-ttu-id="7ee64-111">Oggetto Resource contiene _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="7ee64-111">Resource Object contains _rid, _ts, _etag.</span></span>

## <span data-ttu-id="7ee64-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7ee64-112">PARAMETERS</span></span>

### <span data-ttu-id="7ee64-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7ee64-113">-AccountName</span></span>
<span data-ttu-id="7ee64-114">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="7ee64-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7ee64-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7ee64-115">-Confirm</span></span>
<span data-ttu-id="7ee64-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ee64-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ee64-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ee64-117">-DefaultProfile</span></span>
<span data-ttu-id="7ee64-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7ee64-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ee64-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ee64-119">-InputObject</span></span>
<span data-ttu-id="7ee64-120">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="7ee64-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ee64-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="7ee64-121">-Name</span></span>
<span data-ttu-id="7ee64-122">Nome database.</span><span class="sxs-lookup"><span data-stu-id="7ee64-122">Database name.</span></span>

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

### <span data-ttu-id="7ee64-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ee64-123">-ResourceGroupName</span></span>
<span data-ttu-id="7ee64-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7ee64-124">Name of resource group.</span></span>

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

### <span data-ttu-id="7ee64-125">-Throughput</span><span class="sxs-lookup"><span data-stu-id="7ee64-125">-Throughput</span></span>
<span data-ttu-id="7ee64-126">La velocità effettiva del database Gremlin (RU/s).</span><span class="sxs-lookup"><span data-stu-id="7ee64-126">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="7ee64-127">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="7ee64-127">Default value is 400.</span></span>

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

### <span data-ttu-id="7ee64-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ee64-128">-WhatIf</span></span>
<span data-ttu-id="7ee64-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7ee64-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ee64-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7ee64-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ee64-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ee64-131">CommonParameters</span></span>
<span data-ttu-id="7ee64-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ee64-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ee64-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ee64-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ee64-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7ee64-134">INPUTS</span></span>

### <span data-ttu-id="7ee64-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="7ee64-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="7ee64-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7ee64-136">OUTPUTS</span></span>

### <span data-ttu-id="7ee64-137">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="7ee64-137">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="7ee64-138">Note</span><span class="sxs-lookup"><span data-stu-id="7ee64-138">NOTES</span></span>

## <span data-ttu-id="7ee64-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7ee64-139">RELATED LINKS</span></span>
