---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: b2f6e203b1ef8f14623df2910b853ea6f3841f72
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345520"
---
# <span data-ttu-id="bda5b-101">Get-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="bda5b-101">Get-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="bda5b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bda5b-102">SYNOPSIS</span></span>
<span data-ttu-id="bda5b-103">Ottiene la funzione definita dall'utente di CosmosDB SQL.</span><span class="sxs-lookup"><span data-stu-id="bda5b-103">Gets the CosmosDB Sql User Defined Function.</span></span>

## <span data-ttu-id="bda5b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bda5b-104">SYNTAX</span></span>

### <span data-ttu-id="bda5b-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bda5b-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bda5b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bda5b-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlUserDefinedFunction [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bda5b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bda5b-107">DESCRIPTION</span></span>
<span data-ttu-id="bda5b-108">Il cmdlet **Get-AzCosmosDBSqlUserDefinedFunction** Ottiene l'elenco di tutte le UserDefinedFunctions SQL esistenti di CosmosDB per una determinata ResourceGroupName, AccountName, DatabaseName e ContainerName e ottiene un singolo CosmosDB SQL per una determinata ResourceGroupName, AccountName, DatabaseName, ContainerName e UserDefinedFunctionName.</span><span class="sxs-lookup"><span data-stu-id="bda5b-108">The **Get-AzCosmosDBSqlUserDefinedFunction** cmdlet gets the list of all existing CosmosDB Sql UserDefinedFunctions for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql UserDefinedFunction for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and UserDefinedFunctionName.</span></span>

## <span data-ttu-id="bda5b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bda5b-109">EXAMPLES</span></span>

### <span data-ttu-id="bda5b-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bda5b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlUserDefinedFunction -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {userDefinedFunctionName} -ContainerName {containerName} 

Name                               : {userDefinedFunctionName}
Id                                 : {userDefinedFunctionId}
Resource                           : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetPropertiesResource
```

## <span data-ttu-id="bda5b-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bda5b-111">PARAMETERS</span></span>

### <span data-ttu-id="bda5b-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bda5b-112">-AccountName</span></span>
<span data-ttu-id="bda5b-113">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="bda5b-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="bda5b-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="bda5b-114">-ContainerName</span></span>
<span data-ttu-id="bda5b-115">Nome contenitore.</span><span class="sxs-lookup"><span data-stu-id="bda5b-115">Container name.</span></span>

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

### <span data-ttu-id="bda5b-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bda5b-116">-DatabaseName</span></span>
<span data-ttu-id="bda5b-117">Nome database.</span><span class="sxs-lookup"><span data-stu-id="bda5b-117">Database name.</span></span>

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

### <span data-ttu-id="bda5b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bda5b-118">-DefaultProfile</span></span>
<span data-ttu-id="bda5b-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bda5b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bda5b-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="bda5b-120">-Name</span></span>
<span data-ttu-id="bda5b-121">Nome della funzione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="bda5b-121">User Defined Function Name.</span></span>

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

### <span data-ttu-id="bda5b-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="bda5b-122">-ParentObject</span></span>
<span data-ttu-id="bda5b-123">Oggetto contenitore SQL.</span><span class="sxs-lookup"><span data-stu-id="bda5b-123">Sql Container object.</span></span>

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

### <span data-ttu-id="bda5b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bda5b-124">-ResourceGroupName</span></span>
<span data-ttu-id="bda5b-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bda5b-125">Name of resource group.</span></span>

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

### <span data-ttu-id="bda5b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bda5b-126">CommonParameters</span></span>
<span data-ttu-id="bda5b-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bda5b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bda5b-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bda5b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bda5b-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bda5b-129">INPUTS</span></span>

### <span data-ttu-id="bda5b-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="bda5b-130">None</span></span>

## <span data-ttu-id="bda5b-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bda5b-131">OUTPUTS</span></span>

### <span data-ttu-id="bda5b-132">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="bda5b-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="bda5b-133">Note</span><span class="sxs-lookup"><span data-stu-id="bda5b-133">NOTES</span></span>

## <span data-ttu-id="bda5b-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bda5b-134">RELATED LINKS</span></span>
