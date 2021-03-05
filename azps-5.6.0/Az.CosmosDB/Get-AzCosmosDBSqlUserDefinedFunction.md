---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: 0d422014d3cf2ca2ffa18b60c10b50b21bf91144
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986900"
---
# <span data-ttu-id="3f634-101">Get-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="3f634-101">Get-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="3f634-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f634-102">SYNOPSIS</span></span>
<span data-ttu-id="3f634-103">Ottiene la funzione sql definite dall'utenteDb.</span><span class="sxs-lookup"><span data-stu-id="3f634-103">Gets the CosmosDB Sql User Defined Function.</span></span>

## <span data-ttu-id="3f634-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3f634-104">SYNTAX</span></span>

### <span data-ttu-id="3f634-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f634-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f634-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f634-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlUserDefinedFunction [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f634-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3f634-107">DESCRIPTION</span></span>
<span data-ttu-id="3f634-108">Il cmdlet **Get-AzCosmosDBSqlUserDefinedFunction** ottiene l'elenco di tutte le funzioni Sql UserDefinedFunctions SQL diDb esistenti per un determinato ResourceGroupName, AccountName, DatabaseName e ContainerName e ottiene un'unica Funzione Sql UserDefinedFunction diDb per un dato ResourceGroupName, AccountName, DatabaseName, ContainerName e UserDefinedFunctionName.</span><span class="sxs-lookup"><span data-stu-id="3f634-108">The **Get-AzCosmosDBSqlUserDefinedFunction** cmdlet gets the list of all existing CosmosDB Sql UserDefinedFunctions for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql UserDefinedFunction for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and UserDefinedFunctionName.</span></span>

## <span data-ttu-id="3f634-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3f634-109">EXAMPLES</span></span>

### <span data-ttu-id="3f634-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3f634-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlUserDefinedFunction -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {userDefinedFunctionName} -ContainerName {containerName} 

Name                               : {userDefinedFunctionName}
Id                                 : {userDefinedFunctionId}
Resource                           : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetPropertiesResource
```

## <span data-ttu-id="3f634-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f634-111">PARAMETERS</span></span>

### <span data-ttu-id="3f634-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3f634-112">-AccountName</span></span>
<span data-ttu-id="3f634-113">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="3f634-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="3f634-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="3f634-114">-ContainerName</span></span>
<span data-ttu-id="3f634-115">Nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="3f634-115">Container name.</span></span>

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

### <span data-ttu-id="3f634-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3f634-116">-DatabaseName</span></span>
<span data-ttu-id="3f634-117">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="3f634-117">Database name.</span></span>

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

### <span data-ttu-id="3f634-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f634-118">-DefaultProfile</span></span>
<span data-ttu-id="3f634-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3f634-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f634-120">-Name</span><span class="sxs-lookup"><span data-stu-id="3f634-120">-Name</span></span>
<span data-ttu-id="3f634-121">Nome funzione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="3f634-121">User Defined Function Name.</span></span>

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

### <span data-ttu-id="3f634-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="3f634-122">-ParentObject</span></span>
<span data-ttu-id="3f634-123">Oggetto Contenitore Sql.</span><span class="sxs-lookup"><span data-stu-id="3f634-123">Sql Container object.</span></span>

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

### <span data-ttu-id="3f634-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f634-124">-ResourceGroupName</span></span>
<span data-ttu-id="3f634-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3f634-125">Name of resource group.</span></span>

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

### <span data-ttu-id="3f634-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f634-126">CommonParameters</span></span>
<span data-ttu-id="3f634-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f634-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f634-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3f634-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f634-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="3f634-129">INPUTS</span></span>

### <span data-ttu-id="3f634-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3f634-130">None</span></span>

## <span data-ttu-id="3f634-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3f634-131">OUTPUTS</span></span>

### <span data-ttu-id="3f634-132">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="3f634-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="3f634-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="3f634-133">NOTES</span></span>

## <span data-ttu-id="3f634-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3f634-134">RELATED LINKS</span></span>
