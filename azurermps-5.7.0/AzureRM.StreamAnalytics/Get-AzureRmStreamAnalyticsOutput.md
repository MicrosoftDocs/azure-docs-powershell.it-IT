---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 04A6FD47-482C-4EA6-9375-D8B6FD1F2659
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: ff9ab6f4efe5794b3f1eca9b8ceab91b5cd11316
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517832"
---
# <span data-ttu-id="6b265-101">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="6b265-101">Get-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="6b265-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6b265-102">SYNOPSIS</span></span>
<span data-ttu-id="6b265-103">Ottiene gli output definiti in un processo o in un output di analisi dello Stream specificato.</span><span class="sxs-lookup"><span data-stu-id="6b265-103">Gets the outputs defined in a specified Stream Analytics job or output.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b265-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6b265-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b265-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6b265-105">DESCRIPTION</span></span>
<span data-ttu-id="6b265-106">Il cmdlet **Get-AzureRmStreamAnalyticsOutput** elenca tutti gli output definiti in un processo di analisi dello Stream specificato o ottiene informazioni su un output specifico.</span><span class="sxs-lookup"><span data-stu-id="6b265-106">The **Get-AzureRmStreamAnalyticsOutput** cmdlet lists all of the outputs that are defined in a specified Stream Analytics job or gets information about a specific output.</span></span>

## <span data-ttu-id="6b265-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6b265-107">EXAMPLES</span></span>

### <span data-ttu-id="6b265-108">ESEMPIO 1: ottenere informazioni sugli output dei processi</span><span class="sxs-lookup"><span data-stu-id="6b265-108">EXAMPLE 1: Get information about job outputs</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="6b265-109">Questo comando restituisce informazioni sugli output definiti in Job StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="6b265-109">This command returns information about the outputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="6b265-110">ESEMPIO 2: ottenere informazioni su un output di processo specifico</span><span class="sxs-lookup"><span data-stu-id="6b265-110">EXAMPLE 2: Get information about a specific job output</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="6b265-111">Questo comando restituisce informazioni sull'output denominato output definito in Job StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="6b265-111">This command returns information about the output named Output defined on the job StreamingJob.</span></span>

## <span data-ttu-id="6b265-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6b265-112">PARAMETERS</span></span>

### <span data-ttu-id="6b265-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b265-113">-DefaultProfile</span></span>
<span data-ttu-id="6b265-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6b265-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b265-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="6b265-115">-JobName</span></span>
<span data-ttu-id="6b265-116">Specifica il nome del processo di analisi di Azure stream a cui appartiene l'output di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="6b265-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b265-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="6b265-117">-Name</span></span>
<span data-ttu-id="6b265-118">Specifica il nome dell'output di analisi di Azure Stream da recuperare.</span><span class="sxs-lookup"><span data-stu-id="6b265-118">Specifies the name of the Azure Stream Analytics output to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b265-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b265-119">-ResourceGroupName</span></span>
<span data-ttu-id="6b265-120">Specifica il nome del gruppo di risorse a cui appartiene l'output di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="6b265-120">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b265-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b265-121">CommonParameters</span></span>
<span data-ttu-id="6b265-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b265-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b265-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b265-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b265-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6b265-124">INPUTS</span></span>

### <span data-ttu-id="6b265-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6b265-125">None</span></span>
<span data-ttu-id="6b265-126">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="6b265-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6b265-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6b265-127">OUTPUTS</span></span>

### <span data-ttu-id="6b265-128">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. StreamAnalytics. Models. PSOutput, Microsoft. Azure. Commands. StreamAnalytics]] Microsoft. Azure. Commands. StreamAnalytics. Models. PSOutput</span><span class="sxs-lookup"><span data-stu-id="6b265-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="6b265-129">Note</span><span class="sxs-lookup"><span data-stu-id="6b265-129">NOTES</span></span>

## <span data-ttu-id="6b265-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6b265-130">RELATED LINKS</span></span>

[<span data-ttu-id="6b265-131">New-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="6b265-131">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="6b265-132">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="6b265-132">Remove-AzureRmStreamAnalyticsOutput</span></span>](./Remove-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="6b265-133">Test-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="6b265-133">Test-AzureRmStreamAnalyticsOutput</span></span>](./Test-AzureRmStreamAnalyticsOutput.md)


