---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: 2ee1f932e1829e6c1d9d35ccd2cf67473a851414
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022393"
---
# <span data-ttu-id="01428-101">Set-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="01428-101">Set-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="01428-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="01428-102">SYNOPSIS</span></span>
<span data-ttu-id="01428-103">Imposta il database MongoDB CosmosDB</span><span class="sxs-lookup"><span data-stu-id="01428-103">Sets the CosmosDB MongoDB Database</span></span>

## <span data-ttu-id="01428-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="01428-104">SYNTAX</span></span>

### <span data-ttu-id="01428-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="01428-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01428-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="01428-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBMongoDBDatabase -Name <String> [-Throughput <Int32>] -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01428-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="01428-107">DESCRIPTION</span></span>
<span data-ttu-id="01428-108">Il cmdlet **set-AzCosmosDBMongoDBDatabase** ottiene il database MongoDB CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="01428-108">The **Set-AzCosmosDBMongoDBDatabase** cmdlet gets the CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="01428-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="01428-109">EXAMPLES</span></span>

### <span data-ttu-id="01428-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="01428-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

<span data-ttu-id="01428-111">Oggetto Resource contiene _rid, _ts, _etag proprietà.</span><span class="sxs-lookup"><span data-stu-id="01428-111">Resource Object contains _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="01428-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="01428-112">PARAMETERS</span></span>

### <span data-ttu-id="01428-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="01428-113">-AccountName</span></span>
<span data-ttu-id="01428-114">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="01428-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="01428-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="01428-115">-Confirm</span></span>
<span data-ttu-id="01428-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01428-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01428-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01428-117">-DefaultProfile</span></span>
<span data-ttu-id="01428-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="01428-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01428-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01428-119">-InputObject</span></span>
<span data-ttu-id="01428-120">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="01428-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01428-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="01428-121">-Name</span></span>
<span data-ttu-id="01428-122">Nome database.</span><span class="sxs-lookup"><span data-stu-id="01428-122">Database name.</span></span>

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

### <span data-ttu-id="01428-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01428-123">-ResourceGroupName</span></span>
<span data-ttu-id="01428-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="01428-124">Name of resource group.</span></span>

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

### <span data-ttu-id="01428-125">-Throughput</span><span class="sxs-lookup"><span data-stu-id="01428-125">-Throughput</span></span>
<span data-ttu-id="01428-126">La velocità effettiva del database Mongo (RU/s).</span><span class="sxs-lookup"><span data-stu-id="01428-126">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="01428-127">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="01428-127">Default value is 400.</span></span>

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

### <span data-ttu-id="01428-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01428-128">-WhatIf</span></span>
<span data-ttu-id="01428-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="01428-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01428-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="01428-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01428-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01428-131">CommonParameters</span></span>
<span data-ttu-id="01428-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01428-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01428-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="01428-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01428-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="01428-134">INPUTS</span></span>

### <span data-ttu-id="01428-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="01428-135">None</span></span>

## <span data-ttu-id="01428-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="01428-136">OUTPUTS</span></span>

### <span data-ttu-id="01428-137">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="01428-137">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="01428-138">Note</span><span class="sxs-lookup"><span data-stu-id="01428-138">NOTES</span></span>

## <span data-ttu-id="01428-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="01428-139">RELATED LINKS</span></span>
