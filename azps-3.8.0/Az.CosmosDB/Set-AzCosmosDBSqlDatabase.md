---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 1af202573ff4b783756b8884707922c64ffcf953
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018512"
---
# <span data-ttu-id="d0007-101">Set-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d0007-101">Set-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="d0007-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d0007-102">SYNOPSIS</span></span>
<span data-ttu-id="d0007-103">Crea un nuovo o aggiorna un database SQL esistente di CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="d0007-103">Creates a new or updates an existing CosmosDB Sql Database.</span></span>

## <span data-ttu-id="d0007-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d0007-104">SYNTAX</span></span>

### <span data-ttu-id="d0007-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d0007-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0007-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0007-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBSqlDatabase -Name <String> [-Throughput <Int32>] -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0007-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d0007-107">DESCRIPTION</span></span>
<span data-ttu-id="d0007-108">Il cmdlet **set-AzCosmosDBSqlDatabase** crea un nuovo o aggiorna un database SQL esistente di CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="d0007-108">The **Set-AzCosmosDBSqlDatabase** cmdlet creates a new or updates an existing CosmosDB Sql Database.</span></span>

## <span data-ttu-id="d0007-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d0007-109">EXAMPLES</span></span>

### <span data-ttu-id="d0007-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d0007-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBSqlDatabase -ResourceGroupName {resourceGroupName} -AccountName {accountName}-Name {databaseName}

Name                    : {databaseName}
Id                      : {databaseId}
SqlDatabaseGetResultsId :
_rid                    :
_ts                     :
_etag                   :
_colls                  :
_users                  :
```

## <span data-ttu-id="d0007-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d0007-111">PARAMETERS</span></span>

### <span data-ttu-id="d0007-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d0007-112">-AccountName</span></span>
<span data-ttu-id="d0007-113">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="d0007-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d0007-114">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d0007-114">-Confirm</span></span>
<span data-ttu-id="d0007-115">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0007-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0007-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0007-116">-DefaultProfile</span></span>
<span data-ttu-id="d0007-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d0007-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0007-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0007-118">-InputObject</span></span>
<span data-ttu-id="d0007-119">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="d0007-119">CosmosDB Account object</span></span>

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

### <span data-ttu-id="d0007-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="d0007-120">-Name</span></span>
<span data-ttu-id="d0007-121">Nome database.</span><span class="sxs-lookup"><span data-stu-id="d0007-121">Database name.</span></span>

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

### <span data-ttu-id="d0007-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0007-122">-ResourceGroupName</span></span>
<span data-ttu-id="d0007-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d0007-123">Name of resource group.</span></span>

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

### <span data-ttu-id="d0007-124">-Throughput</span><span class="sxs-lookup"><span data-stu-id="d0007-124">-Throughput</span></span>
<span data-ttu-id="d0007-125">La velocità effettiva del database SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="d0007-125">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="d0007-126">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="d0007-126">Default value is 400.</span></span>

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

### <span data-ttu-id="d0007-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0007-127">-WhatIf</span></span>
<span data-ttu-id="d0007-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d0007-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0007-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d0007-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0007-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0007-130">CommonParameters</span></span>
<span data-ttu-id="d0007-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0007-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0007-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0007-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0007-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d0007-133">INPUTS</span></span>

### <span data-ttu-id="d0007-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d0007-134">None</span></span>

## <span data-ttu-id="d0007-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d0007-135">OUTPUTS</span></span>

### <span data-ttu-id="d0007-136">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="d0007-136">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="d0007-137">Note</span><span class="sxs-lookup"><span data-stu-id="d0007-137">NOTES</span></span>

## <span data-ttu-id="d0007-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d0007-138">RELATED LINKS</span></span>
