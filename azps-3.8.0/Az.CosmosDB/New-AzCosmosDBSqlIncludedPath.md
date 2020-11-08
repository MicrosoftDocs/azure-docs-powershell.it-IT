---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlincludedpath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPath.md
ms.openlocfilehash: 0def7fc552563f9b859fd6af7d07be5cd14cd001
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021599"
---
# <span data-ttu-id="07e7f-101">New-AzCosmosDBSqlIncludedPath</span><span class="sxs-lookup"><span data-stu-id="07e7f-101">New-AzCosmosDBSqlIncludedPath</span></span>

## <span data-ttu-id="07e7f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="07e7f-102">SYNOPSIS</span></span>
<span data-ttu-id="07e7f-103">Crea un nuovo oggetto di tipo PSIncludedPath.</span><span class="sxs-lookup"><span data-stu-id="07e7f-103">Creates a new object of type PSIncludedPath.</span></span> <span data-ttu-id="07e7f-104">Può essere passato come valore di parametro per set-AzCosmosDBSqlContainer.</span><span class="sxs-lookup"><span data-stu-id="07e7f-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="07e7f-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="07e7f-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlIncludedPath [-Path <String>] [-Index <PSIndexes[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07e7f-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07e7f-106">DESCRIPTION</span></span>
<span data-ttu-id="07e7f-107">Oggetto che corrisponde al IncludedPath dell'API SQL.</span><span class="sxs-lookup"><span data-stu-id="07e7f-107">Object corresponding to Sql API's IncludedPath.</span></span>

## <span data-ttu-id="07e7f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="07e7f-108">EXAMPLES</span></span>

### <span data-ttu-id="07e7f-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="07e7f-109">Example 1</span></span>
```powershell
PS C:\> $index1 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
$index2 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash

New-AzCosmosDBSqlIncludedPath -Path "/*" -Index $index1,$index2

Path Indexes
---- -------
/*   {Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes,Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes}
```

## <span data-ttu-id="07e7f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="07e7f-110">PARAMETERS</span></span>

### <span data-ttu-id="07e7f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07e7f-111">-DefaultProfile</span></span>
<span data-ttu-id="07e7f-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="07e7f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07e7f-113">-Index</span><span class="sxs-lookup"><span data-stu-id="07e7f-113">-Index</span></span>
<span data-ttu-id="07e7f-114">Elenco di indici per questo percorso</span><span class="sxs-lookup"><span data-stu-id="07e7f-114">List of indexes for this path</span></span>

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

### <span data-ttu-id="07e7f-115">-Path</span><span class="sxs-lookup"><span data-stu-id="07e7f-115">-Path</span></span>
<span data-ttu-id="07e7f-116">Percorso a cui si applica il comportamento di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="07e7f-116">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="07e7f-117">I percorsi di indice in genere iniziano con radice e terminano con caratteri jolly (/path/\*)</span><span class="sxs-lookup"><span data-stu-id="07e7f-117">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="07e7f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07e7f-118">CommonParameters</span></span>
<span data-ttu-id="07e7f-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07e7f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07e7f-120">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="07e7f-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07e7f-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="07e7f-121">INPUTS</span></span>

### <span data-ttu-id="07e7f-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="07e7f-122">None</span></span>

## <span data-ttu-id="07e7f-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="07e7f-123">OUTPUTS</span></span>

### <span data-ttu-id="07e7f-124">Microsoft. Azure. Commands. CosmosDB. Models. PSIncludedPath</span><span class="sxs-lookup"><span data-stu-id="07e7f-124">Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath</span></span>

## <span data-ttu-id="07e7f-125">Note</span><span class="sxs-lookup"><span data-stu-id="07e7f-125">NOTES</span></span>

## <span data-ttu-id="07e7f-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="07e7f-126">RELATED LINKS</span></span>
