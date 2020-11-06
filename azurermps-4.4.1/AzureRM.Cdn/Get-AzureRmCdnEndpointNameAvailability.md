---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 6BBD68B4-BCC6-479A-AA70-D4ED445CFB32
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointNameAvailability.md
ms.openlocfilehash: 6c5c11123ab39d92bb7b702542b007c8c075f9b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519624"
---
# <span data-ttu-id="071f8-101">Get-AzureRmCdnEndpointNameAvailability</span><span class="sxs-lookup"><span data-stu-id="071f8-101">Get-AzureRmCdnEndpointNameAvailability</span></span>

## <span data-ttu-id="071f8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="071f8-102">SYNOPSIS</span></span>
<span data-ttu-id="071f8-103">Ottiene lo stato di disponibilità dell'endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="071f8-103">Gets availability status of the CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="071f8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="071f8-104">SYNTAX</span></span>

```
Get-AzureRmCdnEndpointNameAvailability -EndpointName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="071f8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="071f8-105">DESCRIPTION</span></span>
<span data-ttu-id="071f8-106">Il cmdlet **Get-AzureRmCdnEndpointNameAvailability** ottiene lo stato di disponibilità dell'endpoint della rete di distribuzione del contenuto di Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="071f8-106">The **Get-AzureRmCdnEndpointNameAvailability** cmdlet gets availability status of the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="071f8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="071f8-107">EXAMPLES</span></span>

## <span data-ttu-id="071f8-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="071f8-108">PARAMETERS</span></span>

### <span data-ttu-id="071f8-109">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="071f8-109">-EndpointName</span></span>
<span data-ttu-id="071f8-110">Specifica il nome dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="071f8-110">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="071f8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="071f8-111">-DefaultProfile</span></span>
<span data-ttu-id="071f8-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="071f8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="071f8-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="071f8-113">CommonParameters</span></span>
<span data-ttu-id="071f8-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="071f8-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="071f8-115">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="071f8-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="071f8-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="071f8-116">INPUTS</span></span>

## <span data-ttu-id="071f8-117">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="071f8-117">OUTPUTS</span></span>

### <span data-ttu-id="071f8-118">Microsoft. Azure. Commands. CDN. Models. endpoint. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="071f8-118">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="071f8-119">Note</span><span class="sxs-lookup"><span data-stu-id="071f8-119">NOTES</span></span>

## <span data-ttu-id="071f8-120">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="071f8-120">RELATED LINKS</span></span>

