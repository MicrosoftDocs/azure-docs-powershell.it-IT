---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6BBD68B4-BCC6-479A-AA70-D4ED445CFB32
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpointnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
ms.openlocfilehash: 09fd2e23cf8c91c2ffea1c10b5363011b9b189a5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018934"
---
# <span data-ttu-id="1ec57-101">Get-AzCdnEndpointNameAvailability</span><span class="sxs-lookup"><span data-stu-id="1ec57-101">Get-AzCdnEndpointNameAvailability</span></span>

## <span data-ttu-id="1ec57-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1ec57-102">SYNOPSIS</span></span>
<span data-ttu-id="1ec57-103">Ottiene lo stato di disponibilità dell'endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="1ec57-103">Gets availability status of the CDN endpoint.</span></span>

## <span data-ttu-id="1ec57-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1ec57-104">SYNTAX</span></span>

```
Get-AzCdnEndpointNameAvailability -EndpointName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1ec57-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1ec57-105">DESCRIPTION</span></span>
<span data-ttu-id="1ec57-106">Il cmdlet **Get-AzCdnEndpointNameAvailability** ottiene lo stato di disponibilità dell'endpoint della rete di distribuzione del contenuto di Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="1ec57-106">The **Get-AzCdnEndpointNameAvailability** cmdlet gets availability status of the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="1ec57-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1ec57-107">EXAMPLES</span></span>

## <span data-ttu-id="1ec57-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1ec57-108">PARAMETERS</span></span>

### <span data-ttu-id="1ec57-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ec57-109">-DefaultProfile</span></span>
<span data-ttu-id="1ec57-110">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1ec57-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1ec57-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="1ec57-111">-EndpointName</span></span>
<span data-ttu-id="1ec57-112">Specifica il nome dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="1ec57-112">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="1ec57-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ec57-113">CommonParameters</span></span>
<span data-ttu-id="1ec57-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ec57-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ec57-115">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1ec57-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ec57-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1ec57-116">INPUTS</span></span>

### <span data-ttu-id="1ec57-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1ec57-117">None</span></span>

## <span data-ttu-id="1ec57-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1ec57-118">OUTPUTS</span></span>

### <span data-ttu-id="1ec57-119">Microsoft. Azure. Commands. CDN. Models. endpoint. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="1ec57-119">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="1ec57-120">Note</span><span class="sxs-lookup"><span data-stu-id="1ec57-120">NOTES</span></span>

## <span data-ttu-id="1ec57-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1ec57-121">RELATED LINKS</span></span>
