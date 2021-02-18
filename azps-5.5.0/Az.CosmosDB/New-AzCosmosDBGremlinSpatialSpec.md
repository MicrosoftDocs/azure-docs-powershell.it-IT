---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinspatialspec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinSpatialSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinSpatialSpec.md
ms.openlocfilehash: 6cdb0d9732c64f26e2ba840623ae6f6df06602b9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181318"
---
# <span data-ttu-id="ea768-101">New-AzCosmosDBGremlinSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="ea768-101">New-AzCosmosDBGremlinSpatialSpec</span></span>

## <span data-ttu-id="ea768-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea768-102">SYNOPSIS</span></span>
<span data-ttu-id="ea768-103">Crea un nuovo oggetto di tipo PSSpatialSpec.</span><span class="sxs-lookup"><span data-stu-id="ea768-103">Creates a new object of type PSSpatialSpec.</span></span> <span data-ttu-id="ea768-104">Può essere passato come valore di parametro per Set-AzCosmosDBGremlinIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="ea768-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinIndexingPolicy.</span></span>

## <span data-ttu-id="ea768-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ea768-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinSpatialSpec -Path <String> -Type <String[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ea768-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ea768-106">DESCRIPTION</span></span>
<span data-ttu-id="ea768-107">Crea un oggetto corrispondente all'API SpatialSpec dell'API Gremlin.</span><span class="sxs-lookup"><span data-stu-id="ea768-107">Creates Object corresponding to Gremlin API's SpatialSpec.</span></span>

## <span data-ttu-id="ea768-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ea768-108">EXAMPLES</span></span>

### <span data-ttu-id="ea768-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ea768-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinSpatialSpec -Path "/abc" -Type String
Path Types
---- -----
/abc {String}
```

## <span data-ttu-id="ea768-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea768-110">PARAMETERS</span></span>

### <span data-ttu-id="ea768-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea768-111">-DefaultProfile</span></span>
<span data-ttu-id="ea768-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ea768-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea768-113">-Path</span><span class="sxs-lookup"><span data-stu-id="ea768-113">-Path</span></span>
<span data-ttu-id="ea768-114">Percorso nel documento JSON da indicizzare.</span><span class="sxs-lookup"><span data-stu-id="ea768-114">Path in JSON document to index.</span></span>

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

### <span data-ttu-id="ea768-115">-Type</span><span class="sxs-lookup"><span data-stu-id="ea768-115">-Type</span></span>
<span data-ttu-id="ea768-116">Matrice di stringhe con valori accettabili: Point, LineString, Poligono, Multipolygon.</span><span class="sxs-lookup"><span data-stu-id="ea768-116">Array of strings with acceptable values: Point, LineString, Polygon, MultiPolygon.</span></span>
<span data-ttu-id="ea768-117">Rappresentare i percorsi del tipo nello stato spaziale.</span><span class="sxs-lookup"><span data-stu-id="ea768-117">Represent's paths spatial type.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea768-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea768-118">CommonParameters</span></span>
<span data-ttu-id="ea768-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea768-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea768-120">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ea768-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea768-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="ea768-121">INPUTS</span></span>

### <span data-ttu-id="ea768-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ea768-122">None</span></span>

## <span data-ttu-id="ea768-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ea768-123">OUTPUTS</span></span>

### <span data-ttu-id="ea768-124">Microsoft.Azure.Commands.BulsDB.Models.PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="ea768-124">Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec</span></span>

## <span data-ttu-id="ea768-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="ea768-125">NOTES</span></span>

## <span data-ttu-id="ea768-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ea768-126">RELATED LINKS</span></span>
