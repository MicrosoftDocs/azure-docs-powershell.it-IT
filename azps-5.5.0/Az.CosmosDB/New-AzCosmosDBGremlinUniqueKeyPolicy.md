---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
ms.openlocfilehash: 275019b1eaf4854c4fd9e5be84791368fe09efba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196791"
---
# <span data-ttu-id="a8872-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="a8872-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span></span>

## <span data-ttu-id="a8872-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8872-102">SYNOPSIS</span></span>
<span data-ttu-id="a8872-103">Crea un nuovo oggettoDb UniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="a8872-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="a8872-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a8872-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a8872-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a8872-105">DESCRIPTION</span></span>
<span data-ttu-id="a8872-106">Il cmdlet **New-AzCosmosDBGremlinUniqueKeyPolicy** crea un nuovo oggetto di tipo PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="a8872-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="a8872-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a8872-107">EXAMPLES</span></span>

### <span data-ttu-id="a8872-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a8872-108">Example 1</span></span>
```powershell
PS C:\> $uk = New-AzCosmosDBGremlinUniqueKey -Path "abc"

 New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey $uk,$uk
 
 UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="a8872-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8872-109">PARAMETERS</span></span>

### <span data-ttu-id="a8872-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8872-110">-DefaultProfile</span></span>
<span data-ttu-id="a8872-111">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a8872-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8872-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="a8872-112">-UniqueKey</span></span>
<span data-ttu-id="a8872-113">Matrice di oggetti di tipo PSUniqueKey.</span><span class="sxs-lookup"><span data-stu-id="a8872-113">Array of objects of type PSUniqueKey.</span></span>

```yaml
Type: PSSqlUniqueKey[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8872-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8872-114">CommonParameters</span></span>
<span data-ttu-id="a8872-115">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8872-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8872-116">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a8872-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8872-117">INPUT</span><span class="sxs-lookup"><span data-stu-id="a8872-117">INPUTS</span></span>

### <span data-ttu-id="a8872-118">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a8872-118">None</span></span>

## <span data-ttu-id="a8872-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a8872-119">OUTPUTS</span></span>

### <span data-ttu-id="a8872-120">Microsoft.Azure.Commands.ChancesDB.Models.PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="a8872-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

## <span data-ttu-id="a8872-121">NOTE</span><span class="sxs-lookup"><span data-stu-id="a8872-121">NOTES</span></span>

## <span data-ttu-id="a8872-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a8872-122">RELATED LINKS</span></span>
