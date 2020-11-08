---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlincompositepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinCompositePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinCompositePath.md
ms.openlocfilehash: 612f4623c7944c3c3d930ece44d4c2ae938e1a68
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018870"
---
# <span data-ttu-id="fb525-101">New-AzCosmosDBGremlinCompositePath</span><span class="sxs-lookup"><span data-stu-id="fb525-101">New-AzCosmosDBGremlinCompositePath</span></span>

## <span data-ttu-id="fb525-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fb525-102">SYNOPSIS</span></span>
<span data-ttu-id="fb525-103">Crea un nuovo oggetto di tipo PSCompositePath.</span><span class="sxs-lookup"><span data-stu-id="fb525-103">Creates a new object of type PSCompositePath.</span></span> <span data-ttu-id="fb525-104">Può essere passato come valore di parametro per set-AzCosmosDBGremlinGraph.</span><span class="sxs-lookup"><span data-stu-id="fb525-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="fb525-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fb525-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinCompositePath [-Path <String>] [-Order <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb525-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fb525-106">DESCRIPTION</span></span>
<span data-ttu-id="fb525-107">Oggetto corrispondente alla CompositePath dell'API Gremlin.</span><span class="sxs-lookup"><span data-stu-id="fb525-107">Object corresponding to Gremlin API's CompositePath.</span></span>

## <span data-ttu-id="fb525-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fb525-108">EXAMPLES</span></span>

### <span data-ttu-id="fb525-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fb525-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinCompositePath -Path "/abc" -Order Ascending

Path Order
---- -----
/abc Ascending
```

## <span data-ttu-id="fb525-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fb525-110">PARAMETERS</span></span>

### <span data-ttu-id="fb525-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb525-111">-DefaultProfile</span></span>
<span data-ttu-id="fb525-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fb525-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb525-113">-Ordine</span><span class="sxs-lookup"><span data-stu-id="fb525-113">-Order</span></span>
<span data-ttu-id="fb525-114">Ottiene o imposta l'ordine di ordinamento per i percorsi compositi.</span><span class="sxs-lookup"><span data-stu-id="fb525-114">Gets or sets sort order for composite paths.</span></span>
<span data-ttu-id="fb525-115">I valori possibili includono: "crescente", "decrescente"</span><span class="sxs-lookup"><span data-stu-id="fb525-115">Possible values include: 'Ascending', 'Descending'</span></span>

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

### <span data-ttu-id="fb525-116">-Path</span><span class="sxs-lookup"><span data-stu-id="fb525-116">-Path</span></span>
<span data-ttu-id="fb525-117">Percorso a cui si applica il comportamento di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="fb525-117">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="fb525-118">I percorsi di indice in genere iniziano con radice e terminano con caratteri jolly (/path/\*)</span><span class="sxs-lookup"><span data-stu-id="fb525-118">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="fb525-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb525-119">CommonParameters</span></span>
<span data-ttu-id="fb525-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb525-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb525-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb525-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb525-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fb525-122">INPUTS</span></span>

### <span data-ttu-id="fb525-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="fb525-123">None</span></span>

## <span data-ttu-id="fb525-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fb525-124">OUTPUTS</span></span>

### <span data-ttu-id="fb525-125">Microsoft. Azure. Commands. CosmosDB. Models. PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="fb525-125">Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath</span></span>

## <span data-ttu-id="fb525-126">Note</span><span class="sxs-lookup"><span data-stu-id="fb525-126">NOTES</span></span>

## <span data-ttu-id="fb525-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fb525-127">RELATED LINKS</span></span>
