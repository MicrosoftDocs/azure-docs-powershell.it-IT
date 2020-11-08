---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F371FD62-D138-4610-84A1-93EDC42D6AAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsInput.md
ms.openlocfilehash: 1f83eaf8ff358c211dbe8b83cfb99d986e56c1ed
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033613"
---
# <span data-ttu-id="a60d8-101">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="a60d8-101">Get-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="a60d8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a60d8-102">SYNOPSIS</span></span>
<span data-ttu-id="a60d8-103">Ottiene gli input del processo di analisi del flusso.</span><span class="sxs-lookup"><span data-stu-id="a60d8-103">Gets Stream Analytics job inputs.</span></span>

## <span data-ttu-id="a60d8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a60d8-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a60d8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a60d8-105">DESCRIPTION</span></span>
<span data-ttu-id="a60d8-106">Il cmdlet **Get-AzStreamAnalyticsInput** elenca tutti gli input definiti in un processo di analisi del flusso o ottiene informazioni su un input specifico.</span><span class="sxs-lookup"><span data-stu-id="a60d8-106">The **Get-AzStreamAnalyticsInput** cmdlet lists all of the inputs that are defined in a Stream Analytics job or gets information about a specific input.</span></span>

## <span data-ttu-id="a60d8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a60d8-107">EXAMPLES</span></span>

### <span data-ttu-id="a60d8-108">Esempio 1: ottenere informazioni sugli input definiti in un processo</span><span class="sxs-lookup"><span data-stu-id="a60d8-108">Example 1: Get information about the inputs defined on a job</span></span>
```powershell
PS C:\>Get-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="a60d8-109">Questo comando restituisce informazioni su tutti gli input definiti in Job StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="a60d8-109">This command returns information about all the inputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="a60d8-110">Esempio 2: ottenere informazioni su un input specifico definito in un processo</span><span class="sxs-lookup"><span data-stu-id="a60d8-110">Example 2: Get information about a specific input defined on a job</span></span>
```powershell
PS C:\>Get-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="a60d8-111">Questo comando restituisce informazioni sull'input denominato EntryStream definito nel processo StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="a60d8-111">This command returns information about the input named EntryStream defined on the job StreamingJob.</span></span>

## <span data-ttu-id="a60d8-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a60d8-112">PARAMETERS</span></span>

### <span data-ttu-id="a60d8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a60d8-113">-DefaultProfile</span></span>
<span data-ttu-id="a60d8-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a60d8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a60d8-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="a60d8-115">-JobName</span></span>
<span data-ttu-id="a60d8-116">Specifica il nome del processo di analisi di Azure stream a cui appartiene l'input di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="a60d8-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="a60d8-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="a60d8-117">-Name</span></span>
<span data-ttu-id="a60d8-118">Specifica il nome dell'input di analisi di Azure Stream da recuperare.</span><span class="sxs-lookup"><span data-stu-id="a60d8-118">Specifies the name of the Azure Stream Analytics input to retrieve.</span></span>

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

### <span data-ttu-id="a60d8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a60d8-119">-ResourceGroupName</span></span>
<span data-ttu-id="a60d8-120">Specifica il nome del gruppo di risorse a cui appartiene l'input di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="a60d8-120">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="a60d8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a60d8-121">CommonParameters</span></span>
<span data-ttu-id="a60d8-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a60d8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a60d8-123">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a60d8-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a60d8-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a60d8-124">INPUTS</span></span>

### <span data-ttu-id="a60d8-125">System. String</span><span class="sxs-lookup"><span data-stu-id="a60d8-125">System.String</span></span>

## <span data-ttu-id="a60d8-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a60d8-126">OUTPUTS</span></span>

### <span data-ttu-id="a60d8-127">Microsoft. Azure. Commands. StreamAnalytics. Models. PSInput</span><span class="sxs-lookup"><span data-stu-id="a60d8-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="a60d8-128">Note</span><span class="sxs-lookup"><span data-stu-id="a60d8-128">NOTES</span></span>

## <span data-ttu-id="a60d8-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a60d8-129">RELATED LINKS</span></span>

[<span data-ttu-id="a60d8-130">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="a60d8-130">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="a60d8-131">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="a60d8-131">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)

[<span data-ttu-id="a60d8-132">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="a60d8-132">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)


