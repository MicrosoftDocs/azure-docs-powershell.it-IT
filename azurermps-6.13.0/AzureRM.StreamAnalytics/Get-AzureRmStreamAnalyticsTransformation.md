---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 34E1CC9E-9F81-4DA6-A777-D816B09BDE1B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsTransformation.md
ms.openlocfilehash: d83038d521e562ec835324dd50740ec929fb5893
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507276"
---
# <span data-ttu-id="5e639-101">Get-AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="5e639-101">Get-AzureRmStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="5e639-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5e639-102">SYNOPSIS</span></span>
<span data-ttu-id="5e639-103">Ottiene informazioni su una trasformazione del processo di analisi del flusso.</span><span class="sxs-lookup"><span data-stu-id="5e639-103">Gets information about a Stream Analytics job transformation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e639-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5e639-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsTransformation [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e639-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e639-105">DESCRIPTION</span></span>
<span data-ttu-id="5e639-106">Il cmdlet **Get-AzureRmStreamAnalyticsTransformation** ottiene le informazioni su una trasformazione definita in un processo di analisi del flusso.</span><span class="sxs-lookup"><span data-stu-id="5e639-106">The **Get-AzureRmStreamAnalyticsTransformation** cmdlet gets information about a transformation defined on a Stream Analytics job.</span></span>

## <span data-ttu-id="5e639-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5e639-107">EXAMPLES</span></span>

### <span data-ttu-id="5e639-108">ESEMPIO 1: ottenere informazioni su una trasformazione di analisi del flusso</span><span class="sxs-lookup"><span data-stu-id="5e639-108">EXAMPLE 1: Get information about a Stream Analytics transformation</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "StreamingJob"
```

<span data-ttu-id="5e639-109">Questo comando restituisce informazioni sulla trasformazione denominata StreamingJob nel processo denominato StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="5e639-109">This command returns information about the transformation called StreamingJob on the job called StreamingJob.</span></span>

## <span data-ttu-id="5e639-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5e639-110">PARAMETERS</span></span>

### <span data-ttu-id="5e639-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e639-111">-DefaultProfile</span></span>
<span data-ttu-id="5e639-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5e639-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e639-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="5e639-113">-JobName</span></span>
<span data-ttu-id="5e639-114">Specifica il nome del processo di analisi di Azure stream a cui appartiene la trasformazione di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="5e639-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="5e639-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="5e639-115">-Name</span></span>
<span data-ttu-id="5e639-116">Specifica il nome della trasformazione di analisi di Azure Stream da recuperare.</span><span class="sxs-lookup"><span data-stu-id="5e639-116">Specifies the name of the Azure Stream Analytics transformation to retrieve.</span></span>

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

### <span data-ttu-id="5e639-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e639-117">-ResourceGroupName</span></span>
<span data-ttu-id="5e639-118">Specifica il nome del gruppo di risorse a cui appartiene la trasformazione di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="5e639-118">Specifies the name of the resource group to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="5e639-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e639-119">CommonParameters</span></span>
<span data-ttu-id="5e639-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e639-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e639-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e639-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e639-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5e639-122">INPUTS</span></span>

### <span data-ttu-id="5e639-123">System. String</span><span class="sxs-lookup"><span data-stu-id="5e639-123">System.String</span></span>

## <span data-ttu-id="5e639-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5e639-124">OUTPUTS</span></span>

### <span data-ttu-id="5e639-125">Microsoft. Azure. Commands. StreamAnalytics. Models. PSTransformation</span><span class="sxs-lookup"><span data-stu-id="5e639-125">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="5e639-126">Note</span><span class="sxs-lookup"><span data-stu-id="5e639-126">NOTES</span></span>

## <span data-ttu-id="5e639-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5e639-127">RELATED LINKS</span></span>

[<span data-ttu-id="5e639-128">New-AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="5e639-128">New-AzureRmStreamAnalyticsTransformation</span></span>](./New-AzureRmStreamAnalyticsTransformation.md)


