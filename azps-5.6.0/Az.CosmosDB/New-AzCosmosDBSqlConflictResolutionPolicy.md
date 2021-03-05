---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqlconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
ms.openlocfilehash: e5742cde3a39cb2bf7dc96b952b3129d353235f0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985205"
---
# <span data-ttu-id="adbb9-101">New-AzCosmosDBSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="adbb9-101">New-AzCosmosDBSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="adbb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adbb9-102">SYNOPSIS</span></span>
<span data-ttu-id="adbb9-103">Crea un nuovo oggetto di tipo PSSqlConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="adbb9-103">Creates a new object of type PSSqlConflictResolutionPolicy.</span></span> <span data-ttu-id="adbb9-104">Può essere passato come valore di parametro per Set-AzCosmosDBSqlContainer.</span><span class="sxs-lookup"><span data-stu-id="adbb9-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="adbb9-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="adbb9-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="adbb9-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="adbb9-106">DESCRIPTION</span></span>
<span data-ttu-id="adbb9-107">Oggetto corrispondente all'api Sql ConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="adbb9-107">Object corresponding to Sql API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="adbb9-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="adbb9-108">EXAMPLES</span></span>

### <span data-ttu-id="adbb9-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="adbb9-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

<span data-ttu-id="adbb9-110">{{ Aggiungi la descrizione di esempio qui }}</span><span class="sxs-lookup"><span data-stu-id="adbb9-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="adbb9-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="adbb9-111">PARAMETERS</span></span>

### <span data-ttu-id="adbb9-112">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="adbb9-112">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="adbb9-113">Da immettere quando il tipo è personalizzato.</span><span class="sxs-lookup"><span data-stu-id="adbb9-113">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="adbb9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adbb9-114">-DefaultProfile</span></span>
<span data-ttu-id="adbb9-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="adbb9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adbb9-116">-Path</span><span class="sxs-lookup"><span data-stu-id="adbb9-116">-Path</span></span>
<span data-ttu-id="adbb9-117">Da immettere quando il tipo è LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="adbb9-117">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="adbb9-118">-Type</span><span class="sxs-lookup"><span data-stu-id="adbb9-118">-Type</span></span>
<span data-ttu-id="adbb9-119">Possono contenere i valori: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="adbb9-119">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="adbb9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adbb9-120">CommonParameters</span></span>
<span data-ttu-id="adbb9-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adbb9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adbb9-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="adbb9-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adbb9-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="adbb9-123">INPUTS</span></span>

### <span data-ttu-id="adbb9-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="adbb9-124">None</span></span>

## <span data-ttu-id="adbb9-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="adbb9-125">OUTPUTS</span></span>

### <span data-ttu-id="adbb9-126">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="adbb9-126">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="adbb9-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="adbb9-127">NOTES</span></span>

## <span data-ttu-id="adbb9-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="adbb9-128">RELATED LINKS</span></span>
