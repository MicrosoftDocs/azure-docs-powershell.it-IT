---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/confirm-azcdnendpointprobeurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
ms.openlocfilehash: afc2400feb8694e74dd46731969429d6d7784369
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007262"
---
# <span data-ttu-id="6e2dd-101">Confirm-AzCdnEndpointProbeURL</span><span class="sxs-lookup"><span data-stu-id="6e2dd-101">Confirm-AzCdnEndpointProbeURL</span></span>

## <span data-ttu-id="6e2dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e2dd-102">SYNOPSIS</span></span>
<span data-ttu-id="6e2dd-103">Convalida un URL valido.</span><span class="sxs-lookup"><span data-stu-id="6e2dd-103">Validates a probe URL.</span></span>

## <span data-ttu-id="6e2dd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6e2dd-104">SYNTAX</span></span>

```
Confirm-AzCdnEndpointProbeURL -ProbeUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6e2dd-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6e2dd-105">DESCRIPTION</span></span>
<span data-ttu-id="6e2dd-106">Il cmdlet **Confirm-AzCdnEndpointProbeURL** verifica se l'URL personale fornito può essere usato per l'accelerazione dinamica del sito.</span><span class="sxs-lookup"><span data-stu-id="6e2dd-106">The **Confirm-AzCdnEndpointProbeURL** cmdlet confirms if the probe URL provided can be used for dynamic site acceleration.</span></span>

## <span data-ttu-id="6e2dd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6e2dd-107">EXAMPLES</span></span>

### <span data-ttu-id="6e2dd-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6e2dd-108">Example 1</span></span>
```powershell
PS C:\> Confirm-AzCdnEndpointProbeURL -ProbeUrl "http://www.bing.com/images"
IsValid: true
ErrorCode: None
Message:
```

<span data-ttu-id="6e2dd-109">Convalida l'URL url " http://www.bing.com/images " "</span><span class="sxs-lookup"><span data-stu-id="6e2dd-109">Validates the probe url "http://www.bing.com/images"</span></span>

## <span data-ttu-id="6e2dd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e2dd-110">PARAMETERS</span></span>

### <span data-ttu-id="6e2dd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e2dd-111">-DefaultProfile</span></span>
<span data-ttu-id="6e2dd-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6e2dd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e2dd-113">-UrlUrl</span><span class="sxs-lookup"><span data-stu-id="6e2dd-113">-ProbeUrl</span></span>
<span data-ttu-id="6e2dd-114">Nome URL proposte per l'URL da convalidare.</span><span class="sxs-lookup"><span data-stu-id="6e2dd-114">Proposed probe URL name to validate.</span></span>

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

### <span data-ttu-id="6e2dd-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e2dd-115">CommonParameters</span></span>
<span data-ttu-id="6e2dd-116">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e2dd-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e2dd-117">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6e2dd-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e2dd-118">INPUT</span><span class="sxs-lookup"><span data-stu-id="6e2dd-118">INPUTS</span></span>

### <span data-ttu-id="6e2dd-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6e2dd-119">None</span></span>

## <span data-ttu-id="6e2dd-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6e2dd-120">OUTPUTS</span></span>

### <span data-ttu-id="6e2dd-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span><span class="sxs-lookup"><span data-stu-id="6e2dd-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span></span>

## <span data-ttu-id="6e2dd-122">NOTE</span><span class="sxs-lookup"><span data-stu-id="6e2dd-122">NOTES</span></span>

## <span data-ttu-id="6e2dd-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6e2dd-123">RELATED LINKS</span></span>
