---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlinconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
ms.openlocfilehash: c67627068ef2fc90f8322b2e8b63dd6cd68acbe3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007966"
---
# <span data-ttu-id="f2a50-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="f2a50-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span></span>

## <span data-ttu-id="f2a50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2a50-102">SYNOPSIS</span></span>
<span data-ttu-id="f2a50-103">Crea un nuovo oggetto di tipo PSConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="f2a50-103">Creates a new object of type PSConflictResolutionPolicy.</span></span> <span data-ttu-id="f2a50-104">Può essere passato come valore di parametro per Set-AzCosmosDBGremlinGraph.</span><span class="sxs-lookup"><span data-stu-id="f2a50-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="f2a50-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f2a50-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2a50-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f2a50-106">DESCRIPTION</span></span>
<span data-ttu-id="f2a50-107">Oggetto corrispondente all'API ConflictResolutionPolicy dell'API Gremlin.</span><span class="sxs-lookup"><span data-stu-id="f2a50-107">Object corresponding to Gremlin API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="f2a50-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f2a50-108">EXAMPLES</span></span>

### <span data-ttu-id="f2a50-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f2a50-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

## <span data-ttu-id="f2a50-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2a50-110">PARAMETERS</span></span>

### <span data-ttu-id="f2a50-111">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="f2a50-111">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="f2a50-112">Da immettere quando il tipo è personalizzato.</span><span class="sxs-lookup"><span data-stu-id="f2a50-112">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="f2a50-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2a50-113">-DefaultProfile</span></span>
<span data-ttu-id="f2a50-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f2a50-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2a50-115">-Path</span><span class="sxs-lookup"><span data-stu-id="f2a50-115">-Path</span></span>
<span data-ttu-id="f2a50-116">Da immettere quando il tipo è LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="f2a50-116">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="f2a50-117">-Type</span><span class="sxs-lookup"><span data-stu-id="f2a50-117">-Type</span></span>
<span data-ttu-id="f2a50-118">Possono contenere i valori: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="f2a50-118">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="f2a50-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2a50-119">CommonParameters</span></span>
<span data-ttu-id="f2a50-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2a50-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2a50-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f2a50-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2a50-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="f2a50-122">INPUTS</span></span>

### <span data-ttu-id="f2a50-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f2a50-123">None</span></span>

## <span data-ttu-id="f2a50-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f2a50-124">OUTPUTS</span></span>

### <span data-ttu-id="f2a50-125">Microsoft.Azure.Commands.FerenzasDB.Models.PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="f2a50-125">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

## <span data-ttu-id="f2a50-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="f2a50-126">NOTES</span></span>

## <span data-ttu-id="f2a50-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f2a50-127">RELATED LINKS</span></span>
