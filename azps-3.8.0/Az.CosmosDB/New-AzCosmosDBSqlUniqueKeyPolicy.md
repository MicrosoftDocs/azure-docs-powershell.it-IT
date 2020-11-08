---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
ms.openlocfilehash: bf91d1948b4040a35ee77f2a1111861a03076783
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021589"
---
# <span data-ttu-id="0c2cf-101">New-AzCosmosDBSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="0c2cf-101">New-AzCosmosDBSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="0c2cf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0c2cf-102">SYNOPSIS</span></span>
<span data-ttu-id="0c2cf-103">Crea un nuovo oggetto SqlUniqueKeyPolicy CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="0c2cf-103">Creates a new CosmosDB SqlUniqueKeyPolicy object.</span></span>

## <span data-ttu-id="0c2cf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0c2cf-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0c2cf-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c2cf-105">DESCRIPTION</span></span>
<span data-ttu-id="0c2cf-106">Il cmdlet **New-AzCosmosDBSqlUniqueKeyPolicy** crea un nuovo oggetto di tipo PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="0c2cf-106">The **New-AzCosmosDBSqlUniqueKeyPolicy** cmdlet creates a new object of type PSSqlUniqueKeyPolicy.</span></span>

## <span data-ttu-id="0c2cf-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0c2cf-107">EXAMPLES</span></span>

### <span data-ttu-id="0c2cf-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0c2cf-108">Example 1</span></span>
```powershell
PS C:\>New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey {psUniqueKey1, psUniqueKey2}

UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="0c2cf-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0c2cf-109">PARAMETERS</span></span>

### <span data-ttu-id="0c2cf-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c2cf-110">-DefaultProfile</span></span>
<span data-ttu-id="0c2cf-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0c2cf-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c2cf-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="0c2cf-112">-UniqueKey</span></span>
<span data-ttu-id="0c2cf-113">Nome database.</span><span class="sxs-lookup"><span data-stu-id="0c2cf-113">Database name.</span></span>

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

### <span data-ttu-id="0c2cf-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c2cf-114">CommonParameters</span></span>
<span data-ttu-id="0c2cf-115">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c2cf-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c2cf-116">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c2cf-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c2cf-117">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0c2cf-117">INPUTS</span></span>

### <span data-ttu-id="0c2cf-118">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0c2cf-118">None</span></span>

## <span data-ttu-id="0c2cf-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0c2cf-119">OUTPUTS</span></span>

### <span data-ttu-id="0c2cf-120">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="0c2cf-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="0c2cf-121">Note</span><span class="sxs-lookup"><span data-stu-id="0c2cf-121">NOTES</span></span>

## <span data-ttu-id="0c2cf-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0c2cf-122">RELATED LINKS</span></span>
