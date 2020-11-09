---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbmongodbindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBIndex.md
ms.openlocfilehash: c88e1567a7784f89eadd112d7a985b1f2f286a40
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299275"
---
# <span data-ttu-id="342fd-101">New-AzCosmosDBMongoDBIndex</span><span class="sxs-lookup"><span data-stu-id="342fd-101">New-AzCosmosDBMongoDBIndex</span></span>

## <span data-ttu-id="342fd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="342fd-102">SYNOPSIS</span></span>
<span data-ttu-id="342fd-103">Crea un nuovo indice MongoDB di CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="342fd-103">Creates a new CosmosDB MongoDB Index.</span></span>

## <span data-ttu-id="342fd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="342fd-104">SYNTAX</span></span>

```
New-AzCosmosDBMongoDBIndex [-TtlInSeconds <Int32>] [-Unique <Boolean>] [-Key <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="342fd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="342fd-105">DESCRIPTION</span></span>
<span data-ttu-id="342fd-106">Il **nuovo AzCosmosDBMongoDBIndex** crea un nuovo indice MongoDB di CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="342fd-106">The **New-AzCosmosDBMongoDBIndex** creates a new CosmosDB MongoDB Index.</span></span>

## <span data-ttu-id="342fd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="342fd-107">EXAMPLES</span></span>

### <span data-ttu-id="342fd-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="342fd-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBMongoDBIndex -TtlInSeconds {val} -Unique 1 -Key "key1"
Key                                                       Options
---                                                       -------
Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndexKeys Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndexOptions
```

## <span data-ttu-id="342fd-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="342fd-109">PARAMETERS</span></span>

### <span data-ttu-id="342fd-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="342fd-110">-DefaultProfile</span></span>
<span data-ttu-id="342fd-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="342fd-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="342fd-112">-Key</span><span class="sxs-lookup"><span data-stu-id="342fd-112">-Key</span></span>
<span data-ttu-id="342fd-113">Matrice di valori chiave come stringhe.</span><span class="sxs-lookup"><span data-stu-id="342fd-113">Array of key values as strings.</span></span>

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

### <span data-ttu-id="342fd-114">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="342fd-114">-TtlInSeconds</span></span>
<span data-ttu-id="342fd-115">Numero di secondi dopo il quale l'indice scade.</span><span class="sxs-lookup"><span data-stu-id="342fd-115">Number of seconds after which the index expires.</span></span>

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

### <span data-ttu-id="342fd-116">-Unique</span><span class="sxs-lookup"><span data-stu-id="342fd-116">-Unique</span></span>
<span data-ttu-id="342fd-117">Bool per indicare se l'indice è univoco o meno.</span><span class="sxs-lookup"><span data-stu-id="342fd-117">Bool to indicate if the index is unique or not.</span></span>

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

### <span data-ttu-id="342fd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="342fd-118">CommonParameters</span></span>
<span data-ttu-id="342fd-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="342fd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="342fd-120">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="342fd-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="342fd-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="342fd-121">INPUTS</span></span>

### <span data-ttu-id="342fd-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="342fd-122">None</span></span>

## <span data-ttu-id="342fd-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="342fd-123">OUTPUTS</span></span>

### <span data-ttu-id="342fd-124">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoIndex</span><span class="sxs-lookup"><span data-stu-id="342fd-124">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndex</span></span>

## <span data-ttu-id="342fd-125">Note</span><span class="sxs-lookup"><span data-stu-id="342fd-125">NOTES</span></span>

## <span data-ttu-id="342fd-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="342fd-126">RELATED LINKS</span></span>
