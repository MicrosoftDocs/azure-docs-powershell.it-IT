---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 5efdbc3f1f8172ba59a78d4ec462f57a527faf07
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93865353"
---
# <span data-ttu-id="882ac-101">Get-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="882ac-101">Get-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="882ac-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="882ac-102">SYNOPSIS</span></span>
<span data-ttu-id="882ac-103">Ottiene il database SQL di CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="882ac-103">Gets the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="882ac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="882ac-104">SYNTAX</span></span>

### <span data-ttu-id="882ac-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="882ac-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="882ac-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="882ac-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabase [-Name <String>] -InputObject <PSDatabaseAccount> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="882ac-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="882ac-107">DESCRIPTION</span></span>
<span data-ttu-id="882ac-108">Il cmdlet **Get-AzCosmosDBSqlDatabase** Ottiene l'elenco di tutti i database SQL CosmosDB esistenti per un ResourceGroupName specifico, AccountName e ottiene un singolo database SQL di CosmosDB per una determinata ResourceGroupName, AccountName, DatabaseName e ContainerName.</span><span class="sxs-lookup"><span data-stu-id="882ac-108">The **Get-AzCosmosDBSqlDatabase** cmdlet gets the list of all existing CosmosDB Sql Databases for a given ResourceGroupName, AccountName and gets a single CosmosDB Sql Database for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="882ac-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="882ac-109">EXAMPLES</span></span>

### <span data-ttu-id="882ac-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="882ac-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabase -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                    : {databaseName}
Id                      : {databaseId}
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="882ac-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="882ac-111">PARAMETERS</span></span>

### <span data-ttu-id="882ac-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="882ac-112">-AccountName</span></span>
<span data-ttu-id="882ac-113">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="882ac-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="882ac-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="882ac-114">-DefaultProfile</span></span>
<span data-ttu-id="882ac-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="882ac-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="882ac-116">-Dettagli</span><span class="sxs-lookup"><span data-stu-id="882ac-116">-Detailed</span></span>
<span data-ttu-id="882ac-117">Se specificato, il cmdlet restituisce il contenitore con il valore della velocità effettiva.</span><span class="sxs-lookup"><span data-stu-id="882ac-117">If provided then, the cmdlet returns the container with the throughput value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="882ac-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="882ac-118">-InputObject</span></span>
<span data-ttu-id="882ac-119">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="882ac-119">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="882ac-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="882ac-120">-Name</span></span>
<span data-ttu-id="882ac-121">Nome database.</span><span class="sxs-lookup"><span data-stu-id="882ac-121">Database name.</span></span>

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

### <span data-ttu-id="882ac-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="882ac-122">-ResourceGroupName</span></span>
<span data-ttu-id="882ac-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="882ac-123">Name of resource group.</span></span>

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

### <span data-ttu-id="882ac-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="882ac-124">CommonParameters</span></span>
<span data-ttu-id="882ac-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="882ac-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="882ac-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="882ac-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="882ac-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="882ac-127">INPUTS</span></span>

### <span data-ttu-id="882ac-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="882ac-128">None</span></span>

## <span data-ttu-id="882ac-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="882ac-129">OUTPUTS</span></span>

### <span data-ttu-id="882ac-130">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="882ac-130">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="882ac-131">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="882ac-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="882ac-132">Note</span><span class="sxs-lookup"><span data-stu-id="882ac-132">NOTES</span></span>

## <span data-ttu-id="882ac-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="882ac-133">RELATED LINKS</span></span>
