---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlincludedpathindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPathIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPathIndex.md
ms.openlocfilehash: f6bd378ac39c0e00975616b08d3bb9c14358d5d0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209843"
---
# <span data-ttu-id="da658-101">New-AzCosmosDBSqlIncludedPathIndex</span><span class="sxs-lookup"><span data-stu-id="da658-101">New-AzCosmosDBSqlIncludedPathIndex</span></span>

## <span data-ttu-id="da658-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da658-102">SYNOPSIS</span></span>
<span data-ttu-id="da658-103">Crea un nuovo oggetto di tipo PSIndexes.</span><span class="sxs-lookup"><span data-stu-id="da658-103">Creates a new object of type PSIndexes.</span></span> <span data-ttu-id="da658-104">Può essere passato come valore di parametro per Set-AzCosmosDBSqlIncludedPath.</span><span class="sxs-lookup"><span data-stu-id="da658-104">It can be passed as a parameter value for Set-AzCosmosDBSqlIncludedPath.</span></span>

## <span data-ttu-id="da658-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="da658-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlIncludedPathIndex -DataType <String> [-Precision <Int32>] -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da658-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="da658-106">DESCRIPTION</span></span>
<span data-ttu-id="da658-107">Oggetto corrispondente agli indici di IncludedPath dell'API Sql.</span><span class="sxs-lookup"><span data-stu-id="da658-107">Object corresponding to Sql API's IncludedPath's Indexes.</span></span>

## <span data-ttu-id="da658-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="da658-108">EXAMPLES</span></span>

### <span data-ttu-id="da658-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="da658-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
DataType Precision Kind
-------- --------- ----
String          -1 Hash
```

## <span data-ttu-id="da658-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da658-110">PARAMETERS</span></span>

### <span data-ttu-id="da658-111">-DataType</span><span class="sxs-lookup"><span data-stu-id="da658-111">-DataType</span></span>
<span data-ttu-id="da658-112">Tipo di dati per il quale viene applicato il comportamento di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="da658-112">Datatype for which the indexing behavior is applied to.</span></span>
<span data-ttu-id="da658-113">I valori possibili includono: 'Stringa', 'Numero', 'Punto', 'Poligono', 'LineString', 'MultiPolygon'</span><span class="sxs-lookup"><span data-stu-id="da658-113">Possible values include: 'String', 'Number', 'Point', 'Polygon', 'LineString', 'MultiPolygon'</span></span>

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

### <span data-ttu-id="da658-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da658-114">-DefaultProfile</span></span>
<span data-ttu-id="da658-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="da658-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da658-116">-Kind</span><span class="sxs-lookup"><span data-stu-id="da658-116">-Kind</span></span>
<span data-ttu-id="da658-117">Indica il tipo di indice.</span><span class="sxs-lookup"><span data-stu-id="da658-117">Indicates the type of index.</span></span>
<span data-ttu-id="da658-118">I valori possibili includono: 'Hash', 'Range', 'Spatial'</span><span class="sxs-lookup"><span data-stu-id="da658-118">Possible values include: 'Hash', 'Range', 'Spatial'</span></span>

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

### <span data-ttu-id="da658-119">-Precisione</span><span class="sxs-lookup"><span data-stu-id="da658-119">-Precision</span></span>
<span data-ttu-id="da658-120">Precisione dell'indice.</span><span class="sxs-lookup"><span data-stu-id="da658-120">The precision of the index.</span></span>
<span data-ttu-id="da658-121">-1 è la precisione massima.</span><span class="sxs-lookup"><span data-stu-id="da658-121">-1 is maximum precision.</span></span>

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

### <span data-ttu-id="da658-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da658-122">CommonParameters</span></span>
<span data-ttu-id="da658-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da658-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da658-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="da658-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da658-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="da658-125">INPUTS</span></span>

### <span data-ttu-id="da658-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="da658-126">None</span></span>

## <span data-ttu-id="da658-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="da658-127">OUTPUTS</span></span>

### <span data-ttu-id="da658-128">Microsoft.Azure.Commands.EnterpriseDb.Models.PSIndexes</span><span class="sxs-lookup"><span data-stu-id="da658-128">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes</span></span>

## <span data-ttu-id="da658-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="da658-129">NOTES</span></span>

## <span data-ttu-id="da658-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="da658-130">RELATED LINKS</span></span>
