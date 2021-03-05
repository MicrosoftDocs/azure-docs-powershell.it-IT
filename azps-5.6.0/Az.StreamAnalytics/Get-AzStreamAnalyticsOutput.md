---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 04A6FD47-482C-4EA6-9375-D8B6FD1F2659
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/get-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 1f959f96b02296d4cc25cca06ae6c95bdef98af7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973854"
---
# <span data-ttu-id="68d76-101">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="68d76-101">Get-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="68d76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68d76-102">SYNOPSIS</span></span>
<span data-ttu-id="68d76-103">Ottiene gli output definiti in un output o in un processo di Analisi di flusso specificato.</span><span class="sxs-lookup"><span data-stu-id="68d76-103">Gets the outputs defined in a specified Stream Analytics job or output.</span></span>

## <span data-ttu-id="68d76-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="68d76-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68d76-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="68d76-105">DESCRIPTION</span></span>
<span data-ttu-id="68d76-106">Il cmdlet **Get-AzStreamAnalyticsOutput** elenca tutti gli output definiti in un processo specifico di Analisi di flusso o riceve informazioni su un output specifico.</span><span class="sxs-lookup"><span data-stu-id="68d76-106">The **Get-AzStreamAnalyticsOutput** cmdlet lists all of the outputs that are defined in a specified Stream Analytics job or gets information about a specific output.</span></span>

## <span data-ttu-id="68d76-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="68d76-107">EXAMPLES</span></span>

### <span data-ttu-id="68d76-108">Esempio 1: Ottenere informazioni sugli output di processo</span><span class="sxs-lookup"><span data-stu-id="68d76-108">Example 1: Get information about job outputs</span></span>
```powershell
PS C:\>Get-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="68d76-109">Questo comando restituisce informazioni sugli output definiti nel processo StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="68d76-109">This command returns information about the outputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="68d76-110">Esempio 2: Ottenere informazioni su un output di processo specifico</span><span class="sxs-lookup"><span data-stu-id="68d76-110">Example 2: Get information about a specific job output</span></span>
```powershell
PS C:\>Get-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="68d76-111">Questo comando restituisce informazioni sull'output denominato Output definito nel processo StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="68d76-111">This command returns information about the output named Output defined on the job StreamingJob.</span></span>

## <span data-ttu-id="68d76-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="68d76-112">PARAMETERS</span></span>

### <span data-ttu-id="68d76-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68d76-113">-DefaultProfile</span></span>
<span data-ttu-id="68d76-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="68d76-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68d76-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="68d76-115">-JobName</span></span>
<span data-ttu-id="68d76-116">Specifica il nome del processo di Analisi di flusso di Azure a cui appartiene l'output di Analisi di flusso di Azure.</span><span class="sxs-lookup"><span data-stu-id="68d76-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="68d76-117">-Name</span><span class="sxs-lookup"><span data-stu-id="68d76-117">-Name</span></span>
<span data-ttu-id="68d76-118">Specifica il nome dell'output di Analisi di flusso di Azure da recuperare.</span><span class="sxs-lookup"><span data-stu-id="68d76-118">Specifies the name of the Azure Stream Analytics output to retrieve.</span></span>

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

### <span data-ttu-id="68d76-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68d76-119">-ResourceGroupName</span></span>
<span data-ttu-id="68d76-120">Specifica il nome del gruppo di risorse a cui appartiene l'output di Analisi di flusso di Azure.</span><span class="sxs-lookup"><span data-stu-id="68d76-120">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="68d76-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68d76-121">CommonParameters</span></span>
<span data-ttu-id="68d76-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68d76-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68d76-123">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68d76-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68d76-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="68d76-124">INPUTS</span></span>

### <span data-ttu-id="68d76-125">System.String</span><span class="sxs-lookup"><span data-stu-id="68d76-125">System.String</span></span>

## <span data-ttu-id="68d76-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="68d76-126">OUTPUTS</span></span>

### <span data-ttu-id="68d76-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span><span class="sxs-lookup"><span data-stu-id="68d76-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="68d76-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="68d76-128">NOTES</span></span>

## <span data-ttu-id="68d76-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="68d76-129">RELATED LINKS</span></span>

[<span data-ttu-id="68d76-130">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="68d76-130">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="68d76-131">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="68d76-131">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="68d76-132">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="68d76-132">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


