---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlcompositepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlCompositePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlCompositePath.md
ms.openlocfilehash: ff78ad82c89b774f034fe6f1d4499db7868d43c7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021602"
---
# <span data-ttu-id="18a02-101">New-AzCosmosDBSqlCompositePath</span><span class="sxs-lookup"><span data-stu-id="18a02-101">New-AzCosmosDBSqlCompositePath</span></span>

## <span data-ttu-id="18a02-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="18a02-102">SYNOPSIS</span></span>
<span data-ttu-id="18a02-103">Crea un nuovo oggetto di tipo PSCompositePath.</span><span class="sxs-lookup"><span data-stu-id="18a02-103">Creates a new object of type PSCompositePath.</span></span> <span data-ttu-id="18a02-104">Può essere passato come valore di parametro per set-AzCosmosDBSqlContainer.</span><span class="sxs-lookup"><span data-stu-id="18a02-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="18a02-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="18a02-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlCompositePath [-Path <String>] [-Order <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="18a02-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18a02-106">DESCRIPTION</span></span>
<span data-ttu-id="18a02-107">Oggetto che corrisponde al CompositePath dell'API SQL.</span><span class="sxs-lookup"><span data-stu-id="18a02-107">Object corresponding to Sql API's CompositePath.</span></span>

## <span data-ttu-id="18a02-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="18a02-108">EXAMPLES</span></span>

### <span data-ttu-id="18a02-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="18a02-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlCompositePath -Path "/abc" -Order Ascending

Path Order
---- -----
/abc Ascending
```

## <span data-ttu-id="18a02-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="18a02-110">PARAMETERS</span></span>

### <span data-ttu-id="18a02-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18a02-111">-DefaultProfile</span></span>
<span data-ttu-id="18a02-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="18a02-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18a02-113">-Ordine</span><span class="sxs-lookup"><span data-stu-id="18a02-113">-Order</span></span>
<span data-ttu-id="18a02-114">Ottiene o imposta l'ordine di ordinamento per i percorsi compositi.</span><span class="sxs-lookup"><span data-stu-id="18a02-114">Gets or sets sort order for composite paths.</span></span>
<span data-ttu-id="18a02-115">I valori possibili includono: "crescente", "decrescente"</span><span class="sxs-lookup"><span data-stu-id="18a02-115">Possible values include: 'Ascending', 'Descending'</span></span>

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

### <span data-ttu-id="18a02-116">-Path</span><span class="sxs-lookup"><span data-stu-id="18a02-116">-Path</span></span>
<span data-ttu-id="18a02-117">Percorso a cui si applica il comportamento di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="18a02-117">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="18a02-118">I percorsi di indice in genere iniziano con radice e terminano con caratteri jolly (/path/\*)</span><span class="sxs-lookup"><span data-stu-id="18a02-118">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="18a02-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18a02-119">CommonParameters</span></span>
<span data-ttu-id="18a02-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18a02-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18a02-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="18a02-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18a02-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="18a02-122">INPUTS</span></span>

### <span data-ttu-id="18a02-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="18a02-123">None</span></span>

## <span data-ttu-id="18a02-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="18a02-124">OUTPUTS</span></span>

### <span data-ttu-id="18a02-125">Microsoft. Azure. Commands. CosmosDB. Models. PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="18a02-125">Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath</span></span>

## <span data-ttu-id="18a02-126">Note</span><span class="sxs-lookup"><span data-stu-id="18a02-126">NOTES</span></span>

## <span data-ttu-id="18a02-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="18a02-127">RELATED LINKS</span></span>
