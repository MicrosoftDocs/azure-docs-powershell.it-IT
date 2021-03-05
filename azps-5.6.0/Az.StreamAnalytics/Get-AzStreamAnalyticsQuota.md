---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: ECD0950F-2490-49E2-85E6-5FA2A59364E6
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/get-azstreamanalyticsquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsQuota.md
ms.openlocfilehash: 8583227cee19a9429a7dfe4cd6bd8678e72d33ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973853"
---
# <span data-ttu-id="0a5cd-101">Get-AzStreamAnalyticsQuota</span><span class="sxs-lookup"><span data-stu-id="0a5cd-101">Get-AzStreamAnalyticsQuota</span></span>

## <span data-ttu-id="0a5cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a5cd-102">SYNOPSIS</span></span>
<span data-ttu-id="0a5cd-103">Ottiene informazioni sulla quota dell'unità di trasmissione per un'area geografica.</span><span class="sxs-lookup"><span data-stu-id="0a5cd-103">Gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="0a5cd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0a5cd-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a5cd-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0a5cd-105">DESCRIPTION</span></span>
<span data-ttu-id="0a5cd-106">Il cmdlet **Get-AzStreamAnalyticsQuota** ottiene informazioni sulla quota di unità di flusso per un'area geografica.</span><span class="sxs-lookup"><span data-stu-id="0a5cd-106">The **Get-AzStreamAnalyticsQuota** cmdlet gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="0a5cd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0a5cd-107">EXAMPLES</span></span>

### <span data-ttu-id="0a5cd-108">ESEMPIO 1: Ottenere informazioni sulla quota dell'unità di trasmissione per un'area geografica</span><span class="sxs-lookup"><span data-stu-id="0a5cd-108">EXAMPLE 1: Get information about the Streaming Unit quota for a region</span></span>
```
PS C:\>Get-AzStreamAnalyticsQuota -Location "West US"
```

<span data-ttu-id="0a5cd-109">Questo comando restituisce informazioni sulla quota di unità di streaming e sull'utilizzo nell'area degli Stati Uniti occidentali.</span><span class="sxs-lookup"><span data-stu-id="0a5cd-109">This command returns information about Streaming Unit quota and usage in the West US region.</span></span>

## <span data-ttu-id="0a5cd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a5cd-110">PARAMETERS</span></span>

### <span data-ttu-id="0a5cd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a5cd-111">-DefaultProfile</span></span>
<span data-ttu-id="0a5cd-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0a5cd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a5cd-113">-Location</span><span class="sxs-lookup"><span data-stu-id="0a5cd-113">-Location</span></span>
<span data-ttu-id="0a5cd-114">Specifica il nome di un'area geografica o di una posizione del data center di Azure per cui ottenere informazioni sulle quote delle unità di streaming.</span><span class="sxs-lookup"><span data-stu-id="0a5cd-114">Specifies the name of an Azure region or data center location for which to get Streaming Unit quota information.</span></span>
<span data-ttu-id="0a5cd-115">Per http://azure.microsoft.com/en-us/regions/#serviceshttp://azure.microsoft.com/en-us/regions/#services un elenco delle aree geografiche di Azure supportate, vedere.</span><span class="sxs-lookup"><span data-stu-id="0a5cd-115">See http://azure.microsoft.com/en-us/regions/#serviceshttp://azure.microsoft.com/en-us/regions/#services for a list of supported Azure regions.</span></span>

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

### <span data-ttu-id="0a5cd-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a5cd-116">CommonParameters</span></span>
<span data-ttu-id="0a5cd-117">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a5cd-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a5cd-118">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a5cd-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a5cd-119">INPUT</span><span class="sxs-lookup"><span data-stu-id="0a5cd-119">INPUTS</span></span>

### <span data-ttu-id="0a5cd-120">System.String</span><span class="sxs-lookup"><span data-stu-id="0a5cd-120">System.String</span></span>

## <span data-ttu-id="0a5cd-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0a5cd-121">OUTPUTS</span></span>

### <span data-ttu-id="0a5cd-122">Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota</span><span class="sxs-lookup"><span data-stu-id="0a5cd-122">Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota</span></span>

## <span data-ttu-id="0a5cd-123">NOTE</span><span class="sxs-lookup"><span data-stu-id="0a5cd-123">NOTES</span></span>

## <span data-ttu-id="0a5cd-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0a5cd-124">RELATED LINKS</span></span>

[<span data-ttu-id="0a5cd-125">Cmdlet di Analisi di flusso di Azure</span><span class="sxs-lookup"><span data-stu-id="0a5cd-125">Azure Stream Analytics Cmdlets</span></span>](./Az.StreamAnalytics.md)


