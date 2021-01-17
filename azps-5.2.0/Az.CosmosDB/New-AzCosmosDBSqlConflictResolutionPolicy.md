---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
ms.openlocfilehash: b11142be65935522a73d3a068be0ee329994e2ee
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334663"
---
# <span data-ttu-id="ea273-101">New-AzCosmosDBSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="ea273-101">New-AzCosmosDBSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="ea273-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ea273-102">SYNOPSIS</span></span>
<span data-ttu-id="ea273-103">Crea un nuovo oggetto di tipo PSSqlConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="ea273-103">Creates a new object of type PSSqlConflictResolutionPolicy.</span></span> <span data-ttu-id="ea273-104">Può essere passato come valore di parametro per set-AzCosmosDBSqlContainer.</span><span class="sxs-lookup"><span data-stu-id="ea273-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="ea273-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ea273-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea273-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ea273-106">DESCRIPTION</span></span>
<span data-ttu-id="ea273-107">Oggetto che corrisponde al ConflictResolutionPolicy dell'API SQL.</span><span class="sxs-lookup"><span data-stu-id="ea273-107">Object corresponding to Sql API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="ea273-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ea273-108">EXAMPLES</span></span>

### <span data-ttu-id="ea273-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ea273-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

<span data-ttu-id="ea273-110">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="ea273-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="ea273-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ea273-111">PARAMETERS</span></span>

### <span data-ttu-id="ea273-112">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="ea273-112">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="ea273-113">Da fornire quando il tipo è personalizzato.</span><span class="sxs-lookup"><span data-stu-id="ea273-113">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="ea273-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea273-114">-DefaultProfile</span></span>
<span data-ttu-id="ea273-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ea273-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea273-116">-Path</span><span class="sxs-lookup"><span data-stu-id="ea273-116">-Path</span></span>
<span data-ttu-id="ea273-117">Da fornire quando il tipo è LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="ea273-117">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="ea273-118">-Digitare</span><span class="sxs-lookup"><span data-stu-id="ea273-118">-Type</span></span>
<span data-ttu-id="ea273-119">Possono avere i valori: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="ea273-119">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="ea273-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea273-120">CommonParameters</span></span>
<span data-ttu-id="ea273-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea273-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea273-122">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea273-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea273-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ea273-123">INPUTS</span></span>

### <span data-ttu-id="ea273-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ea273-124">None</span></span>

## <span data-ttu-id="ea273-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ea273-125">OUTPUTS</span></span>

### <span data-ttu-id="ea273-126">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="ea273-126">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="ea273-127">Note</span><span class="sxs-lookup"><span data-stu-id="ea273-127">NOTES</span></span>

## <span data-ttu-id="ea273-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ea273-128">RELATED LINKS</span></span>
