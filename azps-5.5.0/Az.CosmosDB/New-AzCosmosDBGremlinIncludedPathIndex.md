---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinincludedpathindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPathIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPathIndex.md
ms.openlocfilehash: 5d85baaa308b3a0c58f09f40797c3bb2dca4fabe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196807"
---
# <span data-ttu-id="d37d3-101">New-AzCosmosDBGremlinIncludedPathIndex</span><span class="sxs-lookup"><span data-stu-id="d37d3-101">New-AzCosmosDBGremlinIncludedPathIndex</span></span>

## <span data-ttu-id="d37d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d37d3-102">SYNOPSIS</span></span>
<span data-ttu-id="d37d3-103">Crea un nuovo oggetto di tipo PSIndexes.</span><span class="sxs-lookup"><span data-stu-id="d37d3-103">Creates a new object of type PSIndexes.</span></span> <span data-ttu-id="d37d3-104">Può essere passato come valore di parametro per Set-AzCosmosDBGremlinIncludedPath.</span><span class="sxs-lookup"><span data-stu-id="d37d3-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinIncludedPath.</span></span>

## <span data-ttu-id="d37d3-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d37d3-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIncludedPathIndex -DataType <String> [-Precision <Int32>] -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d37d3-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d37d3-106">DESCRIPTION</span></span>
<span data-ttu-id="d37d3-107">Oggetto corrispondente agli indici di IncludedPath dell'API Di Gremlin.</span><span class="sxs-lookup"><span data-stu-id="d37d3-107">Object corresponding to Gremlin API's IncludedPath's Indexes.</span></span>

## <span data-ttu-id="d37d3-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d37d3-108">EXAMPLES</span></span>

### <span data-ttu-id="d37d3-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d37d3-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash

DataType Precision Kind
-------- --------- ----
String          -1 Hash
```

## <span data-ttu-id="d37d3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d37d3-110">PARAMETERS</span></span>

### <span data-ttu-id="d37d3-111">-DataType</span><span class="sxs-lookup"><span data-stu-id="d37d3-111">-DataType</span></span>
<span data-ttu-id="d37d3-112">Tipo di dati per il quale viene applicato il comportamento di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="d37d3-112">Datatype for which the indexing behavior is applied to.</span></span>
<span data-ttu-id="d37d3-113">I valori possibili includono: 'Stringa', 'Numero', 'Punto', 'Poligono', 'LineString', 'MultiPolygon'</span><span class="sxs-lookup"><span data-stu-id="d37d3-113">Possible values include: 'String', 'Number', 'Point', 'Polygon', 'LineString', 'MultiPolygon'</span></span>

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

### <span data-ttu-id="d37d3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d37d3-114">-DefaultProfile</span></span>
<span data-ttu-id="d37d3-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d37d3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d37d3-116">-Kind</span><span class="sxs-lookup"><span data-stu-id="d37d3-116">-Kind</span></span>
<span data-ttu-id="d37d3-117">Indica il tipo di indice.</span><span class="sxs-lookup"><span data-stu-id="d37d3-117">Indicates the type of index.</span></span>
<span data-ttu-id="d37d3-118">I valori possibili includono: 'Hash', 'Range', 'Spatial'</span><span class="sxs-lookup"><span data-stu-id="d37d3-118">Possible values include: 'Hash', 'Range', 'Spatial'</span></span>

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

### <span data-ttu-id="d37d3-119">-Precisione</span><span class="sxs-lookup"><span data-stu-id="d37d3-119">-Precision</span></span>
<span data-ttu-id="d37d3-120">Precisione dell'indice.</span><span class="sxs-lookup"><span data-stu-id="d37d3-120">The precision of the index.</span></span>
<span data-ttu-id="d37d3-121">-1 è la precisione massima.</span><span class="sxs-lookup"><span data-stu-id="d37d3-121">-1 is maximum precision.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d37d3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d37d3-122">CommonParameters</span></span>
<span data-ttu-id="d37d3-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d37d3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d37d3-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d37d3-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d37d3-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="d37d3-125">INPUTS</span></span>

### <span data-ttu-id="d37d3-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d37d3-126">None</span></span>

## <span data-ttu-id="d37d3-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d37d3-127">OUTPUTS</span></span>

### <span data-ttu-id="d37d3-128">Microsoft.Azure.Commands.EnterpriseDb.Models.PSIndexes</span><span class="sxs-lookup"><span data-stu-id="d37d3-128">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes</span></span>

## <span data-ttu-id="d37d3-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="d37d3-129">NOTES</span></span>

## <span data-ttu-id="d37d3-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d37d3-130">RELATED LINKS</span></span>
