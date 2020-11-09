---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: e144e863ec0c9d55b14295486cdc4e94e26e8909
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299490"
---
# <span data-ttu-id="e8638-101">Get-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="e8638-101">Get-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="e8638-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e8638-102">SYNOPSIS</span></span>
<span data-ttu-id="e8638-103">Ottiene il CosmosDB SQL StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="e8638-103">Gets the CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="e8638-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e8638-104">SYNTAX</span></span>

### <span data-ttu-id="e8638-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8638-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8638-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8638-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8638-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e8638-107">DESCRIPTION</span></span>
<span data-ttu-id="e8638-108">Il cmdlet **Get-AzCosmosDBSqlStoredProcedure** Ottiene l'elenco di tutti i CosmosDB SQL StoredProcedures esistenti per una determinata ResourceGroupName, AccountName, DatabaseName e ContainerName e ottiene un singolo SQL StoredProcedure di CosmosDB per una determinata ResourceGroupName, AccountName, DatabaseName, ContainerName e StoredProcedureName.</span><span class="sxs-lookup"><span data-stu-id="e8638-108">The **Get-AzCosmosDBSqlStoredProcedure** cmdlet gets the list of all existing CosmosDB Sql StoredProcedures for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql StoredProcedure for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and StoredProcedureName.</span></span>

## <span data-ttu-id="e8638-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e8638-109">EXAMPLES</span></span>

### <span data-ttu-id="e8638-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e8638-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlStoredProcedure -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {storedProcedureName} -ContainerName {containerName}

Name                           : {storedProcedureName}
Id                             : {storedProcedureId}
Resource                       : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="e8638-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e8638-111">PARAMETERS</span></span>

### <span data-ttu-id="e8638-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e8638-112">-AccountName</span></span>
<span data-ttu-id="e8638-113">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="e8638-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e8638-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="e8638-114">-ContainerName</span></span>
<span data-ttu-id="e8638-115">Nome contenitore.</span><span class="sxs-lookup"><span data-stu-id="e8638-115">Container name.</span></span>

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

### <span data-ttu-id="e8638-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e8638-116">-DatabaseName</span></span>
<span data-ttu-id="e8638-117">Nome database.</span><span class="sxs-lookup"><span data-stu-id="e8638-117">Database name.</span></span>

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

### <span data-ttu-id="e8638-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8638-118">-DefaultProfile</span></span>
<span data-ttu-id="e8638-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e8638-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8638-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="e8638-120">-Name</span></span>
<span data-ttu-id="e8638-121">Nome Prcodecure archiviato.</span><span class="sxs-lookup"><span data-stu-id="e8638-121">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="e8638-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e8638-122">-ParentObject</span></span>
<span data-ttu-id="e8638-123">Oggetto contenitore SQL.</span><span class="sxs-lookup"><span data-stu-id="e8638-123">Sql Container object.</span></span>

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

### <span data-ttu-id="e8638-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8638-124">-ResourceGroupName</span></span>
<span data-ttu-id="e8638-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e8638-125">Name of resource group.</span></span>

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

### <span data-ttu-id="e8638-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8638-126">CommonParameters</span></span>
<span data-ttu-id="e8638-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8638-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8638-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8638-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8638-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e8638-129">INPUTS</span></span>

### <span data-ttu-id="e8638-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e8638-130">None</span></span>

## <span data-ttu-id="e8638-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e8638-131">OUTPUTS</span></span>

### <span data-ttu-id="e8638-132">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="e8638-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="e8638-133">Note</span><span class="sxs-lookup"><span data-stu-id="e8638-133">NOTES</span></span>

## <span data-ttu-id="e8638-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e8638-134">RELATED LINKS</span></span>
