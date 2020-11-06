---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/confirm-azurermcdnendpointprobeurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Confirm-AzureRmCdnEndpointProbeURL.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Confirm-AzureRmCdnEndpointProbeURL.md
ms.openlocfilehash: d6cf25c352c89592112aaa0a60cf7ba14ff7acf3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517548"
---
# <span data-ttu-id="de773-101">Confirm-AzureRmCdnEndpointProbeURL</span><span class="sxs-lookup"><span data-stu-id="de773-101">Confirm-AzureRmCdnEndpointProbeURL</span></span>

## <span data-ttu-id="de773-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="de773-102">SYNOPSIS</span></span>
<span data-ttu-id="de773-103">Convalida un URL probe.</span><span class="sxs-lookup"><span data-stu-id="de773-103">Validates a probe URL.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de773-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="de773-104">SYNTAX</span></span>

```
Confirm-AzureRmCdnEndpointProbeURL -ProbeUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="de773-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="de773-105">DESCRIPTION</span></span>
<span data-ttu-id="de773-106">Il cmdlet **Confirm-AzureRmCdnEndpointProbeURL** conferma se l'URL probe fornito può essere usato per l'accelerazione dinamica del sito.</span><span class="sxs-lookup"><span data-stu-id="de773-106">The **Confirm-AzureRmCdnEndpointProbeURL** cmdlet confirms if the probe URL provided can be used for dynamic site acceleration.</span></span>

## <span data-ttu-id="de773-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="de773-107">EXAMPLES</span></span>

### <span data-ttu-id="de773-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="de773-108">Example 1</span></span>
```powershell
PS C:\> Confirm-AzureRmCdnEndpointProbeURL -ProbeUrl "http://www.bing.com/images"
IsValid: true
ErrorCode: None
Message:
```

<span data-ttu-id="de773-109">Convalida l'URL probe " http://www.bing.com/images "</span><span class="sxs-lookup"><span data-stu-id="de773-109">Validates the probe url "http://www.bing.com/images"</span></span>

## <span data-ttu-id="de773-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="de773-110">PARAMETERS</span></span>

### <span data-ttu-id="de773-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de773-111">-DefaultProfile</span></span>
<span data-ttu-id="de773-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="de773-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de773-113">-ProbeUrl</span><span class="sxs-lookup"><span data-stu-id="de773-113">-ProbeUrl</span></span>
<span data-ttu-id="de773-114">Nome URL sonda proposto da convalidare.</span><span class="sxs-lookup"><span data-stu-id="de773-114">Proposed probe URL name to validate.</span></span>

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

### <span data-ttu-id="de773-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de773-115">CommonParameters</span></span>
<span data-ttu-id="de773-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de773-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de773-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de773-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de773-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="de773-118">INPUTS</span></span>

### <span data-ttu-id="de773-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="de773-119">None</span></span>

## <span data-ttu-id="de773-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="de773-120">OUTPUTS</span></span>

### <span data-ttu-id="de773-121">Microsoft. Azure. Commands. CDN. Models. endpoint. PSValidateProbeOutput</span><span class="sxs-lookup"><span data-stu-id="de773-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span></span>

## <span data-ttu-id="de773-122">Note</span><span class="sxs-lookup"><span data-stu-id="de773-122">NOTES</span></span>

## <span data-ttu-id="de773-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="de773-123">RELATED LINKS</span></span>
