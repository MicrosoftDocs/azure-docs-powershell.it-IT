---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlspatialspec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlSpatialSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlSpatialSpec.md
ms.openlocfilehash: 0d205c7de9f4515c153f3662d3fededee48793eb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365158"
---
# <span data-ttu-id="8dfc3-101">New-AzCosmosDBSqlSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="8dfc3-101">New-AzCosmosDBSqlSpatialSpec</span></span>

## <span data-ttu-id="8dfc3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8dfc3-102">SYNOPSIS</span></span>
<span data-ttu-id="8dfc3-103">Crea un nuovo oggetto di tipo PSSpatialSpec.</span><span class="sxs-lookup"><span data-stu-id="8dfc3-103">Creates a new object of type PSSpatialSpec.</span></span> <span data-ttu-id="8dfc3-104">Può essere passato come valore di parametro per set-AzCosmosDBSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="8dfc3-104">It can be passed as a parameter value for Set-AzCosmosDBSqlIndexingPolicy.</span></span>

## <span data-ttu-id="8dfc3-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8dfc3-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlSpatialSpec -Path <String> -Type <String[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8dfc3-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8dfc3-106">DESCRIPTION</span></span>
<span data-ttu-id="8dfc3-107">Crea un oggetto corrispondente alla SpatialSpec dell'API SQL.</span><span class="sxs-lookup"><span data-stu-id="8dfc3-107">Creates Object corresponding to Sql API's SpatialSpec.</span></span>

## <span data-ttu-id="8dfc3-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8dfc3-108">EXAMPLES</span></span>

### <span data-ttu-id="8dfc3-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8dfc3-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlSpatialSpec -Path "/abc" -Type String
Path Types
---- -----
/abc {String}
```

## <span data-ttu-id="8dfc3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8dfc3-110">PARAMETERS</span></span>

### <span data-ttu-id="8dfc3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dfc3-111">-DefaultProfile</span></span>
<span data-ttu-id="8dfc3-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8dfc3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8dfc3-113">-Path</span><span class="sxs-lookup"><span data-stu-id="8dfc3-113">-Path</span></span>
<span data-ttu-id="8dfc3-114">Percorso nel documento JSON da indicizzare.</span><span class="sxs-lookup"><span data-stu-id="8dfc3-114">Path in JSON document to index.</span></span>

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

### <span data-ttu-id="8dfc3-115">-Digitare</span><span class="sxs-lookup"><span data-stu-id="8dfc3-115">-Type</span></span>
<span data-ttu-id="8dfc3-116">Matrice di stringhe con valori accettabili: Point, LineString, Polygon e MultiPolygon.</span><span class="sxs-lookup"><span data-stu-id="8dfc3-116">Array of strings with acceptable values: Point, LineString, Polygon, MultiPolygon.</span></span>
<span data-ttu-id="8dfc3-117">Rappresentare i percorsi del tipo spaziale.</span><span class="sxs-lookup"><span data-stu-id="8dfc3-117">Represent's paths spatial type.</span></span>

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

### <span data-ttu-id="8dfc3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dfc3-118">CommonParameters</span></span>
<span data-ttu-id="8dfc3-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dfc3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dfc3-120">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8dfc3-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dfc3-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8dfc3-121">INPUTS</span></span>

### <span data-ttu-id="8dfc3-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8dfc3-122">None</span></span>

## <span data-ttu-id="8dfc3-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8dfc3-123">OUTPUTS</span></span>

### <span data-ttu-id="8dfc3-124">Microsoft. Azure. Commands. CosmosDB. Models. PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="8dfc3-124">Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec</span></span>

## <span data-ttu-id="8dfc3-125">Note</span><span class="sxs-lookup"><span data-stu-id="8dfc3-125">NOTES</span></span>

## <span data-ttu-id="8dfc3-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8dfc3-126">RELATED LINKS</span></span>
