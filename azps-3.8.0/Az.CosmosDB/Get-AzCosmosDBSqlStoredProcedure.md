---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: a9a81336ab921ebd63b8a969be5fbf65f4b7fa14
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018519"
---
# <span data-ttu-id="3a7d1-101">Get-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="3a7d1-101">Get-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="3a7d1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3a7d1-102">SYNOPSIS</span></span>
<span data-ttu-id="3a7d1-103">Ottiene il CosmosDB SQL StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="3a7d1-103">Gets the CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="3a7d1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3a7d1-104">SYNTAX</span></span>

### <span data-ttu-id="3a7d1-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a7d1-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a7d1-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a7d1-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a7d1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a7d1-107">DESCRIPTION</span></span>
<span data-ttu-id="3a7d1-108">Il cmdlet **Get-AzCosmosDBSqlStoredProcedure** Ottiene l'elenco di tutti i CosmosDB SQL StoredProcedures esistenti per una determinata ResourceGroupName, AccountName, DatabaseName e ContainerName e ottiene un singolo SQL StoredProcedure di CosmosDB per una determinata ResourceGroupName, AccountName, DatabaseName, ContainerName e StoredProcedureName.</span><span class="sxs-lookup"><span data-stu-id="3a7d1-108">The **Get-AzCosmosDBSqlStoredProcedure** cmdlet gets the list of all existing CosmosDB Sql StoredProcedures for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql StoredProcedure for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and StoredProcedureName.</span></span>

## <span data-ttu-id="3a7d1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3a7d1-109">EXAMPLES</span></span>

### <span data-ttu-id="3a7d1-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3a7d1-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlStoredProcedure -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {storedProcedureName} -ContainerName {containerName}

Name                           : {storedProcedureName}
Id                             : {storedProcedureId}
Resource                       : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="3a7d1-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3a7d1-111">PARAMETERS</span></span>

### <span data-ttu-id="3a7d1-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3a7d1-112">-AccountName</span></span>
<span data-ttu-id="3a7d1-113">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="3a7d1-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="3a7d1-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="3a7d1-114">-ContainerName</span></span>
<span data-ttu-id="3a7d1-115">Nome contenitore.</span><span class="sxs-lookup"><span data-stu-id="3a7d1-115">Container name.</span></span>

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

### <span data-ttu-id="3a7d1-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3a7d1-116">-DatabaseName</span></span>
<span data-ttu-id="3a7d1-117">Nome database.</span><span class="sxs-lookup"><span data-stu-id="3a7d1-117">Database name.</span></span>

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

### <span data-ttu-id="3a7d1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a7d1-118">-DefaultProfile</span></span>
<span data-ttu-id="3a7d1-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3a7d1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a7d1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a7d1-120">-InputObject</span></span>
<span data-ttu-id="3a7d1-121">Oggetto contenitore SQL.</span><span class="sxs-lookup"><span data-stu-id="3a7d1-121">Sql Container object.</span></span>

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

### <span data-ttu-id="3a7d1-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="3a7d1-122">-Name</span></span>
<span data-ttu-id="3a7d1-123">Nome Prcodecure archiviato.</span><span class="sxs-lookup"><span data-stu-id="3a7d1-123">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="3a7d1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a7d1-124">-ResourceGroupName</span></span>
<span data-ttu-id="3a7d1-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3a7d1-125">Name of resource group.</span></span>

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

### <span data-ttu-id="3a7d1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a7d1-126">CommonParameters</span></span>
<span data-ttu-id="3a7d1-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a7d1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a7d1-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a7d1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a7d1-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3a7d1-129">INPUTS</span></span>

### <span data-ttu-id="3a7d1-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3a7d1-130">None</span></span>

## <span data-ttu-id="3a7d1-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3a7d1-131">OUTPUTS</span></span>

### <span data-ttu-id="3a7d1-132">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="3a7d1-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="3a7d1-133">Note</span><span class="sxs-lookup"><span data-stu-id="3a7d1-133">NOTES</span></span>

## <span data-ttu-id="3a7d1-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3a7d1-134">RELATED LINKS</span></span>
