---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6BBD68B4-BCC6-479A-AA70-D4ED445CFB32
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpointnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
ms.openlocfilehash: 09fd2e23cf8c91c2ffea1c10b5363011b9b189a5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181870"
---
# <span data-ttu-id="1cde3-101">Get-AzCdnEndpointNameAvailability</span><span class="sxs-lookup"><span data-stu-id="1cde3-101">Get-AzCdnEndpointNameAvailability</span></span>

## <span data-ttu-id="1cde3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cde3-102">SYNOPSIS</span></span>
<span data-ttu-id="1cde3-103">Ottiene lo stato di disponibilità dell'endpoint della rete CDN.</span><span class="sxs-lookup"><span data-stu-id="1cde3-103">Gets availability status of the CDN endpoint.</span></span>

## <span data-ttu-id="1cde3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1cde3-104">SYNTAX</span></span>

```
Get-AzCdnEndpointNameAvailability -EndpointName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1cde3-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1cde3-105">DESCRIPTION</span></span>
<span data-ttu-id="1cde3-106">Il cmdlet **Get-AzCdnEndpointNameAvailability** ottiene lo stato di disponibilità dell'endpoint rete per la distribuzione di contenuti (CDN) di Azure.</span><span class="sxs-lookup"><span data-stu-id="1cde3-106">The **Get-AzCdnEndpointNameAvailability** cmdlet gets availability status of the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="1cde3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1cde3-107">EXAMPLES</span></span>

## <span data-ttu-id="1cde3-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1cde3-108">PARAMETERS</span></span>

### <span data-ttu-id="1cde3-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cde3-109">-DefaultProfile</span></span>
<span data-ttu-id="1cde3-110">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="1cde3-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1cde3-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="1cde3-111">-EndpointName</span></span>
<span data-ttu-id="1cde3-112">Specifica il nome dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="1cde3-112">Specifies the name of the endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cde3-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cde3-113">CommonParameters</span></span>
<span data-ttu-id="1cde3-114">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cde3-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cde3-115">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1cde3-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cde3-116">INPUT</span><span class="sxs-lookup"><span data-stu-id="1cde3-116">INPUTS</span></span>

### <span data-ttu-id="1cde3-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1cde3-117">None</span></span>

## <span data-ttu-id="1cde3-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1cde3-118">OUTPUTS</span></span>

### <span data-ttu-id="1cde3-119">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="1cde3-119">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="1cde3-120">NOTE</span><span class="sxs-lookup"><span data-stu-id="1cde3-120">NOTES</span></span>

## <span data-ttu-id="1cde3-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1cde3-121">RELATED LINKS</span></span>
