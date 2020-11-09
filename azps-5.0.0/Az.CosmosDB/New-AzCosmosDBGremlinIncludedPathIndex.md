---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinincludedpathindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPathIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPathIndex.md
ms.openlocfilehash: 5d85baaa308b3a0c58f09f40797c3bb2dca4fabe
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299329"
---
# <span data-ttu-id="ea0f5-101">New-AzCosmosDBGremlinIncludedPathIndex</span><span class="sxs-lookup"><span data-stu-id="ea0f5-101">New-AzCosmosDBGremlinIncludedPathIndex</span></span>

## <span data-ttu-id="ea0f5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ea0f5-102">SYNOPSIS</span></span>
<span data-ttu-id="ea0f5-103">Crea un nuovo oggetto di tipo PSIndexes.</span><span class="sxs-lookup"><span data-stu-id="ea0f5-103">Creates a new object of type PSIndexes.</span></span> <span data-ttu-id="ea0f5-104">Può essere passato come valore di parametro per set-AzCosmosDBGremlinIncludedPath.</span><span class="sxs-lookup"><span data-stu-id="ea0f5-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinIncludedPath.</span></span>

## <span data-ttu-id="ea0f5-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ea0f5-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIncludedPathIndex -DataType <String> [-Precision <Int32>] -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea0f5-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ea0f5-106">DESCRIPTION</span></span>
<span data-ttu-id="ea0f5-107">Oggetto corrispondente agli indici di IncludedPath's dell'API Gremlin.</span><span class="sxs-lookup"><span data-stu-id="ea0f5-107">Object corresponding to Gremlin API's IncludedPath's Indexes.</span></span>

## <span data-ttu-id="ea0f5-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ea0f5-108">EXAMPLES</span></span>

### <span data-ttu-id="ea0f5-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ea0f5-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash

DataType Precision Kind
-------- --------- ----
String          -1 Hash
```

## <span data-ttu-id="ea0f5-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ea0f5-110">PARAMETERS</span></span>

### <span data-ttu-id="ea0f5-111">-DataType</span><span class="sxs-lookup"><span data-stu-id="ea0f5-111">-DataType</span></span>
<span data-ttu-id="ea0f5-112">Tipo di DataType per cui viene applicato il comportamento di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="ea0f5-112">Datatype for which the indexing behavior is applied to.</span></span>
<span data-ttu-id="ea0f5-113">I valori possibili includono: "stringa", "numero", "punto", "poligono", "LineString", "multipoligono"</span><span class="sxs-lookup"><span data-stu-id="ea0f5-113">Possible values include: 'String', 'Number', 'Point', 'Polygon', 'LineString', 'MultiPolygon'</span></span>

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

### <span data-ttu-id="ea0f5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea0f5-114">-DefaultProfile</span></span>
<span data-ttu-id="ea0f5-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ea0f5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea0f5-116">-Tipo</span><span class="sxs-lookup"><span data-stu-id="ea0f5-116">-Kind</span></span>
<span data-ttu-id="ea0f5-117">Indica il tipo di indice.</span><span class="sxs-lookup"><span data-stu-id="ea0f5-117">Indicates the type of index.</span></span>
<span data-ttu-id="ea0f5-118">I valori possibili includono: "hash", "range", "Spatial"</span><span class="sxs-lookup"><span data-stu-id="ea0f5-118">Possible values include: 'Hash', 'Range', 'Spatial'</span></span>

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

### <span data-ttu-id="ea0f5-119">-Precisione</span><span class="sxs-lookup"><span data-stu-id="ea0f5-119">-Precision</span></span>
<span data-ttu-id="ea0f5-120">La precisione dell'indice.</span><span class="sxs-lookup"><span data-stu-id="ea0f5-120">The precision of the index.</span></span>
<span data-ttu-id="ea0f5-121">-1 è la massima precisione.</span><span class="sxs-lookup"><span data-stu-id="ea0f5-121">-1 is maximum precision.</span></span>

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

### <span data-ttu-id="ea0f5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea0f5-122">CommonParameters</span></span>
<span data-ttu-id="ea0f5-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea0f5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea0f5-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea0f5-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea0f5-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ea0f5-125">INPUTS</span></span>

### <span data-ttu-id="ea0f5-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ea0f5-126">None</span></span>

## <span data-ttu-id="ea0f5-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ea0f5-127">OUTPUTS</span></span>

### <span data-ttu-id="ea0f5-128">Microsoft. Azure. Commands. CosmosDB. Models. PSIndexes</span><span class="sxs-lookup"><span data-stu-id="ea0f5-128">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes</span></span>

## <span data-ttu-id="ea0f5-129">Note</span><span class="sxs-lookup"><span data-stu-id="ea0f5-129">NOTES</span></span>

## <span data-ttu-id="ea0f5-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ea0f5-130">RELATED LINKS</span></span>
