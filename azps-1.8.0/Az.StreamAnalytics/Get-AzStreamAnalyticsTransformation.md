---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 34E1CC9E-9F81-4DA6-A777-D816B09BDE1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: ce933affbe3b99854f1ce907c968f35645c1d777
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676415"
---
# <span data-ttu-id="42f99-101">Get-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="42f99-101">Get-AzStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="42f99-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="42f99-102">SYNOPSIS</span></span>
<span data-ttu-id="42f99-103">Ottiene informazioni su una trasformazione del processo di analisi del flusso.</span><span class="sxs-lookup"><span data-stu-id="42f99-103">Gets information about a Stream Analytics job transformation.</span></span>

## <span data-ttu-id="42f99-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="42f99-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsTransformation [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42f99-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42f99-105">DESCRIPTION</span></span>
<span data-ttu-id="42f99-106">Il cmdlet **Get-AzStreamAnalyticsTransformation** ottiene le informazioni su una trasformazione definita in un processo di analisi del flusso.</span><span class="sxs-lookup"><span data-stu-id="42f99-106">The **Get-AzStreamAnalyticsTransformation** cmdlet gets information about a transformation defined on a Stream Analytics job.</span></span>

## <span data-ttu-id="42f99-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="42f99-107">EXAMPLES</span></span>

### <span data-ttu-id="42f99-108">ESEMPIO 1: ottenere informazioni su una trasformazione di analisi del flusso</span><span class="sxs-lookup"><span data-stu-id="42f99-108">EXAMPLE 1: Get information about a Stream Analytics transformation</span></span>
```
PS C:\>Get-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "StreamingJob"
```

<span data-ttu-id="42f99-109">Questo comando restituisce informazioni sulla trasformazione denominata StreamingJob nel processo denominato StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="42f99-109">This command returns information about the transformation called StreamingJob on the job called StreamingJob.</span></span>

## <span data-ttu-id="42f99-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="42f99-110">PARAMETERS</span></span>

### <span data-ttu-id="42f99-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42f99-111">-DefaultProfile</span></span>
<span data-ttu-id="42f99-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="42f99-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42f99-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="42f99-113">-JobName</span></span>
<span data-ttu-id="42f99-114">Specifica il nome del processo di analisi di Azure stream a cui appartiene la trasformazione di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="42f99-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="42f99-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="42f99-115">-Name</span></span>
<span data-ttu-id="42f99-116">Specifica il nome della trasformazione di analisi di Azure Stream da recuperare.</span><span class="sxs-lookup"><span data-stu-id="42f99-116">Specifies the name of the Azure Stream Analytics transformation to retrieve.</span></span>

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

### <span data-ttu-id="42f99-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42f99-117">-ResourceGroupName</span></span>
<span data-ttu-id="42f99-118">Specifica il nome del gruppo di risorse a cui appartiene la trasformazione di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="42f99-118">Specifies the name of the resource group to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="42f99-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42f99-119">CommonParameters</span></span>
<span data-ttu-id="42f99-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42f99-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42f99-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42f99-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42f99-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="42f99-122">INPUTS</span></span>

### <span data-ttu-id="42f99-123">System. String</span><span class="sxs-lookup"><span data-stu-id="42f99-123">System.String</span></span>

## <span data-ttu-id="42f99-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="42f99-124">OUTPUTS</span></span>

### <span data-ttu-id="42f99-125">Microsoft. Azure. Commands. StreamAnalytics. Models. PSTransformation</span><span class="sxs-lookup"><span data-stu-id="42f99-125">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="42f99-126">Note</span><span class="sxs-lookup"><span data-stu-id="42f99-126">NOTES</span></span>

## <span data-ttu-id="42f99-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="42f99-127">RELATED LINKS</span></span>

[<span data-ttu-id="42f99-128">New-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="42f99-128">New-AzStreamAnalyticsTransformation</span></span>](./New-AzStreamAnalyticsTransformation.md)

