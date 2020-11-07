---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: ECD0950F-2490-49E2-85E6-5FA2A59364E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsQuota.md
ms.openlocfilehash: dd36a1dcf5b23c26f0936b3adb0f692335c03c48
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676418"
---
# <span data-ttu-id="c31c4-101">Get-AzStreamAnalyticsQuota</span><span class="sxs-lookup"><span data-stu-id="c31c4-101">Get-AzStreamAnalyticsQuota</span></span>

## <span data-ttu-id="c31c4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c31c4-102">SYNOPSIS</span></span>
<span data-ttu-id="c31c4-103">Ottiene informazioni sulla quota di unità di flusso per un'area geografica.</span><span class="sxs-lookup"><span data-stu-id="c31c4-103">Gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="c31c4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c31c4-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c31c4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c31c4-105">DESCRIPTION</span></span>
<span data-ttu-id="c31c4-106">Il cmdlet **Get-AzStreamAnalyticsQuota** ottiene le informazioni sulla quota di unità di flusso per un'area geografica.</span><span class="sxs-lookup"><span data-stu-id="c31c4-106">The **Get-AzStreamAnalyticsQuota** cmdlet gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="c31c4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c31c4-107">EXAMPLES</span></span>

### <span data-ttu-id="c31c4-108">ESEMPIO 1: ottenere informazioni sulla quota di unità di flusso per un'area geografica</span><span class="sxs-lookup"><span data-stu-id="c31c4-108">EXAMPLE 1: Get information about the Streaming Unit quota for a region</span></span>
```
PS C:\>Get-AzStreamAnalyticsQuota -Location "West US"
```

<span data-ttu-id="c31c4-109">Questo comando restituisce informazioni sulla quota di unità di flusso e sull'utilizzo nell'area ovest degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="c31c4-109">This command returns information about Streaming Unit quota and usage in the West US region.</span></span>

## <span data-ttu-id="c31c4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c31c4-110">PARAMETERS</span></span>

### <span data-ttu-id="c31c4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c31c4-111">-DefaultProfile</span></span>
<span data-ttu-id="c31c4-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c31c4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c31c4-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="c31c4-113">-Location</span></span>
<span data-ttu-id="c31c4-114">Specifica il nome di un'area di Azure o di un centro dati per cui ottenere informazioni sulle quote delle unità di flusso.</span><span class="sxs-lookup"><span data-stu-id="c31c4-114">Specifies the name of an Azure region or data center location for which to get Streaming Unit quota information.</span></span>
<span data-ttu-id="c31c4-115">Vedere https://azure.microsoft.com/en-us/regions/#serviceshttps://azure.microsoft.com/en-us/regions/#services per un elenco delle aree di Azure supportate.</span><span class="sxs-lookup"><span data-stu-id="c31c4-115">See https://azure.microsoft.com/en-us/regions/#serviceshttps://azure.microsoft.com/en-us/regions/#services for a list of supported Azure regions.</span></span>

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

### <span data-ttu-id="c31c4-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c31c4-116">CommonParameters</span></span>
<span data-ttu-id="c31c4-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c31c4-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c31c4-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c31c4-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c31c4-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c31c4-119">INPUTS</span></span>

### <span data-ttu-id="c31c4-120">System. String</span><span class="sxs-lookup"><span data-stu-id="c31c4-120">System.String</span></span>

## <span data-ttu-id="c31c4-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c31c4-121">OUTPUTS</span></span>

### <span data-ttu-id="c31c4-122">Microsoft. Azure. Commands. StreamAnalytics. Models. PSQuota</span><span class="sxs-lookup"><span data-stu-id="c31c4-122">Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota</span></span>

## <span data-ttu-id="c31c4-123">Note</span><span class="sxs-lookup"><span data-stu-id="c31c4-123">NOTES</span></span>

## <span data-ttu-id="c31c4-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c31c4-124">RELATED LINKS</span></span>

[<span data-ttu-id="c31c4-125">Cmdlet di analisi di Azure Stream</span><span class="sxs-lookup"><span data-stu-id="c31c4-125">Azure Stream Analytics Cmdlets</span></span>](./Az.StreamAnalytics.md)

