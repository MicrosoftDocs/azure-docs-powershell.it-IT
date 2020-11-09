---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
ms.openlocfilehash: a51075274c20d0beeb9e73c26ec72f5f69fdf388
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299317"
---
# <span data-ttu-id="e5267-101">New-AzCosmosDBGremlinUniqueKey</span><span class="sxs-lookup"><span data-stu-id="e5267-101">New-AzCosmosDBGremlinUniqueKey</span></span>

## <span data-ttu-id="e5267-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e5267-102">SYNOPSIS</span></span>
<span data-ttu-id="e5267-103">Crea un nuovo oggetto UniqueKeyPolicy CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="e5267-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="e5267-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e5267-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5267-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e5267-105">DESCRIPTION</span></span>
<span data-ttu-id="e5267-106">Il cmdlet **New-AzCosmosDBGremlinUniqueKeyPolicy** crea un nuovo oggetto di tipo PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="e5267-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="e5267-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e5267-107">EXAMPLES</span></span>

### <span data-ttu-id="e5267-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e5267-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinUniqueKey -Path "abc"
UniqueKeys
----------
{Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey}
```

## <span data-ttu-id="e5267-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e5267-109">PARAMETERS</span></span>

### <span data-ttu-id="e5267-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5267-110">-DefaultProfile</span></span>
<span data-ttu-id="e5267-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e5267-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5267-112">-Path</span><span class="sxs-lookup"><span data-stu-id="e5267-112">-Path</span></span>
<span data-ttu-id="e5267-113">Matrice di stringa di valori di percorso</span><span class="sxs-lookup"><span data-stu-id="e5267-113">Array of string of path values</span></span>

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

### <span data-ttu-id="e5267-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5267-114">CommonParameters</span></span>
<span data-ttu-id="e5267-115">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5267-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5267-116">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5267-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5267-117">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e5267-117">INPUTS</span></span>

### <span data-ttu-id="e5267-118">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e5267-118">None</span></span>

## <span data-ttu-id="e5267-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e5267-119">OUTPUTS</span></span>

### <span data-ttu-id="e5267-120">Microsoft. Azure. Commands. CosmosDB. Models. PSUniqueKey</span><span class="sxs-lookup"><span data-stu-id="e5267-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey</span></span>

## <span data-ttu-id="e5267-121">Note</span><span class="sxs-lookup"><span data-stu-id="e5267-121">NOTES</span></span>

## <span data-ttu-id="e5267-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e5267-122">RELATED LINKS</span></span>
