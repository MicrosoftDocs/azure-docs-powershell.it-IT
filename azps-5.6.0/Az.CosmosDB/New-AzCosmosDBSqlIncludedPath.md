---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqlincludedpath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPath.md
ms.openlocfilehash: a9d77cc76521eca1e99dac630673ef3825d1155b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962430"
---
# <span data-ttu-id="91b5c-101">New-AzCosmosDBSqlIncludedPath</span><span class="sxs-lookup"><span data-stu-id="91b5c-101">New-AzCosmosDBSqlIncludedPath</span></span>

## <span data-ttu-id="91b5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91b5c-102">SYNOPSIS</span></span>
<span data-ttu-id="91b5c-103">Crea un nuovo oggetto di tipo PSIncludedPath.</span><span class="sxs-lookup"><span data-stu-id="91b5c-103">Creates a new object of type PSIncludedPath.</span></span> <span data-ttu-id="91b5c-104">Può essere passato come valore di parametro per Set-AzCosmosDBSqlContainer.</span><span class="sxs-lookup"><span data-stu-id="91b5c-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="91b5c-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="91b5c-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlIncludedPath [-Path <String>] [-Index <PSIndexes[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91b5c-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="91b5c-106">DESCRIPTION</span></span>
<span data-ttu-id="91b5c-107">Oggetto corrispondente all'api Sql IncludedPath.</span><span class="sxs-lookup"><span data-stu-id="91b5c-107">Object corresponding to Sql API's IncludedPath.</span></span>

## <span data-ttu-id="91b5c-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="91b5c-108">EXAMPLES</span></span>

### <span data-ttu-id="91b5c-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="91b5c-109">Example 1</span></span>
```powershell
PS C:\> $index1 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
$index2 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash

New-AzCosmosDBSqlIncludedPath -Path "/*" -Index $index1,$index2

Path Indexes
---- -------
/*   {Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes,Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes}
```

## <span data-ttu-id="91b5c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91b5c-110">PARAMETERS</span></span>

### <span data-ttu-id="91b5c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91b5c-111">-DefaultProfile</span></span>
<span data-ttu-id="91b5c-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="91b5c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91b5c-113">-Index</span><span class="sxs-lookup"><span data-stu-id="91b5c-113">-Index</span></span>
<span data-ttu-id="91b5c-114">Elenco di indici per questo percorso</span><span class="sxs-lookup"><span data-stu-id="91b5c-114">List of indexes for this path</span></span>

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

### <span data-ttu-id="91b5c-115">-Path</span><span class="sxs-lookup"><span data-stu-id="91b5c-115">-Path</span></span>
<span data-ttu-id="91b5c-116">Percorso per cui si applica il comportamento di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="91b5c-116">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="91b5c-117">I percorsi di indice iniziano in genere con radice e terminano con un carattere jolly (/path/\*)</span><span class="sxs-lookup"><span data-stu-id="91b5c-117">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="91b5c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91b5c-118">CommonParameters</span></span>
<span data-ttu-id="91b5c-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91b5c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91b5c-120">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="91b5c-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91b5c-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="91b5c-121">INPUTS</span></span>

### <span data-ttu-id="91b5c-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="91b5c-122">None</span></span>

## <span data-ttu-id="91b5c-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="91b5c-123">OUTPUTS</span></span>

### <span data-ttu-id="91b5c-124">Microsoft.Azure.Commands.EnterpriseDb.Models.PSIncludedPath</span><span class="sxs-lookup"><span data-stu-id="91b5c-124">Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath</span></span>

## <span data-ttu-id="91b5c-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="91b5c-125">NOTES</span></span>

## <span data-ttu-id="91b5c-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="91b5c-126">RELATED LINKS</span></span>
