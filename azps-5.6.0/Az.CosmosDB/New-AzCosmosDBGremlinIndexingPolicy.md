---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlinindexingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIndexingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIndexingPolicy.md
ms.openlocfilehash: ce554f3591f022bdbc375c12a50ea9dae85b8baa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998813"
---
# <span data-ttu-id="f4923-101">New-AzCosmosDBGremlinIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="f4923-101">New-AzCosmosDBGremlinIndexingPolicy</span></span>

## <span data-ttu-id="f4923-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4923-102">SYNOPSIS</span></span>
<span data-ttu-id="f4923-103">Crea un nuovo oggettoDb IndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="f4923-103">Creates a new CosmosDB IndexingPolicy object.</span></span>

## <span data-ttu-id="f4923-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f4923-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIndexingPolicy [-IncludedPath <PSIncludedPath[]>] [-SpatialSpec <PSSpatialSpec[]>]
 [-CompositePath <PSCompositePath[][]>] [-ExcludedPath <String[]>] [-Automatic <Boolean>]
 [-IndexingMode <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4923-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f4923-105">DESCRIPTION</span></span>
<span data-ttu-id="f4923-106">Il cmdlet **New-AzCosmosDBGremlinIndexingPolicy** crea un nuovo oggetto di tipo PSIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="f4923-106">The **New-AzCosmosDBGremlinIndexingPolicy** cmdlet creates a new object of type PSIndexingPolicy.</span></span>

## <span data-ttu-id="f4923-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f4923-107">EXAMPLES</span></span>

### <span data-ttu-id="f4923-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f4923-108">Example 1</span></span>
```powershell
PS C:\> $ipath1 = New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash
PS C:\>> $ipath2 = New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash
PS C:\>> $IncludedPath = New-AzCosmosDBGremlinIncludedPath -Path "/*" -Index $ipath1, $ipath2
PS C:\>>  $SpatialSpec = New-AzCosmosDBGremlinSpatialSpec -Path  "/mySpatialPath/*" -Type  "Point", "LineString", "Polygon", "MultiPolygon"
PS C:\>> $cp1 = New-AzCosmosDBGremlinCompositePath -Path "/abc" -Order Ascending
PS C:\>>  $cp2 = New-AzCosmosDBGremlinCompositePath -Path "/aberc" -Order Descending
PS C:\>> $compositePath = (($cp1, $cp2), ($cp2, $cp1))
PS C:\>> New-AzCosmosDBGremlinIndexingPolicy -IncludedPath $IncludedPath -SpatialSpec $SpatialSpec -CompositePath $compositePath -ExcludedPath "/myPathToNotIndex/*" -Automatic 1 -IndexingMode Consistent


Automatic        : True
IndexingMode     : Consistent
IncludedPaths    : {Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath}
ExcludedPaths    : {Microsoft.Azure.Commands.CosmosDB.Models.PSExcludedPath}
CompositeIndexes : {Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath,
                   Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath}
SpatialIndexes   : {Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec}
```

<span data-ttu-id="f4923-109">{{ Aggiungi la descrizione di esempio qui }}</span><span class="sxs-lookup"><span data-stu-id="f4923-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="f4923-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4923-110">PARAMETERS</span></span>

### <span data-ttu-id="f4923-111">-Automatico</span><span class="sxs-lookup"><span data-stu-id="f4923-111">-Automatic</span></span>
<span data-ttu-id="f4923-112">Bool per indicare se il criterio di indicizzazione è automatico</span><span class="sxs-lookup"><span data-stu-id="f4923-112">Bool to indicate if the indexing policy is automatic</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4923-113">-CompositePath</span><span class="sxs-lookup"><span data-stu-id="f4923-113">-CompositePath</span></span>
<span data-ttu-id="f4923-114">Matrice di matrice di oggetti di tipo Microsoft.Azure.Commands.FosDB.PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="f4923-114">Array of array of objects of type Microsoft.Azure.Commands.CosmosDB.PSCompositePath</span></span>

```yaml
Type: PSCompositePath[][]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4923-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4923-115">-DefaultProfile</span></span>
<span data-ttu-id="f4923-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f4923-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4923-117">-ExcludedPath</span><span class="sxs-lookup"><span data-stu-id="f4923-117">-ExcludedPath</span></span>
<span data-ttu-id="f4923-118">Matrice di stringhe contenenti excludedPath(specifica un percorso all'interno di un documento JSON da escludere nel servizio DB di Azure Azure.  .</span><span class="sxs-lookup"><span data-stu-id="f4923-118">Array of strings containing excludedPath(Specifies a path within a JSON document to be excluded in the Azure Cosmos DB service.)  elements.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4923-119">-IncludedPath</span><span class="sxs-lookup"><span data-stu-id="f4923-119">-IncludedPath</span></span>
<span data-ttu-id="f4923-120">Matrice di stringhe contenenti includedPath (specifica un percorso all'interno di un documento JSON da includere negli elementi del servizio DB di Azure Vengonos).</span><span class="sxs-lookup"><span data-stu-id="f4923-120">Array of strings containing includedPath (Specifies a path within a JSON document to be included in the Azure Cosmos DB service.) elements.</span></span>

```yaml
Type: PSIncludedPath[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4923-121">-IndexingMode</span><span class="sxs-lookup"><span data-stu-id="f4923-121">-IndexingMode</span></span>
<span data-ttu-id="f4923-122">Indica la modalità di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="f4923-122">Indicates the indexing mode.</span></span>
<span data-ttu-id="f4923-123">I valori possibili includono: 'Coerente', 'Lazi', 'Nessuno'</span><span class="sxs-lookup"><span data-stu-id="f4923-123">Possible values include: 'Consistent', 'Lazy', 'None'</span></span>

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

### <span data-ttu-id="f4923-124">-SpatialSpec</span><span class="sxs-lookup"><span data-stu-id="f4923-124">-SpatialSpec</span></span>
<span data-ttu-id="f4923-125">Matrice di oggetti di tipo Microsoft.Azure.Commands.BulsDB.PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="f4923-125">Array of objects of type Microsoft.Azure.Commands.CosmosDB.PSSpatialSpec</span></span>

```yaml
Type: PSSpatialSpec[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4923-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4923-126">CommonParameters</span></span>
<span data-ttu-id="f4923-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4923-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4923-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f4923-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4923-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="f4923-129">INPUTS</span></span>

### <span data-ttu-id="f4923-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f4923-130">None</span></span>

## <span data-ttu-id="f4923-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f4923-131">OUTPUTS</span></span>

### <span data-ttu-id="f4923-132">Microsoft.Azure.Commands.EnterpriseDb.Models.PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="f4923-132">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

## <span data-ttu-id="f4923-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="f4923-133">NOTES</span></span>

## <span data-ttu-id="f4923-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f4923-134">RELATED LINKS</span></span>
