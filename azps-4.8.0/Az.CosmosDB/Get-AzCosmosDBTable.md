---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
ms.openlocfilehash: d405c081ab1f848e25b67de4ec100f40b40fb4c8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190348"
---
# <span data-ttu-id="49c3b-101">Get-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="49c3b-101">Get-AzCosmosDBTable</span></span>

## <span data-ttu-id="49c3b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="49c3b-102">SYNOPSIS</span></span>
<span data-ttu-id="49c3b-103">Ottiene una tabella CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="49c3b-103">Gets a CosmosDB Table.</span></span>

## <span data-ttu-id="49c3b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="49c3b-104">SYNTAX</span></span>

### <span data-ttu-id="49c3b-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="49c3b-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49c3b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="49c3b-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBTable [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49c3b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="49c3b-107">DESCRIPTION</span></span>
<span data-ttu-id="49c3b-108">Il cmdlet **Get-AzCosmosDBTable** ottiene una tabella esistente.</span><span class="sxs-lookup"><span data-stu-id="49c3b-108">The **Get-AzCosmosDBTable** cmdlet gets an existing Table.</span></span>

## <span data-ttu-id="49c3b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="49c3b-109">EXAMPLES</span></span>

### <span data-ttu-id="49c3b-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="49c3b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}

Name    Id    Resource
{name}  {id}  Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

<span data-ttu-id="49c3b-111">L'oggetto Resource contiene le proprietà _rid, _ts, _ ETag della tabella.</span><span class="sxs-lookup"><span data-stu-id="49c3b-111">Resource object contains _rid, _ts, _ etag properties of the Table.</span></span>

## <span data-ttu-id="49c3b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="49c3b-112">PARAMETERS</span></span>

### <span data-ttu-id="49c3b-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="49c3b-113">-AccountName</span></span>
<span data-ttu-id="49c3b-114">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="49c3b-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="49c3b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49c3b-115">-DefaultProfile</span></span>
<span data-ttu-id="49c3b-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="49c3b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49c3b-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="49c3b-117">-Name</span></span>
<span data-ttu-id="49c3b-118">Nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="49c3b-118">Name of the Table.</span></span>

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

### <span data-ttu-id="49c3b-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="49c3b-119">-ParentObject</span></span>
<span data-ttu-id="49c3b-120">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="49c3b-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49c3b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49c3b-121">-ResourceGroupName</span></span>
<span data-ttu-id="49c3b-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="49c3b-122">Name of resource group.</span></span>

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

### <span data-ttu-id="49c3b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49c3b-123">CommonParameters</span></span>
<span data-ttu-id="49c3b-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49c3b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49c3b-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="49c3b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49c3b-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="49c3b-126">INPUTS</span></span>

### <span data-ttu-id="49c3b-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="49c3b-127">None</span></span>

## <span data-ttu-id="49c3b-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="49c3b-128">OUTPUTS</span></span>

### <span data-ttu-id="49c3b-129">Microsoft. Azure. Commands. CosmosDB. Models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="49c3b-129">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="49c3b-130">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="49c3b-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="49c3b-131">Note</span><span class="sxs-lookup"><span data-stu-id="49c3b-131">NOTES</span></span>

## <span data-ttu-id="49c3b-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="49c3b-132">RELATED LINKS</span></span>