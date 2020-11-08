---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/confirm-azcdnendpointprobeurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
ms.openlocfilehash: dcd45719754cc8bbb3ef45d8aa9927ae30156937
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202679"
---
# <span data-ttu-id="e5596-101">Confirm-AzCdnEndpointProbeURL</span><span class="sxs-lookup"><span data-stu-id="e5596-101">Confirm-AzCdnEndpointProbeURL</span></span>

## <span data-ttu-id="e5596-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e5596-102">SYNOPSIS</span></span>
<span data-ttu-id="e5596-103">Convalida un URL probe.</span><span class="sxs-lookup"><span data-stu-id="e5596-103">Validates a probe URL.</span></span>

## <span data-ttu-id="e5596-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e5596-104">SYNTAX</span></span>

```
Confirm-AzCdnEndpointProbeURL -ProbeUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e5596-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e5596-105">DESCRIPTION</span></span>
<span data-ttu-id="e5596-106">Il cmdlet **Confirm-AzCdnEndpointProbeURL** conferma se l'URL probe fornito può essere usato per l'accelerazione dinamica del sito.</span><span class="sxs-lookup"><span data-stu-id="e5596-106">The **Confirm-AzCdnEndpointProbeURL** cmdlet confirms if the probe URL provided can be used for dynamic site acceleration.</span></span>

## <span data-ttu-id="e5596-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e5596-107">EXAMPLES</span></span>

### <span data-ttu-id="e5596-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e5596-108">Example 1</span></span>
```powershell
PS C:\> Confirm-AzCdnEndpointProbeURL -ProbeUrl "http://www.bing.com/images"
IsValid: true
ErrorCode: None
Message:
```

<span data-ttu-id="e5596-109">Convalida l'URL probe " http://www.bing.com/images "</span><span class="sxs-lookup"><span data-stu-id="e5596-109">Validates the probe url "http://www.bing.com/images"</span></span>

## <span data-ttu-id="e5596-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e5596-110">PARAMETERS</span></span>

### <span data-ttu-id="e5596-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5596-111">-DefaultProfile</span></span>
<span data-ttu-id="e5596-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e5596-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5596-113">-ProbeUrl</span><span class="sxs-lookup"><span data-stu-id="e5596-113">-ProbeUrl</span></span>
<span data-ttu-id="e5596-114">Nome URL sonda proposto da convalidare.</span><span class="sxs-lookup"><span data-stu-id="e5596-114">Proposed probe URL name to validate.</span></span>

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

### <span data-ttu-id="e5596-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5596-115">CommonParameters</span></span>
<span data-ttu-id="e5596-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5596-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5596-117">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5596-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5596-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e5596-118">INPUTS</span></span>

### <span data-ttu-id="e5596-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e5596-119">None</span></span>

## <span data-ttu-id="e5596-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e5596-120">OUTPUTS</span></span>

### <span data-ttu-id="e5596-121">Microsoft. Azure. Commands. CDN. Models. endpoint. PSValidateProbeOutput</span><span class="sxs-lookup"><span data-stu-id="e5596-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span></span>

## <span data-ttu-id="e5596-122">Note</span><span class="sxs-lookup"><span data-stu-id="e5596-122">NOTES</span></span>

## <span data-ttu-id="e5596-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e5596-123">RELATED LINKS</span></span>
