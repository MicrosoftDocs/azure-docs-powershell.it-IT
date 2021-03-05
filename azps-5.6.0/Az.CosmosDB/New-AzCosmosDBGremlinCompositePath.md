---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlincompositepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinCompositePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinCompositePath.md
ms.openlocfilehash: c88cde11d277a4a2e0473d41f83e1b62e13216bb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007997"
---
# <span data-ttu-id="40ddb-101">New-AzCosmosDBGremlinCompositePath</span><span class="sxs-lookup"><span data-stu-id="40ddb-101">New-AzCosmosDBGremlinCompositePath</span></span>

## <span data-ttu-id="40ddb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40ddb-102">SYNOPSIS</span></span>
<span data-ttu-id="40ddb-103">Crea un nuovo oggetto di tipo PSCompositePath.</span><span class="sxs-lookup"><span data-stu-id="40ddb-103">Creates a new object of type PSCompositePath.</span></span> <span data-ttu-id="40ddb-104">Può essere passato come valore di parametro per Set-AzCosmosDBGremlinGraph.</span><span class="sxs-lookup"><span data-stu-id="40ddb-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="40ddb-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="40ddb-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinCompositePath [-Path <String>] [-Order <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40ddb-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="40ddb-106">DESCRIPTION</span></span>
<span data-ttu-id="40ddb-107">Oggetto corrispondente all'api CompositePath dell'API di Gremlin.</span><span class="sxs-lookup"><span data-stu-id="40ddb-107">Object corresponding to Gremlin API's CompositePath.</span></span>

## <span data-ttu-id="40ddb-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="40ddb-108">EXAMPLES</span></span>

### <span data-ttu-id="40ddb-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="40ddb-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinCompositePath -Path "/abc" -Order Ascending

Path Order
---- -----
/abc Ascending
```

## <span data-ttu-id="40ddb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40ddb-110">PARAMETERS</span></span>

### <span data-ttu-id="40ddb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40ddb-111">-DefaultProfile</span></span>
<span data-ttu-id="40ddb-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="40ddb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40ddb-113">-Ordine</span><span class="sxs-lookup"><span data-stu-id="40ddb-113">-Order</span></span>
<span data-ttu-id="40ddb-114">Ottiene o imposta l'ordinamento per i percorsi compositi.</span><span class="sxs-lookup"><span data-stu-id="40ddb-114">Gets or sets sort order for composite paths.</span></span>
<span data-ttu-id="40ddb-115">I valori possibili includono: 'Crescente', 'Decrescente'</span><span class="sxs-lookup"><span data-stu-id="40ddb-115">Possible values include: 'Ascending', 'Descending'</span></span>

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

### <span data-ttu-id="40ddb-116">-Path</span><span class="sxs-lookup"><span data-stu-id="40ddb-116">-Path</span></span>
<span data-ttu-id="40ddb-117">Percorso per cui si applica il comportamento di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="40ddb-117">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="40ddb-118">I percorsi di indice iniziano in genere con radice e terminano con un carattere jolly (/path/\*)</span><span class="sxs-lookup"><span data-stu-id="40ddb-118">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="40ddb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40ddb-119">CommonParameters</span></span>
<span data-ttu-id="40ddb-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40ddb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40ddb-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="40ddb-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40ddb-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="40ddb-122">INPUTS</span></span>

### <span data-ttu-id="40ddb-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="40ddb-123">None</span></span>

## <span data-ttu-id="40ddb-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="40ddb-124">OUTPUTS</span></span>

### <span data-ttu-id="40ddb-125">Microsoft.Azure.Commands.EnterpriseDb.Models.PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="40ddb-125">Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath</span></span>

## <span data-ttu-id="40ddb-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="40ddb-126">NOTES</span></span>

## <span data-ttu-id="40ddb-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="40ddb-127">RELATED LINKS</span></span>
