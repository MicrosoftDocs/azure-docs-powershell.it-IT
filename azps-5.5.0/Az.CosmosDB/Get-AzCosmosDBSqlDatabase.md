---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 87c0436ce4aa62de7a1145d501e71783433b09eb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199014"
---
# <span data-ttu-id="e1c04-101">Get-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e1c04-101">Get-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="e1c04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1c04-102">SYNOPSIS</span></span>
<span data-ttu-id="e1c04-103">Ottiene il database sql di DatabaseDb.</span><span class="sxs-lookup"><span data-stu-id="e1c04-103">Gets the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="e1c04-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e1c04-104">SYNTAX</span></span>

### <span data-ttu-id="e1c04-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e1c04-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1c04-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1c04-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1c04-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e1c04-107">DESCRIPTION</span></span>
<span data-ttu-id="e1c04-108">Il cmdlet **Get-AzCosmosDBSqlDatabase** ottiene l'elenco di tutti i database Sql esistenti diDbDb per un determinato NomeGruppoSocietà, NomeSocietà e ottiene un singolo database Sql DiRDB per un dato NomeGruppoSocietà, NomeSocietà, NomeDatabase e Nome Container.</span><span class="sxs-lookup"><span data-stu-id="e1c04-108">The **Get-AzCosmosDBSqlDatabase** cmdlet gets the list of all existing CosmosDB Sql Databases for a given ResourceGroupName, AccountName and gets a single CosmosDB Sql Database for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="e1c04-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e1c04-109">EXAMPLES</span></span>

### <span data-ttu-id="e1c04-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e1c04-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabase -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                    : {databaseName}
Id                      : {databaseId}
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="e1c04-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1c04-111">PARAMETERS</span></span>

### <span data-ttu-id="e1c04-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e1c04-112">-AccountName</span></span>
<span data-ttu-id="e1c04-113">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="e1c04-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e1c04-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1c04-114">-DefaultProfile</span></span>
<span data-ttu-id="e1c04-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e1c04-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1c04-116">-Name</span><span class="sxs-lookup"><span data-stu-id="e1c04-116">-Name</span></span>
<span data-ttu-id="e1c04-117">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="e1c04-117">Database name.</span></span>

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

### <span data-ttu-id="e1c04-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e1c04-118">-ParentObject</span></span>
<span data-ttu-id="e1c04-119">Oggetto AccountDb Disa</span><span class="sxs-lookup"><span data-stu-id="e1c04-119">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1c04-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1c04-120">-ResourceGroupName</span></span>
<span data-ttu-id="e1c04-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e1c04-121">Name of resource group.</span></span>

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

### <span data-ttu-id="e1c04-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1c04-122">CommonParameters</span></span>
<span data-ttu-id="e1c04-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1c04-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1c04-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e1c04-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1c04-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="e1c04-125">INPUTS</span></span>

### <span data-ttu-id="e1c04-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e1c04-126">None</span></span>

## <span data-ttu-id="e1c04-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e1c04-127">OUTPUTS</span></span>

### <span data-ttu-id="e1c04-128">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="e1c04-128">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="e1c04-129">Microsoft.Azure.Commands.EnterpriseDb.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="e1c04-129">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="e1c04-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="e1c04-130">NOTES</span></span>

## <span data-ttu-id="e1c04-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e1c04-131">RELATED LINKS</span></span>
