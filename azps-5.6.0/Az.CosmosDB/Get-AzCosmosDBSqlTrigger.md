---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 28b616315913ae70722b5a600d4b10879c7b8334
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986913"
---
# <span data-ttu-id="4d37a-101">Get-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="4d37a-101">Get-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="4d37a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d37a-102">SYNOPSIS</span></span>
<span data-ttu-id="4d37a-103">Recupera il trigger sqldb del database.</span><span class="sxs-lookup"><span data-stu-id="4d37a-103">Gets the CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="4d37a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4d37a-104">SYNTAX</span></span>

### <span data-ttu-id="4d37a-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d37a-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d37a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d37a-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d37a-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4d37a-107">DESCRIPTION</span></span>
<span data-ttu-id="4d37a-108">Il cmdlet **Get-AzCosmosDBSqlTrigger** ottiene l'elenco di tutti i trigger SQL esistenti per Un determinato ResourceGroupName, AccountName, DatabaseName e ContainerName e ottiene un singolo trigger SQL DiRDB per un determinato valore di ResourceGroupName, AccountName, DatabaseName, ContainerName e TriggerName.</span><span class="sxs-lookup"><span data-stu-id="4d37a-108">The **Get-AzCosmosDBSqlTrigger** cmdlet gets the list of all existing CosmosDB Sql Triggers for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql Trigger for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and TriggerName.</span></span>

## <span data-ttu-id="4d37a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4d37a-109">EXAMPLES</span></span>

### <span data-ttu-id="4d37a-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4d37a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlTrigger -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {triggerName} -ContainerName {containerName} 

Name                   : {triggerName}
Id                     : {triggerId}
Resource               : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="4d37a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d37a-111">PARAMETERS</span></span>

### <span data-ttu-id="4d37a-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4d37a-112">-AccountName</span></span>
<span data-ttu-id="4d37a-113">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="4d37a-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="4d37a-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="4d37a-114">-ContainerName</span></span>
<span data-ttu-id="4d37a-115">Nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="4d37a-115">Container name.</span></span>

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

### <span data-ttu-id="4d37a-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4d37a-116">-DatabaseName</span></span>
<span data-ttu-id="4d37a-117">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="4d37a-117">Database name.</span></span>

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

### <span data-ttu-id="4d37a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d37a-118">-DefaultProfile</span></span>
<span data-ttu-id="4d37a-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4d37a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d37a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4d37a-120">-Name</span></span>
<span data-ttu-id="4d37a-121">Nome trigger.</span><span class="sxs-lookup"><span data-stu-id="4d37a-121">Trigger name.</span></span>

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

### <span data-ttu-id="4d37a-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4d37a-122">-ParentObject</span></span>
<span data-ttu-id="4d37a-123">Oggetto Contenitore Sql.</span><span class="sxs-lookup"><span data-stu-id="4d37a-123">Sql Container object.</span></span>

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

### <span data-ttu-id="4d37a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d37a-124">-ResourceGroupName</span></span>
<span data-ttu-id="4d37a-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4d37a-125">Name of resource group.</span></span>

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

### <span data-ttu-id="4d37a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d37a-126">CommonParameters</span></span>
<span data-ttu-id="4d37a-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d37a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d37a-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4d37a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d37a-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="4d37a-129">INPUTS</span></span>

### <span data-ttu-id="4d37a-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4d37a-130">None</span></span>

## <span data-ttu-id="4d37a-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4d37a-131">OUTPUTS</span></span>

### <span data-ttu-id="4d37a-132">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="4d37a-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="4d37a-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="4d37a-133">NOTES</span></span>

## <span data-ttu-id="4d37a-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4d37a-134">RELATED LINKS</span></span>
