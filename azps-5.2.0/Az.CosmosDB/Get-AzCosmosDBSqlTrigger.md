---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 10faa4b020633fdf46122c4864d50f00ef3ba54c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372396"
---
# <span data-ttu-id="a4a58-101">Get-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="a4a58-101">Get-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="a4a58-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a4a58-102">SYNOPSIS</span></span>
<span data-ttu-id="a4a58-103">Ottiene il trigger SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="a4a58-103">Gets the CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="a4a58-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a4a58-104">SYNTAX</span></span>

### <span data-ttu-id="a4a58-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4a58-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4a58-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4a58-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4a58-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a4a58-107">DESCRIPTION</span></span>
<span data-ttu-id="a4a58-108">Il cmdlet **Get-AzCosmosDBSqlTrigger** Ottiene l'elenco di tutti i trigger SQL CosmosDB esistenti per un determinato ResourceGroupName, AccountName, DatabaseName e ContainerName e ottiene un singolo trigger SQL CosmosDB per un determinato ResourceGroupName, AccountName, DatabaseName, ContainerName e triggername.</span><span class="sxs-lookup"><span data-stu-id="a4a58-108">The **Get-AzCosmosDBSqlTrigger** cmdlet gets the list of all existing CosmosDB Sql Triggers for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql Trigger for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and TriggerName.</span></span>

## <span data-ttu-id="a4a58-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a4a58-109">EXAMPLES</span></span>

### <span data-ttu-id="a4a58-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a4a58-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlTrigger -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {triggerName} -ContainerName {containerName} 

Name                   : {triggerName}
Id                     : {triggerId}
Resource               : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="a4a58-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a4a58-111">PARAMETERS</span></span>

### <span data-ttu-id="a4a58-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a4a58-112">-AccountName</span></span>
<span data-ttu-id="a4a58-113">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="a4a58-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a4a58-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="a4a58-114">-ContainerName</span></span>
<span data-ttu-id="a4a58-115">Nome contenitore.</span><span class="sxs-lookup"><span data-stu-id="a4a58-115">Container name.</span></span>

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

### <span data-ttu-id="a4a58-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a4a58-116">-DatabaseName</span></span>
<span data-ttu-id="a4a58-117">Nome database.</span><span class="sxs-lookup"><span data-stu-id="a4a58-117">Database name.</span></span>

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

### <span data-ttu-id="a4a58-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4a58-118">-DefaultProfile</span></span>
<span data-ttu-id="a4a58-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a4a58-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4a58-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="a4a58-120">-Name</span></span>
<span data-ttu-id="a4a58-121">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="a4a58-121">Trigger name.</span></span>

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

### <span data-ttu-id="a4a58-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a4a58-122">-ParentObject</span></span>
<span data-ttu-id="a4a58-123">Oggetto contenitore SQL.</span><span class="sxs-lookup"><span data-stu-id="a4a58-123">Sql Container object.</span></span>

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

### <span data-ttu-id="a4a58-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4a58-124">-ResourceGroupName</span></span>
<span data-ttu-id="a4a58-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a4a58-125">Name of resource group.</span></span>

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

### <span data-ttu-id="a4a58-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4a58-126">CommonParameters</span></span>
<span data-ttu-id="a4a58-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4a58-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4a58-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4a58-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4a58-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a4a58-129">INPUTS</span></span>

### <span data-ttu-id="a4a58-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a4a58-130">None</span></span>

## <span data-ttu-id="a4a58-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a4a58-131">OUTPUTS</span></span>

### <span data-ttu-id="a4a58-132">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="a4a58-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="a4a58-133">Note</span><span class="sxs-lookup"><span data-stu-id="a4a58-133">NOTES</span></span>

## <span data-ttu-id="a4a58-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a4a58-134">RELATED LINKS</span></span>
