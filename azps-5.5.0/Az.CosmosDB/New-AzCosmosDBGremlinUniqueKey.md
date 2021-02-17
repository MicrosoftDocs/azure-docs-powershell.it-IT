---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
ms.openlocfilehash: a51075274c20d0beeb9e73c26ec72f5f69fdf388
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177254"
---
# <span data-ttu-id="97c07-101">New-AzCosmosDBGremlinUniqueKey</span><span class="sxs-lookup"><span data-stu-id="97c07-101">New-AzCosmosDBGremlinUniqueKey</span></span>

## <span data-ttu-id="97c07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97c07-102">SYNOPSIS</span></span>
<span data-ttu-id="97c07-103">Crea un nuovo oggettoDb UniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="97c07-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="97c07-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="97c07-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97c07-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="97c07-105">DESCRIPTION</span></span>
<span data-ttu-id="97c07-106">Il cmdlet **New-AzCosmosDBGremlinUniqueKeyPolicy** crea un nuovo oggetto di tipo PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="97c07-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="97c07-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="97c07-107">EXAMPLES</span></span>

### <span data-ttu-id="97c07-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="97c07-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinUniqueKey -Path "abc"
UniqueKeys
----------
{Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey}
```

## <span data-ttu-id="97c07-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97c07-109">PARAMETERS</span></span>

### <span data-ttu-id="97c07-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97c07-110">-DefaultProfile</span></span>
<span data-ttu-id="97c07-111">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="97c07-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97c07-112">-Path</span><span class="sxs-lookup"><span data-stu-id="97c07-112">-Path</span></span>
<span data-ttu-id="97c07-113">Matrice di valori di stringa di percorso</span><span class="sxs-lookup"><span data-stu-id="97c07-113">Array of string of path values</span></span>

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

### <span data-ttu-id="97c07-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97c07-114">CommonParameters</span></span>
<span data-ttu-id="97c07-115">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97c07-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97c07-116">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="97c07-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97c07-117">INPUT</span><span class="sxs-lookup"><span data-stu-id="97c07-117">INPUTS</span></span>

### <span data-ttu-id="97c07-118">Nessuno</span><span class="sxs-lookup"><span data-stu-id="97c07-118">None</span></span>

## <span data-ttu-id="97c07-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="97c07-119">OUTPUTS</span></span>

### <span data-ttu-id="97c07-120">Microsoft.Azure.Commands.ChancesDB.Models.PSUniqueKey</span><span class="sxs-lookup"><span data-stu-id="97c07-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey</span></span>

## <span data-ttu-id="97c07-121">NOTE</span><span class="sxs-lookup"><span data-stu-id="97c07-121">NOTES</span></span>

## <span data-ttu-id="97c07-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="97c07-122">RELATED LINKS</span></span>
