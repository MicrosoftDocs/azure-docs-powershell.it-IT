---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1D10C1EA-632A-4953-85B1-596A45C30B24
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/get-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
ms.openlocfilehash: 26808bd3db72f8618505045b2b20f6d0b56806da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973869"
---
# <span data-ttu-id="f3da9-101">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f3da9-101">Get-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="f3da9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3da9-102">SYNOPSIS</span></span>
<span data-ttu-id="f3da9-103">Recupera informazioni sui processi di Analisi di flusso.</span><span class="sxs-lookup"><span data-stu-id="f3da9-103">Gets Stream Analytics jobs information.</span></span>

## <span data-ttu-id="f3da9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f3da9-104">SYNTAX</span></span>

### <span data-ttu-id="f3da9-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f3da9-105">ByResourceGroup</span></span>
```
Get-AzStreamAnalyticsJob [-ResourceGroupName] <String> [[-Name] <String>] [-NoExpand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3da9-106">BySubscription</span><span class="sxs-lookup"><span data-stu-id="f3da9-106">BySubscription</span></span>
```
Get-AzStreamAnalyticsJob [-NoExpand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3da9-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f3da9-107">DESCRIPTION</span></span>
<span data-ttu-id="f3da9-108">Il cmdlet **Get-AzStreamAnalyticsJob** elenca tutti i processi di Analisi di flusso definiti nella sottoscrizione di Azure o nel gruppo di risorse specificato oppure ottiene informazioni su un processo specifico all'interno di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f3da9-108">The **Get-AzStreamAnalyticsJob** cmdlet lists all Stream Analytics jobs defined in the Azure subscription or specified resource group or gets job information about a specific job within a resource group.</span></span>

## <span data-ttu-id="f3da9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f3da9-109">EXAMPLES</span></span>

### <span data-ttu-id="f3da9-110">ESEMPIO 1: Ottenere informazioni su tutti i processi di un abbonamento</span><span class="sxs-lookup"><span data-stu-id="f3da9-110">EXAMPLE 1: Get information about all jobs in a subscription</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob
```

<span data-ttu-id="f3da9-111">Questo comando restituisce informazioni su tutti i processi di Analisi di flusso nella sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f3da9-111">This command returns information about all the Stream Analytics jobs in the Azure subscription.</span></span>

### <span data-ttu-id="f3da9-112">ESEMPIO 2: Ottenere informazioni su tutti i processi in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="f3da9-112">EXAMPLE 2: Get information about all jobs in a resource group</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US"
```

<span data-ttu-id="f3da9-113">Questo comando restituisce informazioni su tutti i processi di Analisi di flusso nel gruppo di risorse StreamAnalytics-Default-West-US.</span><span class="sxs-lookup"><span data-stu-id="f3da9-113">This command returns information about all the Stream Analytics jobs in the resource group StreamAnalytics-Default-West-US.</span></span>

### <span data-ttu-id="f3da9-114">ESEMPIO 3: Ottenere informazioni su un processo specifico in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="f3da9-114">EXAMPLE 3: Get information about a specific job in a resource group</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="f3da9-115">Questo comando restituisce informazioni sul processo StreamingJob del processo Analisi di flusso nel gruppo di risorse StreamAnalytics-Default-West-US.</span><span class="sxs-lookup"><span data-stu-id="f3da9-115">This command returns information about the Stream Analytics job StreamingJob in the resource group StreamAnalytics-Default-West-US.</span></span>

## <span data-ttu-id="f3da9-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3da9-116">PARAMETERS</span></span>

### <span data-ttu-id="f3da9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3da9-117">-DefaultProfile</span></span>
<span data-ttu-id="f3da9-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f3da9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3da9-119">-Name</span><span class="sxs-lookup"><span data-stu-id="f3da9-119">-Name</span></span>
<span data-ttu-id="f3da9-120">Specifica il nome del processo di Analisi di flusso di Azure da recuperare.</span><span class="sxs-lookup"><span data-stu-id="f3da9-120">Specifies the name of the Azure Stream Analytics job to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3da9-121">-NoExpand</span><span class="sxs-lookup"><span data-stu-id="f3da9-121">-NoExpand</span></span>
<span data-ttu-id="f3da9-122">Indica che il cmdlet recupererà il processo di Analisi di flusso di Azure, ma non restituirà informazioni su input, output e trasformazione.</span><span class="sxs-lookup"><span data-stu-id="f3da9-122">Indicates the cmdlet will retrieve the Azure Stream Analytics job, but not return information on its inputs, outputs, and transformation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3da9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3da9-123">-ResourceGroupName</span></span>
<span data-ttu-id="f3da9-124">Specifica il nome del gruppo di risorse a cui appartiene il processo di Analisi di flusso di Azure.</span><span class="sxs-lookup"><span data-stu-id="f3da9-124">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3da9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3da9-125">CommonParameters</span></span>
<span data-ttu-id="f3da9-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3da9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3da9-127">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3da9-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3da9-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="f3da9-128">INPUTS</span></span>

### <span data-ttu-id="f3da9-129">System.String</span><span class="sxs-lookup"><span data-stu-id="f3da9-129">System.String</span></span>

### <span data-ttu-id="f3da9-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f3da9-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f3da9-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f3da9-131">OUTPUTS</span></span>

### <span data-ttu-id="f3da9-132">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span><span class="sxs-lookup"><span data-stu-id="f3da9-132">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="f3da9-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="f3da9-133">NOTES</span></span>

## <span data-ttu-id="f3da9-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f3da9-134">RELATED LINKS</span></span>

[<span data-ttu-id="f3da9-135">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f3da9-135">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="f3da9-136">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f3da9-136">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="f3da9-137">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f3da9-137">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="f3da9-138">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f3da9-138">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


