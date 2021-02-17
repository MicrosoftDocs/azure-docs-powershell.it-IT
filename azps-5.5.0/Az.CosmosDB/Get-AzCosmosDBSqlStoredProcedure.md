---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: e144e863ec0c9d55b14295486cdc4e94e26e8909
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177311"
---
# <span data-ttu-id="d3568-101">Get-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="d3568-101">Get-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="d3568-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3568-102">SYNOPSIS</span></span>
<span data-ttu-id="d3568-103">Recupera l'istruzione Sql StoredProcedure sql del databasedi database.</span><span class="sxs-lookup"><span data-stu-id="d3568-103">Gets the CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="d3568-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3568-104">SYNTAX</span></span>

### <span data-ttu-id="d3568-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3568-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3568-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3568-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3568-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d3568-107">DESCRIPTION</span></span>
<span data-ttu-id="d3568-108">Il cmdlet **Get-AzCosmosDBSqlStoredProcedure** ottiene l'elenco di tutti i database Sql StoredProcedures esistenti per un determinato ResourceGroupName, AccountName, DatabaseName e ContainerName e ottiene un unico DatabaseDb Sql StoredProcedure per un determinato ResourceGroupName, AccountName, DatabaseName, ContainerName e StoredProcedureName.</span><span class="sxs-lookup"><span data-stu-id="d3568-108">The **Get-AzCosmosDBSqlStoredProcedure** cmdlet gets the list of all existing CosmosDB Sql StoredProcedures for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql StoredProcedure for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and StoredProcedureName.</span></span>

## <span data-ttu-id="d3568-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3568-109">EXAMPLES</span></span>

### <span data-ttu-id="d3568-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d3568-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlStoredProcedure -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {storedProcedureName} -ContainerName {containerName}

Name                           : {storedProcedureName}
Id                             : {storedProcedureId}
Resource                       : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="d3568-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3568-111">PARAMETERS</span></span>

### <span data-ttu-id="d3568-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d3568-112">-AccountName</span></span>
<span data-ttu-id="d3568-113">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="d3568-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d3568-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="d3568-114">-ContainerName</span></span>
<span data-ttu-id="d3568-115">Nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="d3568-115">Container name.</span></span>

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

### <span data-ttu-id="d3568-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d3568-116">-DatabaseName</span></span>
<span data-ttu-id="d3568-117">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="d3568-117">Database name.</span></span>

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

### <span data-ttu-id="d3568-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3568-118">-DefaultProfile</span></span>
<span data-ttu-id="d3568-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d3568-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3568-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d3568-120">-Name</span></span>
<span data-ttu-id="d3568-121">Nome Prcodecure archiviato.</span><span class="sxs-lookup"><span data-stu-id="d3568-121">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="d3568-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d3568-122">-ParentObject</span></span>
<span data-ttu-id="d3568-123">Oggetto Contenitore Sql.</span><span class="sxs-lookup"><span data-stu-id="d3568-123">Sql Container object.</span></span>

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

### <span data-ttu-id="d3568-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3568-124">-ResourceGroupName</span></span>
<span data-ttu-id="d3568-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d3568-125">Name of resource group.</span></span>

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

### <span data-ttu-id="d3568-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3568-126">CommonParameters</span></span>
<span data-ttu-id="d3568-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3568-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3568-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d3568-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3568-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="d3568-129">INPUTS</span></span>

### <span data-ttu-id="d3568-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d3568-130">None</span></span>

## <span data-ttu-id="d3568-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3568-131">OUTPUTS</span></span>

### <span data-ttu-id="d3568-132">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="d3568-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="d3568-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="d3568-133">NOTES</span></span>

## <span data-ttu-id="d3568-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3568-134">RELATED LINKS</span></span>
