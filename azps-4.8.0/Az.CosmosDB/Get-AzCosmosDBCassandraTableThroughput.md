---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: 05304da0a027f66e145ca1c64942b0ffc9fd0936
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190527"
---
# <span data-ttu-id="3b354-101">Get-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="3b354-101">Get-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="3b354-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3b354-102">SYNOPSIS</span></span>
<span data-ttu-id="3b354-103">Ottiene il valore della velocità effettiva della tabella Cassandra.</span><span class="sxs-lookup"><span data-stu-id="3b354-103">Gets the throughput value of the Cassandra Table.</span></span>

## <span data-ttu-id="3b354-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3b354-104">SYNTAX</span></span>

### <span data-ttu-id="3b354-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3b354-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b354-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b354-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -InputObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b354-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3b354-107">DESCRIPTION</span></span>
<span data-ttu-id="3b354-108">Il cmdlet **Get-AzCosmosDBCassandraTableThroughput** Ottiene l'oggetto throughput corrispondente a uno spazio di base specifico.</span><span class="sxs-lookup"><span data-stu-id="3b354-108">The **Get-AzCosmosDBCassandraTableThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="3b354-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3b354-109">EXAMPLES</span></span>

### <span data-ttu-id="3b354-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3b354-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {tableName}
```

## <span data-ttu-id="3b354-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3b354-111">PARAMETERS</span></span>

### <span data-ttu-id="3b354-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3b354-112">-AccountName</span></span>
<span data-ttu-id="3b354-113">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="3b354-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="3b354-114">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3b354-114">-Confirm</span></span>
<span data-ttu-id="3b354-115">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b354-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b354-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b354-116">-DefaultProfile</span></span>
<span data-ttu-id="3b354-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3b354-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b354-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b354-118">-InputObject</span></span>
<span data-ttu-id="3b354-119">Oggetto tabella Cassandra.</span><span class="sxs-lookup"><span data-stu-id="3b354-119">Cassandra Table object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b354-120">-Barra spaziatrice</span><span class="sxs-lookup"><span data-stu-id="3b354-120">-KeyspaceName</span></span>
<span data-ttu-id="3b354-121">Nome database.</span><span class="sxs-lookup"><span data-stu-id="3b354-121">Database name.</span></span>

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

### <span data-ttu-id="3b354-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="3b354-122">-Name</span></span>
<span data-ttu-id="3b354-123">Nome tabella Cassandra.</span><span class="sxs-lookup"><span data-stu-id="3b354-123">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="3b354-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b354-124">-ResourceGroupName</span></span>
<span data-ttu-id="3b354-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3b354-125">Name of resource group.</span></span>

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

### <span data-ttu-id="3b354-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b354-126">-WhatIf</span></span>
<span data-ttu-id="3b354-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3b354-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b354-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3b354-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b354-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b354-129">CommonParameters</span></span>
<span data-ttu-id="3b354-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b354-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b354-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3b354-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b354-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3b354-132">INPUTS</span></span>

### <span data-ttu-id="3b354-133">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="3b354-133">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="3b354-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3b354-134">OUTPUTS</span></span>

### <span data-ttu-id="3b354-135">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="3b354-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="3b354-136">Note</span><span class="sxs-lookup"><span data-stu-id="3b354-136">NOTES</span></span>

## <span data-ttu-id="3b354-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3b354-137">RELATED LINKS</span></span>
