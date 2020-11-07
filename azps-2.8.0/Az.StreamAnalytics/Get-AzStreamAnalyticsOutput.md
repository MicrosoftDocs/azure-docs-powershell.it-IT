---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 04A6FD47-482C-4EA6-9375-D8B6FD1F2659
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsOutput.md
ms.openlocfilehash: bf4a8734304ce92dac1bc329d6ae0ffa0f30c09c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854462"
---
# <span data-ttu-id="e6e28-101">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="e6e28-101">Get-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="e6e28-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e6e28-102">SYNOPSIS</span></span>
<span data-ttu-id="e6e28-103">Ottiene gli output definiti in un processo o in un output di analisi dello Stream specificato.</span><span class="sxs-lookup"><span data-stu-id="e6e28-103">Gets the outputs defined in a specified Stream Analytics job or output.</span></span>

## <span data-ttu-id="e6e28-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e6e28-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6e28-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e6e28-105">DESCRIPTION</span></span>
<span data-ttu-id="e6e28-106">Il cmdlet **Get-AzStreamAnalyticsOutput** elenca tutti gli output definiti in un processo di analisi dello Stream specificato o ottiene informazioni su un output specifico.</span><span class="sxs-lookup"><span data-stu-id="e6e28-106">The **Get-AzStreamAnalyticsOutput** cmdlet lists all of the outputs that are defined in a specified Stream Analytics job or gets information about a specific output.</span></span>

## <span data-ttu-id="e6e28-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e6e28-107">EXAMPLES</span></span>

### <span data-ttu-id="e6e28-108">ESEMPIO 1: ottenere informazioni sugli output dei processi</span><span class="sxs-lookup"><span data-stu-id="e6e28-108">EXAMPLE 1: Get information about job outputs</span></span>
```
PS C:\>Get-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="e6e28-109">Questo comando restituisce informazioni sugli output definiti in Job StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="e6e28-109">This command returns information about the outputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="e6e28-110">ESEMPIO 2: ottenere informazioni su un output di processo specifico</span><span class="sxs-lookup"><span data-stu-id="e6e28-110">EXAMPLE 2: Get information about a specific job output</span></span>
```
PS C:\>Get-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="e6e28-111">Questo comando restituisce informazioni sull'output denominato output definito in Job StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="e6e28-111">This command returns information about the output named Output defined on the job StreamingJob.</span></span>

## <span data-ttu-id="e6e28-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e6e28-112">PARAMETERS</span></span>

### <span data-ttu-id="e6e28-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6e28-113">-DefaultProfile</span></span>
<span data-ttu-id="e6e28-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e6e28-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6e28-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="e6e28-115">-JobName</span></span>
<span data-ttu-id="e6e28-116">Specifica il nome del processo di analisi di Azure stream a cui appartiene l'output di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="e6e28-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="e6e28-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="e6e28-117">-Name</span></span>
<span data-ttu-id="e6e28-118">Specifica il nome dell'output di analisi di Azure Stream da recuperare.</span><span class="sxs-lookup"><span data-stu-id="e6e28-118">Specifies the name of the Azure Stream Analytics output to retrieve.</span></span>

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

### <span data-ttu-id="e6e28-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6e28-119">-ResourceGroupName</span></span>
<span data-ttu-id="e6e28-120">Specifica il nome del gruppo di risorse a cui appartiene l'output di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="e6e28-120">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="e6e28-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6e28-121">CommonParameters</span></span>
<span data-ttu-id="e6e28-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6e28-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6e28-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6e28-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6e28-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e6e28-124">INPUTS</span></span>

### <span data-ttu-id="e6e28-125">System. String</span><span class="sxs-lookup"><span data-stu-id="e6e28-125">System.String</span></span>

## <span data-ttu-id="e6e28-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e6e28-126">OUTPUTS</span></span>

### <span data-ttu-id="e6e28-127">Microsoft. Azure. Commands. StreamAnalytics. Models. PSOutput</span><span class="sxs-lookup"><span data-stu-id="e6e28-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="e6e28-128">Note</span><span class="sxs-lookup"><span data-stu-id="e6e28-128">NOTES</span></span>

## <span data-ttu-id="e6e28-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e6e28-129">RELATED LINKS</span></span>

[<span data-ttu-id="e6e28-130">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="e6e28-130">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="e6e28-131">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="e6e28-131">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="e6e28-132">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="e6e28-132">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


