---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 34E1CC9E-9F81-4DA6-A777-D816B09BDE1B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsTransformation.md
ms.openlocfilehash: 9c92156f3fe739cd4f4285d536bd8a4c79cd3ec2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686288"
---
# <span data-ttu-id="b2e12-101">Get-AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="b2e12-101">Get-AzureRmStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="b2e12-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b2e12-102">SYNOPSIS</span></span>
<span data-ttu-id="b2e12-103">Ottiene informazioni su una trasformazione del processo di analisi del flusso.</span><span class="sxs-lookup"><span data-stu-id="b2e12-103">Gets information about a Stream Analytics job transformation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2e12-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b2e12-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsTransformation [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2e12-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2e12-105">DESCRIPTION</span></span>
<span data-ttu-id="b2e12-106">Il cmdlet **Get-AzureRmStreamAnalyticsTransformation** ottiene le informazioni su una trasformazione definita in un processo di analisi del flusso.</span><span class="sxs-lookup"><span data-stu-id="b2e12-106">The **Get-AzureRmStreamAnalyticsTransformation** cmdlet gets information about a transformation defined on a Stream Analytics job.</span></span>

## <span data-ttu-id="b2e12-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b2e12-107">EXAMPLES</span></span>

### <span data-ttu-id="b2e12-108">ESEMPIO 1: ottenere informazioni su una trasformazione di analisi del flusso</span><span class="sxs-lookup"><span data-stu-id="b2e12-108">EXAMPLE 1: Get information about a Stream Analytics transformation</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "StreamingJob"
```

<span data-ttu-id="b2e12-109">Questo comando restituisce informazioni sulla trasformazione denominata StreamingJob nel processo denominato StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="b2e12-109">This command returns information about the transformation called StreamingJob on the job called StreamingJob.</span></span>

## <span data-ttu-id="b2e12-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b2e12-110">PARAMETERS</span></span>

### <span data-ttu-id="b2e12-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2e12-111">-DefaultProfile</span></span>
<span data-ttu-id="b2e12-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b2e12-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2e12-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="b2e12-113">-JobName</span></span>
<span data-ttu-id="b2e12-114">Specifica il nome del processo di analisi di Azure stream a cui appartiene la trasformazione di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="b2e12-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="b2e12-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="b2e12-115">-Name</span></span>
<span data-ttu-id="b2e12-116">Specifica il nome della trasformazione di analisi di Azure Stream da recuperare.</span><span class="sxs-lookup"><span data-stu-id="b2e12-116">Specifies the name of the Azure Stream Analytics transformation to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2e12-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2e12-117">-ResourceGroupName</span></span>
<span data-ttu-id="b2e12-118">Specifica il nome del gruppo di risorse a cui appartiene la trasformazione di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="b2e12-118">Specifies the name of the resource group to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="b2e12-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2e12-119">CommonParameters</span></span>
<span data-ttu-id="b2e12-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2e12-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2e12-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2e12-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2e12-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b2e12-122">INPUTS</span></span>

### <span data-ttu-id="b2e12-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b2e12-123">None</span></span>
<span data-ttu-id="b2e12-124">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="b2e12-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b2e12-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b2e12-125">OUTPUTS</span></span>

### <span data-ttu-id="b2e12-126">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. StreamAnalytics. Models. PSTransformation, Microsoft. Azure. Commands. StreamAnalytics]] Microsoft. Azure. Commands. StreamAnalytics. Models. PSTransformation</span><span class="sxs-lookup"><span data-stu-id="b2e12-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="b2e12-127">Note</span><span class="sxs-lookup"><span data-stu-id="b2e12-127">NOTES</span></span>

## <span data-ttu-id="b2e12-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b2e12-128">RELATED LINKS</span></span>

[<span data-ttu-id="b2e12-129">New-AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="b2e12-129">New-AzureRmStreamAnalyticsTransformation</span></span>](./New-AzureRmStreamAnalyticsTransformation.md)


