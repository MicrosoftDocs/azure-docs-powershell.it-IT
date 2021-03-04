---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqlindexingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIndexingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIndexingPolicy.md
ms.openlocfilehash: b3d7591bf5dd83967230f6c96c3ca5b02232e316
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975917"
---
# <span data-ttu-id="a9dec-101">New-AzCosmosDBSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="a9dec-101">New-AzCosmosDBSqlIndexingPolicy</span></span>

## <span data-ttu-id="a9dec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9dec-102">SYNOPSIS</span></span>
<span data-ttu-id="a9dec-103">Crea un nuovo oggettoDb Sql IndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="a9dec-103">Creates a new CosmosDB Sql IndexingPolicy object.</span></span>

## <span data-ttu-id="a9dec-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a9dec-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlIndexingPolicy [-IncludedPath <PSIncludedPath[]>] [-SpatialSpec <PSSpatialSpec[]>]
 [-CompositePath <PSCompositePath[][]>] [-ExcludedPath <String[]>] [-Automatic <Boolean>]
 [-IndexingMode <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9dec-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a9dec-105">DESCRIPTION</span></span>
<span data-ttu-id="a9dec-106">Il cmdlet **New-AzCosmosDBSqlIndexingPolicy** crea un nuovo oggetto di tipo PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="a9dec-106">The **New-AzCosmosDBSqlIndexingPolicy** cmdlet creates a new object of type PSSqlIndexingPolicy.</span></span>

## <span data-ttu-id="a9dec-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a9dec-107">EXAMPLES</span></span>

### <span data-ttu-id="a9dec-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a9dec-108">Example 1</span></span>
```powershell
PS C:\> $ipath1 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
PS C:\> $ipath2 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
PS C:\> $IncludedPath = New-AzCosmosDBSqlIncludedPath -Path "/*" -Index $ipath1, $ipath2
PS C:\>  $SpatialSpec = New-AzCosmosDBSqlSpatialSpec -Path  "/mySpatialPath/*" -Type  "Point", "LineString", "Polygon", "MultiPolygon"
PS C:\> $cp1 = New-AzCosmosDBSqlCompositePath -Path "/abc" -Order Ascending
PS C:\>  $cp2 = New-AzCosmosDBSqlCompositePath -Path "/aberc" -Order Descending
PS C:\> $compositePath = (($cp1, $cp2), ($cp2, $cp1))
PS C:\> New-AzCosmosDBSqlIndexingPolicy -IncludedPath $IncludedPath -SpatialSpec $SpatialSpec -CompositePath $compositePath -ExcludedPath "/myPathToNotIndex/*" -Automatic 1 -IndexingMode Consistent

Automatic        : True
IndexingMode     : Consistent
IncludedPaths    : {Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath}
ExcludedPaths    : {Microsoft.Azure.Commands.CosmosDB.Models.PSExcludedPath}
CompositeIndexes : {Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath,
                   Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath}
SpatialIndexes   : {Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec}
```

## <span data-ttu-id="a9dec-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9dec-109">PARAMETERS</span></span>

### <span data-ttu-id="a9dec-110">-Automatico</span><span class="sxs-lookup"><span data-stu-id="a9dec-110">-Automatic</span></span>
<span data-ttu-id="a9dec-111">Bool per indicare se il criterio di indicizzazione è automatico</span><span class="sxs-lookup"><span data-stu-id="a9dec-111">Bool to indicate if the indexing policy is automatic</span></span>

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

### <span data-ttu-id="a9dec-112">-CompositePath</span><span class="sxs-lookup"><span data-stu-id="a9dec-112">-CompositePath</span></span>
<span data-ttu-id="a9dec-113">Matrice di matrice di oggetti di tipo Microsoft.Azure.Commands.FosDB.PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="a9dec-113">Array of array of objects of type Microsoft.Azure.Commands.CosmosDB.PSCompositePath</span></span>

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

### <span data-ttu-id="a9dec-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9dec-114">-DefaultProfile</span></span>
<span data-ttu-id="a9dec-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a9dec-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9dec-116">-ExcludedPath</span><span class="sxs-lookup"><span data-stu-id="a9dec-116">-ExcludedPath</span></span>
<span data-ttu-id="a9dec-117">Matrice di stringhe contenenti excludedPath(specifica un percorso all'interno di un documento JSON da escludere nel servizio DB di Azure Cordiale).)  .</span><span class="sxs-lookup"><span data-stu-id="a9dec-117">Array of strings containing excludedPath(Specifies a path within a JSON document to be excluded in the Azure Cosmos DB service.)  elements.</span></span>

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

### <span data-ttu-id="a9dec-118">-IncludedPath</span><span class="sxs-lookup"><span data-stu-id="a9dec-118">-IncludedPath</span></span>
<span data-ttu-id="a9dec-119">Matrice di stringhe contenenti includedPath (specifica un percorso all'interno di un documento JSON da includere negli elementi del servizio DB di Azure Vengonos).</span><span class="sxs-lookup"><span data-stu-id="a9dec-119">Array of strings containing includedPath (Specifies a path within a JSON document to be included in the Azure Cosmos DB service.) elements.</span></span>

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

### <span data-ttu-id="a9dec-120">-IndexingMode</span><span class="sxs-lookup"><span data-stu-id="a9dec-120">-IndexingMode</span></span>
<span data-ttu-id="a9dec-121">indica la modalità di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="a9dec-121">indicates the indexing mode.</span></span>
<span data-ttu-id="a9dec-122">I valori possibili includono: 'Coerente', 'Lazi', 'Nessuno'</span><span class="sxs-lookup"><span data-stu-id="a9dec-122">Possible values include: 'Consistent', 'Lazy', 'None'</span></span>

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

### <span data-ttu-id="a9dec-123">-SpatialSpec</span><span class="sxs-lookup"><span data-stu-id="a9dec-123">-SpatialSpec</span></span>
<span data-ttu-id="a9dec-124">Matrice di oggetti di tipo Microsoft.Azure.Commands.BulsDB.PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="a9dec-124">Array of objects of type Microsoft.Azure.Commands.CosmosDB.PSSpatialSpec</span></span>

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

### <span data-ttu-id="a9dec-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9dec-125">CommonParameters</span></span>
<span data-ttu-id="a9dec-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9dec-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9dec-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a9dec-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9dec-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="a9dec-128">INPUTS</span></span>

### <span data-ttu-id="a9dec-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a9dec-129">None</span></span>

## <span data-ttu-id="a9dec-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a9dec-130">OUTPUTS</span></span>

### <span data-ttu-id="a9dec-131">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="a9dec-131">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

## <span data-ttu-id="a9dec-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="a9dec-132">NOTES</span></span>

## <span data-ttu-id="a9dec-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a9dec-133">RELATED LINKS</span></span>
