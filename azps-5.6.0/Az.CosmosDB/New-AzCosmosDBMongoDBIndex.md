---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbmongodbindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBIndex.md
ms.openlocfilehash: a086705465aea30480a4f41f6981a47d8fcc612c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991449"
---
# <span data-ttu-id="2dcbb-101">New-AzCosmosDBMongoDBIndex</span><span class="sxs-lookup"><span data-stu-id="2dcbb-101">New-AzCosmosDBMongoDBIndex</span></span>

## <span data-ttu-id="2dcbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2dcbb-102">SYNOPSIS</span></span>
<span data-ttu-id="2dcbb-103">Crea un nuovo indiceDbDb MongoDB.</span><span class="sxs-lookup"><span data-stu-id="2dcbb-103">Creates a new CosmosDB MongoDB Index.</span></span>

## <span data-ttu-id="2dcbb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2dcbb-104">SYNTAX</span></span>

```
New-AzCosmosDBMongoDBIndex [-TtlInSeconds <Int32>] [-Unique <Boolean>] [-Key <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2dcbb-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2dcbb-105">DESCRIPTION</span></span>
<span data-ttu-id="2dcbb-106">**New-AzCosmosDBMongoDBIndex** crea un nuovo indiceDbDb MongoDB.</span><span class="sxs-lookup"><span data-stu-id="2dcbb-106">The **New-AzCosmosDBMongoDBIndex** creates a new CosmosDB MongoDB Index.</span></span>

## <span data-ttu-id="2dcbb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2dcbb-107">EXAMPLES</span></span>

### <span data-ttu-id="2dcbb-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2dcbb-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBMongoDBIndex -TtlInSeconds {val} -Unique 1 -Key "key1"
Key                                                       Options
---                                                       -------
Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndexKeys Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndexOptions
```

## <span data-ttu-id="2dcbb-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2dcbb-109">PARAMETERS</span></span>

### <span data-ttu-id="2dcbb-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dcbb-110">-DefaultProfile</span></span>
<span data-ttu-id="2dcbb-111">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2dcbb-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2dcbb-112">-Key</span><span class="sxs-lookup"><span data-stu-id="2dcbb-112">-Key</span></span>
<span data-ttu-id="2dcbb-113">Matrice di valori di chiave come stringhe.</span><span class="sxs-lookup"><span data-stu-id="2dcbb-113">Array of key values as strings.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dcbb-114">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="2dcbb-114">-TtlInSeconds</span></span>
<span data-ttu-id="2dcbb-115">Numero di secondi dopo i quali scade l'indice.</span><span class="sxs-lookup"><span data-stu-id="2dcbb-115">Number of seconds after which the index expires.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dcbb-116">-Unique</span><span class="sxs-lookup"><span data-stu-id="2dcbb-116">-Unique</span></span>
<span data-ttu-id="2dcbb-117">Bool per indicare se l'indice è univoco o meno.</span><span class="sxs-lookup"><span data-stu-id="2dcbb-117">Bool to indicate if the index is unique or not.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dcbb-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dcbb-118">CommonParameters</span></span>
<span data-ttu-id="2dcbb-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dcbb-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dcbb-120">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2dcbb-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dcbb-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="2dcbb-121">INPUTS</span></span>

### <span data-ttu-id="2dcbb-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2dcbb-122">None</span></span>

## <span data-ttu-id="2dcbb-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2dcbb-123">OUTPUTS</span></span>

### <span data-ttu-id="2dcbb-124">Microsoft.Azure.Commands.EnterpriseDb.Models.PSMongoIndex</span><span class="sxs-lookup"><span data-stu-id="2dcbb-124">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndex</span></span>

## <span data-ttu-id="2dcbb-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="2dcbb-125">NOTES</span></span>

## <span data-ttu-id="2dcbb-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2dcbb-126">RELATED LINKS</span></span>
