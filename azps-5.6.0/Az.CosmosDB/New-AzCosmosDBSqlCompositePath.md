---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqlcompositepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlCompositePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlCompositePath.md
ms.openlocfilehash: de91a7bb3fc1f4321cf344aa975c14c3976dfdbf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978702"
---
# <span data-ttu-id="928f1-101">New-AzCosmosDBSqlCompositePath</span><span class="sxs-lookup"><span data-stu-id="928f1-101">New-AzCosmosDBSqlCompositePath</span></span>

## <span data-ttu-id="928f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="928f1-102">SYNOPSIS</span></span>
<span data-ttu-id="928f1-103">Crea un nuovo oggetto di tipo PSCompositePath.</span><span class="sxs-lookup"><span data-stu-id="928f1-103">Creates a new object of type PSCompositePath.</span></span> <span data-ttu-id="928f1-104">Può essere passato come valore di parametro per Set-AzCosmosDBSqlContainer.</span><span class="sxs-lookup"><span data-stu-id="928f1-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="928f1-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="928f1-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlCompositePath [-Path <String>] [-Order <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="928f1-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="928f1-106">DESCRIPTION</span></span>
<span data-ttu-id="928f1-107">Oggetto che corrisponde all'api Sql CompositePath.</span><span class="sxs-lookup"><span data-stu-id="928f1-107">Object corresponding to Sql API's CompositePath.</span></span>

## <span data-ttu-id="928f1-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="928f1-108">EXAMPLES</span></span>

### <span data-ttu-id="928f1-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="928f1-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlCompositePath -Path "/abc" -Order Ascending

Path Order
---- -----
/abc Ascending
```

## <span data-ttu-id="928f1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="928f1-110">PARAMETERS</span></span>

### <span data-ttu-id="928f1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="928f1-111">-DefaultProfile</span></span>
<span data-ttu-id="928f1-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="928f1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="928f1-113">-Ordine</span><span class="sxs-lookup"><span data-stu-id="928f1-113">-Order</span></span>
<span data-ttu-id="928f1-114">Ottiene o imposta l'ordinamento per i percorsi compositi.</span><span class="sxs-lookup"><span data-stu-id="928f1-114">Gets or sets sort order for composite paths.</span></span>
<span data-ttu-id="928f1-115">I valori possibili includono: 'Crescente', 'Decrescente'</span><span class="sxs-lookup"><span data-stu-id="928f1-115">Possible values include: 'Ascending', 'Descending'</span></span>

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

### <span data-ttu-id="928f1-116">-Path</span><span class="sxs-lookup"><span data-stu-id="928f1-116">-Path</span></span>
<span data-ttu-id="928f1-117">Percorso per cui si applica il comportamento di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="928f1-117">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="928f1-118">I percorsi di indice iniziano in genere con radice e terminano con un carattere jolly (/path/\*)</span><span class="sxs-lookup"><span data-stu-id="928f1-118">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="928f1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="928f1-119">CommonParameters</span></span>
<span data-ttu-id="928f1-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="928f1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="928f1-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="928f1-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="928f1-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="928f1-122">INPUTS</span></span>

### <span data-ttu-id="928f1-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="928f1-123">None</span></span>

## <span data-ttu-id="928f1-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="928f1-124">OUTPUTS</span></span>

### <span data-ttu-id="928f1-125">Microsoft.Azure.Commands.EnterpriseDb.Models.PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="928f1-125">Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath</span></span>

## <span data-ttu-id="928f1-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="928f1-126">NOTES</span></span>

## <span data-ttu-id="928f1-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="928f1-127">RELATED LINKS</span></span>
