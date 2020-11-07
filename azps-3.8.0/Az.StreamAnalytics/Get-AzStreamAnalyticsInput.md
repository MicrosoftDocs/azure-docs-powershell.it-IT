---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F371FD62-D138-4610-84A1-93EDC42D6AAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsInput.md
ms.openlocfilehash: ba64089da3673957eead10ef1301f5c7c4a59467
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93865429"
---
# <span data-ttu-id="0a6a3-101">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="0a6a3-101">Get-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="0a6a3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0a6a3-102">SYNOPSIS</span></span>
<span data-ttu-id="0a6a3-103">Ottiene gli input del processo di analisi del flusso.</span><span class="sxs-lookup"><span data-stu-id="0a6a3-103">Gets Stream Analytics job inputs.</span></span>

## <span data-ttu-id="0a6a3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0a6a3-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a6a3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0a6a3-105">DESCRIPTION</span></span>
<span data-ttu-id="0a6a3-106">Il cmdlet **Get-AzStreamAnalyticsInput** elenca tutti gli input definiti in un processo di analisi del flusso o ottiene informazioni su un input specifico.</span><span class="sxs-lookup"><span data-stu-id="0a6a3-106">The **Get-AzStreamAnalyticsInput** cmdlet lists all of the inputs that are defined in a Stream Analytics job or gets information about a specific input.</span></span>

## <span data-ttu-id="0a6a3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0a6a3-107">EXAMPLES</span></span>

### <span data-ttu-id="0a6a3-108">ESEMPIO 1: ottenere informazioni sugli input definiti in un processo</span><span class="sxs-lookup"><span data-stu-id="0a6a3-108">EXAMPLE 1: Get information about the inputs defined on a job</span></span>
```
PS C:\>Get-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="0a6a3-109">Questo comando restituisce informazioni su tutti gli input definiti in Job StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="0a6a3-109">This command returns information about all the inputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="0a6a3-110">ESEMPIO 2: ottenere informazioni su un input specifico definito in un processo</span><span class="sxs-lookup"><span data-stu-id="0a6a3-110">EXAMPLE 2: Get information about a specific input defined on a job</span></span>
```
PS C:\>Get-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="0a6a3-111">Questo comando restituisce informazioni sull'input denominato EntryStream definito nel processo StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="0a6a3-111">This command returns information about the input named EntryStream defined on the job StreamingJob.</span></span>

## <span data-ttu-id="0a6a3-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0a6a3-112">PARAMETERS</span></span>

### <span data-ttu-id="0a6a3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a6a3-113">-DefaultProfile</span></span>
<span data-ttu-id="0a6a3-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0a6a3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a6a3-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="0a6a3-115">-JobName</span></span>
<span data-ttu-id="0a6a3-116">Specifica il nome del processo di analisi di Azure stream a cui appartiene l'input di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="0a6a3-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="0a6a3-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="0a6a3-117">-Name</span></span>
<span data-ttu-id="0a6a3-118">Specifica il nome dell'input di analisi di Azure Stream da recuperare.</span><span class="sxs-lookup"><span data-stu-id="0a6a3-118">Specifies the name of the Azure Stream Analytics input to retrieve.</span></span>

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

### <span data-ttu-id="0a6a3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a6a3-119">-ResourceGroupName</span></span>
<span data-ttu-id="0a6a3-120">Specifica il nome del gruppo di risorse a cui appartiene l'input di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="0a6a3-120">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="0a6a3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a6a3-121">CommonParameters</span></span>
<span data-ttu-id="0a6a3-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a6a3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a6a3-123">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a6a3-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a6a3-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0a6a3-124">INPUTS</span></span>

### <span data-ttu-id="0a6a3-125">System. String</span><span class="sxs-lookup"><span data-stu-id="0a6a3-125">System.String</span></span>

## <span data-ttu-id="0a6a3-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0a6a3-126">OUTPUTS</span></span>

### <span data-ttu-id="0a6a3-127">Microsoft. Azure. Commands. StreamAnalytics. Models. PSInput</span><span class="sxs-lookup"><span data-stu-id="0a6a3-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="0a6a3-128">Note</span><span class="sxs-lookup"><span data-stu-id="0a6a3-128">NOTES</span></span>

## <span data-ttu-id="0a6a3-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0a6a3-129">RELATED LINKS</span></span>

[<span data-ttu-id="0a6a3-130">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="0a6a3-130">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="0a6a3-131">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="0a6a3-131">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)

[<span data-ttu-id="0a6a3-132">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="0a6a3-132">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)


