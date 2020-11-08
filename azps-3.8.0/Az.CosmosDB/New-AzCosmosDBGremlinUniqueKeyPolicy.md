---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
ms.openlocfilehash: 593e299a6d7a1aa8131848f6de5f6c7aec8bd8c9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021603"
---
# <span data-ttu-id="7c308-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="7c308-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span></span>

## <span data-ttu-id="7c308-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7c308-102">SYNOPSIS</span></span>
<span data-ttu-id="7c308-103">Crea un nuovo oggetto UniqueKeyPolicy CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="7c308-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="7c308-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7c308-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey <PSUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7c308-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c308-105">DESCRIPTION</span></span>
<span data-ttu-id="7c308-106">Il cmdlet **New-AzCosmosDBGremlinUniqueKeyPolicy** crea un nuovo oggetto di tipo PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="7c308-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="7c308-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7c308-107">EXAMPLES</span></span>

### <span data-ttu-id="7c308-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7c308-108">Example 1</span></span>
```powershell
PS C:\> $uk = New-AzCosmosDBGremlinUniqueKey -Path "abc"

 New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey $uk,$uk
 
 UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="7c308-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7c308-109">PARAMETERS</span></span>

### <span data-ttu-id="7c308-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c308-110">-DefaultProfile</span></span>
<span data-ttu-id="7c308-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7c308-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c308-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="7c308-112">-UniqueKey</span></span>
<span data-ttu-id="7c308-113">Matrice di oggetti di tipo PSUniqueKey.</span><span class="sxs-lookup"><span data-stu-id="7c308-113">Array of objects of type PSUniqueKey.</span></span>

```yaml
Type: PSUniqueKey[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c308-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c308-114">CommonParameters</span></span>
<span data-ttu-id="7c308-115">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c308-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c308-116">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7c308-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c308-117">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7c308-117">INPUTS</span></span>

### <span data-ttu-id="7c308-118">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7c308-118">None</span></span>

## <span data-ttu-id="7c308-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7c308-119">OUTPUTS</span></span>

### <span data-ttu-id="7c308-120">Microsoft. Azure. Commands. CosmosDB. Models. PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="7c308-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

## <span data-ttu-id="7c308-121">Note</span><span class="sxs-lookup"><span data-stu-id="7c308-121">NOTES</span></span>

## <span data-ttu-id="7c308-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7c308-122">RELATED LINKS</span></span>
