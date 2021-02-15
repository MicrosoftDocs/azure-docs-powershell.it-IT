---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
ms.openlocfilehash: e3c96cfd4051a186e0584d810088bc06a57ad862
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200607"
---
# <span data-ttu-id="3e22c-101">New-AzCosmosDBSqlUniqueKey</span><span class="sxs-lookup"><span data-stu-id="3e22c-101">New-AzCosmosDBSqlUniqueKey</span></span>

## <span data-ttu-id="3e22c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e22c-102">SYNOPSIS</span></span>
<span data-ttu-id="3e22c-103">Crea un nuovo oggetto Sql UniqueKey del database di database.</span><span class="sxs-lookup"><span data-stu-id="3e22c-103">Creates a new CosmosDB Sql UniqueKey object.</span></span>

## <span data-ttu-id="3e22c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3e22c-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e22c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3e22c-105">DESCRIPTION</span></span>
<span data-ttu-id="3e22c-106">Il cmdlet **New-AzCosmosDBSqlUniqueKey** crea un nuovo oggetto di tipo PSUniqueKey.</span><span class="sxs-lookup"><span data-stu-id="3e22c-106">The **New-AzCosmosDBSqlUniqueKey** cmdlet creates a new object of type PSUniqueKey.</span></span>

## <span data-ttu-id="3e22c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3e22c-107">EXAMPLES</span></span>

### <span data-ttu-id="3e22c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3e22c-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlUniqueKey -Path {path}

Path
----
{path}
```

## <span data-ttu-id="3e22c-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e22c-109">PARAMETERS</span></span>

### <span data-ttu-id="3e22c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e22c-110">-DefaultProfile</span></span>
<span data-ttu-id="3e22c-111">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3e22c-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e22c-112">-Path</span><span class="sxs-lookup"><span data-stu-id="3e22c-112">-Path</span></span>
<span data-ttu-id="3e22c-113">Matrice di valori di stringa di percorso</span><span class="sxs-lookup"><span data-stu-id="3e22c-113">Array of string of path values</span></span>

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

### <span data-ttu-id="3e22c-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e22c-114">CommonParameters</span></span>
<span data-ttu-id="3e22c-115">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e22c-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e22c-116">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3e22c-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e22c-117">INPUT</span><span class="sxs-lookup"><span data-stu-id="3e22c-117">INPUTS</span></span>

### <span data-ttu-id="3e22c-118">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3e22c-118">None</span></span>

## <span data-ttu-id="3e22c-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3e22c-119">OUTPUTS</span></span>

### <span data-ttu-id="3e22c-120">Microsoft.Azure.Commands.ChancesDB.Models.PSSqlUniqueKey</span><span class="sxs-lookup"><span data-stu-id="3e22c-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey</span></span>

## <span data-ttu-id="3e22c-121">NOTE</span><span class="sxs-lookup"><span data-stu-id="3e22c-121">NOTES</span></span>

## <span data-ttu-id="3e22c-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3e22c-122">RELATED LINKS</span></span>
