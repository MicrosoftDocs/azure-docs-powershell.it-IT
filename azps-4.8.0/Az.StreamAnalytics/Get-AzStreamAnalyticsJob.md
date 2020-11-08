---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1D10C1EA-632A-4953-85B1-596A45C30B24
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
ms.openlocfilehash: 826089ca0db48e89138e9df78f0aa483b110ba30
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94030958"
---
# <span data-ttu-id="92e08-101">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="92e08-101">Get-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="92e08-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="92e08-102">SYNOPSIS</span></span>
<span data-ttu-id="92e08-103">Ottiene le informazioni sui processi di analisi del flusso.</span><span class="sxs-lookup"><span data-stu-id="92e08-103">Gets Stream Analytics jobs information.</span></span>

## <span data-ttu-id="92e08-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="92e08-104">SYNTAX</span></span>

### <span data-ttu-id="92e08-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="92e08-105">ByResourceGroup</span></span>
```
Get-AzStreamAnalyticsJob [-ResourceGroupName] <String> [[-Name] <String>] [-NoExpand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92e08-106">BySubscription</span><span class="sxs-lookup"><span data-stu-id="92e08-106">BySubscription</span></span>
```
Get-AzStreamAnalyticsJob [-NoExpand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92e08-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="92e08-107">DESCRIPTION</span></span>
<span data-ttu-id="92e08-108">Il cmdlet **Get-AzStreamAnalyticsJob** elenca tutti i processi di analisi dello Stream definiti nell'abbonamento di Azure o nel gruppo di risorse specificato o ottiene informazioni sul lavoro su un processo specifico all'interno di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="92e08-108">The **Get-AzStreamAnalyticsJob** cmdlet lists all Stream Analytics jobs defined in the Azure subscription or specified resource group or gets job information about a specific job within a resource group.</span></span>

## <span data-ttu-id="92e08-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="92e08-109">EXAMPLES</span></span>

### <span data-ttu-id="92e08-110">ESEMPIO 1: ottenere informazioni su tutti i processi in una sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="92e08-110">EXAMPLE 1: Get information about all jobs in a subscription</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob
```

<span data-ttu-id="92e08-111">Questo comando restituisce informazioni su tutti i processi di analisi del flusso nell'abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="92e08-111">This command returns information about all the Stream Analytics jobs in the Azure subscription.</span></span>

### <span data-ttu-id="92e08-112">ESEMPIO 2: ottenere informazioni su tutti i processi in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="92e08-112">EXAMPLE 2: Get information about all jobs in a resource group</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US"
```

<span data-ttu-id="92e08-113">Questo comando restituisce informazioni su tutti i processi di analisi del flusso nel gruppo di risorse StreamAnalytics-default-West-US.</span><span class="sxs-lookup"><span data-stu-id="92e08-113">This command returns information about all the Stream Analytics jobs in the resource group StreamAnalytics-Default-West-US.</span></span>

### <span data-ttu-id="92e08-114">ESEMPIO 3: ottenere informazioni su un processo specifico in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="92e08-114">EXAMPLE 3: Get information about a specific job in a resource group</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="92e08-115">Questo comando restituisce informazioni sul processo di analisi del flusso di lavoro di StreamingJob nel gruppo di risorse StreamAnalytics-default-West-US.</span><span class="sxs-lookup"><span data-stu-id="92e08-115">This command returns information about the Stream Analytics job StreamingJob in the resource group StreamAnalytics-Default-West-US.</span></span>

## <span data-ttu-id="92e08-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="92e08-116">PARAMETERS</span></span>

### <span data-ttu-id="92e08-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92e08-117">-DefaultProfile</span></span>
<span data-ttu-id="92e08-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="92e08-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92e08-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="92e08-119">-Name</span></span>
<span data-ttu-id="92e08-120">Specifica il nome del processo di analisi di Azure Stream da recuperare.</span><span class="sxs-lookup"><span data-stu-id="92e08-120">Specifies the name of the Azure Stream Analytics job to retrieve.</span></span>

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

### <span data-ttu-id="92e08-121">-NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="92e08-121">-NoExpand</span></span>
<span data-ttu-id="92e08-122">Indica che il cmdlet recupererà il processo di analisi di Azure Stream, ma non restituirà informazioni sugli input, gli output e la trasformazione.</span><span class="sxs-lookup"><span data-stu-id="92e08-122">Indicates the cmdlet will retrieve the Azure Stream Analytics job, but not return information on its inputs, outputs, and transformation.</span></span>

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

### <span data-ttu-id="92e08-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92e08-123">-ResourceGroupName</span></span>
<span data-ttu-id="92e08-124">Specifica il nome del gruppo di risorse a cui appartiene il processo di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="92e08-124">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="92e08-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92e08-125">CommonParameters</span></span>
<span data-ttu-id="92e08-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92e08-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92e08-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92e08-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92e08-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="92e08-128">INPUTS</span></span>

### <span data-ttu-id="92e08-129">System. String</span><span class="sxs-lookup"><span data-stu-id="92e08-129">System.String</span></span>

### <span data-ttu-id="92e08-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="92e08-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="92e08-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="92e08-131">OUTPUTS</span></span>

### <span data-ttu-id="92e08-132">Microsoft. Azure. Commands. StreamAnalytics. Models. PSJob</span><span class="sxs-lookup"><span data-stu-id="92e08-132">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="92e08-133">Note</span><span class="sxs-lookup"><span data-stu-id="92e08-133">NOTES</span></span>

## <span data-ttu-id="92e08-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="92e08-134">RELATED LINKS</span></span>

[<span data-ttu-id="92e08-135">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="92e08-135">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="92e08-136">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="92e08-136">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="92e08-137">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="92e08-137">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="92e08-138">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="92e08-138">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


