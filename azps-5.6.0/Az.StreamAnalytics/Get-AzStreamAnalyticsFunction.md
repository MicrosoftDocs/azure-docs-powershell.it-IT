---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 7F08A880-1FC5-4542-8AB8-927BB999A552
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/get-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsFunction.md
ms.openlocfilehash: 681782db0e1621e8d1126ca1f3425ce87e8e30d4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973918"
---
# <span data-ttu-id="6c7ca-101">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="6c7ca-101">Get-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="6c7ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c7ca-102">SYNOPSIS</span></span>
<span data-ttu-id="6c7ca-103">Ottiene funzioni in un processo di Analisi di flusso.</span><span class="sxs-lookup"><span data-stu-id="6c7ca-103">Gets functions in a Stream Analytics job.</span></span>

## <span data-ttu-id="6c7ca-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6c7ca-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c7ca-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6c7ca-105">DESCRIPTION</span></span>
<span data-ttu-id="6c7ca-106">Il cmdlet **Get-AzStreamAnalyticsFunction** ottiene un elenco delle funzioni definite in un processo di Analisi di flusso di Azure o informazioni su una funzione specifica.</span><span class="sxs-lookup"><span data-stu-id="6c7ca-106">The **Get-AzStreamAnalyticsFunction** cmdlet gets a list of the functions that are defined in an Azure Stream Analytics job or information about a specific function.</span></span>

## <span data-ttu-id="6c7ca-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6c7ca-107">EXAMPLES</span></span>

### <span data-ttu-id="6c7ca-108">Esempio 1: Ottenere tutte le funzioni di Analisi di flusso</span><span class="sxs-lookup"><span data-stu-id="6c7ca-108">Example 1: Get all Stream Analytics functions</span></span>
```
PS C:\>Get-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22"
```

<span data-ttu-id="6c7ca-109">Questo comando ottiene le funzioni definite nel processo denominato StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="6c7ca-109">This command gets the functions defined on the job named StreamJob22.</span></span>

### <span data-ttu-id="6c7ca-110">Esempio 2: Ottenere una funzione specifica di Analisi di flusso</span><span class="sxs-lookup"><span data-stu-id="6c7ca-110">Example 2: Get a specific Stream Analytics function</span></span>
```
PS C:\>Get-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="6c7ca-111">Questo comando recupera informazioni sulla funzione denominata ScoreTweet definita nel processo denominato StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="6c7ca-111">This command gets information about the function named ScoreTweet defined on the job named StreamJob22.</span></span>

## <span data-ttu-id="6c7ca-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c7ca-112">PARAMETERS</span></span>

### <span data-ttu-id="6c7ca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c7ca-113">-DefaultProfile</span></span>
<span data-ttu-id="6c7ca-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6c7ca-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c7ca-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="6c7ca-115">-JobName</span></span>
<span data-ttu-id="6c7ca-116">Specifica il nome del processo di Analisi di flusso a cui appartengono le funzioni.</span><span class="sxs-lookup"><span data-stu-id="6c7ca-116">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="6c7ca-117">Questo cmdlet ottiene le funzioni per il processo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="6c7ca-117">This cmdlet gets functions for the job that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c7ca-118">-Name</span><span class="sxs-lookup"><span data-stu-id="6c7ca-118">-Name</span></span>
<span data-ttu-id="6c7ca-119">Specifica il nome della funzione Di analisi di flusso recuperata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c7ca-119">Specifies the name of the Stream Analytics function that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c7ca-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c7ca-120">-ResourceGroupName</span></span>
<span data-ttu-id="6c7ca-121">Specifica il nome del gruppo di risorse a cui appartengono le funzioni di Analisi di flusso.</span><span class="sxs-lookup"><span data-stu-id="6c7ca-121">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="6c7ca-122">Questo cmdlet ottiene le funzioni per il gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="6c7ca-122">This cmdlet gets functions for the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c7ca-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c7ca-123">CommonParameters</span></span>
<span data-ttu-id="6c7ca-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c7ca-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c7ca-125">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c7ca-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c7ca-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="6c7ca-126">INPUTS</span></span>

### <span data-ttu-id="6c7ca-127">System.String</span><span class="sxs-lookup"><span data-stu-id="6c7ca-127">System.String</span></span>

## <span data-ttu-id="6c7ca-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6c7ca-128">OUTPUTS</span></span>

### <span data-ttu-id="6c7ca-129">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span><span class="sxs-lookup"><span data-stu-id="6c7ca-129">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="6c7ca-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="6c7ca-130">NOTES</span></span>

## <span data-ttu-id="6c7ca-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6c7ca-131">RELATED LINKS</span></span>

[<span data-ttu-id="6c7ca-132">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="6c7ca-132">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="6c7ca-133">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="6c7ca-133">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="6c7ca-134">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="6c7ca-134">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)


