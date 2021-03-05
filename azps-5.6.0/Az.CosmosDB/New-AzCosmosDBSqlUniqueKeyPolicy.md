---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
ms.openlocfilehash: 6ef9e9b4fe2332af22bb8bdab1334096860f53ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986858"
---
# <span data-ttu-id="4b5b1-101">New-AzCosmosDBSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="4b5b1-101">New-AzCosmosDBSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="4b5b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b5b1-102">SYNOPSIS</span></span>
<span data-ttu-id="4b5b1-103">Crea un nuovo oggettoSqlsDB SqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="4b5b1-103">Creates a new CosmosDB SqlUniqueKeyPolicy object.</span></span>

## <span data-ttu-id="4b5b1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4b5b1-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4b5b1-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4b5b1-105">DESCRIPTION</span></span>
<span data-ttu-id="4b5b1-106">Il cmdlet **New-AzCosmosDBSqlUniqueKeyPolicy** crea un nuovo oggetto di tipo PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="4b5b1-106">The **New-AzCosmosDBSqlUniqueKeyPolicy** cmdlet creates a new object of type PSSqlUniqueKeyPolicy.</span></span>

## <span data-ttu-id="4b5b1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4b5b1-107">EXAMPLES</span></span>

### <span data-ttu-id="4b5b1-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4b5b1-108">Example 1</span></span>
```powershell
PS C:\>New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey {psUniqueKey1, psUniqueKey2}

UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="4b5b1-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b5b1-109">PARAMETERS</span></span>

### <span data-ttu-id="4b5b1-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b5b1-110">-DefaultProfile</span></span>
<span data-ttu-id="4b5b1-111">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4b5b1-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b5b1-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="4b5b1-112">-UniqueKey</span></span>
<span data-ttu-id="4b5b1-113">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="4b5b1-113">Database name.</span></span>

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

### <span data-ttu-id="4b5b1-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b5b1-114">CommonParameters</span></span>
<span data-ttu-id="4b5b1-115">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b5b1-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b5b1-116">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4b5b1-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b5b1-117">INPUT</span><span class="sxs-lookup"><span data-stu-id="4b5b1-117">INPUTS</span></span>

### <span data-ttu-id="4b5b1-118">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4b5b1-118">None</span></span>

## <span data-ttu-id="4b5b1-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4b5b1-119">OUTPUTS</span></span>

### <span data-ttu-id="4b5b1-120">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="4b5b1-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="4b5b1-121">NOTE</span><span class="sxs-lookup"><span data-stu-id="4b5b1-121">NOTES</span></span>

## <span data-ttu-id="4b5b1-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4b5b1-122">RELATED LINKS</span></span>
