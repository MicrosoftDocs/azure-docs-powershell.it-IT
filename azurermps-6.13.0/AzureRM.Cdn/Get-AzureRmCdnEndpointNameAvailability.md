---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 6BBD68B4-BCC6-479A-AA70-D4ED445CFB32
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnendpointnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointNameAvailability.md
ms.openlocfilehash: c5db5d27edb537602638ff5654a6da3ac35813ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519290"
---
# <span data-ttu-id="42f91-101">Get-AzureRmCdnEndpointNameAvailability</span><span class="sxs-lookup"><span data-stu-id="42f91-101">Get-AzureRmCdnEndpointNameAvailability</span></span>

## <span data-ttu-id="42f91-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="42f91-102">SYNOPSIS</span></span>
<span data-ttu-id="42f91-103">Ottiene lo stato di disponibilità dell'endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="42f91-103">Gets availability status of the CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42f91-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="42f91-104">SYNTAX</span></span>

```
Get-AzureRmCdnEndpointNameAvailability -EndpointName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="42f91-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42f91-105">DESCRIPTION</span></span>
<span data-ttu-id="42f91-106">Il cmdlet **Get-AzureRmCdnEndpointNameAvailability** ottiene lo stato di disponibilità dell'endpoint della rete di distribuzione del contenuto di Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="42f91-106">The **Get-AzureRmCdnEndpointNameAvailability** cmdlet gets availability status of the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="42f91-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="42f91-107">EXAMPLES</span></span>

## <span data-ttu-id="42f91-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="42f91-108">PARAMETERS</span></span>

### <span data-ttu-id="42f91-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42f91-109">-DefaultProfile</span></span>
<span data-ttu-id="42f91-110">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="42f91-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="42f91-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="42f91-111">-EndpointName</span></span>
<span data-ttu-id="42f91-112">Specifica il nome dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="42f91-112">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="42f91-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42f91-113">CommonParameters</span></span>
<span data-ttu-id="42f91-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42f91-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42f91-115">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42f91-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42f91-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="42f91-116">INPUTS</span></span>

### <span data-ttu-id="42f91-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="42f91-117">None</span></span>

## <span data-ttu-id="42f91-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="42f91-118">OUTPUTS</span></span>

### <span data-ttu-id="42f91-119">Microsoft. Azure. Commands. CDN. Models. endpoint. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="42f91-119">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="42f91-120">Note</span><span class="sxs-lookup"><span data-stu-id="42f91-120">NOTES</span></span>

## <span data-ttu-id="42f91-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="42f91-121">RELATED LINKS</span></span>
