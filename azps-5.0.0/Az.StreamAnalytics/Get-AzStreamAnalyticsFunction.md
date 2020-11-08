---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 7F08A880-1FC5-4542-8AB8-927BB999A552
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsFunction.md
ms.openlocfilehash: ceedee89473385202037cfedb23e4373995b6f98
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200077"
---
# <span data-ttu-id="fde3f-101">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="fde3f-101">Get-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="fde3f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fde3f-102">SYNOPSIS</span></span>
<span data-ttu-id="fde3f-103">Ottiene funzioni in un processo di analisi del flusso.</span><span class="sxs-lookup"><span data-stu-id="fde3f-103">Gets functions in a Stream Analytics job.</span></span>

## <span data-ttu-id="fde3f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fde3f-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fde3f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fde3f-105">DESCRIPTION</span></span>
<span data-ttu-id="fde3f-106">Il cmdlet **Get-AzStreamAnalyticsFunction** ottiene un elenco delle funzioni definite in un processo di analisi di Azure Stream o informazioni su una funzione specifica.</span><span class="sxs-lookup"><span data-stu-id="fde3f-106">The **Get-AzStreamAnalyticsFunction** cmdlet gets a list of the functions that are defined in an Azure Stream Analytics job or information about a specific function.</span></span>

## <span data-ttu-id="fde3f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fde3f-107">EXAMPLES</span></span>

### <span data-ttu-id="fde3f-108">Esempio 1: ottenere tutte le funzioni di analisi dello stream</span><span class="sxs-lookup"><span data-stu-id="fde3f-108">Example 1: Get all Stream Analytics functions</span></span>
```
PS C:\>Get-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22"
```

<span data-ttu-id="fde3f-109">Questo comando consente di ottenere le funzioni definite nel processo denominato StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="fde3f-109">This command gets the functions defined on the job named StreamJob22.</span></span>

### <span data-ttu-id="fde3f-110">Esempio 2: ottenere una specifica funzione di analisi del flusso</span><span class="sxs-lookup"><span data-stu-id="fde3f-110">Example 2: Get a specific Stream Analytics function</span></span>
```
PS C:\>Get-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="fde3f-111">Questo comando ottiene le informazioni sulla funzione denominata ScoreTweet definita nel processo denominato StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="fde3f-111">This command gets information about the function named ScoreTweet defined on the job named StreamJob22.</span></span>

## <span data-ttu-id="fde3f-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fde3f-112">PARAMETERS</span></span>

### <span data-ttu-id="fde3f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fde3f-113">-DefaultProfile</span></span>
<span data-ttu-id="fde3f-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fde3f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fde3f-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="fde3f-115">-JobName</span></span>
<span data-ttu-id="fde3f-116">Specifica il nome del processo di analisi del flusso a cui appartengono le funzioni.</span><span class="sxs-lookup"><span data-stu-id="fde3f-116">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="fde3f-117">Questo cmdlet ottiene le funzioni per il processo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="fde3f-117">This cmdlet gets functions for the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="fde3f-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="fde3f-118">-Name</span></span>
<span data-ttu-id="fde3f-119">Specifica il nome della funzione flusso di analisi che questo cmdlet ottiene.</span><span class="sxs-lookup"><span data-stu-id="fde3f-119">Specifies the name of the Stream Analytics function that this cmdlet gets.</span></span>

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

### <span data-ttu-id="fde3f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fde3f-120">-ResourceGroupName</span></span>
<span data-ttu-id="fde3f-121">Specifica il nome del gruppo di risorse a cui appartiene le funzioni di analisi flusso.</span><span class="sxs-lookup"><span data-stu-id="fde3f-121">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="fde3f-122">Questo cmdlet ottiene le funzioni per il gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="fde3f-122">This cmdlet gets functions for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="fde3f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fde3f-123">CommonParameters</span></span>
<span data-ttu-id="fde3f-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fde3f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fde3f-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fde3f-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fde3f-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fde3f-126">INPUTS</span></span>

### <span data-ttu-id="fde3f-127">System. String</span><span class="sxs-lookup"><span data-stu-id="fde3f-127">System.String</span></span>

## <span data-ttu-id="fde3f-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fde3f-128">OUTPUTS</span></span>

### <span data-ttu-id="fde3f-129">Microsoft. Azure. Commands. StreamAnalytics. Models. PSFunction</span><span class="sxs-lookup"><span data-stu-id="fde3f-129">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="fde3f-130">Note</span><span class="sxs-lookup"><span data-stu-id="fde3f-130">NOTES</span></span>

## <span data-ttu-id="fde3f-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fde3f-131">RELATED LINKS</span></span>

[<span data-ttu-id="fde3f-132">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="fde3f-132">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="fde3f-133">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="fde3f-133">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="fde3f-134">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="fde3f-134">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)

