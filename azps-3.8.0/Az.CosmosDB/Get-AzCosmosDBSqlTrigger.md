---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 6631cad83260a935f2849391941ec0cf6514b188
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018518"
---
# <span data-ttu-id="68d9d-101">Get-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="68d9d-101">Get-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="68d9d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="68d9d-102">SYNOPSIS</span></span>
<span data-ttu-id="68d9d-103">Ottiene il trigger SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="68d9d-103">Gets the CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="68d9d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="68d9d-104">SYNTAX</span></span>

### <span data-ttu-id="68d9d-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="68d9d-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68d9d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="68d9d-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68d9d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="68d9d-107">DESCRIPTION</span></span>
<span data-ttu-id="68d9d-108">Il cmdlet **Get-AzCosmosDBSqlTrigger** Ottiene l'elenco di tutti i trigger SQL CosmosDB esistenti per un determinato ResourceGroupName, AccountName, DatabaseName e ContainerName e ottiene un singolo trigger SQL CosmosDB per un determinato ResourceGroupName, AccountName, DatabaseName, ContainerName e triggername.</span><span class="sxs-lookup"><span data-stu-id="68d9d-108">The **Get-AzCosmosDBSqlTrigger** cmdlet gets the list of all existing CosmosDB Sql Triggers for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql Trigger for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and TriggerName.</span></span>

## <span data-ttu-id="68d9d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="68d9d-109">EXAMPLES</span></span>

### <span data-ttu-id="68d9d-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="68d9d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlTrigger -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {triggerName} -ContainerName {containerName} 

Name                   : {triggerName}
Id                     : {triggerId}
Resource               : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="68d9d-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="68d9d-111">PARAMETERS</span></span>

### <span data-ttu-id="68d9d-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="68d9d-112">-AccountName</span></span>
<span data-ttu-id="68d9d-113">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="68d9d-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="68d9d-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="68d9d-114">-ContainerName</span></span>
<span data-ttu-id="68d9d-115">Nome contenitore.</span><span class="sxs-lookup"><span data-stu-id="68d9d-115">Container name.</span></span>

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

### <span data-ttu-id="68d9d-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="68d9d-116">-DatabaseName</span></span>
<span data-ttu-id="68d9d-117">Nome database.</span><span class="sxs-lookup"><span data-stu-id="68d9d-117">Database name.</span></span>

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

### <span data-ttu-id="68d9d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68d9d-118">-DefaultProfile</span></span>
<span data-ttu-id="68d9d-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="68d9d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68d9d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68d9d-120">-InputObject</span></span>
<span data-ttu-id="68d9d-121">Oggetto contenitore SQL.</span><span class="sxs-lookup"><span data-stu-id="68d9d-121">Sql Container object.</span></span>

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

### <span data-ttu-id="68d9d-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="68d9d-122">-Name</span></span>
<span data-ttu-id="68d9d-123">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="68d9d-123">Trigger name.</span></span>

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

### <span data-ttu-id="68d9d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68d9d-124">-ResourceGroupName</span></span>
<span data-ttu-id="68d9d-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="68d9d-125">Name of resource group.</span></span>

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

### <span data-ttu-id="68d9d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68d9d-126">CommonParameters</span></span>
<span data-ttu-id="68d9d-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68d9d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68d9d-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68d9d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68d9d-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="68d9d-129">INPUTS</span></span>

### <span data-ttu-id="68d9d-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="68d9d-130">None</span></span>

## <span data-ttu-id="68d9d-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="68d9d-131">OUTPUTS</span></span>

### <span data-ttu-id="68d9d-132">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="68d9d-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="68d9d-133">Note</span><span class="sxs-lookup"><span data-stu-id="68d9d-133">NOTES</span></span>

## <span data-ttu-id="68d9d-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="68d9d-134">RELATED LINKS</span></span>
