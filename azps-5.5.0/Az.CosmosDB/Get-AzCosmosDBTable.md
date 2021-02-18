---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
ms.openlocfilehash: d405c081ab1f848e25b67de4ec100f40b40fb4c8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181374"
---
# <span data-ttu-id="cc374-101">Get-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="cc374-101">Get-AzCosmosDBTable</span></span>

## <span data-ttu-id="cc374-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc374-102">SYNOPSIS</span></span>
<span data-ttu-id="cc374-103">Ottiene una tabellaDbDb.</span><span class="sxs-lookup"><span data-stu-id="cc374-103">Gets a CosmosDB Table.</span></span>

## <span data-ttu-id="cc374-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cc374-104">SYNTAX</span></span>

### <span data-ttu-id="cc374-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cc374-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc374-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc374-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBTable [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc374-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cc374-107">DESCRIPTION</span></span>
<span data-ttu-id="cc374-108">Il **cmdlet Get-AzCosmosDBTable** ottiene una tabella esistente.</span><span class="sxs-lookup"><span data-stu-id="cc374-108">The **Get-AzCosmosDBTable** cmdlet gets an existing Table.</span></span>

## <span data-ttu-id="cc374-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cc374-109">EXAMPLES</span></span>

### <span data-ttu-id="cc374-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cc374-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}

Name    Id    Resource
{name}  {id}  Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

<span data-ttu-id="cc374-111">L'oggetto risorsa _rid proprietà _ts, _ts etag_ della tabella.</span><span class="sxs-lookup"><span data-stu-id="cc374-111">Resource object contains _rid, _ts, _ etag properties of the Table.</span></span>

## <span data-ttu-id="cc374-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc374-112">PARAMETERS</span></span>

### <span data-ttu-id="cc374-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cc374-113">-AccountName</span></span>
<span data-ttu-id="cc374-114">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="cc374-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="cc374-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc374-115">-DefaultProfile</span></span>
<span data-ttu-id="cc374-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cc374-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc374-117">-Name</span><span class="sxs-lookup"><span data-stu-id="cc374-117">-Name</span></span>
<span data-ttu-id="cc374-118">Nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="cc374-118">Name of the Table.</span></span>

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

### <span data-ttu-id="cc374-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="cc374-119">-ParentObject</span></span>
<span data-ttu-id="cc374-120">Oggetto AccountDb Disa</span><span class="sxs-lookup"><span data-stu-id="cc374-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="cc374-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc374-121">-ResourceGroupName</span></span>
<span data-ttu-id="cc374-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cc374-122">Name of resource group.</span></span>

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

### <span data-ttu-id="cc374-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc374-123">CommonParameters</span></span>
<span data-ttu-id="cc374-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc374-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc374-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cc374-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc374-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="cc374-126">INPUTS</span></span>

### <span data-ttu-id="cc374-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="cc374-127">None</span></span>

## <span data-ttu-id="cc374-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cc374-128">OUTPUTS</span></span>

### <span data-ttu-id="cc374-129">Microsoft.Azure.Commands.EnterpriseDb.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="cc374-129">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="cc374-130">Microsoft.Azure.Commands.EnterpriseDb.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="cc374-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="cc374-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="cc374-131">NOTES</span></span>

## <span data-ttu-id="cc374-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cc374-132">RELATED LINKS</span></span>
