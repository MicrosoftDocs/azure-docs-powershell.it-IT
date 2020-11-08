---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6BBD68B4-BCC6-479A-AA70-D4ED445CFB32
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpointnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
ms.openlocfilehash: 09fd2e23cf8c91c2ffea1c10b5363011b9b189a5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203007"
---
# <span data-ttu-id="981ae-101">Get-AzCdnEndpointNameAvailability</span><span class="sxs-lookup"><span data-stu-id="981ae-101">Get-AzCdnEndpointNameAvailability</span></span>

## <span data-ttu-id="981ae-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="981ae-102">SYNOPSIS</span></span>
<span data-ttu-id="981ae-103">Ottiene lo stato di disponibilità dell'endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="981ae-103">Gets availability status of the CDN endpoint.</span></span>

## <span data-ttu-id="981ae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="981ae-104">SYNTAX</span></span>

```
Get-AzCdnEndpointNameAvailability -EndpointName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="981ae-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="981ae-105">DESCRIPTION</span></span>
<span data-ttu-id="981ae-106">Il cmdlet **Get-AzCdnEndpointNameAvailability** ottiene lo stato di disponibilità dell'endpoint della rete di distribuzione del contenuto di Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="981ae-106">The **Get-AzCdnEndpointNameAvailability** cmdlet gets availability status of the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="981ae-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="981ae-107">EXAMPLES</span></span>

## <span data-ttu-id="981ae-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="981ae-108">PARAMETERS</span></span>

### <span data-ttu-id="981ae-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="981ae-109">-DefaultProfile</span></span>
<span data-ttu-id="981ae-110">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="981ae-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="981ae-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="981ae-111">-EndpointName</span></span>
<span data-ttu-id="981ae-112">Specifica il nome dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="981ae-112">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="981ae-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="981ae-113">CommonParameters</span></span>
<span data-ttu-id="981ae-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="981ae-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="981ae-115">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="981ae-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="981ae-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="981ae-116">INPUTS</span></span>

### <span data-ttu-id="981ae-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="981ae-117">None</span></span>

## <span data-ttu-id="981ae-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="981ae-118">OUTPUTS</span></span>

### <span data-ttu-id="981ae-119">Microsoft. Azure. Commands. CDN. Models. endpoint. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="981ae-119">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="981ae-120">Note</span><span class="sxs-lookup"><span data-stu-id="981ae-120">NOTES</span></span>

## <span data-ttu-id="981ae-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="981ae-121">RELATED LINKS</span></span>
