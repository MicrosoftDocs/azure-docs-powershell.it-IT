---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlindexingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIndexingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIndexingPolicy.md
ms.openlocfilehash: cb8ecea538273adf9db14168a3b60d5679536cda
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204627"
---
# <span data-ttu-id="f3adc-101">New-AzCosmosDBSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="f3adc-101">New-AzCosmosDBSqlIndexingPolicy</span></span>

## <span data-ttu-id="f3adc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3adc-102">SYNOPSIS</span></span>
<span data-ttu-id="f3adc-103">Crea un nuovo oggettoDb Sql IndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="f3adc-103">Creates a new CosmosDB Sql IndexingPolicy object.</span></span>

## <span data-ttu-id="f3adc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f3adc-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlIndexingPolicy [-IncludedPath <PSIncludedPath[]>] [-SpatialSpec <PSSpatialSpec[]>]
 [-CompositePath <PSCompositePath[][]>] [-ExcludedPath <String[]>] [-Automatic <Boolean>]
 [-IndexingMode <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3adc-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f3adc-105">DESCRIPTION</span></span>
<span data-ttu-id="f3adc-106">Il cmdlet **New-AzCosmosDBSqlIndexingPolicy** crea un nuovo oggetto di tipo PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="f3adc-106">The **New-AzCosmosDBSqlIndexingPolicy** cmdlet creates a new object of type PSSqlIndexingPolicy.</span></span>

## <span data-ttu-id="f3adc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f3adc-107">EXAMPLES</span></span>

### <span data-ttu-id="f3adc-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f3adc-108">Example 1</span></span>
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

## <span data-ttu-id="f3adc-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3adc-109">PARAMETERS</span></span>

### <span data-ttu-id="f3adc-110">-Automatico</span><span class="sxs-lookup"><span data-stu-id="f3adc-110">-Automatic</span></span>
<span data-ttu-id="f3adc-111">Bool per indicare se il criterio di indicizzazione è automatico</span><span class="sxs-lookup"><span data-stu-id="f3adc-111">Bool to indicate if the indexing policy is automatic</span></span>

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

### <span data-ttu-id="f3adc-112">-CompositePath</span><span class="sxs-lookup"><span data-stu-id="f3adc-112">-CompositePath</span></span>
<span data-ttu-id="f3adc-113">Matrice di matrice di oggetti di tipo Microsoft.Azure.Commands.FosDB.PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="f3adc-113">Array of array of objects of type Microsoft.Azure.Commands.CosmosDB.PSCompositePath</span></span>

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

### <span data-ttu-id="f3adc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3adc-114">-DefaultProfile</span></span>
<span data-ttu-id="f3adc-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f3adc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3adc-116">-ExcludedPath</span><span class="sxs-lookup"><span data-stu-id="f3adc-116">-ExcludedPath</span></span>
<span data-ttu-id="f3adc-117">Matrice di stringhe contenenti excludedPath(specifica un percorso all'interno di un documento JSON da escludere nel servizio DB di Azure Cordiale).)  .</span><span class="sxs-lookup"><span data-stu-id="f3adc-117">Array of strings containing excludedPath(Specifies a path within a JSON document to be excluded in the Azure Cosmos DB service.)  elements.</span></span>

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

### <span data-ttu-id="f3adc-118">-IncludedPath</span><span class="sxs-lookup"><span data-stu-id="f3adc-118">-IncludedPath</span></span>
<span data-ttu-id="f3adc-119">Matrice di stringhe contenenti includedPath (specifica un percorso all'interno di un documento JSON da includere negli elementi del servizio DB di Azure Cordiale).</span><span class="sxs-lookup"><span data-stu-id="f3adc-119">Array of strings containing includedPath (Specifies a path within a JSON document to be included in the Azure Cosmos DB service.) elements.</span></span>

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

### <span data-ttu-id="f3adc-120">-IndexingMode</span><span class="sxs-lookup"><span data-stu-id="f3adc-120">-IndexingMode</span></span>
<span data-ttu-id="f3adc-121">indica la modalità di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="f3adc-121">indicates the indexing mode.</span></span>
<span data-ttu-id="f3adc-122">I valori possibili includono: 'Coerente', 'Lazi', 'Nessuno'</span><span class="sxs-lookup"><span data-stu-id="f3adc-122">Possible values include: 'Consistent', 'Lazy', 'None'</span></span>

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

### <span data-ttu-id="f3adc-123">-SpatialSpec</span><span class="sxs-lookup"><span data-stu-id="f3adc-123">-SpatialSpec</span></span>
<span data-ttu-id="f3adc-124">Matrice di oggetti di tipo Microsoft.Azure.Commands.BulsDB.PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="f3adc-124">Array of objects of type Microsoft.Azure.Commands.CosmosDB.PSSpatialSpec</span></span>

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

### <span data-ttu-id="f3adc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3adc-125">CommonParameters</span></span>
<span data-ttu-id="f3adc-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3adc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3adc-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f3adc-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3adc-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="f3adc-128">INPUTS</span></span>

### <span data-ttu-id="f3adc-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f3adc-129">None</span></span>

## <span data-ttu-id="f3adc-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f3adc-130">OUTPUTS</span></span>

### <span data-ttu-id="f3adc-131">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="f3adc-131">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

## <span data-ttu-id="f3adc-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="f3adc-132">NOTES</span></span>

## <span data-ttu-id="f3adc-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f3adc-133">RELATED LINKS</span></span>
