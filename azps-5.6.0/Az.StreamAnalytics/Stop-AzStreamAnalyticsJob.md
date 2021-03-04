---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1EC96B4E-7731-4EE3-A0C1-EA0793F0FE5C
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/stop-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
ms.openlocfilehash: 2a13466b792426cdf06b7c52a8067f3adf5b787d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993144"
---
# <span data-ttu-id="94716-101">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="94716-101">Stop-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="94716-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94716-102">SYNOPSIS</span></span>
<span data-ttu-id="94716-103">Interrompe un processo di Analisi di flusso.</span><span class="sxs-lookup"><span data-stu-id="94716-103">Stops a Stream Analytics job.</span></span>

## <span data-ttu-id="94716-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="94716-104">SYNTAX</span></span>

```
Stop-AzStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94716-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="94716-105">DESCRIPTION</span></span>
<span data-ttu-id="94716-106">Il cmdlet **Stop-AzStreamAnalyticsJob** interrompe in modo asincrono l'esecuzione di un processo di Analisi di flusso in Azure e deassegna le risorse in uso.</span><span class="sxs-lookup"><span data-stu-id="94716-106">The **Stop-AzStreamAnalyticsJob** cmdlet asynchronously stops a Stream Analytics job from running in Azure and deallocates resources that were that were being used.</span></span>
<span data-ttu-id="94716-107">La definizione e i metadati del processo rimangono disponibili all'interno dell'abbonamento tramite le API portale e gestione di Azure, in modo che il processo possa essere modificato e riavviato.</span><span class="sxs-lookup"><span data-stu-id="94716-107">The job definition and metadata remain available within your subscription through both the Azure Portal and Management APIs, such that the job can be edited and restarted.</span></span>
<span data-ttu-id="94716-108">Non verrà addebitato alcun processo in stato di interruzione.</span><span class="sxs-lookup"><span data-stu-id="94716-108">You will not be charged for a job in the Stopped state.</span></span>

## <span data-ttu-id="94716-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="94716-109">EXAMPLES</span></span>

### <span data-ttu-id="94716-110">Esempio 1: Interrompere un processo in esecuzione</span><span class="sxs-lookup"><span data-stu-id="94716-110">Example 1: Stop a running job</span></span>
```powershell
PS C:\>Stop-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="94716-111">Questo comando interrompe il processo StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="94716-111">This command stops the job StreamingJob.</span></span>

## <span data-ttu-id="94716-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94716-112">PARAMETERS</span></span>

### <span data-ttu-id="94716-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94716-113">-DefaultProfile</span></span>
<span data-ttu-id="94716-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="94716-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94716-115">-Name</span><span class="sxs-lookup"><span data-stu-id="94716-115">-Name</span></span>
<span data-ttu-id="94716-116">Specifica il nome del processo di Analisi di flusso di Azure da interrompere.</span><span class="sxs-lookup"><span data-stu-id="94716-116">Specifies the name of the Azure Stream Analytics job to stop.</span></span>

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

### <span data-ttu-id="94716-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94716-117">-ResourceGroupName</span></span>
<span data-ttu-id="94716-118">Specifica il nome del gruppo di risorse a cui appartiene il processo di Analisi di flusso di Azure.</span><span class="sxs-lookup"><span data-stu-id="94716-118">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="94716-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94716-119">CommonParameters</span></span>
<span data-ttu-id="94716-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94716-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94716-121">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94716-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94716-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="94716-122">INPUTS</span></span>

### <span data-ttu-id="94716-123">System.String</span><span class="sxs-lookup"><span data-stu-id="94716-123">System.String</span></span>

## <span data-ttu-id="94716-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="94716-124">OUTPUTS</span></span>

### <span data-ttu-id="94716-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="94716-125">System.Boolean</span></span>

## <span data-ttu-id="94716-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="94716-126">NOTES</span></span>

## <span data-ttu-id="94716-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="94716-127">RELATED LINKS</span></span>

[<span data-ttu-id="94716-128">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="94716-128">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="94716-129">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="94716-129">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="94716-130">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="94716-130">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="94716-131">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="94716-131">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="94716-132">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="94716-132">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)


