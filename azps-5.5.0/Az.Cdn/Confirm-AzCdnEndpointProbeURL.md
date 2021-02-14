---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/confirm-azcdnendpointprobeurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
ms.openlocfilehash: dcd45719754cc8bbb3ef45d8aa9927ae30156937
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181886"
---
# <span data-ttu-id="99a5c-101">Confirm-AzCdnEndpointProbeURL</span><span class="sxs-lookup"><span data-stu-id="99a5c-101">Confirm-AzCdnEndpointProbeURL</span></span>

## <span data-ttu-id="99a5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99a5c-102">SYNOPSIS</span></span>
<span data-ttu-id="99a5c-103">Convalida un URL valido.</span><span class="sxs-lookup"><span data-stu-id="99a5c-103">Validates a probe URL.</span></span>

## <span data-ttu-id="99a5c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="99a5c-104">SYNTAX</span></span>

```
Confirm-AzCdnEndpointProbeURL -ProbeUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="99a5c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="99a5c-105">DESCRIPTION</span></span>
<span data-ttu-id="99a5c-106">Il cmdlet **Confirm-AzCdnEndpointProbeURL** verifica se l'URL personale fornito può essere usato per l'accelerazione dinamica del sito.</span><span class="sxs-lookup"><span data-stu-id="99a5c-106">The **Confirm-AzCdnEndpointProbeURL** cmdlet confirms if the probe URL provided can be used for dynamic site acceleration.</span></span>

## <span data-ttu-id="99a5c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="99a5c-107">EXAMPLES</span></span>

### <span data-ttu-id="99a5c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="99a5c-108">Example 1</span></span>
```powershell
PS C:\> Confirm-AzCdnEndpointProbeURL -ProbeUrl "http://www.bing.com/images"
IsValid: true
ErrorCode: None
Message:
```

<span data-ttu-id="99a5c-109">Convalida l'URL url " http://www.bing.com/images " "</span><span class="sxs-lookup"><span data-stu-id="99a5c-109">Validates the probe url "http://www.bing.com/images"</span></span>

## <span data-ttu-id="99a5c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99a5c-110">PARAMETERS</span></span>

### <span data-ttu-id="99a5c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99a5c-111">-DefaultProfile</span></span>
<span data-ttu-id="99a5c-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="99a5c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99a5c-113">-UrlUrl</span><span class="sxs-lookup"><span data-stu-id="99a5c-113">-ProbeUrl</span></span>
<span data-ttu-id="99a5c-114">Nome URL proposte per l'URL da convalidare.</span><span class="sxs-lookup"><span data-stu-id="99a5c-114">Proposed probe URL name to validate.</span></span>

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

### <span data-ttu-id="99a5c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99a5c-115">CommonParameters</span></span>
<span data-ttu-id="99a5c-116">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99a5c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99a5c-117">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="99a5c-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99a5c-118">INPUT</span><span class="sxs-lookup"><span data-stu-id="99a5c-118">INPUTS</span></span>

### <span data-ttu-id="99a5c-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="99a5c-119">None</span></span>

## <span data-ttu-id="99a5c-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="99a5c-120">OUTPUTS</span></span>

### <span data-ttu-id="99a5c-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span><span class="sxs-lookup"><span data-stu-id="99a5c-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span></span>

## <span data-ttu-id="99a5c-122">NOTE</span><span class="sxs-lookup"><span data-stu-id="99a5c-122">NOTES</span></span>

## <span data-ttu-id="99a5c-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="99a5c-123">RELATED LINKS</span></span>
