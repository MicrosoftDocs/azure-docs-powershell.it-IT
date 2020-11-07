---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlindatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabaseThroughput.md
ms.openlocfilehash: 75ea7849424d8587f4eb4151bde63f31ea35676f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93865498"
---
# <span data-ttu-id="9fbaf-101">Update-AzCosmosDBGremlinDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="9fbaf-101">Update-AzCosmosDBGremlinDatabaseThroughput</span></span>

## <span data-ttu-id="9fbaf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9fbaf-102">SYNOPSIS</span></span>
<span data-ttu-id="9fbaf-103">Aggiorna il valore di throughput di un database di CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="9fbaf-103">Updates the throughput value of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="9fbaf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9fbaf-104">SYNTAX</span></span>

### <span data-ttu-id="9fbaf-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9fbaf-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fbaf-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fbaf-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSDatabaseAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9fbaf-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fbaf-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9fbaf-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9fbaf-108">EXAMPLES</span></span>

### <span data-ttu-id="9fbaf-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9fbaf-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinDatabaseThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myDatabaseName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabases/{myDatabaseName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="9fbaf-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9fbaf-110">PARAMETERS</span></span>

### <span data-ttu-id="9fbaf-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9fbaf-111">-AccountName</span></span>
<span data-ttu-id="9fbaf-112">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="9fbaf-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9fbaf-113">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9fbaf-113">-Confirm</span></span>
<span data-ttu-id="9fbaf-114">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fbaf-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fbaf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fbaf-115">-DefaultProfile</span></span>
<span data-ttu-id="9fbaf-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9fbaf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fbaf-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9fbaf-117">-InputObject</span></span>
<span data-ttu-id="9fbaf-118">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="9fbaf-118">CosmosDB Account object</span></span>

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

### <span data-ttu-id="9fbaf-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="9fbaf-119">-Name</span></span>
<span data-ttu-id="9fbaf-120">Nome database.</span><span class="sxs-lookup"><span data-stu-id="9fbaf-120">Database name.</span></span>

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

### <span data-ttu-id="9fbaf-121">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9fbaf-121">-ParentObject</span></span>
<span data-ttu-id="9fbaf-122">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="9fbaf-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="9fbaf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fbaf-123">-ResourceGroupName</span></span>
<span data-ttu-id="9fbaf-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9fbaf-124">Name of resource group.</span></span>

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

### <span data-ttu-id="9fbaf-125">-Throughput</span><span class="sxs-lookup"><span data-stu-id="9fbaf-125">-Throughput</span></span>
<span data-ttu-id="9fbaf-126">La velocità effettiva del database Gremlin (RU/s).</span><span class="sxs-lookup"><span data-stu-id="9fbaf-126">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="9fbaf-127">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="9fbaf-127">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fbaf-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fbaf-128">-WhatIf</span></span>
<span data-ttu-id="9fbaf-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9fbaf-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fbaf-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9fbaf-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fbaf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fbaf-131">CommonParameters</span></span>
<span data-ttu-id="9fbaf-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fbaf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fbaf-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9fbaf-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fbaf-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9fbaf-134">INPUTS</span></span>

### <span data-ttu-id="9fbaf-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="9fbaf-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="9fbaf-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9fbaf-136">OUTPUTS</span></span>

### <span data-ttu-id="9fbaf-137">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="9fbaf-137">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="9fbaf-138">Note</span><span class="sxs-lookup"><span data-stu-id="9fbaf-138">NOTES</span></span>

## <span data-ttu-id="9fbaf-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9fbaf-139">RELATED LINKS</span></span>
