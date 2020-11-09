---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinspatialspec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinSpatialSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinSpatialSpec.md
ms.openlocfilehash: 6cdb0d9732c64f26e2ba840623ae6f6df06602b9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299311"
---
# <span data-ttu-id="e3439-101">New-AzCosmosDBGremlinSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="e3439-101">New-AzCosmosDBGremlinSpatialSpec</span></span>

## <span data-ttu-id="e3439-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e3439-102">SYNOPSIS</span></span>
<span data-ttu-id="e3439-103">Crea un nuovo oggetto di tipo PSSpatialSpec.</span><span class="sxs-lookup"><span data-stu-id="e3439-103">Creates a new object of type PSSpatialSpec.</span></span> <span data-ttu-id="e3439-104">Può essere passato come valore di parametro per set-AzCosmosDBGremlinIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="e3439-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinIndexingPolicy.</span></span>

## <span data-ttu-id="e3439-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3439-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinSpatialSpec -Path <String> -Type <String[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e3439-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3439-106">DESCRIPTION</span></span>
<span data-ttu-id="e3439-107">Crea un oggetto corrispondente alla SpatialSpec dell'API Gremlin.</span><span class="sxs-lookup"><span data-stu-id="e3439-107">Creates Object corresponding to Gremlin API's SpatialSpec.</span></span>

## <span data-ttu-id="e3439-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3439-108">EXAMPLES</span></span>

### <span data-ttu-id="e3439-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e3439-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinSpatialSpec -Path "/abc" -Type String
Path Types
---- -----
/abc {String}
```

## <span data-ttu-id="e3439-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e3439-110">PARAMETERS</span></span>

### <span data-ttu-id="e3439-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3439-111">-DefaultProfile</span></span>
<span data-ttu-id="e3439-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e3439-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3439-113">-Path</span><span class="sxs-lookup"><span data-stu-id="e3439-113">-Path</span></span>
<span data-ttu-id="e3439-114">Percorso nel documento JSON da indicizzare.</span><span class="sxs-lookup"><span data-stu-id="e3439-114">Path in JSON document to index.</span></span>

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

### <span data-ttu-id="e3439-115">-Digitare</span><span class="sxs-lookup"><span data-stu-id="e3439-115">-Type</span></span>
<span data-ttu-id="e3439-116">Matrice di stringhe con valori accettabili: Point, LineString, Polygon e MultiPolygon.</span><span class="sxs-lookup"><span data-stu-id="e3439-116">Array of strings with acceptable values: Point, LineString, Polygon, MultiPolygon.</span></span>
<span data-ttu-id="e3439-117">Rappresentare i percorsi del tipo spaziale.</span><span class="sxs-lookup"><span data-stu-id="e3439-117">Represent's paths spatial type.</span></span>

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

### <span data-ttu-id="e3439-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3439-118">CommonParameters</span></span>
<span data-ttu-id="e3439-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3439-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3439-120">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3439-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3439-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e3439-121">INPUTS</span></span>

### <span data-ttu-id="e3439-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e3439-122">None</span></span>

## <span data-ttu-id="e3439-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3439-123">OUTPUTS</span></span>

### <span data-ttu-id="e3439-124">Microsoft. Azure. Commands. CosmosDB. Models. PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="e3439-124">Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec</span></span>

## <span data-ttu-id="e3439-125">Note</span><span class="sxs-lookup"><span data-stu-id="e3439-125">NOTES</span></span>

## <span data-ttu-id="e3439-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3439-126">RELATED LINKS</span></span>
