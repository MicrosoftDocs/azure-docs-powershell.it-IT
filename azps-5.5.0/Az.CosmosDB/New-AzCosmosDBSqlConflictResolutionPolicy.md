---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
ms.openlocfilehash: b11142be65935522a73d3a068be0ee329994e2ee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198959"
---
# <span data-ttu-id="1a52c-101">New-AzCosmosDBSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="1a52c-101">New-AzCosmosDBSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="1a52c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a52c-102">SYNOPSIS</span></span>
<span data-ttu-id="1a52c-103">Crea un nuovo oggetto di tipo PSSqlConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="1a52c-103">Creates a new object of type PSSqlConflictResolutionPolicy.</span></span> <span data-ttu-id="1a52c-104">Può essere passato come valore di parametro per Set-AzCosmosDBSqlContainer.</span><span class="sxs-lookup"><span data-stu-id="1a52c-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="1a52c-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1a52c-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a52c-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1a52c-106">DESCRIPTION</span></span>
<span data-ttu-id="1a52c-107">Oggetto corrispondente all'api Sql ConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="1a52c-107">Object corresponding to Sql API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="1a52c-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1a52c-108">EXAMPLES</span></span>

### <span data-ttu-id="1a52c-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1a52c-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

<span data-ttu-id="1a52c-110">{{ Aggiungi la descrizione di esempio qui }}</span><span class="sxs-lookup"><span data-stu-id="1a52c-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="1a52c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a52c-111">PARAMETERS</span></span>

### <span data-ttu-id="1a52c-112">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="1a52c-112">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="1a52c-113">Da immettere quando il tipo è personalizzato.</span><span class="sxs-lookup"><span data-stu-id="1a52c-113">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="1a52c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a52c-114">-DefaultProfile</span></span>
<span data-ttu-id="1a52c-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1a52c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a52c-116">-Path</span><span class="sxs-lookup"><span data-stu-id="1a52c-116">-Path</span></span>
<span data-ttu-id="1a52c-117">Da immettere quando il tipo è LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="1a52c-117">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="1a52c-118">-Type</span><span class="sxs-lookup"><span data-stu-id="1a52c-118">-Type</span></span>
<span data-ttu-id="1a52c-119">Possono contenere i valori: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="1a52c-119">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="1a52c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a52c-120">CommonParameters</span></span>
<span data-ttu-id="1a52c-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a52c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a52c-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1a52c-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a52c-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="1a52c-123">INPUTS</span></span>

### <span data-ttu-id="1a52c-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1a52c-124">None</span></span>

## <span data-ttu-id="1a52c-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1a52c-125">OUTPUTS</span></span>

### <span data-ttu-id="1a52c-126">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="1a52c-126">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="1a52c-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="1a52c-127">NOTES</span></span>

## <span data-ttu-id="1a52c-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1a52c-128">RELATED LINKS</span></span>
