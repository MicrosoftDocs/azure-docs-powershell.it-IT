---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: F371FD62-D138-4610-84A1-93EDC42D6AAC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: 724441a09ec2714048ec43b781f5792903bce73a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509547"
---
# <span data-ttu-id="f1b6e-101">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="f1b6e-101">Get-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="f1b6e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f1b6e-102">SYNOPSIS</span></span>
<span data-ttu-id="f1b6e-103">Ottiene gli input del processo di analisi del flusso.</span><span class="sxs-lookup"><span data-stu-id="f1b6e-103">Gets Stream Analytics job inputs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1b6e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f1b6e-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1b6e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1b6e-105">DESCRIPTION</span></span>
<span data-ttu-id="f1b6e-106">Il cmdlet **Get-AzureRmStreamAnalyticsInput** elenca tutti gli input definiti in un processo di analisi del flusso o ottiene informazioni su un input specifico.</span><span class="sxs-lookup"><span data-stu-id="f1b6e-106">The **Get-AzureRmStreamAnalyticsInput** cmdlet lists all of the inputs that are defined in a Stream Analytics job or gets information about a specific input.</span></span>

## <span data-ttu-id="f1b6e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f1b6e-107">EXAMPLES</span></span>

### <span data-ttu-id="f1b6e-108">ESEMPIO 1: ottenere informazioni sugli input definiti in un processo</span><span class="sxs-lookup"><span data-stu-id="f1b6e-108">EXAMPLE 1: Get information about the inputs defined on a job</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="f1b6e-109">Questo comando restituisce informazioni su tutti gli input definiti in Job StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="f1b6e-109">This command returns information about all the inputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="f1b6e-110">ESEMPIO 2: ottenere informazioni su un input specifico definito in un processo</span><span class="sxs-lookup"><span data-stu-id="f1b6e-110">EXAMPLE 2: Get information about a specific input defined on a job</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="f1b6e-111">Questo comando restituisce informazioni sull'input denominato EntryStream definito nel processo StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="f1b6e-111">This command returns information about the input named EntryStream defined on the job StreamingJob.</span></span>

## <span data-ttu-id="f1b6e-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f1b6e-112">PARAMETERS</span></span>

### <span data-ttu-id="f1b6e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1b6e-113">-DefaultProfile</span></span>
<span data-ttu-id="f1b6e-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f1b6e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1b6e-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="f1b6e-115">-JobName</span></span>
<span data-ttu-id="f1b6e-116">Specifica il nome del processo di analisi di Azure stream a cui appartiene l'input di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="f1b6e-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="f1b6e-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="f1b6e-117">-Name</span></span>
<span data-ttu-id="f1b6e-118">Specifica il nome dell'input di analisi di Azure Stream da recuperare.</span><span class="sxs-lookup"><span data-stu-id="f1b6e-118">Specifies the name of the Azure Stream Analytics input to retrieve.</span></span>

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

### <span data-ttu-id="f1b6e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1b6e-119">-ResourceGroupName</span></span>
<span data-ttu-id="f1b6e-120">Specifica il nome del gruppo di risorse a cui appartiene l'input di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="f1b6e-120">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="f1b6e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1b6e-121">CommonParameters</span></span>
<span data-ttu-id="f1b6e-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1b6e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1b6e-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1b6e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1b6e-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f1b6e-124">INPUTS</span></span>

### <span data-ttu-id="f1b6e-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f1b6e-125">None</span></span>
<span data-ttu-id="f1b6e-126">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="f1b6e-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f1b6e-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f1b6e-127">OUTPUTS</span></span>

### <span data-ttu-id="f1b6e-128">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. StreamAnalytics. Models. PSInput, Microsoft. Azure. Commands. StreamAnalytics]] Microsoft. Azure. Commands. StreamAnalytics. Models. PSInput</span><span class="sxs-lookup"><span data-stu-id="f1b6e-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="f1b6e-129">Note</span><span class="sxs-lookup"><span data-stu-id="f1b6e-129">NOTES</span></span>

## <span data-ttu-id="f1b6e-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f1b6e-130">RELATED LINKS</span></span>

[<span data-ttu-id="f1b6e-131">New-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="f1b6e-131">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="f1b6e-132">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="f1b6e-132">Remove-AzureRmStreamAnalyticsInput</span></span>](./Remove-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="f1b6e-133">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="f1b6e-133">Test-AzureRmStreamAnalyticsInput</span></span>](./Test-AzureRmStreamAnalyticsInput.md)


