---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
ms.openlocfilehash: b172c5e22c26cba8d88d188198868da720d611d4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990329"
---
# <span data-ttu-id="a5a63-101">New-AzCosmosDBSqlUniqueKey</span><span class="sxs-lookup"><span data-stu-id="a5a63-101">New-AzCosmosDBSqlUniqueKey</span></span>

## <span data-ttu-id="a5a63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5a63-102">SYNOPSIS</span></span>
<span data-ttu-id="a5a63-103">Crea un nuovo oggetto Sql UniqueKey del database di database.</span><span class="sxs-lookup"><span data-stu-id="a5a63-103">Creates a new CosmosDB Sql UniqueKey object.</span></span>

## <span data-ttu-id="a5a63-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a5a63-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5a63-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a5a63-105">DESCRIPTION</span></span>
<span data-ttu-id="a5a63-106">Il cmdlet **New-AzCosmosDBSqlUniqueKey** crea un nuovo oggetto di tipo PSUniqueKey.</span><span class="sxs-lookup"><span data-stu-id="a5a63-106">The **New-AzCosmosDBSqlUniqueKey** cmdlet creates a new object of type PSUniqueKey.</span></span>

## <span data-ttu-id="a5a63-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a5a63-107">EXAMPLES</span></span>

### <span data-ttu-id="a5a63-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a5a63-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlUniqueKey -Path {path}

Path
----
{path}
```

## <span data-ttu-id="a5a63-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5a63-109">PARAMETERS</span></span>

### <span data-ttu-id="a5a63-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5a63-110">-DefaultProfile</span></span>
<span data-ttu-id="a5a63-111">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a5a63-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5a63-112">-Path</span><span class="sxs-lookup"><span data-stu-id="a5a63-112">-Path</span></span>
<span data-ttu-id="a5a63-113">Matrice di valori di stringa di percorso</span><span class="sxs-lookup"><span data-stu-id="a5a63-113">Array of string of path values</span></span>

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

### <span data-ttu-id="a5a63-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5a63-114">CommonParameters</span></span>
<span data-ttu-id="a5a63-115">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5a63-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5a63-116">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a5a63-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5a63-117">INPUT</span><span class="sxs-lookup"><span data-stu-id="a5a63-117">INPUTS</span></span>

### <span data-ttu-id="a5a63-118">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a5a63-118">None</span></span>

## <span data-ttu-id="a5a63-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a5a63-119">OUTPUTS</span></span>

### <span data-ttu-id="a5a63-120">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlUniqueKey</span><span class="sxs-lookup"><span data-stu-id="a5a63-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey</span></span>

## <span data-ttu-id="a5a63-121">NOTE</span><span class="sxs-lookup"><span data-stu-id="a5a63-121">NOTES</span></span>

## <span data-ttu-id="a5a63-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a5a63-122">RELATED LINKS</span></span>
