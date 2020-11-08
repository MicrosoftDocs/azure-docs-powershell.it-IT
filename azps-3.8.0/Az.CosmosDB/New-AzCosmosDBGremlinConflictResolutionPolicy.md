---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
ms.openlocfilehash: 4662368f89f77c331619472feefe16736c40ef55
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020044"
---
# <span data-ttu-id="a3345-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="a3345-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span></span>

## <span data-ttu-id="a3345-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a3345-102">SYNOPSIS</span></span>
<span data-ttu-id="a3345-103">Crea un nuovo oggetto di tipo PSConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="a3345-103">Creates a new object of type PSConflictResolutionPolicy.</span></span> <span data-ttu-id="a3345-104">Può essere passato come valore di parametro per set-AzCosmosDBGremlinGraph.</span><span class="sxs-lookup"><span data-stu-id="a3345-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="a3345-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a3345-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3345-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a3345-106">DESCRIPTION</span></span>
<span data-ttu-id="a3345-107">Oggetto corrispondente alla ConflictResolutionPolicy dell'API Gremlin.</span><span class="sxs-lookup"><span data-stu-id="a3345-107">Object corresponding to Gremlin API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="a3345-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a3345-108">EXAMPLES</span></span>

### <span data-ttu-id="a3345-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a3345-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

## <span data-ttu-id="a3345-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a3345-110">PARAMETERS</span></span>

### <span data-ttu-id="a3345-111">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="a3345-111">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="a3345-112">Da fornire quando il tipo è personalizzato.</span><span class="sxs-lookup"><span data-stu-id="a3345-112">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="a3345-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3345-113">-DefaultProfile</span></span>
<span data-ttu-id="a3345-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a3345-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3345-115">-Path</span><span class="sxs-lookup"><span data-stu-id="a3345-115">-Path</span></span>
<span data-ttu-id="a3345-116">Da fornire quando il tipo è LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="a3345-116">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="a3345-117">-Digitare</span><span class="sxs-lookup"><span data-stu-id="a3345-117">-Type</span></span>
<span data-ttu-id="a3345-118">Possono avere i valori: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="a3345-118">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="a3345-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3345-119">CommonParameters</span></span>
<span data-ttu-id="a3345-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3345-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3345-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a3345-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3345-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a3345-122">INPUTS</span></span>

### <span data-ttu-id="a3345-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a3345-123">None</span></span>

## <span data-ttu-id="a3345-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a3345-124">OUTPUTS</span></span>

### <span data-ttu-id="a3345-125">Microsoft. Azure. Commands. CosmosDB. Models. PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="a3345-125">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

## <span data-ttu-id="a3345-126">Note</span><span class="sxs-lookup"><span data-stu-id="a3345-126">NOTES</span></span>

## <span data-ttu-id="a3345-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a3345-127">RELATED LINKS</span></span>
