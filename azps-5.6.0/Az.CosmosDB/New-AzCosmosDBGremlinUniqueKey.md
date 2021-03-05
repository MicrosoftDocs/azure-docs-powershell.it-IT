---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
ms.openlocfilehash: b2984ffc8b2c268f5298d88e9dc64e0729798e97
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998786"
---
# <span data-ttu-id="3e5eb-101">New-AzCosmosDBGremlinUniqueKey</span><span class="sxs-lookup"><span data-stu-id="3e5eb-101">New-AzCosmosDBGremlinUniqueKey</span></span>

## <span data-ttu-id="3e5eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e5eb-102">SYNOPSIS</span></span>
<span data-ttu-id="3e5eb-103">Crea un nuovo oggettoDb UniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="3e5eb-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="3e5eb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3e5eb-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e5eb-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3e5eb-105">DESCRIPTION</span></span>
<span data-ttu-id="3e5eb-106">Il cmdlet **New-AzCosmosDBGremlinUniqueKeyPolicy** crea un nuovo oggetto di tipo PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="3e5eb-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="3e5eb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3e5eb-107">EXAMPLES</span></span>

### <span data-ttu-id="3e5eb-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3e5eb-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinUniqueKey -Path "abc"
UniqueKeys
----------
{Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey}
```

## <span data-ttu-id="3e5eb-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e5eb-109">PARAMETERS</span></span>

### <span data-ttu-id="3e5eb-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e5eb-110">-DefaultProfile</span></span>
<span data-ttu-id="3e5eb-111">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3e5eb-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e5eb-112">-Path</span><span class="sxs-lookup"><span data-stu-id="3e5eb-112">-Path</span></span>
<span data-ttu-id="3e5eb-113">Matrice di valori di stringa di percorso</span><span class="sxs-lookup"><span data-stu-id="3e5eb-113">Array of string of path values</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e5eb-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e5eb-114">CommonParameters</span></span>
<span data-ttu-id="3e5eb-115">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e5eb-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e5eb-116">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3e5eb-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e5eb-117">INPUT</span><span class="sxs-lookup"><span data-stu-id="3e5eb-117">INPUTS</span></span>

### <span data-ttu-id="3e5eb-118">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3e5eb-118">None</span></span>

## <span data-ttu-id="3e5eb-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3e5eb-119">OUTPUTS</span></span>

### <span data-ttu-id="3e5eb-120">Microsoft.Azure.Commands.ChancesDB.Models.PSUniqueKey</span><span class="sxs-lookup"><span data-stu-id="3e5eb-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey</span></span>

## <span data-ttu-id="3e5eb-121">NOTE</span><span class="sxs-lookup"><span data-stu-id="3e5eb-121">NOTES</span></span>

## <span data-ttu-id="3e5eb-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3e5eb-122">RELATED LINKS</span></span>
