---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinincludedpath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPath.md
ms.openlocfilehash: 779589d3789e9b6baa1864f22366fb40b1c41c3c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033204"
---
# <span data-ttu-id="b3b47-101">New-AzCosmosDBGremlinIncludedPath</span><span class="sxs-lookup"><span data-stu-id="b3b47-101">New-AzCosmosDBGremlinIncludedPath</span></span>

## <span data-ttu-id="b3b47-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b3b47-102">SYNOPSIS</span></span>
<span data-ttu-id="b3b47-103">Crea un nuovo oggetto di tipo PSIncludedPath.</span><span class="sxs-lookup"><span data-stu-id="b3b47-103">Creates a new object of type PSIncludedPath.</span></span> <span data-ttu-id="b3b47-104">Può essere passato come valore di parametro per set-AzCosmosDBGremlinGraph.</span><span class="sxs-lookup"><span data-stu-id="b3b47-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="b3b47-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b3b47-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIncludedPath [-Path <String>] [-Index <PSIndexes[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3b47-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3b47-106">DESCRIPTION</span></span>
<span data-ttu-id="b3b47-107">Oggetto corrispondente alla IncludedPath dell'API Gremlin.</span><span class="sxs-lookup"><span data-stu-id="b3b47-107">Object corresponding to Gremlin API's IncludedPath.</span></span>

## <span data-ttu-id="b3b47-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b3b47-108">EXAMPLES</span></span>

### <span data-ttu-id="b3b47-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b3b47-109">Example 1</span></span>
```powershell
PS C:\> $index1 = New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash
New-AzCosmosDBGremlinIncludedPath -Path "/*" -Index $index1
Path Indexes
---- -------
/*   {Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes}
```

## <span data-ttu-id="b3b47-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b3b47-110">PARAMETERS</span></span>

### <span data-ttu-id="b3b47-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3b47-111">-DefaultProfile</span></span>
<span data-ttu-id="b3b47-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b3b47-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3b47-113">-Index</span><span class="sxs-lookup"><span data-stu-id="b3b47-113">-Index</span></span>
<span data-ttu-id="b3b47-114">Elenco di indici per questo percorso</span><span class="sxs-lookup"><span data-stu-id="b3b47-114">List of indexes for this path</span></span>

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

### <span data-ttu-id="b3b47-115">-Path</span><span class="sxs-lookup"><span data-stu-id="b3b47-115">-Path</span></span>
<span data-ttu-id="b3b47-116">Percorso a cui si applica il comportamento di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="b3b47-116">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="b3b47-117">I percorsi di indice in genere iniziano con radice e terminano con caratteri jolly (/path/\*)</span><span class="sxs-lookup"><span data-stu-id="b3b47-117">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="b3b47-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3b47-118">CommonParameters</span></span>
<span data-ttu-id="b3b47-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3b47-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3b47-120">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3b47-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3b47-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b3b47-121">INPUTS</span></span>

### <span data-ttu-id="b3b47-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b3b47-122">None</span></span>

## <span data-ttu-id="b3b47-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b3b47-123">OUTPUTS</span></span>

### <span data-ttu-id="b3b47-124">Microsoft. Azure. Commands. CosmosDB. Models. PSIncludedPath</span><span class="sxs-lookup"><span data-stu-id="b3b47-124">Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath</span></span>

## <span data-ttu-id="b3b47-125">Note</span><span class="sxs-lookup"><span data-stu-id="b3b47-125">NOTES</span></span>

## <span data-ttu-id="b3b47-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b3b47-126">RELATED LINKS</span></span>
