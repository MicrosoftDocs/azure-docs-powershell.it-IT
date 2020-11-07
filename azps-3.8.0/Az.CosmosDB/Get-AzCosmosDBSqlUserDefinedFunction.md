---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: c8cfb1077f418c9d671729cb0ff762141a7b77c4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864496"
---
# <span data-ttu-id="379bb-101">Get-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="379bb-101">Get-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="379bb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="379bb-102">SYNOPSIS</span></span>
<span data-ttu-id="379bb-103">Ottiene la funzione definita dall'utente di CosmosDB SQL.</span><span class="sxs-lookup"><span data-stu-id="379bb-103">Gets the CosmosDB Sql User Defined Function.</span></span>

## <span data-ttu-id="379bb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="379bb-104">SYNTAX</span></span>

### <span data-ttu-id="379bb-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="379bb-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="379bb-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="379bb-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlUserDefinedFunction [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="379bb-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="379bb-107">DESCRIPTION</span></span>
<span data-ttu-id="379bb-108">Il cmdlet **Get-AzCosmosDBSqlUserDefinedFunction** Ottiene l'elenco di tutte le UserDefinedFunctions SQL esistenti di CosmosDB per una determinata ResourceGroupName, AccountName, DatabaseName e ContainerName e ottiene un singolo CosmosDB SQL per una determinata ResourceGroupName, AccountName, DatabaseName, ContainerName e UserDefinedFunctionName.</span><span class="sxs-lookup"><span data-stu-id="379bb-108">The **Get-AzCosmosDBSqlUserDefinedFunction** cmdlet gets the list of all existing CosmosDB Sql UserDefinedFunctions for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql UserDefinedFunction for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and UserDefinedFunctionName.</span></span>

## <span data-ttu-id="379bb-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="379bb-109">EXAMPLES</span></span>

### <span data-ttu-id="379bb-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="379bb-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlUserDefinedFunction -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {userDefinedFunctionName} -ContainerName {containerName} 

Name                               : {userDefinedFunctionName}
Id                                 : {userDefinedFunctionId}
Resource                           : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetPropertiesResource
```

## <span data-ttu-id="379bb-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="379bb-111">PARAMETERS</span></span>

### <span data-ttu-id="379bb-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="379bb-112">-AccountName</span></span>
<span data-ttu-id="379bb-113">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="379bb-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="379bb-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="379bb-114">-ContainerName</span></span>
<span data-ttu-id="379bb-115">Nome contenitore.</span><span class="sxs-lookup"><span data-stu-id="379bb-115">Container name.</span></span>

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

### <span data-ttu-id="379bb-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="379bb-116">-DatabaseName</span></span>
<span data-ttu-id="379bb-117">Nome database.</span><span class="sxs-lookup"><span data-stu-id="379bb-117">Database name.</span></span>

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

### <span data-ttu-id="379bb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="379bb-118">-DefaultProfile</span></span>
<span data-ttu-id="379bb-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="379bb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="379bb-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="379bb-120">-InputObject</span></span>
<span data-ttu-id="379bb-121">Oggetto contenitore SQL.</span><span class="sxs-lookup"><span data-stu-id="379bb-121">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="379bb-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="379bb-122">-Name</span></span>
<span data-ttu-id="379bb-123">Nome della funzione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="379bb-123">User Defined Function Name.</span></span>

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

### <span data-ttu-id="379bb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="379bb-124">-ResourceGroupName</span></span>
<span data-ttu-id="379bb-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="379bb-125">Name of resource group.</span></span>

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

### <span data-ttu-id="379bb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="379bb-126">CommonParameters</span></span>
<span data-ttu-id="379bb-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="379bb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="379bb-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="379bb-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="379bb-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="379bb-129">INPUTS</span></span>

### <span data-ttu-id="379bb-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="379bb-130">None</span></span>

## <span data-ttu-id="379bb-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="379bb-131">OUTPUTS</span></span>

### <span data-ttu-id="379bb-132">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="379bb-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="379bb-133">Note</span><span class="sxs-lookup"><span data-stu-id="379bb-133">NOTES</span></span>

## <span data-ttu-id="379bb-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="379bb-134">RELATED LINKS</span></span>
