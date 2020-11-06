---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 1D10C1EA-632A-4953-85B1-596A45C30B24
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: a2bf5146958e10dc60c656f08a329d2ec01d1eeb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512132"
---
# <span data-ttu-id="c7a4f-101">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c7a4f-101">Get-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="c7a4f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c7a4f-102">SYNOPSIS</span></span>
<span data-ttu-id="c7a4f-103">Ottiene le informazioni sui processi di analisi del flusso.</span><span class="sxs-lookup"><span data-stu-id="c7a4f-103">Gets Stream Analytics jobs information.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7a4f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c7a4f-104">SYNTAX</span></span>

### <span data-ttu-id="c7a4f-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c7a4f-105">ByResourceGroup</span></span>
```
Get-AzureRmStreamAnalyticsJob [-ResourceGroupName] <String> [[-Name] <String>] [-NoExpand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7a4f-106">BySubscription</span><span class="sxs-lookup"><span data-stu-id="c7a4f-106">BySubscription</span></span>
```
Get-AzureRmStreamAnalyticsJob [-NoExpand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7a4f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c7a4f-107">DESCRIPTION</span></span>
<span data-ttu-id="c7a4f-108">Il cmdlet **Get-AzureRmStreamAnalyticsJob** elenca tutti i processi di analisi dello Stream definiti nell'abbonamento di Azure o nel gruppo di risorse specificato o ottiene informazioni sul lavoro su un processo specifico all'interno di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c7a4f-108">The **Get-AzureRmStreamAnalyticsJob** cmdlet lists all Stream Analytics jobs defined in the Azure subscription or specified resource group or gets job information about a specific job within a resource group.</span></span>

## <span data-ttu-id="c7a4f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c7a4f-109">EXAMPLES</span></span>

### <span data-ttu-id="c7a4f-110">ESEMPIO 1: ottenere informazioni su tutti i processi in una sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="c7a4f-110">EXAMPLE 1: Get information about all jobs in a subscription</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsJob
```

<span data-ttu-id="c7a4f-111">Questo comando restituisce informazioni su tutti i processi di analisi del flusso nell'abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="c7a4f-111">This command returns information about all the Stream Analytics jobs in the Azure subscription.</span></span>

### <span data-ttu-id="c7a4f-112">ESEMPIO 2: ottenere informazioni su tutti i processi in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="c7a4f-112">EXAMPLE 2: Get information about all jobs in a resource group</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US"
```

<span data-ttu-id="c7a4f-113">Questo comando restituisce informazioni su tutti i processi di analisi del flusso nel gruppo di risorse StreamAnalytics-default-West-US.</span><span class="sxs-lookup"><span data-stu-id="c7a4f-113">This command returns information about all the Stream Analytics jobs in the resource group StreamAnalytics-Default-West-US.</span></span>

### <span data-ttu-id="c7a4f-114">ESEMPIO 3: ottenere informazioni su un processo specifico in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="c7a4f-114">EXAMPLE 3: Get information about a specific job in a resource group</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="c7a4f-115">Questo comando restituisce informazioni sul processo di analisi del flusso di lavoro di StreamingJob nel gruppo di risorse StreamAnalytics-default-West-US.</span><span class="sxs-lookup"><span data-stu-id="c7a4f-115">This command returns information about the Stream Analytics job StreamingJob in the resource group StreamAnalytics-Default-West-US.</span></span>

## <span data-ttu-id="c7a4f-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c7a4f-116">PARAMETERS</span></span>

### <span data-ttu-id="c7a4f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7a4f-117">-DefaultProfile</span></span>
<span data-ttu-id="c7a4f-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c7a4f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7a4f-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="c7a4f-119">-Name</span></span>
<span data-ttu-id="c7a4f-120">Specifica il nome del processo di analisi di Azure Stream da recuperare.</span><span class="sxs-lookup"><span data-stu-id="c7a4f-120">Specifies the name of the Azure Stream Analytics job to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7a4f-121">-NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="c7a4f-121">-NoExpand</span></span>
<span data-ttu-id="c7a4f-122">Indica che il cmdlet recupererà il processo di analisi di Azure Stream, ma non restituirà informazioni sugli input, gli output e la trasformazione.</span><span class="sxs-lookup"><span data-stu-id="c7a4f-122">Indicates the cmdlet will retrieve the Azure Stream Analytics job, but not return information on its inputs, outputs, and transformation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7a4f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7a4f-123">-ResourceGroupName</span></span>
<span data-ttu-id="c7a4f-124">Specifica il nome del gruppo di risorse a cui appartiene il processo di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="c7a4f-124">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7a4f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7a4f-125">CommonParameters</span></span>
<span data-ttu-id="c7a4f-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7a4f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7a4f-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7a4f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7a4f-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c7a4f-128">INPUTS</span></span>

### <span data-ttu-id="c7a4f-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c7a4f-129">None</span></span>
<span data-ttu-id="c7a4f-130">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="c7a4f-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c7a4f-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c7a4f-131">OUTPUTS</span></span>

### <span data-ttu-id="c7a4f-132">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. StreamAnalytics. Models. PSJob, Microsoft. Azure. Commands. StreamAnalytics]] Microsoft. Azure. Commands. StreamAnalytics. Models. PSJob</span><span class="sxs-lookup"><span data-stu-id="c7a4f-132">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="c7a4f-133">Note</span><span class="sxs-lookup"><span data-stu-id="c7a4f-133">NOTES</span></span>

## <span data-ttu-id="c7a4f-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c7a4f-134">RELATED LINKS</span></span>

[<span data-ttu-id="c7a4f-135">New-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c7a4f-135">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="c7a4f-136">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c7a4f-136">Remove-AzureRmStreamAnalyticsJob</span></span>](./Remove-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="c7a4f-137">Start-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c7a4f-137">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="c7a4f-138">Stop-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c7a4f-138">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)


