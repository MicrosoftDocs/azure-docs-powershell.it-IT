---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbtablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTableThroughput.md
ms.openlocfilehash: 7b48190a9ef01d468e762d93d7bc63a96e831de8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986872"
---
# <span data-ttu-id="7dc0f-101">Get-AzCosmosDBTableThroughput</span><span class="sxs-lookup"><span data-stu-id="7dc0f-101">Get-AzCosmosDBTableThroughput</span></span>

## <span data-ttu-id="7dc0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7dc0f-102">SYNOPSIS</span></span>
<span data-ttu-id="7dc0f-103">Ottiene la velocità effettiva di una tabella AMMORT.</span><span class="sxs-lookup"><span data-stu-id="7dc0f-103">Gets the throughput of a CosmosDB Table.</span></span>

## <span data-ttu-id="7dc0f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7dc0f-104">SYNTAX</span></span>

### <span data-ttu-id="7dc0f-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7dc0f-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTableThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7dc0f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7dc0f-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBTableThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7dc0f-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7dc0f-107">DESCRIPTION</span></span>
<span data-ttu-id="7dc0f-108">Il cmdlet **Get-AzCosmosDBTableThroughput** ottiene la velocità effettiva di una tabella Da fare.</span><span class="sxs-lookup"><span data-stu-id="7dc0f-108">The **Get-AzCosmosDBTableThroughput** cmdlet gets the throughput of a CosmosDB Table.</span></span>

## <span data-ttu-id="7dc0f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7dc0f-109">EXAMPLES</span></span>

### <span data-ttu-id="7dc0f-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7dc0f-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTableThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="7dc0f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7dc0f-111">PARAMETERS</span></span>

### <span data-ttu-id="7dc0f-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7dc0f-112">-AccountName</span></span>
<span data-ttu-id="7dc0f-113">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="7dc0f-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7dc0f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dc0f-114">-DefaultProfile</span></span>
<span data-ttu-id="7dc0f-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7dc0f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7dc0f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7dc0f-116">-InputObject</span></span>
<span data-ttu-id="7dc0f-117">Oggetto Account Aziendale</span><span class="sxs-lookup"><span data-stu-id="7dc0f-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="7dc0f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="7dc0f-118">-Name</span></span>
<span data-ttu-id="7dc0f-119">Nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="7dc0f-119">Name of the Table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7dc0f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7dc0f-120">-ResourceGroupName</span></span>
<span data-ttu-id="7dc0f-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7dc0f-121">Name of resource group.</span></span>

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

### <span data-ttu-id="7dc0f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dc0f-122">CommonParameters</span></span>
<span data-ttu-id="7dc0f-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7dc0f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dc0f-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7dc0f-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dc0f-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="7dc0f-125">INPUTS</span></span>

### <span data-ttu-id="7dc0f-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7dc0f-126">None</span></span>

## <span data-ttu-id="7dc0f-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7dc0f-127">OUTPUTS</span></span>

### <span data-ttu-id="7dc0f-128">Microsoft.Azure.Commands.EnterpriseDb.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="7dc0f-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="7dc0f-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="7dc0f-129">NOTES</span></span>

## <span data-ttu-id="7dc0f-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7dc0f-130">RELATED LINKS</span></span>
