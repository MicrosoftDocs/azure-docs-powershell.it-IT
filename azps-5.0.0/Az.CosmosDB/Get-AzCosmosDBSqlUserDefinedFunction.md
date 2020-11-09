---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: b2f6e203b1ef8f14623df2910b853ea6f3841f72
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299472"
---
# <span data-ttu-id="72e2c-101">Get-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="72e2c-101">Get-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="72e2c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="72e2c-102">SYNOPSIS</span></span>
<span data-ttu-id="72e2c-103">Ottiene la funzione definita dall'utente di CosmosDB SQL.</span><span class="sxs-lookup"><span data-stu-id="72e2c-103">Gets the CosmosDB Sql User Defined Function.</span></span>

## <span data-ttu-id="72e2c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="72e2c-104">SYNTAX</span></span>

### <span data-ttu-id="72e2c-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="72e2c-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72e2c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="72e2c-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlUserDefinedFunction [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72e2c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="72e2c-107">DESCRIPTION</span></span>
<span data-ttu-id="72e2c-108">Il cmdlet **Get-AzCosmosDBSqlUserDefinedFunction** Ottiene l'elenco di tutte le UserDefinedFunctions SQL esistenti di CosmosDB per una determinata ResourceGroupName, AccountName, DatabaseName e ContainerName e ottiene un singolo CosmosDB SQL per una determinata ResourceGroupName, AccountName, DatabaseName, ContainerName e UserDefinedFunctionName.</span><span class="sxs-lookup"><span data-stu-id="72e2c-108">The **Get-AzCosmosDBSqlUserDefinedFunction** cmdlet gets the list of all existing CosmosDB Sql UserDefinedFunctions for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql UserDefinedFunction for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and UserDefinedFunctionName.</span></span>

## <span data-ttu-id="72e2c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="72e2c-109">EXAMPLES</span></span>

### <span data-ttu-id="72e2c-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="72e2c-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlUserDefinedFunction -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {userDefinedFunctionName} -ContainerName {containerName} 

Name                               : {userDefinedFunctionName}
Id                                 : {userDefinedFunctionId}
Resource                           : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetPropertiesResource
```

## <span data-ttu-id="72e2c-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="72e2c-111">PARAMETERS</span></span>

### <span data-ttu-id="72e2c-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="72e2c-112">-AccountName</span></span>
<span data-ttu-id="72e2c-113">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="72e2c-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="72e2c-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="72e2c-114">-ContainerName</span></span>
<span data-ttu-id="72e2c-115">Nome contenitore.</span><span class="sxs-lookup"><span data-stu-id="72e2c-115">Container name.</span></span>

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

### <span data-ttu-id="72e2c-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="72e2c-116">-DatabaseName</span></span>
<span data-ttu-id="72e2c-117">Nome database.</span><span class="sxs-lookup"><span data-stu-id="72e2c-117">Database name.</span></span>

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

### <span data-ttu-id="72e2c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72e2c-118">-DefaultProfile</span></span>
<span data-ttu-id="72e2c-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="72e2c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72e2c-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="72e2c-120">-Name</span></span>
<span data-ttu-id="72e2c-121">Nome della funzione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="72e2c-121">User Defined Function Name.</span></span>

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

### <span data-ttu-id="72e2c-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="72e2c-122">-ParentObject</span></span>
<span data-ttu-id="72e2c-123">Oggetto contenitore SQL.</span><span class="sxs-lookup"><span data-stu-id="72e2c-123">Sql Container object.</span></span>

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

### <span data-ttu-id="72e2c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72e2c-124">-ResourceGroupName</span></span>
<span data-ttu-id="72e2c-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="72e2c-125">Name of resource group.</span></span>

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

### <span data-ttu-id="72e2c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72e2c-126">CommonParameters</span></span>
<span data-ttu-id="72e2c-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72e2c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72e2c-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72e2c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72e2c-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="72e2c-129">INPUTS</span></span>

### <span data-ttu-id="72e2c-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="72e2c-130">None</span></span>

## <span data-ttu-id="72e2c-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="72e2c-131">OUTPUTS</span></span>

### <span data-ttu-id="72e2c-132">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="72e2c-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="72e2c-133">Note</span><span class="sxs-lookup"><span data-stu-id="72e2c-133">NOTES</span></span>

## <span data-ttu-id="72e2c-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="72e2c-134">RELATED LINKS</span></span>
