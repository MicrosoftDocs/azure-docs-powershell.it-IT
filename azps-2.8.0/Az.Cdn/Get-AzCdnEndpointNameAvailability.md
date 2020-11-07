---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6BBD68B4-BCC6-479A-AA70-D4ED445CFB32
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpointnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
ms.openlocfilehash: f21c8303f1ec156132653a5d05c1149ef10a9ee7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675568"
---
# <span data-ttu-id="b730f-101">Get-AzCdnEndpointNameAvailability</span><span class="sxs-lookup"><span data-stu-id="b730f-101">Get-AzCdnEndpointNameAvailability</span></span>

## <span data-ttu-id="b730f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b730f-102">SYNOPSIS</span></span>
<span data-ttu-id="b730f-103">Ottiene lo stato di disponibilità dell'endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="b730f-103">Gets availability status of the CDN endpoint.</span></span>

## <span data-ttu-id="b730f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b730f-104">SYNTAX</span></span>

```
Get-AzCdnEndpointNameAvailability -EndpointName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b730f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b730f-105">DESCRIPTION</span></span>
<span data-ttu-id="b730f-106">Il cmdlet **Get-AzCdnEndpointNameAvailability** ottiene lo stato di disponibilità dell'endpoint della rete di distribuzione del contenuto di Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="b730f-106">The **Get-AzCdnEndpointNameAvailability** cmdlet gets availability status of the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="b730f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b730f-107">EXAMPLES</span></span>

## <span data-ttu-id="b730f-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b730f-108">PARAMETERS</span></span>

### <span data-ttu-id="b730f-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b730f-109">-DefaultProfile</span></span>
<span data-ttu-id="b730f-110">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b730f-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b730f-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="b730f-111">-EndpointName</span></span>
<span data-ttu-id="b730f-112">Specifica il nome dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="b730f-112">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="b730f-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b730f-113">CommonParameters</span></span>
<span data-ttu-id="b730f-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b730f-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b730f-115">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b730f-115">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b730f-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b730f-116">INPUTS</span></span>

### <span data-ttu-id="b730f-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b730f-117">None</span></span>

## <span data-ttu-id="b730f-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b730f-118">OUTPUTS</span></span>

### <span data-ttu-id="b730f-119">Microsoft. Azure. Commands. CDN. Models. endpoint. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="b730f-119">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="b730f-120">Note</span><span class="sxs-lookup"><span data-stu-id="b730f-120">NOTES</span></span>

## <span data-ttu-id="b730f-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b730f-121">RELATED LINKS</span></span>
