---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlcompositepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlCompositePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlCompositePath.md
ms.openlocfilehash: ff78ad82c89b774f034fe6f1d4499db7868d43c7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477424"
---
# <span data-ttu-id="a2815-101">New-AzCosmosDBSqlCompositePath</span><span class="sxs-lookup"><span data-stu-id="a2815-101">New-AzCosmosDBSqlCompositePath</span></span>

## <span data-ttu-id="a2815-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a2815-102">SYNOPSIS</span></span>
<span data-ttu-id="a2815-103">Crea un nuovo oggetto di tipo PSCompositePath.</span><span class="sxs-lookup"><span data-stu-id="a2815-103">Creates a new object of type PSCompositePath.</span></span> <span data-ttu-id="a2815-104">Può essere passato come valore di parametro per set-AzCosmosDBSqlContainer.</span><span class="sxs-lookup"><span data-stu-id="a2815-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="a2815-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a2815-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlCompositePath [-Path <String>] [-Order <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a2815-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a2815-106">DESCRIPTION</span></span>
<span data-ttu-id="a2815-107">Oggetto che corrisponde al CompositePath dell'API SQL.</span><span class="sxs-lookup"><span data-stu-id="a2815-107">Object corresponding to Sql API's CompositePath.</span></span>

## <span data-ttu-id="a2815-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a2815-108">EXAMPLES</span></span>

### <span data-ttu-id="a2815-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a2815-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlCompositePath -Path "/abc" -Order Ascending

Path Order
---- -----
/abc Ascending
```

## <span data-ttu-id="a2815-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a2815-110">PARAMETERS</span></span>

### <span data-ttu-id="a2815-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2815-111">-DefaultProfile</span></span>
<span data-ttu-id="a2815-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a2815-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2815-113">-Ordine</span><span class="sxs-lookup"><span data-stu-id="a2815-113">-Order</span></span>
<span data-ttu-id="a2815-114">Ottiene o imposta l'ordine di ordinamento per i percorsi compositi.</span><span class="sxs-lookup"><span data-stu-id="a2815-114">Gets or sets sort order for composite paths.</span></span>
<span data-ttu-id="a2815-115">I valori possibili includono: "crescente", "decrescente"</span><span class="sxs-lookup"><span data-stu-id="a2815-115">Possible values include: 'Ascending', 'Descending'</span></span>

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

### <span data-ttu-id="a2815-116">-Path</span><span class="sxs-lookup"><span data-stu-id="a2815-116">-Path</span></span>
<span data-ttu-id="a2815-117">Percorso a cui si applica il comportamento di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="a2815-117">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="a2815-118">I percorsi di indice in genere iniziano con radice e terminano con caratteri jolly (/path/\*)</span><span class="sxs-lookup"><span data-stu-id="a2815-118">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="a2815-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2815-119">CommonParameters</span></span>
<span data-ttu-id="a2815-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2815-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2815-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a2815-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2815-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a2815-122">INPUTS</span></span>

### <span data-ttu-id="a2815-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a2815-123">None</span></span>

## <span data-ttu-id="a2815-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a2815-124">OUTPUTS</span></span>

### <span data-ttu-id="a2815-125">Microsoft. Azure. Commands. CosmosDB. Models. PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="a2815-125">Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath</span></span>

## <span data-ttu-id="a2815-126">Note</span><span class="sxs-lookup"><span data-stu-id="a2815-126">NOTES</span></span>

## <span data-ttu-id="a2815-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a2815-127">RELATED LINKS</span></span>
