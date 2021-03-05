---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 34E1CC9E-9F81-4DA6-A777-D816B09BDE1B
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/get-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: 0c009ed05b475e466ab0b2c0dd7c6f18e70c2f9d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973838"
---
# <span data-ttu-id="71659-101">Get-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="71659-101">Get-AzStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="71659-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71659-102">SYNOPSIS</span></span>
<span data-ttu-id="71659-103">Ottiene informazioni sulla trasformazione di un processo di Analisi di flusso.</span><span class="sxs-lookup"><span data-stu-id="71659-103">Gets information about a Stream Analytics job transformation.</span></span>

## <span data-ttu-id="71659-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="71659-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsTransformation [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71659-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="71659-105">DESCRIPTION</span></span>
<span data-ttu-id="71659-106">Il cmdlet **Get-AzStreamAnalyticsTransformation** ottiene informazioni su una trasformazione definita in un processo di Analisi di flusso.</span><span class="sxs-lookup"><span data-stu-id="71659-106">The **Get-AzStreamAnalyticsTransformation** cmdlet gets information about a transformation defined on a Stream Analytics job.</span></span>

## <span data-ttu-id="71659-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="71659-107">EXAMPLES</span></span>

### <span data-ttu-id="71659-108">ESEMPIO 1: Ottenere informazioni su una trasformazione di Analisi di flusso</span><span class="sxs-lookup"><span data-stu-id="71659-108">EXAMPLE 1: Get information about a Stream Analytics transformation</span></span>
```
PS C:\>Get-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "StreamingJob"
```

<span data-ttu-id="71659-109">Questo comando restituisce informazioni sulla trasformazione chiamata StreamingJob nel processo denominato StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="71659-109">This command returns information about the transformation called StreamingJob on the job called StreamingJob.</span></span>

## <span data-ttu-id="71659-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71659-110">PARAMETERS</span></span>

### <span data-ttu-id="71659-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71659-111">-DefaultProfile</span></span>
<span data-ttu-id="71659-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="71659-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71659-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="71659-113">-JobName</span></span>
<span data-ttu-id="71659-114">Specifica il nome del processo di Analisi di flusso di Azure a cui appartiene la trasformazione Analisi di flusso di Azure.</span><span class="sxs-lookup"><span data-stu-id="71659-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="71659-115">-Name</span><span class="sxs-lookup"><span data-stu-id="71659-115">-Name</span></span>
<span data-ttu-id="71659-116">Specifica il nome della trasformazione di Analisi di flusso di Azure da recuperare.</span><span class="sxs-lookup"><span data-stu-id="71659-116">Specifies the name of the Azure Stream Analytics transformation to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71659-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71659-117">-ResourceGroupName</span></span>
<span data-ttu-id="71659-118">Specifica il nome del gruppo di risorse a cui appartiene la trasformazione di Analisi di flusso di Azure.</span><span class="sxs-lookup"><span data-stu-id="71659-118">Specifies the name of the resource group to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="71659-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71659-119">CommonParameters</span></span>
<span data-ttu-id="71659-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71659-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71659-121">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71659-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71659-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="71659-122">INPUTS</span></span>

### <span data-ttu-id="71659-123">System.String</span><span class="sxs-lookup"><span data-stu-id="71659-123">System.String</span></span>

## <span data-ttu-id="71659-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="71659-124">OUTPUTS</span></span>

### <span data-ttu-id="71659-125">Microsoft.Azure.Commands.StreamAnalytics.Models.PS Transformation</span><span class="sxs-lookup"><span data-stu-id="71659-125">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="71659-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="71659-126">NOTES</span></span>

## <span data-ttu-id="71659-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="71659-127">RELATED LINKS</span></span>

[<span data-ttu-id="71659-128">New-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="71659-128">New-AzStreamAnalyticsTransformation</span></span>](./New-AzStreamAnalyticsTransformation.md)


