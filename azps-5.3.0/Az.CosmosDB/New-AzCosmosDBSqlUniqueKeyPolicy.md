---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
ms.openlocfilehash: bf91d1948b4040a35ee77f2a1111861a03076783
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98487872"
---
# <span data-ttu-id="7e3b4-101">New-AzCosmosDBSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="7e3b4-101">New-AzCosmosDBSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="7e3b4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7e3b4-102">SYNOPSIS</span></span>
<span data-ttu-id="7e3b4-103">Crea un nuovo oggetto SqlUniqueKeyPolicy CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="7e3b4-103">Creates a new CosmosDB SqlUniqueKeyPolicy object.</span></span>

## <span data-ttu-id="7e3b4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7e3b4-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7e3b4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e3b4-105">DESCRIPTION</span></span>
<span data-ttu-id="7e3b4-106">Il cmdlet **New-AzCosmosDBSqlUniqueKeyPolicy** crea un nuovo oggetto di tipo PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="7e3b4-106">The **New-AzCosmosDBSqlUniqueKeyPolicy** cmdlet creates a new object of type PSSqlUniqueKeyPolicy.</span></span>

## <span data-ttu-id="7e3b4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7e3b4-107">EXAMPLES</span></span>

### <span data-ttu-id="7e3b4-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7e3b4-108">Example 1</span></span>
```powershell
PS C:\>New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey {psUniqueKey1, psUniqueKey2}

UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="7e3b4-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7e3b4-109">PARAMETERS</span></span>

### <span data-ttu-id="7e3b4-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e3b4-110">-DefaultProfile</span></span>
<span data-ttu-id="7e3b4-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7e3b4-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e3b4-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="7e3b4-112">-UniqueKey</span></span>
<span data-ttu-id="7e3b4-113">Nome database.</span><span class="sxs-lookup"><span data-stu-id="7e3b4-113">Database name.</span></span>

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

### <span data-ttu-id="7e3b4-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e3b4-114">CommonParameters</span></span>
<span data-ttu-id="7e3b4-115">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e3b4-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e3b4-116">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e3b4-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e3b4-117">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7e3b4-117">INPUTS</span></span>

### <span data-ttu-id="7e3b4-118">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7e3b4-118">None</span></span>

## <span data-ttu-id="7e3b4-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7e3b4-119">OUTPUTS</span></span>

### <span data-ttu-id="7e3b4-120">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="7e3b4-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="7e3b4-121">Note</span><span class="sxs-lookup"><span data-stu-id="7e3b4-121">NOTES</span></span>

## <span data-ttu-id="7e3b4-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7e3b4-122">RELATED LINKS</span></span>
