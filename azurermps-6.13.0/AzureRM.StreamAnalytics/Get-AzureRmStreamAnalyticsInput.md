---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: F371FD62-D138-4610-84A1-93EDC42D6AAC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: 8b63dbd497edce422fc4cf70182ca8259721d8d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507284"
---
# <span data-ttu-id="6cf6b-101">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="6cf6b-101">Get-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="6cf6b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6cf6b-102">SYNOPSIS</span></span>
<span data-ttu-id="6cf6b-103">Ottiene gli input del processo di analisi del flusso.</span><span class="sxs-lookup"><span data-stu-id="6cf6b-103">Gets Stream Analytics job inputs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6cf6b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6cf6b-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6cf6b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6cf6b-105">DESCRIPTION</span></span>
<span data-ttu-id="6cf6b-106">Il cmdlet **Get-AzureRmStreamAnalyticsInput** elenca tutti gli input definiti in un processo di analisi del flusso o ottiene informazioni su un input specifico.</span><span class="sxs-lookup"><span data-stu-id="6cf6b-106">The **Get-AzureRmStreamAnalyticsInput** cmdlet lists all of the inputs that are defined in a Stream Analytics job or gets information about a specific input.</span></span>

## <span data-ttu-id="6cf6b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6cf6b-107">EXAMPLES</span></span>

### <span data-ttu-id="6cf6b-108">ESEMPIO 1: ottenere informazioni sugli input definiti in un processo</span><span class="sxs-lookup"><span data-stu-id="6cf6b-108">EXAMPLE 1: Get information about the inputs defined on a job</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="6cf6b-109">Questo comando restituisce informazioni su tutti gli input definiti in Job StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="6cf6b-109">This command returns information about all the inputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="6cf6b-110">ESEMPIO 2: ottenere informazioni su un input specifico definito in un processo</span><span class="sxs-lookup"><span data-stu-id="6cf6b-110">EXAMPLE 2: Get information about a specific input defined on a job</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="6cf6b-111">Questo comando restituisce informazioni sull'input denominato EntryStream definito nel processo StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="6cf6b-111">This command returns information about the input named EntryStream defined on the job StreamingJob.</span></span>

## <span data-ttu-id="6cf6b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6cf6b-112">PARAMETERS</span></span>

### <span data-ttu-id="6cf6b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cf6b-113">-DefaultProfile</span></span>
<span data-ttu-id="6cf6b-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6cf6b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cf6b-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="6cf6b-115">-JobName</span></span>
<span data-ttu-id="6cf6b-116">Specifica il nome del processo di analisi di Azure stream a cui appartiene l'input di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="6cf6b-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="6cf6b-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="6cf6b-117">-Name</span></span>
<span data-ttu-id="6cf6b-118">Specifica il nome dell'input di analisi di Azure Stream da recuperare.</span><span class="sxs-lookup"><span data-stu-id="6cf6b-118">Specifies the name of the Azure Stream Analytics input to retrieve.</span></span>

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

### <span data-ttu-id="6cf6b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cf6b-119">-ResourceGroupName</span></span>
<span data-ttu-id="6cf6b-120">Specifica il nome del gruppo di risorse a cui appartiene l'input di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="6cf6b-120">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="6cf6b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cf6b-121">CommonParameters</span></span>
<span data-ttu-id="6cf6b-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cf6b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cf6b-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cf6b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cf6b-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6cf6b-124">INPUTS</span></span>

### <span data-ttu-id="6cf6b-125">System. String</span><span class="sxs-lookup"><span data-stu-id="6cf6b-125">System.String</span></span>

## <span data-ttu-id="6cf6b-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6cf6b-126">OUTPUTS</span></span>

### <span data-ttu-id="6cf6b-127">Microsoft. Azure. Commands. StreamAnalytics. Models. PSInput</span><span class="sxs-lookup"><span data-stu-id="6cf6b-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="6cf6b-128">Note</span><span class="sxs-lookup"><span data-stu-id="6cf6b-128">NOTES</span></span>

## <span data-ttu-id="6cf6b-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6cf6b-129">RELATED LINKS</span></span>

[<span data-ttu-id="6cf6b-130">New-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="6cf6b-130">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="6cf6b-131">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="6cf6b-131">Remove-AzureRmStreamAnalyticsInput</span></span>](./Remove-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="6cf6b-132">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="6cf6b-132">Test-AzureRmStreamAnalyticsInput</span></span>](./Test-AzureRmStreamAnalyticsInput.md)


