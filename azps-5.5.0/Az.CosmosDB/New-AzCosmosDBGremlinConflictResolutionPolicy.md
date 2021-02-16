---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
ms.openlocfilehash: 4662368f89f77c331619472feefe16736c40ef55
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198966"
---
# <span data-ttu-id="ec6e4-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="ec6e4-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span></span>

## <span data-ttu-id="ec6e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec6e4-102">SYNOPSIS</span></span>
<span data-ttu-id="ec6e4-103">Crea un nuovo oggetto di tipo PSConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="ec6e4-103">Creates a new object of type PSConflictResolutionPolicy.</span></span> <span data-ttu-id="ec6e4-104">Può essere passato come valore di parametro per Set-AzCosmosDBGremlinGraph.</span><span class="sxs-lookup"><span data-stu-id="ec6e4-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="ec6e4-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ec6e4-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec6e4-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ec6e4-106">DESCRIPTION</span></span>
<span data-ttu-id="ec6e4-107">Oggetto corrispondente all'API ConflictResolutionPolicy dell'API Gremlin.</span><span class="sxs-lookup"><span data-stu-id="ec6e4-107">Object corresponding to Gremlin API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="ec6e4-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ec6e4-108">EXAMPLES</span></span>

### <span data-ttu-id="ec6e4-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ec6e4-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

## <span data-ttu-id="ec6e4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec6e4-110">PARAMETERS</span></span>

### <span data-ttu-id="ec6e4-111">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="ec6e4-111">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="ec6e4-112">Da immettere quando il tipo è personalizzato.</span><span class="sxs-lookup"><span data-stu-id="ec6e4-112">To be provided when the type is custom.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec6e4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec6e4-113">-DefaultProfile</span></span>
<span data-ttu-id="ec6e4-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ec6e4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec6e4-115">-Path</span><span class="sxs-lookup"><span data-stu-id="ec6e4-115">-Path</span></span>
<span data-ttu-id="ec6e4-116">Da immettere quando il tipo è LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="ec6e4-116">To be provided when the type is LastWriterWins.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec6e4-117">-Type</span><span class="sxs-lookup"><span data-stu-id="ec6e4-117">-Type</span></span>
<span data-ttu-id="ec6e4-118">Possono contenere i valori: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="ec6e4-118">Can have the values: LastWriterWins, Custom, Manual.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec6e4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec6e4-119">CommonParameters</span></span>
<span data-ttu-id="ec6e4-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec6e4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec6e4-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ec6e4-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec6e4-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="ec6e4-122">INPUTS</span></span>

### <span data-ttu-id="ec6e4-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ec6e4-123">None</span></span>

## <span data-ttu-id="ec6e4-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ec6e4-124">OUTPUTS</span></span>

### <span data-ttu-id="ec6e4-125">Microsoft.Azure.Commands.FerenzasDB.Models.PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="ec6e4-125">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

## <span data-ttu-id="ec6e4-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="ec6e4-126">NOTES</span></span>

## <span data-ttu-id="ec6e4-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ec6e4-127">RELATED LINKS</span></span>
