---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
ms.openlocfilehash: 54f7a1cb17413fe9d6703dbd0e909555e0c3926a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957438"
---
# <span data-ttu-id="e6130-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="e6130-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span></span>

## <span data-ttu-id="e6130-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6130-102">SYNOPSIS</span></span>
<span data-ttu-id="e6130-103">Crea un nuovo oggettoDb UniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="e6130-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="e6130-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e6130-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e6130-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e6130-105">DESCRIPTION</span></span>
<span data-ttu-id="e6130-106">Il cmdlet **New-AzCosmosDBGremlinUniqueKeyPolicy** crea un nuovo oggetto di tipo PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="e6130-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="e6130-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e6130-107">EXAMPLES</span></span>

### <span data-ttu-id="e6130-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e6130-108">Example 1</span></span>
```powershell
PS C:\> $uk = New-AzCosmosDBGremlinUniqueKey -Path "abc"

 New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey $uk,$uk
 
 UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="e6130-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6130-109">PARAMETERS</span></span>

### <span data-ttu-id="e6130-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6130-110">-DefaultProfile</span></span>
<span data-ttu-id="e6130-111">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e6130-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6130-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="e6130-112">-UniqueKey</span></span>
<span data-ttu-id="e6130-113">Matrice di oggetti di tipo PSUniqueKey.</span><span class="sxs-lookup"><span data-stu-id="e6130-113">Array of objects of type PSUniqueKey.</span></span>

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

### <span data-ttu-id="e6130-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6130-114">CommonParameters</span></span>
<span data-ttu-id="e6130-115">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6130-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6130-116">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e6130-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6130-117">INPUT</span><span class="sxs-lookup"><span data-stu-id="e6130-117">INPUTS</span></span>

### <span data-ttu-id="e6130-118">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e6130-118">None</span></span>

## <span data-ttu-id="e6130-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e6130-119">OUTPUTS</span></span>

### <span data-ttu-id="e6130-120">Microsoft.Azure.Commands.ChancesDB.Models.PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="e6130-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

## <span data-ttu-id="e6130-121">NOTE</span><span class="sxs-lookup"><span data-stu-id="e6130-121">NOTES</span></span>

## <span data-ttu-id="e6130-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e6130-122">RELATED LINKS</span></span>
