---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlcompositepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlCompositePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlCompositePath.md
ms.openlocfilehash: ff78ad82c89b774f034fe6f1d4499db7868d43c7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181310"
---
# <span data-ttu-id="c25b5-101">New-AzCosmosDBSqlCompositePath</span><span class="sxs-lookup"><span data-stu-id="c25b5-101">New-AzCosmosDBSqlCompositePath</span></span>

## <span data-ttu-id="c25b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c25b5-102">SYNOPSIS</span></span>
<span data-ttu-id="c25b5-103">Crea un nuovo oggetto di tipo PSCompositePath.</span><span class="sxs-lookup"><span data-stu-id="c25b5-103">Creates a new object of type PSCompositePath.</span></span> <span data-ttu-id="c25b5-104">Può essere passato come valore di parametro per Set-AzCosmosDBSqlContainer.</span><span class="sxs-lookup"><span data-stu-id="c25b5-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="c25b5-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c25b5-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlCompositePath [-Path <String>] [-Order <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c25b5-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c25b5-106">DESCRIPTION</span></span>
<span data-ttu-id="c25b5-107">Oggetto corrispondente al compositePath dell'API Sql.</span><span class="sxs-lookup"><span data-stu-id="c25b5-107">Object corresponding to Sql API's CompositePath.</span></span>

## <span data-ttu-id="c25b5-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c25b5-108">EXAMPLES</span></span>

### <span data-ttu-id="c25b5-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c25b5-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlCompositePath -Path "/abc" -Order Ascending

Path Order
---- -----
/abc Ascending
```

## <span data-ttu-id="c25b5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c25b5-110">PARAMETERS</span></span>

### <span data-ttu-id="c25b5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c25b5-111">-DefaultProfile</span></span>
<span data-ttu-id="c25b5-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c25b5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c25b5-113">-Ordine</span><span class="sxs-lookup"><span data-stu-id="c25b5-113">-Order</span></span>
<span data-ttu-id="c25b5-114">Ottiene o imposta l'ordinamento per i percorsi compositi.</span><span class="sxs-lookup"><span data-stu-id="c25b5-114">Gets or sets sort order for composite paths.</span></span>
<span data-ttu-id="c25b5-115">I valori possibili includono: 'Crescente', 'Decrescente'</span><span class="sxs-lookup"><span data-stu-id="c25b5-115">Possible values include: 'Ascending', 'Descending'</span></span>

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

### <span data-ttu-id="c25b5-116">-Path</span><span class="sxs-lookup"><span data-stu-id="c25b5-116">-Path</span></span>
<span data-ttu-id="c25b5-117">Percorso per cui si applica il comportamento di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="c25b5-117">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="c25b5-118">I percorsi di indice iniziano in genere con radice e terminano con un carattere jolly (/path/\*)</span><span class="sxs-lookup"><span data-stu-id="c25b5-118">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="c25b5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c25b5-119">CommonParameters</span></span>
<span data-ttu-id="c25b5-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c25b5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c25b5-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c25b5-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c25b5-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="c25b5-122">INPUTS</span></span>

### <span data-ttu-id="c25b5-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c25b5-123">None</span></span>

## <span data-ttu-id="c25b5-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c25b5-124">OUTPUTS</span></span>

### <span data-ttu-id="c25b5-125">Microsoft.Azure.Commands.EnterpriseDb.Models.PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="c25b5-125">Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath</span></span>

## <span data-ttu-id="c25b5-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="c25b5-126">NOTES</span></span>

## <span data-ttu-id="c25b5-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c25b5-127">RELATED LINKS</span></span>
