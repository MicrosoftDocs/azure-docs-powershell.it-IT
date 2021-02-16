---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprobehealthresponsematch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
ms.openlocfilehash: edc0309b5e1a0c8b17d400e965074d38ca02bb80
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202898"
---
# <span data-ttu-id="1e1cf-101">New-AzApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="1e1cf-101">New-AzApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="1e1cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e1cf-102">SYNOPSIS</span></span>
<span data-ttu-id="1e1cf-103">Crea una corrispondenza di risposta di integrità risposta usata da Health Gateway per un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="1e1cf-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="1e1cf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1e1cf-104">SYNTAX</span></span>

```
New-AzApplicationGatewayProbeHealthResponseMatch [-Body <String>] [-StatusCode <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e1cf-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1e1cf-105">DESCRIPTION</span></span>
<span data-ttu-id="1e1cf-106">Il cmdlet **Add-AzApplicationGatewayProbeHealthResponseMatch crea** una corrispondenza health response usata da Health Istanza per un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="1e1cf-106">**The Add-AzApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="1e1cf-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1e1cf-107">EXAMPLES</span></span>

### <span data-ttu-id="1e1cf-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1e1cf-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="1e1cf-109">Questo comando crea una corrispondenza della risposta all'integrità che può essere passata aConfig come parametro.</span><span class="sxs-lookup"><span data-stu-id="1e1cf-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="1e1cf-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e1cf-110">PARAMETERS</span></span>

### <span data-ttu-id="1e1cf-111">-Body</span><span class="sxs-lookup"><span data-stu-id="1e1cf-111">-Body</span></span>
<span data-ttu-id="1e1cf-112">Corpo che deve essere contenuto nella risposta all'integrità.</span><span class="sxs-lookup"><span data-stu-id="1e1cf-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="1e1cf-113">Il valore predefinito è vuoto</span><span class="sxs-lookup"><span data-stu-id="1e1cf-113">Default value is empty</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e1cf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e1cf-114">-DefaultProfile</span></span>
<span data-ttu-id="1e1cf-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1e1cf-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e1cf-116">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="1e1cf-116">-StatusCode</span></span>
<span data-ttu-id="1e1cf-117">Intervalli consentiti di codici di stato integri. L'intervallo predefinito di codici di stato integri è 200 - 399</span><span class="sxs-lookup"><span data-stu-id="1e1cf-117">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e1cf-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e1cf-118">CommonParameters</span></span>
<span data-ttu-id="1e1cf-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e1cf-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e1cf-120">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e1cf-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e1cf-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="1e1cf-121">INPUTS</span></span>

### <span data-ttu-id="1e1cf-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1e1cf-122">None</span></span>

## <span data-ttu-id="1e1cf-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1e1cf-123">OUTPUTS</span></span>

### <span data-ttu-id="1e1cf-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthMatch</span><span class="sxs-lookup"><span data-stu-id="1e1cf-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="1e1cf-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="1e1cf-125">NOTES</span></span>

## <span data-ttu-id="1e1cf-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1e1cf-126">RELATED LINKS</span></span>
