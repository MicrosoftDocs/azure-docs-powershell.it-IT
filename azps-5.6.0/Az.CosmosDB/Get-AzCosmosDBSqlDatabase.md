---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 6d0fe9565a969de19234d65378fd91a1af7a327f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015373"
---
# <span data-ttu-id="33746-101">Get-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="33746-101">Get-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="33746-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33746-102">SYNOPSIS</span></span>
<span data-ttu-id="33746-103">Ottiene il database SQL di DatabaseDb.</span><span class="sxs-lookup"><span data-stu-id="33746-103">Gets the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="33746-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="33746-104">SYNTAX</span></span>

### <span data-ttu-id="33746-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="33746-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33746-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="33746-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33746-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="33746-107">DESCRIPTION</span></span>
<span data-ttu-id="33746-108">Il cmdlet **Get-AzCosmosDBSqlDatabase** ottiene l'elenco di tutti i database Sql DatabaseDb esistenti per un determinato NomeGruppoSocietà, NomeSocietà e ottiene un singolo database Sql DiRDB per un dato NomeGruppoSocietà, NomeSocietà, NomeDatabase e Nome Container.</span><span class="sxs-lookup"><span data-stu-id="33746-108">The **Get-AzCosmosDBSqlDatabase** cmdlet gets the list of all existing CosmosDB Sql Databases for a given ResourceGroupName, AccountName and gets a single CosmosDB Sql Database for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="33746-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="33746-109">EXAMPLES</span></span>

### <span data-ttu-id="33746-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="33746-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabase -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                    : {databaseName}
Id                      : {databaseId}
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="33746-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33746-111">PARAMETERS</span></span>

### <span data-ttu-id="33746-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="33746-112">-AccountName</span></span>
<span data-ttu-id="33746-113">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="33746-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="33746-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33746-114">-DefaultProfile</span></span>
<span data-ttu-id="33746-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="33746-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33746-116">-Name</span><span class="sxs-lookup"><span data-stu-id="33746-116">-Name</span></span>
<span data-ttu-id="33746-117">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="33746-117">Database name.</span></span>

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

### <span data-ttu-id="33746-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="33746-118">-ParentObject</span></span>
<span data-ttu-id="33746-119">Oggetto Account Aziendale</span><span class="sxs-lookup"><span data-stu-id="33746-119">CosmosDB Account object</span></span>

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

### <span data-ttu-id="33746-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33746-120">-ResourceGroupName</span></span>
<span data-ttu-id="33746-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="33746-121">Name of resource group.</span></span>

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

### <span data-ttu-id="33746-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33746-122">CommonParameters</span></span>
<span data-ttu-id="33746-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33746-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33746-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="33746-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33746-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="33746-125">INPUTS</span></span>

### <span data-ttu-id="33746-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="33746-126">None</span></span>

## <span data-ttu-id="33746-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="33746-127">OUTPUTS</span></span>

### <span data-ttu-id="33746-128">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="33746-128">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="33746-129">Microsoft.Azure.Commands.EnterpriseDb.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="33746-129">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="33746-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="33746-130">NOTES</span></span>

## <span data-ttu-id="33746-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="33746-131">RELATED LINKS</span></span>
