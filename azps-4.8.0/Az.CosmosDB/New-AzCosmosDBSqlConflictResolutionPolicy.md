---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
ms.openlocfilehash: b11142be65935522a73d3a068be0ee329994e2ee
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190335"
---
# <span data-ttu-id="5e8bb-101">New-AzCosmosDBSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="5e8bb-101">New-AzCosmosDBSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="5e8bb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5e8bb-102">SYNOPSIS</span></span>
<span data-ttu-id="5e8bb-103">Crea un nuovo oggetto di tipo PSSqlConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="5e8bb-103">Creates a new object of type PSSqlConflictResolutionPolicy.</span></span> <span data-ttu-id="5e8bb-104">Può essere passato come valore di parametro per set-AzCosmosDBSqlContainer.</span><span class="sxs-lookup"><span data-stu-id="5e8bb-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="5e8bb-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5e8bb-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e8bb-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e8bb-106">DESCRIPTION</span></span>
<span data-ttu-id="5e8bb-107">Oggetto che corrisponde al ConflictResolutionPolicy dell'API SQL.</span><span class="sxs-lookup"><span data-stu-id="5e8bb-107">Object corresponding to Sql API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="5e8bb-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5e8bb-108">EXAMPLES</span></span>

### <span data-ttu-id="5e8bb-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5e8bb-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

<span data-ttu-id="5e8bb-110">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="5e8bb-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="5e8bb-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5e8bb-111">PARAMETERS</span></span>

### <span data-ttu-id="5e8bb-112">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="5e8bb-112">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="5e8bb-113">Da fornire quando il tipo è personalizzato.</span><span class="sxs-lookup"><span data-stu-id="5e8bb-113">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="5e8bb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e8bb-114">-DefaultProfile</span></span>
<span data-ttu-id="5e8bb-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5e8bb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e8bb-116">-Path</span><span class="sxs-lookup"><span data-stu-id="5e8bb-116">-Path</span></span>
<span data-ttu-id="5e8bb-117">Da fornire quando il tipo è LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="5e8bb-117">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="5e8bb-118">-Digitare</span><span class="sxs-lookup"><span data-stu-id="5e8bb-118">-Type</span></span>
<span data-ttu-id="5e8bb-119">Possono avere i valori: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="5e8bb-119">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="5e8bb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e8bb-120">CommonParameters</span></span>
<span data-ttu-id="5e8bb-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e8bb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e8bb-122">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e8bb-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e8bb-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5e8bb-123">INPUTS</span></span>

### <span data-ttu-id="5e8bb-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5e8bb-124">None</span></span>

## <span data-ttu-id="5e8bb-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5e8bb-125">OUTPUTS</span></span>

### <span data-ttu-id="5e8bb-126">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="5e8bb-126">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="5e8bb-127">Note</span><span class="sxs-lookup"><span data-stu-id="5e8bb-127">NOTES</span></span>

## <span data-ttu-id="5e8bb-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5e8bb-128">RELATED LINKS</span></span>
