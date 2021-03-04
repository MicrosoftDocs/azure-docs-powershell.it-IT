---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlinincludedpath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPath.md
ms.openlocfilehash: c3022ea8f2ddbfbf0fc2a51bfd63706c4a8ea884
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957454"
---
# <span data-ttu-id="05236-101">New-AzCosmosDBGremlinIncludedPath</span><span class="sxs-lookup"><span data-stu-id="05236-101">New-AzCosmosDBGremlinIncludedPath</span></span>

## <span data-ttu-id="05236-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05236-102">SYNOPSIS</span></span>
<span data-ttu-id="05236-103">Crea un nuovo oggetto di tipo PSIncludedPath.</span><span class="sxs-lookup"><span data-stu-id="05236-103">Creates a new object of type PSIncludedPath.</span></span> <span data-ttu-id="05236-104">Può essere passato come valore di parametro per Set-AzCosmosDBGremlinGraph.</span><span class="sxs-lookup"><span data-stu-id="05236-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="05236-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="05236-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIncludedPath [-Path <String>] [-Index <PSIndexes[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05236-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="05236-106">DESCRIPTION</span></span>
<span data-ttu-id="05236-107">Oggetto corrispondente all'API Incluso dell'API di Gremlin.</span><span class="sxs-lookup"><span data-stu-id="05236-107">Object corresponding to Gremlin API's IncludedPath.</span></span>

## <span data-ttu-id="05236-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="05236-108">EXAMPLES</span></span>

### <span data-ttu-id="05236-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="05236-109">Example 1</span></span>
```powershell
PS C:\> $index1 = New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash
New-AzCosmosDBGremlinIncludedPath -Path "/*" -Index $index1
Path Indexes
---- -------
/*   {Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes}
```

## <span data-ttu-id="05236-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05236-110">PARAMETERS</span></span>

### <span data-ttu-id="05236-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05236-111">-DefaultProfile</span></span>
<span data-ttu-id="05236-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="05236-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05236-113">-Index</span><span class="sxs-lookup"><span data-stu-id="05236-113">-Index</span></span>
<span data-ttu-id="05236-114">Elenco di indici per questo percorso</span><span class="sxs-lookup"><span data-stu-id="05236-114">List of indexes for this path</span></span>

```yaml
Type: PSIndexes[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05236-115">-Path</span><span class="sxs-lookup"><span data-stu-id="05236-115">-Path</span></span>
<span data-ttu-id="05236-116">Percorso per cui si applica il comportamento di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="05236-116">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="05236-117">I percorsi di indice iniziano in genere con radice e terminano con un carattere jolly (/path/\*)</span><span class="sxs-lookup"><span data-stu-id="05236-117">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="05236-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05236-118">CommonParameters</span></span>
<span data-ttu-id="05236-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05236-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05236-120">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="05236-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05236-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="05236-121">INPUTS</span></span>

### <span data-ttu-id="05236-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="05236-122">None</span></span>

## <span data-ttu-id="05236-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="05236-123">OUTPUTS</span></span>

### <span data-ttu-id="05236-124">Microsoft.Azure.Commands.EnterpriseDb.Models.PSIncludedPath</span><span class="sxs-lookup"><span data-stu-id="05236-124">Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath</span></span>

## <span data-ttu-id="05236-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="05236-125">NOTES</span></span>

## <span data-ttu-id="05236-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="05236-126">RELATED LINKS</span></span>
