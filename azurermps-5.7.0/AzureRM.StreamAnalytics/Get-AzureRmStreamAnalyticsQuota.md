---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: ECD0950F-2490-49E2-85E6-5FA2A59364E6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsQuota.md
ms.openlocfilehash: de676da4e276cf7e2b49558c81e9d7f6876d158b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517835"
---
# <span data-ttu-id="25fc7-101">Get-AzureRmStreamAnalyticsQuota</span><span class="sxs-lookup"><span data-stu-id="25fc7-101">Get-AzureRmStreamAnalyticsQuota</span></span>

## <span data-ttu-id="25fc7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="25fc7-102">SYNOPSIS</span></span>
<span data-ttu-id="25fc7-103">Ottiene informazioni sulla quota di unità di flusso per un'area geografica.</span><span class="sxs-lookup"><span data-stu-id="25fc7-103">Gets information about the Streaming Unit quota for a region.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25fc7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="25fc7-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="25fc7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="25fc7-105">DESCRIPTION</span></span>
<span data-ttu-id="25fc7-106">Il cmdlet **Get-AzureRmStreamAnalyticsQuota** ottiene le informazioni sulla quota di unità di flusso per un'area geografica.</span><span class="sxs-lookup"><span data-stu-id="25fc7-106">The **Get-AzureRmStreamAnalyticsQuota** cmdlet gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="25fc7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="25fc7-107">EXAMPLES</span></span>

### <span data-ttu-id="25fc7-108">ESEMPIO 1: ottenere informazioni sulla quota di unità di flusso per un'area geografica</span><span class="sxs-lookup"><span data-stu-id="25fc7-108">EXAMPLE 1: Get information about the Streaming Unit quota for a region</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsQuota -Location "West US"
```

<span data-ttu-id="25fc7-109">Questo comando restituisce informazioni sulla quota di unità di flusso e sull'utilizzo nell'area ovest degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="25fc7-109">This command returns information about Streaming Unit quota and usage in the West US region.</span></span>

## <span data-ttu-id="25fc7-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="25fc7-110">PARAMETERS</span></span>

### <span data-ttu-id="25fc7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25fc7-111">-DefaultProfile</span></span>
<span data-ttu-id="25fc7-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="25fc7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25fc7-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="25fc7-113">-Location</span></span>
<span data-ttu-id="25fc7-114">Specifica il nome di un'area di Azure o di un centro dati per cui ottenere informazioni sulle quote delle unità di flusso.</span><span class="sxs-lookup"><span data-stu-id="25fc7-114">Specifies the name of an Azure region or data center location for which to get Streaming Unit quota information.</span></span>
<span data-ttu-id="25fc7-115">Vedere https://azure.microsoft.com/en-us/regions/#serviceshttps://azure.microsoft.com/en-us/regions/#services per un elenco delle aree di Azure supportate.</span><span class="sxs-lookup"><span data-stu-id="25fc7-115">See https://azure.microsoft.com/en-us/regions/#serviceshttps://azure.microsoft.com/en-us/regions/#services for a list of supported Azure regions.</span></span>

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

### <span data-ttu-id="25fc7-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25fc7-116">CommonParameters</span></span>
<span data-ttu-id="25fc7-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25fc7-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25fc7-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25fc7-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25fc7-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="25fc7-119">INPUTS</span></span>

### <span data-ttu-id="25fc7-120">Nessuno</span><span class="sxs-lookup"><span data-stu-id="25fc7-120">None</span></span>
<span data-ttu-id="25fc7-121">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="25fc7-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="25fc7-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="25fc7-122">OUTPUTS</span></span>

### <span data-ttu-id="25fc7-123">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. StreamAnalytics. Models. PSQuota, Microsoft. Azure. Commands. StreamAnalytics]] Microsoft. Azure. Commands. StreamAnalytics. Models. PSQuota</span><span class="sxs-lookup"><span data-stu-id="25fc7-123">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota</span></span>

## <span data-ttu-id="25fc7-124">Note</span><span class="sxs-lookup"><span data-stu-id="25fc7-124">NOTES</span></span>

## <span data-ttu-id="25fc7-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="25fc7-125">RELATED LINKS</span></span>

[<span data-ttu-id="25fc7-126">Cmdlet di analisi di Azure Stream</span><span class="sxs-lookup"><span data-stu-id="25fc7-126">Azure Stream Analytics Cmdlets</span></span>](./AzureRM.StreamAnalytics.md)


