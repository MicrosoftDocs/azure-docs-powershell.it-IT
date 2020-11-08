---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandrakeyspacethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspaceThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspaceThroughput.md
ms.openlocfilehash: 0c104573fe0ecfb710f37c9c2fe898a6777f49e8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018500"
---
# <span data-ttu-id="cdaac-101">Update-AzCosmosDBCassandraKeyspaceThroughput</span><span class="sxs-lookup"><span data-stu-id="cdaac-101">Update-AzCosmosDBCassandraKeyspaceThroughput</span></span>

## <span data-ttu-id="cdaac-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cdaac-102">SYNOPSIS</span></span>
<span data-ttu-id="cdaac-103">Aggiorna il valore di throughput di un CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="cdaac-103">Updates the throughput value of a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="cdaac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cdaac-104">SYNTAX</span></span>

### <span data-ttu-id="cdaac-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cdaac-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdaac-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cdaac-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSDatabaseAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cdaac-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cdaac-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cdaac-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cdaac-108">EXAMPLES</span></span>

### <span data-ttu-id="cdaac-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cdaac-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraKeyspaceThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myKeyspaceName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="cdaac-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cdaac-110">PARAMETERS</span></span>

### <span data-ttu-id="cdaac-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cdaac-111">-AccountName</span></span>
<span data-ttu-id="cdaac-112">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="cdaac-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="cdaac-113">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cdaac-113">-Confirm</span></span>
<span data-ttu-id="cdaac-114">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdaac-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdaac-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdaac-115">-DefaultProfile</span></span>
<span data-ttu-id="cdaac-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cdaac-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdaac-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cdaac-117">-InputObject</span></span>
<span data-ttu-id="cdaac-118">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="cdaac-118">CosmosDB Account object</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cdaac-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="cdaac-119">-Name</span></span>
<span data-ttu-id="cdaac-120">Nome della barra spaziatrice Cassandra.</span><span class="sxs-lookup"><span data-stu-id="cdaac-120">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="cdaac-121">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="cdaac-121">-ParentObject</span></span>
<span data-ttu-id="cdaac-122">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="cdaac-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="cdaac-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdaac-123">-ResourceGroupName</span></span>
<span data-ttu-id="cdaac-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cdaac-124">Name of resource group.</span></span>

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

### <span data-ttu-id="cdaac-125">-Throughput</span><span class="sxs-lookup"><span data-stu-id="cdaac-125">-Throughput</span></span>
<span data-ttu-id="cdaac-126">La velocità effettiva di Cassandra della barra spaziatrice (RU/s).</span><span class="sxs-lookup"><span data-stu-id="cdaac-126">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="cdaac-127">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="cdaac-127">Default value is 400.</span></span>

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

### <span data-ttu-id="cdaac-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdaac-128">-WhatIf</span></span>
<span data-ttu-id="cdaac-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cdaac-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdaac-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cdaac-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdaac-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdaac-131">CommonParameters</span></span>
<span data-ttu-id="cdaac-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdaac-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdaac-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cdaac-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdaac-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cdaac-134">INPUTS</span></span>

### <span data-ttu-id="cdaac-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="cdaac-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="cdaac-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cdaac-136">OUTPUTS</span></span>

### <span data-ttu-id="cdaac-137">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="cdaac-137">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="cdaac-138">Note</span><span class="sxs-lookup"><span data-stu-id="cdaac-138">NOTES</span></span>

## <span data-ttu-id="cdaac-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cdaac-139">RELATED LINKS</span></span>
