---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: 05304da0a027f66e145ca1c64942b0ffc9fd0936
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199046"
---
# <span data-ttu-id="4f08b-101">Get-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="4f08b-101">Get-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="4f08b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f08b-102">SYNOPSIS</span></span>
<span data-ttu-id="4f08b-103">Ottiene il valore di velocità effettiva della tabella Cassandra.</span><span class="sxs-lookup"><span data-stu-id="4f08b-103">Gets the throughput value of the Cassandra Table.</span></span>

## <span data-ttu-id="4f08b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4f08b-104">SYNTAX</span></span>

### <span data-ttu-id="4f08b-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4f08b-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f08b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f08b-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -InputObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f08b-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4f08b-107">DESCRIPTION</span></span>
<span data-ttu-id="4f08b-108">Il cmdlet **Get-AzCosmosDBCassandraTableThroughput** ottiene l'oggetto velocità effettiva corrispondente a un determinato keyspace.</span><span class="sxs-lookup"><span data-stu-id="4f08b-108">The **Get-AzCosmosDBCassandraTableThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="4f08b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4f08b-109">EXAMPLES</span></span>

### <span data-ttu-id="4f08b-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4f08b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {tableName}
```

## <span data-ttu-id="4f08b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f08b-111">PARAMETERS</span></span>

### <span data-ttu-id="4f08b-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4f08b-112">-AccountName</span></span>
<span data-ttu-id="4f08b-113">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="4f08b-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="4f08b-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4f08b-114">-Confirm</span></span>
<span data-ttu-id="4f08b-115">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f08b-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f08b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f08b-116">-DefaultProfile</span></span>
<span data-ttu-id="4f08b-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4f08b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f08b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f08b-118">-InputObject</span></span>
<span data-ttu-id="4f08b-119">Oggetto Table di Cassandra.</span><span class="sxs-lookup"><span data-stu-id="4f08b-119">Cassandra Table object.</span></span>

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

### <span data-ttu-id="4f08b-120">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="4f08b-120">-KeyspaceName</span></span>
<span data-ttu-id="4f08b-121">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="4f08b-121">Database name.</span></span>

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

### <span data-ttu-id="4f08b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="4f08b-122">-Name</span></span>
<span data-ttu-id="4f08b-123">Nome tabella Cassandra.</span><span class="sxs-lookup"><span data-stu-id="4f08b-123">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="4f08b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f08b-124">-ResourceGroupName</span></span>
<span data-ttu-id="4f08b-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4f08b-125">Name of resource group.</span></span>

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

### <span data-ttu-id="4f08b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f08b-126">-WhatIf</span></span>
<span data-ttu-id="4f08b-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4f08b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f08b-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4f08b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f08b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f08b-129">CommonParameters</span></span>
<span data-ttu-id="4f08b-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f08b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f08b-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4f08b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f08b-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="4f08b-132">INPUTS</span></span>

### <span data-ttu-id="4f08b-133">Microsoft.Azure.Commands.EnterpriseDb.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="4f08b-133">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="4f08b-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4f08b-134">OUTPUTS</span></span>

### <span data-ttu-id="4f08b-135">Microsoft.Azure.Commands.EnterpriseDb.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="4f08b-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="4f08b-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="4f08b-136">NOTES</span></span>

## <span data-ttu-id="4f08b-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4f08b-137">RELATED LINKS</span></span>
