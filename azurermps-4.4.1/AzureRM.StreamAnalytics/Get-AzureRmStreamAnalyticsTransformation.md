---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 34E1CC9E-9F81-4DA6-A777-D816B09BDE1B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsTransformation.md
ms.openlocfilehash: 24313884b92a9a4c738425d64463c695ff689c7b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511228"
---
# <span data-ttu-id="76c37-101">Get-AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="76c37-101">Get-AzureRmStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="76c37-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="76c37-102">SYNOPSIS</span></span>
<span data-ttu-id="76c37-103">Ottiene informazioni su una trasformazione del processo di analisi del flusso.</span><span class="sxs-lookup"><span data-stu-id="76c37-103">Gets information about a Stream Analytics job transformation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76c37-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="76c37-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsTransformation [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76c37-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="76c37-105">DESCRIPTION</span></span>
<span data-ttu-id="76c37-106">Il cmdlet **Get-AzureRmStreamAnalyticsTransformation** ottiene le informazioni su una trasformazione definita in un processo di analisi del flusso.</span><span class="sxs-lookup"><span data-stu-id="76c37-106">The **Get-AzureRmStreamAnalyticsTransformation** cmdlet gets information about a transformation defined on a Stream Analytics job.</span></span>

## <span data-ttu-id="76c37-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="76c37-107">EXAMPLES</span></span>

### <span data-ttu-id="76c37-108">ESEMPIO 1: ottenere informazioni su una trasformazione di analisi del flusso</span><span class="sxs-lookup"><span data-stu-id="76c37-108">EXAMPLE 1: Get information about a Stream Analytics transformation</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "StreamingJob"
```

<span data-ttu-id="76c37-109">Questo comando restituisce informazioni sulla trasformazione denominata StreamingJob nel processo denominato StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="76c37-109">This command returns information about the transformation called StreamingJob on the job called StreamingJob.</span></span>

## <span data-ttu-id="76c37-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="76c37-110">PARAMETERS</span></span>

### <span data-ttu-id="76c37-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="76c37-111">-JobName</span></span>
<span data-ttu-id="76c37-112">Specifica il nome del processo di analisi di Azure stream a cui appartiene la trasformazione di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="76c37-112">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="76c37-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="76c37-113">-Name</span></span>
<span data-ttu-id="76c37-114">Specifica il nome della trasformazione di analisi di Azure Stream da recuperare.</span><span class="sxs-lookup"><span data-stu-id="76c37-114">Specifies the name of the Azure Stream Analytics transformation to retrieve.</span></span>

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

### <span data-ttu-id="76c37-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76c37-115">-ResourceGroupName</span></span>
<span data-ttu-id="76c37-116">Specifica il nome del gruppo di risorse a cui appartiene la trasformazione di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="76c37-116">Specifies the name of the resource group to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="76c37-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76c37-117">-DefaultProfile</span></span>
<span data-ttu-id="76c37-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="76c37-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76c37-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76c37-119">CommonParameters</span></span>
<span data-ttu-id="76c37-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76c37-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76c37-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76c37-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76c37-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="76c37-122">INPUTS</span></span>

## <span data-ttu-id="76c37-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="76c37-123">OUTPUTS</span></span>

### <span data-ttu-id="76c37-124">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. StreamAnalytics. Models. PSTransformation, Microsoft. Azure. Commands. StreamAnalytics]] Microsoft. Azure. Commands. StreamAnalytics. Models. PSTransformation</span><span class="sxs-lookup"><span data-stu-id="76c37-124">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="76c37-125">Note</span><span class="sxs-lookup"><span data-stu-id="76c37-125">NOTES</span></span>

## <span data-ttu-id="76c37-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="76c37-126">RELATED LINKS</span></span>

[<span data-ttu-id="76c37-127">New-AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="76c37-127">New-AzureRmStreamAnalyticsTransformation</span></span>](./New-AzureRmStreamAnalyticsTransformation.md)


